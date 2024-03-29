---
description: Een histogram lijkt op een staafdiagram, maar het groepeert getallen in bereiken (emmers).
title: Histogram
feature: Visualizations
exl-id: 5901eb15-51cf-45a0-a80b-5824adf33bdd
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Histogram

Een histogram lijkt op een staafdiagram, maar het groepeert getallen in bereiken (emmers). Analytics automatiseert de &#39;bucketing&#39; van getallen in bereiken, maar u kunt de instellingen wijzigen in [Geavanceerde instellingen](#section_09D774C584864D4CA6B5672DC2927477).

## Een histogram maken {#section_74647707CC984A1CB6D3097F43A30B45}

Een histogram maken:

1. Klikken **[!UICONTROL Visualizations]** in het linkerspoor.
1. Slepen **[!UICONTROL Histogram]** in het deelvenster.
1. Kies een metrisch teken dat u naar de histogram wilt slepen en klik op **[!UICONTROL Build]**.

![Leeg histogram, deelvenster met een metrisch veld onder Daling.](assets/histogram.png)

>[!NOTE]
>
>Histogrammen ondersteunen alleen standaardmeetwaarden, geen berekende meetwaarden.

Hier hebben we de metagegevens voor paginaweergaven gebruikt voor unieke bezoekers. Het eerste (linker) emmertje komt overeen met een paginaweergave per unieke persoon, het tweede emmertje met twee paginaweergaven, enzovoort.

![](assets/histogram2.png)

## Geavanceerde instellingen {#section_09D774C584864D4CA6B5672DC2927477}

Als u uw histogram-instellingen wilt aanpassen, klikt u op het pictogram Instellingen (&quot;versnelling&quot;) in de rechterbovenhoek. Hier volgen de instellingen die u kunt wijzigen:

| Histograminstellingen | Wat het doet |
|---|---|
| Emmertje starten | Hiermee bepaalt u met welk emmertje het histogram begint. &quot;1&quot; is de standaardwaarde. U kunt begingetallen instellen van 0 tot oneindig (geen negatieve getallen). |
| Metrische emmertjes | Hiermee kunt u het aantal gegevensbereiken (emmers) vergroten/verkleinen. Het maximumaantal emmers is 50. |
| Grootte van metrisch emmertje | Hiermee kunt u de grootte van elk emmertje instellen. U kunt bijvoorbeeld de emmergrootte wijzigen van de paginaweergave 1 in de weergave van 2 pagina&#39;s. |
| Telmethode | Hiermee kunt u kiezen uit [Bezoeker](https://experienceleague.adobe.com/docs/analytics/components/metrics/unique-visitors.html), [Bezoek](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html), of Type Actief. Paginaweergaven per bezoek of pagina per persoon of paginaweergaven per gebeurtenis. Bij Actief wordt &quot;Voorvallen&quot; gebruikt als de metrische y-as in een vrije-vormtabel. |

<!--Russ or Meike - Check Hit Type link above. -->

**Voorbeelden**:

* Startemmertje: 1; Metrische emmers: 5; Metrische Emmergrootte: 2 resulteert in dit histogram: 1-2, 3-4, 5-6, 7-8, 9-10.
* Startemmertje: 0; Metrische emmers: 3; Metrische Emmergrootte: 5 resulteert in dit histogram: 0-4, 5-9, 10-14

## Histogramgegevens weergeven en bewerken {#section_B2CD7CDF0F6B432F928103AE7AAA3617}

Als u de gegevensbron voor het histogramdiagram wilt weergeven of wijzigen, klikt u op de punt naast de kop van het histogram om naar **[!UICONTROL Data Source Settings]** > **[!UICONTROL Show Data Source]**.

![Instellingen gegevensbron met Selectie weergeven en Selectie vergrendelen geselecteerd.](assets/manage-data-source.png)

Vooraf samengestelde filters die in de tabel worden weergegeven, zijn interne filters die niet worden weergegeven in de filterkiezer. Klik op het pictogram &quot;i&quot; naast de filternaam en klik vervolgens op **[!UICONTROL Make public]** om het filter openbaar te maken.

![Segmenten die het bewerkvenster en de koppeling Openbaar maken weergeven.](assets/prebuilt_segments.png)

Ga voor meer manieren om gegevenstabellen en andere visualisaties in Freeform te beheren, zoals het uitvoeren van gegevensonderverdelingen, naar [hier](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html).

## Blogbericht

Zie dit blogbericht over informatie op [gebruiken histogrammen om onverwachte gegevenswaarden te identificeren](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/using-histograms-to-identify-unexpected-data-values/ba-p/596168).
