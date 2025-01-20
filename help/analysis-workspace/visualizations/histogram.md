---
description: Een histogram lijkt op een staafdiagram, maar het groepeert getallen in bereiken (emmers).
title: Histogram
feature: Visualizations
exl-id: 5901eb15-51cf-45a0-a80b-5824adf33bdd
role: User
source-git-commit: 55b312552d32070875714a77e1177bf0da5f9d87
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 2%

---

# Histogram {#histogram}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_histogram_button"
>title="Histogram"
>abstract="Maak een histogramvisualisatie om de distributie van numerieke gegevens in groepen bereiken weer te geven."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de visualisatie van de Histogram in_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._<br/>_zie [ Histogram ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/histogram) voor_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


De ![ visualisatie van de Histogram ](/help/assets/icons/Histogram.svg) **[!UICONTROL Histogram]** is gelijkaardig aan a [!UICONTROL Bar] visualisatie, maar het groepeert aantallen in waaiers (emmers). De analyse automatiseert het &quot;knippen&quot;van aantallen in waaiers, maar u kunt de montages in [ Geavanceerde Montages ](#advanced-settings) veranderen.

## Gebruiken

Een histogram maken:

1. Voeg a ![ Histogram ](/help/assets/icons/Histogram.svg) **[!UICONTROL Histogram]** visualisatie toe. Zie [ een visualisatie aan een paneel ](freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.
1. Sleep metrisch van de **[!UICONTROL Metrics]** componentenlijst, of selecteer metrisch van [!UICONTROL *een metrisch*] dropdown menu toevoegen.
1. (optioneel) Selecteer **[!UICONTROL Show advanced settings]** . Zie [ Geavanceerde montages ](#advanced-settings).
1. Selecteer **[!UICONTROL Build]** .

>[!NOTE]
>
>Histogrammen ondersteunen alleen standaardmeetwaarden, geen berekende meetwaarden.

In het onderstaande voorbeeld wordt een histogram gebruikt om sessies voor het aantal personen te emmeren. Uit het histogram blijkt dat de meeste personen tussen de 16 en 21 sessies hebben voor het geselecteerde datumbereik.

![](assets/histogram.png)

## Geavanceerde instellingen

Als onderdeel van de visualisatie zijn specifieke histograminstellingen beschikbaar.

| Histograminstellingen | Beschrijving |
|---|---|
| **[!UICONTROL Starting bucket]** | Hiermee bepaalt u met welk emmertje het histogram begint. &quot;1&quot; is de standaardwaarde. U kunt begingetallen instellen van 0 tot oneindig (geen negatieve getallen). |
| **[!UICONTROL Metric buckets]** | Hiermee kunt u het aantal gegevensbereiken (emmers) vergroten/verkleinen. Het maximumaantal emmers is 50. |
| **[!UICONTROL Metric bucket size]** | Hiermee kunt u de grootte van elk emmertje instellen. U kunt bijvoorbeeld de emmergrootte wijzigen van de paginaweergave 1 in de weergave van 2 pagina&#39;s. |
| **[!UICONTROL Counting method]** | Selecteer uit **[!UICONTROL Person]**, **[!UICONTROL Session]** of **[!UICONTROL Event]** . Bijvoorbeeld paginaweergaven per sessie, of paginaweergaven per persoon of paginaweergaven per gebeurtenis. |

<!--Russ or Meike - Check Hit Type link above. -->

**Voorbeelden**:

| Beginemmer | Metrische emmers | Grootte van metrische emmer | Resultaat |
|:----:|:--:|:--:|:--|
| 1 | 5 | 2 | ![ Histogram, beginnend emmer 1, metrische emmers 5, metrische emmer grootte 2 ](assets/histogram-1-5-2.png) |
| 0 | 3 | 5 | ![ Histogram, beginnend emmer 0, metrische emmers 3, metrische emmer grootte 5 ](assets/histogram-0-3-5.png) |

>[!MORELIKETHIS]
>
>[ voeg een visualisatie aan een paneel toe ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Visualisatie-instellingen ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Contextmenu Visualisatie ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>


## Blogbericht

Verwijs naar dit blogpost over informatie over [ gebruikend histogrammen om onverwachte gegevenswaarden ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/using-histograms-to-identify-unexpected-data-values/ba-p/596168) te identificeren.
