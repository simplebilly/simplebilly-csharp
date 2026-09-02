# Org.OpenAPITools.Model.StockTransfer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LineItems** | **Object** | JSON array of &#x60;{product_id, name, quantity, batch_number?}&#x60;. | 
**Notes** | **string** |  | [optional] 
**SourceWarehouseId** | **string** | References the warehouse entity. | 
**Status** | **StockTransferStatus** | One of: draft | completed | cancelled | 
**TargetWarehouseId** | **string** | References the warehouse entity. | 
**TransferDate** | **DateOnly** |  | 
**TransferNumber** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

