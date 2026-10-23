# Zippendo.Model.CreateOrderChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Display name for the channel. | 
**Type** | **string** | Type of the order channel. Platform channels (Shopify, WooCommerce) are created via their connect flows. | 
**BrandId** | **string** | Brand this channel belongs to; null for organization-wide | [optional] 
**Enabled** | **bool** | Whether the channel is active. | [optional] [default to true]
**Role** | **string** | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfillment or tracking is pushed back to the platform. | [optional] [default to RoleEnum.OrdersAndRates]
**Settings** | [**CreateOrderChannelRequestSettings**](CreateOrderChannelRequestSettings.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

