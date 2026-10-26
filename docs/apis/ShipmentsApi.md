# Zippendo.Api.ShipmentsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BatchSendShipments**](ShipmentsApi.md#batchsendshipments) | **POST** /orgs/{orgId}/shipments/batch-send | Batch send shipments |
| [**BatchSplitShipment**](ShipmentsApi.md#batchsplitshipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/batch-split-shipment | Batch split shipment |
| [**CreateReturnShipment**](ShipmentsApi.md#createreturnshipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/create-return | Create return shipment |
| [**CreateShipment**](ShipmentsApi.md#createshipment) | **POST** /orgs/{orgId}/shipments | Create shipment |
| [**DeleteShipment**](ShipmentsApi.md#deleteshipment) | **DELETE** /orgs/{orgId}/shipments/{shipmentId} | Delete shipment |
| [**FetchShipmentLabel**](ShipmentsApi.md#fetchshipmentlabel) | **POST** /orgs/{orgId}/shipments/{shipmentId}/fetch-label | Fetch missing label |
| [**GetShipment**](ShipmentsApi.md#getshipment) | **GET** /orgs/{orgId}/shipments/{shipmentId} | Get shipment |
| [**GetShipmentDocumentContent**](ShipmentsApi.md#getshipmentdocumentcontent) | **GET** /orgs/{orgId}/shipments/{shipmentId}/documents/{documentId}/content | Download shipment document |
| [**ListShipments**](ShipmentsApi.md#listshipments) | **GET** /orgs/{orgId}/shipments | List shipments |
| [**SendShipment**](ShipmentsApi.md#sendshipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/send | Send shipment |
| [**SplitShipment**](ShipmentsApi.md#splitshipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-shipment | Split shipment |
| [**SplitShipmentParcel**](ShipmentsApi.md#splitshipmentparcel) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-parcel | Split parcels |
| [**TrackShipment**](ShipmentsApi.md#trackshipment) | **GET** /orgs/{orgId}/shipments/{shipmentId}/tracking | Get shipment tracking |
| [**UpdateShipment**](ShipmentsApi.md#updateshipment) | **PATCH** /orgs/{orgId}/shipments/{shipmentId} | Update shipment |

<a id="batchsendshipments"></a>
# **BatchSendShipments**
> BatchSendShipments200Response BatchSendShipments (string orgId, BatchSendShipmentsRequest batchSendShipmentsRequest)

Batch send shipments

Send multiple shipments in `pending` or `error` status to their carriers in one request. Each shipment is processed independently and reported in `results`; a failure on one shipment never aborts the others. Use it to send every shipment on an order at once.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **batchSendShipmentsRequest** | [**BatchSendShipmentsRequest**](BatchSendShipmentsRequest.md) |  |  |

### Return type

[**BatchSendShipments200Response**](BatchSendShipments200Response.md)

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="batchsplitshipment"></a>
# **BatchSplitShipment**
> BatchSplitShipment201Response BatchSplitShipment (string orgId, string shipmentId, BatchSplitShipmentRequest batchSplitShipmentRequest)

Batch split shipment

Split a parcel into multiple new shipments with per-line quantities in a single atomic operation. Only draft or pending shipments can be split.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |
| **batchSplitShipmentRequest** | [**BatchSplitShipmentRequest**](BatchSplitShipmentRequest.md) |  |  |

### Return type

[**BatchSplitShipment201Response**](BatchSplitShipment201Response.md)

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

<a id="createreturnshipment"></a>
# **CreateReturnShipment**
> CreateShipment201Response CreateReturnShipment (string orgId, string shipmentId)

Create return shipment

Create and auto-send a return shipment from a dispatched outbound shipment with swapped sender/receiver. Requires a configured return shipping rule. The return is returned with the outcome of sending it: `dispatched`, or `error` with the carrier's reasons in `errors`. Returns 409 while a return for the same shipment is already being created.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

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
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **409** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createshipment"></a>
# **CreateShipment**
> CreateShipment201Response CreateShipment (string orgId, CreateShipmentRequest createShipmentRequest)

Create shipment

Create a new shipment for an organization. When orderId is provided, parties and parcels are derived from the order. When shippingRuleId is provided, carrier settings and the sender address derive from the rule.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **createShipmentRequest** | [**CreateShipmentRequest**](CreateShipmentRequest.md) |  |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

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

<a id="deleteshipment"></a>
# **DeleteShipment**
> RevokeApiToken200Response DeleteShipment (string orgId, string shipmentId)

Delete shipment

Delete a shipment. Only shipments in pending status can be deleted.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |

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
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="fetchshipmentlabel"></a>
# **FetchShipmentLabel**
> CreateShipment201Response FetchShipmentLabel (string orgId, string shipmentId)

Fetch missing label

Ask the carrier again for the label of a dispatched shipment whose label could not be downloaded when it was sent (it carries a LABEL_DOWNLOAD_FAILED or CARRIER_BOOKING_UNCONFIRMED warning). Stores the label, clears the warning and returns the shipment.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

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
| **409** | Default Response |  -  |
| **422** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getshipment"></a>
# **GetShipment**
> CreateShipment201Response GetShipment (string orgId, string shipmentId)

Get shipment

Retrieve a single shipment by its ID, including parcels, parties, documents and activity.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

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

<a id="getshipmentdocumentcontent"></a>
# **GetShipmentDocumentContent**
> void GetShipmentDocumentContent (string orgId, string shipmentId, string documentId, string disposition = null, string filename = null)

Download shipment document

Streams a shipment document or label file from storage.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |
| **documentId** | **string** | Document identifier. |  |
| **disposition** | **string** | Render the document inline (default) or force a download. | [optional] [default to inline] |
| **filename** | **string** | Suggested filename (without extension) for attachment downloads. | [optional]  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listshipments"></a>
# **ListShipments**
> ListShipments200Response ListShipments (string orgId, int page = null, int limit = null, string brandId = null, string brandScope = null, string status = null, string type = null, string search = null, string filter = null)

List shipments

List all shipments for an organization, paginated and ordered by newest first. Accepts an advanced filter definition.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization ID |  |
| **page** | **int** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **string** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional]  |
| **brandScope** | **string** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional]  |
| **status** | **string** | Filter by shipment status. | [optional]  |
| **type** | **string** | Filter by direction. | [optional]  |
| **search** | **string** | Search by shipment reference or parcel tracking number. | [optional]  |
| **filter** | **string** | Advanced filter as a JSON-encoded definition: a &#x60;conjunction&#x60; (&#x60;and&#x60;/&#x60;or&#x60;) over &#x60;conditions&#x60;, each &#x60;{ id, field, operator, value }&#x60; or a nested group. Fields and operators per list are documented under Filtering lists in the API overview. An invalid filter returns 400 &#x60;FILTER_INVALID&#x60;. | [optional]  |

### Return type

[**ListShipments200Response**](ListShipments200Response.md)

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
| **403** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="sendshipment"></a>
# **SendShipment**
> CreateShipment201Response SendShipment (string orgId, string shipmentId)

Send shipment

Send a shipment in `pending` or `error` status to its carrier, generating labels and tracking. Returns 422 with the carrier's errors if sending fails, and 409 while the same shipment is already being sent.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

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
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **409** | Default Response |  -  |
| **422** | Default Response |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="splitshipment"></a>
# **SplitShipment**
> SplitShipment201Response SplitShipment (string orgId, string shipmentId, SplitShipmentRequest splitShipmentRequest)

Split shipment

Move order lines from a parcel into a new shipment. Only draft or pending shipments can be split.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |
| **splitShipmentRequest** | [**SplitShipmentRequest**](SplitShipmentRequest.md) |  |  |

### Return type

[**SplitShipment201Response**](SplitShipment201Response.md)

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

<a id="splitshipmentparcel"></a>
# **SplitShipmentParcel**
> SplitShipmentParcel200Response SplitShipmentParcel (string orgId, string shipmentId, SplitShipmentParcelRequest splitShipmentParcelRequest)

Split parcels

Redistribute order lines across parcels within a shipment, moving lines between parcels and creating new ones. Only draft, pending or error shipments can be modified.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |
| **splitShipmentParcelRequest** | [**SplitShipmentParcelRequest**](SplitShipmentParcelRequest.md) |  |  |

### Return type

[**SplitShipmentParcel200Response**](SplitShipmentParcel200Response.md)

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

<a id="trackshipment"></a>
# **TrackShipment**
> TrackShipment200Response TrackShipment (string orgId, string shipmentId)

Get shipment tracking

Retrieve the tracking timeline for a shipment, including current status and all carrier events.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |

### Return type

[**TrackShipment200Response**](TrackShipment200Response.md)

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

<a id="updateshipment"></a>
# **UpdateShipment**
> CreateShipment201Response UpdateShipment (string orgId, string shipmentId, UpdateShipmentRequest updateShipmentRequest)

Update shipment

Update a draft, pending or error shipment; fields left out keep their stored values. A draft becomes pending when the update sets its carrier settings or service point and it has a carrier, or applies a shipping rule, which overrides carrier settings and sender party.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orgId** | **string** | Organization identifier. |  |
| **shipmentId** | **string** | Shipment identifier. |  |
| **updateShipmentRequest** | [**UpdateShipmentRequest**](UpdateShipmentRequest.md) |  |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

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

