# Zippendo.Api.OrgsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteOrgLogo**](OrgsApi.md#deleteorglogo) | **DELETE** /orgs/{orgId}/branding/logo | Delete org logo |
| [**GetOrg**](OrgsApi.md#getorg) | **GET** /orgs/{id} | Get org |
| [**GetOrgBranding**](OrgsApi.md#getorgbranding) | **GET** /orgs/{orgId}/branding | Get org branding |
| [**GetOrgLogo**](OrgsApi.md#getorglogo) | **GET** /orgs/{orgId}/branding/logo | Download org logo |
| [**UpdateOrg**](OrgsApi.md#updateorg) | **PUT** /orgs/{id} | Update org |
| [**UpdateOrgBranding**](OrgsApi.md#updateorgbranding) | **PUT** /orgs/{orgId}/branding | Update org branding |
| [**UploadOrgLogo**](OrgsApi.md#uploadorglogo) | **POST** /orgs/{orgId}/branding/logo | Upload org logo |

<a id="deleteorglogo"></a>
# **DeleteOrgLogo**
> GetOrgBranding200Response DeleteOrgLogo (string orgId)

Delete org logo

Removes the org logo. Requires the customBranding entitlement.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getorg"></a>
# **GetOrg**
> GetOrg200Response GetOrg (string id)

Get org

Returns a specific organization by ID, including its member count.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Resource ID |  |

### Return type

[**GetOrg200Response**](GetOrg200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getorgbranding"></a>
# **GetOrgBranding**
> GetOrgBranding200Response GetOrgBranding (string orgId)

Get org branding

Returns the org's brand colors and an authenticated URL to download the logo.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getorglogo"></a>
# **GetOrgLogo**
> System.IO.Stream GetOrgLogo (string orgId)

Download org logo

Returns the org logo image bytes with the stored content type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |

### Return type

**System.IO.Stream**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/png, image/jpeg, image/webp


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The logo image bytes |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateorg"></a>
# **UpdateOrg**
> UpdateOrg200Response UpdateOrg (string id, UpdateOrgRequest updateOrgRequest)

Update org

Updates an existing organization's profile, billing, and customs settings.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Resource ID |  |
| **updateOrgRequest** | [**UpdateOrgRequest**](UpdateOrgRequest.md) |  |  |

### Return type

[**UpdateOrg200Response**](UpdateOrg200Response.md)

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

<a id="updateorgbranding"></a>
# **UpdateOrgBranding**
> GetOrgBranding200Response UpdateOrgBranding (string orgId, UpdateOrgBrandingRequest updateOrgBrandingRequest)

Update org branding

Sets the org brand colors. Requires the customBranding entitlement.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **updateOrgBrandingRequest** | [**UpdateOrgBrandingRequest**](UpdateOrgBrandingRequest.md) |  |  |

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)

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

<a id="uploadorglogo"></a>
# **UploadOrgLogo**
> GetOrgBranding200Response UploadOrgLogo (string orgId, System.IO.Stream file)

Upload org logo

Uploads the org logo as multipart/form-data. Accepts PNG, JPG, or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Requires the customBranding entitlement.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **file** | **System.IO.Stream****System.IO.Stream** | Image file (PNG, JPG, or WEBP) |  |

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **413** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

