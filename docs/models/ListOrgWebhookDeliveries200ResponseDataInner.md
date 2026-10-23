# Zippendo.Model.ListOrgWebhookDeliveries200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Delivery log ID | 
**WebhookId** | **string** | ID of the webhook this delivery belongs to | 
**Event** | **string** | Event type that was delivered | 
**Success** | **bool** | Whether the delivery succeeded | 
**Attempt** | **decimal** | Delivery attempt number | 
**CreatedAt** | **string** | Delivery timestamp (ISO 8601) | 
**Payload** | **Object** | JSON payload that was sent | 
**StatusCode** | **decimal** | HTTP status code returned by the endpoint | 
**Response** | **string** | Response body returned by the endpoint | 
**Duration** | **decimal** | Request duration in milliseconds | 
**Error** | **string** | Error message if the delivery failed | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

