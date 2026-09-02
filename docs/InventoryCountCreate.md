# Org.OpenAPITools.Model.InventoryCountCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CountDate** | **DateOnly** |  | 
**CountNumber** | **string** |  | 
**LineItems** | **Object** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. | 
**Notes** | **string** |  | [optional] 
**Status** | **InventoryCountStatus** | One of: draft | counting | reviewed | posted | 
**WarehouseId** | **string** | References the warehouse entity. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

