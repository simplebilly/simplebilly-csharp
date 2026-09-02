# Org.OpenAPITools.Model.EmissionEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityValue** | **string** | Activity amount in &#x60;unit&#x60; (kWh, l, km, t, tkm, EUR). | 
**CategoryId** | **string** | GHG-Protocol category key, e.g. \&quot;purchased_goods\&quot;, \&quot;business_travel\&quot;. | 
**Description** | **string** |  | 
**EfSource** | **string** | Emission-factor source, e.g. \&quot;UBA-2024\&quot;, \&quot;DEFRA-2024\&quot;. | 
**EfVersion** | **string** |  | 
**Method** | **EmissionMethod** | \&quot;activity\&quot; | \&quot;spend\&quot; | \&quot;supplier\&quot;. | 
**Scope** | **GhgScope** | GHG scope: \&quot;1\&quot; | \&quot;2\&quot; | \&quot;3\&quot;. | 
**Tco2e** | **string** | Computed server-side: activity * factor / 1000, rounded to 4 dp. | 
**Unit** | **string** | Unit of the activity value. | 
**UpdatedAt** | **DateTime?** |  | [optional] 
**Year** | **int** | Reporting year. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

