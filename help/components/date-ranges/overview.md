---
title: Overzicht van datumbereiken
description: Leer welke datumbereiken zijn en hoe u deze kunt gebruiken in rapporten.
feature: Calendar
exl-id: 99b31bd9-32f1-4da1-9e47-6d90c66282c5
role: User
source-git-commit: 747e77b964006404d70b500b28ec44005d65d944
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Overzicht van datumbereiken

In een project van Workspace, gebruikt u typisch de [ kalender in een paneel ](/help/analysis-workspace/c-panels/panels.md#calendar) om de datumwaaier voor de visualisaties in dat paneel te specificeren.

Met datumbereikcomponenten kunt u de kalenderinstellingen voor het deelvenster definiëren en overschrijven.

<!-- Very old video, should we show it?

+++ View a video illustrating use of calendar and date ranges

>[!VIDEO](https://video.tv.adobe.com/v/24136?format=jpeg)

{{videoaa}}
+++

-->

## Datumbereiken gebruiken

U kunt een component met datumbereik gebruiken om de kalender voor het deelvenster opnieuw te definiëren.

Of u kunt een datumbereik in een tabel met vrije vorm gebruiken als metrisch of als een dimensie.

![ het waaiergebruik van de Datum ](/help/components/date-ranges/assets/date-ranges-usage.png)

- **Metrisch**. Bijvoorbeeld, om een afmeting voor twee verschillende maanden voor specifieke metrisch te vergelijken.
- **Dimension**. Om metrisch op verschillende afmetingspunten voor de afmeting van de datumwaaier te vergelijken.

>[!NOTE]
>
>Wanneer u datumbereiken in een tabel met vrije vorm gebruikt, overschrijven de datumbereiken de kalender die is opgegeven voor het deelvenster waartoe de tabel met vrije vorm behoort.
>

U gebruikt een datumwaaier aangezien u [ om het even welke component ](/help/components/overview.md#analysis-workspace-components) zou gebruiken. U sleept de datumwaaier van het ](/help/assets/icons/Calendar.svg) 2} componentenpaneel van de Kalender ![ en laat vallen de component op:**[!UICONTROL Date ranges]**

- **[!UICONTROL Calendar]**: U ![ Schakelaar ](/help/assets/icons/Switch.svg) **[!UICONTROL Replace]** de huidige kalenderconfiguratie met de datumwaaier.
- **Metrische kolomkopbal**: U ![ Schakelaar ](/help/assets/icons/Switch.svg) **[!UICONTROL Replace]** metrisch, ![ voegt ](/help/assets/icons/Add.svg)**[!UICONTROL Add]**de datumwaaier als metrisch toe, of ![ filter ](/help/assets/icons/Filter.svg)**[!UICONTROL Filter]**metrisch gebruikend de component van de datumwaaier.
- **de kolomkopbal van het Dimension**: U ![ Schakelaar ](/help/assets/icons/Switch.svg) **[!UICONTROL Replace]** de huidige afmetingen. De nieuwe dimensie is nu **[!UICONTROL Date ranges]** . Zodra de afmeting de waaiers van de Datum is, kunt u ](/help/assets/icons/Add.svg)**[!UICONTROL Add]**extra datumwaaiers als afmetingspunten toevoegen ![.
- **punt van het Dimension**: U ![ Uitsplitsing ](/help/assets/icons/Breakdown.svg) **[!UICONTROL Breakdown]** het specifieke afmetingspunt door de datumwaaier.

U kunt ook rechtstreeks een kolom voor het datumbereik toevoegen in een visualisatie voor de tabel Vrije vorm:

1. In een metrische kolom, selecteer van het contextmenu:

   - **[!UICONTROL Add time period column]**. U kunt tussen voorgestelde opties selecteren die op de huidige kalender gebaseerd zijn of a [ waaier van de douanedatum ](#custom-date-ranges) creëren.
   - **[!UICONTROL Compare time periods]**. U kunt tussen een voorgestelde optie selecteren die op de huidige kalender gebaseerd is of a [ waaier van de douanedatum ](#custom-date-ranges) creëren.

1. Op basis van uw selectie worden extra kolommen voor het datumbereik toegevoegd aan de tabel Vrije vorm.

## Standaarddatumbereiken

Analysis Workspace biedt een aantal standaarddatumbereiken.


| Dag | Week | Maand | Kwart | Jaar |
|---|---|---|---|---|
| Vandaag | Deze week | Deze maand | Dit kwartaal | Dit jaar |
| Gisteren | Deze week (behalve vandaag) | Deze maand (behalve vandaag) | Dit kwartaal (exclusief vandaag) | Dit jaar (behalve vandaag) |
| 2 dagen geleden | 2 weken geleden | 2 maanden geleden |   |  |
| 3 dagen geleden | 3 weken geleden | 3 maanden geleden |  | |
| Laatste 7 dagen | Vorige week | Vorige maand | Laatste kwartaal | Vorig jaar |
| Laatste 14 dagen | Afgelopen 2 volledige weken | Laatste 2 volledige maanden | Afgelopen 4 volledige kwartalen | |
| Laatste 30 dagen | Afgelopen 3 volledige weken | Laatste 3 volledige maanden | | |
| Laatste 60 dagen | Laatste 4 volledige weken | Laatste 6 volledige maanden | | |
| Laatste 90 dagen | Afgelopen 12 volledige weken | Laatste 12 volledige maanden | | |
| Laatste 7 volledige dagen | Afgelopen 52 volledige weken | Laatste 13 volledige maanden | | |
| Laatste 14 volledige dagen | | | | |
| Laatste 30 volledige dagen | | | | |
| Laatste 90 volledige dagen | | | | |

<table style="table-layout:fixed">

## Aangepaste datumbereiken

U kunt uw eigen aangepaste datumbereiken maken. Zie [ datumwaaier ](/help/components/date-ranges/create.md) voor de diverse opties tot stand brengen beschikbaar om datumwaaiers tot stand te brengen. U bouwt dan, wijzigt, en bewaart datumwaaiers in de [ de waaierbouwer van de Datum ](create.md#date-range-builder).

U gebruikt de [ manager van de waaier van de Datum ](manage.md) om datumwaaiers te beheren.
