---
title: Gegevens migreren van Google Analytics naar Customer Journey Analytics
description: Leer de overkoepelende workflow voor het verplaatsen van gegevens van Google Analytics naar Adobe Experience Platform en het weergeven van rapporten in Customer Journey Analytics.
source-git-commit: 7c195453490499cc42e7d5b2f2d111e2654f918c
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Gegevens migreren van Google Analytics naar Customer Journey Analytics

Als u nog niet eerder met Customer Journey Analytics hebt gewerkt, is het mogelijk dat uw organisatie over bestaande gegevens beschikt op een ander Analytics-platform, zoals Google Analytics. U kunt deze overkoepelende stappen volgen om die gegevens naar Adobe Experience Platform te verplaatsen, zodat u rapporten in Customer Journey Analytics kunt bekijken.

Workflows worden verschaft voor zowel historische gegevens als actuele gegevensverzameling. U kunt een van deze workflows of beide workflows volgen, afhankelijk van de gegevensbehoeften van uw organisatie.

## Historische gegevens van Google Analytics naar Adobe Experience Platform halen

Bij het verzamelen van historische gegevens (backfill) worden gegevens uit Google geëxporteerd en geïmporteerd in Adobe Experience Platform. Zie [Gegevens van Google Analytics opnemen in Adobe Experience Platform](backfill.md).

Als u historische gegevens eenmaal in het Platform hebt opgenomen, kunt u [Huidige gegevens streaming configureren](streaming.md)of de rapportage van teruggevulde gegevens in CJA onmiddellijk starten door [Verbinding maken](/help/connections/create-connection.md).

## Een bestaande Google Analytics-implementatie voor Adobe Experience Platform configureren {#configure}

Bij het verzamelen van huidige (streaming) gegevens moeten gegevens naar Adobe Experience Edge worden verzonden, waarna die gegevens naar Adobe Experience Platform worden doorgestuurd. Zie [Streaming Google Analytics-gegevens instellen in Adobe Experience Platform](streaming.md).

## Vorm een Verbinding en de Mening van Gegevens in CJA

Als u historische gegevens eenmaal hebt ingevoerd en/of gegevensverzameling hebt geconfigureerd voor Adobe Experience Platform, kunt u [Verbinding maken](/help/connections/create-connection.md) zodat Customer Journey Analytics naar die gegevens kan verwijzen.

De verbinding gebruiken om één of meerdere te creëren [Gegevens](/help/data-views/create-dataview.md) voor gebruik in Analysis Workspace.

## Rapporten maken

Nadat u de afmetingen en metriek hebt geconfigureerd in een gegevensweergave, kunt u beginnen met het gebruik van Analysis Workspace om de gewenste rapporten te genereren. Zie [Rapport over gegevens over Google Analytics in Customer Journey Analytics](report.md).
