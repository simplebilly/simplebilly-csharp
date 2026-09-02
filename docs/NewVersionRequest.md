# Org.OpenAPITools.Model.NewVersionRequest
Body for uploading a new version. Bytes must already be stored under `file_name` via the object storage API.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FileName** | **string** | Storage key of the already-uploaded bytes. | 
**FileSize** | **long?** |  | [optional] 
**MimeType** | **string** |  | [optional] 
**OriginalName** | **string** |  | [optional] 
**Sha256Hash** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

