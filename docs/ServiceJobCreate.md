# Org.OpenAPITools.Model.ServiceJobCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | **string** | Street + zip + city of the job location. | [optional] 
**CustomerEmail** | **string** | Customer email for email notifications. | [optional] 
**CustomerId** | **Guid?** | References the customer entity. | [optional] 
**CustomerName** | **string** | Denormalized customer name for quick display. | [optional] 
**CustomerPhone** | **string** | Customer phone for SMS notifications later. | [optional] 
**Description** | **string** | What work needs to be done. | [optional] 
**EstimatedDurationMinutes** | **int** | Estimated time for the job in minutes. | [optional] 
**Lat** | **double?** | Latitude for map display (OpenStreetMap). | [optional] 
**Lng** | **double?** | Longitude for map display (OpenStreetMap). | [optional] 
**Notes** | **string** |  | [optional] 
**Status** | **ServiceJobStatus** | Dispatch status: \&quot;pending\&quot;, \&quot;assigned\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot;, \&quot;cancelled\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

