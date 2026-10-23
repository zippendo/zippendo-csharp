# Zippendo.Model.CreateOrderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OrderNumber** | **string** | Human-readable order number. | 
**OrderChannelId** | **string** | ID of the order channel this order belongs to. | 
**OrderLines** | [**List&lt;CreateOrderRequestOrderLinesInner&gt;**](CreateOrderRequestOrderLinesInner.md) | Line items in the order. | 
**ExternalId** | **string** | Identifier of the order in the source platform. | [optional] 
**CustomerName** | **string** | Customer full name. | [optional] 
**CustomerEmail** | **string** | Customer email address. | [optional] 
**ShippingAddress** | [**CreateOrderRequestShippingAddress**](CreateOrderRequestShippingAddress.md) |  | [optional] 
**SubtotalAmount** | **decimal** | Order subtotal before shipping and tax. | [optional] 
**TotalAmount** | **decimal** | Order grand total. | [optional] 
**Currency** | **string** | ISO 4217 currency code. | [optional] 
**Notes** | **string** | Free-form internal notes. | [optional] 
**ShippingRuleId** | **string** | Shipping rule to ship this order with. When set, a shipment is created immediately (and dispatched if the channel has autoShipOnCreate enabled). | [optional] 
**ShippingMethodTitle** | **string** | Shipping-method title from the source checkout; matched against the order channel&#39;s shipping-method mappings to pick a shipping rule. | [optional] 
**ExternalData** | **Dictionary&lt;string, Object&gt;** | Raw platform-specific payload for reference. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

