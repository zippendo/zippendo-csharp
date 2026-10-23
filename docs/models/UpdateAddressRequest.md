# Zippendo.Model.UpdateAddressRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Company or person the parcel is sent from, printed on labels | [optional] 
**Description** | **string** | Internal label for this address; send null or an empty string to clear it | [optional] 
**AttContact** | **string** | Contact person at this address; send null or an empty string to clear it | [optional] 
**Address1** | **string** | Address line 1 | [optional] 
**Address2** | **string** | Address line 2; send null or an empty string to clear it | [optional] 
**Zipcode** | **string** | Postal/ZIP code | [optional] 
**City** | **string** | City | [optional] 
**Phone** | **string** | Phone number | [optional] 
**CountryCode** | **string** | ISO country code | [optional] 
**State** | **string** | State/Province; send null or an empty string to clear it | [optional] 
**Email** | **string** | Email address | [optional] 
**Customs** | **Dictionary&lt;string, string&gt;** | Customs identifiers | [optional] 
**AddressTypes** | **List&lt;UpdateAddressRequest.AddressTypesEnum&gt;** | Address types (sender, pickup, return) | [optional] 
**BrandId** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

