# Zippendo.Api.OrderChannelsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOrderChannel**](OrderChannelsApi.md#createorderchannel) | **POST** /orgs/{orgId}/order-channels | Create order channel |
| [**CreateOrderChannelWebhookSecret**](OrderChannelsApi.md#createorderchannelwebhooksecret) | **POST** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Create or rotate webhook signing secret |
| [**DeleteOrderChannel**](OrderChannelsApi.md#deleteorderchannel) | **DELETE** /orgs/{orgId}/order-channels/{channelId} | Delete order channel |
| [**GetOrderChannel**](OrderChannelsApi.md#getorderchannel) | **GET** /orgs/{orgId}/order-channels/{channelId} | Get order channel |
| [**GetOrderChannelWebhookStatus**](OrderChannelsApi.md#getorderchannelwebhookstatus) | **GET** /orgs/{orgId}/order-channels/{channelId}/webhooks | Get channel webhook status |
| [**ListOrderChannels**](OrderChannelsApi.md#listorderchannels) | **GET** /orgs/{orgId}/order-channels | List order channels |
| [**RevokeOrderChannelWebhookSecret**](OrderChannelsApi.md#revokeorderchannelwebhooksecret) | **DELETE** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Revoke webhook signing secret |
| [**UpdateOrderChannel**](OrderChannelsApi.md#updateorderchannel) | **PATCH** /orgs/{orgId}/order-channels/{channelId} | Update order channel |

<a id="createorderchannel"></a>
# **CreateOrderChannel**
> ListOrderChannels200ResponseDataInner CreateOrderChannel (string orgId, CreateOrderChannelRequest createOrderChannelRequest)

Create order channel

Creates a new order channel for an organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createOrderChannelRequest** | [**CreateOrderChannelRequest**](CreateOrderChannelRequest.md) |  |  |

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createorderchannelwebhooksecret"></a>
# **CreateOrderChannelWebhookSecret**
> CreateOrderChannelWebhookSecret201Response CreateOrderChannelWebhookSecret (string orgId, string channelId)

Create or rotate webhook signing secret

Generates (or rotates) the custom channel's webhook signing secret used to authenticate order pushes to the ingest URL. The secret is returned only once. Rotating invalidates the previous secret immediately.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **channelId** | **string** | Order channel ID. |  |

### Return type

[**CreateOrderChannelWebhookSecret201Response**](CreateOrderChannelWebhookSecret201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteorderchannel"></a>
# **DeleteOrderChannel**
> RevokeApiToken200Response DeleteOrderChannel (string orgId, string channelId)

Delete order channel

Deletes an order channel and cascades deletion of its orders.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **channelId** | **string** | Order channel ID. |  |

### Return type

[**RevokeApiToken200Response**](RevokeApiToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getorderchannel"></a>
# **GetOrderChannel**
> ListOrderChannels200ResponseDataInner GetOrderChannel (string orgId, string channelId)

Get order channel

Returns a single order channel by ID, including its linked shipping rules.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **channelId** | **string** | Order channel ID. |  |

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getorderchannelwebhookstatus"></a>
# **GetOrderChannelWebhookStatus**
> GetOrderChannelWebhookStatus200Response GetOrderChannelWebhookStatus (string orgId, string channelId)

Get channel webhook status

Returns whether webhooks are enabled and lists the webhooks registered with the platform.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **channelId** | **string** | Order channel ID. |  |

### Return type

[**GetOrderChannelWebhookStatus200Response**](GetOrderChannelWebhookStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listorderchannels"></a>
# **ListOrderChannels**
> ListOrderChannels200Response ListOrderChannels (string orgId, int page = null, int limit = null, string brandId = null, string brandScope = null, string type = null, string enabled = null, string search = null)

List order channels

Returns a paginated list of order channels for an organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **string** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional]  |
| **brandScope** | **string** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional]  |
| **type** | **string** | Filter by channel type. | [optional]  |
| **enabled** | **string** | Filter by enabled state. | [optional]  |
| **search** | **string** | Search by channel name. | [optional]  |

### Return type

[**ListOrderChannels200Response**](ListOrderChannels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="revokeorderchannelwebhooksecret"></a>
# **RevokeOrderChannelWebhookSecret**
> RevokeOrderChannelWebhookSecret200Response RevokeOrderChannelWebhookSecret (string orgId, string channelId)

Revoke webhook signing secret

Revokes the custom channel's webhook signing secret. All subsequent pushes to the ingest URL are rejected until a new secret is generated.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **channelId** | **string** | Order channel ID. |  |

### Return type

[**RevokeOrderChannelWebhookSecret200Response**](RevokeOrderChannelWebhookSecret200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateorderchannel"></a>
# **UpdateOrderChannel**
> ListOrderChannels200ResponseDataInner UpdateOrderChannel (string orgId, string channelId, UpdateOrderChannelRequest updateOrderChannelRequest)

Update order channel

Updates an order channel and its linked shipping rules.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **channelId** | **string** | Order channel ID. |  |
| **updateOrderChannelRequest** | [**UpdateOrderChannelRequest**](UpdateOrderChannelRequest.md) |  |  |

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

