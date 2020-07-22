---
description: De rijinstellingen variëren afhankelijk van de component die u naar de tabel hebt gesleept.
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
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

De rijinstellingen variëren afhankelijk van de component die u naar de tabel hebt gesleept. Als u de tabelrijinstellingen wilt openen, klikt u op het pictogram Instellingen naast een dimensie, segment, metrisch, tijdsperiode of een verdeling binnen elk van deze instellingen:

![](assets/row-settings.png)

| Instelling | Beschrijving |
|--- |--- |
| Datums uitlijnen | Dit is een instelling op tabelniveau waarmee de datums van elke kolom worden uitgelijnd op alle datums die op dezelfde rij beginnen. Uitlijnen op datum wordt standaard ingeschakeld wanneer een tijddimensie wordt gebruikt in de rijen van de tabel en verschillende datumbereiken worden toegepast in de kolommen. In een dagelijkse tabel waarin oktober en september op de kolommen worden toegepast, begint de linkerkolom bijvoorbeeld met 1 oktober en begint de rechterkolom met 1 september. |
| Uitsplitsing naar positie | Deze instelling is standaard uitgeschakeld en de onderverdelingen zijn gekoppeld aan statische rijitems. Bijvoorbeeld, laten wij zeggen u de hoogste 3 pagina afmetingspunten (Homepage, Resultaten van het Onderzoek, Afhandeling) door het Kanaal van de Marketing. Dan verlaat u het project en keert twee weken later terug. Nadat u het project opnieuw hebt geopend, zijn de bovenste drie pagina&#39;s gewijzigd. In plaats daarvan zijn Homepage, Zoekresultaten en Afhandeling de bovenste 4-6 pagina&#39;s. Standaard worden uw uitsplitsingen naar marketingkanaal nog steeds weergegeven onder Homepage, Zoekresultaten en Afhandeling, ook al staan deze nu in de rijen 4-6. <br> Daarentegen worden de bovenste drie posten altijd uitgesplitst in **uitsplitsing naar positie** , ongeacht wat ze zijn. Als u terugverwijst naar ons voorbeeld, worden de uitsplitsingen van het marketingkanaal gekoppeld aan de bovenste drie pagina&#39;s van de tabel, niet aan Homepage, Zoekresultaten en Afhandeling, die nu in de rijen 4-6 staan. |
| Percentage | **Percentage berekenen op kolom** is de standaardinstelling; de in een kolom zichtbare percentages worden berekend op basis van het totale aantal kolommen. <br>**Bereken percentages door rij **dwingt de lijst Freeform om de celpercentages over de rij in tegenstelling tot onderaan de kolom te berekenen, met Eindtotaal als noemer. Dit is vooral handig voor het trenderen van percentages. Deze instelling is standaard ingeschakeld wanneer u het pictogram Visualiseren gebruikt. |
| Kolomtotalen | Deze instellingen zijn alleen beschikbaar voor [statische rijen](manual-vs-dynamic-rows.md). <br> **Als som van de huidige rijen** wordt een som van de rijen aan de clientzijde van de tabel weergegeven. Dit betekent dat het totaal *niet* de-duplicaatgegevens zoals bezoeken of bezoekers zal dedupliceren. <br> **Toon het grote totaal** toont een server-zijsom wat betekent het totaal zal duplo metriek. |
