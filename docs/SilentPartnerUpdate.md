# Org.OpenAPITools.Model.SilentPartnerUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContractDate** | **DateOnly?** | Datum des Vertragsabschlusses. | [optional] 
**Einlage** | **string** | Einlage (§ 230 HGB). | [optional] 
**GewinnquotePct** | **string** | Gewinnbeteiligungsquote in Prozent (§ 231 HGB). | [optional] 
**Gewinnvortrag** | **string** | Nicht erhobene Gewinne (§ 232 Abs. 3 HGB). | [optional] 
**InstrumentType** | **InstrumentType** | Instrument: \&quot;typisch\&quot; | \&quot;atypisch\&quot; | \&quot;partiarisches_darlehen\&quot; | \&quot;genussrecht\&quot;. | [optional] 
**KestPflichtig** | **bool?** | 25 % Kapitalertragsteuer einbehalten (§ 43 Abs. 1 Nr. 3 EStG; typisch + partiarisches Darlehen). | [optional] 
**Name** | **string** | Name des stillen Gesellschafters. | [optional] 
**Notes** | **string** | Freitext-Notizen. | [optional] 
**VerlustVerrechnungskonto** | **string** | Kumulierte Verluste gegen die Einlage (§ 232 Abs. 2 HGB, ≤ Einlage). | [optional] 
**Verlustbeteiligung** | **bool?** | Verlustbeteiligung (§ 231 Abs. 2 HGB; kann ausgeschlossen werden). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

