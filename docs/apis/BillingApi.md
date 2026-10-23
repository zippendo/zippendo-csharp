# Zippendo.Api.BillingApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetBillingUsage**](BillingApi.md#getbillingusage) | **GET** /orgs/{orgId}/billing/usage | Get usage |

<a id="getbillingusage"></a>
# **GetBillingUsage**
> GetBillingUsage200Response GetBillingUsage (string orgId)

Get usage

Get detailed usage statistics for the current billing period.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |

### Return type

[**GetBillingUsage200Response**](GetBillingUsage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

