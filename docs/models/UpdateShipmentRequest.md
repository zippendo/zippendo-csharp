# Zippendo.Model.UpdateShipmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Reference** | **string** | Customer-facing shipment reference. | [optional] 
**AddressId** | **string** | Sender address identifier. | [optional] 
**ServicePointId** | **string** | Selected service point ID. | [optional] 
**Parties** | [**List&lt;CreateShipmentRequestPartiesInner&gt;**](CreateShipmentRequestPartiesInner.md) | Parties involved in the shipment. Optional when orderId is provided. | [optional] 
**Type** | **string** | Direction of the shipment relative to the organization. | [optional] 
**CarrierSettings** | [**UpdateShipmentRequestCarrierSettings**](UpdateShipmentRequestCarrierSettings.md) |  | [optional] 
**Parcels** | [**List&lt;CreateShipmentRequestParcelsInner&gt;**](CreateShipmentRequestParcelsInner.md) | Parcels to include. Optional when orderId is provided. | [optional] 
**PickupDetails** | [**CreateShipmentRequestPickupDetails**](CreateShipmentRequestPickupDetails.md) |  | [optional] 
**TermOfTrade** | **string** | Incoterm governing the shipment. | [optional] 
**Status** | **string** | Lifecycle status of the shipment. | [optional] 
**OrderId** | **string** | Order to derive parties and parcels from. | [optional] 
**LabelPrinterId** | **string** | Printer to assign for labels. | [optional] 
**DocumentPrinterId** | **string** | Printer to assign for documents. | [optional] 
**ShippingRuleId** | **string** | Shipping rule to apply to the shipment. Pass null to clear. | [optional] 
**Droppoint** | [**UpdateShipmentRequestDroppoint**](UpdateShipmentRequestDroppoint.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

