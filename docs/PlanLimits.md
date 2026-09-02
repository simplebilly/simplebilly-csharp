# Org.OpenAPITools.Model.PlanLimits
Per-plan numeric limits. `-1` in any field means unlimited.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MaxConnectors** | **int** |  | 
**MaxInvoicesPerMonth** | **long** |  | 
**MaxUsers** | **int** |  | 
**Metered** | **Dictionary&lt;string, long&gt;** |  | [optional] 
**PaidConnectors** | **List&lt;string&gt;** | Connectors that are *not* included in this plan (require a higher tier). Empty &#x3D; all connectors included on this plan. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

