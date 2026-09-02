# Org.OpenAPITools.Model.Absence

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AbsenceType** | **AbsenceType** | One of \&quot;vacation\&quot;, \&quot;sick\&quot;, \&quot;sabbatical\&quot;, \&quot;parental\&quot;, \&quot;other\&quot;. | [optional] 
**ApprovedAt** | **DateTime?** |  | [optional] 
**ApprovedBy** | **Guid?** | References the user entity. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**DeletedAt** | **DateTime?** |  | [optional] 
**EmployeeId** | **Guid** | References the employee entity. | [optional] 
**EndDate** | **DateOnly** |  | [optional] 
**Id** | **Guid** |  | [optional] 
**Notes** | **string** |  | [optional] 
**StartDate** | **DateOnly** |  | [optional] 
**Status** | **AbsenceStatus** | One of \&quot;pending\&quot;, \&quot;approved\&quot;, \&quot;rejected\&quot;, \&quot;cancelled\&quot;. | [optional] 
**TenantId** | **Guid** |  | [optional] 
**UpdatedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

