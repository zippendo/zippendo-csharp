# Zippendo.Model.CreateOrderChannelRequestSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UseWebhooks** | **bool** | Use webhooks for real-time order sync. | [optional] [default to true]
**SiteUrl** | **string** | WooCommerce store URL. | [optional] 
**AutoFulfill** | **bool** | Push tracking back to the platform when a shipment is dispatched. Enabled by default (opt-out) — set to false to disable write-back; an unset value still syncs. | [optional] 
**AutoSync** | **bool** | Periodically poll the channel for new orders. | [optional] [default to false]
**SyncIntervalMinutes** | **int** | Polling interval in minutes (5-1440). | [optional] [default to 15]
**AutoShipOnCreate** | **bool** | Create a shipment automatically when an order arrives. | [optional] [default to false]
**DefaultCarrierId** | **string** | Default carrier ID for auto-shipping. | [optional] 
**DefaultProductId** | **string** | Default carrier product ID for auto-shipping. | [optional] 
**DefaultAddressId** | **string** | Default sender address ID for auto-shipping. | [optional] 
**ShippingMethodMappings** | [**List&lt;CreateOrderChannelRequestSettingsShippingMethodMappingsInner&gt;**](CreateOrderChannelRequestSettingsShippingMethodMappingsInner.md) | Map imported shipping-method titles to shipping rules, for channels without checkout rate integration. | [optional] 
**SyncOnlyUnfulfilled** | **bool** | Only import orders that are not yet fulfilled. | [optional] [default to true]
**SyncOrdersSince** | **DateTimeOffset** | Only sync orders placed at or after this timestamp. | [optional] 
**ServicePointCount** | **int** | Number of service points to show at checkout (1-20). | [optional] [default to 6]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

