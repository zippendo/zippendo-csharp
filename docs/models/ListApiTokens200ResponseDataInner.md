# Zippendo.Model.ListApiTokens200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique API token identifier | 
**Name** | **string** | Token name for identification | 
**TokenPrefix** | **string** | First 12 chars of the token for identification | 
**Scopes** | **List&lt;string&gt;** | Permission scopes granted by the token | 
**CreatedAt** | **string** | Creation timestamp (ISO 8601) | 
**CreatedBy** | [**ListApiTokens200ResponseDataInnerCreatedBy**](ListApiTokens200ResponseDataInnerCreatedBy.md) |  | 
**BrandId** | **string** | Brand this token is restricted to, or null for organization-wide access | 
**LastUsedAt** | **string** | Timestamp the token was last used (ISO 8601), null if never used | 
**ExpiresAt** | **string** | Expiry timestamp (ISO 8601), null if it never expires | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

