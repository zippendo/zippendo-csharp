# Zippendo.Model.SplitShipmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ParcelId** | **string** | Parcel whose order lines are split into a new shipment. | 
**OrderLineIds** | **List&lt;string&gt;** | Order line IDs to move. If omitted, all order lines in the parcel are moved. | [optional] 
**CarrierId** | **string** | Carrier for the new shipment. Copied from the original if omitted. | [optional] 
**ProductId** | **string** | Carrier product for the new shipment. Copied from the original if omitted. | [optional] 
**Services** | **List&lt;string&gt;** | Service codes for the new shipment. Copied from the original if omitted. | [optional] 
**AdditionalParameters** | [**Dictionary&lt;string, CreateShippingRuleRequestAdditionalParametersValue&gt;**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific parameters for the new shipment. Copied from the original if omitted. | [optional] 
**Reference** | **string** | Reference for the new shipment. Defaults to the original reference with a suffix. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

