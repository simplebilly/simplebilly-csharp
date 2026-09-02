# Org.OpenAPITools.Model.Bom

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Components** | **Object** | JSON array of &#x60;{product_id, name, quantity, unit, scrap_rate}&#x60;. | [optional] 
**Description** | **string** |  | [optional] 
**Name** | **string** |  | 
**OutputQuantity** | **long** | Output quantity per production run (defaults to 1). | [optional] 
**ProductId** | **Guid** | The finished product this BOM produces. References the product entity. | 
**Status** | **BomStatus** | One of: draft | active | archived | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

