# Zippendo.Model.ListOrderChannels200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique order channel ID. | 
**Name** | **string** | Display name of the channel. | 
**Type** | **string** | Type of the order channel (sales platform). | 
**Enabled** | **bool** | Whether the channel is active. | 
**Role** | **string** | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfillment or tracking is pushed back to the platform. | 
**HasCredentials** | **bool** | Whether credentials are configured (values are never exposed). | 
**Settings** | [**ListOrderChannels200ResponseDataInnerSettings**](ListOrderChannels200ResponseDataInnerSettings.md) |  | 
**OrgId** | **string** | Owning organization ID. | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601). | 
**UpdatedAt** | **string** | Last update timestamp (ISO 8601). | 
**BrandId** | **string** | Brand this channel belongs to, or null for organization-wide. Orders synced from this channel inherit it, and so do the shipments and documents made from them. | 
**WebhooksEnabled** | **bool** | Whether real-time webhooks are enabled. | [optional] 
**LastSyncAt** | **DateTimeOffset** | Timestamp of the last successful sync. | [optional] 
**LastSyncError** | **string** | Error message from the last failed sync. | [optional] 
**ShippingRuleIds** | **List&lt;string&gt;** | IDs of shipping rules linked to this channel. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

