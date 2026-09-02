# Org.OpenAPITools.Model.EmployeeCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | **string** |  | [optional] 
**BackupEmployeeId** | **Guid?** | References another employee who covers when this employee is absent. | [optional] 
**Bic** | **string** |  | [optional] 
**City** | **string** |  | [optional] 
**Country** | **CountryCode** |  | [optional] 
**DateOfBirth** | **DateOnly?** |  | [optional] 
**DepartmentId** | **Guid** | References the department entity. | [optional] 
**Email** | **string** |  | [optional] 
**FirstName** | **string** |  | [optional] 
**Gender** | **Gender** | Gender for pay-transparency reporting: \&quot;male\&quot;, \&quot;female\&quot; or \&quot;diverse\&quot;. | [optional] 
**HireDate** | **DateOnly?** |  | [optional] 
**HourlyCost** | **string** | Hourly cost rate in EUR for labor-cost reporting; when unset the rate is derived from &#x60;monthly_salary / (weekly_hours * 4.33)&#x60;. | [optional] 
**Iban** | **string** |  | [optional] 
**JobTitle** | **string** |  | [optional] 
**LastLogin** | **DateTime?** |  | [optional] 
**LastName** | **string** |  | [optional] 
**LastUpdated** | **DateTime?** |  | [optional] 
**MonthlySalary** | **string** | Gross monthly salary in EUR for pay-transparency reporting. | [optional] 
**Phone** | **string** |  | [optional] 
**State** | **string** |  | [optional] 
**Status** | **EmployeeStatus** |  | [optional] 
**UserId** | **Guid?** | References the user entity. | [optional] 
**WeeklyHours** | **string** | Contractual weekly working hours for pay-transparency normalization. | [optional] 
**Zip** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

