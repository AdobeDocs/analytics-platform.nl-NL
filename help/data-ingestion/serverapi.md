---
title: Gegevens verzamelen via de Adobe Experience Platform Edge Network Server-API
description: Verklaar hoe te om gegevens in Customer Journey Analytics via de Server API van de Edge Network van Adobe Experience Platform en de Edge Network in te voeren
solution: Customer Journey Analytics
feature: Basics
exl-id: 6bfb7254-5bb7-45c6-86a2-0651a0d222fa
role: Admin
source-git-commit: 90d1c51c11f0ab4d7d61b8e115efa8257a985446
workflow-type: tm+mt
source-wordcount: '2176'
ht-degree: 0%

---

# Gegevens verzamelen via de Edge Network Server-API

Deze snelstartgids legt uit hoe u de volgende gegevens van apparaten zoals IoT-apparaten, set-top boxes, gameconsoles, bureaubladtoepassingen rechtstreeks in Adobe Experience Platform kunt invoeren met behulp van de Adobe Experience Platform Edge Network Server API en Edge Network. Gebruik die gegevens vervolgens in Customer Journey Analytics.

Hiervoor moet u:

- **opstelling een schema en dataset** in Adobe Experience Platform om het model (schema) van de gegevens te bepalen die u wilt verzamelen en waar te om de gegevens (dataset) eigenlijk te verzamelen.

- **opstelling een datastream** om de Edge Network van Adobe Experience Platform te vormen om uw verzamelde gegevens aan de dataset te leiden u in Adobe Experience Platform vormde.

- **Server API van het Gebruik** om gegevens van uw toepassing of spel direct te verzenden die op een Desktop, gokkenconsole, apparaat IoT, of reeks-hoogste doos aan uw gegevensstroom lopen.

- **stelt en bevestigt** op. Zorg voor een omgeving waarin u uw ontwikkeling kunt doorlopen en publiceer deze live op uw productieomgeving als alles is gevalideerd.

- **opstelling een verbinding** in Customer Journey Analytics. Deze verbinding zou (minstens) uw dataset van Adobe Experience Platform moeten omvatten.

- **opstelling een gegevensmening** in Customer Journey Analytics om metriek en afmeting te bepalen die u in Analysis Workspace wilt gebruiken.

- **opstelling een project** in Customer Journey Analytics om uw rapporten en visualisaties te bouwen.

>[!NOTE]
>
>Deze handleiding voor snel starten is een vereenvoudigde gids voor het opnemen van gegevens die zijn verzameld bij een toepassing of game die op een IoT-apparaat, set-top box, gameconsole of desktop in Adobe Experience Platform wordt uitgevoerd en in Customer Journey Analytics wordt gebruikt. Het wordt ten zeerste aanbevolen de aanvullende informatie te bestuderen wanneer deze wordt vermeld.


## Een schema en gegevensset instellen

Als u gegevens in Adobe Experience Platform wilt invoeren, moet u eerst definiëren welke gegevens u wilt verzamelen. Alle gegevens die in Adobe Experience Platform worden ingevoerd, moeten voldoen aan een standaard, gedenormaliseerde structuur, zodat deze kan worden herkend en kan worden toegepast door de mogelijkheden en functies op de downstreammarkt. Het Model van Gegevens van de ervaring (XDM) is het standaardkader dat een structuur in de vorm van schema&#39;s verstrekt.

Zodra u een schema hebt bepaald, gebruikt u één of meerdere datasets om de inzameling van gegevens op te slaan en te beheren. Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens (typisch een lijst) die een schema (kolommen) en gebieden (rijen) bevat.

Alle gegevens die in Adobe Experience Platform worden opgenomen moeten met een vooraf gedefinieerd schema in overeenstemming zijn alvorens het als dataset kan worden voortgeduurd.

### Een schema instellen

U wilt enkele minimale gegevens bijhouden van profielen die uw game op een console afspelen, zoals identificatie, scores, voortgang en andere informatie.
U moet eerst een schema definiëren dat deze gegevens modelleert.

Uw schema instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Schemas]** within [!UICONTROL DATA MANAGEMENT] in het linkerspoor.

