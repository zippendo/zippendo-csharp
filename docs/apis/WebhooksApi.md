# Zippendo.Api.WebhooksApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOrgWebhook**](WebhooksApi.md#createorgwebhook) | **POST** /orgs/{orgId}/webhooks | Create webhook |
| [**DeleteOrgWebhook**](WebhooksApi.md#deleteorgwebhook) | **DELETE** /orgs/{orgId}/webhooks/{webhookId} | Delete webhook |
| [**GetOrgWebhook**](WebhooksApi.md#getorgwebhook) | **GET** /orgs/{orgId}/webhooks/{webhookId} | Get webhook |
| [**ListOrgWebhookDeliveries**](WebhooksApi.md#listorgwebhookdeliveries) | **GET** /orgs/{orgId}/webhooks/{webhookId}/deliveries | List webhook deliveries |
| [**ListOrgWebhooks**](WebhooksApi.md#listorgwebhooks) | **GET** /orgs/{orgId}/webhooks | List webhooks |
| [**TestOrgWebhook**](WebhooksApi.md#testorgwebhook) | **POST** /orgs/{orgId}/webhooks/{webhookId}/test | Test webhook |
| [**UpdateOrgWebhook**](WebhooksApi.md#updateorgwebhook) | **PATCH** /orgs/{orgId}/webhooks/{webhookId} | Update webhook |

<a id="createorgwebhook"></a>
# **CreateOrgWebhook**
> CreateOrgWebhook201Response CreateOrgWebhook (string orgId, CreateOrgWebhookRequest createOrgWebhookRequest)

Create webhook

Create a new webhook endpoint for an organization that receives event notifications.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createOrgWebhookRequest** | [**CreateOrgWebhookRequest**](CreateOrgWebhookRequest.md) |  |  |

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)

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
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteorgwebhook"></a>
# **DeleteOrgWebhook**
> DeleteOrgWebhook200Response DeleteOrgWebhook (string orgId, string webhookId)

Delete webhook

Permanently delete a webhook and all its delivery logs.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **webhookId** | **string** | Webhook ID |  |

### Return type

[**DeleteOrgWebhook200Response**](DeleteOrgWebhook200Response.md)

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

<a id="getorgwebhook"></a>
# **GetOrgWebhook**
> CreateOrgWebhook201Response GetOrgWebhook (string orgId, string webhookId)

Get webhook

Get a specific webhook including its signing secret.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **webhookId** | **string** | Webhook ID |  |

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)

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

<a id="listorgwebhookdeliveries"></a>
# **ListOrgWebhookDeliveries**
> ListOrgWebhookDeliveries200Response ListOrgWebhookDeliveries (string orgId, string webhookId, int page = null, int limit = null)

List webhook deliveries

List the delivery history for a specific webhook.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **webhookId** | **string** | Webhook ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |

### Return type

[**ListOrgWebhookDeliveries200Response**](ListOrgWebhookDeliveries200Response.md)

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

<a id="listorgwebhooks"></a>
# **ListOrgWebhooks**
> ListOrgWebhooks200Response ListOrgWebhooks (string orgId, int page = null, int limit = null, string brandId = null, string brandScope = null, string isActive = null, string search = null)

List webhooks

List all webhooks belonging to an organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **string** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional]  |
| **brandScope** | **string** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional]  |
| **isActive** | **string** | Filter by active state. | [optional]  |
| **search** | **string** | Search by webhook name or URL. | [optional]  |

### Return type

[**ListOrgWebhooks200Response**](ListOrgWebhooks200Response.md)

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

<a id="testorgwebhook"></a>
# **TestOrgWebhook**
> TestOrgWebhook200Response TestOrgWebhook (string orgId, string webhookId)

Test webhook

Send a test ping event to the webhook endpoint to verify connectivity.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **webhookId** | **string** | Webhook ID |  |

### Return type

[**TestOrgWebhook200Response**](TestOrgWebhook200Response.md)

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

<a id="updateorgwebhook"></a>
# **UpdateOrgWebhook**
> CreateOrgWebhook201Response UpdateOrgWebhook (string orgId, string webhookId, UpdateOrgWebhookRequest updateOrgWebhookRequest)

Update webhook

Update the configuration of an existing webhook.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **webhookId** | **string** | Webhook ID |  |
| **updateOrgWebhookRequest** | [**UpdateOrgWebhookRequest**](UpdateOrgWebhookRequest.md) |  |  |

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)

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

