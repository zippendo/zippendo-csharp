# Zippendo.Model.CreateOrgWebhookRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Human-readable webhook name | 
**Url** | **string** | Webhook endpoint URL | 
**Events** | **List&lt;CreateOrgWebhookRequest.EventsEnum&gt;** | Events to subscribe to | 
**IsActive** | **bool** | Whether the webhook is active | [optional] [default to true]
**BrandId** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

