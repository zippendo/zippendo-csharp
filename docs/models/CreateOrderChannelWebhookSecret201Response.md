# Zippendo.Model.CreateOrderChannelWebhookSecret201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Secret** | **string** | The webhook signing secret. Returned only once — store it in your system; every push to the ingest URL must carry an HMAC-SHA256 hex signature of the raw body computed with it. | 
**WebhookUrl** | **string** | The ingest URL your system pushes signed order events to. | 
**CreatedAt** | **DateTimeOffset** | When this secret was issued (ISO 8601). | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

