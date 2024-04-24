---
title: Het API-gebruik voor rapportage tijdens migreren naar Customer Journey Analytics
description: Leer hoe u het gebruik van API's van Adobe Analytics naar Customer Journey Analytics kunt exporteren
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: d26a6956-870f-44f2-9c32-f732bff17737
source-git-commit: 8b7fedb9625ba60af1fea0b1580d32d2366081b8
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Stap 7: Poort het rapport API gebruik wanneer het migreren aan Customer Journey Analytics

+++ breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere migratieproces past. Controleer of alle vorige migratiestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige migratietaken hebt uitgevoerd.

De informatie op deze pagina heeft betrekking op Stap 7, zoals aangegeven in de onderstaande tabel:

| Migratietaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| **Stap 2: [Het migratiepad kiezen](/help/getting-started/cja-migration/cja-migration-path.md)** | Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van het migratiepad dat u hebt gekozen in Stap 2. |
| **Stap 4: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 5: [Extra implementatietaken uitvoeren](/help/getting-started/cja-getting-started.md)** | Op dit punt in het migratieproces, moet u diverse taken uitvoeren alvorens uw milieu van de Customer Journey Analytics klaar aan gebruik is.<p>Deze extra taken gelden voor migraties uit Adobe Analytics en voor nieuwe implementaties van Customers Journey Analytics.</p><p>Deze taken omvatten:</p><ul><li>Andere gegevens in Experience Platform plaatsen</li><li>Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics</li><li>Gegevensweergaven maken</li><li>Het gebruik van de API voor rapportage porteren</li><li>Verantwoording van gegevensfeeds en -Data Warehouse</li><li>Projecten en onderdelen migreren</li><li>Gebruiker aan boord plannen</li></ul> <p>Zie voor meer informatie [Aan de slag met Customer Journey Analytics](/help/getting-started/cja-getting-started.md). |

{style="table-layout:auto"}

+++

Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API.

De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander subdomein.

Zie de eindpuntgids voor Adobe Analytics en Customer Journey Analytics.

De meeste API-aanroepen kunnen eenvoudig van Adobe Analytics naar Customer Journey Analytics worden vertaald.

Voeg de Customer Journey Analytics API aan hun API project toe.

Voeg de IMS org-id toe aan de header van hun API-aanroepen.

cja.adobe.io vs. analytics.adobe.io

Aanvullende koppen

## Volgende, vervang de Diervoeders en de Data Warehouse van Gegevens

Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om [De functies Gegevensfeeds en Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md) je gebruikte in Adobe Analytics.
