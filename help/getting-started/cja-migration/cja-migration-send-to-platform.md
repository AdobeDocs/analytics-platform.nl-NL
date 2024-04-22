---
title: Gegevens verzenden naar Adobe Experience Platform tijdens migreren naar Customer Journey Analytics
description: Gegevens verzenden naar Adobe Experience Platform tijdens migreren naar Customer Journey Analytics
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: da71e96749093821b49806c5a1bfd2f82ca85dd4
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Stap 3: Gegevens verzenden naar Adobe Experience Platform tijdens het migreren naar Customer Journey Analytics

+++De informatie op deze pagina maakt deel uit van een groter migratieproces. Breid deze sectie uit om te zien waar deze informatie binnen het migratieproces past. </br></br>U moet alle vorige migratiestappen voltooien alvorens met de informatie op deze pagina verder te gaan.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige migratietaken hebt uitgevoerd.

De informatie op deze pagina heeft betrekking op Stap 3, zoals aangegeven in de onderstaande tabel:

| Migratietaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| **Stap 2: [Kies de migratiemethode](/help/getting-started/cja-migration/cja-migration-method.md)** | Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| <span class="preview">**Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)**</span> | <span class="preview">Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van de migratiemethode die u hebt gekozen in Stap 1.</span> |
| **Stap 4: [Gegevenstoewijzing naar het XDM-schema](/help/getting-started/cja-migration/cja-migration-xdm.md)** | [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) in Adobe Experience Platform worden gebruikt om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens.<p>De meeste migratiemethodes vereisen dat u of een nieuw schema XDM creeert, of uw bestaand schema van Adobe Analytics aan XDM in kaart brengt door datastream afbeelding te gebruiken.</p> |
| **Stap 5: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 6: [Gebruiker aan boord plannen](/help/getting-started/cja-migration/cja-migration-onboarding.md)** | Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace. |
| **Stap 7: [Poort voor het gebruik van de rapportage-API](/help/getting-started/cja-migration/cja-migration-api.md)** | De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API. |
| **Stap 8: [Gegevensfeeds en -Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md)** | Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om de functies Gegevensfeeds en Data Warehouse te vervangen die u in Adobe Analytics gebruikte. |
| **Stap 9: [Projecten en onderdelen migreren](/help/getting-started/cja-migration/cja-migration-projects.md)** | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics. |

{style="table-layout:auto"}

+++


Na u [Kies de migratiemethode](#step-2-choose-your-customer-journey-analytics-migration-method) dat het beste is voor uw organisatie, kunt u beginnen gegevens naar Adobe Experience Platform te verzenden om het in Customer Journey Analytics ter beschikking te stellen.

Het proces voor het verzenden van gegevens naar Experience Platform voor elke migratiemethode wordt hieronder getoond. Volg de koppelingen in de onderstaande tabel voor meer informatie.

| Migratiemethode | Proces voor het verzenden van gegevens naar platform |
|---------|----------|
| Nieuwe implementatie van de Web SDK | [Gegevens invoeren via de Adobe Experience Platform Web SDK](/help/data-ingestion/aepwebsdk.md) |
| Uw Adobe Analytics-implementatie migreren voor gebruik van de Web SDK | Als u de tagextensie Analytics gebruikt: [Migreren van de Adobe Analytics-tagextensie naar de Web SDK-tagextensie](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/analytics-extension-to-web-sdk)<p>of</p><p>Als u AppMeasurement gebruikt: [Migreren van AppMeasurement naar de Web SDK](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/appmeasurement-to-web-sdk) |
| Configureer uw bestaande Adobe Analytics Web SDK-implementatie om gegevens naar de Customer Journey Analytics te verzenden | [Een gegevensstroom instellen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-datastream) in [Gegevens invoeren via de Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) |
| Bronverbinding voor analyse | [Gegevens van traditionele Adobe Analytics verzamelen en gebruiken](/help/data-ingestion/analytics.md) |

## Daarna, kaartgegevens aan het XDM schema

Nadat u gegevens naar het Experience Platform hebt verzonden door de koppelingen in de bovenstaande tabel te volgen, moet u mogelijk [kaartgegevens naar het XDM-schema](/help/getting-started/cja-migration/cja-migration-xdm.md), afhankelijk van de implementatiemethode die u hebt gekozen.

De volgende implementatiemethoden vereisen dat u gegevens toewijst aan het XDM-schema:

* Migreren van de Adobe Analytics-tagextensie naar de Web SDK-tagextensie

* Configureer uw bestaande Adobe Analytics Web SDK-implementatie om gegevens naar de Customer Journey Analytics te verzenden

Alternatief, als u verkoos om een nieuwe implementatie van het Web SDK te doen, wordt een afbeelding niet vereist omdat u reeds [een nieuw XDM-schema instellen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-schema) als onderdeel van de nieuwe implementatie.

Als u ervoor kiest om de Analytics Source Connector voor uw migratie te gebruiken, is geen toewijzing vereist omdat de Analytics Source Connector hetzelfde Adobe Analytics-schema gebruikt in plaats van het XDM-schema.
