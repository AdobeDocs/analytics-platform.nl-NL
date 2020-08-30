---
description: Creeer de waaiers van de douanedatum in de Werkruimte van de Analyse, en sla hen als componenten van de Tijd op.
keywords: Analysis Workspace
title: Aangepaste datumbereiken maken
topic: Reports and analytics
uuid: c8873d41-454d-4f22-ad1f-38cacec5a3bc
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 3%

---


# Aangepaste datumbereiken maken

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Creeer de waaiers van de douanedatum in de Werkruimte van de Analyse, en sla hen als componenten van de Tijd op.

**[!UICONTROL Components]** > **[!UICONTROL New Date Range]**

Op paneelniveau is een datumbereik van toepassing. Om een datumwaaier aan uw project toe te voegen, klik **Panels** > *`<select panel>`*, en geef een nieuw datumbereik op.

## Datumbereik voor &quot;twee maanden geleden&quot;

De volgende waaier van de douanedatum toont een datumwaaier voor &quot;twee maanden geleden,&quot;met een Summiere visualisatie die van de Verandering richtingsverandering toont.

![](assets/date-range-two-months-ago.png)

De waaier van de douanedatum wordt getoond bij de bovenkant van [!UICONTROL Date Range] componentpaneel in uw project:

![](assets/date-range-panel-two-months-ago.png)

U kunt deze waaier van de douanedatum in een kolom naast een douane slepen, maandelijkse het rollen datumwaaier gebruikend de Laatste vooraf ingestelde Maand voor een vergelijking. Voeg een Summiere Visualisatie van de Verandering toe en selecteer de totalen van elke kolom om richtingsverandering te tonen:

![](assets/date-range-two-months-table.png)

## Gebruik een roldatumbereik van 7 dagen

Een datumwaaier is op het paneelniveau van toepassing. Om een datumwaaier aan uw project toe te voegen, klik **Acties** > **Panel toevoegen**, en geef een nieuw datumbereik op.

In de Bouwer van de Waaier van de Datum, kunt u een waaier van de douanedatum tot stand brengen die in het paneel van Componenten met andere datumwaaiers toont.

Bijvoorbeeld, kunt u een datumwaaier creëren die een 7 dag het rollen venster specificeert dat één week geleden beëindigt:

![](assets/create_date_range.png)

Gebruik *`rolling daily`*.

* De instellingen voor het begin zijn: *`current day minus 14 days`*.

* De montages van het Eind zouden zijn *`current day minus 7 days`*.

Deze datumwaaier kan een component zijn die u op om het even welke vrije vormlijst sleept.
