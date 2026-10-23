# Zippendo.Api.AddressesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAddress**](AddressesApi.md#createaddress) | **POST** /orgs/{orgId}/addresses | Create address |
| [**DeleteAddress**](AddressesApi.md#deleteaddress) | **DELETE** /orgs/{orgId}/addresses/{addressId} | Delete address |
| [**GetAddress**](AddressesApi.md#getaddress) | **GET** /orgs/{orgId}/addresses/{addressId} | Get address |
| [**ListAddresses**](AddressesApi.md#listaddresses) | **GET** /orgs/{orgId}/addresses | List addresses |
| [**UpdateAddress**](AddressesApi.md#updateaddress) | **PUT** /orgs/{orgId}/addresses/{addressId} | Update address |

<a id="createaddress"></a>
# **CreateAddress**
> ListAddresses200ResponseDataInner CreateAddress (string orgId, CreateAddressRequest createAddressRequest)

Create address

Creates a new sender, pickup or return address for the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createAddressRequest** | [**CreateAddressRequest**](CreateAddressRequest.md) |  |  |

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)

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

<a id="deleteaddress"></a>
# **DeleteAddress**
> string DeleteAddress (string orgId, string addressId)

Delete address

Deletes an address belonging to the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **addressId** | **string** | Address ID |  |

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

<a id="getaddress"></a>
# **GetAddress**
> ListAddresses200ResponseDataInner GetAddress (string orgId, string addressId)

Get address

Returns a single address belonging to the organization, identified by its ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **addressId** | **string** | Address ID |  |

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)

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

<a id="listaddresses"></a>
# **ListAddresses**
> ListAddresses200Response ListAddresses (string orgId, int page = null, int limit = null, string type = null, string countryCode = null, string search = null, string brandId = null, string brandScope = null)

List addresses

Returns a paginated list of addresses for the organization, optionally filtered by type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |
| **type** | **string** | Filter by address type (sender, pickup, return) | [optional]  |
| **countryCode** | **string** | Filter by ISO 3166-1 alpha-2 country code. | [optional]  |
| **search** | **string** | Search by company name, description, contact or city. | [optional]  |
| **brandId** | **string** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional]  |
| **brandScope** | **string** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional]  |

### Return type

[**ListAddresses200Response**](ListAddresses200Response.md)

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

<a id="updateaddress"></a>
# **UpdateAddress**
> ListAddresses200ResponseDataInner UpdateAddress (string orgId, string addressId, UpdateAddressRequest updateAddressRequest)

Update address

Updates an existing address belonging to the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **addressId** | **string** | Address ID |  |
| **updateAddressRequest** | [**UpdateAddressRequest**](UpdateAddressRequest.md) |  |  |

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)

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

