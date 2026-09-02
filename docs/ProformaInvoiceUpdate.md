# Org.OpenAPITools.Model.ProformaInvoiceUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConvertedAt** | **DateTime?** |  | [optional] 
**ConvertedToInvoiceId** | **string** | Set when the proforma was converted into a real invoice. References the invoice entity. | [optional] 
**Currency** | **CurrencyCode** |  | [optional] 
**CustomerId** | **string** | References the customer entity. | [optional] 
**CustomerSnapshot** | **Object** | Snapshot of the recipient at issue time (address, VAT id, …). | [optional] 
**IssueDate** | **DateOnly?** |  | [optional] 
**LineItems** | **Object** |  | [optional] 
**Notes** | **string** |  | [optional] 
**OrderNumber** | **string** | Reference to the order/quote this proforma belongs to. | [optional] 
**PaymentDueDate** | **DateOnly?** | Optional deadline the real invoice should carry after conversion. | [optional] 
**QuotationId** | **string** | References the quotation entity. | [optional] 
**Status** | **ProformaInvoiceStatus** | &#x60;draft&#x60; | &#x60;sent&#x60; | &#x60;converted&#x60;. | [optional] 
**Subtotal** | **string** |  | [optional] 
**TotalAmount** | **string** |  | [optional] 
**TotalTax** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

