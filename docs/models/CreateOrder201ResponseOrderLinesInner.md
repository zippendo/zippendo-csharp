# Zippendo.Model.CreateOrder201ResponseOrderLinesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Product name. | 
**Quantity** | **long** | Quantity ordered. | 
**Sku** | **string** | Stock keeping unit identifier. | [optional] 
**UnitPrice** | **decimal** | Price per unit. | [optional] 
**TotalPrice** | **decimal** | Total price for the line. | [optional] 
**Currency** | **string** | ISO 4217 currency code. | [optional] 
**Weight** | **decimal** | Item weight in the given unit. | [optional] 
**WeightUnit** | **string** | Unit of the weight value. | [optional] 
**VariantId** | **string** | Platform variant identifier. | [optional] 
**ProductId** | **string** | Platform product identifier. | [optional] 
**ImageUrl** | **string** | Product image URL. | [optional] 
**HsCode** | **string** | Harmonized System customs code (6-13 digits). | [optional] 
**CountryOfOrigin** | **string** | ISO 3166-1 alpha-2 country of origin. | [optional] 
**ProvinceOfOrigin** | **string** | ISO 3166-2 province of origin. | [optional] 
**Barcode** | **string** | Item barcode (EAN/UPC). | [optional] 
**RequiresShipping** | **bool** | Whether the item requires shipping. | [optional] 
**Taxable** | **bool** | Whether the item is taxable. | [optional] 
**GiftCard** | **bool** | Whether the item is a gift card. | [optional] 
**Vendor** | **string** | Vendor or brand name. | [optional] 
**Id** | **string** | Order line ID. Send it back as &#x60;orderLines[].id&#x60; when updating the order to edit this line in place. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

