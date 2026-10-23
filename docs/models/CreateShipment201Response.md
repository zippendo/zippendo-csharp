# Zippendo.Model.CreateShipment201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique shipment identifier. | 
**Reference** | **string** | Customer-facing shipment reference. | 
**Parties** | [**List&lt;CreateShipment201ResponsePartiesInner&gt;**](CreateShipment201ResponsePartiesInner.md) | Parties involved in the shipment (sender, receiver, etc.). | 
**Type** | **string** | Direction of the shipment relative to the organization. | 
**CarrierSettings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  | 
**Parcels** | [**List&lt;CreateShipment201ResponseParcelsInner&gt;**](CreateShipment201ResponseParcelsInner.md) | Parcels included in the shipment. | 
**Errors** | [**List&lt;CreateShipment201ResponseErrorsInner&gt;**](CreateShipment201ResponseErrorsInner.md) | Carrier errors recorded for the shipment. | 
**Status** | **string** | Lifecycle status of the shipment. | 
**OrgId** | **string** | Owning organization identifier. | 
**Logs** | [**List&lt;CreateShipment201ResponseLogsInner&gt;**](CreateShipment201ResponseLogsInner.md) | Request/response logs captured during carrier interactions. | 
**Activities** | [**List&lt;CreateShipment201ResponseActivitiesInner&gt;**](CreateShipment201ResponseActivitiesInner.md) | Chronological activity history of the shipment. | 
**CreatedAt** | **string** | Timestamp when the shipment was created. | 
**UpdatedAt** | **string** | Timestamp when the shipment was last updated. | 
**AddressId** | **string** | Sender address identifier. | [optional] 
**ServicePointId** | **string** | Selected service point ID. | [optional] 
**PickupDetails** | [**CreateShipment201ResponsePickupDetails**](CreateShipment201ResponsePickupDetails.md) |  | [optional] 
**TermOfTrade** | **string** | Incoterm governing the shipment. | [default to "DAP"]
**Documents** | [**List&lt;CreateShipment201ResponseDocumentsInner&gt;**](CreateShipment201ResponseDocumentsInner.md) | Documents generated for the shipment (labels, invoices). | [optional] 
**Tracking** | [**CreateShipment201ResponseTracking**](CreateShipment201ResponseTracking.md) |  | [optional] 
**OrderId** | **string** | Associated order identifier. | [optional] 
**ShippingRuleId** | **string** | Applied shipping rule identifier. | [optional] 
**ShippingRule** | [**CreateShipment201ResponseShippingRule**](CreateShipment201ResponseShippingRule.md) |  | [optional] 
**LabelPrinterId** | **string** | Printer assigned for labels on this shipment. | [optional] 
**DocumentPrinterId** | **string** | Printer assigned for documents on this shipment. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

