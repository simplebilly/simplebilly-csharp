# Org.OpenAPITools.Model.ProductionOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BomId** | **Guid?** | References the BOM entity. | [optional] 
**Components** | **Object** | JSON snapshot of the BOM components at creation time. | [optional] 
**EndDate** | **DateOnly?** |  | [optional] 
**Notes** | **string** |  | [optional] 
**OrderNumber** | **string** |  | 
**ProductId** | **Guid** | The finished product to manufacture. References the product entity. | 
**Quantity** | **long** | Quantity of finished product to produce. | 
**SourceWarehouseId** | **string** | Warehouse components are consumed from. References the warehouse entity. | [optional] 
**StartDate** | **DateOnly?** |  | [optional] 
**Status** | **ProductionOrderStatus** | One of: planned | in_production | completed | cancelled | [optional] 
**TargetWarehouseId** | **string** | Warehouse the finished product is added to. References the warehouse entity. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

