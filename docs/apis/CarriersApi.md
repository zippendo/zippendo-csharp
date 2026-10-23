# Zippendo.Api.CarriersApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ConnectCarrier**](CarriersApi.md#connectcarrier) | **POST** /orgs/{orgId}/carriers | Connect carrier |
| [**DisconnectCarrier**](CarriersApi.md#disconnectcarrier) | **DELETE** /orgs/{orgId}/carriers/{carrierId} | Disconnect carrier |
| [**GetCarrier**](CarriersApi.md#getcarrier) | **GET** /orgs/{orgId}/carriers/{carrierId} | Get carrier |
| [**ListCarrierProductServicePoints**](CarriersApi.md#listcarrierproductservicepoints) | **POST** /orgs/{orgId}/carriers/{carrierId}/products/{productId}/service-points | List product service points |
| [**ListCarrierProducts**](CarriersApi.md#listcarrierproducts) | **GET** /orgs/{orgId}/carriers/{carrierId}/products | List carrier products |
| [**ListCarriers**](CarriersApi.md#listcarriers) | **GET** /orgs/{orgId}/carriers | List carriers |
| [**UpdateCarrier**](CarriersApi.md#updatecarrier) | **PUT** /orgs/{orgId}/carriers/{carrierId} | Update carrier |

<a id="connectcarrier"></a>
# **ConnectCarrier**
> ListCarriers200ResponseDataInner ConnectCarrier (string orgId, ConnectCarrierRequest connectCarrierRequest)

Connect carrier

Connects a new carrier to the organization with its configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **connectCarrierRequest** | [**ConnectCarrierRequest**](ConnectCarrierRequest.md) |  |  |

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="disconnectcarrier"></a>
# **DisconnectCarrier**
> string DisconnectCarrier (string orgId, string carrierId)

Disconnect carrier

Disconnects a carrier from the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **carrierId** | **string** | Carrier ID |  |

### Return type

**string**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcarrier"></a>
# **GetCarrier**
> ListCarriers200ResponseDataInner GetCarrier (string orgId, string carrierId)

Get carrier

Returns a single connected carrier.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **carrierId** | **string** | Carrier ID |  |

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)

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

<a id="listcarrierproductservicepoints"></a>
# **ListCarrierProductServicePoints**
> List&lt;ListCarrierProductServicePoints200ResponseInner&gt; ListCarrierProductServicePoints (string orgId, string carrierId, string productId, ListCarrierProductServicePointsRequest listCarrierProductServicePointsRequest)

List product service points

Returns pickup service points near a location for a specific carrier product.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **carrierId** | **string** | Carrier ID |  |
| **productId** | **string** | Carrier product ID |  |
| **listCarrierProductServicePointsRequest** | [**ListCarrierProductServicePointsRequest**](ListCarrierProductServicePointsRequest.md) |  |  |

### Return type

[**List&lt;ListCarrierProductServicePoints200ResponseInner&gt;**](ListCarrierProductServicePoints200ResponseInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listcarrierproducts"></a>
# **ListCarrierProducts**
> List&lt;ListCarrierProducts200ResponseInner&gt; ListCarrierProducts (string orgId, string carrierId)

List carrier products

Returns the carrier products available for a connected carrier.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **carrierId** | **string** | Carrier ID |  |

### Return type

[**List&lt;ListCarrierProducts200ResponseInner&gt;**](ListCarrierProducts200ResponseInner.md)

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

<a id="listcarriers"></a>
# **ListCarriers**
> ListCarriers200Response ListCarriers (string orgId, int page = null, int limit = null, string brandId = null, string brandScope = null, string carrierSlug = null, string search = null)

List carriers

Returns a paginated list of carriers connected to the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **string** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional]  |
| **brandScope** | **string** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional]  |
| **carrierSlug** | **string** | Filter by carrier slug. | [optional]  |
| **search** | **string** | Search by carrier name. | [optional]  |

### Return type

[**ListCarriers200Response**](ListCarriers200Response.md)

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatecarrier"></a>
# **UpdateCarrier**
> ListCarriers200ResponseDataInner UpdateCarrier (string orgId, string carrierId, UpdateCarrierRequest updateCarrierRequest)

Update carrier

Updates a connected carrier's configuration or name.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **carrierId** | **string** | Carrier ID |  |
| **updateCarrierRequest** | [**UpdateCarrierRequest**](UpdateCarrierRequest.md) |  |  |

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)

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

