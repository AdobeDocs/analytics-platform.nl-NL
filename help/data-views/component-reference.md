---
title: Standaardcomponentverwijzing
description: Details en informatie over alle standaardcomponenten die u kunt toevoegen aan elke gegevensweergave.
exl-id: e23ce27a-77ab-4641-a126-93f00d4e6e14
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: c36dddb31261a3a5e37be9c4566f5e7ec212f53c
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Standaardcomponentverwijzing

De meeste afmetingen en metriek in CJA zijn gebaseerd op schemaelementen van uw dataset van Adobe Experience Platform. Er zijn echter verschillende componenten beschikbaar om aan een gegevensweergave toe te voegen, ongeacht de verbinding die u gebruikt.

[!UICONTROL Standard components] zijn componenten die niet van de gebieden van het datasetschema worden geproduceerd maar in plaats daarvan geproduceerd systeem. Sommige systeemonderdelen zijn vereist om de rapportagemogelijkheden in Analysis Workspace te vergemakkelijken, terwijl andere systeemonderdelen optioneel zijn.

![Standaardonderdelen](assets/standard-components.png)

## Vereiste standaardonderdelen

Deze vereiste standaardcomponenten worden standaard toegevoegd aan elke gegevensweergave. Ze zijn essentieel voor de rapportagemogelijkheden die Customer Journey Analytics biedt.

| Componentnaam | Dimension of metrisch | Notities |
| --- | --- | --- |
| [!UICONTROL People] | Metrisch | Gebaseerd op de persoon-id die is opgegeven in een [!UICONTROL Connection]. |
| [!UICONTROL Sessions] | Metrisch | Gebaseerd op de de zittingsmontages van de gegevensmening. |
| [!UICONTROL Events] | Metrisch | Het aantal rijen van alle gebeurtenisdatasets in a [!UICONTROL Connection]. |
| [!UICONTROL Minute] | Dimension | De minuut dat een bepaalde gebeurtenis heeft plaatsgevonden (naar beneden afgerond). Het eerste afmetingspunt is de eerste minuut in de datumwaaier, en het laatste afmetingspunt is de laatste minuut in de datumwaaier. |
| [!UICONTROL Hour] | Dimension | Het uur dat een bepaalde gebeurtenis heeft plaatsgevonden (naar beneden afgerond). Het eerste afmetingspunt is het eerste uur in de datumwaaier, en het laatste afmetingspunt is het laatste uur in de datumwaaier. |
| [!UICONTROL Day] | Dimension | De dag waarop een bepaalde gebeurtenis plaatsvond. Het eerste afmetingspunt is de eerste dag in de datumwaaier, en het laatste afmetingspunt is de laatste dag in de datumwaaier. |
| [!UICONTROL Week] | Dimension | De week waarin een bepaalde gebeurtenis plaatsvond. Het eerste dimensie-item is de eerste week in het datumbereik en het laatste dimensie-item is de laatste week in het datumbereik. |
| [!UICONTROL Month] | Dimension | De maand waarin een bepaalde gebeurtenis heeft plaatsgevonden. Het eerste afmetingspunt is de eerste maand in de datumwaaier, en het laatste afmetingspunt is de laatste maand in de datumwaaier. |
| [!UICONTROL Quarter] | Dimension | Het kwart dat een bepaalde gebeurtenis heeft plaatsgevonden. De post van de eerste dimensie is het eerste kwartaal in het datumbereik, en de laatste dimensie is het laatste kwartaal in het datumbereik. |
| [!UICONTROL Year] | Dimension | Het jaar waarin een bepaalde gebeurtenis plaatsvond. De eerste dimensie-post is het eerste jaar in het datumbereik, en de laatste dimensie-post is het meest recente jaar in het datumbereik. |

## Optionele standaardonderdelen

Optionele standaardonderdelen zijn beschikbaar onder **[!UICONTROL Data views]** > **[!UICONTROL Edit data view]** > **[!UICONTROL Components]** tab > **[!UICONTROL Standard Components]** tab.

