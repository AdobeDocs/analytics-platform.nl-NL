---
title: Controlelogboeken
description: Leer hoe u Customer Journey Analytics-auditlogs kunt weergeven en beheren.
exl-id: 360609f2-b811-49ee-ad4a-a54ceb23bfa3
feature: Privacy
role: Admin
source-git-commit: 2ef96ad194f8c7acec35bd7635c650af4370531a
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Controlelogboeken {#audit-logs}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="tools_auditlog_userid"
>title="Gebruikers-id"
>abstract="De gebruiker - identiteitskaart kan worden gevonden door de infoknoop op een logboekingang te raken die de gewenste gebruiker bevat."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="tools_auditlog_componentid"
>title="Component-id"
>abstract="De component-id kunt u vinden door op de knop Info te drukken op een logbestandvermelding die de gewenste component bevat."

<!-- markdownlint-enable MD034 -->


Om de transparantie en zichtbaarheid van de in het systeem uitgevoerde activiteiten te vergroten, kunt u in Adobe Customer Journey Analytics gebruikersactiviteiten voor verschillende services en mogelijkheden controleren in de vorm van &quot;auditlogs&quot;. Deze logboeken vormen een auditspoor dat kan helpen met het oplossen van problemenkwesties, en uw zaken kunnen effectief voldoen aan het beleid en de regelgevende vereisten van het collectieve gegevensbeheer, zoals de Wet van de Portabiliteit en van de Verantwoording van de Ziekteverzekering (HIPAA).

In een fundamentele betekenis, vertelt een controlelogboek **wie** **uitvoerde wat** actie, en **wanneer**. Elke actie die in een logboek wordt geregistreerd bevat meta-gegevens die op het actietype, datum en tijd, e-mailidentiteitskaart van de gebruiker die de actie, en extra attributen relevant voor het actietype uitvoerde.

Auditlogboeken worden 90 dagen bewaard. Daarna, worden de controlelogboeken automatisch geschrapt.

Dit onderwerp behandelt controlelogboeken in Customer Journey Analytics, met inbegrip van hoe te om hen in UI te bekijken en te beheren.

## Toegang tot auditlogboeken

Wanneer de eigenschap voor uw organisatie wordt toegelaten, worden de controlelogboeken automatisch verzameld aangezien de activiteit voorkomt. U te hoeven niet om logboekinzameling manueel toe te laten.

Als u controlelogboeken wilt weergeven en exporteren, moet u de toegangsbeheermachtiging van **[!UICONTROL Audit Logs Access]** in Adobe Console hebben gekregen. Leren hoe te om individuele toestemmingen voor de eigenschappen van Customer Journey Analytics te beheren, gelieve te verwijzen naar de [ documentatie van de toegangscontrole ](../technotes/access-control.md).

## Bekijk het controlelogboek in UI

Navigeer in Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Audit Logs]** .

Het controlelogboek voor vandaag en gisteren wordt getoond door gebrek.

![ het logboek van de Controle vandaag en gisteren benadrukkend. ](assets/audit_ui.png)

U kunt selecteren welke kolommen zichtbaar zijn door naar de kolomkiezer rechtsboven te gaan.

## Informatie over afzonderlijke logbestandvermeldingen weergeven

Dubbelklik op de knop Info (i) naast een beschrijving.

![ Logboek van de Controle die de infoknoop benadrukt. ](assets/info-button-audit.png)

De volgende items worden weergegeven:

* **[!UICONTROL Action Name]**: De actie die is uitgevoerd. Mogelijke waarden zijn:
   * API_REQUEST: Elke actie activeert een back-end API-aanvraag. Er worden details weergegeven over wat de API-aanvraag was.
   * GOEDKEURING: er is een &quot;goedkeuringshandeling&quot; uitgevoerd.
   * CREATE: Er is een handeling &quot;create&quot; uitgevoerd.
   * DELETE: er is een handeling &quot;delete&quot; uitgevoerd.
   * BEWERKEN: er is een bewerking &quot;bewerken&quot; uitgevoerd.
   * EMBARGO: Wanneer u een verzoek in de [ Rapporterende Manager van de Activiteit ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests) beperkt, wordt de actie geregistreerd in het Logboek van de Controle onder EMBARGO.
   * EXPORTEREN: er is een handeling &quot;exporteren&quot; uitgevoerd.
   * ORG_CHANGE: Er is een actie tot wijziging van de organisatie uitgevoerd.
   * REFRESH: Er is een actie &quot;vernieuwen&quot; uitgevoerd.
   * DELEN: er is een actie &quot;delen&quot; uitgevoerd.
   * OVERDRACHT: er is een overdrachtsactie uitgevoerd.
   * ONGOEDKEURING: er is een actie &quot;unaccept&quot; uitgevoerd.
   * UNSHARE: Er is een handeling &quot;unshare&quot; uitgevoerd.
