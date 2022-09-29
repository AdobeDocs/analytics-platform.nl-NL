---
title: Adobe Journey Optimizer met Customer Journey Analytics integreren
description: Breng door AJO gegenereerde gegevens in en analyseer deze met Analysis Workspace in CJA.
source-git-commit: 28bc99a7f5ec7b280fd26a7a45dc076e67f652dc
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 1%

---


# Adobe Journey Optimizer met Customer Journey Analytics integreren

[Adobe Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html?lang=nl) helpt u verbonden, contextafhankelijke en persoonlijke ervaringen te bieden. Het helpt uw klanten aan de volgende stap in hun klantenreis blootstellen.

U kunt gegevens die door Journey Optimizer zijn gegenereerd, importeren om een geavanceerde analyse uit te voeren in Customer Journey Analytics door de volgende stappen uit te voeren:

## Gegevens verzenden van Journey Optimizer naar Adobe Experience Platform

Adobe Experience Platform fungeert als de centrale gegevensbron en de verbinding tussen Journey Optimizer en Customer Journey Analytics. Zie [Aan de slag met gegevenssets](https://experienceleague.adobe.com/docs/journey-optimizer/using/data-management/datasets/get-started-datasets.html) in de Journey Optimizer-gebruikershandleiding voor informatie over het verzenden van Journey Optimizer-gegevens naar Platform als een gegevensset.

## Verbinding maken in Customer Journey Analytics

Zodra Journey Optimizer-gegevens in Adobe Experience Platform zijn opgeslagen, kunt u [Verbinding maken](/help/connections/create-connection.md) op basis van uw Journey Optimizer-gegevensset. Selecteer de gegevensset die u naar het Platform hebt verzonden.

## De gegevensweergave configureren om de afmetingen en afmetingen van Journey Optimizer aan te passen

Nadat u een verbinding hebt gemaakt, kunt u een of meer [Gegevens](/help/data-views/create-dataview.md) om de gewenste afmetingen en metriek te vormen beschikbaar in Customer Journey Analytics.

U kunt de volgende metriek in een gegevensmening tot stand brengen om gelijke gelijkheid met gelijkaardige metriek in Journey Optimizer te bereiken. Zie [Componentinstellingen](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond hoe te om afmetingen en metriek aan te passen.

| Metrisch | Beschrijving | Instellingen voor gegevensweergave |
| --- | --- | --- |
| Bounces | Het aantal berichten dat is teruggestuurd | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Als aan bepaalde criteria is voldaan<br>Gelijk aan: `bounce`<br>Gelijk aan: `denylist` |
| Fouten | Het aantal berichten dat is uitgevallen | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `error` |
| Exclusief | Het aantal uitgesloten berichten | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `exclude` |
| Abonnementen opzeggen | Het aantal aftekeningmeldingen | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageInteraction.interactionType` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `unsubscribe` |
| Klikken | Het aantal klikken binnen berichten | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageInteraction.interactionType` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `click` |
| Openen | Het aantal geopende berichten | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageInteraction.interactionType` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `open` |
| Spam-klachten | Aantal klachten over spam | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageInteraction.interactionType` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `spam_complaint` |
| Berichten verzonden | Het aantal berichten dat is verzonden | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `sent` |
| Synchronisatiefouten | Het totale aantal berichten dat niet kon worden gesynchroniseerd | Het element SchemaString gebruiken `_experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category` met de volgende instellingen:<br>Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `sync` |

## Berekende metriek configureren met behulp van Journey Optimizer-meetgegevens

Zodra u de gewenste afmetingen en metriek voor de dataset van Journey Optimizer hebt gevormd, kunt u ook vormen [Berekende cijfers](/help/components/calc-metrics/calc-metr-overview.md) voor meer inzichten over die gegevens. Deze berekende metriek zijn gebaseerd op de bovengenoemde metriek die in de Manager van de Mening van Gegevens wordt gecreeerd.

| Berekende metrische waarde | Beschrijving | Formule |
| --- | --- | --- |
| Totaal aantal verzonden berichten | Het totale aantal verzonden, geslaagde of mislukte berichten | `[Messages successfully sent]` + `[Bounces]` + `[Sync failures]` |

## Verschillen in rapportage tussen Journey Optimizer en Customer Journey Analytics

Gegevensverschillen tussen producten liggen doorgaans tussen 1-2%. Grotere verschillen tussen producten kunnen mogelijk worden toegeschreven aan:

* De verwerkingstijd voor binnenkomende gegevens kan enigszins verschillen tussen producten, vooral voor gegevens die binnen de laatste twee uur worden verzameld. Gebruik datumbereiken met uitzondering van vandaag om verschillen in verwerkingstijd te verkleinen.
* De berekende metrische &quot;Totaal verzonden berichten&quot;omvat niet metrisch &quot;probeert&quot;. Gegevens voor de metrische waarde &#39;Retries&#39; zijn niet opgenomen in de Dataset en tonen mogelijk lagere aantallen in CJA-rapportage versus AJO-rapportage. Nochtans, worden de gegevens van het nieuwe begin samengekomen in &quot;Berichten met succes verzonden&quot;of metrische &quot;Bounces&quot;. De datumwaaiers van het gebruik een week of ouder om discrepanties met de &quot;Totale verzonden berichten&quot;metrisch tussen producten te verlichten.
