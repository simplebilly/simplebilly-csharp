# Org.OpenAPITools.Model.ReturnOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerContactId** | **string** | References the contact entity. | [optional] 
**CustomerName** | **string** |  | [optional] 
**LineItems** | **Object** | JSON array of &#x60;{product_id, name, quantity, condition, restock, batch_number?}&#x60;. | [optional] 
**Notes** | **string** |  | [optional] 
**OrderId** | **string** | References the order entity. | [optional] 
**OrderNumber** | **string** |  | [optional] 
**ReturnNumber** | **string** |  | 
**ReturnReason** | **string** |  | [optional] 
**Status** | **ReturnOrderStatus** | One of: requested | received | inspected | restocked | closed | 
**WarehouseId** | **string** | Warehouse into which restockable items are returned. References the warehouse entity. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

