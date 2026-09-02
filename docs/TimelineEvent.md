# Org.OpenAPITools.Model.TimelineEvent
Single timeline entry aggregated from the contact's activity across all related modules (communications, quotations, orders, invoices, documents).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **string** | RFC3339 UTC timestamp for sorting. | 
**Detail** | **string** |  | [optional] 
**Id** | **string** | Source record id (stringified). | 
**Status** | **string** |  | [optional] 
**Title** | **string** |  | 
**Type** | **string** | Source module: communication | quotation | order | invoice | attachment. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

