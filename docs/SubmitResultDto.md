# Org.OpenAPITools.Model.SubmitResultDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Answers** | **List&lt;int&gt;** | Selected answer indices (required for scored builtin trainings). | 
**AssignmentId** | **Guid?** |  | [optional] 
**Score** | **int** | Score 0–100. Only trusted for plugin trainings without server-side scoring; builtin trainings are always re-scored from &#x60;answers&#x60;. | 
**TrainingCode** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

