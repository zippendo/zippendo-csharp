# Zippendo.Api.RulesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateShippingRule**](RulesApi.md#createshippingrule) | **POST** /orgs/{orgId}/shipping-rules | Create shipping rule |
| [**DeleteShippingRule**](RulesApi.md#deleteshippingrule) | **DELETE** /orgs/{orgId}/shipping-rules/{ruleId} | Delete shipping rule |
| [**GetShippingRule**](RulesApi.md#getshippingrule) | **GET** /orgs/{orgId}/shipping-rules/{ruleId} | Get shipping rule |
| [**ListShippingRules**](RulesApi.md#listshippingrules) | **GET** /orgs/{orgId}/shipping-rules | List shipping rules |
| [**UpdateShippingRule**](RulesApi.md#updateshippingrule) | **PATCH** /orgs/{orgId}/shipping-rules/{ruleId} | Update shipping rule |

<a id="createshippingrule"></a>
# **CreateShippingRule**
> CreateShippingRule201Response CreateShippingRule (string orgId, CreateShippingRuleRequest createShippingRuleRequest)

Create shipping rule

Creates a new shipping rule with conditions and carrier product for the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createShippingRuleRequest** | [**CreateShippingRuleRequest**](CreateShippingRuleRequest.md) |  |  |

### Return type

[**CreateShippingRule201Response**](CreateShippingRule201Response.md)

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

<a id="deleteshippingrule"></a>
# **DeleteShippingRule**
> DeleteShippingRule200Response DeleteShippingRule (string orgId, string ruleId)

Delete shipping rule

Deletes a shipping rule belonging to the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **ruleId** | **string** | Shipping Rule ID |  |

### Return type

[**DeleteShippingRule200Response**](DeleteShippingRule200Response.md)

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

<a id="getshippingrule"></a>
# **GetShippingRule**
> ListShippingRules200ResponseDataInner GetShippingRule (string orgId, string ruleId)

Get shipping rule

Returns a single shipping rule with its carrier, address and printer relations.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **ruleId** | **string** | Shipping Rule ID |  |

### Return type

[**ListShippingRules200ResponseDataInner**](ListShippingRules200ResponseDataInner.md)

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

<a id="listshippingrules"></a>
# **ListShippingRules**
> ListShippingRules200Response ListShippingRules (string orgId, int page = null, int limit = null, string brandId = null, string brandScope = null, string carrierId = null, string search = null)

List shipping rules

Returns a paginated list of shipping rules for the organization with their relations.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **string** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional]  |
| **brandScope** | **string** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional]  |
| **carrierId** | **string** | Filter by carrier. | [optional]  |
| **search** | **string** | Search by rule name. | [optional]  |

### Return type

[**ListShippingRules200Response**](ListShippingRules200Response.md)

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

<a id="updateshippingrule"></a>
# **UpdateShippingRule**
> CreateShippingRule201Response UpdateShippingRule (string orgId, string ruleId, UpdateShippingRuleRequest updateShippingRuleRequest)

Update shipping rule

Updates an existing shipping rule for the organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **ruleId** | **string** | Shipping Rule ID |  |
| **updateShippingRuleRequest** | [**UpdateShippingRuleRequest**](UpdateShippingRuleRequest.md) |  |  |

### Return type

[**CreateShippingRule201Response**](CreateShippingRule201Response.md)

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