1. Selecteer **[!UICONTROL Create schema]** .
.
1. In Uitgezocht een klassenstap van de Create schematovenaar:

   1. Selecteer **[!UICONTROL Experience Event]** .

      ![ creeer een schema ](./assets/create-ee-schema-wizard-step-1.png)

      >[!INFO]
      >
      >    Een schema van de Gebeurtenis van de Ervaring wordt gebruikt om het _gedrag_ van een profiel (als scènenaam, drukknop te modelleren om aan wagentje toe te voegen). Een individueel schema van het Profiel wordt gebruikt om de profiel _attributen_ (zoals naam, e-mail, geslacht) te modelleren.

   1. Selecteer **[!UICONTROL Next]** .


1. In het gedeelte [!UICONTROL Name and review step] van de wizard [!UICONTROL Create schema] :

   1. Voer een **[!UICONTROL Schema display name]** in voor uw schema en (optioneel) een **[!UICONTROL Description]** .

      ![ Naam uw schema ](./assets/create-ee-schema-wizard-step-2.png)

   1. Selecteer **[!UICONTROL Finish]** .

1. Op het tabblad Structuur van het voorbeeldschema:

   1. Selecteer **[!UICONTROL + Add]** in [!UICONTROL Field groups] .

      ![ voeg gebiedsgroep ](./assets/add-field-group-button.png) toe

      Veldgroepen zijn herbruikbare verzamelingen van objecten en kenmerken waarmee u het schema eenvoudig kunt uitbreiden.

   1. Selecteer in het dialoogvenster [!UICONTROL Add fields groups] de veldgroep **[!UICONTROL Blinding Light]** in de lijst. Deze veldgroep wordt gemaakt om de voortgang van de gebruiker bij te houden bij het afspelen van een fictieve game met de naam Blinding Light op een console.

      ![ Blinding Light veldgroup ](assets/schema-fieldgroup-blindinglight.png)

      U kunt de voorvertoningsknop selecteren om een voorvertoning weer te geven van de velden die deel uitmaken van deze veldgroep, bijvoorbeeld `scores > afterMatch` .

      ![ Blinding Lichte gebiedsgroepvoorproef ](assets/schema-fieldgroup-blindinglight-preview.png)

      Selecteer **[!UICONTROL Back]** om de voorvertoning te sluiten.

   1. Selecteer **[!UICONTROL Add field groups]** .

1. Selecteer **[!UICONTROL +]** naast de naam van het schema.

   ![ het Schema van het Voorbeeld voegt de knoop van het Gebied toe ](./assets/example-gamingschema-plus.png)

1. Typ in het deelvenster [!UICONTROL Field Properties] `identification` als de [!UICONTROL Field name] , **[!UICONTROL Identification]** als de [!UICONTROL Display name] , selecteer **[!UICONTROL Object]** als de [!UICONTROL Type] en selecteer **[!UICONTROL ExperienceEvent Core v2.1]** als de [!UICONTROL Field Group] .

   >[!NOTE]
   >
   >Als die veldgroep niet beschikbaar is, zoekt u naar een andere veldgroep met identiteitsvelden. Of [ creeer een nieuwe gebiedsgroep ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/field-groups.html) en [ voeg nieuwe identiteitsgebieden ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/fields/identity.html#define-a-identity-field) (als `ecid`, `crmId`, en anderen toe u) aan de gebiedsgroep nodig hebt en selecteer die nieuwe gebiedsgroep.

   ![ Voorwerp van de Identificatie ](./assets/identification-field-gaming.png)

   Het identificatieobject voegt id-mogelijkheden toe aan uw schema. In uw geval wilt u profielen identificeren die uw game afspelen met de Experience Cloud-id en het e-mailadres waarmee ze zich aanmelden bij hun gameconsole. Er zijn veel andere kenmerken beschikbaar om de identiteit van uw persoon te volgen.

   Selecteer **[!UICONTROL Apply]** om dit object aan uw schema toe te voegen.

1. Selecteer het veld **[!UICONTROL ecid]** in het identificatieobject dat u net hebt toegevoegd en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Primary Identity]** en **[!UICONTROL ECID]** in de lijst [!UICONTROL Identity namespace] in het rechterdeelvenster.

   ![ specificeer ECID als identiteit ](./assets/specify-identity-gaming.png)

   U geeft de Experience Cloud Identity op als de primaire identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (aan te sluiten) met dezelfde ECID.

   Selecteer **[!UICONTROL Apply]** . U ziet dat er een vingerafdrukpictogram wordt weergegeven in het ecid-kenmerk.

