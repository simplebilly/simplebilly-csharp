# Org.OpenAPITools.Model.JobApplication

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CvFile** | **string** | Relative path of the stored CV file under the upload dir. | [optional] 
**CvText** | **string** | Extracted CV text, used for match-scoring. | [optional] 
**Email** | **string** |  | [optional] 
**MatchReason** | **string** |  | [optional] 
**MatchScore** | **int?** | 0-100 LLM match score against the posting&#39;s required profile. | [optional] 
**Name** | **string** |  | [optional] 
**Phone** | **string** |  | [optional] 
**PostingId** | **Guid?** | References the job_posting entity. | [optional] 
**Source** | **string** | website | email | board | 
**Status** | **ApplicationStatus** | new | reviewing | interview | hired | rejected | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

