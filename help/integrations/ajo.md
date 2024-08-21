---
title: Adobe Journey Optimizer integreren met Customer Journey Analytics
description: Breng gegevens die door Adobe Journey Optimizer zijn gegenereerd, in Customer Journey Analytics en analyseer deze met Analysis Workspace.
exl-id: 9333ada2-b4d6-419e-9ee1-5c96f06a3bfd
feature: Experience Platform Integration
role: Admin
source-git-commit: 5434b8432608ba5ee49f7062070fa1624af1b46a
workflow-type: tm+mt
source-wordcount: '2868'
ht-degree: 0%

---

# Journey Optimizer integreren met Customer Journey Analytics

[ Adobe Journey Optimizer ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) helpt u verbonden, contextafhankelijke, en gepersonaliseerde ervaringen leveren. Het helpt uw klanten aan de volgende stap in hun klantenreis blootstellen.

U kunt gegevens vormen die door Journey Optimizer worden geproduceerd om geavanceerde analyse in Customer Journey Analytics uit te voeren. U kunt deze integratie automatisch configureren. Indien nodig, kunt u extra, handaanpassingen aan de datasets, afmetingen, of metriek maken die in uw verbinding of gegevensmeningen beschikbaar zijn.

## Journey Optimizer-integratie automatisch configureren

{{release-limited-testing-section}}

Journey Optimizer biedt ondersteuning voor het gebruik van Customer Journey Analytics als rapportageengine. Zie [ begonnen worden met de nieuwe Rapporterende interface ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja) in de documentatie van Journey Optimizer.

Wanneer u Customer Journey Analytics die voor Journey Optimizer rapporteert hebt toegelaten, automatisch wordt de a [ verbinding ](/help/connections/overview.md) en [ gegevensmening ](/help/data-views/data-views.md) gecreeerd voor de specifieke zandbak.

### Verbinding

De verbinding heeft de naam **[!UICONTROL AJO Enabled Connection (*zandbaknaam *)]**en heeft het volgende uit de dooswaarden voor configuratie en datasets:

| **montages van de Verbinding** | Waarde |
|---|---| 
| [!UICONTROL Connection name] | `AJO Enabled Connection (`_`sandbox name`_`)` |
| [!UICONTROL Connection description] | [!UICONTROL *beschrijf hier uw verbinding*] |
| [!UICONTROL Tags] | [!UICONTROL *Uitgezochte markeringen*] |


| **montages van Gegevens** | Waarde |
|---|---| 
| [!UICONTROL Enable rolling data window] | Enabled. [!UICONTROL Selected number of months] `13` . |
| [!UICONTROL Sandbox] | [!UICONTROL *naam van zandbak*] (gehandicapt; u kunt dit het plaatsen niet wijzigen). |
| [!UICONTROL Average number of daily events] | minder dan 1 miljoen (uitgeschakeld; u kunt deze instelling niet wijzigen). |


