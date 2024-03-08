---
title: Gegevens migreren van Googles Analytics naar Customer Journey Analytics
description: Leer de overkoepelende workflow voor het verplaatsen van gegevens van Googles Analytics naar Adobe Experience Platform en het weergeven van rapporten in Customer Journey Analytics.
exl-id: 10c485c9-66ab-4925-a357-a66a374d4c6f
feature: Use Cases
role: Admin
source-git-commit: 46d799ad2621d83906908a3f60a59a1027c6518c
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Gegevens migreren van Googles Analytics naar Customer Journey Analytics

Als u niet bekend bent met Customer Journey Analytics, is het mogelijk dat uw organisatie bestaande gegevens heeft op een ander analyseplatform, zoals Googles Analytics. U kunt deze overkoepelende stappen volgen om die gegevens naar Adobe Experience Platform te verplaatsen, zodat u rapporten in Customer Journey Analytics kunt bekijken.

Workflows worden verschaft voor zowel historische gegevens als actuele gegevensverzameling. U kunt een van deze workflows of beide workflows volgen, afhankelijk van de gegevensbehoeften van uw organisatie.

## Historische gegevens van Googles Analytics naar Adobe Experience Platform halen

Bij het verzamelen van historische gegevens (backfill) worden gegevens uit Google geëxporteerd en geïmporteerd in Adobe Experience Platform. Zie [Gegevens van Googles Analytics opnemen in Adobe Experience Platform](backfill.md).

Als u met succes historische gegevens naar Platform brengt, kunt u of [Huidige gegevens streaming configureren](streaming.md)of de rapportage van teruggevulde gegevens in Customer Journey Analytics onmiddellijk starten door [Verbinding maken](/help/connections/create-connection.md).

## Een bestaande implementatie van Googles Analytics voor Adobe Experience Platform configureren {#configure}

Bij het verzamelen van huidige (streaming) gegevens moeten gegevens naar het Adobe Experience Platform Edge Network worden verzonden, dat die gegevens vervolgens doorstuurt naar Adobe Experience Platform. Zie [Gegevens voor streaming Googles Analytics instellen in Adobe Experience Platform](streaming.md).

## Een verbinding en gegevensweergave configureren in Customer Journey Analytics

Als u de historische gegevens eenmaal hebt ingevoerd en/of de gegevensverzameling hebt geconfigureerd voor Adobe Experience Platform, kunt u [Verbinding maken](/help/connections/create-connection.md) zodat Customer Journey Analytics naar die gegevens kan verwijzen.

De verbinding gebruiken om één of meerdere te creëren [Gegevens weergeven](/help/data-views/create-dataview.md) voor gebruik in Analysis Workspace.

## Rapporten maken

Nadat u de afmetingen en metriek hebt geconfigureerd in een gegevensweergave, kunt u beginnen met het gebruik van Analysis Workspace om de gewenste rapporten te genereren. Zie [Rapport over gegevens over Googles Analytics in Customer Journey Analytics](report.md).
