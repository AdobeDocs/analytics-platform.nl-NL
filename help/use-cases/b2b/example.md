---
title: Een B2B-voorbeeldproject
description: Leer hoe te opstelling, vorm en rapport over B2B- gegevens
solution: Customer Journey Analytics
feature: Use Cases
hide: true
hidefromtoc: true
source-git-commit: c4a4dcd0e4c0d7473570c2db3aa3d99e34c2a1cf
workflow-type: tm+mt
source-wordcount: '1559'
ht-degree: 2%

---

# Een B2B-voorbeeldproject

Dit artikel verklaart, door voorbeelden, hoe te opstelling, vorm en rapport over B2B- gegevens in Customer Journey Analytics.

## Verbinding

Bepaal uw verbinding om alle relevante B2B datasets van Experience Platform te omvatten. Dit omvat de belangrijke raadplegingsdatasets die in een typische B2B opstelling binnen Experience Platform worden vereist. Zie [Gegevens op accountniveau toevoegen als een opzoekgegevensset](b2b.md) voor meer informatie .

Gegevensbestanden die u kunt toevoegen aan uw verbinding:

| Gegevensset | Schema | Type schema | Basisklasse | Beschrijving |
|---|---|---|---|---|
| B2B-activiteitengegevens | B2B Activiteitsschema | Gebeurtenis | XDM ExperienceEvent | Een ExperienceEvent is een feitenverslag van wat voorkwam, met inbegrip van het tijdstip en de identiteit van het betrokken individu. ExperienceEvents kunnen expliciete (direct waarneembare menselijke acties) of impliciete (opgewekte zonder directe menselijke actie) zijn en worden geregistreerd zonder aggregatie of interpretatie. Zij zijn kritiek voor tijd-domein analyses aangezien zij voor waarneming en analyse van veranderingen toestaan die in een bepaald venster van tijd en de vergelijking tussen veelvoudige vensters van tijd voorkomen om tendensen te volgen. |
| B2B-persoonsgegevensset | B2B Personenschema | Profiel | Afzonderlijk XDM-profiel | Een XDM Individueel Profiel vormt een enkelvoudige vertegenwoordiging van de attributen en de belangen van zowel geïdentificeerde als gedeeltelijk geïdentificeerde individuen. Minder geïdentificeerde profielen kunnen alleen anonieme gedragssignalen bevatten, zoals browsercookies, terwijl sterk geïdentificeerde profielen gedetailleerde persoonlijke gegevens kunnen bevatten zoals naam, geboortedatum, locatie en e-mailadres. Naarmate een profiel groeit, wordt het een robuuste opslagplaats voor persoonlijke gegevens, identificatiegegevens, contactgegevens en communicatievoorkeuren voor een individu. |
| Gegevensset voor B2B-campagnegelid | B2B Campagne Member Schema | Opzoeken | XDM Business Campaign-leden | XDM Business Campaign-leden zijn een standaard XDM-klasse (Experience Data Model) waarmee een contactpersoon of lead wordt beschreven die aan een zakelijke campagne is gekoppeld. |
| B2B-accountgegevens | B2B-accountschema | Opzoeken | XDM Business Account | XDM Business Account is een standaard XDM-klasse (Experience Data Model) waarmee de minimaal vereiste eigenschappen van een zakelijke account worden vastgelegd. |
| B2B-gegevensset betreffende de relatie van rekeningpersonen | B2B-relatieschema van rekeningpersonen | Opzoeken | XDM Zakelijke account Person Relatie | De Verhouding van de Persoon van de Rekening van XDM van de BedrijfsRekening is een standaardklasse van de Gegevens van de Ervaring (XDM) die de minimum vereiste eigenschappen van een persoon vangt die met een bedrijfsrekening wordt geassocieerd. |
| B2B-opportuniteitsgegevensset | B2B-opportuniteitsschema | Opzoeken | XDM Business Opportunity | XDM Business Opportunity is een standaard XDM-klasse (Experience Data Model) waarmee de minimaal vereiste eigenschappen van een zakelijke opportuniteit worden vastgelegd. |
| B2B Dataset van de Betrekking van de Kans van de Persoon | B2B Opportunity Person Relatie Schema | Opzoeken | XDM Business Opportunity Person Relatie | De Relatie van de Persoon van de Kans van de Onderneming XDM is een standaardKlasse van de Gegevens van de Ervaring Model (XDM) die de minimum vereiste eigenschappen van een persoon vangt die met een bedrijfskans wordt geassocieerd. |
| Gegevensset voor B2B-campagne | B2B-campagnereschema | Opzoeken | XDM Business Campaign | XDM Business Campaign is een standaard XDM-klasse (Experience Data Model) waarmee de minimaal vereiste eigenschappen van een zakelijke campagne worden vastgelegd. |
| Gegevensset voor B2B-marketinglijst | B2B-schema voor marketinglijsten | Opzoeken | XDM Marketing List | XDM Business Marketing List is een standaard XDM-klasse (Experience Data Model) waarmee de minimaal vereiste eigenschappen van een marketinglijst worden vastgelegd. Op de markt brengende lijsten staan u toe om aan potentiële cliënten voorrang te geven die zeer waarschijnlijk uw product zullen kopen. |
| Gegevensset voor B2B-marketinglijsten | B2B-schema Leden op marketinglijst | Opzoeken | Leden van XDM-marketinglijst | De Leden van de Lijst van de Bedrijfs XDM is een standaardGegevensmodel van de Ervaring (XDM) klasse die leden, personen, of contacten verbonden aan een marketing lijst beschrijft. |

