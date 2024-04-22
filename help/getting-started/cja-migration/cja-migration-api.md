---
title: Het API-gebruik voor rapportage tijdens migreren naar Customer Journey Analytics
description: Leer hoe u het gebruik van API's van Adobe Analytics naar Customer Journey Analytics kunt exporteren
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: d26a6956-870f-44f2-9c32-f732bff17737
source-git-commit: 21d77f06595993172460b724dc7991cb9a5a02a8
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# Stap 7: Poort het rapport API gebruik wanneer het migreren aan Customer Journey Analytics

+++ breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere migratieproces past. Controleer of alle vorige migratiestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige migratietaken hebt uitgevoerd.

De informatie op deze pagina heeft betrekking op Stap 7, zoals aangegeven in de onderstaande tabel:

| Migratietaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| **Stap 2: [Kies de migratiemethode](/help/getting-started/cja-migration/cja-migration-method.md)** | Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van de migratiemethode die u hebt gekozen in Stap 1. |
| **Stap 4: [Gegevens toewijzen aan het XDM-schema](/help/getting-started/cja-migration/cja-migration-xdm.md)** | [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) in Adobe Experience Platform worden gebruikt om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens.<p>De meeste migratiemethodes vereisen dat u of een nieuw schema XDM creeert, of uw bestaand schema van Adobe Analytics aan XDM in kaart brengt door datastream afbeelding te gebruiken.</p> |
| **Stap 5: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 6: [Gebruiker aan boord plannen](/help/getting-started/cja-migration/cja-migration-onboarding.md)** | Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace. |
| <span class="preview">**Stap 7: [Poort voor het gebruik van de rapportage-API](/help/getting-started/cja-migration/cja-migration-api.md)**</span> | <span class="preview">De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API.</span> |
| **Stap 8: [Gegevensfeeds en -Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md)** | Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om de functies Gegevensfeeds en Data Warehouse te vervangen die u in Adobe Analytics gebruikte. |
| **Stap 9: [Projecten en onderdelen migreren](/help/getting-started/cja-migration/cja-migration-projects.md)** | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics. |
| **Stap 10: [Na de migratie uitvoeren](/help/getting-started/cja-getting-started.md)** | Nadat u de migratie voltooit, moet u diverse taken uitvoeren, met inbegrip van het brengen van andere gegevens in Experience Platform, het creëren van verbindingen tussen de datasets van het Platform en Customer Journey Analytics, het creëren van gegevensmeningen, en het leren hoe te om over kanaalgegevens in Analysis Workspace te rapporteren. |

{style="table-layout:auto"}

+++

Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API.

De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt.

## Volgende, vervang de Diervoeders en de Data Warehouse van Gegevens

Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om [De functies Gegevensfeeds en Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md) je gebruikte in Adobe Analytics.
