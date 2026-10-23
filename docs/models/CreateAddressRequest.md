# Zippendo.Model.CreateAddressRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Company or person the parcel is sent from, printed on labels | 
**Address1** | **string** | Address line 1 | 
**Zipcode** | **string** | Postal/ZIP code | 
**City** | **string** | City | 
**Phone** | **string** | Phone number | 
**CountryCode** | **string** | Country code (ISO 2 or 3 letter) | 
**Email** | **string** | Email address | 
**Description** | **string** | Internal label for this address; never printed or sent to a carrier | [optional] 
**AttContact** | **string** | Contact person at this address, printed as the att. line | [optional] 
**Address2** | **string** | Address line 2 | [optional] 
**State** | **string** | State/Province | [optional] 
**Customs** | **Dictionary&lt;string, string&gt;** | Customs identifiers (voec, eori, sprn, ioss, fda, duns) | [optional] 
**AddressTypes** | **List&lt;CreateAddressRequest.AddressTypesEnum&gt;** | Address types (sender, pickup, return) | [optional] 
**BrandId** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