De verhouding tussen de raadplegingsschema&#39;s, het profielschema, en gebeurtenisschema wordt bepaald in B2B opstelling binnen Experience Platform. Zie schema&#39;s in [Real-time Customer Data Platform B2B Edition](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/schemas/b2b.html?lang=en) en [Een veel-op-een relatie definiëren tussen twee schema&#39;s in Real-time Customer Data Platform B2B Edition](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-b2b.html?lang=en) voor meer informatie .

![Relatie tussen B2B-schema&#39;s](assets/classes.png)

Voor elke raadplegingsdataset die u aan uw verbinding toevoegt, moet u de verhouding aan een gebeurtenisdataset uitdrukkelijk bepalen gebruikend Sleutel en de Gelijke sleutel in de Edit datasetdialoog. Bijvoorbeeld:

![Sleutel - Overeenkomende sleutel](assets/key-matchingkey.png)


In de onderstaande tabel vindt u een voorbeeld van het [!UICONTROL Person ID], [!UICONTROL Key], en [!UICONTROL Matching key] waarden voor elk van de gegevenssets.


| Gegevensset | Persoon-id | Sleutel | Overeenkomende sleutel (in gegevensset voor gebeurtenissen) |
|---|---|---|---|
| B2B-activiteitengegevens | `personKey.sourceKey` | | |
| B2B-persoonsgegevensset | `b2b.personKey.sourceKey` | | |
| B2B-accountgegevens | | `accountKey.sourceKey` | *_organisationID*`.interactions.accountKey.sourceKey` |
| B2B-opportuniteitsgegevensset | | `accountKey.sourceKey` | *_organisationID*`.interactions.accountKey.sourceKey` |
| Gegevensset voor B2B-campagne | | `campaignKey.sourceKey` | *_organisationID*`.interactions.campaignKey.sourceKey` |
| Gegevensset voor B2B-marketinglijst | | `listKey.sourceKey` | `listOperations.listKey.sourceKey` |

{style="table-layout:auto"}


In de tabel *_organisationID*`.interaction.*`, verwijst naar de aangepaste veldgroep die u aan het B2B-activiteitenschema hebt toegevoegd om de relatie met het B2B-account en het B2B-opportuniteitsschema te definiëren. De `listOperations.listKey.sourceKey` Verwijst naar Add aan de gebiedsgroep van de Lijst die aan het B2B schema van de Activiteit wordt toegevoegd om te volgen wanneer een persoon aan een specifieke lijst wordt toegevoegd.

Zie [Gegevenssets toevoegen en configureren](../../connections/create-connection.md) voor meer informatie over hoe te om montages voor een datset te vormen.


## Gegevensweergaven

Om toegang tot relevante B2B afmetingen en metriek te hebben wanneer het bouwen van uw project van de Werkruimte, moet u uw gegevensmening dienovereenkomstig bepalen.

In deze sectie worden aanbevelingen en suggesties gegeven over de dimensies en metriek die moeten worden meegenomen bij het definiëren van de [componenten](../../data-views/create-dataview.md#components) van uw gegevensweergave.

Voor elke component, worden de naam, het schemapad, en (indien van toepassing) details over de configuratie verstrekt.


### B2B-activiteitengegevensset

Het B2B-activiteitengegevensbestand bevat de relevante ervaringsgebeurtenissen en is vereist als onderdeel van een verbinding.

+++ Details

#### Metrics

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Toevoegen aan campagne | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `leadOperation.addToCampaign` |
| Toevoegen aan opportunity | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `opportunityEvent.addToOpportunity` |
| Toepassing gesloten | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `application.close` |
| Toepassing starten | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `application.launch` |
| Campagnestream | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** ` leadOperation.changeCampaignStream` |
| Afhandeling | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `commerce.checkouts` |
| Regelafstand omzetten | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `leadOperation.convertLead` |
| E-mail geklikt | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `directMarketing.emailClicked` |
| E-mail bezorgd | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `directMarketing.emailDelivered` |
| E-mail geopend | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `directMarketing.emailOpened` |
| E-mail verzonden | String | eventType | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `directMarketing.emailSent` |
| E-mail niet geabonneerd | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `directMarketing.emailUnsubscribed` |
| Formulier ingevuld | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `web.formFilledOut` |
| Formulier gestart | String | `web.fillOutForm.webFormName` | |
| Leads | String | eventType | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `leadOperation.newLead` |
| Opportunity bijgewerkt | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `opportunityEvent.opportunityUpdated` |
| Prijs | Dubbel | *_organisationID*`.interactions.products.price` |  |
| Prioriteit | Geheel | `leadOperation.changeScore.priority` |  |
| Prodelijst toevoegen | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `commerce.productListAdds.value` |
| Prodelijst geopend | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `commerce.productListOpens.value` |
| Prodweergave | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `commerce.productViews.value` |
| Aankopen | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `commerce.purchases.value` |
| Verwijderen uit opportunity | String | `eventType` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `opportunityEvent.removeFromOpportunity` |
| Opslaan voor later | String | eventType | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `commerce.productViews.value` |

{style="table-layout:auto"}


#### Dimensies

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Accountsleutel (bronsleutel) | String | *_organisationID*`.Interactions.accountKey.sourceKey` | |
| Omgezette status | String | `leadOperation.convertLead.convertedStatus` | |
| Type gebeurtenis | String | `eventType` | |
| Formuliernaam | String | `leadOperation.newLead.formName` | |
| Id | String | `_id` | |
| Melding wordt verzonden | Boolean | `leadOperation.convertLead.isSentNotificationEmail` | |
| Trefwoorden | String | `search.keywords` | |
| Lijst-id | String | `listOperations.listID` | |
| Lijstnaam | String | `leadOperation.newLead.listName` | |
| Paginanaam | String | `web.webPageDetails.name` | |
| Persoonssleutel (bronsleutel) | String | `personKey.sourceKey` | |
| Geproduceerd door | String | madeBy | |
| Productnaam | String | *_organisationID*`.Interactions.products.name` | |
| Rol | String | `opportunityEvent.role` | |
| Tijdstempel | Datum/tijd | `timestamp` | Datum-tijdnotatie: **[!UICONTROL Day]** |
| URL | String | `web.webPageDetails.URL` | |
| Webformuliernaam | String | `web.fillOutForm.webFormName` | |
| Product-URL | String | *_organisationID*`.Interactions.products.url` | |

{style="table-layout:auto"}

+++


### B2B Gegevensset personen

Het B2B-persoonlijke gegevensbestand bevat de relevante profielen.

+++ Details


#### Metrics

Geen metrische componenten worden bepaald als deel van deze dataset.


#### Dimensies

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Laatste activiteitendatum | Datum/tijd | `extSourceSystemAudit.lastActivityDate` | Datum-tijdnotatie: **[!UICONTROL Day]** |
| Persoon-id | String | `personID` | |

{style="table-layout:auto"}

+++ Details

### B2B-opportuniteitsgegevensset

De B2B-opportuniteitsdataset bevat de relevante mogelijkheden.

+++ Details

#### Metrics

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Verwachte inkomsten | Dubbel | `expectedRevenue.amount` | Gedraging: **[!UICONTROL Count values]** |
| Aantal kansen | Dubbel | `opportunityAmount.amount` | Gedraging: **[!UICONTROL Count values]** |
| Opportunity Stage - Gesloten boek | String | `opportunityStage` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `Closed - Booked` |
| Opportunity Stage - Perspectief | String | `opportunityStage` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `Prospect` |
| Opportunity Stage - Kwalificatie | String | `opportunityStage` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `Opportunity Qualification` |
| Opportunity Stage - Definitie van oplossing | String | `opportunityStage` | **[!UICONTROL Set include/exclude values]**<br/>**[!UICONTROL Case sensitive]**<br/>Overeenkomst:**[!UICONTROL If all criteria are met]**<br/> Criteria: **[!UICONTROL Equals]** `Solution Definition and Validation` |

{style="table-layout:auto"}


#### Dimensies

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Gesloten vlag | Boolean | `isClosed` | |
| Bedrijfs-id | String | `opportunityID` | |
| Prognose-categorie | String | `forecastCategoryName` | |
| Laatste activiteitendatum | Datum/tijd | `lastActivityDate` | Datum-/tijdnotatie: **[!UICONTROL Day]** |
| Bron lood | String | `leadSource` | |
| Naam opportunity | String | `opportunityName` | |
| Opportunity-status | String | `opportunityStage` | |
| Won-markering | Boolean | `isWon` | |

{style="table-layout:auto"}

+++

### B2B-gegevensset campagne

De B2B dataset van de Campagne bevat campagnegegevens.

+++ Details

#### Metrics

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Campagnekosten | Dubbel | `actualCost.amount` | |

{style="table-layout:auto"}


#### Dimensies

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Campagne-id | String | `campaignID` | |
| Campagnenaam | String | `campaignName` | |
| Begindatum campagne | Datum/tijd | `campaignStartDate` | Datum-/tijdnotatie: **[!UICONTROL Day]** |
| Kanaalnaam | String | `channelName` | |
| Bovenliggende campagne-id | String | `parentCampaignID` | |

{style="table-layout:auto"}

+++


### B2B-rekeninggegevensset

De gegevensset B2B-account bevat de accountgegevens.

+++ Details

#### Metrics

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Jaarlijkse inkomsten | Dubbel | `accountOrganization.annualRevenue.amount` | |
| Aantal werknemers | Geheel | `accountOrganization.numberOfEmployees` | |

{style="table-layout:auto"}


#### Dimensies

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Account-id | String | `accountID` | |
| Accounttype | String | `accountType` | |
| Plaats | String | `accountBillingAddress.city` | |
| Land | String | `accountBillingAddress.country` | |
| Industrie | String | `accountOrganization.industry` | |
| Regio | String | `accountBillingAddress.region` | |
| Bron-id | String | `accountKey.sourceID` | |
| Source Instance ID | String | `accountKey.sourceInstanceID` | |
| Bronsleutel | String | `accountKey.sourceKey` | |
| Brontype | String | `accountKey.sourceType` | |

{style="table-layout:auto"}

+++


### B2B Gegevensset Campagne-lid

De gegevensset van het B2B-campagnerelid bevat de interacties van leden van campagnes.

+++ Details

#### Metrics

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Afgekeerd | Lang | *_organisationID*`.campaignBounced` | Gedraging: **[!UICONTROL Count values]** |
| Geklikt | Lang | *_organisationID*`.campaignClicked` | Gedraging: **[!UICONTROL Count values]** |
| Geopend | Lang | *_organisationID*`.CampaignOpened` | Gedraging: **[!UICONTROL Count values]** |
| Verzonden | Lang | *_organisationID*`.campaignSent` | Gedraging: **[!UICONTROL Count values]** |
| Geabonneerd | Lang | *_organisationID*`.campaignSubscribed` | Gedraging: **[!UICONTROL Count values]** |
| Webinar-registratie | Lang | *_organisationID*`.Registrations` | Gedraging: **[!UICONTROL Count values]** |

{style="table-layout:auto"}

#### Dimensies

| Componentnaam | Schema, gegevenstype | Schemapad | Configuratie |
|---|---|---|---|
| Campagne-id | String | `campaignID` | |
| ID Campagne-lid | String | `campaignMemberID` | |
| Campagne-lidstatus | String | `memberStatus` | |
| Reden voor de status van campagnelid | String | `memberStatusReason` | |
| Aanmaakdatum | Datum/tijd | `extSourceSystemAudit.createdDate` | Datum-/tijdnotatie: **[!UICONTROL Day]** |
| Eerste beantwoorde datum | String | `firstRespondedDate` | Datum-/tijdnotatie: **[!UICONTROL Day]** |
| Heeft succes bereikt | Boolean | `hasReachedSuccess` | |
| Heeft gereageerd | Boolean | `hasResponded` | |
| Laatste status | String | `lastStatus` | |
| Laatst bijgewerkt op | Datum/tijd | `extSourceSystemAudit.lastUpdatedDate` | Datum-/tijdnotatie: **[!UICONTROL Day]** |
| Lidmaatschapsdatum | Datum/tijd | `membershipDate` | Datum-/tijdnotatie: **[!UICONTROL Day]** |
| Nurturigheidskadentie | String | `nurtureCadence` | |
| Naam track | String | `nurtureTrackName` | |
| Persoon-id | String | `personID` | |
| Datum bereikt | Datum/tijd | `reachedSuccessDate` | Datum-/tijdnotatie: **[!UICONTROL Day]** |
| Webinar Registration ID | String | `webinarRegistrationID` | |
| URL voor webregistratie | String | `webinarConfirmationUrl` | |
| isExhausted | Boolean | isExhausted | |

{style="table-layout:auto"}

+++

<!--
### B2B Marketing List Member dataset

The B2B Marketing List Member dataset contains member of marketing lists.

-->

## Werkruimte

Met uw behoorlijk bepaalde componenten, kunt u specifieke B2B visualisaties in uw project van de Werkruimte nu bouwen.

Hieronder ziet u een voorbeeld van een Workspace-project dat is gebaseerd op de hierboven beschreven verbinding en gegevensweergave. Zie de beschrijvingen voor elke visualisatie voor meer informatie.

+++ Details

![Visualisaties](assets/visualizations.png)

+++

