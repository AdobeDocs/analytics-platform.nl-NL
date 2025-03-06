---
title: Gegevens verzenden naar Adobe Experience Platform tijdens migreren naar Customer Journey Analytics
description: Gegevens verzenden naar Adobe Experience Platform tijdens migreren naar Customer Journey Analytics
solution: Customer Journey Analytics
feature: Basics
exl-id: d9d7f186-9077-4372-94ad-8dd5b97779ca
source-git-commit: 773c03dfec99abcabdc667c549cce0dc1b1aabc4
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# Stap 3: Gegevens naar Adobe Experience Platform verzenden bij een upgrade

++ + breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere verbeteringsproces past. Zorg ervoor dat alle vorige upgradestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige upgradetaken hebt uitgevoerd.

De informatie op deze pagina behandelt Stap 3 van het verbeteringsproces, zoals benadrukt in de hieronder lijst:

| Upgradetaak | Details |
|---------|----------|
| **Stap 1: [ wordt begonnen met de verbetering](/help/getting-started/cja-upgrade/cja-upgrade-getstarted.md)** | Leer de voordelen van een upgrade naar Customer Journey Analytics en het standaard upgradeproces. |
| **Stap 2: [ kies de verbeteringspad](/help/getting-started/cja-upgrade/cja-upgrade-path.md)** | Er zijn verschillende methoden beschikbaar voor de upgrade naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| <span class="preview">**Stap 3: Verzend gegevens naar Adobe Experience Platform**</span> | <span class="preview"> het proces om gegevens naar Adobe Experience Platform te verzenden verschilt afhankelijk van de verbeteringspad die u in Stap 2 koos.</span> |
| **Stap 4: [ behoud historische gegevens](/help/getting-started/cja-upgrade/cja-upgrade-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 5: [ voer extra implementatietaken uit](/help/getting-started/cja-getting-started.md)** | Op dit punt in het upgradeproces moet u verschillende taken uitvoeren voordat uw Customer Journey Analytics-omgeving gebruiksklaar is.<p>Deze extra taken zijn van toepassing op upgrades vanuit Adobe Analytics en nieuwe Customer Journey Analytics-implementaties.</p><p>Deze taken omvatten:</p><ul><li>Andere gegevens in Experience Platform plaatsen</li><li>Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics</li><li>Gegevensweergaven maken</li><li>Het gebruik van de API voor rapportage porteren</li><li>Boekhouding voor gegevensfeeds en Data Warehouse</li><li>Projecten en onderdelen migreren</li><li>Gebruiker aan boord plannen</li></ul> <p>Voor meer informatie, zie [ Customer Journey Analytics Begonnen ](/help/getting-started/cja-getting-started.md) worden. |

{style="table-layout:auto"}

+++


Nadat u [ de verbeteringspad ](/help/getting-started/cja-upgrade/cja-upgrade-path.md) kiest die voor uw organisatie het best is, kunt u beginnen verzendend gegevens naar Adobe Experience Platform om het in Customer Journey Analytics beschikbaar te maken.

Het proces voor het verzenden van gegevens naar Experience Platform voor elk upgradepad wordt hieronder weergegeven. Volg de verbindingen in de lijst voor gedetailleerde configuratieinformatie.

| Upgradepad | Proces voor het verzenden van gegevens naar platform | Aanvullende informatie |
|---------|----------|----------|
| Nieuwe implementatie van de Experience Platform Web SDK | <ol><li>Maak een XDM-schema voor uw organisatie.<p>Werk samen met uw gegevensteam om het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics te identificeren.</p></li><li>Implementeer de Experience Platform Web SDK.</li><li>Gegevens verzenden naar platform.</li></ol><p>Voor gedetailleerde informatie over elk van deze stappen, zie [ Gegevens van de Samenvatting via het Web SDK van Adobe Experience Platform ](/help/data-ingestion/aepwebsdk.md). | Omdat dit een nieuwe implementatie van het Web SDK van Experience Platform is, wordt de schemaafbeelding niet vereist omdat u het schema als één van de eerste stappen tijdens implementatie moet tot stand brengen. |
| Een Adobe Analytics-implementatie migreren voor gebruik van de Web SDK | <ol><li>Verplaats uw bestaande Adobe Analytics-implementatie naar de Experience Platform Web SDK en bevestig vervolgens dat alles werkt in Adobe Analytics.<p>Gebruik de volgende bronnen voor informatie over hoe u dit doet, afhankelijk van het feit of uw huidige implementatie de extensie Analytics of AppMeasurement is:</p><ul><li>Als u de de markeringsuitbreiding van de Analyse gebruikt, zie [ van de de markeringsuitbreiding van Adobe Analytics aan de de markeringsuitbreiding van SDK van het Web ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/analytics-extension-to-web-sdk) migreren</li><li>Als u AppMeasurement gebruikt, zie [ Migreer van AppMeasurement aan het Web SDK ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/appmeasurement-to-web-sdk)</li></ul><li>[ creeer een schema XDM voor uw organisatie ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-schema-and-dataset).<p>Werk samen met uw gegevensteam om het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics te identificeren.</p></li><li>[ Prep van Gegevens van het Gebruik om alle gebieden in het gegevensvoorwerp aan uw XDM schema ](https://experienceleague.adobe.com/en/docs/experience-platform/data-prep/home) in kaart te brengen.</li><li>Begin verzendend gegevens naar Platform door [ vestiging een datastream ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-datastream).</li></ol> |  |
| Configureer uw bestaande Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden | <ol><li>Begin verzendend gegevens naar Platform door [ vestiging een datastream ](/help/data-ingestion/aepwebsdk.md#set-up-a-datastream).<p>Omdat uw implementatie van Adobe Analytics reeds de SDK van het Web van Experience Platform gebruikt, kunt u de andere secties in [ negeren samenvoegt gegevens via het Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk).</p><p>Als u al gegevens naar Platform verzendt met uw Adobe Analytics-implementatie, is deze stap niet vereist. U moet eenvoudig een verbinding tussen de datasets van het Platform en Customer Journey Analytics tot stand brengen, zoals later in dit proces wordt beschreven.</p></li><li>(Facultatief) [ creeer een schema XDM voor uw organisatie ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk#set-up-a-schema-and-dataset).<p>Werk samen met uw gegevensteam om het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics te identificeren.</p><p>Nota: Voor informatie over de voordelen om een schema te creëren XDM, zie [ uw schema ](/help/getting-started/cja-upgrade/cja-upgrade-path.md#choose-your-schema) kiezen.</li><li>(Voorwaardelijk) als u een schema XDM creeerde, [ gebruiksGegevens Prep om alle gebieden in het gegevensvoorwerp aan uw schema XDM ](https://experienceleague.adobe.com/en/docs/experience-platform/data-prep/home) in kaart te brengen.</li></ol> |  |
| De bronaansluiting Analytics gebruiken | [ Samenvatting en gebruiksgegevens van traditionele Adobe Analytics ](/help/data-ingestion/analytics.md) | Adobe Analytics-gegevens worden automatisch toegewezen aan het XDM-schema wanneer u de bronconnector Analytics gebruikt. Aanvullende toewijzing is niet vereist. |

## Daarna, bewaart historische gegevens

Daarna, besluit hoe u [ historische gegevens van Adobe Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-historical-data.md) zult behouden.
