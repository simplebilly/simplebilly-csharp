# Org.OpenAPITools.Model.PurchaseOrderCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **string** |  | [optional] 
**DeliveryAddress** | **Object** |  | [optional] 
**ExpectedDeliveryDate** | **DateOnly?** |  | [optional] 
**LineItems** | **Object** | JSON array of &#x60;{product_id, name, quantity, unit_price_net, tax_rate, delivery_date}&#x60;. | [optional] 
**Notes** | **string** |  | [optional] 
**OrderDate** | **DateOnly** |  | 
**PoNumber** | **string** |  | 
**Status** | **PurchaseOrderStatus** | One of: draft | ordered | partially_received | received | cancelled | 
**SupplierContactId** | **string** | References the supplier entity. | [optional] 
**SupplierName** | **string** |  | [optional] 
**TotalGrossAmount** | **string** |  | [optional] 
**TotalNetAmount** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

