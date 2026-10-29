# Zippendo.Model.UpdateShippingRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Shipping rule name | [optional] 
**Description** | **string** | Optional description | [optional] 
**Translations** | [**Dictionary&lt;string, CreateShippingRuleRequestTranslationsValue&gt;**](CreateShippingRuleRequestTranslationsValue.md) | Checkout name and description per language; a blank field falls back to the rule&#39;s own text | [optional] 
**Direction** | **string** | Whether this rule is for outbound or inbound (return) shipments | [optional] 
**CarrierId** | **string** | Carrier ID | [optional] 
**ProductId** | **string** | Product ID from carrier | [optional] 
**Services** | **List&lt;string&gt;** | List of selected services | [optional] 
**AdditionalParameters** | [**Dictionary&lt;string, CreateShippingRuleRequestAdditionalParametersValue&gt;**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific extra parameters, keyed by the carrier parameter &#x60;key&#x60; from the product&#39;s &#x60;additionalParameters[].key&#x60;. Omit to leave the rule&#39;s parameters unchanged. | [optional] 
**AddressId** | **string** | Sender address ID | [optional] 
**ReceivingCountries** | **List&lt;string&gt;** | List of supported country codes | [optional] 
**EmailNotification** | **bool** | Send an email notification to the receiver | [optional] 
**PhoneNotification** | **bool** | Send an SMS notification to the receiver | [optional] 
**MinWeight** | **decimal** | Minimum required weight in kg | [optional] 
**MaxWeight** | **decimal** | Maximum allowed weight in kg | [optional] 
**MinOrderValue** | **decimal** | Minimum required order value in currency units | [optional] 
**MaxOrderValue** | **decimal** | Maximum allowed order value in currency units | [optional] 
**Conditions** | [**List&lt;CreateShippingRuleRequestConditionsInner&gt;**](CreateShippingRuleRequestConditionsInner.md) | Rule conditions (weight/price/quantity) | [optional] 
**GenerateProformaInvoice** | **bool** | Generate proforma invoice for shipments | [optional] 
**GenerateCommercialInvoice** | **bool** | Generate commercial invoice for international shipments | [optional] 
**GeneratePackingList** | **bool** | Generate a packing slip with parcel and item details | [optional] 
**AutoPrintLabels** | **bool** | Automatically print labels when shipment is sent | [optional] 
**AutoPrintDocuments** | **bool** | Automatically print documents when shipment is sent | [optional] 
**AutoPrintTrigger** | **string** | When automatic printing starts: &#x60;ON_BOOKING&#x60; prints as soon as the shipment is sent, &#x60;ON_SCAN&#x60; waits until the packing slip is scanned. | [optional] 
**LabelPrinterId** | **string** | ID of the label printer | [optional] 
**DocumentPrinterId** | **string** | ID of the document printer | [optional] 
**ReturnShippingRuleId** | **string** | ID of the return shipping rule | [optional] 
**AutoCreateReturnShipment** | **bool** | Automatically create and send a return shipment on dispatch | [optional] 
**BrandId** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

