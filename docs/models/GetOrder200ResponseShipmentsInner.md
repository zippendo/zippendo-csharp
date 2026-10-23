# Zippendo.Model.GetOrder200ResponseShipmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique shipment identifier. | 
**Reference** | **string** | Customer-facing shipment reference. | 
**Status** | **string** | Lifecycle status of the shipment. | 
**Type** | **string** | Direction of the shipment relative to the organization. | 
**CarrierSettings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  | 
**CreatedAt** | **string** | Timestamp when the shipment was created. | 
**UpdatedAt** | **string** | Timestamp when the shipment was last updated. | 
**Parcels** | [**List&lt;GetOrder200ResponseShipmentsInnerParcelsInner&gt;**](GetOrder200ResponseShipmentsInnerParcelsInner.md) | Compact parcels for the order&#39;s fulfillment view (no QR/label payloads). | 
**Tracking** | [**CreateShipment201ResponseTracking**](CreateShipment201ResponseTracking.md) |  | [optional] 
**ServicePointId** | **string** | Selected service point ID. | [optional] 
**ShippingRuleId** | **string** | ID of the shipping rule used for this shipment. | [optional] 
**Documents** | [**List&lt;CreateShipment201ResponseDocumentsInner&gt;**](CreateShipment201ResponseDocumentsInner.md) | Documents (labels, customs forms) for this shipment. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

