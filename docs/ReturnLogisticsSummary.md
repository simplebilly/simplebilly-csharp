# Org.OpenAPITools.Model.ReturnLogisticsSummary
Warehouse-level aggregation for the returns logistics dashboard.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ByStatus** | **Object** | Number of return orders per status. | 
**ByWarehouse** | [**List&lt;ReturnWarehouseSummary&gt;**](ReturnWarehouseSummary.md) | Per-warehouse aggregation. | 
**ItemsRestocked** | **long** | Sum of &#x60;restock: true&#x60; line-item quantities. | 
**ItemsScrapped** | **long** | Sum of &#x60;restock: false&#x60; line-item quantities (scrapped/disposed). | 
**TotalItems** | **long** | Sum of all line-item quantities across returns. | 
**TotalReturns** | **long** | Total number of return orders (excluding soft-deleted). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

