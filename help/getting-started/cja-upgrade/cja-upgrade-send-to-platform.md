---
title: Gegevens verzenden naar Adobe Experience Platform tijdens migreren naar Customer Journey Analytics
description: Gegevens verzenden naar Adobe Experience Platform tijdens migreren naar Customer Journey Analytics
solution: Customer Journey Analytics
feature: Basics
exl-id: d9d7f186-9077-4372-94ad-8dd5b97779ca
source-git-commit: 6cceeaa3b57808a82012b124435aa1b7dbf1b3f2
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%

---

# Stap 3: Gegevens naar Adobe Experience Platform verzenden bij een upgrade

++ + breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere verbeteringsproces past. Zorg ervoor dat alle vorige upgradestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige upgradetaken hebt uitgevoerd.

De informatie op deze pagina behandelt Stap 3 van het verbeteringsproces, zoals benadrukt in de hieronder lijst:

| Upgradetaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de upgrade](/help/getting-started/cja-upgrade/cja-upgrade-getstarted.md)** | Leer de voordelen van een upgrade naar de Customer Journey Analytics en het standaard upgradeproces. |
| **Stap 2: [Het upgradepad kiezen](/help/getting-started/cja-upgrade/cja-upgrade-path.md)** | Er zijn verschillende methoden beschikbaar voor de upgrade naar de Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| <span class="preview">**Stap 3: Gegevens verzenden naar Adobe Experience Platform**</span> | <span class="preview">Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van het upgradepad dat u hebt gekozen in Stap 2.</span> |
| **Stap 4: [Historische gegevens behouden](/help/getting-started/cja-upgrade/cja-upgrade-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 5: [Extra implementatietaken uitvoeren](/help/getting-started/cja-getting-started.md)** | Op dit punt in het verbeteringsproces, moet u diverse taken uitvoeren alvorens uw milieu van de Customer Journey Analytics klaar is te gebruiken.<p>Deze extra taken zijn van toepassing op upgrades vanuit Adobe Analytics en op nieuwe implementaties van Customers Journey Analytics.</p><p>Deze taken omvatten:</p><ul><li>Andere gegevens in Experience Platform plaatsen</li><li>Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics</li><li>Gegevensweergaven maken</li><li>Het gebruik van de API voor rapportage porteren</li><li>Verantwoording van gegevensfeeds en -Data Warehouse</li><li>Projecten en onderdelen migreren</li><li>Gebruiker aan boord plannen</li></ul> <p>Zie voor meer informatie [Aan de slag met Customer Journey Analytics](/help/getting-started/cja-getting-started.md). |

{style="table-layout:auto"}

+++


Na u [kiezen voor het upgradepad](/help/getting-started/cja-upgrade/cja-upgrade-path.md) dat het beste is voor uw organisatie, kunt u beginnen gegevens naar Adobe Experience Platform te verzenden om het in Customer Journey Analytics ter beschikking te stellen.

Het proces voor het verzenden van gegevens naar Experience Platform voor elk verbeteringspad wordt hieronder getoond. Volg de verbindingen in de lijst voor gedetailleerde configuratieinformatie.

| Upgradepad | Proces voor het verzenden van gegevens naar platform | Aanvullende informatie |
|---------|----------|----------|
| Nieuwe implementatie van het Web SDK van het Experience Platform | <ol><li>Maak een XDM-schema voor uw organisatie.<p>Werk met uw gegevensteam om het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics te identificeren.</p></li><li>Voer SDK van het Web van het Experience Platform uit.</li><li>Gegevens verzenden naar platform.</li></ol><p>Voor gedetailleerde informatie over elk van deze stappen, zie [Gegevens invoeren via de Adobe Experience Platform Web SDK](/help/data-ingestion/aepwebsdk.md). | Omdat dit een nieuwe implementatie van het Web SDK van het Experience Platform is, wordt de schemaafbeelding niet vereist omdat u het schema als één van de eerste stappen tijdens implementatie moet tot stand brengen. |
| Uw Adobe Analytics-implementatie migreren voor gebruik van de Web SDK | <ol><li>Verplaats uw bestaande Adobe Analytics-implementatie naar de SDK van het Web Experience Platform en bevestig vervolgens dat alles in Adobe Analytics werkt.<p>Voor informatie over hoe te om dit te doen, gebruik de volgende middelen, afhankelijk van of uw huidige implementatie de de marktextenuitbreiding of het AppMeasurement van de Analytics is:</p><ul><li>Als u de extensie Analytics gebruikt, raadpleegt u [Migreren van de Adobe Analytics-tagextensie naar de Web SDK-tagextensie](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/analytics-extension-to-web-sdk)</li><li>Als u AppMeasurement gebruikt, zie [Migreren van AppMeasurement naar de Web SDK](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/appmeasurement-to-web-sdk)</li></ul><li>[Een XDM-schema voor uw organisatie maken](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-schema-and-dataset).<p>Werk met uw gegevensteam om het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics te identificeren.</p></li><li>[Gegevensvoorinstelling gebruiken om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema](https://experienceleague.adobe.com/en/docs/experience-platform/data-prep/home).</li><li>Gegevens naar platform verzenden door [een gegevensstroom instellen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-datastream).</li></ol> |  |
| Configureer uw bestaande Adobe Analytics Web SDK-implementatie om gegevens naar de Customer Journey Analytics te verzenden | <ol><li>Gegevens naar platform verzenden door [een gegevensstroom instellen](/help/data-ingestion/aepwebsdk.md#set-up-a-datastream).<p>Omdat uw Adobe Analytics-implementatie al gebruikmaakt van de SDK van het Web Experience Platform, kunt u de andere secties in [Gegevens invoeren via de Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk).</p><p>Als u al gegevens naar Platform verzendt met uw Adobe Analytics-implementatie, is deze stap niet vereist. U moet eenvoudig een verbinding tussen de datasets van het Platform en Customer Journey Analytics tot stand brengen, zoals later in dit proces wordt beschreven.</p></li><li>(Optioneel) [Een XDM-schema voor uw organisatie maken](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-schema-and-dataset).<p>Werk met uw gegevensteam om het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics te identificeren.</p><p>Opmerking: zie voor informatie over de voordelen van het maken van een XDM-schema [Kies uw schema](/help/getting-started/cja-upgrade/cja-upgrade-path.md#choose-your-schema).</li><li>(Voorwaardelijk) Als u een XDM-schema hebt gemaakt, [Gebruik Gegevensvoorinstelling om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema](https://experienceleague.adobe.com/en/docs/experience-platform/data-prep/home).</li></ol> |
| De Bronverbinding Analytics gebruiken | [Gegevens van traditionele Adobe Analytics verzamelen en gebruiken](/help/data-ingestion/analytics.md) | Adobe Analytics-gegevens worden automatisch toegewezen aan het XDM-schema wanneer u de Bronverbinding Analytics gebruikt. Aanvullende toewijzing is niet vereist. |

## Daarna, bewaart historische gegevens

Daarna bepaalt u hoe u [historische Adobe Analytics-gegevens behouden](/help/getting-started/cja-upgrade/cja-upgrade-historical-data.md).
