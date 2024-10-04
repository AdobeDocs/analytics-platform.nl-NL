---
title: Gegevens migreren uit Googles Analytics
description: Leer de overkoepelende workflow voor het verplaatsen van gegevens van Googles Analytics naar Adobe Experience Platform en het weergeven van rapporten in Customer Journey Analytics.
exl-id: 10c485c9-66ab-4925-a357-a66a374d4c6f
feature: Use Cases
role: Admin
source-git-commit: 90d1c51c11f0ab4d7d61b8e115efa8257a985446
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Gegevens migreren uit Googles Analytics

Als u niet bekend bent met Customer Journey Analytics, is het mogelijk dat uw organisatie bestaande gegevens heeft op een ander analyseplatform, zoals Googles Analytics. U kunt deze overkoepelende stappen volgen om die gegevens naar Adobe Experience Platform te verplaatsen, zodat u rapporten in Customer Journey Analytics kunt bekijken.

Workflows worden verschaft voor zowel historische gegevens als actuele gegevensverzameling. U kunt een van deze workflows of beide workflows volgen, afhankelijk van de gegevensbehoeften van uw organisatie.

## Historische gegevens van Googles Analytics naar Adobe Experience Platform halen

Bij het verzamelen van historische gegevens (backfill) worden gegevens uit Google geëxporteerd en geïmporteerd in Adobe Experience Platform. Zie [ Ingest Googles Analytics gegevens in Adobe Experience Platform ](backfill.md).

Zodra u met succes historische gegevens in Platform brengt, kunt u of [ het stromen huidige gegevens ](streaming.md) vormen, of onmiddellijk beginnen rapporterend over achtergevulde gegevens in Customer Journey Analytics door [ het Creëren van een verbinding ](/help/connections/create-connection.md).

## Een bestaande implementatie van Googles Analytics voor Adobe Experience Platform configureren {#configure}

Bij het verzamelen van huidige (streaming) gegevens moeten gegevens naar de Adobe Experience Platform-Edge Network worden verzonden, die die gegevens vervolgens doorstuurt naar Adobe Experience Platform. Zie [ opstelling het stromen Googles Analytics gegevens in Adobe Experience Platform ](streaming.md).

## Een verbinding en gegevensweergave configureren in Customer Journey Analytics

Zodra u met succes historische gegevens opneemt en/of gegevensinzameling aan Adobe Experience Platform vormt, kunt u [ een verbinding ](/help/connections/create-connection.md) tot stand brengen om Customer Journey Analytics toe te staan om die gegevens van verwijzingen te voorzien.

Gebruik de verbinding om één of meerdere [ Meningen van Gegevens ](/help/data-views/create-dataview.md) voor gebruik in Analysis Workspace tot stand te brengen.

## Rapporten maken

Nadat u de afmetingen en metriek hebt geconfigureerd in een gegevensweergave, kunt u beginnen met het gebruik van Analysis Workspace om de gewenste rapporten te genereren. Zie [ Rapport over Googles Analytics gegevens in Customer Journey Analytics ](report.md).
