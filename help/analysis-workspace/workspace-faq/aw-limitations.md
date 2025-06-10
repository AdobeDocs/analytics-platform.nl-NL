---
description: Meer informatie over bekende beperkingen in Adobe Analysis Workspace en de bijbehorende componenten
title: Bekende beperkingen in Analysis Workspace
feature: FAQ
exl-id: 334cfe24-a4b2-43be-94df-5a2df90612f0
role: User
source-git-commit: 38be838fccf896a12da3fbadac50e578081312ba
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 1%

---

# Bekende beperkingen in Analysis Workspace

Hier volgt een lijst met bekende beperkingen in Analysis Workspace en de bijbehorende componenten:

## Tabellen

* Datumvergelijkingskolommen kunnen niet worden toegevoegd wanneer datumbereiken of metriek worden gebruikt als rijen van een tabel.
* Metrisch maken van selectie is uitgeschakeld wanneer segmenten worden gebruikt als rijen van een tabel. Bovendien moet Metrisch maken van selectie niet worden toegepast op kolommen met datumuitlijning.
* Voorwaardelijke opmaak voor splitsingsrijen kan geen aangepaste bereiken gebruiken.
* De totale rijen van de lijst kunnen niet worden getrand wanneer Berekende totalen door de rijwaarden op te tellen wordt toegepast die (typisch wordt gebruikt met Statische rijpunten) plaatsen.

## Visualisaties

* Visualisaties waarbij segmenten zoals [!UICONTROL Fallout] , [!UICONTROL Flow] , [!UICONTROL Cohort] en [!UICONTROL Histogram] worden gebruikt, kunnen berekende metriek niet als invoer accepteren.
* [!UICONTROL Flow]: de afmetingen voor in- en uitstappen, bijvoorbeeld [!UICONTROL Entry page] , kunnen niet worden gebruikt in de stroom.
* [!UICONTROL Cohort]: niet-gehele getallen kunnen niet worden gebruikt als Cohortcriteria.

## Segmenten

* Bepaalde metriek en afmetingen kunnen niet worden gesegmenteerd, zoals [!UICONTROL Events] , [!UICONTROL Persons] , enzovoort.
* Ad hoc segmenten die in [ worden gecreeerd paneeldropzone ](/help/analysis-workspace/c-panels/panels.md) zijn een type van snel segment. Ze worden alleen weergegeven in het linkerdeelvenster van Workspace of in Segmentbeheer als ze openbaar zijn gemaakt. Voor meer informatie, zie [ Snelle segmenten ](/help/components/segments/seg-quick.md).

## Berekende standaarden

* Berekende meetgegevens kunnen niet worden gebruikt in bepaalde visualisaties. Zie [ Visualisaties ](#visualizations).
* Berekende metriek kunnen niet worden gebruikt in het deelvenster [!UICONTROL Attribution] , omdat berekende metriek zelf afzonderlijke attributiemodellen kunnen bevatten.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een berekende metrische waarde wordt gemaakt vanuit Workspace (in tegenstelling tot de waarde die wordt gemaakt op basis van [!UICONTROL Components > segments]). Bijvoorbeeld [!UICONTROL IP Address] .

## Datumbereik

* Aangepaste datumbereiken bieden geen ondersteuning voor [!UICONTROL This day last year] , [!UICONTROL This day last month] , enzovoort.


## Rapportinstellingen

* Sommige instellingen op de pagina [!UICONTROL Report Settings] zijn niet van toepassing. Analysis Workspace gebruikt alleen de [!UICONTROL Language/Currency/Encoding] -instellingen onderaan: [!UICONTROL Thousands separator] , [!UICONTROL Scheduled Report Encoding] en [!UICONTROL CSV Separator Character] .

