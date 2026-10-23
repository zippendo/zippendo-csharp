# Zippendo.Model.BatchSendShipments200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ShipmentId** | **string** | The shipment this result refers to. | 
**Status** | **string** | &#x60;sent&#x60; when the carrier accepted it, &#x60;failed&#x60; when the carrier or Zippendo rejected it, and &#x60;skipped&#x60; when the batch ran out of time before reaching it. A &#x60;skipped&#x60; shipment was never sent to the carrier and is safe to submit again. | 
**Code** | **string** | Canonical machine-readable error code, present when &#x60;status&#x60; is &#x60;failed&#x60; or &#x60;skipped&#x60;. | [optional] 
**Message** | **string** | Human-readable detail, present when &#x60;status&#x60; is &#x60;failed&#x60; or &#x60;skipped&#x60;. | [optional] 
**Errors** | [**List&lt;SendShipment422ResponseErrorsInner&gt;**](SendShipment422ResponseErrorsInner.md) | Carrier-specific errors, present when the carrier rejected the shipment. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

