---
title: Standaardcomponentverwijzing
description: Details en informatie over alle standaardcomponenten die u kunt toevoegen aan elke gegevensweergave.
source-git-commit: 86522f1ea5ae241351514d954672ec5fd7990944
workflow-type: tm+mt
source-wordcount: '523'
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
| [!UICONTROL People] | Metrisch | Gebaseerd op de persoonID in [!UICONTROL Connection] wordt gespecificeerd. |
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

Optionele standaardcomponenten zijn beschikbaar onder **[!UICONTROL Data views]** > **[!UICONTROL Edit data view]** > **[!UICONTROL Components]** tab > **[!UICONTROL Standard Components]** tab.

| Componentnaam | Dimension of metrisch | Notities |
| --- | --- | --- |
| [!UICONTROL Session Starts] | Metrisch | Het aantal gebeurtenissen dat de eerste gebeurtenis van een sessie was. Indien gebruikt in een filterdefinitie (bv. &#39;[!UICONTROL Session Starts] bestaat&#39;), het filters neer tot enkel de eerste gebeurtenis van elke zitting. |
| [!UICONTROL Session Ends] | Metrisch | Het aantal gebeurtenissen dat de laatste gebeurtenis van een sessie was. Net als [!UICONTROL Session Starts], kan deze ook worden gebruikt in een filterdefinitie om items tot aan de laatste gebeurtenis van elke sessie te filteren. |
| [!UICONTROL Time Spent (seconds)] | Metrisch | Hiermee wordt de tijd tussen twee verschillende waarden voor een dimensie samengevat. |
| [!UICONTROL Time Spent per Event] | Dimension | Sluit [!UICONTROL Time Spent] metrisch in [!UICONTROL Event] emmers. |
| [!UICONTROL Time Spent per Session] | Dimension | Sluit [!UICONTROL Time Spent] metrisch in [!UICONTROL Session] emmers. |
| [!UICONTROL Time Spent per Person] | Dimension | Sluit [!UICONTROL Time Spent] metrisch in [!UICONTROL Person] emmers. |
| [!UICONTROL Batch ID] | Dimension | Vertegenwoordigt de partij van het Experience Platform dat een [!UICONTROL Event] deel van was. |
| [!UICONTROL Dataset ID] | Dimension | Vertegenwoordigt de dataset van het Experience Platform dat een [!UICONTROL Event] deel van was. |