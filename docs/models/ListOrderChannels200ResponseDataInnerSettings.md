# Zippendo.Model.ListOrderChannels200ResponseDataInnerSettings
Channel settings (webhook secret and checkout token hash omitted).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UseWebhooks** | **bool** | Use webhooks for real-time order sync. | [default to true]
**WebhookId** | **string** | External webhook identifier for management. | [optional] 
**WebhookIds** | **List&lt;int&gt;** | Registered WooCommerce webhook ids. | [optional] 
**WebhookSecretCreatedAt** | **DateTimeOffset** | When the custom channel&#39;s webhook signing secret was issued. A non-secret signal so clients can show that a secret exists; the secret itself is never returned after creation. | [optional] 
**SiteUrl** | **string** | WooCommerce store URL. | [optional] 
**AutoFulfill** | **bool** | Push tracking back to the platform when a shipment is dispatched. Enabled by default (opt-out) — set to false to disable write-back; an unset value still syncs. | [optional] 
**CheckoutTokenCreatedAt** | **DateTimeOffset** | When the checkout token was issued (internal; never exposed in API responses). | [optional] 
**AutoSync** | **bool** | Periodically poll the channel for new orders. | [default to false]
**SyncIntervalMinutes** | **int** | Polling interval in minutes (5-1440). | [default to 15]
**AutoShipOnCreate** | **bool** | Create a shipment automatically when an order arrives. | [default to false]
**DefaultCarrierId** | **string** | Default carrier ID for auto-shipping. | [optional] 
**DefaultProductId** | **string** | Default carrier product ID for auto-shipping. | [optional] 
**DefaultAddressId** | **string** | Default sender address ID for auto-shipping. | [optional] 
**ShippingMethodMappings** | [**List&lt;ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner&gt;**](ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner.md) | Map imported shipping-method titles to shipping rules, for channels without checkout rate integration. | [optional] 
**SyncOnlyUnfulfilled** | **bool** | Only import orders that are not yet fulfilled. | [default to true]
**SyncOrdersSince** | **DateTimeOffset** | Only sync orders placed at or after this timestamp. | [optional] 
**ServicePointCount** | **int** | Number of service points to show at checkout (1-20). | [default to 6]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

