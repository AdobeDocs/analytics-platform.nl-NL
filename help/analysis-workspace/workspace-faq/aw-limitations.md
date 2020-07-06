---
description: Lijst met bekende beperkingen in Adobe Analysis Workspace en verwante componenten
title: Bekende beperkingen in Analysis Workspace
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 2%

---


# Bekende beperkingen in Analysis Workspace

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Hier volgt een lijst met bekende beperkingen in Analysis Workspace en de bijbehorende componenten:

## Tabellen

* Datumvergelijkingskolommen kunnen niet worden toegevoegd wanneer datumbereiken of metriek worden gebruikt als rijen van een tabel.
* Metrisch maken van selectie is uitgeschakeld wanneer segmenten worden gebruikt als rijen van een tabel. Bovendien moet Metrisch maken van selectie niet worden toegepast op kolommen met datumuitlijning.
* Voorwaardelijke opmaak voor splitsingsrijen kan geen aangepaste bereiken gebruiken.
* De totale rijen van de lijst kunnen niet worden getrand wanneer Berekende totalen door de rijwaarden op te tellen wordt toegepast die (typisch wordt gebruikt met Statische rijpunten) plaatsen.
* [!UICONTROL Contribution Analysis] kan [!UICONTROL daily] alleen _met de_ granulariteit worden uitgevoerd. Het kan niet worden uitgevoerd tegen [!UICONTROL hourly], [!UICONTROL weekly]etc., gegevens.

## Visualisaties

* Visualisaties die de hefboomfinanciering segmentatie, zoals [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort]en [!UICONTROL Histogram], niet berekende metriek als input accepteren.
* [!UICONTROL Flow]: Afmetingen in- en uitgangen, bv. [!UICONTROL Entry page], kan niet worden gebruikt in Flow.
* [!UICONTROL Cohort]: Niet-gehele getallen kunnen niet als cohortcriteria worden gebruikt.

<!--## Panels

* Segment Comparison: The [!UICONTROL Everyone Else] segment does not get created if a segment template is used in the initial drop zone.<-->

## Componenten > Filters

* Bepaalde maatstaven en dimensies kunnen niet worden gesegmenteerd, zoals [!UICONTROL Occurrences], [!UICONTROL Unique Visitors]enz.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een filter wordt gemaakt in Workspace (en niet van [!UICONTROL Components > Filters]). Bijvoorbeeld, IP Adres.

## Componenten > Berekende cijfers

* Berekende meetgegevens kunnen niet worden gebruikt in bepaalde visualisaties. Zie &#39;Visualisaties&#39; hierboven.
* Berekende metriek kunnen niet in het [!UICONTROL Attribution] paneel worden gebruikt, aangezien de berekende metriek zelf afzonderlijke attributiemodellen kunnen omvatten.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een berekende metrische waarde wordt gemaakt in Workspace (in tegenstelling tot het resultaat van [!UICONTROL Components > Segments]). Bijvoorbeeld, [!UICONTROL IP Address].

## Componenten > Datumbereik

* Aangepaste datumbereiken bieden geen ondersteuning voor [!UICONTROL This day last year], [!UICONTROL This day last month]enzovoort.

## Componenten > Rapportinstellingen

* Sommige instellingen op de [!UICONTROL Report Settings] pagina zijn niet van toepassing. Analysis Workspace gebruikt alleen de onderste [!UICONTROL Language/Currency/Encoding] instellingen: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding]en [!UICONTROL CSV Separator Character].

## Attribution IQ

* Een subset metriek wordt niet ondersteund in [!UICONTROL Attribution IQ]. Voor een volledige lijst, zie de Veelgestelde vragen van [Attributie IQ](../attribution/faq.md).
