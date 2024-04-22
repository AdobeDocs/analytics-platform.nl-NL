---
title: Gegevensfeeds en -Data Warehouse vervangen bij migreren naar Customer Journey Analytics
description: Uw migratie van Adobe Analytics naar Customer Journey Analytics plannen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 3a99aed3-26b9-494f-aaf9-f8eaa2c2d88f
source-git-commit: 21d77f06595993172460b724dc7991cb9a5a02a8
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 1%

---

# Stap 8: Gegevensfeeds en -Data Warehouse vervangen bij migreren naar Customer Journey Analytics

+++ breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere migratieproces past. Controleer of alle vorige migratiestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige migratietaken hebt uitgevoerd.

De informatie op deze pagina heeft betrekking op Stap 8, zoals aangegeven in de onderstaande tabel:

| Migratietaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| **Stap 2: [Kies de migratiemethode](/help/getting-started/cja-migration/cja-migration-method.md)** | Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van de migratiemethode die u hebt gekozen in Stap 1. |
| **Stap 4: [Gegevens toewijzen aan het XDM-schema](/help/getting-started/cja-migration/cja-migration-xdm.md)** | [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) in Adobe Experience Platform worden gebruikt om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens.<p>De meeste migratiemethodes vereisen dat u of een nieuw schema XDM creeert, of uw bestaand schema van Adobe Analytics aan XDM in kaart brengt door datastream afbeelding te gebruiken.</p> |
| **Stap 5: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 6: [Gebruiker aan boord plannen](/help/getting-started/cja-migration/cja-migration-onboarding.md)** | Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace. |
| **Stap 7: [Poort voor het gebruik van de rapportage-API](/help/getting-started/cja-migration/cja-migration-api.md)** | De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API. |
| <span class="preview">**Stap 8: [Gegevensfeeds en -Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md)**</span> | <span class="preview">Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om de functies Gegevensfeeds en Data Warehouse te vervangen die u in Adobe Analytics gebruikte.</span> |
| **Stap 9: [Projecten en onderdelen migreren](/help/getting-started/cja-migration/cja-migration-projects.md)** | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics. |
| **Stap 10: [Na de migratie uitvoeren](/help/getting-started/cja-getting-started.md)** | Nadat u de migratie voltooit, moet u diverse taken uitvoeren, met inbegrip van het brengen van andere gegevens in Experience Platform, het creëren van verbindingen tussen de datasets van het Platform en Customer Journey Analytics, het creëren van gegevensmeningen, en het leren hoe te om over kanaalgegevens in Analysis Workspace te rapporteren. |

{style="table-layout:auto"}

+++

Als u momenteel Gegevensfeeds of -Data Warehouse gebruikt in Adobe Analytics, gebruikt u de volgende tabel voor meer informatie over de verschillende exportopties die beschikbaar zijn in Customer Journey Analytics:

| Adobe Analytics | Customer Journey Analytics |
|---------|----------|
| Gegevensfeeds | Evalueer uw het gebruikscase van de Diervoeders van Gegevens, dan gebruik om het even welke combinatie alternatieve uitvoermethodes die in Customer Journey Analytics beschikbaar zijn: <ul><li>Onbewerkte gegevenssets exporteren [datasets exporteren naar cloudopslagbestemmingen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets). &#x200B;</li><li>Voor het exporteren van publiek- of gebeurtenisniveau met Person-id of Tijdstempel gebruikt u [Volledige tabelexport](/help/analysis-workspace/export/export-cloud.md). &#x200B;</li><li>Voor directe integratie met Power BI en Tableau gebruikt u de [Customer Journey Analytics BI Extension](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/bi-extension). &#x200B;</li><li>Voor directe SQL-toegang tot gegevens in Adobe Experience Platform gebruikt u de [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/en/docs/experience-platform/query/home).</li></ul> |
| Data Warehouse | Adobe Analytics Data Warehouse exporteren naar gebruik wijzigen [Volledige tabelexport](/help/analysis-workspace/export/export-cloud.md) in de Customer Journey Analytics.<p>De Volledige Uitvoer van de Lijst van de Customer Journey Analytics is de evolutie van de rapporten van de Data Warehouse in Adobe Analytics, met vele nieuwe, vaak-gevraagde eigenschappen die niet vandaag in Data Warehouse beschikbaar zijn.</p> |

{style="table-layout:auto"}

## Daarna, migreer projecten en componenten

Het gebied voor componentmigratie in Adobe Analytics gebruiken om [projecten en de bijbehorende onderdelen migreren](/help/getting-started/cja-migration/cja-migration-projects.md) van Adobe Analytics naar Customer Journey Analytics.
