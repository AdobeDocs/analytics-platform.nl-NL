---
description: De rijinstellingen variëren afhankelijk van de component die u naar de tabel hebt gesleept.
title: Rij-instellingen
uuid: f30c31d5-1fd4-4b93-94c3-ca441099fe2e
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 6%

---


# Rij-instellingen

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

De rijinstellingen variëren afhankelijk van de component die u naar de tabel hebt gesleept.

U kunt ook met de [rechtermuisknop klikken op handelingen in een tabel](/help/analysis-workspace/visualizations/freeform-table.md) om geselecteerde rijen te beheren.

Als u de tabelrijinstellingen wilt openen, klikt u op het pictogram Instellingen naast een dimensie, segment, metrisch, tijdsperiode of een verdeling binnen elk van deze instellingen:

![](assets/row-settings.png)

| Rijinstelling | Beschrijving |
|--- |--- |
| Datumvergelijkingen | Datums uit elke kolom uitlijnen met alle datums die op dezelfde rij beginnen.   Wanneer u ervoor kiest de datums op elkaar af te stemmen, bijvoorbeeld in een vergelijking van maand na maand tussen oktober en september 2016, begint de linkerkolom met 1 oktober en begint de rechterkolom met 1 september.<br>Standaard uitgeschakeld. |
| Percentage | Bereken percentages door rijDwingt de lijst Freeform om de celpercentages over de rij in tegenstelling tot onderaan de kolom te berekenen. Dit is vooral handig voor het trenderen van percentages.<br>Deze optie is standaard ingeschakeld wanneer u het pictogram Visualiseren gebruikt. |
| Kolomtotalen | Deze instellingen worden alleen weergegeven met [statische rijen](/help/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md) (wanneer u een eindige set items hebt geselecteerd) en niet met dynamische rijen (wanneer u een afmeting uitvoert waarin alle items worden weergegeven).<ul><li>**[!UICONTROL Show sum of current rows as the total]** - hier ziet u een som van de rijen aan de clientzijde van de tabel, wat betekent dat het totaal **niet** de dubbele meetgegevens zoals bezoeken of bezoekers zal dedupliceren.</li><li>**[!UICONTROL Show Grand Total]** - dit toont een bedrag aan serverzijde, wat betekent het totaal metriek zoals bezoeken of bezoekers zal dedupliceren.</li></ul> |
| Uitsplitsingen | **[!UICONTROL Breakdown by position]**: U kunt onderverdelingen uitvoeren op basis van een vaste locatie in een tabel voor vrije vorm. U kunt bijvoorbeeld opgeven dat de bovenste zeven rijen altijd moeten worden opgesplitst.<br>(Eerder was de lijst met waarden in de uitsplitsing &quot;vergrendeld&quot;. Dit leidde bijvoorbeeld tot een situatie waarbij u een lijst van de bovenste 50 pagina&#39;s voor het geselecteerde datumbereik had als u Datum op pagina hebt uitgebroken. Als u dat rapport opsloeg en een maand later weer zou uitvoeren, zouden de bovenste 50 pagina&#39;s waarschijnlijk allemaal anders zijn. Analysis Workspace zou echter de resultaten van de oorspronkelijke indeling gebruiken en dezelfde pagina&#39;s retourneren, maar met de huidige maand als het datumbereik.)<br>Uitsplitsingen uitvoeren op basis van een vaste locatie: 1. Verdeel enkele rijen in uw tabel. 2. Klik op het pictogram Instellingen (versnelling) naast de tabelrij die u op een vaste positie wilt plaatsen. 3. Schakel het selectievakje naast Uitsplitsing op positie in. 4. Wijzig de sorteervolgorde of het datumbereik. U ziet dat de onderverdelingen nu zijn gekoppeld aan de rijpositie, niet aan de rijen met harde codes.<br>Standaard uitgeschakeld. |