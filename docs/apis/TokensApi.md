# Zippendo.Api.TokensApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateApiToken**](TokensApi.md#createapitoken) | **POST** /orgs/{orgId}/api-tokens | Create API keys |
| [**GetApiToken**](TokensApi.md#getapitoken) | **GET** /orgs/{orgId}/api-tokens/{tokenId} | Get API keys |
| [**ListApiTokens**](TokensApi.md#listapitokens) | **GET** /orgs/{orgId}/api-tokens | List API keys |
| [**RevokeApiToken**](TokensApi.md#revokeapitoken) | **DELETE** /orgs/{orgId}/api-tokens/{tokenId} | Revoke API keys |
| [**UpdateApiToken**](TokensApi.md#updateapitoken) | **PATCH** /orgs/{orgId}/api-tokens/{tokenId} | Update API keys |
| [**VerifyApiToken**](TokensApi.md#verifyapitoken) | **POST** /api-tokens/verify | Verify API keys |

<a id="createapitoken"></a>
# **CreateApiToken**
> CreateApiToken201Response CreateApiToken (string orgId, CreateApiTokenRequest createApiTokenRequest)

Create API keys

Creates a new API token for the specified organization. The full token is only shown once.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createApiTokenRequest** | [**CreateApiTokenRequest**](CreateApiTokenRequest.md) |  |  |

### Return type

[**CreateApiToken201Response**](CreateApiToken201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getapitoken"></a>
# **GetApiToken**
> ListApiTokens200ResponseDataInner GetApiToken (string orgId, string tokenId)

Get API keys

Returns metadata for a specific API token. The token secret is never returned.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **tokenId** | **string** | API Token ID |  |

### Return type

[**ListApiTokens200ResponseDataInner**](ListApiTokens200ResponseDataInner.md)

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
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listapitokens"></a>
# **ListApiTokens**
> ListApiTokens200Response ListApiTokens (string orgId, int page = null, int limit = null)

List API keys

Returns a paginated list of API tokens belonging to the specified organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |

### Return type

[**ListApiTokens200Response**](ListApiTokens200Response.md)

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

<a id="revokeapitoken"></a>
# **RevokeApiToken**
> RevokeApiToken200Response RevokeApiToken (string orgId, string tokenId)

Revoke API keys

Revokes and deletes an API token.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **tokenId** | **string** | API Token ID |  |

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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateapitoken"></a>
# **UpdateApiToken**
> ListApiTokens200ResponseDataInner UpdateApiToken (string orgId, string tokenId, UpdateApiTokenRequest updateApiTokenRequest)

Update API keys

Updates the name of an API token.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **tokenId** | **string** | API Token ID |  |
| **updateApiTokenRequest** | [**UpdateApiTokenRequest**](UpdateApiTokenRequest.md) |  |  |

### Return type

[**ListApiTokens200ResponseDataInner**](ListApiTokens200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="verifyapitoken"></a>
# **VerifyApiToken**
> VerifyApiToken200Response VerifyApiToken (VerifyApiTokenRequest verifyApiTokenRequest)

Verify API keys

Verifies whether an API token is valid and returns its metadata.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **verifyApiTokenRequest** | [**VerifyApiTokenRequest**](VerifyApiTokenRequest.md) |  |  |

### Return type

[**VerifyApiToken200Response**](VerifyApiToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

