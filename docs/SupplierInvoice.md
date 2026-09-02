# Org.OpenAPITools.Model.SupplierInvoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **string** |  | [optional] 
**GoodsReceiptId** | **string** | References the goods receipt entity. | [optional] 
**InvoiceDate** | **DateOnly** |  | 
**InvoiceNumber** | **string** |  | 
**LineItems** | **Object** | JSON array of &#x60;{product_id, name, quantity, unitPriceNet, taxRate}&#x60;. | 
**Notes** | **string** |  | [optional] 
**PurchaseOrderId** | **string** | References the purchase order entity. | [optional] 
**Status** | **SupplierInvoiceStatus** | One of: draft | matched | has_variances | posted | cancelled | 
**SupplierContactId** | **string** | References the supplier entity. | [optional] 
**SupplierName** | **string** |  | [optional] 
**TotalGrossAmount** | **string** |  | [optional] 
**TotalNetAmount** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

