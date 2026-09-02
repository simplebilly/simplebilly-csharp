# Org.OpenAPITools.Model.Activity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityType** | **ActivityType** | One of: call | email | meeting | task | note | 
**AssignedTo** | **string** | User responsible (&#x60;employee.employee_id&#x60;). | [optional] 
**ContactId** | **string** | Contact this activity belongs to (&#x60;contact.contact_id&#x60;). References the contact entity. | [optional] 
**Description** | **string** |  | [optional] 
**DueDate** | **DateOnly?** | Follow-up / Wiedervorlage date. Open activities with a due date in the past are overdue. | [optional] 
**ReminderDate** | **DateOnly?** | When to remind about the follow-up. | [optional] 
**Status** | **ActivityStatus** | One of: open | done | cancelled | 
**Subject** | **string** | Short subject line. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

