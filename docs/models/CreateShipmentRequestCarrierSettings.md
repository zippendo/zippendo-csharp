# Zippendo.Model.CreateShipmentRequestCarrierSettings
Carrier configuration for the shipment. Optional when shippingRuleId is provided.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CarrierId** | **string** | Identifier of the carrier to use. | 
**ProductId** | **string** | Identifier of the carrier product/service. | 
**Services** | **List&lt;string&gt;** | Additional service codes requested from the carrier. | 
**AdditionalParameters** | [**Dictionary&lt;string, CreateShippingRuleRequestAdditionalParametersValue&gt;**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific extra parameters as key/value pairs. | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

