# Zippendo.Model.ListCarrierProducts200ResponseInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Display name of the carrier product | 
**ProductId** | **string** | Unique carrier product identifier | 
**Type** | **string** | Direction of the shipment for this product | 
**AvailableCountries** | **List&lt;string&gt;** | Receiver countries this product delivers to | 
**AvailableSenderCountries** | **List&lt;string&gt;** | Sender countries supported by this product | 
**Description** | **string** | Description of the carrier product | [optional] 
**IsServicePoint** | **bool** | Whether this product delivers to a service point | [default to false]
**IsPickupAvailable** | **bool** | Whether carrier pickup is available for this product | [default to false]
**Services** | [**List&lt;ListCarrierProducts200ResponseInnerServicesInner&gt;**](ListCarrierProducts200ResponseInnerServicesInner.md) | Additional services available for this product | [optional] 
**AdditionalParameters** | [**List&lt;ListCarrierProducts200ResponseInnerAdditionalParametersInner&gt;**](ListCarrierProducts200ResponseInnerAdditionalParametersInner.md) | Extra parameters that can or must be supplied for this product | [optional] 
**WeightLimits** | [**ListCarrierProducts200ResponseInnerWeightLimits**](ListCarrierProducts200ResponseInnerWeightLimits.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

