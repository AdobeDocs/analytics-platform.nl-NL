---
description: Lijst van bekende beperkingen in de Werkruimte van de Analyse van Adobe en zijn verwante componenten
title: Bekende beperkingen in de Analyse Werkruimte
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 2%

---


# Bekende beperkingen in de Analyse Werkruimte

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Hier is een lijst van bekende beperkingen in de Werkruimte van de Analyse en zijn verwante componenten:

## Tabellen

* De de vergelijkingskolommen van de datum kunnen niet worden toegevoegd wanneer of datumwaaiers of metriek als rijen van een lijst worden gebruikt.
* Creeer metrisch van selectie is gehandicapt wanneer de segmenten als rijen van een lijst worden gebruikt. Bovendien, creeer metrisch van selectie niet op datum-gerichte kolommen zou moeten worden toegepast.
* Het voorwaardelijke formatteren voor mislukkingsrijen kan geen douanereeksen gebruiken.
* De totale rijen van de lijst kunnen niet worden getrind wanneer de Berekende totalen door de rijwaarden samen te vatten wordt het plaatsen toegepast (typisch gebruikt met Statische rijpunten).
* [!UICONTROL Contribution Analysis] kan worden uitgevoerd op de [!UICONTROL daily] granulariteit _alleen_. Het kan niet worden bestreden [!UICONTROL hourly], [!UICONTROL weekly], enz., gegevens.

## Visualisaties

* Visualisaties die hefboomsegmentatie, zoals [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort]en [!UICONTROL Histogram], kan berekende metriek als input niet accepteren.
* [!UICONTROL Flow]: afmetingen voor in- en uitgang, bv. [!UICONTROL Entry page], kan niet in Stroom worden gebruikt.
* [!UICONTROL Cohort]: Niet-gehelen kunnen niet worden gebruikt als cohortcriteria.

<!--## Panels

* Segment Comparison: The [!UICONTROL Everyone Else] segment does not get created if a segment template is used in the initial drop zone.<-->

## Componenten > Filters

* Bepaalde metriek en afmetingen zijn niet segmenteerbaar, zoals [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], enz.
* Bepaalde componenten en exploitanten zijn niet beschikbaar als een filter van Werkruimte (in tegenstelling tot wordt gecreeerd van) wordt gecreeerd [!UICONTROL Components > Filters]). Bijvoorbeeld, IP Adres.

## Componenten > Berekende waarden

* De berekende metriek kunnen niet in bepaalde visualisaties worden gebruikt. Zie &#39;Visualisaties&#39; hierboven.
* De berekende metriek kunnen niet in worden gebruikt [!UICONTROL Attribution] paneel, aangezien de berekende metriek zelf afzonderlijke attributiemodellen kunnen omvatten.
* Bepaalde componenten en exploitanten zijn niet beschikbaar als berekende metrisch van Werkruimte (in tegenstelling tot wordt gecreeerd van [!UICONTROL Components > Segments]). Bijvoorbeeld, [!UICONTROL IP Address].

## Componenten > Datumbereik

* De datumwaaiers van de douane steunen niet [!UICONTROL This day last year], [!UICONTROL This day last month], enz.

## Componenten > Rapportinstellingen

* Enkele montages op [!UICONTROL Report Settings] pagina is niet van toepassing. De Werkruimte van de analyse gebruikt slechts [!UICONTROL Language/Currency/Encoding] instellingen onderaan: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding]en [!UICONTROL CSV Separator Character].

## Attribution IQ

* Een ondergroep van metriek wordt niet gesteund in [!UICONTROL Attribution IQ]. Voor een volledige lijst, zie [Attributie IQ FAQ](../attribution/faq.md).
