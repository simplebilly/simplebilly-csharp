# Org.OpenAPITools.Model.KonzernStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Groessenbefreit** | **bool** |  | 
**Kapitalmarktorientiert** | **bool** |  | 
**Konzernabschlusspflicht** | **bool** |  | 
**MissingGroupFigures** | **bool** | Keine group_figures-Zeile für das Jahr vorhanden → keine Größenbefreiung. | 
**Mutterunternehmen** | **bool** | Mutterunternehmen: mindestens eine beherrschte Beteiligung (§ 290 Abs. 1 HGB). | 
**ParentName** | **string** | Mutterunternehmen für die Zwischenholding-Befreiung (§ 291 HGB). | [optional] 
**ParentSitus** | **string** |  | [optional] 
**Participations** | [**List&lt;KonzernBeteiligung&gt;**](KonzernBeteiligung.md) |  | 
**Thresholds** | [**KonzernThresholds**](KonzernThresholds.md) |  | 
**Year** | **int** |  | 
**ZwischenholdingBefreit** | **bool** |  | 
**ZwischenholdingHinweis** | **string** | Hinweis zu den § 291-Voraussetzungen (EU/EWR-Sitz, geprüfter Konzernabschluss). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