1. Selecteer het veld **[!UICONTROL email]** in het identificatieobject dat u net hebt toegevoegd en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Email]** in de lijst [!UICONTROL Identity namespace] in het deelvenster [!UICONTROL Field Properties] .

   ![ specificeer e-mail als identiteit ](./assets/specify-email-identity-gaming.png)

   U geeft het e-mailadres op als een andere identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (naaien).

   Selecteer **[!UICONTROL Apply]** . U ziet dat er een vingerafdrukpictogram wordt weergegeven in het e-mailkenmerk.

   Selecteer **[!UICONTROL Save]** .

1. Selecteer het hoofdelement van het schema met de naam van het schema en selecteer vervolgens de **[!UICONTROL Profile]** switch.

   U wordt gevraagd het schema in te schakelen voor het profiel. Zodra toegelaten, wanneer het gegeven in datasets wordt opgenomen die op dit schema worden gebaseerd, worden die gegevens samengevoegd in het Real-Time Profiel van de Klant.

   Zie [ het schema voor gebruik in het Profiel van de Klant in real time ](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#profile) voor meer informatie toelaten.

   >[!IMPORTANT]
   >
   >    Nadat u een schema hebt opgeslagen dat is ingeschakeld voor profiel, kan het niet meer worden uitgeschakeld voor profiel.

   ![ laat schema voor profiel ](./assets/enable-for-profile.png) toe

1. Selecteer **[!UICONTROL Save]** om het schema op te slaan.

U hebt een minimaal schema gemaakt dat de gegevens modelleert die u van uw game kunt vastleggen. Met het schema kunnen profielen worden geïdentificeerd aan de hand van de identiteit en het e-mailadres van het Experience Cloud. Door het schema voor profiel in te schakelen, zorgt u ervoor dat de gegevens die zijn vastgelegd in uw consolegame worden toegevoegd aan het Real-Time Klantprofiel.

Naast gedragsgegevens kunt u ook profielkenmerkgegevens vastleggen vanaf uw console (bijvoorbeeld details van profielen die zijn ondertekend in de console).

Als u profielgegevens wilt vastleggen, doet u het volgende:

- Maak een schema op basis van de klasse Individueel profiel XDM.

- Voeg de het gebiedsgroep van de Kern van het Profiel v2 aan het schema toe.

- Voeg een identificatieobject toe op basis van de veldgroep Profile Core v2.

- Experience Cloud-id definiëren als primaire id en e-mailadres als id.

- Het schema inschakelen voor profiel

Zie [ schema&#39;s in UI ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html) voor meer informatie creëren en uitgeven bij het toevoegen van en het verwijderen van gebiedsgroepen en individuele gebieden aan een schema.

### Een gegevensset instellen

Met uw schema, hebt u uw gegevensmodel bepaald. U moet nu de constructie bepalen om die gegevens op te slaan en te beheren door datasets te gebruiken.

Uw gegevensset instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Datasets]** within [!UICONTROL DATA MANAGEMENT] in het linkerspoor.

2. Selecteer **[!UICONTROL Create dataset]** .

   ![ creeer dataset ](./assets/create-dataset.png)

3. Selecteer **[!UICONTROL Create dataset from schema]** .

   ![ creeer dataset van schema ](./assets/create-dataset-from-schema.png)

4. Selecteer het schema dat u eerder hebt gemaakt en selecteer **[!UICONTROL Next]** .

5. Geef uw gegevensset een naam en (optioneel) geef een beschrijving op.

   ![ dataset van de Naam ](./assets/name-your-datatest.png)

6. Selecteer **[!UICONTROL Finish]** .

7. Selecteer de **[!UICONTROL Profile]** schakelaar.

   U wordt ertoe aangezet om de dataset voor profiel toe te laten. Zodra toegelaten, verrijkt de dataset klantenprofielen in real time met zijn opgenomen gegevens.

   >[!IMPORTANT]
   >
   >    U kunt een dataset voor profiel slechts toelaten wanneer het schema, waaraan de dataset voldoet, ook voor profiel wordt toegelaten.

   ![ laat schema voor profiel ](./assets/aepwebsdk-dataset-profile.png) toe

Zie {de gids UI van de Datasets van 0} ](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=nl) voor veel meer informatie over hoe te bekijken, voorproef, tot stand brengen, een dataset schrappen. [ En hoe te om een dataset voor het Profiel van de Klant in real time toe te laten.

## Een gegevensstroom instellen

Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web van Adobe Experience Platform en Mobiele SDKs en de Server API van de Edge Network van Adobe Experience Platform. Wanneer het verzamelen van gegevens met Adobe Experience Platform SDKs en de Server APIs van de Edge Network, worden de gegevens verzonden naar de Edge Network van Adobe Experience Platform. Het is de gegevensstroom die bepaalt aan welke diensten dat de gegevens door:sturen.

In uw opstelling, wilt u de gegevens die u van het spel verzamelt worden verzonden naar uw dataset in Adobe Experience Platform.

Uw gegevensstroom instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform **[!UICONTROL Datastreams]** in [!UICONTROL DATA COLLECTION] in de linkertrack.

2. Selecteer **[!UICONTROL New Datastream]** .

3. Geef een naam en beschrijf de gegevensstroom. Selecteer het schema in de lijst [!UICONTROL Event Schema] .

   ![ Nieuwe DataStream ](./assets/new-datastream.png)

4. Selecteer **[!UICONTROL Save]** .

5. Selecteer **[!UICONTROL Add Service]** .

6. In de lus [!UICONTROL Add Service screen] :

   1. Selecteer **[!UICONTROL Adobe Experience Platform]** in de lijst [!UICONTROL Service] .

   2. Zorg ervoor dat **[!UICONTROL Enabled]** is geselecteerd.

   3. Selecteer de gegevensset in de lijst [!UICONTROL Event Dataset] .

      ![ datastream AEP dienst ](./assets/datastream-aep-service.png)

   4. Laat de andere instellingen staan en selecteer **[!UICONTROL Save]** om de gegevensstroom op te slaan.

Uw gegevensstroom is nu geconfigureerd om de gegevens die van uw game zijn verzameld door te sturen naar uw gegevensset in Adobe Experience Platform.

Zie [ Overzicht van gegevensstromen ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html) voor meer informatie over hoe te om een gegevensstroom te vormen en hoe te om gevoelige gegevens te behandelen.

## Edge Network Server-API gebruiken

Bij de ontwikkeling van uw game kunt u desgewenst relevante aanroepen toevoegen aan de Adobe Experience Platform Edge Network Server-API.

Als u bijvoorbeeld de score van de speler wilt bijwerken, gebruikt u:

```
curl -X POST "https://server.adobedc.net/ee/v2/interact?dataStreamId={DATASTREAM_ID}"
-H "Authorization: Bearer {TOKEN}"
-H "x-gw-ims-org-id: {ORG_ID}"
-H "x-api-key: {API_KEY}"
-H "Content-Type: application/json"
-d '{
   "event": {
      "xdm": {
         "identityMap": {
            "Email_LC_SHA256": [
               {
                  "id": "0c7e6a405862e402eb76a70f8a26fc732d07c32931e9fae9ab1582911d2e8a3b",
                  "primary": true
               }
            ]
         },
         "eventType": "game.scoreUpdate",
         "{sandbox}": {
            "scores": {
               "afterMatch": 132391",
            }
         },
         "timestamp": "2021-08-09T14:09:20.859Z"
      }
   }
}'
```

In het verzoek van de POST van het voorbeeld, `{DATASTREAM_ID}` richt aan het herkenningsteken van de voorbeeldgegevensstroom u vroeger vormde. `{sandbox}` is de unieke naam van de sandbox die het pad identificeert naar de aangepaste veldgroep Blinding Light.

Zie [ Interactieve gegevensinzameling ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html) en [ Niet-interactieve gegevensinzameling ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/non-interactive-data-collection.html) voor meer informatie over hoe te om de Server API van de Edge Network te gebruiken.

## Een verbinding instellen

Om de gegevens van Adobe Experience Platform in Customer Journey Analytics te gebruiken, creeert u een verbinding die de gegevens omvat die uit vestiging uw schema, dataset, en werkschema voortvloeien.

Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over deze datasets te rapporteren, moet u eerst een verband tussen datasets in Adobe Experience Platform en Workspace vestigen.

Om uw verbinding tot stand te brengen:

1. Selecteer **[!UICONTROL Connections]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Create new connection]** .

