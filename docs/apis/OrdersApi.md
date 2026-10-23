# Zippendo.Api.OrdersApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOrder**](OrdersApi.md#createorder) | **POST** /orgs/{orgId}/orders | Create order |
| [**DeleteOrder**](OrdersApi.md#deleteorder) | **DELETE** /orgs/{orgId}/orders/{orderId} | Delete order |
| [**GetOrder**](OrdersApi.md#getorder) | **GET** /orgs/{orgId}/orders/{orderId} | Get order |
| [**ListOrders**](OrdersApi.md#listorders) | **GET** /orgs/{orgId}/orders | List orders |
| [**UpdateOrder**](OrdersApi.md#updateorder) | **PATCH** /orgs/{orgId}/orders/{orderId} | Update order |

<a id="createorder"></a>
# **CreateOrder**
> CreateOrder201Response CreateOrder (string orgId, CreateOrderRequest createOrderRequest)

Create order

Creates a new order under an existing order channel for the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createOrderRequest** | [**CreateOrderRequest**](CreateOrderRequest.md) |  |  |

### Return type

[**CreateOrder201Response**](CreateOrder201Response.md)

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
| **404** | Default Response |  -  |
| **409** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteorder"></a>
# **DeleteOrder**
> RevokeApiToken200Response DeleteOrder (string orgId, string orderId)

Delete order

Deletes an order. Fails if the order has associated shipments.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **orderId** | **string** | Order ID. |  |

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

<a id="getorder"></a>
# **GetOrder**
> GetOrder200Response GetOrder (string orgId, string orderId)

Get order

Returns a single order with its channel, shipping rule, shipments, and documents.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **orderId** | **string** | Order ID. |  |

### Return type

[**GetOrder200Response**](GetOrder200Response.md)

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

<a id="listorders"></a>
# **ListOrders**
> ListOrders200Response ListOrders (string orgId, int page = null, int limit = null, string brandId = null, string brandScope = null, string status = null, string orderChannelId = null, string search = null, string filter = null)

List orders

Returns a paginated list of orders for an organization, filterable by status, channel, search term and an advanced filter definition.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **string** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional]  |
| **brandScope** | **string** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional]  |
| **status** | **string** | Order fulfillment status derived from its shipments. | [optional]  |
| **orderChannelId** | **string** | Filter by order channel ID. | [optional]  |
| **search** | **string** | Search by order number or customer name/email. | [optional]  |
| **filter** | **string** | Advanced filter as a JSON-encoded definition: a &#x60;conjunction&#x60; (&#x60;and&#x60;/&#x60;or&#x60;) over &#x60;conditions&#x60;, each &#x60;{ id, field, operator, value }&#x60; or a nested group. Fields and operators per list are documented under Filtering lists in the API overview. An invalid filter returns 400 &#x60;FILTER_INVALID&#x60;. | [optional]  |

### Return type

[**ListOrders200Response**](ListOrders200Response.md)

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

<a id="updateorder"></a>
# **UpdateOrder**
> CreateOrder201Response UpdateOrder (string orgId, string orderId, UpdateOrderRequest updateOrderRequest)

Update order

Updates an order that is not yet fulfilled or cancelled.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID. |  |
| **orderId** | **string** | Order ID. |  |
| **updateOrderRequest** | [**UpdateOrderRequest**](UpdateOrderRequest.md) |  |  |

### Return type

[**CreateOrder201Response**](CreateOrder201Response.md)

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

