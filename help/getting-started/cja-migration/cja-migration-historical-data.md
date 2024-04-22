---
title: Historische gegevens behouden bij migreren naar Customer Journey Analytics
description: Leer hoe u historische gegevens kunt behouden tijdens het migreren naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 1d17151b-3a12-468e-9a4f-9e5994599570
source-git-commit: 923dfac33fcde368392fe29c6530069cc0d8fb9d
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# Stap 5: historische gegevens behouden bij migreren naar Customer Journey Analytics

+++ breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere migratieproces past. Controleer of alle vorige migratiestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige migratietaken hebt uitgevoerd.

De informatie op deze pagina heeft betrekking op Stap 5, zoals aangegeven in de onderstaande tabel:

| Migratietaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| **Stap 2: [Kies de migratiemethode](/help/getting-started/cja-migration/cja-migration-method.md)** | Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van de migratiemethode die u hebt gekozen in Stap 1. |
| **Stap 4: [Gegevens toewijzen aan het XDM-schema](/help/getting-started/cja-migration/cja-migration-xdm.md)** | [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) in Adobe Experience Platform worden gebruikt om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens.<p>De meeste migratiemethodes vereisen dat u of een nieuw schema XDM creeert, of uw bestaand schema van Adobe Analytics aan XDM in kaart brengt door datastream afbeelding te gebruiken.</p> |
| <span class="preview">**Stap 5: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)**</span> | <span class="preview">De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar.</span> |
| **Stap 6: [Gebruiker aan boord plannen](/help/getting-started/cja-migration/cja-migration-onboarding.md)** | Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace. |
| **Stap 7: [Poort voor het gebruik van de rapportage-API](/help/getting-started/cja-migration/cja-migration-api.md)** | De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API. |
| **Stap 8: [Gegevensfeeds en -Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md)** | Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om de functies Gegevensfeeds en Data Warehouse te vervangen die u in Adobe Analytics gebruikte. |
| **Stap 9: [Projecten en onderdelen migreren](/help/getting-started/cja-migration/cja-migration-projects.md)** | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics. |

{style="table-layout:auto"}

+++

Kies een van de volgende opties om historische gegevens te behouden wanneer u van Adobe Analytics naar Customer Journey Analytics gaat:

## De Bronverbinding Analytics gebruiken

U kunt de opdracht [Bronverbinding voor analyse](/help/data-ingestion/analytics.md) om historische gegevens te behouden. Ongeacht de migratiemethode die u kiest (zelfs als u migreert gebruikend het Web SDK), kunt u de Verbinding van de Bron van Analytics gebruiken om historische gegevens van uw milieu van Adobe Analytics te behouden.

U kunt de Verbinding van de Bron van Analytics gebruiken om historische gegevens op de volgende manieren te behouden:

* Breng historische gegevens in zijn eigen specifieke plaats, los van uw huidige gegevens.

* Wijs historische gegevens toe op een manier die u toestaat om het aan uw nieuwe gegevens te binden. <!-- Possible? Explain -->

## Bestaande Adobe Analytics-implementatie onderhouden

U kunt uw bestaande Adobe Analytics-implementatie gedurende een specifiek tijdsbestek (bijvoorbeeld 1 jaar) naast uw nieuwe Customer Journey Analytics-implementatie handhaven. Als u deze optie kiest, moet u de Adobe Analytics-implementatie uitschakelen nadat u voldoende gegevens in de Customer Journey Analytics hebt.

Neem contact op met de accountvertegenwoordiger van de Adobe om de prijs voor deze optie te bepalen.

## Volgende, plan gebruiker aan boord

[Voorzien dat de gebruiker aan boord gaat van de Customer Journey Analytics](/help/getting-started/cja-migration/cja-migration-onboarding.md). Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace.
