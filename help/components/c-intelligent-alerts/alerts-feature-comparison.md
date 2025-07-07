---
description: Ervaar hoe waarschuwingen verschillen in Customer Journey Analytics met Adobe Analytics
title: Vergelijking van Customer Journey Analytics- en Adobe Analytics-functies voor waarschuwingen
feature: Workspace Basics
role: User, Admin
exl-id: 04e819c4-9fb5-4459-9f8b-40d78385ed90
source-git-commit: 9e07dfc84bc06aef987d99c225cefb4e0406f552
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Vergelijking van waarschuwingsfuncties

Het gebruik van waarschuwingen in Customer Journey Analytics is bijna hetzelfde als het gebruik van waarschuwingen in Adobe Analytics. Er zijn echter belangrijke verschillen. In de volgende secties worden de belangrijkste verschillen beschreven.

## Uurwaarschuwingen zijn niet beschikbaar

Het uuralarm is **niet** beschikbaar in Customer Journey Analytics terwijl het uuralarm in Adobe Analytics beschikbaar is. In Customer Journey Analytics kunnen waarschuwingen worden geconfigureerd voor dagelijks, wekelijks of maandelijks.

U kunt gegevens op verschillende manieren in Adobe Experience Platform invoeren. Dientengevolge, kan de volledigheid en de beschikbaarheid van gegevens niet betrouwbaar worden bereikt binnen de beperkingen van een uur.  De flexibiliteit van het opnemen van gegevens houdt in dat waarschuwingen per uur onpraktisch zijn vanwege de grote kans op onvolledige gegevens. Voor meer informatie, zie [ de ingangstijden van Gegevens variëren ](#data-ingestion-times-vary-in-customer-journey-analytics).

## De tijd van gegevensinvoer varieert

De tijd die nodig is voordat de gegevens zijn voltooid en beschikbaar zijn voor rapportage in Customer Journey Analytics, varieert per organisatie.

Dit is om de volgende redenen:

* De capaciteit van het platform om allerlei gegevensschema&#39;s en types te houden

  In tegenstelling tot Adobe Analytics (die slechts op Webgegevens) rapporteert, [ kunnen vele verschillende types van gegevens in Adobe Experience Platform ](/help/data-ingestion/data-ingestion.md) worden opgenomen om op in Customer Journey Analytics worden gemeld, en niet kunnen alle soorten gegevens opeenvolgend en in echt - tijd worden verzonden.

* Een vertraging in de levering van partijgegevens aan de datasets van het Platform

  Terwijl sommige gegevens beschikbaar zouden kunnen zijn om op vroeger te rapporteren, worden alle [ partijgegevens opgenomen in een dataset van het Platform ](/help/data-ingestion/data-ingestion.md#ingest-and-use-batch-data.), typisch die zich van 3 tot 9 uren voorbij de tijd van de gegevensgebeurtenis uitstrekken. Voor nauwkeurige waarschuwingen moet de gegevensinvoer volledig zijn, met alle partijgegevens beschikbaar in de dataset. <!--3 to 9 hours is a sweet spot, what we are suggesting.  -->

Om deze redenen is gegevensinvoer voor de verschillende soorten gebeurtenisgegevens die kunnen worden ingevoerd, alleen na enige vertraging volledig, meestal variërend van 3 tot 9 uur na de tijd van de gegevensgebeurtenis. Voor waarschuwingen is accuraat, moeten de gebeurtenisgegevens voor een bepaald gebeurtenisbereik volledig zijn, wat betekent dat Adobe geen gebeurtenisgegevens meer ontvangt voor het opgegeven gebeurtenisbereik.

Voor deze vertraging in de innametijd hebben waarschuwingen een standaardvertraging van 9 uur voordat ze worden verzonden.

U kunt de standaardvertraging van 9 uur aanpassen aan een willekeurige locatie tussen 0 en 24 uur. Als u echter de vertraging tot minder dan 9 uur verkort, kan dit betekenen dat u onvolledige gegevens rapporteert, wat leidt tot onjuiste waarschuwingsinformatie.

Voor meer informatie over hoe te om de vertraging aan te passen, en de factoren u zou moeten overwegen wanneer het doen dit, zie [ alarm ](/help/components/c-intelligent-alerts/alert-builder.md) creëren.

<!-- Starting with "However," the rest of this information should probably go into the actual documentation where we document the option to adjust the delay. -->

## Een waarschuwing maken

In Analysis Workspace in Adobe Analytics, kunt u alarm van Analysis Workspace op veelvoudige manieren [ tot stand brengen. ](https://experienceleague.adobe.com/nl/docs/analytics/components/alerts/alert-builder) In Customer Journey Analytics, kunt u slechts [ een alarm ](alert-builder.md) in Analysis Workspace van een selectie in een vrije vormlijst tot stand brengen.

Zowel steunen Adobe Analytics als Customer Journey Analytics de verwezenlijking van alarm door de [ manager van de Alarm ](alert-manager.md)
