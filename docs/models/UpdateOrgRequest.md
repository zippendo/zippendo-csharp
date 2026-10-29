# Zippendo.Model.UpdateOrgRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Organization name | [optional] 
**Slug** | **string** | Organization slug | [optional] 
**Description** | **string** | Organization description | [optional] 
**Currency** | **string** | Billing currency (ISO 4217 code) | [optional] 
**VatNumber** | **string** | Company VAT/tax ID for invoices | [optional] 
**Phone** | **string** | Billing/contact phone number | [optional] 
**BillingEmail** | **string** | Billing email for invoices | [optional] 
**CompanyName** | **string** | Legal company name | [optional] 
**AddressLine1** | **string** | Address line 1 | [optional] 
**AddressLine2** | **string** | Address line 2 | [optional] 
**City** | **string** | City | [optional] 
**PostalCode** | **string** | Postal code | [optional] 
**Country** | **string** | Country (ISO 3166-1 alpha-2 code) | [optional] 
**Customs** | **Dictionary&lt;string, string&gt;** | Organization-wide customs identifiers (EORI, IOSS, VOEC, etc.); null clears all | [optional] 
**PackingSlipScanCode** | **string** | Code printed on packing slips that a scan turns into a print: &#x60;QR&#x60;, &#x60;BARCODE&#x60;, or &#x60;NONE&#x60; for no code. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

