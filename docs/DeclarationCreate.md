# Org.OpenAPITools.Model.DeclarationCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DeclarationType** | **DeclarationType** | Art der Erklärung: \&quot;dcgk\&quot; (Entsprechenserklärung § 161 AktG) oder \&quot;unternehmensfuehrung\&quot; (Erklärung zur Unternehmensführung § 289f HGB). | [optional] 
**IsCurrent** | **bool** | Kennzeichnet die aktuell gültige Fassung (max. eine je Mandant). | [optional] 
**Text** | **string** | Inhalt der Erklärung als Markdown. | [optional] 
**ValidFrom** | **DateOnly** | Datum, ab dem die Erklärung gilt. | [optional] 
**VarVersion** | **string** | Versionsbezeichnung der Erklärung (z.B. \&quot;2025-01\&quot;). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

