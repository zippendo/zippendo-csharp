# Zippendo.Model.ListAvailableCarriers200ResponseInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Display name of the carrier | 
**Slug** | **string** | Unique carrier slug identifier | 
**Group** | **string** | Carrier group or family name | [optional] 
**Description** | **string** | Short description of the carrier | [optional] 
**Logo** | **string** | URL to the carrier logo image | [optional] 
**BrandColor** | **string** | Carrier brand color (hex) | [optional] 
**LearnMoreUrl** | **string** | URL with more information about the carrier | [optional] 
**RequiredFields** | [**List&lt;ListAvailableCarriers200ResponseInnerRequiredFieldsInner&gt;**](ListAvailableCarriers200ResponseInnerRequiredFieldsInner.md) | Configuration fields that must be provided to connect the carrier | [optional] 
**OptionalFields** | [**List&lt;ListAvailableCarriers200ResponseInnerRequiredFieldsInner&gt;**](ListAvailableCarriers200ResponseInnerRequiredFieldsInner.md) | Optional configuration fields for the carrier | [optional] 
**Deprecated** | **bool** | Whether this integration is deprecated (still works, but discouraged) | [optional] 
**DeprecationMessage** | **string** | Guidance shown alongside the deprecated tag (e.g. what to migrate to) | [optional] 
**Beta** | **bool** | Whether this integration is newly launched and still being verified in production | [optional] 
**GeneratesCustomsDocuments** | **bool** | Whether the carrier produces the customs declaration (CN22/CN23) itself and returns it with the label. | [optional] 
**GeneratesCommercialInvoice** | **bool** | Whether the carrier produces the commercial invoice itself and returns it with the label, e.g. via electronic trade documents. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

