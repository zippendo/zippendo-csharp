# Zippendo.Model.ListAddresses200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique address identifier | 
**Name** | **string** | Company or person the parcel is sent from, printed on labels | 
**Address1** | **string** | Address line 1 | 
**Zipcode** | **string** | Postal/ZIP code | 
**City** | **string** | City | 
**Phone** | **string** | Phone number | 
**CountryCode** | **string** | ISO country code | 
**Email** | **string** | Email address | 
**AddressTypes** | **List&lt;ListAddresses200ResponseDataInner.AddressTypesEnum&gt;** | Address types (sender, pickup, return) | 
**OrgId** | **string** | Owning organization ID | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601) | 
**UpdatedAt** | **string** | Last update timestamp (ISO 8601) | 
**Description** | **string** | Internal label for this address; never printed or sent to a carrier | 
**AttContact** | **string** | Contact person at this address, printed as the att. line | 
**Address2** | **string** | Address line 2 | 
**State** | **string** | State/Province | 
**Customs** | **Dictionary&lt;string, string&gt;** | Customs identifiers keyed by type | [optional] 
**BrandId** | **string** | Brand this record belongs to, or null when it is organization-wide | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

