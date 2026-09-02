# Org.OpenAPITools.Model.CreateTicketRequest
Request body for creating a support ticket. Wraps the generated `SupportTicketCreateDto` fields plus `message_body` which is not a Model field (used to create the initial `ticket_message`).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **Guid?** |  | [optional] 
**ChannelType** | **string** |  | [optional] 
**CustomerEmail** | **string** |  | [optional] 
**CustomerId** | **string** |  | [optional] 
**CustomerName** | **string** |  | [optional] 
**ExternalId** | **string** |  | [optional] 
**MessageBody** | **string** |  | 
**OrderRef** | **string** |  | [optional] 
**Subject** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

