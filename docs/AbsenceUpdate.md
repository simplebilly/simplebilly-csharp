# Org.OpenAPITools.Model.AbsenceUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AbsenceType** | **AbsenceType** | One of \&quot;vacation\&quot;, \&quot;sick\&quot;, \&quot;sabbatical\&quot;, \&quot;parental\&quot;, \&quot;other\&quot;. | [optional] 
**ApprovedAt** | **DateTime?** |  | [optional] 
**ApprovedBy** | **Guid?** | References the user entity. | [optional] 
**EmployeeId** | **Guid?** | References the employee entity. | [optional] 
**EndDate** | **DateOnly?** |  | [optional] 
**Notes** | **string** |  | [optional] 
**StartDate** | **DateOnly?** |  | [optional] 
**Status** | **AbsenceStatus** | One of \&quot;pending\&quot;, \&quot;approved\&quot;, \&quot;rejected\&quot;, \&quot;cancelled\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