| Naam gegevensset | Schema | Het type DataSet | Type gegevensbron | Persoon-id | Sleutel | Overeenkomende sleutel | Nieuwe gegevens importeren | Backfill-gegevens |
|---|---|---|---|---|---|---|---|---|
| [!UICONTROL AJO Entity Dataset] | [!UICONTROL AJO Entity Record Schema] | [!UICONTROL Lookup] | [!UICONTROL Other] | - | ` _id` | `_experience. decisioning. propositions. scopeDetails. correlationID` | ![ Groene Status ](assets/../../connections/assets/status-green.svg) op | ![ Grijs van de Status ](assets/../../connections/assets/status-gray.svg) weg |
| [!UICONTROL Journey Step Events] | [!UICONTROL Journey Step Event schema for Journey Orchestration] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL  IdentityMap(\<primary\>)] | - | - | ![ Groene Status ](assets/../../connections/assets/status-green.svg) op | ![ Grijs van de Status ](assets/../../connections/assets/status-gray.svg) weg |
| [!UICONTROL AJO Email Tracking Experience Event Dataset] | [!UICONTROL AJO Email Tracking Experience Event Schema] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL IdentityMap(\<primary\>)] | - | - | ![ Groene Status ](assets/../../connections/assets/status-green.svg) op | ![ Grijs van de Status ](assets/../../connections/assets/status-gray.svg) weg |
| [!UICONTROL AJO Message Feedback Event Dataset] | [!UICONTROL AJO Message Feedback Event Schema] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL IdentityMap(\<primary\>)] | - | - | ![ Groene Status ](assets/../../connections/assets/status-green.svg) op | ![ Grijs van de Status ](assets/../../connections/assets/status-gray.svg) weg |
| [!UICONTROL AJO Push Tracking Experience Event Dataset] | [!UICONTROL AJO Push Tracking Experience Event Schema] | [!UICONTROL Event] | [!UICONTROL Other] | [!UICONTROL IdentityMap(\<primary\>)] | - | - | ![ Groene Status ](assets/../../connections/assets/status-green.svg) op | ![ Grijs van de Status ](assets/../../connections/assets/status-gray.svg) weg |


### Gegevens, weergave

De gegevensmening heeft de naam **AJO laat de Mening van Gegevens toe (*zandbaknaam*)**.

