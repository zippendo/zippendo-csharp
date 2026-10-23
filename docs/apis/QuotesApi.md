# Zippendo.Api.QuotesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateShippingQuote**](QuotesApi.md#createshippingquote) | **POST** /orgs/{orgId}/shipping-quote | Calculate shipping rates |

<a id="createshippingquote"></a>
# **CreateShippingQuote**
> CreateShippingQuote200Response CreateShippingQuote (string orgId, CreateShippingQuoteRequest createShippingQuoteRequest)

Calculate shipping rates

Calculates shipping rates from configured shipping rules based on cart items and destination.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createShippingQuoteRequest** | [**CreateShippingQuoteRequest**](CreateShippingQuoteRequest.md) |  |  |

### Return type

[**CreateShippingQuote200Response**](CreateShippingQuote200Response.md)

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
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

