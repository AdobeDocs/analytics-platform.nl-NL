---
description: Gebruik de belangrijkste metrische samenvatting visualisatie om metrische prestaties over twee chronologie te vergelijken.
title: Samenvatting van metrische sleutel
feature: Visualizations
exl-id: ef606c53-b370-419a-904b-573ee6d70a8d
role: User
source-git-commit: a62ac798da9d66fa3d88262ef7d04aa4bf6a3303
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Samenvatting van metrische sleutel {#key-metric-summary}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_keymetricsummary_button"
>title="Samenvatting van metrische sleutel"
>abstract="Maak een visualisatie die een combinatie is van de diagrammen voor de regel, de samenvattingswijziging en het samenvattingsnummer. Gebruik deze visualisatie om te vergelijken hoe belangrijk de metriek tussen twee periodes trending."

<!-- markdownlint-enable MD034 -->


![ KeyMetrics ](/help/assets/icons/KeyMetrics.svg) **[!UICONTROL Key metric summary]** visualisatie laat u zien hoe belangrijke metrisch binnen één enkel tijdkader trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. Het biedt de voordelen van meerdere visualisaties die in één visualisatie worden gecombineerd:

* **[!UICONTROL Line]** visualisatie laat zien hoe de metrische waarde wordt afgenomen voor de primaire datumbereiken en de vergelijkingsdatumbereiken

* **[!UICONTROL Summary percent change]** toont de metrische toename of daling tussen de primaire en vergelijkingsdatumwaaiers

* Huidige totale waarde ([!UICONTROL **summiere aantal**]) voor metrisch

Deze visualisatie heeft betrekking op een aantal veelvoorkomende gebruiksgevallen, waaronder:

* Een analist probeert te begrijpen hoe de creatie van kansen deze maand in vergelijking met hetzelfde tijdsbestek vorig jaar eruit zag.

* Een markering die onderzoekt hoe de productie van lood voor een specifiek loodtype van deze maand in vorige maand is veranderd.

* Een uitvoerend directeur die wil begrijpen hoe nieuwe boekingen van dit kwartaal aan vorig kwartaal veranderden.

## Gebruiken

1. Voeg a ![ KeyMetrics ](/help/assets/icons/KeyMetrics.svg) **[!UICONTROL Key metric summary]** visualisatie toe. Zie [ een visualisatie aan een paneel ](freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.

1. Configureer de visualisatie door een **[!UICONTROL Metric]** , een **[!UICONTROL Primary date range]** , een **[!UICONTROL Comparison date range]** (optioneel) en een **[!UICONTROL Filter]** (optioneel) te selecteren:

   ![ Zeer belangrijke metrische configuratie die de opties voor metrisch, primaire datumwaaier, de waaier van de vergelijkingsdatum, en segment tonen.](assets/key-metrics-config.png)

   | Optie | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Metric]** | Selecteer metrisch u wilt onderzoeken. Alle metriek worden ondersteund. |
   | **[!UICONTROL Primary date range]** | Het huidige datumbereik voor de vrije-vormtabel. |
   | **[!UICONTROL Comparison date range]** | Het datumbereik waarmee u het primaire datumbereik wilt vergelijken. |
   | **[!UICONTROL Filter (optional)]** | Filters waarin u specifiek geïnteresseerd bent voor deze samenvatting. |

   {style="table-layout:auto"}

1. Selecteer **[!UICONTROL Build]** .

<!--## How the Key Metric Summary visualization handles the comparison date range

(This will probably release in January. Per Jaden Howell)

* If the primary date range is set to the panel date range, there are 2-6 options that are considered 'relative' to the primary date range. These usually include the previous period (same amount of time immediately proceeding the primary date range), and 52 weeks prior to that date range.

* If the comparison date range is set to one of the 'relative' options, upon updating the primary date range, the comparison date range updates to the period immediate preceding the panel date range.

* If your comparison date range is *not* set to a 'relative' option, then updating the panel date range changes your primary date range, but has no effect on the comparison date range.

**Example 1**

Primary date range is set to the panel's date range: 'Yesterday'
Comparison date range is set to a relative date range, one of: 'Previous day', 'Same day last week', 'Same day 4 weeks prior', 'Same day last month', 'Same day last year', or 'Same day 52 weeks prior'.
When I change the panel's date range to 'This month', the comparison date range will update to 'Previous month'.

**Example 2**
 
Primary date range is set to the panel's date range: 'Yesterday'
Comparison date range is set to a non-relative date range, such as 'Feb 2nd, 2022', 'Highest sales day', 'Last week', etc. 

>[!NOTE]
>
>Last week is relative to the day the project is opened on, but it is not based on the panel's date range of 'Yesterday'. In other cases, such as if the panel's date range was 'This week', it may be relative.

When you change the panel's date range to '4 days ago', the comparison date range remains at the previous selection. -->

De output van de belangrijkste metrische samenvatting kijkt als:

![ Zeer belangrijke metrische output die de metische, summiere verandering, samenvattingsaantal, en lijngrafieken tonen.](assets/key-metrics.png)

* De **[!UICONTROL Previous period]** lijngrafiek (altijd grijs weergegeven) komt overeen met de **[!UICONTROL Comparison date range]** in de configuratiestap.

* Als een vergelijkingsdatumbereik niet is opgegeven tijdens de configuratie of verborgen is in de visualisatie-instellingen, wordt alleen de lijngrafiek voor het primaire datumbereik weergegeven. De samenvattingswijziging is verborgen.

* Vanaf hier kunt u de cursor boven de lijngrafieken houden om de statistieken voor afzonderlijke dagen weer te geven:


## Configureren

Na het bouwen van visualisatie, kunt u de originele configuratie uitgeven.

1. Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) **[!UICONTROL Configure visualization]** bij de bovenkant van visualisatie.

   U wordt teruggezet naar de originele configuratiedialoog.

