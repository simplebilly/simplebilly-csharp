# Org.OpenAPITools.Model.Model

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BackupCodes** | **List&lt;string&gt;** |  | 
**CreatedAt** | **DateTime** |  | 
**DeletedAt** | **DateTime?** |  | [optional] 
**Email** | **string** |  | 
**EmailVerified** | **bool** |  | 
**Id** | **Guid** |  | 
**IsActive** | **bool** |  | 
**IsTotpEnabled** | **bool** |  | 
**LastLogin** | **DateTime?** |  | [optional] 
**Name** | **string** |  | 
**OauthId** | **string** |  | [optional] 
**OauthProvider** | **string** |  | [optional] 
**PasswordChangedAt** | **DateTime?** | Set on password change; auth/refresh tokens issued before this timestamp are rejected by the auth middleware. | [optional] 
**PasswordHash** | **string** |  | 
**Picture** | **string** |  | [optional] 
**PrivacyAcceptedAt** | **DateTime?** | When the user accepted the data privacy policy (GDPR consent record). | [optional] 
**TotpSecret** | **string** |  | [optional] 
**UpdatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

