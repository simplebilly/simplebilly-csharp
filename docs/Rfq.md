# Org.OpenAPITools.Model.Rfq

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **string** |  | [optional] 
**LineItems** | **Object** | JSON array of &#x60;{product_id, name, sku, quantity, requested_unit_price?, quoted_unit_price?}&#x60;. | 
**Notes** | **string** |  | [optional] 
**RequestedDate** | **DateOnly** |  | 
**ResponseDate** | **DateOnly?** |  | [optional] 
**RfqNumber** | **string** |  | 
**Status** | **RfqStatus** | One of: draft | sent | offer_received | rejected | converted | 
**SupplierContactId** | **string** | References the supplier entity. | [optional] 
**SupplierName** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

