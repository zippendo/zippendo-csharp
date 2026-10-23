# Zippendo.Model.UpdateOrg200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique organization identifier | 
**Name** | **string** | Organization name | 
**Slug** | **string** | Organization URL slug (unique identifier) | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601) | 
**UpdatedAt** | **string** | Last update timestamp (ISO 8601) | 
**Description** | **string** | Organization description | 
**Currency** | **string** | Billing currency (ISO 4217 code) | [default to "DKK"]
**VatNumber** | **string** | Company VAT/tax ID for invoices | [optional] 
**BillingEmail** | **string** | Billing email for invoices | [optional] 
**CompanyName** | **string** | Legal company name | [optional] 
**AddressLine1** | **string** | Address line 1 | [optional] 
**AddressLine2** | **string** | Address line 2 | [optional] 
**City** | **string** | City | [optional] 
**PostalCode** | **string** | Postal code | [optional] 
**Country** | **string** | Country (ISO 3166-1 alpha-2 code) | [optional] 
**Customs** | **Dictionary&lt;string, string&gt;** | Customs identifiers keyed by type | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