| Componentnaam | Dimension of metrisch | Notities en waarden |
| --- | --- | --- |
| [!UICONTROL AM/PM] | Afmeting van tijd-paring | AM of PM |
| [!UICONTROL Batch ID] | Dimension | Vertegenwoordigt de partij van het Experience Platform die [!UICONTROL Event] maakte deel uit van. |
| [!UICONTROL Dataset ID] | Dimension | Vertegenwoordigt de dataset van het Experience Platform die een [!UICONTROL Event] maakte deel uit van. |
| [!UICONTROL Day of Month] | Afmeting van tijd-paring | 1-31 |
| [!UICONTROL Day of Week] | Afmeting van tijd-paring | Maandag, dinsdag, woensdag, donderdag, vrijdag, zaterdag, zondag |
| [!UICONTROL Day of Year] | Afmeting van tijd-paring | 1-366 |
| [!UICONTROL Hour of Day] | Afmeting van tijd-paring | 0-23 |
| [!UICONTROL  Month of Year] | Afmeting van tijd-paring | Januari - december |
| [!UICONTROL Person ID] | Dimension | Voor elk gegevenssetschema dat in het Experience Platform is gedefinieerd, kan een eigen set met een of meer identiteiten zijn gedefinieerd en gekoppeld aan een naamruimte Identiteit. Elk van deze kan worden gebruikt als de persoon-id. Voorbeelden zijn Cookie-id, Stitched ID, Gebruikersnaam, Trackingcode enzovoort. De [!UICONTROL Person ID] dimensie is de basis voor het combineren van gegevenssets en het identificeren van unieke bezoekers in CJA.<p>Mogelijke gebruiksgevallen zijn:<ul><li>Het creëren van een filter op een specifieke waarde van persoonidentiteitskaart om alles tot het gedrag van die gebruiker te filtreren.</li><li>Foutopsporing: ervoor zorgen dat de gegevens voor een specifieke cookie-id (of een specifieke klant-id) aanwezig zijn.</li><li>Het identificeren van de gebruikers die binnen aan een vraagcentrum riepen.</li></ul> |
| [!UICONTROL Person ID namespace] | Dimension | Welk type van identiteitskaart [!UICONTROL Person ID] bestaat uit: Voorbeelden: `email address`, `cookie ID`, `Analytics ID`, enz. |
| [!UICONTROL Quarter of Year] | Afmeting van tijd-paring | Q1, Q2, Q3, Q4 |
| [!UICONTROL Session Starts] | Metrisch | Het aantal gebeurtenissen dat de eerste gebeurtenis van een sessie was. Indien gebruikt in een filterdefinitie (bv. &#39;[!UICONTROL Session Starts] bestaat&#39;), filtert het tot enkel de eerste gebeurtenis van elke zitting. |
| [!UICONTROL Session Ends] | Metrisch | Het aantal gebeurtenissen dat de laatste gebeurtenis van een sessie was. Vergelijkbaar met [!UICONTROL Session Starts], kan het ook in een filterdefinitie worden gebruikt om dingen tot de laatste gebeurtenis van elke zitting te filtreren. |
| [!UICONTROL Time Spent (seconds)] | Metrisch | Hiermee wordt de tijd tussen twee verschillende waarden voor een dimensie samengevat. |
| [!UICONTROL Time Spent per Event] | Dimension | Emmert de [!UICONTROL Time Spent] metrisch in [!UICONTROL Event] emmers. |
| [!UICONTROL Time Spent per Session] | Dimension | Emmert de [!UICONTROL Time Spent] metrisch in [!UICONTROL Session] emmers. |
| [!UICONTROL Time Spent per Person] | Dimension | Emmert de [!UICONTROL Time Spent] metrisch in [!UICONTROL Person] emmers. |
| [!UICONTROL Weekend]/[!UICONTROL Weekday] | Afmeting van tijd-paring | Weekend of Weekdag |
