# Org.OpenAPITools.Model.QuotaOverride
Schema of the `tenants.quotas` JSON override column. Any field that is present overrides the plan-derived value.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Features** | [**QuotaOverrideFeatures**](QuotaOverrideFeatures.md) |  | [optional] 
**MaxConnectors** | **int?** |  | [optional] 
**MaxInvoicesPerMonth** | **long?** |  | [optional] 
**MaxUsers** | **int?** |  | [optional] 
**Metered** | **Dictionary&lt;string, long&gt;** |  | [optional] 
**Plan** | **string** | Custom plan id; unknown ids resolve to enterprise limits. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