* **[!UICONTROL Date Created]**: De datum en tijd waarop de actie is uitgevoerd.
* **[!UICONTROL Description]**: Een overzicht van de handeling.
* **[!UICONTROL User Name]**: De gebruiker die de handeling heeft uitgevoerd. Soms ontbreekt de gebruikersnaam. Overweeg het gebruiken van de [ eigenschap van het Gebruik van het 0} Product, aangezien het altijd de login gebruikersnaam omvat.](https://experienceleague.adobe.com/en/docs/analytics-platform/using/tools/product-usage/usage-overview)
* **[!UICONTROL Email]**: Het e-mailadres van de gebruiker die de handeling heeft uitgevoerd.
* **[!UICONTROL Component Name]**: De component waarop de gebruiker actie heeft uitgevoerd.
* **[!UICONTROL Component Type]**: Het type component. Mogelijke waarden zijn:
   * ANNOTATIE
   * AUDICE
   * CALCULATED_METRIC
   * VERBINDING
   * DATA_GROUP
   * DATA_VIEW
   * DATASET_STITCHING
   * DATE_RANGE
   * FEATURE_ACCESS
   * FILTER
   * IMS_ORG
   * MOBIEL
   * PROJECT (Workspace)
   * RAPPORT
   * SCHEDULED_PROJECT
   * GEBRUIKER
   * USER_GROUP
* **[!UICONTROL Component ID]**: De id van de component waarop de gebruiker actie heeft uitgevoerd.
* **[!UICONTROL IMS Org ID]**: De IMS-id van de organisatie, in de notatie `ABC123@AdobeOrg` .
* **[!UICONTROL Log ID]**: Een unieke id die dit logbestandvermelding identificeert.
* **[!UICONTROL User ID]**: De unieke id die de gebruiker identificeert die de handeling heeft uitgevoerd.
* **[!UICONTROL User Type]**: Het gebruikte verificatietype. Geldige waarden zijn:
   * IMS
   * OKTA

### Controllerlogboeken filteren

Selecteer het pictogram van funnel (![ filter ](assets/filter-icon.png)) om een lijst van filtercontroles te tonen om smalle resultaten te helpen. Alleen de laatste 1.000 records worden weergegeven, ongeacht de verschillende geselecteerde filters.

![ Logboek van de Controle die de filters tonen voor de Waaier van de Datum worden getoond.](assets/filters.png)

De volgende filters zijn beschikbaar voor controlegebeurtenissen in UI:

| Filter | Beschrijving |
| --- | --- |
| [!UICONTROL Date Range] | U kunt filteren op een ander datumbereik door een andere datum te selecteren of een datumbereik te selecteren door de cursor over meerdere datums te slepen. Standaard is de datum van vandaag en gisteren geselecteerd. |
| [!UICONTROL Action] | Filter op een willekeurige actienaam die hierboven wordt vermeld. |
| [!UICONTROL User ID] | Filter op een specifieke gebruiker op basis van de gebruikersnaam. U kunt de gebruikersnaam vinden door de knop info (i) naast een gebruikersnaam te selecteren. |
| [!UICONTROL Email] | Filter op het e-mailadres van een specifieke gebruiker. U kunt het e-mailbericht vinden door op de knop Info (i) naast een gebruikersnaam te klikken. |
| [!UICONTROL Component ID] | Filter op een specifieke component-id. De gebruikers-id kunt u vinden door de knop info (i) voor een gewenste component te selecteren. |
| [!UICONTROL Component Type] | Filter op elk componenttype dat hierboven wordt vermeld. |

{style="table-layout:auto"}

## Gebeurtenistypen die zijn vastgelegd in auditlogboeken

In de volgende tabel wordt aangegeven op welke handelingen componenttypen worden vastgelegd in auditlogboeken:

| Componenttype | Handelingen |
| --- | --- |
| [!UICONTROL Annotation] | <ul><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL Audience] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li><li>Exporteren</li><li>Vernieuwen</li></ul> |
| [!UICONTROL Calculated Metric] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL Connection] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL Data View] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL Date Range] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL Filter] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL IMS Org] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL Project] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL Report] | <ul><li>API_Request</li></ul> |
| [!UICONTROL Scheduled Project] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL User] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |
| [!UICONTROL User Group] | <ul><li>API_Request</li><li>Maken</li><li>Verwijderen</li><li>Bewerken</li></ul> |

{style="table-layout:auto"}

## Auditlogboeken downloaden

U kunt controlelogboeken in CSV of formaten downloaden JSON. Alle toegepaste filters of geselecteerde kolommen worden weergegeven in de gedownloade bestanden.

1. Klik op **[!UICONTROL Download]** rechtsboven in het scherm.
1. Geef de indeling op.
1. Klik nogmaals op **[!UICONTROL Download]** .

## De controlelogboeken beheren in de API

Alle acties die u in UI kunt uitvoeren kunnen ook worden gedaan gebruikend API vraag. Zie [ Customer Journey Analytics API verwijzingsdocument ](https://developer.adobe.com/cja-apis/docs/api/#tag/Audit-Logs) voor meer informatie.
