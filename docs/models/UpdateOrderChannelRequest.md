# Zippendo.Model.UpdateOrderChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BrandId** | **string** | Brand this channel belongs to; null for organization-wide | [optional] 
**Name** | **string** | Display name for the channel. | [optional] 
**Enabled** | **bool** | Whether the channel is active. | [optional] 
**Role** | **string** | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfillment or tracking is pushed back to the platform. | [optional] 
**Credentials** | **Dictionary&lt;string, Object&gt;** | Type-specific platform credentials. | [optional] 
**Settings** | [**UpdateOrderChannelRequestSettings**](UpdateOrderChannelRequestSettings.md) |  | [optional] 
**ShippingRuleIds** | **List&lt;string&gt;** | IDs of shipping rules linked to this channel. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

