---
title: Verbindingen beheren
description: Beschrijft hoe te om verbindingen aan de datasets van het Experience Platform in Customer Journey Analytics (CJA) te beheren.
mini-toc-levels: 3
exl-id: 0a87518c-3608-44ad-b5e3-976f97560433
source-git-commit: b0e07ca9533a2d53c916c6db31acaccbd78a41a3
workflow-type: tm+mt
source-wordcount: '1339'
ht-degree: 0%

---

# Verbindingen beheren

Zodra Admin gebruikers [één of meerdere verbindingen](/help/connections/create-connection.md) hebben gecreeerd, kunnen zij hen in [!UICONTROL Connections] Manager beheren. De recentste update aan de ervaring van de Verbinding voegt twee belangrijke mogelijkheden binnen de pagina van de Details van de Verbinding toe, die verder op deze pagina wordt beschreven:

* Het laat u de **status van de datasets van uw verbinding en van het innameproces** controleren. Deze statuscontrole laat u weten wanneer uw gegevens beschikbaar zijn zodat u naar Analysis Workspace kunt gaan en de analyse kunt starten.

* Het laat u **om het even welke gegevensdiscrepanties** wegens verkeerde configuratie identificeren. Ontbreekt u rijen? Zo ja, welke rijen ontbreken en waarom? Hebt u verbindingen verkeerd gevormd en ontbrekende gegevens in CJA veroorzaakt?

>[!NOTE]
> Deze functionaliteit is over het algemeen beschikbaar op 20 september 2021.

## Verbindingsbeheer {#connections-manager}

Met de Connections Manager kunt u:

* Bekijk al uw verbindingen bij een blik, met inbegrip van de eigenaar, de zandbak, en toen zij werden gecreeerd en werden gewijzigd.
* Alle gegevenssets weergeven in een verbinding.
* Controleer de status van een verbinding.
* Een verbinding verwijderen.
* Wijzig de naam van een verbinding.
* Maak een gegevensweergave via een verbinding.

![Verbindingen beheren](assets/conn-manager.png)

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Name] | De vriendschappelijke naam van de verbinding. Wanneer u op de naam van de hyperlink klikt, gaat u naar de pagina Verbindingsdetails die hieronder wordt beschreven. |
| Verbindingsinfo | Klik op het infopictogram naast de naam van de verbinding om de volgende informatie weer te geven:![Verbindingsgegevens weergeven](assets/conn-info.png) |
| Een verbinding bewerken | Klik op de ellips (...) naast de naam van de verbinding en klik vervolgens op [!UICONTROL Edit].![Bewerk ](assets/conn-edit-delete.png) verbindingZie &quot;Verbinding bewerken&quot; hieronder voor meer informatie. |
| Een verbinding verwijderen | Klik op de ellips (...) naast de naam van de verbinding en klik vervolgens op [!UICONTROL Delete]. Meer informatie vindt u onder de kop Verbindingen verwijderen hieronder. |
| Gegevensweergave maken | Klik op de ellips (...) naast de naam van de verbinding en klik vervolgens op [!UICONTROL Create data view]. Met deze actie maakt u een nieuwe gegevensweergave op basis van deze verbinding. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html?lang=en) |
| [!UICONTROL Datasets] | De datasets die deel van de verbinding uitmaken. U kunt op de hyperlink klikken om alle datasets in de verbinding weer te geven. Als u op een gegevensset klikt, wordt die gegevensset in Adobe Experience Platform geopend op een nieuw tabblad. |
| [!UICONTROL Sandbox] | De [Adobe Experience Platform-sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=en) waaruit deze verbinding de gegevenssets tekent. Deze sandbox werd geselecteerd toen u de verbinding voor het eerst maakte. Het kan niet worden gewijzigd. |
| [!UICONTROL Owner] | De persoon die de verbinding heeft gemaakt. |
| [!UICONTROL Import Data Sets] | Hiermee kunt u in- of uitschakelen wat voorheen &#39;gegevensstreaming&#39; werd genoemd. |
| [!UICONTROL Date Created] | De datum waarop de verbinding voor het eerst is gemaakt. |
| [!UICONTROL Last Modified] | De datum waarop de verbinding voor het laatst is bijgewerkt. |

### Verbindingen verwijderen {#connections-delete}

Alleen beheerders hebben toestemming om een verbinding te verwijderen. Deze handeling wordt niet weergegeven voor niet-beheerders.

1. Klik op de ellips (...) naast de naam van de verbinding.
1. Klik op [!UICONTROL Delete].

