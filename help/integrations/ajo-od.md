---
title: Adobe Journey Optimizer-beheer voor Besluit integreren met Customer Journey Analytics (CJA)
description: Neem gegevens die door Adobe Journey Optimizer Decision Management zijn gegenereerd, in Customer Journey Analytics op en analyseer deze met Analysis Workspace.
source-git-commit: 00a87f5f370310672ca37ab9df08350d14fc6a91
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Beslissingsbeheer integreren met Customer Journey Analytics


Adobe Journey Optimizer [Beslissingsbeheer](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=en) maakt verpersoonlijking gemakkelijk met een centrale bibliotheek van marketing aanbiedingen en een besluitvormingsmotor die regels en beperkingen op rijke, real-time profielen toepast die door Adobe Experience Platform worden gecreeerd om u te helpen uw klanten het juiste aanbod op het juiste ogenblik verzenden.

Beslissingsbeheer maakt deel uit van en is geïntegreerd met Adobe Journey Optimizer (AJO). Het kan ook worden gebruikt onafhankelijk van reizen en campagnes die in de AJO zijn gedefinieerd, met behulp van zijn rijke [API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/getting-started.html?lang=en) ondersteuning.

U kunt gegevens invoeren die door Beslissingsbeheer worden geproduceerd om geavanceerde analyse in Customer Journey Analytics (CJA) uit te voeren door de volgende stappen uit te voeren:

## Gegevens van Beslissingsbeheer naar Adobe Experience Platform verzenden

Adobe Experience Platform fungeert als de centrale gegevensbron en als schakel tussen Besluitbeheer en Customer Journey Analytics. Gegevens van het besluitvormingsbeheer worden in Experience Platform verzameld **automatisch** of als onderdeel van **expliciet verzonden ervaringsgebeurtenissen** (bijvoorbeeld afbeeldingen of klikken). Zie [Aan de slag met gegevensverzameling](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/collect-event-data/data-collection.html?lang=en) voor meer informatie .

## Verbinding maken

Zodra de gegevens van het Beslissingsbeheer in Adobe Experience Platform zijn, kunt u tot een [Verbinding](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en) op basis van uw gegevensbestanden voor Beslissingsbeheer. Of u kunt gegevenssets voor Beslissingsbeheer toevoegen aan een bestaande verbinding.

Selecteer en vorm de volgende datasets:

| Gegevensset | Het type DataSet | Verbindingsinstellingen | Beschrijving |
| --- | --- | --- | --- |
| ODE-beslissingsgebeurtenissen - _sandbox_ beslissing | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat automatisch gegenereerde gegevens voor besluitvormingsgebeurtenissen van het Beheer van Besluit. _Sandbox_ verwijst naar de specifieke naam van de sandbox. |
| Dataset voor AJO-feedbackgebeurtenis | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor berichtlevering. |
| Dataset voor AJO-e-mailtrackingervaring | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor het bijhouden van e-mail. |
| Dataset voor AJO-gebeurtenis voor het bijhouden van push | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor het bijhouden van pushberichten. |
| Dataset AJO-entiteit | Opzoeken | Sleutel: `_id`<br>Overeenkomende sleutel: `_experience.decisioning.propositions.`<br>`scopeDetails.correlationID` | Bevat classificaties die de meta-gegevens van de Reizen en van de Campagne aan alle gebeurtenisgegevens van AJO associëren. |

{style="table-layout:auto"}

## Een gegevensweergave maken

Nadat u een verbinding hebt gemaakt, kunt u een of meer [Gegevens](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en) om de gewenste afmetingen en metriek te vormen beschikbaar in CJA.

>[!NOTE]
>
>De verschillen in gegevens tussen AJO en CJA zijn doorgaans minder dan 1-2%. Grotere verschillen zijn mogelijk voor gegevens die in de laatste twee uur zijn verzameld. Gebruik datumbereiken met uitzondering van vandaag om verschillen in verwerkingstijd te verkleinen.

### Dimensies configureren

U kunt de volgende afmetingen in een gegevensmening tot stand brengen om benaderende pariteit met gelijkaardige dimensies in Beslissingsbeheer te bereiken. Zie [Componentinstellingen](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond afmetingsaanpassingsopties.

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

U kunt de volgende metriek in een gegevensmening tot stand brengen om benaderende pariteit met gelijkaardige metriek in Beslissingsbeheer te bereiken. Zie [Componentinstellingen](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond metriek aanpassingsopties.

| Metrisch | Beschrijving | Schema-element | Componentinstellingen |
| --- | --- | --- | --- |
| Gebeurtenistype (naam wijzigen om naar een specifieke gebeurtenis te verwijzen, bijvoorbeeld `Feedback` for `message.feedback`) [1] | Hoeveelheid van een specifiek type gebeurtenis | `eventType` | Componenttype: Metrisch <br/>**[!UICONTROL Set Include Exclude Values]**: Aan<br/>**[!UICONTROL Match]**: [!UICONTROL If all criteria are met]<br/>**[!UICONTROL Criteria]**:**[!UICONTROL Equals]**`message.feedback` |
| Beslissingsoptiescore | Berekende waarde voor een beslissingsoptie in de context van één bereik. | `_experience.decisioning.`<br/>`propositionDetails.selections.score` | Componenttype: Metrisch |
| Reservekopiescore voor alternatieven | Berekende waarde voor een back-upbeslissingsoptie in de context van één bereik. | `_experience.decisioning.`<br/>`propositionDetails.fallback.score` | Componenttype: Metrisch |
| Voorstel afgewezen | Het aantal aanbiedingen dat zonder enige andere directe interactie wordt afgewezen of afgewezen. | `_experience.decisioning.`<br/>`propositionEventType.display` | Componenttype: Metrisch |
| Weergave aanbiedingen | Het aantal aanbiedingen dat aan het profiel wordt getoond. | `_experience.decisioning.`<br/>`propositionEventType.display` | Componenttype: Metrisch |
| Interactie van aanbiedingen | Het aantal aanbiedingen dat aan het profiel wordt getoond. | `_experience.decisioning.`<br/>`propositionEventType.interact` | Componenttype: Metrisch |
| Verzendvoorstellen | Het aantal voorstellen dat naar het profiel is verzonden. | `_experience.decisioning.`<br/>`propositionEventType.send` | Componenttype: Metrisch |
| Trigger voor aanbiedingen | Het aantal aanbiedingen dat is gekozen om door de client-SDK te worden weergegeven. | `_experience.decisioning.`<br/>`propositionEventType.trigger` | Componenttype: Metrisch |
| Abonnement op voorstellen opgezegd | Het aantal aanbiedingen dat wordt aangevraagd door profiel, hoeft in de toekomst niet te worden weergegeven. | `_experience.decisioning.`<br/>`propositionEventType.trigger` | Componenttype: Metrisch |

{style="table-layout:auto"}

[1] U kunt meerdere metriek definiëren voor de verschillende beschikbare gebeurtenistypen. Zie [Inclusief instellingen van waardecomponent](/help/data-views/component-settings/include-exclude-values.md) voor meer informatie .