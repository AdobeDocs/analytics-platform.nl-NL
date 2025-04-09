---
description: Een histogram lijkt op een staafdiagram, maar het groepeert getallen in bereiken (emmers).
title: Histogram
feature: Visualizations
exl-id: 5901eb15-51cf-45a0-a80b-5824adf33bdd
role: User
source-git-commit: c94e97723a4ed30e675144e02196c93016b13235
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 2%

---

# Histogram {#histogram}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_histogram_button"
>title="Histogram"
>abstract="Maak een histogramvisualisatie om de verdeling van numerieke gegevens in groepen bereiken weer te geven."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_In dit artikel wordt de histogramvisualisatie in_ ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics** beschreven._<br/>_Zie [Histogram](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/histogram) voor de_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics-versie** van dit artikel._

>[!ENDSHADEBOX]


De ![histogramvisualisatie](/help/assets/icons/Histogram.svg) **[!UICONTROL Histogram]** is vergelijkbaar met een [!UICONTROL Bar] visualisatie, maar groepeert getallen in bereiken (buckets). Analytics automatiseert het &#39;indelen&#39; van getallen in bereiken, maar u kunt de instellingen wijzigen in [Geavanceerde instellingen](#advanced-settings).

## Gebruiken

Een histogram maken:

1. Voeg a ![ Histogram ](/help/assets/icons/Histogram.svg) **[!UICONTROL Histogram]** visualisatie toe. Zie [ een visualisatie aan een paneel ](freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.
1. Sleep metrisch van de **[!UICONTROL Metrics]** componentenlijst, of selecteer metrisch van [!UICONTROL *een metrisch*] dropdown menu toevoegen.
1. (optioneel) Selecteer **[!UICONTROL Show advanced settings]** . Zie [ Geavanceerde montages ](#advanced-settings).
1. Selecteer **[!UICONTROL Build]** .

>[!NOTE]
>
>Histogrammen ondersteunen alleen standaardstatistieken, geen berekende statistieken.

In het onderstaande voorbeeld wordt een histogram gebruikt om sessies te bucketen voor het aantal personen. Het histogram laat zien dat de meeste personen tussen de 16-21 sessies hebben voor het geselecteerde datumbereik.

![Histogram](assets/histogram.png)

## Geavanceerde instellingen

Als onderdeel van de visualisatie zijn specifieke histograminstellingen beschikbaar.

| Instellingen voor histogrammen | Beschrijving |
|---|---|
| **[!UICONTROL Starting bucket]** | Hiermee bepaalt u met welk emmertje het histogram begint. &quot;1&quot; is de standaardwaarde. U kunt begingetallen instellen van 0 tot oneindig (geen negatieve getallen). |
| **[!UICONTROL Metric buckets]** | Hiermee kunt u het aantal gegevensbereiken (emmers) vergroten/verkleinen. Het maximumaantal emmers is 50. |
| **[!UICONTROL Metric bucket size]** | Hiermee kunt u de grootte van elke emmer instellen. U kunt bijvoorbeeld de grootte van de bucket wijzigen van 1 paginaweergave naar 2 paginaweergaven. |
| **[!UICONTROL Counting method]** | Kies uit **[!UICONTROL Global Account]** [!BADGE B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, [!BADGE **[!UICONTROL Account]** B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, **[!UICONTROL Buying Group]** [!BADGE B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, **[!UICONTROL Opportunity]** [!BADGE B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, **[!UICONTROL Person]**, **[!UICONTROL Session]** of **[!UICONTROL Event]**. Bijvoorbeeld paginaweergaven per account [!BADGE B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, paginaweergaven per sessie, of paginaweergaven per persoon, of paginaweergaven per evenement. |

<!--Russ or Meike - Check Hit Type link above. -->

**Voorbeelden**:

| Startbak | Metrische emmers | Grootte van metrische emmer | Resultaat |
|:----:|:--:|:--:|:--|
| 1 | 5 | 2 | ![Histogram, startbak 1, metrische bakken 5, metrische bak maat 2](assets/histogram-1-5-2.png) |
| 0 | 3 | 5 | ![ Histogram, beginnend emmer 0, metrische emmers 3, metrische emmer grootte 5 ](assets/histogram-0-3-5.png) |

>[!MORELIKETHIS]
>
>[ voeg een visualisatie aan een paneel toe ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Visualisatie-instellingen](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Visualisatie contextmenu](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>[Histogrammen gebruiken om onverwachte gegevenswaarden te identificeren](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/using-histograms-to-identify-unexpected-data-values/ba-p/596168)

