# Org.OpenAPITools.Model.CustomerCommunicationUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Body** | **string** | The message body, call summary or note text. | [optional] 
**Channel** | **CommunicationChannel** |  | [optional] 
**ContactId** | **string** | The contact (customer/supplier) this communication belongs to. References the contact entity. | [optional] 
**Counterparty** | **string** | Email/phone of the counterparty, if applicable. | [optional] 
**Direction** | **CommunicationDirection** |  | [optional] 
**OccurredAt** | **DateTime?** | When the communication happened (defaults to now on create). | [optional] 
**Subject** | **string** |  | [optional] 
**Tags** | **Object** | Free-form tags, e.g. &#x60;[\&quot;follow-up-required\&quot;]&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

