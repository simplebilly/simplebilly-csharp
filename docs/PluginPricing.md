# Org.OpenAPITools.Model.PluginPricing
How a plugin is priced in the marketplace. Tagged on `type` so the same enum deserializes both the API DTO and the `plugin_marketplace.json` manifest (`{\"type\":\"free\"}` / `{\"type\":\"one_time\",\"price\":99.0}` / `{\"type\":\"recurring\",\"price_per_month\":19.9}`).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Price** | **double** |  | 
**PricePerMonth** | **double** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

