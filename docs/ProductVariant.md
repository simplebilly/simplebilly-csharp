# Org.OpenAPITools.Model.ProductVariant

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Barcode** | **string** |  | [optional] 
**ImageLink** | **string** |  | [optional] 
**IsActive** | **bool** |  | [optional] 
**Name** | **string** | Human-readable variant label, e.g. \&quot;Red / M\&quot;. | [optional] 
**OptionValues** | **Object** | Option name → value map, e.g. &#x60;{\&quot;Color\&quot;: \&quot;Red\&quot;, \&quot;Size\&quot;: \&quot;M\&quot;}&#x60;. | [optional] 
**Price** | **string** | Explicit override price for this variant (takes precedence over parent price + delta). | [optional] 
**PriceDelta** | **string** | Price adjustment relative to the parent product&#39;s &#x60;default_price&#x60;. | [optional] 
**ProductId** | **Guid** | The parent product this variant belongs to. References the product entity. | 
**Sku** | **string** | Variant-specific SKU (must be unique per tenant). | 
**StockQuantity** | **long?** | Variant-level stock (optional — may be tracked on the parent only). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

