# Zippendo.Model.CreateOrder201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique order ID. | 
**OrderNumber** | **string** | Human-readable order number. | 
**OrderLines** | [**List&lt;CreateOrder201ResponseOrderLinesInner&gt;**](CreateOrder201ResponseOrderLinesInner.md) | Line items in the order. | 
**Status** | **string** | Order fulfillment status derived from its shipments. | 
**OrderChannelId** | **string** | ID of the order channel this order belongs to. | 
**OrgId** | **string** | Owning organization ID. | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601). | 
**UpdatedAt** | **string** | Last update timestamp (ISO 8601). | 
**ExternalId** | **string** | Identifier of the order in the source platform. | [optional] 
**CustomerName** | **string** | Customer full name. | [optional] 
**CustomerEmail** | **string** | Customer email address. | [optional] 
**ShippingAddress** | [**CreateOrder201ResponseShippingAddress**](CreateOrder201ResponseShippingAddress.md) |  | [optional] 
**SubtotalAmount** | **decimal** | Order subtotal before shipping and tax. | [optional] 
**TotalAmount** | **decimal** | Order grand total. | [optional] 
**Currency** | **string** | ISO 4217 currency code. | [optional] 
**ShippingRuleId** | **string** | ID of the applied shipping rule. | [optional] 
**Notes** | **string** | Free-form internal notes. | [optional] 
**ExternalData** | **Dictionary&lt;string, Object&gt;** | Raw platform-specific payload for reference. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

