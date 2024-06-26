---
title: Adobe Journey Optimizer integreren met Customer Journey Analytics
description: Breng gegevens die door Adobe Journey Optimizer zijn gegenereerd, in Customer Journey Analytics en analyseer deze met Analysis Workspace.
exl-id: 9333ada2-b4d6-419e-9ee1-5c96f06a3bfd
feature: Experience Platform Integration
role: Admin
source-git-commit: 529dd2ed2af60f8b417a5bf7d728a201dad70218
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# Journey Optimizer integreren met Customer Journey Analytics

[Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) helpt u verbonden, contextafhankelijke en gepersonaliseerde ervaringen te bieden. Het helpt uw klanten aan de volgende stap in hun klantenreis blootstellen.

U kunt gegevens vormen die door Journey Optimizer worden geproduceerd om geavanceerde analyse in Customer Journey Analytics uit te voeren. U kunt deze integratie automatisch configureren. Indien nodig, kunt u extra, handaanpassingen aan de datasets, afmetingen, of metriek maken die in uw verbinding of gegevensmeningen beschikbaar zijn.

## Journey Optimizer-integratie automatisch configureren

{{release-limited-testing-section}}

Journey Optimizer biedt ondersteuning voor het gebruik van Customer Journey Analytics als rapportageengine. Zie [Ga aan de slag met de nieuwe rapportinterface](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja) in de documentatie van Journey Optimizer.

Als u rapportage van Customers Journey Analytics voor Journey Optimizer hebt ingeschakeld, wordt automatisch een [verbinding](/help/connections/overview.md) en [gegevensweergave](/help/data-views/data-views.md) worden gemaakt voor de specifieke sandbox.

### Verbinding

De verbinding heeft de naam **[!UICONTROL AJO Enabled Connection (*naam sandbox *)]**en heeft de volgende uit de vakwaarden voor configuratie en datasets:

| **Verbindingsinstellingen** | Waarde |
|---|---| 
| [!UICONTROL Connection name] | `AJO Enabled Connection (`_`sandbox name`_`)` |
| [!UICONTROL Connection description] | [!UICONTROL *Beschrijf hier uw verbinding*] |
| [!UICONTROL Tags] | [!UICONTROL *Labels selecteren*] |


| **Gegevensinstellingen** | Waarde |
|---|---| 
| [!UICONTROL Enable rolling data window] | Enabled. [!UICONTROL Selected number of months] `13`. |
| [!UICONTROL Sandbox] | [!UICONTROL *naam van sandbox*] (uitgeschakeld; u kunt deze instelling niet wijzigen). |
| [!UICONTROL Average number of daily events] | minder dan 1 miljoen (uitgeschakeld; u kunt deze instelling niet wijzigen). |


| Naam gegevensset | Schema | Het type DataSet | Type gegevensbron | Persoon-id | Sleutel | Overeenkomende sleutel | Nieuwe gegevens importeren | Backfill-gegevens |
|---|---|---|---|---|---|---|---|---|
| [!UICONTROL AJO Entity Dataset] | [!UICONTROL AJO Entity Record Schema] | [!UICONTROL Lookup] | [!UICONTROL Other] | - | ` _id` | `_experience.decisioning.`<br/>`propositions.scopeDetails.`<br/>`correlationID` | ![Status groen](assets/../../connections/assets/status-green.svg) Aan | ![Status grijs](assets/../../connections/assets/status-gray.svg) Uit |
| [!UICONTROL Journey Step Events] | [!UICONTROL Journey Step Event schema for Journey Orchestration] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL  IdentityMap(\<primary\>)] | - | - | ![Status groen](assets/../../connections/assets/status-green.svg) Aan | ![Status grijs](assets/../../connections/assets/status-gray.svg) Uit |
| [!UICONTROL AJO Email Tracking Experience Event Dataset] | [!UICONTROL AJO Email Tracking Experience Event Schema] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL IdentityMap(\<primary\>)] | - | - | ![Status groen](assets/../../connections/assets/status-green.svg) Aan | ![Status grijs](assets/../../connections/assets/status-gray.svg) Uit |
| [!UICONTROL AJO Email Tracking Experience Event Dataset] | [!UICONTROL AJO Email Tracking Experience Event Schema] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL IdentityMap(\<primary\>)] | - | - | ![Status groen](assets/../../connections/assets/status-green.svg) Aan | ![Status grijs](assets/../../connections/assets/status-gray.svg) Uit |
| [!UICONTROL AJO Message Feedback Event Dataset] | [!UICONTROL AJO Message Feedback Event Schema] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL IdentityMap(\<primary\>)] | - | - | ![Status groen](assets/../../connections/assets/status-green.svg) Aan | ![Status grijs](assets/../../connections/assets/status-gray.svg) Uit |
| [!UICONTROL AJO Push Tracking Experience Event Dataset] | [!UICONTROL AJO Push Tracking Experience Event Schema] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL IdentityMap(\<primary\>)] | - | - | ![Status groen](assets/../../connections/assets/status-green.svg) Aan | ![Status grijs](assets/../../connections/assets/status-gray.svg) Uit |


