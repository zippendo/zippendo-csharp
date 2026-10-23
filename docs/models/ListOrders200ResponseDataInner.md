# Zippendo.Model.ListOrders200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique order ID. | 
**OrderNumber** | **string** | Human-readable order number. | 
**Status** | **string** | Order fulfillment status derived from its shipments. | 
**ShipmentCount** | **long** | Number of shipments created for the order. | 
**OrderChannel** | [**ListOrders200ResponseDataInnerOrderChannel**](ListOrders200ResponseDataInnerOrderChannel.md) |  | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601). | 
**UpdatedAt** | **string** | Last update timestamp (ISO 8601). | 
**CustomerName** | **string** | Customer full name. | [optional] 
**CustomerEmail** | **string** | Customer email address. | [optional] 
**BrandId** | **string** | Brand this record belongs to, or null when it is organization-wide | 
**SubtotalAmount** | **decimal** | Order subtotal before shipping and tax. | [optional] 
**TotalAmount** | **decimal** | Order grand total. | [optional] 
**Currency** | **string** | ISO 4217 currency code. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

