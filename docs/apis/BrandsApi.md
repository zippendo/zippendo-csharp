# Zippendo.Api.BrandsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveOrgBrand**](BrandsApi.md#archiveorgbrand) | **POST** /orgs/{orgId}/brands/{brandId}/archive | Archive brand |
| [**CheckBrandSlug**](BrandsApi.md#checkbrandslug) | **GET** /orgs/{orgId}/brands/check-slug/{slug} | Check brand slug availability |
| [**CreateOrgBrand**](BrandsApi.md#createorgbrand) | **POST** /orgs/{orgId}/brands | Create brand |
| [**DeleteBrandLogo**](BrandsApi.md#deletebrandlogo) | **DELETE** /orgs/{orgId}/brands/{brandId}/logo | Delete brand logo |
| [**GetBrandLogo**](BrandsApi.md#getbrandlogo) | **GET** /orgs/{orgId}/brands/{brandId}/logo | Get brand logo |
| [**GetOrgBrand**](BrandsApi.md#getorgbrand) | **GET** /orgs/{orgId}/brands/{brandId} | Get brand |
| [**ListOrgBrands**](BrandsApi.md#listorgbrands) | **GET** /orgs/{orgId}/brands | List brands |
| [**UnarchiveOrgBrand**](BrandsApi.md#unarchiveorgbrand) | **POST** /orgs/{orgId}/brands/{brandId}/unarchive | Unarchive brand |
| [**UpdateOrgBrand**](BrandsApi.md#updateorgbrand) | **PATCH** /orgs/{orgId}/brands/{brandId} | Update brand |
| [**UploadBrandLogo**](BrandsApi.md#uploadbrandlogo) | **POST** /orgs/{orgId}/brands/{brandId}/logo | Upload brand logo |

<a id="archiveorgbrand"></a>
# **ArchiveOrgBrand**
> ListOrgBrands200ResponseDataInner ArchiveOrgBrand (string orgId, string brandId)

Archive brand

Archives a brand: it leaves the brand switcher and default listings, but its orders, shipments and settings are retained and remain visible in the organization-wide view.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **brandId** | **string** | Brand ID |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

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

<a id="checkbrandslug"></a>
# **CheckBrandSlug**
> CheckBrandSlug200Response CheckBrandSlug (string orgId, string slug)

Check brand slug availability

Reports whether a brand slug is free within this organization. Brand slugs are unique per organization, so the same slug may exist in another organization. Archived brands still hold their slug.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **slug** | **string** | Brand slug to check |  |

### Return type

[**CheckBrandSlug200Response**](CheckBrandSlug200Response.md)

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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createorgbrand"></a>
# **CreateOrgBrand**
> ListOrgBrands200ResponseDataInner CreateOrgBrand (string orgId, CreateOrgBrandRequest createOrgBrandRequest)

Create brand

Creates a brand (sub-account) in the organization. The slug is derived from the name when omitted. Requires a plan that includes brands.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createOrgBrandRequest** | [**CreateOrgBrandRequest**](CreateOrgBrandRequest.md) |  |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

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
| **409** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletebrandlogo"></a>
# **DeleteBrandLogo**
> ListOrgBrands200ResponseDataInner DeleteBrandLogo (string orgId, string brandId)

Delete brand logo

Removes a brand's logo. Its documents fall back to the organization's logo. Requires the brands and customBranding entitlements.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **brandId** | **string** | Brand ID |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

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

<a id="getbrandlogo"></a>
# **GetBrandLogo**
> System.IO.Stream GetBrandLogo (string orgId, string brandId)

Get brand logo

Streams the brand's logo bytes. This is the URL returned as the brand's `logoUrl`.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **brandId** | **string** | Brand ID |  |

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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getorgbrand"></a>
# **GetOrgBrand**
> ListOrgBrands200ResponseDataInner GetOrgBrand (string orgId, string brandId)

Get brand

Returns a single brand (sub-account) by id.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **brandId** | **string** | Brand ID |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

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

<a id="listorgbrands"></a>
# **ListOrgBrands**
> ListOrgBrands200Response ListOrgBrands (string orgId, string includeArchived = null)

List brands

Returns the organization's brands (sub-accounts). Archived brands are excluded unless `includeArchived` is set.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **includeArchived** | **string** | Include archived brands in the response | [optional]  |

### Return type

[**ListOrgBrands200Response**](ListOrgBrands200Response.md)

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

<a id="unarchiveorgbrand"></a>
# **UnarchiveOrgBrand**
> ListOrgBrands200ResponseDataInner UnarchiveOrgBrand (string orgId, string brandId)

Unarchive brand

Restores an archived brand so it appears in the brand switcher again.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **brandId** | **string** | Brand ID |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

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

<a id="updateorgbrand"></a>
# **UpdateOrgBrand**
> ListOrgBrands200ResponseDataInner UpdateOrgBrand (string orgId, string brandId, UpdateOrgBrandRequest updateOrgBrandRequest)

Update brand

Updates a brand's name, slug, identity overrides (company name, VAT, customs, address) and document colors. Null clears an override so the organization's value applies again.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **brandId** | **string** | Brand ID |  |
| **updateOrgBrandRequest** | [**UpdateOrgBrandRequest**](UpdateOrgBrandRequest.md) |  |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

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
| **409** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="uploadbrandlogo"></a>
# **UploadBrandLogo**
> ListOrgBrands200ResponseDataInner UploadBrandLogo (string orgId, string brandId, System.IO.Stream file)

Upload brand logo

Uploads a brand's logo as multipart/form-data. Accepts PNG, JPG or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Documents for this brand's shipments use it instead of the organization's logo. Requires the brands and customBranding entitlements.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **brandId** | **string** | Brand ID |  |
| **file** | **System.IO.Stream****System.IO.Stream** | Image file (PNG, JPG, or WEBP) |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

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

