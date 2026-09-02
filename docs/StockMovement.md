# Org.OpenAPITools.Model.StockMovement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Delta** | **long** | Signed movement: positive &#x3D; into stock, negative &#x3D; out of stock. | 
**MovementType** | **MovementType** | One of the &#x60;MOVEMENT_*&#x60; constants. | 
**ProductId** | **Guid** | References the product entity. | 
**Quantity** | **long** | Absolute quantity moved (always &gt;&#x3D; 0). | 
**Reason** | **string** |  | [optional] 
**ReferenceId** | **string** | Primary-key of the referencing entity. | [optional] 
**ReferenceType** | **ReferenceType** | Entity that caused the movement, e.g. &#x60;goods_receipt&#x60;, &#x60;stock_transfer&#x60;. | [optional] 
**WarehouseId** | **string** | References the warehouse entity. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

