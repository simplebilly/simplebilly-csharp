# Org.OpenAPITools.Model.EmissionsReport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ByCategory** | [**List&lt;CategoryTotal&gt;**](CategoryTotal.md) |  | 
**ByScope** | [**List&lt;ScopeTotal&gt;**](ScopeTotal.md) |  | 
**ByYear** | [**List&lt;YearTotal&gt;**](YearTotal.md) |  | 
**DataQuality** | [**DataQuality**](DataQuality.md) |  | 
**IntensityPerEmployee** | **double?** |  | [optional] 
**IntensityPerRevenueMio** | **double?** | tCO2e per million EUR net revenue. | [optional] 
**NetRevenue** | **double?** | Sum of paid/sent/partially-paid invoices (EUR net) in the year. | [optional] 
**SpendBasedEstimateTco2e** | **double?** | Spend-based estimate from bookkeeping payments (EXIOBASE factor). | [optional] 
**Targets** | [**List&lt;TargetProgress&gt;**](TargetProgress.md) |  | 
**TotalTco2e** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

