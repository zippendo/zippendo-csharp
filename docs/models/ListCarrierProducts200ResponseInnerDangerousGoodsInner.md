# Zippendo.Model.ListCarrierProducts200ResponseInnerDangerousGoodsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | **string** | &#x60;limited_quantity&#x60;: dangerous goods packed in limited quantities (LQ). &#x60;regulated&#x60;: fully regulated dangerous goods (ADR). | 
**ServiceId** | **string** | The service that declares these dangerous goods to the carrier. | 
**Parameters** | [**ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters**](ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters.md) |  | 
**OwnedParameters** | **List&lt;string&gt;** | Every additional parameter that describes the declared goods, including those &#x60;parameters&#x60; does not fill. A declaration replaces them all, so a value saved for other goods is never sent. | [optional] 
**SingleParcel** | **bool** | The carrier takes this declaration on a shipment of one parcel only. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

