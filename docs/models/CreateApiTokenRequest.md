# Zippendo.Model.CreateApiTokenRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Token name for identification | 
**Scopes** | **List&lt;CreateApiTokenRequest.ScopesEnum&gt;** | Permission scopes for the token | 
**ExpiresInDays** | **int** | Token expiry in days (optional, max 365) | [optional] 
**BrandId** | **string** | Restrict this token to a single brand. Requests made with it can only read and write that brand&#39;s data. Omit for organization-wide access. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

