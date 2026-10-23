# Zippendo.Model.GetOrder200ResponseShippingRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique shipping rule identifier. | 
**Name** | **string** | Display name of the shipping rule. | 
**CarrierId** | **string** | Carrier applied by the rule. | 
**ProductId** | **string** | Carrier product applied by the rule. | 
**Services** | **List&lt;string&gt;** | Additional service codes applied by the rule. | 
**AddressId** | **string** | Sender address applied by the rule. | 
**ReturnShippingRuleId** | **string** | ID of the linked return shipping rule. | [optional] 
**AutoCreateReturnShipment** | **bool** | Whether a return shipment is created automatically. | [optional] 
**AutoPrintLabels** | **bool** | Whether labels are printed automatically on send. | [optional] 
**AutoPrintDocuments** | **bool** | Whether documents are printed automatically on send. | [optional] 
**LabelPrinterId** | **string** | Printer used for labels. | [optional] 
**DocumentPrinterId** | **string** | Printer used for documents. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

