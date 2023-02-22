---
title: Adobe Journey Optimizer (AJO) integreren met Customer Journey Analytics (CJA)
description: Breng door AJO gegenereerde gegevens in en analyseer deze met Analysis Workspace in CJA.
exl-id: 9333ada2-b4d6-419e-9ee1-5c96f06a3bfd
source-git-commit: 3a4dbe9a87f8e195a4daf78423d29d73f2be0f83
workflow-type: tm+mt
source-wordcount: '647'
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

>!![NOTE]
De verschillen in gegevens tussen AJO en CJA zijn doorgaans minder dan 1-2%. Grotere verschillen zijn mogelijk voor gegevens die in de laatste twee uur zijn verzameld. Gebruik datumbereiken met uitzondering van vandaag om verschillen in verwerkingstijd te verkleinen.

### Dimensies configureren in de gegevensweergave

In Journey Optimizer kunt u de volgende afmetingen maken om een vergelijkbare pariteit met vergelijkbare afmetingen te bereiken. Zie [Componentinstellingen](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond afmetingsaanpassingsopties.

| Dimension | Schema-element | Componentinstellingen |
| --- | --- | --- |
| Reisnaam | `_experience.customerJourneyManagement.`<br>`entities.journey.journeyName` | Componenttype: Dimension |
| Naam en versie van reis | `_experience.customerJourneyManagement.`<br>`entities.journey.journeyNameAndVersion` | Componenttype: Dimension |
| Naam van knooppunt | `_experience.customerJourneyManagement.`<br>`entities.journey.journeyName` | Componenttype: Dimension |
| Type knooppunt | `_experience.customerJourneyManagement.`<br>`entities.journey.journeyNodeType` | Componenttype: Dimension |
| Campagneraam | `_experience.customerJourneyManagement.`<br>`entities.campaign.name` | Componenttype: Dimension |
| Kanaal | `_experience.customerJourneyManagement.`<br>`entities.channelDetails.channel._id` | Componenttype: Dimension |
| Titel duwen | `_experience.customerJourneyManagement.`<br>`entities.channelDetails.push.title` | Componenttype: Dimension |
| E-mailonderwerp | `_experience.customerJourneyManagement.`<br>`entities.channelDetails.email.subject` | Componenttype: Dimension |
| Koppelingslabel | `_experience.customerJourneyManagement.`<br>`messageInteraction.label` | Componenttype: Dimension |
| Naam experiment | `_experience.customerJourneyManagement.`<br>`entities.experiment.experimentName` | Componenttype: Dimension<br>Contextlabels: Experimentatieexperiment |
| Naam behandeling | `_experience.customerJourneyManagement.`<br>`entities.experiment.treatmentName` | Componenttype: Dimension<br>Contextlabels: Experimentvariant |
| Reden voor mislukte e-maillevering | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.messageFailure.reason` | Componenttype: Dimension |
| Reden voor uitsluiting van e-mail | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.messageExclusion.reason` | Componenttype: Dimension |

{style=&quot;table-layout:auto&quot;}

### Metriek configureren in de gegevensweergave

U kunt de volgende metriek in een gegevensmening tot stand brengen om gelijke gelijkheid met gelijkaardige metriek in Journey Optimizer te bereiken. Zie [Componentinstellingen](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond metriek aanpassingsopties.

| Metrisch | Beschrijving | Schema-element | Componentinstellingen |
| --- | --- | --- | --- |
| Bounces | Het aantal berichten dat is teruggedraaid, inclusief zowel directe stuitingen als stuitingen na levering. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Als aan bepaalde criteria is voldaan<br>Gelijk aan: `bounce`, is gelijk aan: `denylist` |
| Stortingen na levering | Sommige e-mailservices melden de geleverde e-mailberichten en sturen deze later weer op. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.messageFailure.category` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `async` |
| E-mailklikken | De telling van kliks binnen berichten. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `click` |
| E-mailopenen | Het aantal geopende berichten. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `open` |
| Fouten | Het aantal berichten dat uittrok. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `error` |
| Exclusief | Het aantal uitgesloten berichten. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `exclude` |
| Verzenden | Het aantal berichten dat e-mailproviders hebben geaccepteerd. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `sent` |
| Spam-klachten | Het aantal spamklachten. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `spam_complaint` |
| Abonnementen opzeggen | The count of unsubscribes. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Waarden voor uitsluiten opnemen: Gelijk `unsubscribe` |

{style=&quot;table-layout:auto&quot;}

### Berekende waarden configureren in Analysis Workspace

Zodra u de gewenste afmetingen en metriek voor de dataset van Journey Optimizer hebt gevormd, kunt u ook vormen [Berekende cijfers](/help/components/calc-metrics/calc-metr-overview.md) voor meer inzichten over die gegevens. Deze berekende metriek zijn gebaseerd op de bovengenoemde metriek die in de Manager van de Mening van Gegevens wordt gecreeerd.

| Berekende metrische waarde | Beschrijving | Formule |
| --- | --- | --- |
| Berichten verzonden | Het totale aantal verzonden berichten. Bevat gelukte of mislukte berichten. | `[Sends] + [Bounces] - [Bounces After Delivery]` |
| Berichten geleverd | Het aantal e-mails dat aan klanten wordt geleverd. | `[Sends] - [Bounces After Delivery]` |

{style=&quot;table-layout:auto&quot;}