3. In het [!UICONTROL Untitled connection] -scherm:

   Geef een naam en beschrijf de verbinding in [!UICONTROL Connection Settings] .

   Selecteer de juiste sandbox in de lijst [!UICONTROL Sandbox] in [!UICONTROL Data settings] en selecteer het aantal dagelijkse gebeurtenissen in de lijst [!UICONTROL Average number of daily events] .

   ![ de Montages van de Verbinding ](./assets/cja-connections-1.png)

   Selecteer **[!UICONTROL Add datasets]** .

   In de stap [!UICONTROL Select datasets] in [!UICONTROL Add datasets] :

   - Selecteer datasets die u vroeger en/of andere relevante datasets creeerde u in uw verbinding wilt omvatten

   - Selecteer **[!UICONTROL Next]** .

   In de stap [!UICONTROL Datasets settings] in [!UICONTROL Add datasets] :

   - Voor elke gegevensset:

      - Selecteer een [!UICONTROL Person ID] van de beschikbare identiteiten die in de datasetschema&#39;s in Adobe Experience Platform worden bepaald.

      - Selecteer de juiste gegevensbron in de lijst [!UICONTROL Data source type] . Als u **[!UICONTROL Other]** opgeeft, voegt u een beschrijving voor de gegevensbron toe.

      - Stel **[!UICONTROL Import all new data]** en **[!UICONTROL Dataset backfill existing data]** in op basis van uw voorkeuren.

   - Selecteer **[!UICONTROL Add datasets]** .

   Selecteer **[!UICONTROL Save]** .

