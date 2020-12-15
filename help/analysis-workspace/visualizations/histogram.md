---
description: Een histogram is een nieuw visualisatietype in Analysis Workspace.
title: Histogram
uuid: 8a6bd2c4-da15-4f64-b889-ab9add685046
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 3%

---


# Histogram

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Een histogram lijkt op een staafdiagram, maar het groepeert getallen in bereiken (emmers). Analytics automatiseert de &quot;bucketing&quot;van aantallen in waaiers, maar u kunt de montages in [Geavanceerde Montages](#section_09D774C584864D4CA6B5672DC2927477) veranderen.

## Een histogram maken {#section_74647707CC984A1CB6D3097F43A30B45}

Een histogram maken:

1. Klik op **[!UICONTROL Visualizations]** in de linkertrack.
1. Sleep **[!UICONTROL Histogram]** naar het deelvenster.
1. Kies een metrisch teken om naar de histogram te slepen en klik op **[!UICONTROL Build]**.

![](assets/histogram.png)

>[!NOTE]
>
>Histogrammen ondersteunen alleen standaardmeetwaarden, geen berekende meetwaarden.

Hier hebben we de metagegevens voor paginaweergaven gebruikt voor unieke bezoekers. Het eerste (linker) emmertje komt overeen met een paginaweergave per unieke bezoeker, het tweede emmertje met twee paginaweergaven, enzovoort.

![](assets/histogram2.png)

## Geavanceerde instellingen {#section_09D774C584864D4CA6B5672DC2927477}

Als u uw histogram-instellingen wilt aanpassen, klikt u op het pictogram Instellingen (&quot;versnelling&quot;) in de rechterbovenhoek. Hier volgen de instellingen die u kunt wijzigen:

| Histograminstellingen | Wat het doet |
|---|---|
| Emmertje starten | Hiermee bepaalt u met welk emmertje het histogram begint. &quot;1&quot; is de standaardwaarde. U kunt begingetallen instellen van 0 tot oneindig (geen negatieve getallen). |
| Metrische emmertjes | Hiermee kunt u het aantal gegevensbereiken (emmers) vergroten/verkleinen. Het maximumaantal emmers is 50. |
| Grootte van metrisch emmertje | Hiermee kunt u de grootte van elk emmertje instellen. U kunt bijvoorbeeld de emmergrootte wijzigen van de paginaweergave 1 in de weergave van 2 pagina&#39;s. |
| Telmethode | Hiermee kunt u kiezen uit [Visitor](https://docs.adobe.com/content/help/en/analytics/components/metrics/unique-visitors.html), [Visit](https://docs.adobe.com/content/help/en/analytics/components/metrics/visits.html) of Type Actief. Paginaweergaven per bezoek of pagina per bezoeker of pagina worden bijvoorbeeld weergegeven per hit. Bij Actief wordt &quot;Voorvallen&quot; gebruikt als de metrische y-as in een vrije-vormtabel. |

<!--Russ or Meike - Check Hit Type link above. -->

**Voorbeelden**:

* Emmertje starten: 1; Metrische emmers: 5; Grootte metrische Emmertje: 2 resulteert in dit histogram: 1-2, 3-4, 5-6, 7-8, 9-10.
* Emmertje starten: 0; Metrische emmers: 3. Grootte metrische Emmertje: 5 resulteert in dit histogram: 0-4, 5-9, 10-14

## Histogramgegevens weergeven en bewerken {#section_B2CD7CDF0F6B432F928103AE7AAA3617}

Als u de gegevensbron voor het histogramdiagram wilt weergeven of wijzigen, klikt u op de punt naast de kop van het histogram om naar **[!UICONTROL Data Source Settings]** > **[!UICONTROL Show Data Source]** te gaan.

![](assets/manage-data-source.png)

Vooraf gebouwde segmenten die in de lijst verschijnen zijn interne segmenten en zullen niet omhoog in de selecteur van het Segment verschijnen. Klik op het pictogram &quot;i&quot; naast de segmentnaam en klik vervolgens op **[!UICONTROL Make public]** om het segment openbaar te maken.

![](assets/prebuilt_segments.png)

Ga [hier](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) voor meer manieren om gegevenstabellen en andere visualisaties te beheren, zoals het uitvoeren van gegevensuitsplitsingen.
