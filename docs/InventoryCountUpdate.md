# Org.OpenAPITools.Model.InventoryCountUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CountDate** | **DateOnly?** |  | [optional] 
**CountNumber** | **string** |  | [optional] 
**LineItems** | **Object** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. | [optional] 
**Notes** | **string** |  | [optional] 
**Status** | **InventoryCountStatus** | One of: draft | counting | reviewed | posted | [optional] 
**WarehouseId** | **string** | References the warehouse entity. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

