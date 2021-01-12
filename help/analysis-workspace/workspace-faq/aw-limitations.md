---
description: Lijst van bekende beperkingen in Adobe Analysis Workspace en de bijbehorende onderdelen
title: Bekende beperkingen in Analysis Workspace
translation-type: tm+mt
source-git-commit: 7f6afbb7c0376791c286021d9ffe4ac670ed7bd7
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 1%

---


# Bekende beperkingen in Analysis Workspace

Hier volgt een lijst met bekende beperkingen in Analysis Workspace en de bijbehorende componenten:

## Tabellen

* Datumvergelijkingskolommen kunnen niet worden toegevoegd wanneer datumbereiken of metriek worden gebruikt als rijen van een tabel.
* Metrisch maken van selectie is uitgeschakeld wanneer segmenten worden gebruikt als rijen van een tabel. Bovendien moet Metrisch maken van selectie niet worden toegepast op kolommen met datumuitlijning.
* Voorwaardelijke opmaak voor splitsingsrijen kan geen aangepaste bereiken gebruiken.
* De totale rijen van de lijst kunnen niet worden getrand wanneer Berekende totalen door de rijwaarden op te tellen wordt toegepast die (typisch wordt gebruikt met Statische rijpunten) plaatsen.
* [!UICONTROL Contribution Analysis] kan  [!UICONTROL daily] alleen _met de_ granulariteit worden uitgevoerd. Deze kan niet worden uitgevoerd tegen gegevens [!UICONTROL hourly], [!UICONTROL weekly], enz.

## Visualisaties

* Voor visualisaties waarbij segmentatie wordt toegepast, zoals [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort] en [!UICONTROL Histogram], kunnen berekende metriek niet als invoer worden geaccepteerd.
* [!UICONTROL Flow]: Afmetingen in- en uitgangen, bv.  [!UICONTROL Entry page], kan niet worden gebruikt in Flow.
* [!UICONTROL Cohort]: Niet-gehele getallen kunnen niet als cohortcriteria worden gebruikt.

## Deelvensters

* Segmentvergelijking: Het [!UICONTROL Everyone Else] segment wordt niet gecreeerd als een segmentmalplaatje in de aanvankelijke dalingsstreek wordt gebruikt.

## Componenten > Filters

* Bepaalde metriek en afmetingen kunnen niet worden gefilterd, zoals [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], enz.
* Ad-hoc filters die in [paneeldropzone](/help/analysis-workspace/c-panels/panels.md) worden gecreeerd zullen niet in de linkerspoorstaaf van Workspace of de de componentenmanager van de Filter verschijnen, tenzij zij openbaar worden gemaakt. U doet dit door het filter te bewerken en **[!UICONTROL Make this filter public]** te selecteren.

## Componenten > Berekende cijfers

* Berekende meetgegevens kunnen niet worden gebruikt in bepaalde visualisaties. Zie &#39;Visualisaties&#39; hierboven.
* Berekende metriek kunnen niet worden gebruikt in het [!UICONTROL Attribution] paneel, aangezien de berekende metriek zelf afzonderlijke attributiemodellen kunnen omvatten.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een berekende metrische waarde wordt gemaakt in Workspace (in tegenstelling tot het resultaat van [!UICONTROL Components > Segments]). Bijvoorbeeld, [!UICONTROL IP Address].

## Componenten > Datumbereik

* Aangepaste datumbereiken bieden geen ondersteuning voor [!UICONTROL This day last year], [!UICONTROL This day last month], enzovoort.


## Componenten > Rapportinstellingen

* Sommige instellingen op de pagina [!UICONTROL Report Settings] zijn niet van toepassing. Analysis Workspace gebruikt alleen de [!UICONTROL Language/Currency/Encoding]-instellingen onderaan: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding] en [!UICONTROL CSV Separator Character].

## Attribution IQ

* Een subset van metriek wordt niet ondersteund in [!UICONTROL Attribution IQ]. Voor een volledige lijst, zie [Veelgestelde vragen van de Attribution IQ](../attribution/faq.md).
