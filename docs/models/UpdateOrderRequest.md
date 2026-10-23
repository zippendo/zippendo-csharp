# Zippendo.Model.UpdateOrderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OrderNumber** | **string** | Human-readable order number. | [optional] 
**CustomerName** | **string** | Customer full name. | [optional] 
**CustomerEmail** | **string** | Customer email address. | [optional] 
**ShippingAddress** | [**CreateOrderRequestShippingAddress**](CreateOrderRequestShippingAddress.md) |  | [optional] 
**OrderLines** | [**List&lt;CreateOrderRequestOrderLinesInner&gt;**](CreateOrderRequestOrderLinesInner.md) | Line items in the order. | [optional] 
**SubtotalAmount** | **decimal** | Order subtotal before shipping and tax. | [optional] 
**TotalAmount** | **decimal** | Order grand total. | [optional] 
**Currency** | **string** | ISO 4217 currency code. | [optional] 
**Notes** | **string** | Free-form internal notes. | [optional] 
**Status** | **string** | Order fulfillment status derived from its shipments. | [optional] 
**ShippingRuleId** | **string** | ID of the shipping rule to apply. | [optional] 
**ServicePointId** | **string** | Service point ID to apply to unsent outbound shipments. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

