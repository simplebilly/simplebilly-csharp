# Org.OpenAPITools.Model.ServiceAssignment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EmployeeId** | **Guid** | References the employees entity. | [optional] 
**JobId** | **Guid** | References the service_jobs entity. | [optional] 
**Notes** | **string** |  | [optional] 
**ScheduledDate** | **DateOnly** | Work day the assignment is scheduled for. | [optional] 
**ScheduledEnd** | **string** | Planned end time of the assignment. | [optional] 
**ScheduledStart** | **string** | Planned start time of the assignment. | [optional] 
**Status** | **ServiceAssignmentStatus** | Assignment lifecycle status: \&quot;planned\&quot;, \&quot;confirmed\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot; or \&quot;cancelled\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

