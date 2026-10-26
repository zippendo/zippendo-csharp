# Zippendo.Model.CreateShippingRule201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique shipping rule identifier | 
**Name** | **string** | Shipping rule name | 
**Translations** | [**Dictionary&lt;string, ListShippingRules200ResponseDataInnerTranslationsValue&gt;**](ListShippingRules200ResponseDataInnerTranslationsValue.md) | Checkout name and description per language | 
**CarrierId** | **string** | Carrier ID | 
**ProductId** | **string** | Product ID from carrier | 
**Services** | **List&lt;string&gt;** | List of selected services | 
**AdditionalParameters** | [**Dictionary&lt;string, ListShippingRules200ResponseDataInnerAdditionalParametersValue&gt;**](ListShippingRules200ResponseDataInnerAdditionalParametersValue.md) | Carrier-specific extra parameters, keyed by the carrier parameter &#x60;key&#x60; from the product&#39;s &#x60;additionalParameters[].key&#x60;. | 
**AddressId** | **string** | Sender address ID | 
**ReceivingCountries** | **List&lt;string&gt;** | List of supported country codes | 
**Conditions** | [**List&lt;ListShippingRules200ResponseDataInnerConditionsInner&gt;**](ListShippingRules200ResponseDataInnerConditionsInner.md) | Rule conditions (weight/price/quantity) | 
**OrgId** | **string** | Owning organization ID | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601) | 
**UpdatedAt** | **string** | Last update timestamp (ISO 8601) | 
**Description** | **string** | Optional description | 
**Direction** | **string** | Whether this rule is for outbound or inbound (return) shipments | [default to DirectionEnum.Outbound]
**EmailNotification** | **bool** | Send an email notification to the receiver | [default to false]
**PhoneNotification** | **bool** | Send an SMS notification to the receiver | [default to false]
**MinWeight** | **decimal** | Minimum required weight in kg. Orders below this are excluded from the rule. | 
**MaxWeight** | **decimal** | Maximum allowed weight in kg. Orders exceeding this are excluded from the rule. | 
**MinOrderValue** | **decimal** | Minimum required order value in currency units. Orders below this are excluded from the rule. | 
**MaxOrderValue** | **decimal** | Maximum allowed order value in currency units. Orders exceeding this are excluded from the rule. | 
**GenerateProformaInvoice** | **bool** | Generate proforma invoice for shipments | [default to false]
**GenerateCommercialInvoice** | **bool** | Generate commercial invoice for international shipments | [default to false]
**GeneratePackingList** | **bool** | Generate a packing slip with parcel and item details | [default to false]
**AutoPrintLabels** | **bool** | Automatically print labels when shipment is sent | [default to false]
**AutoPrintDocuments** | **bool** | Automatically print documents when shipment is sent | [default to false]
**LabelPrinterId** | **string** | ID of the label printer | 
**DocumentPrinterId** | **string** | ID of the document printer | 
**ReturnShippingRuleId** | **string** | ID of the return shipping rule | 
**AutoCreateReturnShipment** | **bool** | Automatically create and send a return shipment on dispatch | [default to false]
**BrandId** | **string** | Brand this record belongs to, or null when it is organization-wide | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

