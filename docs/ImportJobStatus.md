# Org.OpenAPITools.Model.ImportJobStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Error** | **string** | Set only when the job failed. | [optional] 
**JobId** | **string** |  | 
**Processed** | **long** |  | 
**Progress** | **int** | 0–100 | 
**Provider** | **string** | Which competitor the import came from (lexoffice | billbee); the frontend uses it to label the job. Absent for legacy jobs. | [optional] 
**Stage** | **string** | queued | fetching | downloading | importing | done | 
**Status** | **string** | pending | running | done | failed | 
**Total** | **long** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

