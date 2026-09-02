# Org.OpenAPITools.Model.SupplierCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **string** | Currency for the minimum order value. | 
**DeliveryTerms** | **string** | Incoterms, e.g. \&quot;EXW\&quot;, \&quot;DAP\&quot;. | [optional] 
**EarlyPaymentDiscountPercent** | **string** | Early-payment discount percentage (Skonto), e.g. 2.0. | [optional] 
**IsDefault** | **bool** | Is this the default condition for the supplier? | [optional] 
**MinimumOrderValue** | **string** | Minimum order value required for this supplier. | [optional] 
**Notes** | **string** |  | [optional] 
**PaymentDueDays** | **int?** | Number of days within which payment is due. | [optional] 
**PaymentTerms** | **string** | Payment terms, e.g. \&quot;14 Tage, 2% Skonto\&quot;. | [optional] 
**SupplierContactId** | **string** | The supplier this condition applies to (&#x60;contact_id&#x60;). References the supplier entity. | 
**SupplierName** | **string** | The name of the supplier, denormalized for easy listing. | [optional] 
**VolumeDiscountTiers** | **Object** | Tiered discounts: JSON array of &#x60;{min_quantity, discount_percent}&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

