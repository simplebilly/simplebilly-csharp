# Org.OpenAPITools.Model.CostingLine
A single costing line: material cost for one BOM component.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LineCost** | **string** | total_quantity × unit_purchase_price (0 when price unknown). | 
**Name** | **string** |  | 
**ProductId** | **Guid** |  | 
**QuantityPerUnit** | **long** | Component quantity required per finished unit. | 
**Sku** | **string** |  | 
**TotalQuantity** | **long** | Total component quantity consumed by this order. | 
**UnitPurchasePrice** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

