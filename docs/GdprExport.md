# Org.OpenAPITools.Model.GdprExport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityLog** | [**List&lt;GdprActivity&gt;**](GdprActivity.md) |  | 
**ApiKeys** | [**List&lt;GdprApiKey&gt;**](GdprApiKey.md) | Key identifiers and names only — never a usable credential. | 
**Billing** | [**List&lt;GdprBillingInfo&gt;**](GdprBillingInfo.md) |  | 
**ExportedAt** | **DateTime** |  | 
**GeneratedByAi** | **bool** | Honesty field: this document is a plain data dump, never AI-generated. | 
**Notifications** | [**List&lt;GdprNotification&gt;**](GdprNotification.md) |  | 
**RefreshTokens** | [**List&lt;GdprRefreshToken&gt;**](GdprRefreshToken.md) | Session records: metadata only, never the token hash. | 
**Tenants** | [**List&lt;GdprTenant&gt;**](GdprTenant.md) |  | 
**UsageEvents** | [**List&lt;GdprUsageEvent&gt;**](GdprUsageEvent.md) |  | 
**User** | [**GdprUser**](GdprUser.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

