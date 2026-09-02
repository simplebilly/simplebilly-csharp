# Org.OpenAPITools.Model.ShippingRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Carrier** | **string** | Provider that auto-filled this rule (e.g. \&quot;ups\&quot;), if any. | [optional] 
**Country** | **CountryCode** | None &#x3D; applies to all countries. | [optional] 
**DeliveryTime** | **string** | Delivery time text, e.g. \&quot;1-3\&quot;. | [optional] 
**IsActive** | **bool** |  | [optional] 
**MaxWeightKg** | **double?** |  | [optional] 
**MinWeightKg** | **double?** |  | [optional] 
**Name** | **string** | Delivery-method label, e.g. \&quot;Standardversand\&quot;. | 
**Notes** | **string** |  | [optional] 
**Price** | **string** | Shipping cost in the shop&#39;s currency. | 
**Priority** | **int** | Lower wins when multiple rules match. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

