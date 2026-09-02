# Org.OpenAPITools.Model.ProductionOrderCosting
Actual-costing (Nachkalkulation) report for a production order.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CostPerUnit** | **string** | material_cost_total ÷ quantity. | 
**CostSource** | **string** | \&quot;actual\&quot; when costed from stock-movement consumption, else \&quot;planned\&quot;. | 
**Lines** | [**List&lt;CostingLine&gt;**](CostingLine.md) |  | 
**MarginPerUnit** | **string** | sale_price − cost_per_unit. | [optional] 
**MarginPercent** | **string** | margin_per_unit ÷ cost_per_unit as a percentage. | [optional] 
**MaterialCostTotal** | **string** | Total material cost for the whole order. | 
**OrderNumber** | **string** |  | 
**ProductionOrderId** | **Guid** |  | 
**Quantity** | **long** |  | 
**SalePrice** | **string** | Finished product&#39;s sale price per unit (used to compute margin). | [optional] 
**Status** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

