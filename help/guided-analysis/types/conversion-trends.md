---
title: Conversietrends, analyse
description: Wijzigingen in de conversiesnelheid in de loop der tijd bijhouden.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: 75501e77-a172-48b4-9c91-b12d39e93c37
role: User
source-git-commit: bd8c9951386608572d84006bd5465e57214c56d4
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# [!UICONTROL Conversion trends] analyse {#conversion-trends}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_guidedanalysis_conversiontrends_button"
>title="Conversietrends"
>abstract="Wijzigingen in conversietarieven bijhouden in de loop van de tijd."

<!-- markdownlint-enable MD034 -->


De ![ analyse van de Trends van de Omzetting ](/help/assets/icons/ConversionTrends.svg) **[!UICONTROL Conversion trends]** verstrekt een trended visualisatie van omzettingen in tijd. De horizontale as is een tijdinterval, terwijl de verticale as de omzettingssnelheid vertegenwoordigt.


>[!VIDEO](https://video.tv.adobe.com/v/3432446/?quality=12&learn=on&captions=dut)


## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **de optimaliseringsinspanningen van het Spoor**: Na het identificeren van zeer belangrijke knelpunten die u het gebruiken van de [ analyse van het Trechter ](funnel.md) wilt verbeteren, kunt u deze analyse gebruiken om te volgen hoe die optimalisaties omzettingspercentage in tijd beïnvloeden.
* **A/B testende evaluatie**: Evalueer de doeltreffendheid van tests A/B of experimenten die binnen de context van een trechter worden uitgevoerd. Door de omrekeningskoersen tussen verschillende variaties te vergelijken, kunt u gemakkelijk bepalen welke tests hogere omrekeningskoersen verstrekken, die tot gegeven-gedreven besluiten leiden waarrond variaties permanent moeten uitvoeren.
* **de evaluatie van de Campagne in tijd**: Meet de doeltreffendheid van marketing campagnes in tijd. U kunt een segment maken dat zich richt op gebruikers die een bepaalde campagne hebben aangeraakt, en hun conversietarieven vergelijken met andere campagnes. U kunt de huidige omrekeningskoersen ook vergelijken met vergelijkbare campagnes die in het verleden zijn gevoerd.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen deze analyse en [ Trechter ](funnel.md).
* **[!UICONTROL Steps]**: De aanraakpunten voor gebeurtenissen die u wilt bijhouden. Elke balk in het diagram vertegenwoordigt een stap. U kunt maximaal tien stappen opnemen.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. De opties zijn [!UICONTROL Users] en [!UICONTROL Sessions] .
* **[!UICONTROL Segments]**: De segmenten waarin u de trechter wilt vergelijken. Elk segment dat is geselecteerd, splitst elke stap in meerdere balken. Elke kleur vertegenwoordigt een ander segment. U kunt maximaal drie segmenten opnemen.

### Diagraminstellingen

De [!UICONTROL Conversion trends] -analyse biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties zijn [!UICONTROL Line] .
* **[!UICONTROL Conversion from]** - Hiermee bepaalt u het percentage van de berekening van stap tot stap. U kunt onder andere de conversie van de [!UICONTROL First step] of [!UICONTROL Previous step] berekenen.

>[!NOTE]
>
>De **Gemiddelde** kolom in de de analyselijst van de tendensen van de Omzetting verschilt van de **Totale** kolom in de [ de analyse van het Trechter ](funnel.md) lijst. Het eerste is een gemiddelde van de intervalkolommen (bijvoorbeeld het gemiddelde van de dagelijkse omrekeningskoersen), terwijl het laatste een geaggregeerde berekening is over het volledige datumbereik.

### Tijdvergelijking

{{apply-time-comparison}}


### Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben, die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

<!--
## Example

See below for an example of the analysis.

![Conversion trends time compare](../assets/conversion-trends-compare.png)

-->