Wanneer u een verbinding in [!UICONTROL Customer Journey Analytics] schrapt, zal een foutenmelding erop wijzen dat:

* Gegevensweergaven die zijn gemaakt op basis van de verwijderde verbinding, werken niet meer.
* Op dezelfde manier zullen om het even welke projecten van de Werkruimte die van gegevensmeningen in de geschrapte verbinding afhangen ophouden werkend.

[Leer ](/help/getting-started/cja-deletion.md) meer over schrappingsimplicaties.

### Zoeken naar een verbinding of gegevensset

U kunt naar verbindingen zoeken gebruikend de bar van het Onderzoek bij de bovenkant, onder de [!UICONTROL Connections] titel.

### Verbindingen sorteren

U kunt verbindingen sorteren door op elke kolomkop te klikken en omhoog of omlaag te sorteren.

## Pagina Verbindingsgegevens {#connection-detail}

De nieuwe pagina van de Details van Verbindingen geeft u een zeer gedetailleerde mening van de status van een verbinding.

Hiermee kunt u:

* Controleer de status van de datasets van uw verbinding en van het innameproces.
* Identificeer configuratieproblemen die tot overgeslagen, of geschrapte verslagen leiden.
* Zie wanneer de gegevens beschikbaar zijn voor rapportage.

Hier worden de widgets en instellingen beschreven:

![Verbindingsdetails weergeven](assets/conn-details.png)

