# Zippendo.Model.ListCarriers200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique carrier identifier | 
**Name** | **string** | Carrier display name | 
**CarrierSlug** | **string** | Carrier slug identifier | 
**Config** | [**Dictionary&lt;string, ListCarriers200ResponseDataInnerConfigValue&gt;**](ListCarriers200ResponseDataInnerConfigValue.md) | Carrier configuration (required and optional fields) | 
**OrgId** | **string** | Owning organization ID | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601) | 
**UpdatedAt** | **string** | Last update timestamp (ISO 8601) | 
**BrandId** | **string** | Brand this record belongs to, or null when it is organization-wide | 
**Logo** | **string** | Carrier logo URL | [optional] 
**BrandColor** | **string** | Carrier brand color (hex) | [optional] 
**Deprecated** | **bool** | Whether this integration is deprecated (still works, but discouraged) | [optional] 
**DeprecationMessage** | **string** | Guidance shown alongside the deprecated tag (e.g. what to migrate to) | [optional] 
**Beta** | **bool** | Whether this integration is newly launched and still being verified in production | [optional] 
**GeneratesCustomsDocuments** | **bool** | Whether the carrier produces the customs declaration (CN22/CN23) itself and returns it with the label. | [optional] 
**GeneratesCommercialInvoice** | **bool** | Whether the carrier produces the commercial invoice itself and returns it with the label, e.g. via electronic trade documents. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

