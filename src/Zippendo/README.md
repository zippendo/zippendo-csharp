# Created with Openapi Generator

<a id="cli"></a>
## Creating the library
Create a config.yaml file similar to what is below, then run the following powershell command to generate the library `java -jar "<path>/openapi-generator/modules/openapi-generator-cli/target/openapi-generator-cli.jar" generate -c config.yaml`

```yaml
generatorName: csharp
inputSpec: /local/openapi.csharp.json
outputDir: out

# https://openapi-generator.tech/docs/generators/csharp
additionalProperties:
  packageGuid: '{EAC7F58E-7778-4A26-A629-6CB91B88CD79}'

# https://openapi-generator.tech/docs/integrations/#github-integration
# gitHost:
# gitUserId:
# gitRepoId:

# https://openapi-generator.tech/docs/globals
# globalProperties:

# https://openapi-generator.tech/docs/customization/#inline-schema-naming
# inlineSchemaOptions:

# https://openapi-generator.tech/docs/customization/#name-mapping
# modelNameMappings:
# nameMappings:

# https://openapi-generator.tech/docs/customization/#openapi-normalizer
# openapiNormalizer:

# templateDir: https://openapi-generator.tech/docs/templating/#modifying-templates

# releaseNote:
```

<a id="usage"></a>
## Using the library in your project

```cs
using Microsoft.Extensions.Hosting;
using Microsoft.Extensions.DependencyInjection;
using Zippendo.Api;
using Zippendo.Client;
using Zippendo.Model;
using Org.OpenAPITools.Extensions;

namespace YourProject
{
    public class Program
    {
        public static async Task Main(string[] args)
        {
            var host = CreateHostBuilder(args).Build();
            var api = host.Services.GetRequiredService<IAddressesApi>();
            ICreateAddressApiResponse apiResponse = await api.CreateAddressAsync("todo");
            ListAddresses200ResponseDataInner? model = apiResponse.Ok();
        }

        public static IHostBuilder CreateHostBuilder(string[] args) => Host.CreateDefaultBuilder(args)
          .ConfigureApi((context, options) =>
          {
              // The type of token here depends on the api security specifications
              // Available token types are ApiKeyToken, BasicToken, BearerToken, HttpSigningToken, and OAuthToken.
              BearerToken token = new("<your token>");
              options.AddTokens(token);

              // optionally choose the method the tokens will be provided with, default is RateLimitProvider
              options.UseProvider<RateLimitProvider<BearerToken>, BearerToken>();

              options.ConfigureJsonOptions((jsonOptions) =>
              {
                  // your custom converters if any
              });

              options.AddApiHttpClients(client =>
              {
                  // client configuration
              }, builder =>
              {
                  builder
                      .AddRetryPolicy(2)
                      .AddTimeoutPolicy(TimeSpan.FromSeconds(5))
                      .AddCircuitBreakerPolicy(10, TimeSpan.FromSeconds(30));
                      // add whatever middleware you prefer
                  }
              );
          });
    }
}
```
<a id="questions"></a>
## Questions

- What about HttpRequest failures and retries?
  Configure Polly in the IHttpClientBuilder
- How are tokens used?
  Tokens are provided by a TokenProvider class. The default is RateLimitProvider which will perform client side rate limiting.
  Other providers can be used with the UseProvider method.
- Does an HttpRequest throw an error when the server response is not Ok?
  It depends how you made the request. If the return type is ApiResponse<T> no error will be thrown, though the Content property will be null.
  StatusCode and ReasonPhrase will contain information about the error.
  If the return type is T, then it will throw. If the return type is TOrDefault, it will return null.
- How do I validate requests and process responses?
  Use the provided On and After partial methods in the api classes.

## Api Information
- appName: Zippendo Public API
- appVersion: 1.0.0
- appDescription: Public API documentation for Zippendo. Authenticate using your API token (Bearer token prefixed with zipp_).  **Brands (sub-accounts).** An organization can be split into brands, each keeping its own orders, shipments and configuration separate. There are two ways to scope requests to one brand, and NEITHER changes any request body:  1. **Bind the token.** Create an API token with a &#x60;brandId&#x60; and every request it makes is confined    to that brand — reads filtered, writes stamped. This is the recommended way to give a single    brand&#39;s team its own credential. 2. **Send the &#x60;X-Zippendo-Brand&#x60; header.** An organization-wide token can scope an individual    request by sending the brand&#39;s id or slug in this header. Most SDKs let you set it once on the    client so every call inherits it.  A brand-bound token that receives an &#x60;X-Zippendo-Brand&#x60; header naming a different brand is rejected with &#x60;403 BRAND_ACCESS_DENIED&#x60; — the binding is never widened. Omit both and requests cover the whole organization, which is the behaviour of every existing token.  Records that belong to no brand carry &#x60;brandId: null&#x60;. Configuration (carriers, shipping rules, addresses) with a null brand is organization-wide and remains visible inside every brand; orders and shipments with a null brand are only visible organization-wide.  List endpoints additionally take a &#x60;?brandScope&#x3D;own|shared|both&#x60; parameter to narrow further within whichever brand context already applies. &#x60;own&#x60; returns only rows assigned to that brand, and requires a brand context — a brand-bound token, a resolved brand session, or the &#x60;X-Zippendo-Brand&#x60; header above — otherwise &#x60;400&#x60;. &#x60;shared&#x60; returns only the organization-wide rows (equivalent to filtering &#x60;brandId&#x3D;none&#x60;). The default, &#x60;both&#x60;, keeps the existing behaviour: a brand context sees its own rows plus the organization-wide ones. Set &#x60;X-Zippendo-Brand-Scope&#x60; as a client default to apply the same choice to every request instead of repeating the query parameter on each call — an explicit &#x60;brandScope&#x60; query parameter always wins over the header, and a blank header value is ignored.  Brands themselves are managed under the **Brands** tag. Retiring a brand is done with &#x60;POST /orgs/{orgId}/brands/{brandId}/archive&#x60; — permanent deletion is a dashboard-only action, since it is refused while any order, shipment, member or token still references the brand. Brands require a plan that includes them; creating one beyond your plan&#39;s limit returns &#x60;403&#x60;.

## Build
This C# SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project.

- SDK version: 1.3.16
- Generator version: 7.24.0
- Build package: org.openapitools.codegen.languages.CSharpClientCodegen
