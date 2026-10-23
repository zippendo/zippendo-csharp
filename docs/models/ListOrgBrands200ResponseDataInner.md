# Zippendo.Model.ListOrgBrands200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique brand identifier | 
**OrgId** | **string** | Owning organization | 
**Name** | **string** | Brand display name | 
**Slug** | **string** | URL-safe identifier, unique within the organization | 
**UseOrgCustoms** | **bool** | Whether this brand ships under the organization&#39;s fiscal identity. True (the default) declares the organization&#39;s VAT number and customs identifiers and ignores the brand&#39;s own. False makes the brand&#39;s own values the sole source — nothing falls back to the organization, so an identifier the brand has not set is not declared at all. | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601) | 
**UpdatedAt** | **string** | Last update timestamp (ISO 8601) | 
**CompanyName** | **string** | Legal entity name printed on this brand&#39;s documents | [optional] 
**VatNumber** | **string** | VAT/tax ID for this brand&#39;s shipments and documents | [optional] 
**Customs** | **Dictionary&lt;string, string&gt;** | Customs identifiers keyed by type | [optional] 
**AddressLine1** | **string** | Street address line 1 | [optional] 
**AddressLine2** | **string** | Street address line 2 | [optional] 
**City** | **string** | City | [optional] 
**PostalCode** | **string** | Postal code | [optional] 
**Country** | **string** | Country (ISO 3166-1 alpha-2) | [optional] 
**PrimaryColor** | **string** | Primary brand color — document title and table headers | [optional] 
**SecondaryColor** | **string** | Secondary brand color — subtitle, section headings, totals accent | [optional] 
**LogoUrl** | **string** | Authenticated URL for the brand logo, or null when none is set | 
**ArchivedAt** | **string** | When the brand was archived; null when active | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

