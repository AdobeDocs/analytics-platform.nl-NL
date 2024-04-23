---
title: Gegevens toewijzen aan het XDM-schema bij migreren naar Customer Journey Analytics
description: Leer hoe u gegevens aan het XDM-schema kunt toewijzen bij het migreren naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 86ce60cf-b3c7-43b5-aa18-9e16fa942e54
source-git-commit: 3e362a62d2ffd6d15e3028706e3704264df80222
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Stap 4: Wijs gegevens aan het XDM schema toe wanneer het migreren aan Customer Journey Analytics

+++ breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere migratieproces past. Controleer of alle vorige migratiestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige migratietaken hebt uitgevoerd.

De informatie op deze pagina heeft betrekking op Stap 4, zoals aangegeven in de onderstaande tabel:

| Migratietaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| **Stap 2: [Kies de migratiemethode](/help/getting-started/cja-migration/cja-migration-method.md)** | Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van de migratiemethode die u hebt gekozen in Stap 1. |
| <span class="preview">**Stap 4: [Gegevens toewijzen aan het XDM-schema](/help/getting-started/cja-migration/cja-migration-xdm.md)**</span> | <span class="preview">[XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) in Adobe Experience Platform worden gebruikt om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens.<p>De meeste migratiemethodes vereisen dat u of een nieuw schema XDM creeert, of uw bestaand schema van Adobe Analytics aan XDM in kaart brengt door datastream afbeelding te gebruiken.</p></span> |
| **Stap 5: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 6: [Gebruiker aan boord plannen](/help/getting-started/cja-migration/cja-migration-onboarding.md)** | Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace. |
| **Stap 7: [Poort voor het gebruik van de rapportage-API](/help/getting-started/cja-migration/cja-migration-api.md)** | De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API. |
| **Stap 8: [Gegevensfeeds en -Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md)** | Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om de functies Gegevensfeeds en Data Warehouse te vervangen die u in Adobe Analytics gebruikte. |
| **Stap 9: [Projecten en onderdelen migreren](/help/getting-started/cja-migration/cja-migration-projects.md)** | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics. |

{style="table-layout:auto"}

+++

Niet alle migratiemethoden vereisen dat u uw Adobe Analytics-gegevens toewijst aan het XDM-schema. In de volgende tabel wordt aangegeven voor welke implementatiemethoden XDM-schematoewijzing is vereist:


| Migratiemethode | XDM-toewijzing vereist? | Meer informatie |
|---------|----------|---------|
| **Nieuwe implementatie van de Web SDK**<p>De basisstappen zijn:</p><ol><li>Een XDM-schema voor uw organisatie maken</li><li>De SDK van het web implementeren</li><li>Gegevens verzenden naar platform</li></ol> | Nee | Een toewijzing is niet vereist omdat u al [een nieuw XDM-schema instellen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-schema) als onderdeel van de nieuwe uitvoering. |
| **Uw Adobe Analytics-implementatie migreren voor gebruik van de Web SDK**<p>De basisstappen zijn:</p><ol><li>Verplaats uw bestaande Adobe Analytics-implementatie naar de Web SDK en bevestig dat alles daar werkt.</li><li>Creeer een schema XDM voor uw organisatie aangezien u tijd hebt.</li><li>Gebruik gegevenstoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.</li><li>Gegevens verzenden naar platform</li></ol> | Ja | Werken met uw gegevensteam, identificeer het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics, dan bepalen hoe u eVars en Props aan XDM in kaart zult brengen.</br>[Gegevensvoorinstelling gebruiken om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema](https://experienceleague.adobe.com/en/docs/experience-platform/data-prep/home) |
| **Configureer uw bestaande Adobe Analytics Web SDK-implementatie om gegevens naar de Customer Journey Analytics te verzenden**<p>De basisstappen zijn:</p><ol><li>Gegevens verzenden naar Customer Journey Analytics.<!-- What's involved here? Just point it at CJA? --></li><li>(Optioneel) Maak een XDM-schema voor uw organisatie terwijl u tijd hebt.</li><li>Gebruik gegevenstoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.</li></ol> | Ja | Werken met uw gegevensteam, identificeer het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics, dan bepalen hoe u eVars en Props aan XDM in kaart zult brengen.</br>[Gegevensvoorinstelling gebruiken om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema](https://experienceleague.adobe.com/en/docs/experience-platform/data-prep/home) |
| **Bronverbinding voor analyse**</br> Als uw Adobe Analytics-implementatie AppMeasurement of de extensie Analytics is, kunt u beginnen met het verzenden van gegevens naar een gegevensweergave in Customer Journey Analytics.<p>Dit is de eenvoudigste manier om gegevens naar de Customer Journey Analytics te krijgen, maar op de lange termijn is dit de minst haalbare methode.</p> | Nee | Een toewijzing wordt niet vereist omdat de Verbinding van de Bron van Analytics uw bestaand schema van Adobe Analytics eerder dan het schema XDM gebruikt. |

{style="table-layout:auto"}

<!-- Does it benefit the customer to do this all at the same time if they're using multiple AEP apps? If so, have multiple sections like this. Or can they do CJA first and AJO later?

### Plan data mapping for Customer Journey Analytics


### Plan data mapping for Customer Journey analytics and other Adobe Experience platform applications

-->

## Daarna, bewaart historische gegevens

Kies vervolgens de methode die u wilt gebruiken [historische Adobe Analytics-gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md).
