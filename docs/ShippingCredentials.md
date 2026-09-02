# Org.OpenAPITools.Model.ShippingCredentials
Per-tenant credentials for real shipping provider APIs (stored in the `shipping` key of the settings JSON blob). Auth is either OAuth client credentials (UPS) or a user-supplied API key (DHL).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Dhl** | [**DhlCredentials**](DhlCredentials.md) |  | [optional] 
**Ups** | [**UpsCredentials**](UpsCredentials.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

