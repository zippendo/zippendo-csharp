# Zippendo.Model.CreateShipmentRequestParcelsInnerOrderLinesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Quantity** | **long** | Number of units in this order line. | 
**Id** | **string** | Unique order line identifier. | [optional] 
**OrderLineId** | **string** | ID of the order line this packed line came from. Null when the item did not originate from an order line, such as a free gift or a replacement part. | [optional] 
**Sku** | **string** | Stock keeping unit of the product. Optional — not every webshop assigns SKUs. | [optional] 
**Description** | **string** | Human-readable product description. | [optional] 
**UnitPrice** | **decimal** | Price per unit in the order line currency. | [optional] 
**Currency** | **string** | ISO 4217 currency code. | [optional] 
**VatPercent** | **decimal** | VAT percentage applied to the unit price. | [optional] 
**Location** | **string** | Warehouse picking location. | [optional] 
**CountryOfOrigin** | **string** | ISO 3166-1 alpha-2 country of origin. | [optional] 
**HsCode** | **string** | Harmonized System customs code. | [optional] 
**TarrifNumber** | **string** | Deprecated misspelling of &#x60;hsCode&#x60;, kept for backwards compatibility. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

