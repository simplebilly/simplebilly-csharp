# Org.OpenAPITools.Model.GenerateVariantsRequest
Request body for generating the full variant set from option values.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Options** | **Dictionary&lt;string, List&lt;string&gt;&gt;** | Option name → list of values, e.g. &#x60;{\&quot;Color\&quot;: [\&quot;Red\&quot;, \&quot;Blue\&quot;], \&quot;Size\&quot;: [\&quot;S\&quot;, \&quot;M\&quot;]}&#x60;. The cartesian product of these lists is generated. | [optional] 
**PriceDelta** | **string** | Optional per-variant price delta applied to every generated variant. | [optional] 
**ProductId** | **Guid** |  | 
**SkuPrefix** | **string** | Optional prefix for the generated SKUs (suffix is the option values joined by &#x60;-&#x60;). Falls back to the parent product&#39;s SKU. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

