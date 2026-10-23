# Zippendo .NET SDK

Official C# client for the [Zippendo](https://zippendo.com) shipping & logistics API. Targets .NET
Standard 2.0 (so .NET Framework 4.6.1+ and every modern .NET) and .NET 10, using `HttpClient` and
`System.Text.Json` through `Microsoft.Extensions.Http`.

Book shipments and print labels with PostNord, GLS, DAO, Bring, DHL, DPD, UPS and more, track
parcels, and manage orders, shipping rules and webhooks from your own code. New to the API? Start with
the [SDK guide](https://www.zippendo.com/docs/sdks/overview) or browse the
[API reference](https://www.zippendo.com/docs/api-reference/overview). To work from an AI assistant
instead, connect the [Zippendo MCP server](https://www.zippendo.com/docs/mcp/overview).

## Install

```sh
dotnet add package Zippendo
```

## Authentication

Create an API token in your Zippendo dashboard (**Settings → API tokens**). It is a Bearer token
prefixed with `zipp_`. The clients are registered with dependency injection, so they work the same in
ASP.NET Core, a worker service or a console app:

```csharp
using Microsoft.Extensions.DependencyInjection;
using Zippendo.Api;
using Zippendo.Client;
using Zippendo.Extensions;

var services = new ServiceCollection();
services.AddLogging();
services.AddApi(options =>
{
    options.AddTokens(new BearerToken(Environment.GetEnvironmentVariable("ZIPPENDO_API_TOKEN")!));
});

var provider = services.BuildServiceProvider();
var shipments = provider.GetRequiredService<IShipmentsApi>();
```

In ASP.NET Core, call `builder.Services.AddApi(...)` the same way and inject `IShipmentsApi` where you
need it (the host already registers logging). The base URL defaults to `https://api.zippendo.com`.

## Resources & clients

The API is split into resource clients — `IShipmentsApi`, `IOrdersApi`, `ICarriersApi`,
`IAddressesApi`, `IRulesApi`, `IWebhooksApi`, `ITokensApi`, and more. `AddApi` registers all of them.

## The `orgId` parameter

Every call takes an `orgId` (your organization ID, found in the dashboard). It is explicit on each
call by design: one API token can be granted access to multiple organizations, and `orgId` selects
which one the request acts on.

## Brands

A brand is a sub-account inside an organization: one company running several consumer-facing labels
(say Acme and Globex) keeps each label's orders and shipments separate, with its own company name,
address and logo on the documents its shipments produce. Scope a request to one brand with the
`X-Zippendo-Brand` header, whose value is the brand's ID or slug.

The header is not a method parameter — it applies uniformly to every operation, so set it once on the
clients' `HttpClient` and every call inherits it:

```csharp
services.AddApi(options =>
{
    options.AddTokens(new BearerToken(token));
    options.AddApiHttpClients(client =>
    {
        // Configuring the HttpClient replaces the default that sets the base URL, so set it here too.
        client.BaseAddress = new Uri(ClientUtils.BASE_ADDRESS);
        client.DefaultRequestHeaders.Add("X-Zippendo-Brand", "acme"); // brand ID or slug
    });
});
```

To address two brands from one process, build a service provider per brand. Omit the header and the
request covers the whole organization — the behaviour of every existing token. A header naming a brand
that does not exist in the organization is rejected with `404 BRAND_NOT_FOUND`.

An API token created with a `brandId` is permanently confined to that brand and needs no header.
Sending `X-Zippendo-Brand` naming a *different* brand on such a token is refused with
`403 BRAND_ACCESS_DENIED` — the binding is never widened.

List operations also take a `brandScope` argument (`"own"` / `"shared"` / `"both"`) to narrow further
within whichever brand context already applies: `"own"` returns only that brand's rows and needs a
brand context (otherwise `400`); `"shared"` returns only the unassigned rows (equivalent to
`brandId: "none"`). Add an `X-Zippendo-Brand-Scope` default header the same way to cover every call.
An explicit `brandScope` passed to a call still wins over the header.

## Listing & pagination

List endpoints accept `page` (1-based) and `limit`, and return a page with `Data` plus `Total`,
`Page`, `Limit`, and `TotalPages`. Responses do not throw on an HTTP error, so check the result:

```csharp
var response = await shipments.ListShipmentsAsync("org_8f3kd92ld0", page: 1, limit: 50);
if (response.TryOk(out var result) && result != null)
{
    Console.WriteLine($"{result.Data.Count} of {result.Total} ({result.TotalPages} pages)");
}
```

## Creating resources

```csharp
using Zippendo.Model;

var orders = provider.GetRequiredService<IOrdersApi>();
var response = await orders.CreateOrderAsync("org_8f3kd92ld0", new CreateOrderRequest(
    orderNumber: "1001",
    orderChannelId: "chan_7d2k1",
    orderLines: new List<CreateOrderRequestOrderLinesInner>
    {
        new CreateOrderRequestOrderLinesInner(name: "T-shirt", quantity: 2)
    }));
Console.WriteLine(response.Created()?.Id);
```

See [`./docs`](./docs) for the full request/response shape of every operation.

## Error handling

A non-2xx response comes back with `IsSuccessStatusCode` false and Zippendo's canonical
`{ code, error, message }` body in `RawContent` — branch on the machine-readable `code`:

```csharp
using System.Text.Json;

var response = await shipments.GetShipmentAsync("org_8f3kd92ld0", "shp_missing");
if (!response.IsSuccessStatusCode)
{
    using var body = JsonDocument.Parse(response.RawContent);
    var code = body.RootElement.GetProperty("code").GetString();
    Console.Error.WriteLine($"{(int)response.StatusCode} {code}"); // e.g. "404 SHIPMENT_NOT_FOUND"
}
```

## Configuration

Set `client.BaseAddress` in `AddApiHttpClients` (as under [Brands](#brands)) to point at a different
environment. The second argument configures each client's `IHttpClientBuilder`, for retries and
timeouts:

```csharp
options.AddApiHttpClients(
    client => client.BaseAddress = new Uri("https://staging.api.zippendo.com"),
    builder => builder.AddRetryPolicy(2).AddTimeoutPolicy(TimeSpan.FromSeconds(30)));
```

The default token provider spaces requests made with one token at least 40 ms apart; pass a shorter
`timeout` to `BearerToken` to change that.

## Reference

Full per-endpoint and per-model documentation is in [`./docs`](./docs). Hosted reference:
<https://www.zippendo.com/docs/api-reference/overview>.

## License

[MIT](./LICENSE.md)
