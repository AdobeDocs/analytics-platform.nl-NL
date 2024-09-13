---
description: Leer hoe intelligente waarschuwingen verschillen in Customer Journey Analytics met Adobe Analytics
title: Customer Journey Analytics voor het vergelijken van intelligente waarschuwingen en Adobe Analytics
feature: Workspace Basics
role: User, Admin
source-git-commit: 1613b3fc7e9cce1fb74b86bb7435612b2d469eb1
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# Vergelijking van de functie Intelligente waarschuwingen: Customer Journey Analytics en Adobe Analytics

Het gebruik van intelligente waarschuwingen in de Customer Journey Analytics is bijna hetzelfde als het gebruik van intelligente waarschuwingen in Adobe Analytics. Er zijn echter belangrijke verschillen.

In de volgende secties worden de belangrijkste verschillen beschreven.

## Uurwaarschuwingen zijn niet beschikbaar in de Customer Journey Analytics

Uurwaarschuwingen zijn niet beschikbaar in de Customer Journey Analytics, zoals in Adobe Analytics. In Customer Journey Analytics, kunnen de alarm voor dagelijks, wekelijks, of maandelijks worden gevormd.

Dit komt door de verschillende manieren waarop gegevens in Adobe Experience Platform kunnen worden ingevoerd voordat ze in de Customer Journey Analytics worden gemeld. De volledigheid en beschikbaarheid van gegevens kunnen niet binnen een uur betrouwbaar worden bereikt, waardoor waarschuwingen per uur onpraktisch zijn vanwege de grote kans op onvolledige gegevens. Voor meer informatie, zie [ de ingangstijden van Gegevens variëren ](#data-ingestion-times-vary-in-customer-journey-analytics).

## De Customer Journey Analytics varieert bij het innemen van gegevens

De tijd die nodig is voordat de gegevens zijn voltooid en beschikbaar zijn om in de Customer Journey Analytics te worden gerapporteerd, varieert per organisatie.

Dit is om de volgende redenen:

* De capaciteit van het platform om allerlei gegevensschema&#39;s en types te houden

  In tegenstelling tot Adobe Analytics (die slechts op Webgegevens) rapporteert, [ kunnen vele verschillende types van gegevens in Adobe Experience Platform ](/help/data-ingestion/data-ingestion.md) worden opgenomen om in Customer Journey Analytics worden gemeld, en niet kunnen alle soorten gegevens opeenvolgend en in echt - tijd worden verzonden.

* Een vertraging in de levering van partijgegevens aan de datasets van het Platform

  Terwijl sommige gegevens beschikbaar zouden kunnen zijn om op vroeger te rapporteren, worden alle [ partijgegevens opgenomen in een dataset van het Platform ](/help/data-ingestion/data-ingestion.md#ingest-and-use-batch-data.), typisch die zich van 3 tot 9 uren voorbij de tijd van de gegevensgebeurtenis uitstrekken. Voor nauwkeurige waarschuwingen moet de gegevensinvoer volledig zijn, met alle partijgegevens beschikbaar in de dataset. <!--3 to 9 hours is a sweet spot, what we are suggesting.  -->

Om deze redenen is gegevensinvoer voor de verschillende soorten gebeurtenisgegevens die kunnen worden ingevoerd, alleen na enige vertraging volledig, meestal variërend van 3 tot 9 uur na de tijd van de gegevensgebeurtenis. Voor waarschuwingen is accuraat, moeten de gebeurtenisgegevens voor een bepaald gebeurtenisbereik volledig zijn, wat betekent dat de Adobe geen gebeurtenisgegevens meer ontvangt voor het opgegeven gebeurtenisbereik.

Voor deze vertraging in de innametijd hebben waarschuwingen een standaardvertraging van 9 uur voordat ze worden verzonden.

U kunt de standaardvertraging van 9 uur aanpassen aan een willekeurige locatie tussen 0 en 24 uur. Als u echter de vertraging tot minder dan 9 uur verkort, kan dit betekenen dat u onvolledige gegevens rapporteert, wat leidt tot onjuiste waarschuwingsinformatie.

Zie <!--add link --> voor meer informatie over het aanpassen van de vertraging en de factoren die u daarbij in acht moet nemen.

<!-- Starting with "However," the rest of this information should probably go into the actual documentation where we document the option to adjust the delay. -->





