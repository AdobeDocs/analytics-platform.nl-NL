---
title: Adobe Journey Optimizer-beslissingsbeheer integreren
description: Neem gegevens die door Adobe Journey Optimizer Decision Management zijn gegenereerd, in Customer Journey Analytics in en analyseer deze met Analysis Workspace.
exl-id: fde45264-46cf-4c68-9872-7fb739748f21
feature: Experience Platform Integration
role: Admin
source-git-commit: 979564d0249abadd454ce43aba9aeae2c78a44f0
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Beslissingsbeheer integreren


Het Beheer van het Besluit van Adobe Journey Optimizer ](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html) maakt verpersoonlijking gemakkelijk met een centrale bibliotheek van marketing aanbiedingen en een besluitvormingsmotor die regels en beperkingen op rijke, in real time profielen toepast die door Adobe Experience Platform worden gecreeerd om u te helpen uw klanten het juiste aanbod op het juiste ogenblik verzenden.[

Beslissingsbeheer is onderdeel van en geïntegreerd met Adobe Journey Optimizer. Het kan ook onafhankelijk van reizen en campagnes worden gebruikt die in Adobe Journey Optimizer worden bepaald, gebruikend zijn rijke [ API ](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/getting-started.html) steun.

U kunt gegevens invoeren die door Beslissingsbeheer worden geproduceerd om geavanceerde analyse in Customer Journey Analytics uit te voeren door de volgende stappen uit te voeren:

## Gegevens van Beslissingsbeheer naar Adobe Experience Platform verzenden

Adobe Experience Platform fungeert als de centrale gegevensbron en als schakel tussen besluitvormingsbeheer en Customer Journey Analytics. De gegevens van het Beheer van het Besluit worden verzameld automatisch in Experience Platform **** of als deel van **uitdrukkelijk verzonden ervaringsgebeurtenissen** (bijvoorbeeld impressies of kliks). Zie [ Begonnen het worden met gegevensinzameling ](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/collect-event-data/data-collection.html) voor meer details.

## Verbinding maken

Zodra de gegevens van het Beheer van het Besluit in Adobe Experience Platform zijn, kunt u a [ Verbinding ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) tot stand brengen die op uw datasets van het Beheer van het Besluit wordt gebaseerd. Of u kunt gegevenssets voor Beslissingsbeheer toevoegen aan een bestaande verbinding.

Selecteer en vorm de volgende datasets:

| Gegevensset | Het type DataSet | Verbindingsinstellingen | Beschrijving |
| --- | --- | --- | --- |
| ODE DecisonEvents - _zandbak_ beslissing | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat automatisch gegenereerde gegevens voor besluitvormingsgebeurtenissen van het Beheer van Besluit. _Sandbox_ verwijst naar de specifieke zandbaknaam. |
| Dataset voor Adobe Journey Optimizer-feedbackgebeurtenis | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor berichtlevering. |
| Adobe Journey Optimizer Email Tracking Experience Event Dataset | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor het bijhouden van e-mail. |
| Dataset voor Adobe Journey Optimizer Push Tracking Experience | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor het bijhouden van pushberichten. |
| Gegevensset Adobe Journey Optimizer Entiteit | Opzoeken | Sleutel: `_id`<br> Vergelijkende Sleutel: `_experience.decisioning.propositions.`<br>`scopeDetails.correlationID` | Bevat classificaties die de meta-gegevens van de Reis en van de Campagne aan alle gebeurtenisgegevens van Adobe Journey Optimizer associëren. |

{style="table-layout:auto"}

## Een gegevensweergave maken

Nadat een verbinding wordt gecreeerd, kunt u één of meerdere [ Meningen van Gegevens ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) tot stand brengen om de gewenste dimensies en metriek te vormen beschikbaar in Customer Journey Analytics.

>[!NOTE]
>
>De verschillen tussen gegevens tussen Adobe Journey Optimizer en Customer Journey Analytics zijn doorgaans kleiner dan 1-2%. Grotere verschillen zijn mogelijk voor gegevens die in de laatste twee uur zijn verzameld. Gebruik datumbereiken met uitzondering van vandaag om verschillen in verwerkingstijd te verkleinen.

### Dimensies configureren

U kunt de volgende afmetingen in een gegevensmening tot stand brengen om benaderende pariteit met gelijkaardige dimensies in Beslissingsbeheer te bereiken. Zie [ montages van de Component ](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond de opties van de afmetingsaanpassing.

| Dimension | Schema-element | Componentinstellingen |
| --- | --- | --- |
| Naam activiteit | `_experience.decisioning.`<br/>`propositionDetails.activity.name` | Componenttype: Dimension |
| Container-id | `_experience.decisioning.containerID` | Componenttype: Dimension |
| Correlatie-id | `_experience.decisioning.`<br/>`propositions.scopeDetails.correlationID` | Componenttype: Dimension |
| Naam van beslissingsoptie | `_experience.decisioning.`<br/>`propositionDetails.selections.name` | Componenttype: Dimension |
| Naam van optie voor alternatieven | `_experience.decisioning.`<br/>`propositionDetails.fallback.name` | Componenttype: Dimension |
| Plaatsingsnaam | `_experience.decisioning.`<br/>`propositionDetails.placement.name` | Componenttype: Dimension |

{style="table-layout:auto"}


### Metrische gegevens configureren

U kunt de volgende metriek in een gegevensmening tot stand brengen om benaderende pariteit met gelijkaardige metriek in Beslissingsbeheer te bereiken. Zie [ montages van de Component ](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond metrieke aanpassingsopties.

| Metrisch | Beschrijving | Schema-element | Componentinstellingen |
| --- | --- | --- | --- |
| Het Type van gebeurtenis (noem anders om naar een specifieke gebeurtenis te verwijzen, bijvoorbeeld `Feedback` voor `message.feedback`) [ 1 ] | Hoeveelheid van een specifiek type gebeurtenis | `eventType` | Componenttype: Metrisch <br/>**[!UICONTROL Set Include Exclude Values]**: Aan<br/>**[!UICONTROL Match]**: [!UICONTROL If all criteria are met]<br/>**[!UICONTROL Criteria]**:**[!UICONTROL Equals]**`message.feedback` |
| Beslissingsoptiescore | Berekende waarde voor een beslissingsoptie in de context van één bereik. | `_experience.decisioning.`<br/>`propositionDetails.selections.score` | Componenttype: Metrisch |
| Reservekopiescore voor alternatieven | Berekende waarde voor een back-upbeslissingsoptie in de context van één bereik. | `_experience.decisioning.`<br/>`propositionDetails.fallback.score` | Componenttype: Metrisch |
| Voorstel afgewezen | Het aantal aanbiedingen dat zonder enige andere directe interactie wordt afgewezen of afgewezen. | `_experience.decisioning.`<br/>`propositionEventType.dismiss` | Componenttype: Metrisch |
| Weergave aanbiedingen | Het aantal aanbiedingen dat aan het profiel wordt getoond. | `_experience.decisioning.`<br/>`propositionEventType.display` | Componenttype: Metrisch |
| Interactie van aanbiedingen | Het aantal aanbiedingen waarmee het profiel interactie had. | `_experience.decisioning.`<br/>`propositionEventType.interact` | Componenttype: Metrisch |
| Verzendvoorstellen | Het aantal voorstellen dat naar het profiel is verzonden. | `_experience.decisioning.`<br/>`propositionEventType.send` | Componenttype: Metrisch |
| Trigger voor aanbiedingen | Het aantal aanbiedingen dat is gekozen om door de client-SDK te worden weergegeven. | `_experience.decisioning.`<br/>`propositionEventType.trigger` | Componenttype: Metrisch |
| Abonnement op voorstellen opgezegd | Het aantal aanbiedingen dat wordt aangevraagd door profiel, hoeft in de toekomst niet te worden weergegeven. | `_experience.decisioning.`<br/>`propositionEventType.unsubscribe` | Componenttype: Metrisch |

{style="table-layout:auto"}

[ 1 ] U kunt veelvoudige metriek voor de diverse beschikbare gebeurtenistypen bepalen. Zie [ omvatten omvat de montages van de waardecomponent ](/help/data-views/component-settings/include-exclude-values.md) voor meer informatie.
