# Zippendo.Model.CreateShipmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Direction of the shipment relative to the organization. | 
**Reference** | **string** | Customer-facing shipment reference. | [optional] 
**AddressId** | **string** | Sender address identifier. | [optional] 
**ServicePointId** | **string** | Selected service point ID. | [optional] 
**Parties** | [**List&lt;CreateShipmentRequestPartiesInner&gt;**](CreateShipmentRequestPartiesInner.md) | Parties involved in the shipment. Optional when orderId is provided. | [optional] 
**CarrierSettings** | [**CreateShipmentRequestCarrierSettings**](CreateShipmentRequestCarrierSettings.md) |  | [optional] 
**Parcels** | [**List&lt;CreateShipmentRequestParcelsInner&gt;**](CreateShipmentRequestParcelsInner.md) | Parcels to include. Optional when orderId is provided. | [optional] 
**PickupDetails** | [**CreateShipmentRequestPickupDetails**](CreateShipmentRequestPickupDetails.md) |  | [optional] 
**TermOfTrade** | **string** | Incoterm governing the shipment. | [optional] [default to "DAP"]
**Status** | **string** | Lifecycle status of the shipment. | [optional] [default to StatusEnum.Pending]
**OrderId** | **string** | Order to derive parties and parcels from. | [optional] 
**LabelPrinterId** | **string** | Printer to assign for labels. | [optional] 
**DocumentPrinterId** | **string** | Printer to assign for documents. | [optional] 
**ShippingRuleId** | **string** | Create the shipment from this shipping rule: carrier settings and the sender address derive from the rule (explicit carrierSettings and addressId are then ignored). | [optional] 
**Droppoint** | [**CreateShipmentRequestDroppoint**](CreateShipmentRequestDroppoint.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

