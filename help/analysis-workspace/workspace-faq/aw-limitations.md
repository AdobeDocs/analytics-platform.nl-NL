---
description: Lijst van bekende beperkingen in Adobe Analysis Workspace en de bijbehorende onderdelen
title: Bekende beperkingen in Analysis Workspace
feature: FAQ
exl-id: 334cfe24-a4b2-43be-94df-5a2df90612f0
source-git-commit: 17030d5ac3b488a6c628e6de7aab8b710e5c175a
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 1%

---

# Bekende beperkingen in Analysis Workspace

Hier volgt een lijst met bekende beperkingen in Analysis Workspace en de bijbehorende componenten:

## Tabellen

* Datumvergelijkingskolommen kunnen niet worden toegevoegd wanneer datumbereiken of metriek worden gebruikt als rijen van een tabel.
* De optie Metrisch maken van selectie is uitgeschakeld wanneer filters worden gebruikt als rijen van een tabel. Bovendien moet Metrisch maken van selectie niet worden toegepast op kolommen met datumuitlijning.
* Voorwaardelijke opmaak voor splitsingsrijen kan geen aangepaste bereiken gebruiken.
* De totale rijen van de lijst kunnen niet worden getrand wanneer Berekende totalen door de rijwaarden op te tellen wordt toegepast die (typisch wordt gebruikt met Statische rijpunten) plaatsen.
* [!UICONTROL Contribution Analysis] kan worden uitgevoerd op [!UICONTROL daily] granulariteit _alleen_. Het kan niet worden bestreden [!UICONTROL hourly], [!UICONTROL weekly], enz., gegevens.

## Visualisaties

* Visualisaties die filters gebruiken, zoals [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort], en [!UICONTROL Histogram], kan berekende metriek niet accepteren als invoer.
* [!UICONTROL Flow]: Afmetingen in- en uitgangen, bv. [!UICONTROL Entry page], kan niet worden gebruikt in Flow.
* [!UICONTROL Cohort]: Niet-gehele getallen kunnen niet als cohortcriteria worden gebruikt.

## Componenten > Filters

* Bepaalde metriek en afmetingen kunnen niet worden gefilterd, zoals [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], enz.
* Ad-hocfilters die zijn gemaakt in het dialoogvenster [dropzone van deelvenster](/help/analysis-workspace/c-panels/panels.md) niet in de linkerrail van Workspace of de de componentenmanager van de Filter verschijnen, tenzij zij openbaar worden gemaakt. U doet dit door het filter te bewerken en **[!UICONTROL Make this filter public]**.

## Componenten > Berekende cijfers

* Berekende meetgegevens kunnen niet worden gebruikt in bepaalde visualisaties. Zie &#39;Visualisaties&#39; hierboven.
* Berekende metriek kan niet worden gebruikt in de [!UICONTROL Attribution] , aangezien berekende metriek zelf afzonderlijke attributiemodellen kunnen bevatten.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een berekende metrische waarde wordt gemaakt in Workspace (in tegenstelling tot het resultaat [!UICONTROL Components > filters]). Bijvoorbeeld, [!UICONTROL IP Address].

## Componenten > Datumbereik

* Aangepaste datumbereiken worden niet ondersteund [!UICONTROL This day last year], [!UICONTROL This day last month], enz.


## Componenten > Rapportinstellingen

* Enkele instellingen in het dialoogvenster [!UICONTROL Report Settings] is niet van toepassing. Analysis Workspace gebruikt alleen de [!UICONTROL Language/Currency/Encoding] instellingen onderaan: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding], en [!UICONTROL CSV Separator Character].

## Attribution IQ

* Een subset van metriek wordt niet ondersteund in [!UICONTROL Attribution IQ]. Voor een volledige lijst raadpleegt u de [Veelgestelde vragen over Attribution IQ](../attribution/faq.md).
