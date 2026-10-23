# Zippendo.Model.CreateShipment201ResponseLogsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique log entry identifier. | 
**Direction** | **string** | Direction of the logged request. | 
**CreatedAt** | **string** | Timestamp when the log entry was created. | 
**Request** | **Object** | Captured request payload. | 
**Response** | **Object** | Captured response payload. | [optional] 
**StatusCode** | **decimal** | HTTP status code of the response. | [optional] 
**Error** | **string** | Error message if the request failed. | [optional] 
**Duration** | **decimal** | Request duration in milliseconds. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