Zie [ Overzicht van Verbindingen ](../connections/overview.md) voor meer informatie over om een verbinding tot stand te brengen en te beheren en datasets te selecteren en te combineren.

## Een gegevensweergave instellen

Een gegevensmening is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

Uw gegevensweergave maken:

1. Selecteer **[!UICONTROL Data views]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Create new data view]** .

3. In de stap [!UICONTROL Configure] :

   Selecteer de verbinding in de lijst [!UICONTROL Connection] .

   Naam en (optioneel) beschrijf uw verbinding.

   ![ de mening van Gegevens vormt ](./assets/cja-dataview-1.png)

   Selecteer **[!UICONTROL Save and continue]** .

4. In de stap [!UICONTROL Components] :

   Voeg schemagebieden en/of standaardcomponent toe die u aan de [!UICONTROL METRICS] of [!UICONTROL DIMENSIONS] componentenvakjes wilt omvatten.

   Selecteer **[!UICONTROL Save and continue]** .

5. In de stap [!UICONTROL Settings] :

   ![ de meningsmontages van Gegevens ](./assets/cja-dataview-3.png)

   Laat de instellingen ongewijzigd en selecteer **[!UICONTROL Save and finish]** .

Zie [ overzicht van de meningen van Gegevens ](../data-views/data-views.md) voor meer informatie over om een gegevensmening tot stand te brengen en uit te geven, welke componenten voor u aan gebruik in uw gegevensmening en hoe te filter en zittingsmontages te gebruiken beschikbaar zijn.


## Een project instellen

Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen op basis van uw gegevens. U gebruikt de projecten van Workspace om gegevenscomponenten, lijsten, en visualisaties te combineren om uw analyse te bundelen en met iedereen in uw organisatie te delen.

Uw project maken:

1. Selecteer **[!UICONTROL Projects]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Projects]** in de linkernavigatie.

3. Selecteer **[!UICONTROL Create project]** .

   ![ Project van Workspace ](./assets/cja-projects-1.png)

   Selecteer **[!UICONTROL Blank project]** .

   ![ Workspace - Leeg Project ](./assets/cja-projects-2.png)

4. Selecteer de gegevensweergave in de lijst.

   ![ de Uitgezochte mening van Gegevens van Workspace ](./assets/cja-projects-3.png).

5. Als u uw eerste rapport wilt maken, sleept u de afmetingen en metriek op de [!UICONTROL Freeform table] in de [!UICONTROL Panel] .

Zie [ overzicht van Analysis Workspace ](../analysis-workspace/home.md) voor meer informatie over hoe te om projecten tot stand te brengen en uw analyse te bouwen gebruikend componenten, visualisaties, en panelen.

>[!SUCCESS]
>
>U hebt alle stappen uitgevoerd. Eerst definieert u welke gegevens u wilt verzamelen (schema) en waar u deze wilt opslaan (dataset) in Adobe Experience Platform. U vormde een gegevensstroom op de Edge Network om ervoor te zorgen dat de gegevens aan die dataset kunnen door:sturen. Vervolgens hebt u de Edge Network Server-API gebruikt om die gegevens naar uw gegevensstroom te verzenden. U hebt een verbinding in Customer Journey Analytics gedefinieerd om uw spelgegevens en andere gegevens te gebruiken. Met de definitie van uw gegevensweergave kunt u opgeven welke dimensie en metriek u wilt gebruiken en hebt u uiteindelijk uw eerste project gemaakt waarmee u uw gamegegevens kunt visualiseren en analyseren.