- Op het tabblad **[!UICONTROL Configure]** worden de volgende waarden uit het vak geconfigureerd.

  | Instellingen | Waarde |
  |---|---|
  | [!UICONTROL Connection] | AJO Toegelaten Verbinding (*zandbaknaam*) |
  | [!UICONTROL Name] | `AJO Enabled Data View (`_`sandbox name`_`)` |
  | [!UICONTROL External ID] | `AJO_Enabled_Data_View__`_`sandbox_name`_`_` (afgeleid van de naam) |
  | [!UICONTROL Description] | `undefined` |

  {style="table-layout:fixed"}

  | Compatibiliteit | Waarde |
  |---|---|
  | [!UICONTROL Set as the default data view in Adobe Journey Optimizer] | Ingeschakeld (standaard).<br/><br/> Deze configuratieoptie staat u toe om een gegevensmening aan gebruik met Journey Optimizer, zonder de behoefte aan handconfiguratie aan te wijzen. Voor informatie hoe te om deze configuratieoptie (als niet reeds toegelaten door gebrek) toe te laten, zie de [ sectie van de Verenigbaarheid ](/help/data-views/create-dataview.md#compatibility) in [ creeer of geef een gegevensmening ](/help/data-views/create-dataview.md) uit. <br/><br/> wanneer u de optie onbruikbaar maakt, zet een dialoog u ertoe aan of u wilt blijven veranderend de standaardgegevensmening. Wanneer u **[!UICONTROL Continue]** selecteert, moet u een andere gegevensweergave selecteren als de standaardgegevensweergave. Selecteer **[!UICONTROL Confirm]** om uw selectie te bevestigen. Selecteer **[!UICONTROL Cancel]** om te annuleren en de standaardgegevensweergave te wijzigen. |

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


- In het **lusje van Componenten**:
   - Alle metriek en afmetingen waaraan [!UICONTROL (AJO)] is toegevoegd, worden automatisch toegevoegd als onderdeel van deze automatische configuratie.
   - Sommige metriek of afmetingen die automatisch zijn toegevoegd zijn gebaseerd op afgeleide gebieden. Deze afgeleide gebieden worden specifiek gecreeerd voor deze integratie. De metrische waarde [!UICONTROL Landing Page Clicks (AJO)] is bijvoorbeeld gebaseerd op het afgeleide veld [!UICONTROL Landing Page Clicks] .
   - Sommige metriek of dimensies hebben extra configuratie. [!UICONTROL Spam Complaint (AJO)] heeft bijvoorbeeld [!UICONTROL Format] - en [!UICONTROL Include Exclude Values] -instellingen toegepast.
   - Alle automatisch toegevoegde metriek en afmetingen hebben een contextlabel met de naam `:`*`name_of_metric_or_dimension`*. De metrische waarde [!UICONTROL Landing Page Clicks (AJO)] heeft bijvoorbeeld het contextlabel `:Landing page clicks (AJO)` .

- Op het tabblad **[!UICONTROL Settings]** worden geen specifieke configuratiewaarden toegepast

>[!IMPORTANT]
>
>Het wijzigen van om het even welke automatisch gevormde waarden voor de verbinding en gegevensmening heeft gevolgen voor Journey Optimizer rapporterend die zich op en het gebruiken van de automatisch gevormde integratie van de Customer Journey Analytics baseert.


## Een gegevensweergave handmatig configureren voor gebruik met Journey Optimizer

In de volgende secties wordt beschreven hoe u handmatig gegevens, gegenereerd door Journey Optimizer, kunt gebruiken om geavanceerde analyses in de Customer Journey Analytics uit te voeren. Deze handconfiguratie is noodzakelijk slechts als de [ automatische configuratieoptie ](#automatically-configure-a-customer-journey-analytics-data-view-to-be-used-with-adobe-journey-optimizer) voor uw behoeften ontoereikend is.

### Gegevens van Journey Optimizer naar Experience Platform verzenden

Adobe Experience Platform fungeert als de centrale gegevensbron en de verbinding tussen Journey Optimizer en Customer Journey Analytics. Zie [ begonnen worden met Datasets ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/data-management/datasets/get-started-datasets) in de gebruikersgids van Journey Optimizer voor stappen op hoe te om de gegevens van Journey Optimizer naar Experience Platform als dataset te verzenden.

### Verbinding maken

Zodra het gegeven van Journey Optimizer in Adobe Experience Platform is, kunt u [ een verbinding ](/help/connections/create-connection.md) creëren die op uw datasets van Journey Optimizer wordt gebaseerd. U kunt ook Journey Optimizer-gegevenssets toevoegen aan een bestaande verbinding.

Selecteer en vorm de volgende datasets:

| Gegevensset | Het type DataSet | Verbindingsinstellingen | Beschrijving |
| --- | --- | --- | --- |
| Dataset voor AJO-feedbackgebeurtenis | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat gebeurtenissen van de berichtlevering, zoals &quot;[!UICONTROL Sends]&quot;en &quot;[!UICONTROL Bounces]&quot;. |
| AJO Email Tracking Experience Event Dataset | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat e-mail volgende gebeurtenissen zoals &quot;[!UICONTROL Opens]&quot;, &quot;[!UICONTROL Clicks]&quot;, en &quot;[!UICONTROL Unsubscribes]&quot;. |
| Dataset voor AJO Push Tracking Experience | Gebeurtenis | Persoon-id: `IdentityMap` | Bevat push het volgen gebeurtenissen zoals &quot;[!UICONTROL App Launches]&quot;. |
| Gebeurtenissen reisstap | Gebeurtenis | Persoon-id: `_experience.journeyOrchestration.`<br>`stepEvents.profileID` | Bevat gebeurtenissen die tonen welke profielen aan elk knooppunt van de reis deelnamen. |
| Gegevensset AJO Entiteit | Opzoeken | Sleutel: `_id`<br> Vergelijkende Sleutel: `_experience.decisioning.propositions.`<br>`scopeDetails.correlationID` | Bevat classificaties die de meta-gegevens van de Reis en van de Campagne aan alle gebeurtenisgegevens van Journey Optimizer associëren. |

{style="table-layout:auto"}


### De weergave Gegevens configureren

Nadat een verbinding wordt gecreeerd, kunt u één of meerdere [ Meningen van Gegevens ](/help/data-views/create-dataview.md) tot stand brengen om de gewenste dimensies en metriek te vormen beschikbaar in Customer Journey Analytics.

>[!NOTE]
>
>De verschillen tussen gegevens tussen Journey Optimizer en Customer Journey Analytics zijn doorgaans kleiner dan 1-2%. Grotere verschillen zijn mogelijk voor gegevens die in de laatste twee uur zijn verzameld. Gebruik datumbereiken met uitzondering van vandaag om verschillen in verwerkingstijd te verkleinen.


#### Dimensies configureren

In Journey Optimizer kunt u de volgende afmetingen maken om een vergelijkbare pariteit met vergelijkbare afmetingen te bereiken. Zie [ montages van de Component ](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details op de opties van de afmetingsaanpassing.

| Dimension | Beschrijving | Gegevensset(s) | Schema-element | Componentinstellingen |
| --- | --- | --- | --- | --- |
| Fout bij uitvoeren van handeling (AJO) | De voorwaarde van de fout die Journey Runtime verhinderde actie uit te voeren. | Gebeurtenissen reisstap | `_experience.journeyOrchestration.`<br/>`stepEvents.actionExecutionError ` | Componenttype: Dimension |
| Handelinglabel (AJO) | De klant genereerde weergavenaam van het element waarmee de eindgebruiker interactie had. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.`<br/>`propositionAction.label` | Componenttype: Dimension |
| Batch-id (AJO) | GUID die bij aanroeping van elke nieuwe partijinstantie voor een geplande Actie van de Reis of van de Campagne wordt gecreeerd. Bijvoorbeeld, als een geplande Actie van de Reis of van de Campagne bij 8.00am en 10.00am loopt, zijn er twee verschillende batchInstanceID?s. | AJO Push Tracking Experience Event Dataset, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | ` _experience.customerJourneyManagement.`<br/>`messageExecution.batchInstanceID` | Componenttype: Dimension |
| Tijdstempel batchinstantie (AJO) | Het tijdstempel van de batchinstantie. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Dimension (Afgeleid veld) |
| Campagne-id (AJO) | De id van de campagne. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.entities.`<br/>`campaign.campaignID` | Componenttype: Dimension |
| Campagnenaam (AJO) | De naam van de campagne. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.entities.`<br/>`campaign.name` | Componenttype: Dimension |
| Campagne-versie-id (AJO) | De versie-id van de campagne. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.`<br/>`entities.campaign.campaignVersionID` | Componenttype: Dimension |
| Kanaal (AJO) | Het kanaal waarnaar deze gegevens moeten worden gecorreleerd. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.`<br/>`entities.channelDetails.channel._id` | Componenttype: Dimension |
| Correlatie-id (AJO) | De correlatie-id. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.propositions.`<br/>`scopeDetails.correlationID` | Componenttype: Dimension |
| Beslissingsbeleid-ID (AJO) | De id van het besluitvormingsbeleid dat wordt gebruikt bij de beslissing welke punten in dit voorstel moeten worden opgenomen. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Dimension (Afgeleid veld) |
| E-mailontvangerdomein (AJO) | Domein van e-mailadres | AJO Push Tracking Experience Event Dataset, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`emailChannelContext.address` | Componenttype: Dimension |
| E-mailonderwerp (AJO) | E-mailonderwerp, niet-gepersonaliseerd | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.entities.`<br/>`channelDetails.email.subject` | Componenttype: Dimension |
| Gebeurtenis-id (AJO) | Een unieke id voor de gebeurtenis in de tijdreeks. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_id` | Componenttype: Dimension (Afgeleid veld) |
| Id van afsluitcriteria (AJO) | De id van de uitreiscriteria die worden gebruikt om te bepalen of de reis moet worden verlaten. | Gebeurtenissen reisstap | `_experience.journeyOrchestration.`<br/>`stepEvents.exitCriteriaID` | Componenttype: Dimension |
| Naam van afsluitcriteria (AJO) | Naam van uitstapcriteria. | Gebeurtenissen reisstap | `_experience.journeyOrchestration.`<br/>`stepEvents.exitCriteriaName` | Componenttype: Dimension |
| Experiment-id (AJO) | De id van het experiment. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.`<br/>`entities.experiment.experimentId` | Componenttype: Dimension |
| Naam experiment (AJO) | De naam van het experiment. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.entities.`<br/>`experiment.experimentName` | Componenttype: Dimension-contextlabels: Experimentatieditatie |
| Ophaalfout (AJO) | De voorwaarde van de fout die Journey Runtime verhinderde haal uit te voeren. | Gebeurtenissen reisstap | `_experience.journeyOrchestration.`<br/>`stepEvents.fetchError` | Componenttype: Dimension |
| Is Send-Time geoptimaliseerd (AJO) | Is berichtuitvoering SendTimeOptimized | AJO Push Tracking Experience Event Dataset, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageProfile.isSendTimeOptimized` | Componenttype: Dimension |
| Is testreis (AJO) | Is het gebeurtenisdeel van een testreis uitvoering | Gebeurtenissen reisstap | `_experience.journeyOrchestration.`<br/>`stepEvents.inTest` | Componenttype: Dimension |
| Is testbericht (AJO) | Is bericht verzonden als testuitvoering | AJO Push Tracking Experience Event Dataset, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageProfile.isTestExecution` | Componenttype: Dimension |
| Objectnummer (AJO) | De id van het item. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.`<br/>`propositions.items.id` | Componenttype: Dimension |
| Itemnaam (AJO) | De naam van het item | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.`<br/>`propositions.items.name` | Componenttype: Dimension |
| Reisactie-id | Reisactie-id, waarvoor MessageExecution wordt geactiveerd. | AJO Push Tracking Experience Event Dataset, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageExecution.journeyActionID` | Componenttype: Dimension |
| Naam van handelingknooppunt (AJO) | De naam van het actieknooppunt van de reis. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset, AJO Entity Dataset | Afgeleide velden | Componenttype: Dimension (Afgeleid veld) |
| Naam van knooppunt voor reisgebeurtenis (AJO) | Deze waarde wordt ingesteld wanneer een segment of externe gebeurtenis zich voordoet in een transport. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset, AJO Entity Dataset | Afgeleide velden | Componenttype: Dimension (Afgeleid veld) |
| Reis-id (AJO) | De id van de reis. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.`<br/>`entities.journey.journeyID` | Componenttype: Dimension |
| Naam reis (AJO) | De naam van de reis. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.`<br/>`entities.journey.journeyName` | Componenttype: Dimension |
| Naam en versie van reis (AJO) | De naam en versie van de reis. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.`<br/>`entities.journey.journeyNameAndVersion` | Componenttype: Dimension |
| Reisversie-id (AJO) | De versie-id van de reis. | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.entities.`<br/>`journey.journeyVersionID` | Componenttype: Dimension |
| Openingspagina-id (AJO) | Unieke id voor landingspagina. | AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageInteraction.landingpage.landingPageID` | Componenttype: Dimension |
| Openingspagina Source (AJO) | De bron van de bestemmingspagina. | AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Dimension (Afgeleid veld) |
| Koppelings-URL (AJO) | De URL waarop de gebruiker heeft geklikt. | AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageInteraction.urlID` | Componenttype: Dimension |

{style="table-layout:auto"}

#### Metrische gegevens configureren

U kunt de volgende metriek in een gegevensmening tot stand brengen om gelijke gelijkheid met gelijkaardige metriek in Journey Optimizer te bereiken. Zie [ montages van de Component ](/help/data-views/component-settings/overview.md) in de Manager van de Mening van Gegevens voor details rond metrieke aanpassingsopties.

| Metrisch | Beschrijving | Gegevensset(s) | Schema-element | Componentinstellingen |
| --- | --- | --- | --- | --- |
| App-installaties (AJO) | Aantal toepassingsinstallaties | Dataset voor AJO Push Tracking Experience | `application.installs.value` | Componenttype: Metrisch |
| App Launches (AJO) | Aantal keer dat mobiele app wordt gestart | Dataset voor AJO Push Tracking Experience | `application.launches.value` | Componenttype: Metrisch |
| Stemmen voor uitgaande kanalen (AJO) | Totaal aantal berichten die over uitgaande kanalen worden teruggestuurd | Dataset voor AJO-feedbackgebeurtenis | `_experience.customerJourneyManagement.`<br/>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch |
| Klikken (AJO) | Het totale aantal kliks op alle kanalen | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Email Tracking Experience Event Dataset, AJO Message Feedback Event Dataset | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| Aantal terugvalaanbiedingen (AJO) | Aantal fallback-voorstellen. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.propositions.items.`<br/>`itemSelection.selectionDetail.selectionType` | Componenttype: Metrisch |
| Aantal voorstellen (AJO) | Aantal voorstellen. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | ` _experience.decisioning.`<br/>`propositions.items.id` | Componenttype: Metrisch |
| Metrisch opmaken (AJO) | Dedup, metrisch | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_id` | Componenttype: Metrisch |
| Geleverd (AJO) | Totaal aantal geleverde berichten. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| Afgewezen (AJO) | Telt telkens wanneer het inApp-bericht wordt gesloten door de Adobe-SDK, ongeacht welke actie de eindgebruiker kiest om het te sluiten. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.`<br/>`propositionEventType.dismiss` | Componenttype: Metrisch |
| Weergaven (AJO) | Dit aantal geeft AJO-berichten weer. Dit omvat e-mail die wordt geopend, Webvertoningen, en inapp vertoningen. Mobiele platforms rapporteren geen SMS- en pushberichtweergaven en worden daarom niet geteld. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Email Tracking Experience Event Dataset, AJO Message Feedback Event Dataset | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| E-mail wordt geopend (AJO) | Totaal aantal e-mailberichten wordt geopend | AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageInteraction.interactionType` | Componenttype: Metrisch |
| Binnenkomende klikken (AJO) | Totaal aantal klikken over binnenkomende kanalen | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.`<br/>`propositionEventType.interact` | Componenttype: Metrisch |
| Binnenkomende afwijzingen (AJO) | Totaal aantal ontslagen over binnenkomende kanalen | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.`<br/>`propositionEventType.dismiss` | Componenttype: Metrisch |
| Binnenkomende indrukkingen (AJO) | Totaal aantal indrukkingen over binnenkomende kanalen | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.`<br/>`propositionEventType.display` | Componenttype: Metrisch |
| Reiseinde (AJO) | True als de huidige stap tot een einde van een reisexemplaar heeft geleid. Dat de laatste stap in een reis voor een bepaald profiel met succes werd uitgevoerd. | Gebeurtenissen reisstap | `_experience.journeyOrchestration.`<br/>`stepEvents.instanceEnded` | Componenttype: Metrisch |
| Reis Enters (AJO) | True if the step event was a trip entry event for a profile. | Gebeurtenissen reisstap | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| Reisuitgangen (AJO) | True als de huidige stap tot een einde van een reisexemplaar heeft geleid. Dat is de laatste stap in een reis voor een bepaald profiel met succes werd uitgevoerd. | Gebeurtenissen reisstap | `_experience.journeyOrchestration.`<br/>`stepEvents.instanceEnded` | Componenttype: Metrisch |
| Transparantie-storingen (AJO) | Geeft de huidige status van de stap die is uitgevoerd. Mogelijke waarden: `Transitions` (Volgende stap vindt plaats bij een gebeurtenisovergang), `EndStep` (De laatste stap in deze reisinstantie is uitgevoerd), `Error` (Deze stap heeft een fout aangetroffen en de huidige reisinstantie beëindigd), `TimedOut` (De huidige stap is beëindigd vanwege een time-out bij een opname of bij een handeling). | Gebeurtenissen reisstap | `_experience.journeyOrchestration.`<br/>`stepEvents.stepStatus` | Componenttype: Metrisch |
| Openingspagina klikt (AJO) | Het totale aantal klikken op de landingspagina. | AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| Landing Page Conversions (AJO) | Totaal aantal conversies op bestemmingspagina. | AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageInteraction.interactionType` | Componenttype: Metrisch |
| Weergaven van bestemmingspagina (AJO) | Het totale aantal weergaven op de landingspagina. | AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageInteraction.interactionType` | Componenttype: Metrisch |
| Node Enters (AJO) | True if the step event was a node entrance event for a profile. | Gebeurtenissen reisstap | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| Uitgaande klikken (AJO) | Totaal aantal klikken over uitgaande kanalen | AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageInteraction.interactionType` | Componenttype: Metrisch |
| Uitgaande fouten (AJO) | Totaal aantal berichten die fouten over uitgaande kanalen hebben | Dataset voor AJO-feedbackgebeurtenis | `_experience.customerJourneyManagement.`<br/>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch |
| Uitgaande uitsluitingen (AJO) | Totaal aantal uitsluitingsgebeurtenissen over uitgaande kanalen | Dataset voor AJO-feedbackgebeurtenis | `_experience.customerJourneyManagement.`<br/>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch |
| Uitgaande verzendingen (AJO) | Totaal aantal berichten verzenden over uitgaande kanalen | Dataset voor AJO-feedbackgebeurtenis | `_experience.customerJourneyManagement.`<br/>`messageDeliveryfeedback.feedbackStatus` | Componenttype: Metrisch |
| Aangepaste acties duwen (AJO) | Het totale aantal aangepaste handelingen in pushinteractie. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `eventType` | Componenttype: Metrisch |
| Pushinteracties (AJO) | Aantal keren dat mobiele app wordt gestart vanwege een directe interactie met pushberichten | Dataset voor AJO Push Tracking Experience | `application.launches.value` | Componenttype: Metrisch |
| Verzenden (AJO) | Het totale aantal berichten dat over alle kanalen wordt verzonden | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| SMS Inbound Messages (AJO) | Binnenkomend antwoord van SMS. Bijvoorbeeld stoppen, starten, abonneren, enz. | AJO Push Tracking Experience Event Dataset, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`smsChannelContext.inboundMessage` | Componenttype: Metrisch |
| Spam Complaint (AJO) | Totaal aantal klachten over spam | AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageInteraction.interactionType` | Componenttype: Metrisch |
| Abonnementenlijst toegevoegd (AJO) | Totaal aantal toevoegingen aan abonnementenlijst. | AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| Abonnementenlijst wordt verwijderd (AJO) | Het totale aantal verwijderingen uit de abonnementenlijst. | AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| Gericht (AJO) | Dit aantal van het aantal keren dat een voorstel gericht was op een persoon. Dit is het aantal tijden een voorstel voor vertoning aan een persoon werd overwogen. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | Afgeleide velden | Componenttype: Metrisch (Afgeleid veld) |
| Teweeggebracht (AJO) | Het voorstel is gekozen om door de Adobe SDK te worden weergegeven. Andere factoren kunnen voorkomen dat het daadwerkelijk wordt weergegeven. | AJO Push Tracking Experience Event Dataset, Journey Step Events, AJO Message Feedback Event Dataset, AJO Email Tracking Experience Event Dataset | `_experience.decisioning.`<br/>`propositionEventType.trigger` | Componenttype: Metrisch |
| Unieke bezoekers in de experimenten (AJO) | De unieke bezoekers in het experiment | Gegevensset AJO Entiteit | `_experience.customerJourneyManagement.`<br/>`entities.experiment.experimentId` | Componenttype: Metrisch |
| Abonnement opzeggen (AJO) | Totaal aantal afgeschreven bedragen | AJO Email Tracking Experience Event Dataset | `_experience.customerJourneyManagement.`<br/>`messageInteraction.interactionType` | Componenttype: Metrisch |

{style="table-layout:auto"}
