# Org.OpenAPITools.Model.Job

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Attempts** | **int** |  | [optional] 
**JobType** | **string** | Discriminator the worker dispatches on (e.g. \&quot;webhook.deliver\&quot;). | 
**MaxAttempts** | **int** |  | 
**Payload** | **Object** |  | [optional] 
**RunAt** | **DateTime?** | Earliest execution time; None &#x3D; run now. | [optional] 
**Status** | **JobStatus** | pending | running | done | failed | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

