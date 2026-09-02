# Org.OpenAPITools.Model.SupportTicket

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssignedTo** | **Guid?** |  | [optional] 
**ChannelId** | **Guid?** |  | [optional] 
**ChannelType** | **SupportChannelType** |  | [optional] 
**ClosedAt** | **DateTime?** |  | [optional] 
**CreatedAt** | **DateTime** |  | 
**CustomerEmail** | **string** |  | [optional] 
**CustomerId** | **string** | References the customer entity. | [optional] 
**CustomerName** | **string** |  | [optional] 
**ExternalId** | **string** |  | [optional] 
**FirstMessageAt** | **DateTime** |  | 
**LastMessageAt** | **DateTime** |  | 
**LeadId** | **Guid?** | References the lead entity. | [optional] 
**MessageCount** | **int** |  | 
**OrderRef** | **string** |  | [optional] 
**Priority** | **TicketPriority** |  | 
**Resolution** | **string** |  | [optional] 
**Status** | **SupportTicketStatus** |  | 
**Subject** | **string** |  | 
**Tags** | **Object** |  | 
**TenantId** | **Guid** |  | 
**UpdatedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

