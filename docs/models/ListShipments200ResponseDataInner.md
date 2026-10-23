# Zippendo.Model.ListShipments200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique shipment identifier. | 
**Reference** | **string** | Customer-facing shipment reference. | 
**Type** | **string** | Direction of the shipment relative to the organization. | 
**CarrierSettings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  | 
**Status** | **string** | Lifecycle status of the shipment. | 
**CreatedAt** | **string** | Timestamp when the shipment was created. | 
**UpdatedAt** | **string** | Timestamp when the shipment was last updated. | 
**BrandId** | **string** | Brand this record belongs to, or null when it is organization-wide | 
**Address** | [**ListShipments200ResponseDataInnerAddress**](ListShipments200ResponseDataInnerAddress.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

