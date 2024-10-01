---
description: Een histogram lijkt op een staafdiagram, maar het groepeert getallen in bereiken (emmers).
title: Histogram
feature: Visualizations
exl-id: 5901eb15-51cf-45a0-a80b-5824adf33bdd
role: User
source-git-commit: 5b441472a21db99728d012c19f12d98f984086f5
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 2%

---

# Histogram {#histogram}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_workspace_histogram_button"
>title="Histogram"
>abstract="Maak een histogramvisualisatie om de distributie van numerieke gegevens in groepen bereiken weer te geven."

<!-- markdownlint-enable MD034 -->


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

In het onderstaande voorbeeld wordt een histogram gebruikt om sessies voor het aantal personen te emmeren. Het histogram toont aan dat de meeste personen tussen 16 en 21 zittingen voor de geselecteerde gegevenswaaier hebben.

![](assets/histogram.png)

## Geavanceerde instellingen {#section_09D774C584864D4CA6B5672DC2927477}

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
