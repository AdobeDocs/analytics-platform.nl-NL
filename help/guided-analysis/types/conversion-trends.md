---
title: Conversietrends, weergave
description: Wijzigingen in de conversiesnelheid in de loop der tijd bijhouden.
feature: Guided Analysis
keywords: productanalyse
exl-id: 75501e77-a172-48b4-9c91-b12d39e93c37
role: User
source-git-commit: e448f6ddbff2673abbd2920aacf41d4268f3ce07
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Conversietrends, weergave

De **Conversietrends** de mening verstrekt een trended visualisatie rond omzettingspercentages in tijd. De horizontale as is een tijdinterval, terwijl de verticale as de omzettingssnelheid vertegenwoordigt.

>[!VIDEO](https://video.tv.adobe.com/v/3421662/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Optimalisatie-inspanningen bijhouden**: Na het identificeren van de belangrijkste knelpunten die u wilt verbeteren gebruiken [Wrijving](friction.md)kunt u deze weergave gebruiken om te volgen hoe deze optimalisaties de conversiesnelheid in de loop der tijd beïnvloeden.
* **A/B-testevaluatie**: De doeltreffendheid van A/B-tests of -experimenten die in de context van een trechter worden uitgevoerd, evalueren. Door de omrekeningskoersen tussen verschillende variaties te vergelijken, kunt u gemakkelijk bepalen welke tests hogere omrekeningskoersen verstrekken, die tot gegeven-gedreven besluiten leiden waarrond variaties permanent moeten uitvoeren.
* **Campagneevaluatie in de loop der tijd**: De doeltreffendheid van marketingcampagnes in de loop der tijd meten. U kunt een segment maken dat zich richt op gebruikers die een bepaalde campagne hebben aangeraakt, en hun conversietarieven vergelijken met andere campagnes. U kunt de huidige omrekeningskoersen ook vergelijken met vergelijkbare campagnes die in het verleden zijn gevoerd.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakel tussen dit weergavetype en [Wrijving](friction.md).
* **[!UICONTROL Steps]**: De aanraakpunten voor gebeurtenissen die u wilt bijhouden. Elke balk in het diagram vertegenwoordigt een stap. U kunt maximaal tien stappen opnemen.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. Opties omvatten [!UICONTROL Users] en [!UICONTROL Sessions].
* **[!UICONTROL Segments]**: De segmenten waar u de trechter doorheen wilt vergelijken. Elk segment dat is geselecteerd, splitst elke stap in meerdere balken. Elke kleur vertegenwoordigt een ander segment. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De [!UICONTROL Conversion trends] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Line].
* **[!UICONTROL Conversion from]**: Hiermee bepaalt u het percentage van de berekening van stap tot stap. U kunt onder andere de conversie van de [!UICONTROL First step] of [!UICONTROL Previous step].

>[!NOTE]
>
>De **Gemiddeld** de kolom in de de meningslijst van de tendensen van de Omzetting verschilt van **Totaal** in de [Wrijvingsweergave](friction.md) tabel. Het eerste is een gemiddelde van de intervalkolommen (bijvoorbeeld het gemiddelde van de dagelijkse omrekeningskoersen), terwijl het laatste een geaggregeerde berekening is over het volledige datumbereik.

## Tijdvergelijking

{{apply-time-comparison}}

![Conversietrends tijdvergelijking](../assets/conversion-trends-compare.png)

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
