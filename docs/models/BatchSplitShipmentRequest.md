# Zippendo.Model.BatchSplitShipmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ParcelId** | **string** | Parcel whose order lines are split across new shipments. | 
**Shipments** | [**List&lt;BatchSplitShipmentRequestShipmentsInner&gt;**](BatchSplitShipmentRequestShipmentsInner.md) | New shipments to create from the split parcel. | 
**CarrierId** | **string** | Carrier for all new shipments. Copied from the original if omitted. | [optional] 
**ProductId** | **string** | Carrier product for all new shipments. Copied from the original if omitted. | [optional] 
**Services** | **List&lt;string&gt;** | Service codes for all new shipments. Copied from the original if omitted. | [optional] 
**AdditionalParameters** | [**Dictionary&lt;string, CreateShippingRuleRequestAdditionalParametersValue&gt;**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific parameters for all new shipments. Copied from the original if omitted. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

