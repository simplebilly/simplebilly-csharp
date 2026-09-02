# Org.OpenAPITools.Model.TaxRateCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CountryCode** | **string** | ISO 3166-1 alpha-2 country code. | 
**EffectiveFrom** | **DateOnly?** | Date this rate took effect; &#x60;None&#x60; &#x3D; not date-bound. | [optional] 
**IsDefault** | **bool** | Default rate for the country (one per country); fallback for lookups when no dated rate applies. | 
**Name** | **string** | Human name, e.g. \&quot;VAT\&quot;. | 
**RatePercent** | **long** | Rate in hundredths of a percent: 1900 &#x3D; 19.00%. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