| Widget/Setting | Beschrijving |
| --- | --- |
| Gegevensset selecteren | Hiermee kunt u een of alle gegevenssets in de verbinding kiezen. U kunt geen datasets selecteren. Wordt standaard ingesteld op [!UICONTROL All datasets]. |
| Kalender-/datumbereiken | Het datumbereik geeft aan wanneer u gegevens hebt toegevoegd aan de verbinding. Alle standaardkalendervoorinstellingen worden opgenomen. U kunt het datumbereik aanpassen, maar in de vervolgkeuzelijst worden geen aangepaste datumbereiken weergegeven. |
| [!UICONTROL Records available] widget | Vertegenwoordigt het totale aantal rijen beschikbaar voor rapportering, **voor de volledige verbinding**. Deze telling is onafhankelijk van enige kalendermontages. Het verandert als u een dataset van de datasetselecteur selecteert of door een dataset in de lijst te selecteren. (Let op: er is een latentie van 1-2 uur om de gegevens weer te geven in de rapportage, zodra deze is toegevoegd.) |
| [!UICONTROL Metrics] widget | Hiermee geeft u een overzicht van de records die zijn toegevoegd/overgeslagen/verwijderd en het aantal toegevoegde batches, **voor de gegevensset en het datumbereik dat u hebt geselecteerd**. |
| [!UICONTROL Records added] widget | Geeft aan hoeveel rijen zijn toegevoegd in de geselecteerde tijdsperiode, **voor de gegevensset en het datumbereik dat u hebt geselecteerd**. Om de 10 minuten bijgewerkt. |
| [!UICONTROL Records skipped] widget | Geeft aan hoeveel rijen zijn overgeslagen in de geselecteerde tijdsperiode, **voor de gegevensset en het datumbereik dat u hebt geselecteerd**. Redenen voor het overslaan van records zijn: Tijdstempels ontbreken, persoon-id ontbreekt enzovoort. Om de 10 minuten bijgewerkt. |
| [!UICONTROL Records deleted] widget | Geeft aan hoeveel rijen zijn verwijderd in de geselecteerde tijdsperiode, **voor de gegevensset en het datumbereik dat u hebt geselecteerd**. Iemand heeft bijvoorbeeld een dataset in Experience Platform verwijderd. Om de 10 minuten bijgewerkt. |
| Zoekvak voor gegevensset | U kunt zoeken op naam van gegevensset of [!UICONTROL Dataset ID]. |
| [!UICONTROL Datasets] | Toont de datasets die deel van de verbinding uitmaken. U kunt op de hyperlink klikken om alle datasets in de verbinding weer te geven. |
| [!UICONTROL Dataset ID] | Deze id wordt automatisch gegenereerd door Adobe Experience Platform. |
| [!UICONTROL Batches] | Geeft aan hoeveel gegevensbatches aan deze gegevensset zijn toegevoegd. |
| [!UICONTROL Last added] | Toont timestamp voor de laatste toegevoegde partij aan deze dataset. |
| [!UICONTROL Dataset type] | Het gegevenstype van de dataset voor deze dataset kan [!UICONTROL Event], [!UICONTROL Lookup], of [!UICONTROL Profile] zijn. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en#configure-dataset) |
| Schema | Het Adobe Experience Platform-schema waarop de gegevenssets in deze verbinding zijn gebaseerd. |
| **Rechterspoor op verbindingsniveau** |  |
| [!UICONTROL Refresh] | Vernieuw de verbinding zodat onlangs toegevoegde verslagen worden weerspiegeld. |
| [!UICONTROL Delete] | Verwijder deze verbinding. |
| [!UICONTROL Create data view] | Maak een nieuwe gegevensweergave op basis van deze verbinding. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html?lang=en) |
| [!UICONTROL Connection Name] | Toont de vriendschappelijke naam van de verbinding. |
| [!UICONTROL Connection description] | Toont een meer gedetailleerde beschrijving die ideaal het doel van deze verbinding beschrijft. |
| [!UICONTROL Person ID] | Toont een identiteit die in het datasetschema in het Experience Platform werd bepaald. Dit is [!UICONTROL Person ID] u koos tijdens de verwezenlijking van de verbinding. Als u een verbinding creeert die datasets met verschillende IDs omvat, zal het melden dat weerspiegelen. Om datasets werkelijk samen te voegen, moet u het zelfde [!UICONTROL Person ID] gebruiken. |
| [!UICONTROL Sandbox] | De [Adobe Experience Platform-sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=en) waaruit deze verbinding de gegevensset(s) tekent. Deze sandbox werd geselecteerd toen u de verbinding voor het eerst maakte. Het kan niet worden gewijzigd. |
| [!UICONTROL Connection ID] | Deze id is een systeem dat is gegenereerd in Adobe Experience Platform. |
| [!UICONTROL IMS Org ID] | De [organisatie-id](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en) die is gekoppeld aan uw Experience Cloud-bedrijf dat u hebt ingericht. Vroeger genoemd &quot;login bedrijf&quot;. |
| [!UICONTROL Data views using connection] | Hier worden alle gegevensweergaven weergegeven die deze verbinding gebruiken. |
| [!UICONTROL Import new data] | Geeft aan of nieuwe batches met gegevens al dan niet moeten worden toegevoegd aan de historische gegevens (backfill). |
| **Rechterspoor op gegevenssetniveau** |  |
| [!UICONTROL Dataset description] | Beschrijft de parameters van elke dataset in deze verbinding. |
| [!UICONTROL Records available] | Vertegenwoordigt het totale aantal rijen die voor deze dataset, voor de bepaalde tijdspanne worden opgenomen die door de kalender wordt geselecteerd. Er is geen latentie in termen van het krijgen van de gegevens om in rapportering te verschijnen, zodra het wordt toegevoegd. (De uitzondering is dat wanneer u een gloednieuwe verbinding creeert, er [latentie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=en#3.-getting-data-into-customer-trip-analytics) zal zijn. |
| [!UICONTROL Records added] | Hoeveel rijen zijn toegevoegd in de geselecteerde tijdsperiode. |
| [!UICONTROL Records skipped] | Hoeveel rijen zijn overgeslagen tijdens inname in de geselecteerde tijdsperiode. |
| [!UICONTROL Record skipped errors] | De reden waarom records zijn overgeslagen, wordt hier aangegeven. Het kan gaan om ontbrekende tijdstempels, ontbrekende persoon-id, enzovoort. |
| [!UICONTROL Batches ingested] | Hoeveel gegevensbatches zijn toegevoegd aan deze gegevensset. |
| [!UICONTROL Last added] | Wanneer de laatste batch is toegevoegd. |
| [!UICONTROL Dataset type] | Ofwel [!UICONTROL Event], [!UICONTROL Lookup], of [!UICONTROL Profile]. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en#configure-dataset) |
| [!UICONTROL Schema] | Het Adobe Experience Platform-schema waarop deze gegevensset is gebaseerd. |
| [!UICONTROL Dataset ID] | Deze id is een systeem dat is gegenereerd in Adobe Experience Platform. |
| [!UICONTROL Backfill data] | Backfill (historische) gegevens worden in drie statussen bijgehouden: [!UICONTROL In queue], [!UICONTROL In progress] (met aangegeven voortgangspercentage) en [!UICONTROL Complete]. |

### Verbinding bewerken

Hiermee kunnen beheerders de verbinding bewerken. Selecteer een verbinding en klik op [!UICONTROL Edit Connection] om dit dialoogvenster te openen. Hier kunt u het volgende doen:

* Nieuwe gegevens beginnen en stoppen. Dit proces werd voorheen &quot;gegevensstreaming&quot; genoemd.
* Wijzig de naam van een verbinding.
