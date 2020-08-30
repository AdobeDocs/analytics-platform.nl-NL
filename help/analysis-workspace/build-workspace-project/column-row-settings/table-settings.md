---
description: De montages van de rij variëren afhankelijk van welke component u in de lijst hebt gesleept.
title: Rij-instellingen
uuid: f30c31d5-1fd4-4b93-94c3-ca441099fe2e
translation-type: tm+mt
source-git-commit: df326581abbbd0dd0d29638962ccb71bb0aee837
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 2%

---


# Rij-instellingen

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

De montages van de rij variëren afhankelijk van welke component u in de lijst hebt gesleept. Om tot de montages van de lijstrij toegang te hebben, klik het pictogram van Montages naast een afmeting, segment, metrisch, tijdspanne, of een onderbreking binnen elk van deze:

![](assets/row-settings.png)

| Instelling | Beschrijving |
|--- |--- |
| datums uitlijnen | Dit is een lijst-vlak het plaatsen dat data van elke kolom aan al begin op de zelfde rij richt. Het richten van de datum wordt toegelaten door gebrek wanneer een tijddimensie in de rijen van de lijst wordt gebruikt, en de verschillende datumwaaiers worden toegepast in de kolommen. Bijvoorbeeld, in een dagelijkse lijst met Oktober en September die op de kolommen wordt toegepast, begint de linkerkolom met Oktober 1 en de juiste kolom begint met 1 September. |
| Uitsplitsing naar positie | Door gebrek, is dit het plaatsen gehandicapt en de onderverdelingen worden bevestigd aan statische rijpunten. Bijvoorbeeld, zeggen u de hoogste 3 de afmetingspunten van de Pagina (Homepage, de Resultaten van het Onderzoek, Afhandeling) door het Kanaal van de Marketing. Dan, verlaat u het project en terugkeer twee weken later. Op het openen van het project opnieuw, zijn de hoogste 3 pagina&#39;s veranderd, en nu Homepage, zijn de Resultaten van het Onderzoek en de Afhandeling de hoogste 4-6 pagina&#39;s in plaats daarvan. Door gebrek, zullen uw de onderverdelingen van het Kanaal van de Marketing nog onder Homepage, de Resultaten van het Onderzoek en de Controle verschijnen, alhoewel zij nu in rijen 4-6 zijn. <br> Daarentegen **Uitsplitsing naar positie** zullen altijd de top 3 - posten uitsplitsen, ongeacht wat ze zijn. Verwijzend terug naar ons voorbeeld, wanneer u uw project heropent, zullen de onderbrekingen van het Kanaal van de Marketing aan de bovenkant 3 pagina&#39;s in de lijst, niet Homepage, de Resultaten van het Onderzoek en de Controle worden gebonden die nu in rijen 4-6 zijn. |
| Percentages | **Percentage berekenen per kolom** de standaardinstelling; de percentages die in een kolom zichtbaar zijn, worden berekend op basis van het kolomtotaal. <br>**Berekent percentages per rij** dwingt de lijst Freeform om de celpercentages over de rij in tegenstelling tot onderaan de kolom, met Groot totaal als noemer te berekenen. Dit is vooral nuttig voor trendpercentages. Dit het plaatsen wordt toegelaten door gebrek wanneer het gebruiken van het Visualize pictogram. |
| Totalen kolom | Deze instellingen zijn alleen beschikbaar voor [statische rijen](manual-vs-dynamic-rows.md). <br> **Toon als som van huidige rijen** toont een cliënt-zijsom de rijen in de lijst wat betekent het totaal zal *niet* deduplicatie-metingen zoals bezoeken of bezoekers. <br> **Totaal-generaal weergeven** toont een server-zijsom wat betekent het totaal zal de-duplicaat metriek. |