### Gegevens, weergave

De gegevensweergave heeft de naam **AJO Enable Data View (*naam sandbox*)**.

- In de **[!UICONTROL Configure]** worden de volgende waarden uit het vak geconfigureerd.

  | Instellingen | Waarde |
  |---|---|
  | [!UICONTROL Connection] | Verbinding met AJO ingeschakeld (*naam sandbox*) |
  | [!UICONTROL Name] | `AJO Enabled Data View (`_`sandbox name`_`)` |
  | [!UICONTROL External ID] | `AJO_Enabled_Data_View__`_`sandbox_name`_`_` (afgeleid van de naam) |
  | [!UICONTROL Description] | `undefined` |

  {style="table-layout:fixed"}

  | Compatibiliteit | Waarde |
  |---|---|
  | [!UICONTROL Set as default data view in Adobe Journey Optimizer] | Ingeschakeld (standaard).<br/><br/>Deze configuratieoptie staat u toe om een gegevensmening aan te wijzen om met Journey Optimizer, zonder de behoefte aan handconfiguratie te gebruiken. Voor informatie hoe te om deze configuratieoptie (als niet reeds toegelaten door gebrek) toe te laten, zie [Compatibiliteit](/help/data-views/create-dataview.md#compatibility) sectie in [Een gegevensweergave maken of bewerken](/help/data-views/create-dataview.md). <br/><br/>Wanneer u de optie uitschakelt, wordt u in een dialoogvenster gevraagd of u wilt doorgaan met het wijzigen van de standaardgegevensweergave. Wanneer u **[!UICONTROL Continue]** selecteert u een andere gegevensweergave als de standaardgegevensweergave. Selecteren **[!UICONTROL Confirm]** om uw selectie te bevestigen. Selecteren **[!UICONTROL Cancel]** om te annuleren, wijzigt u de standaardgegevensweergave. |

  | Containers | Waarde |
  |---|---|
  | [!UICONTROL Person container name] | `Person` |
  | [!UICONTROL Session container name] | `Session` |
  | [!UICONTROL Event container name] | `Event` |

  | Kalender | Waarde |
  |---|---|
  | [!UICONTROL Time zone] | Tijdzone die voldoet aan uw locatie |
  | [!UICONTROL Calendar type] | Gregoriaans |
  | [!UICONTROL First month of the year] | Januari |
  | [!UICONTROL First day of the week] | zondag |


- In de **Componenten** tab:
   - Alle metriek en dimensies die **[!UICONTROL (AJO)]** toegevoegd aan hun naam worden automatisch toegevoegd als deel van deze automatische configuratie.
   - Sommige metriek of afmetingen die automatisch zijn toegevoegd zijn gebaseerd op afgeleide gebieden. Deze afgeleide gebieden worden specifiek gecreeerd voor deze integratie. De maateenheid voor klikken op bestemmingspagina (AJO) is bijvoorbeeld gebaseerd op het afgeleide veld voor klikken op bestemmingspagina.
   - Sommige metriek of dimensies hebben extra configuratie. Zo zijn er bijvoorbeeld instellingen voor Indeling en Inclusief waarden niet van toepassing op Spam Complaint (AJO).
   - Alle automatisch toegevoegde metriek en afmetingen hebben een contextetiket genoemd **[!UICONTROL :*naam_van_metrisch_of_dimensie *]**. Bijvoorbeeld de[!UICONTROL Landing Page Clicks (AJO)] metrisch heeft het contextetiket [!UICONTROL :Landing page clicks (AJO)].

- In de **[!UICONTROL Settings]** tab, er worden geen specifieke configuratiewaarden toegepast

>[!IMPORTANT]
>
>Het wijzigen van om het even welke automatisch gevormde waarden voor de verbinding en gegevensmening heeft gevolgen voor Journey Optimizer rapporterend die zich op en het gebruiken van de automatisch gevormde integratie van de Customer Journey Analytics baseert.


## Een gegevensweergave handmatig configureren voor gebruik met Journey Optimizer

In de volgende secties wordt beschreven hoe u handmatig gegevens, gegenereerd door Journey Optimizer, kunt gebruiken om geavanceerde analyses in de Customer Journey Analytics uit te voeren. Dit is alleen nodig als de [automatische configuratie, optie](#automatically-configure-a-customer-journey-analytics-data-view-to-be-used-with-adobe-journey-optimizer) is onvoldoende voor uw behoeften.

### Gegevens van Journey Optimizer naar Experience Platform verzenden

Adobe Experience Platform fungeert als de centrale gegevensbron en de verbinding tussen Journey Optimizer en Customer Journey Analytics. Zie [Aan de slag met gegevenssets](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/data-management/datasets/get-started-datasets) in de gebruikersgids van Journey Optimizer voor stappen op hoe te om de gegevens van Journey Optimizer naar Experience Platform als dataset te verzenden.

### Verbinding maken in Customer Journey Analytics

Zodra Journey Optimizer-gegevens in Adobe Experience Platform zijn opgeslagen, kunt u [Verbinding maken](/help/connections/create-connection.md) op basis van uw Journey Optimizer-gegevenssets. U kunt ook Journey Optimizer-gegevenssets toevoegen aan een bestaande verbinding.

Selecteer en vorm de volgende datasets:

| Gegevensset | Het type DataSet | Verbindingsinstellingen | Beschrijving |
| --- | --- | --- | --- |
| Dataset voor AJO-feedbackgebeurtenis | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor berichtlevering, zoals &#39;[!UICONTROL Sends]&#39; en &#39;[!UICONTROL Bounces]&quot;. |
| AJO Email Tracking Experience Event Dataset | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor het bijhouden van e-mail, zoals &#39;[!UICONTROL Opens]&#39;, &#39;[!UICONTROL Clicks]&#39;, en &#39;[!UICONTROL Unsubscribes]&quot;. |
| Dataset voor AJO Push Tracking Experience | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen voor het bijhouden van pushberichten, zoals &#39;[!UICONTROL App Launches]&quot;. |
| Gebeurtenissen reisstap | Gebeurtenis | Persoon-id: `_experience.journeyOrchestration.`<br>`stepEvents.profileID` | Bevat gebeurtenissen die tonen welke profielen aan elk knooppunt van de reis deelnamen. |
| Gegevensset AJO Entiteit | Opzoeken | Sleutel: `_id`<br>Overeenkomende sleutel: `_experience.decisioning.propositions.`<br>`scopeDetails.correlationID` | Bevat classificaties die de meta-gegevens van de Reis en van de Campagne aan alle gebeurtenisgegevens van Journey Optimizer associëren. |

{style="table-layout:auto"}


### De gegevensweergave configureren om de afmetingen en afmetingen van Journey Optimizer aan te passen

Nadat u een verbinding hebt gemaakt, kunt u een of meer [Gegevens weergeven](/help/data-views/create-dataview.md) om de gewenste afmetingen en metriek te vormen beschikbaar in Customer Journey Analytics.

>[!NOTE]
>
>De verschillen tussen gegevens tussen Journey Optimizer en Customer Journey Analytics zijn doorgaans kleiner dan 1-2%. Grotere verschillen zijn mogelijk voor gegevens die in de laatste twee uur zijn verzameld. Gebruik datumbereiken met uitzondering van vandaag om verschillen in verwerkingstijd te verkleinen.


#### Dimensies configureren in de gegevensweergave

In Journey Optimizer kunt u de volgende afmetingen maken om een vergelijkbare pariteit met vergelijkbare afmetingen te bereiken. Zie [Componentinstellingen](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details over afmetingsaanpassingsopties.

| Dimension | Schema-element | Componentinstellingen |
| --- | --- | --- |
| Reisnaam | `_experience.customerJourneyManagement.`<br>`entities.journey.journeyName` | Componenttype: Dimension |
| Naam en versie van reis | `_experience.customerJourneyManagement.`<br>`entities.journey.journeyNameAndVersion` | Componenttype: Dimension |
| Naam van knooppunt | `_experience.customerJourneyManagement.`<br>`entities.journey.journeyNodeName` | Componenttype: Dimension |
| Type knooppunt | `_experience.customerJourneyManagement.`<br>`entities.journey.journeyNodeType` | Componenttype: Dimension |
| Campagneraam | `_experience.customerJourneyManagement.`<br>`entities.campaign.name` | Componenttype: Dimension |
| Kanaal | `_experience.customerJourneyManagement.`<br>`entities.channelDetails.channel._id` | Componenttype: Dimension |
| Titel duwen | `_experience.customerJourneyManagement.`<br>`entities.channelDetails.push.title` | Componenttype: Dimension |
| E-mailonderwerp | `_experience.customerJourneyManagement.`<br>`entities.channelDetails.email.subject` | Componenttype: Dimension |
| Koppelingslabel | `_experience.customerJourneyManagement.`<br>`messageInteraction.label` | Componenttype: Dimension |
| Naam experiment | `_experience.customerJourneyManagement.`<br>`entities.experiment.experimentName` | Componenttype: Dimension<br>Contextlabels: experimenteerprogramma |
| Naam behandeling | `_experience.customerJourneyManagement.`<br>`entities.experiment.treatmentName` | Componenttype: Dimension<br>Contextlabels: experimentele variabele |
| Reden voor mislukte e-maillevering | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.messageFailure.reason` | Componenttype: Dimension |
| Reden voor uitsluiting van e-maillevering | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.messageExclusion.reason` | Componenttype: Dimension |
| Elementlabel | `_experience.decisioning.propositionAction.label` | Componenttype: Dimension |

{style="table-layout:auto"}

#### Metriek configureren in de gegevensweergave

U kunt de volgende metriek in een gegevensmening tot stand brengen om gelijke gelijkheid met gelijkaardige metriek in Journey Optimizer te bereiken. Zie [Componentinstellingen](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond metriek aanpassingsopties.

| Metrisch | Beschrijving | Schema-element | Componentinstellingen |
| --- | --- | --- | --- |
| Bounces | Het aantal berichten dat is teruggedraaid, inclusief zowel directe stuitingen als stuitingen na levering. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch<br>Inclusief waarden voor uitsluiten: als aan een van de criteria wordt voldaan<br>Gelijk aan: `bounce`, is gelijk aan: `denylist` |
| Stortingen na aflevering | Sommige e-mailservices melden de geleverde e-mailberichten en sturen deze later weer op. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.messageFailure.category` | Componenttype: Metrisch<br>Inclusief exclusief waarden: Gelijk `async` |
| E-mailklikken | De telling van kliks binnen berichten. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Inclusief exclusief waarden: Gelijk `click` |
| E-mailopenen | Het aantal geopende berichten. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Inclusief exclusief waarden: Gelijk `open` |
| Fouten | Het aantal berichten dat uittrok. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch<br>Inclusief exclusief waarden: Gelijk `error` |
| Exclusief | Het aantal uitgesloten berichten. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch<br>Inclusief exclusief waarden: Gelijk `exclude` |
| Verzenden | Het aantal berichten dat e-mailproviders hebben geaccepteerd. | `_experience.customerJourneyManagement.`<br>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch<br>Inclusief exclusief waarden: Gelijk `sent` |
| Spam-klachten | Het aantal spamklachten. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Inclusief exclusief waarden: Gelijk `spam_complaint` |
| Abonnementen opzeggen | The count of unsubscribes. | `_experience.customerJourneyManagement.`<br>`messageInteraction.interactionType` | Componenttype: Metrisch<br>Inclusief exclusief waarden: Gelijk `unsubscribe` |
| Edge verzendt | Het aantal tijden het randnetwerk verzendt een bericht naar of het Web of Mobiele SDK | Het element SchemaString gebruiken `_experience.decisioning.propositionEventType.send` | |
| Binnenkomende beeldschermen | Het aantal keer dat een Web- of InApp-bericht aan de gebruiker wordt getoond | Het element SchemaString gebruiken `_experience.decisioning.propositionEventType.display` | |
| Binnenkomende klikken | De telling van Web of InApp bericht klikt | Het element SchemaString gebruiken `_experience.decisioning.propositionEventType.interact` | |
| InApp-triggers | Het aantal keren dat de beslissingsengine het bericht heeft voorgesteld, moet worden weergegeven. De mobiele SDK kan de beslissing negeren, waardoor het aantal daadwerkelijke weergaven afneemt. | Het element SchemaString gebruiken `_experience.decisioning.propositionEventType.trigger` | |
| InApp-ontslagen | Het aantal keren dat een InApp-bericht door de SDK uit de gebruikersinterface wordt verwijderd | Het element SchemaString gebruiken `_experience.decisioning.propositionEventType.dismiss` | |

{style="table-layout:auto"}

#### Berekende waarden configureren in Analysis Workspace

Zodra u de gewenste afmetingen en metriek voor de dataset van Journey Optimizer hebt gevormd, kunt u ook vormen [Berekende cijfers](/help/components/calc-metrics/calc-metr-overview.md) voor meer inzichten over die gegevens. Deze berekende metriek zijn gebaseerd op de bovengenoemde metriek die in de Manager van de Mening van Gegevens wordt gecreeerd.

| Berekende metrische waarde | Beschrijving | Formule |
| --- | --- | --- |
| Berichten verzonden | Het totale aantal verzonden berichten. Bevat gelukte of mislukte berichten. | `[Sends] + [Bounces] - [Bounces After Delivery]` |
| Berichten geleverd | Het aantal e-mails dat aan klanten wordt geleverd. | `[Sends] - [Bounces After Delivery]` |

{style="table-layout:auto"}
