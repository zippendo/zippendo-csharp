# Zippendo.Api.CarrierCatalogApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListAvailableCarriers**](CarrierCatalogApi.md#listavailablecarriers) | **GET** /orgs/{orgId}/available-carriers | List available carriers |

<a id="listavailablecarriers"></a>
# **ListAvailableCarriers**
> List&lt;ListAvailableCarriers200ResponseInner&gt; ListAvailableCarriers (string orgId)

List available carriers

Returns the carriers available to connect, as supported by the carrier server.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |

### Return type

[**List&lt;ListAvailableCarriers200ResponseInner&gt;**](ListAvailableCarriers200ResponseInner.md)

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
| **500** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