1. Wijzig desgewenst de instellingen. Selecteer **[!UICONTROL Reset]** om de huidige instellingen opnieuw in te stellen. Selecteer **[!UICONTROL Build]** om de visualisatie opnieuw op te bouwen.

## Instellingen

Als onderdeel van de visualisatie-instellingen zijn specifieke metrische summiere instellingen voor de sleutel beschikbaar.

| Instelling | Beschrijving |
|---|---|
| **[!UICONTROL Summary display type]** | Selecteer tussen **[!UICONTROL Emphasize percent change]** of **[!UICONTROL Emphasize number value]** . |
| **[!UICONTROL Show trendlines]** | Trendlines tonen in de visualisatie. |
| **[!UICONTROL Show max and min on trendlines]** | Toon maximum en minimumwaarde op trendlines. |
| **[!UICONTROL Show comparison percentage and trendline]** | Vergelijkingspercentage tonen bij trendline. Als deze optie niet is geselecteerd, worden beide verborgen. |
| **[!UICONTROL Number value options]** | **[!UICONTROL Show total number]** of **[!UICONTROL Show raw difference]** voor de getalwaarde. |
| **[!UICONTROL Abbreviate value]** | Selecteer **[!UICONTROL Abbreviate value]** om de getalwaarde op een intelligente manier te verkorten. Als deze optie is geselecteerd, voert u een getal in om de hoeveelheid afkorting te definiëren. Bijvoorbeeld:<br/><table><tr><td>**Oorspronkelijke waarde**</td><td>**Afkorting**</td><td>**Resultaat**</td></tr><tr><td>$ 12.011.141,25</td><td>Niet geselecteerd</td><td  align="right">$ 12.011.141,25</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, ingesteld op 1</td><td align="right">$ 12 MB</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, ingesteld op 2</td><td  align="right">$ 12,0 MB</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, ingesteld op 2</td><td align="right">$ 12,011M</td></tr><tr><td>$ 12.011.141,25</td><td>Selecteren, instellen op 3</td><td align="right">$ 12,011M</td></tr></table> |

>[!MORELIKETHIS]
>
>[ voeg een visualisatie aan een paneel toe ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Visualisatie-instellingen ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Contextmenu Visualisatie ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>
