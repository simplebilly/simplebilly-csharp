# Org.OpenAPITools.Model.DeliveryDateCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **string** | References the customer entity. | [optional] 
**FulfilledDate** | **DateOnly?** | Date actually delivered (set on fulfillment). | [optional] 
**Note** | **string** |  | [optional] 
**OrderNumber** | **string** | Sales order number (&#x60;order.order_number&#x60;). | 
**OriginalDate** | **DateOnly?** | Original date promised before rescheduling. | [optional] 
**ProductId** | **string** | Product line item this date applies to, if per-item. References the product entity. | [optional] 
**PromisedDate** | **DateOnly** | Date promised to the customer. | 
**Status** | **DeliveryDateStatus** | One of: promised | confirmed | rescheduled | fulfilled | late | cancelled | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

