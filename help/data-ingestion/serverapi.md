---
title: Gegevens verzamelen via de Adobe Experience Platform Edge Network Server-API
description: Uitleggen hoe u gegevens in Customer Journey Analytics kunt opnemen via de Adobe Experience Platform Edge Network Server-API en het Edge Network
solution: Customer Journey Analytics
feature: Basics
exl-id: 6bfb7254-5bb7-45c6-86a2-0651a0d222fa
source-git-commit: caf2db9ae0b550ce47fa196a955fcceddf8bf2b7
workflow-type: tm+mt
source-wordcount: '2181'
ht-degree: 0%

---

# Gegevens verzamelen via de Adobe Experience Platform Edge Network Server-API

In deze snelstartgids wordt uitgelegd hoe u gegevens voor het bijhouden van gegevens kunt invoeren van apparaten zoals IoT-apparaten, set-top boxes, gameconsoles, bureaubladtoepassingen rechtstreeks in Adobe Experience Platform met de Adobe Experience Platform Edge Network Server API en Edge Network. Gebruik die gegevens vervolgens in Customer Journey Analytics.

Hiervoor moet u:

- **Een schema en gegevensset instellen** in Adobe Experience Platform om het model (schema) te bepalen van de gegevens die u wilt verzamelen en waar te om de gegevens (dataset) daadwerkelijk te verzamelen.

- **Een gegevensstroom instellen** om het Adobe Experience Platform Edge Network te configureren om de verzamelde gegevens te routeren naar de gegevensset die u in Adobe Experience Platform hebt geconfigureerd.

- **Server-API gebruiken** om gegevens rechtstreeks vanuit uw toepassing of game die op een desktop, spelconsole, IoT-apparaat of set-top box worden uitgevoerd, naar uw datastream te verzenden.

- **Implementeren en valideren**. Zorg voor een omgeving waarin u uw ontwikkeling kunt doorlopen en publiceer deze live op uw productieomgeving als alles is gevalideerd.

- **Een verbinding instellen** in de Customer Journey Analytics. Deze verbinding zou (minstens) uw dataset van Adobe Experience Platform moeten omvatten.

- **Een gegevensweergave instellen** in Customer Journey Analytics om metriek en afmeting te bepalen die u in Analysis Workspace wilt gebruiken.

- **Een project instellen** in Customer Journey Analytics om uw rapporten en visualisaties te bouwen.

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

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Schemas]** binnen [!UICONTROL DATA MANAGEMENT].

1. Selecteren **[!UICONTROL Create schema]**. .
1. In Uitgezocht een klassenstap van de Create schematovenaar:

   1. Selecteren **[!UICONTROL Experience Event]**.

      ![Een schema maken](./assets/create-ee-schema-wizard-step-1.png)

      >[!INFO]
      >
      >    Een schema van de Gebeurtenis van de Ervaring wordt gebruikt om het _gedrag_ van een profiel (zoals scènenaam, drukknop om aan winkelwagentje toe te voegen). Een afzonderlijk profielschema wordt gebruikt om het profiel te modelleren _attributes_ (zoals naam, e-mail, geslacht).

   1. Selecteren **[!UICONTROL Next]**.


1. In de [!UICONTROL Name and review step] van de [!UICONTROL Create schema] wizard:

   1. Voer een **[!UICONTROL Schema display name]** voor uw schema en (optioneel) a **[!UICONTROL Description]**.

      ![Geef uw schema een naam](./assets/create-ee-schema-wizard-step-2.png)

   1. Selecteren **[!UICONTROL Finish]**.

1. Op het tabblad Structuur van het voorbeeldschema:

   1. Selecteren **[!UICONTROL + Add]** in [!UICONTROL Field groups].

      ![Veldgroep toevoegen](./assets/add-field-group-button.png)

      Veldgroepen zijn herbruikbare verzamelingen van objecten en kenmerken waarmee u het schema eenvoudig kunt uitbreiden.

   1. In de [!UICONTROL Add fields groups] selecteert u de **[!UICONTROL Blinding Light]** veldgroep in de lijst. Deze veldgroep wordt gemaakt om de voortgang van de gebruiker bij te houden bij het afspelen van een fictieve game met de naam Blinding Light op een console.

      ![Blinding, lichtveldgroep](assets/schema-fieldgroup-blindinglight.png)

      U kunt de voorvertoningsknop selecteren om een voorvertoning weer te geven van de velden die deel uitmaken van deze veldgroep, zoals `scores > afterMatch`.

      ![Voorvertoning van bindingslichtveldgroep](assets/schema-fieldgroup-blindinglight-preview.png)

      Selecteren **[!UICONTROL Back]** om de voorvertoning te sluiten.

   1. Selecteren **[!UICONTROL Add field groups]**.

1. Selecteren **[!UICONTROL +]** naast de naam van het schema.

   ![Voorbeeld: Veld toevoegen, knop](./assets/example-gamingschema-plus.png)

1. In de [!UICONTROL Field Properties] paneel, enter `identification` als de [!UICONTROL Field name], **[!UICONTROL Identification]** als de [!UICONTROL Display name], selecteert u **[!UICONTROL Object]** als de [!UICONTROL Type] en selecteert u **[!UICONTROL ExperienceEvent Core v2.1]** als de [!UICONTROL Field Group].

   ![Identificatieobject](./assets/identification-field-gaming.png)

   Het identificatieobject voegt id-mogelijkheden toe aan uw schema. In uw geval wilt u profielen identificeren die uw game afspelen met de Experience Cloud-id en het e-mailadres waarmee ze zich aanmelden bij hun gameconsole. Er zijn veel andere kenmerken beschikbaar om de identiteit van uw persoon te volgen.

   Selecteren **[!UICONTROL Apply]** om dit object aan uw schema toe te voegen.

1. Selecteer de **[!UICONTROL ecid]** veld in het identificatieobject dat u zojuist hebt toegevoegd, en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Primary Identity]** en **[!UICONTROL ECID]** van de [!UICONTROL Identity namespace] in het rechterdeelvenster.

   ![ECID opgeven als identiteit](./assets/specify-identity-gaming.png)

   U geeft de Experience Cloud Identity op als de primaire identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (aan te sluiten) met dezelfde ECID.

   Selecteren **[!UICONTROL Apply]**. U ziet dat er een vingerafdrukpictogram wordt weergegeven in het ecid-kenmerk.

1. Selecteer de **[!UICONTROL email]** veld in het identificatieobject dat u zojuist hebt toegevoegd, en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Email]** van de [!UICONTROL Identity namespace] in de lijst [!UICONTROL Field Properties] deelvenster.

   ![E-mail opgeven als identiteit](./assets/specify-email-identity-gaming.png)

   U geeft het e-mailadres op als een andere identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (naaien).

   Selecteren **[!UICONTROL Apply]**. U ziet dat er een vingerafdrukpictogram wordt weergegeven in het e-mailkenmerk.

   Selecteren **[!UICONTROL Save]**.

1. Selecteer het basiselement van uw schema dat de naam van het schema toont, dan selecteer **[!UICONTROL Profile]** switch.

   U wordt gevraagd het schema in te schakelen voor het profiel. Zodra toegelaten, wanneer het gegeven in datasets wordt opgenomen die op dit schema worden gebaseerd, worden die gegevens samengevoegd in het Real-Time Profiel van de Klant.

   Zie [Het schema inschakelen voor gebruik in Real-Time Klantprofiel](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=en#profile) voor meer informatie .

   >[!IMPORTANT]
   >
   >    Nadat u een schema hebt opgeslagen dat is ingeschakeld voor profiel, kan het niet meer worden uitgeschakeld voor profiel.

   ![Schema voor profiel inschakelen](./assets/enable-for-profile.png)

1. Selecteren **[!UICONTROL Save]** om uw schema op te slaan.

U hebt een minimaal schema gemaakt dat de gegevens modelleert die u van uw game kunt vastleggen. Met het schema kunnen profielen worden geïdentificeerd aan de hand van de identiteit en het e-mailadres van het Experience Cloud. Door het schema voor profiel in te schakelen, zorgt u ervoor dat de gegevens die zijn vastgelegd in uw consolegame worden toegevoegd aan het Real-Time Klantprofiel.

Naast gedragsgegevens kunt u ook profielkenmerkgegevens vastleggen vanaf uw console (bijvoorbeeld details van profielen die zijn ondertekend in de console).

Als u profielgegevens wilt vastleggen, doet u het volgende:

- Maak een schema op basis van de klasse Individueel profiel XDM.

- Voeg de het gebiedsgroep van de Kern van het Profiel v2 aan het schema toe.

- Voeg een identificatieobject toe op basis van de veldgroep Profile Core v2.

- Experience Cloud-id definiëren als primaire id en e-mailadres als id.

- Het schema inschakelen voor profiel

Zie [Schema&#39;s maken en bewerken in de gebruikersinterface](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html) voor meer informatie over het toevoegen en verwijderen van veldgroepen en afzonderlijke velden aan een schema.

### Een gegevensset instellen

Met uw schema, hebt u uw gegevensmodel bepaald. U moet nu de constructie bepalen om die gegevens op te slaan en te beheren door datasets te gebruiken.

Uw gegevensset instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Datasets]** binnen [!UICONTROL DATA MANAGEMENT].

2. Selecteren **[!UICONTROL Create dataset]**.

   ![Gegevensset maken](./assets/create-dataset.png)

3. Selecteren **[!UICONTROL Create dataset from schema]**.

   ![Gegevensset maken van schema](./assets/create-dataset-from-schema.png)

4. Selecteer het eerder gemaakte schema en selecteer **[!UICONTROL Next]**.

5. Geef uw gegevensset een naam en (optioneel) geef een beschrijving op.

   ![Gegevensset naam](./assets/name-your-datatest.png)

6. Selecteren **[!UICONTROL Finish]**.

7. Selecteer de **[!UICONTROL Profile]** switch.

   U wordt ertoe aangezet om de dataset voor profiel toe te laten. Zodra toegelaten, verrijkt de dataset klantenprofielen in real time met zijn opgenomen gegevens.

   >[!IMPORTANT]
   >
   >    U kunt een dataset voor profiel slechts toelaten wanneer het schema, waaraan de dataset voldoet, ook voor profiel wordt toegelaten.

   ![Schema voor profiel inschakelen](./assets/aepwebsdk-dataset-profile.png)

Zie [UI-gids voor gegevensbestanden](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=nl) voor veel meer informatie over hoe te om, voorproef te bekijken, creeer, schrapt een dataset. En hoe te om een dataset voor het Profiel van de Klant in real time toe te laten.

## Een gegevensstroom instellen

Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van Adobe Experience Platform Web en Mobiele SDKs en de Server API van het Netwerk van Adobe Experience Platform Edge. Bij het verzamelen van gegevens met de Adobe Experience Platform SDK&#39;s en Edge Network Server-API&#39;s worden gegevens verzonden naar het Adobe Experience Platform Edge Network. Het is de gegevensstroom die bepaalt aan welke diensten dat de gegevens door:sturen.

In uw opstelling, wilt u de gegevens die u van het spel verzamelt worden verzonden naar uw dataset in Adobe Experience Platform.

Uw gegevensstroom instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform **[!UICONTROL Datastreams]** van [!UICONTROL DATA COLLECTION] in het linkerspoor.

2. Selecteren **[!UICONTROL New Datastream]**.

3. Geef een naam en beschrijf de gegevensstroom. Selecteer uw schema in het menu [!UICONTROL Event Schema] lijst.

   ![Nieuwe DataStream](./assets/new-datastream.png)

4. Selecteren **[!UICONTROL Save]**.

5. Selecteren **[!UICONTROL Add Service]**.

6. In de [!UICONTROL Add Service screen]:

   1. Selecteren **[!UICONTROL Adobe Experience Platform]** van de [!UICONTROL Service] lijst.

   2. Zorgen **[!UICONTROL Enabled]** is geselecteerd.

   3. Selecteer uw gegevensset in het menu [!UICONTROL Event Dataset] lijst.

      ![DataStream AEP-service](./assets/datastream-aep-service.png)

   4. Laat de andere instellingen staan en selecteer **[!UICONTROL Save]** om de gegevensstroom op te slaan.

Uw gegevensstroom is nu geconfigureerd om de gegevens die van uw game zijn verzameld door te sturen naar uw gegevensset in Adobe Experience Platform.

Zie [Overzicht gegevensstromen](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=en) voor meer informatie over hoe te om een gegevensstroom te vormen en hoe te om gevoelige gegevens te behandelen.

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

In het verzoek van de POST van het voorbeeld, `{DATASTREAM_ID}` verwijst naar de id van de voorbeeldgegevensstroom die u eerder hebt geconfigureerd. `{sandbox}` Dit is de unieke naam van de sandbox die het pad identificeert naar de aangepaste veldgroep Blinding Light.

Zie [Interactieve gegevensverzameling](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=en) en [Niet-interactieve gegevensverzameling](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/non-interactive-data-collection.html?lang=en) voor meer informatie over het gebruik van de Edge Network Server-API.

## Een verbinding instellen

Om de gegevens van Adobe Experience Platform in Customer Journey Analytics te gebruiken, creeert u een verbinding die de gegevens omvat die uit vestiging uw schema, dataset, en werkschema voortvloeien.

Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over deze datasets te rapporteren, moet u eerst een verband tussen datasets in Adobe Experience Platform en Werkruimte vestigen.

Om uw verbinding tot stand te brengen:

1. Selecteer in de gebruikersinterface van de Customer Journey Analytics de optie **[!UICONTROL Connections]** in de bovenste navigatie.

2. Selecteren **[!UICONTROL Create new connection]**.

3. In de [!UICONTROL Untitled connection] scherm:

   Geef een naam en beschrijf de verbinding in [!UICONTROL Connection Settings].

   Selecteer de juiste sandbox in het menu [!UICONTROL Sandbox] lijst in [!UICONTROL Data settings] en selecteert u het aantal dagelijkse gebeurtenissen in het menu [!UICONTROL Average number of daily events] lijst.

   ![Verbindingsinstellingen](./assets/cja-connections-1.png)

   Selecteren **[!UICONTROL Add datasets]**.

   In de [!UICONTROL Select datasets] stap in [!UICONTROL Add datasets]:

   - Selecteer datasets die u vroeger en/of andere relevante datasets creeerde u in uw verbinding wilt omvatten

   - Selecteren **[!UICONTROL Next]**.

   In de [!UICONTROL Datasets settings] stap in [!UICONTROL Add datasets]:

   - Voor elke gegevensset:

      - Selecteer een [!UICONTROL Person ID] uit de beschikbare identiteiten die zijn gedefinieerd in de gegevenssetschema&#39;s in Adobe Experience Platform.

      - Selecteer de juiste gegevensbron in het menu [!UICONTROL Data source type] lijst. Als u **[!UICONTROL Other]** Voeg vervolgens een beschrijving voor uw gegevensbron toe.

      - Set **[!UICONTROL Import all new data]** en **[!UICONTROL Dataset backfill existing data]** volgens uw voorkeuren.

   - Selecteren **[!UICONTROL Add datasets]**.

   Selecteren **[!UICONTROL Save]**.

Zie [Overzicht van verbindingen](../connections/overview.md) voor meer informatie over om een verbinding tot stand te brengen en te beheren en datasets te selecteren en te combineren.

## Een gegevensweergave instellen

Een gegevensmening is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

Uw gegevensweergave maken:

1. Selecteer in de gebruikersinterface van de Customer Journey Analytics de optie **[!UICONTROL Data views]** in de bovenste navigatie.

2. Selecteren **[!UICONTROL Create new data view]**.

3. In de [!UICONTROL Configure] stap:

   Selecteer uw verbinding van [!UICONTROL Connection] lijst.

   Naam en (optioneel) beschrijf uw verbinding.

   ![Gegevensweergave configureren](./assets/cja-dataview-1.png)

   Selecteren **[!UICONTROL Save and continue]**.

4. In de [!UICONTROL Components] stap:

   Voeg schemagebieden en/of standaardcomponent toe die u aan wilt omvatten [!UICONTROL METRICS] of [!UICONTROL DIMENSIONS] deelvakken.

   Selecteren **[!UICONTROL Save and continue]**.

5. In de [!UICONTROL Settings] stap:

   ![Instellingen voor gegevensweergave](./assets/cja-dataview-3.png)

   De instellingen ongewijzigd laten en selecteren **[!UICONTROL Save and finish]**.

Zie [Overzicht van gegevensweergaven](../data-views/data-views.md) voor meer informatie over het maken en bewerken van een gegevensweergave, welke componenten beschikbaar zijn voor u in de gegevensweergave en hoe u filter- en sessieinstellingen kunt gebruiken.


## Een project instellen

Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen op basis van uw gegevens. U gebruikt de projecten van de Werkruimte om gegevenscomponenten, lijsten, en visualisaties te combineren om uw analyse te bundelen en met iedereen in uw organisatie te delen.

Uw project maken:

1. Selecteer in de gebruikersinterface van de Customer Journey Analytics de optie **[!UICONTROL Projects]** in de bovenste navigatie.

2. Selecteren **[!UICONTROL Projects]** in de linkernavigatie.

3. Selecteren **[!UICONTROL Create project]**.

   ![Werkruimteproject](./assets/cja-projects-1.png)

   Selecteren **[!UICONTROL Blank project]**.

   ![Werkruimte - Leeg project](./assets/cja-projects-2.png)

4. Selecteer de gegevensweergave in de lijst.

   ![Werkruimte selecteren, gegevensweergave](./assets/cja-projects-3.png).

5. Als u uw eerste rapport wilt maken, sleept u de afmetingen en metriek naar het [!UICONTROL Freeform table] in de [!UICONTROL Panel].

Zie [Analysis Workspace-overzicht](../analysis-workspace/home.md) voor meer informatie over hoe te om projecten tot stand te brengen en uw analyse te bouwen gebruikend componenten, visualisaties, en panelen.

>[!SUCCESS]
>
>U hebt alle stappen uitgevoerd. Eerst definieert u welke gegevens u wilt verzamelen (schema) en waar u deze wilt opslaan (dataset) in Adobe Experience Platform. U vormde een gegevensstroom op het Netwerk van de Rand om ervoor te zorgen dat de gegevens aan die dataset kunnen door:sturen. Vervolgens hebt u de Edge Network Server-API gebruikt om die gegevens naar uw gegevensstroom te verzenden. U hebt een verbinding in Customer Journey Analytics gedefinieerd om uw spelgegevens en andere gegevens te gebruiken. Met de definitie van uw gegevensweergave kunt u opgeven welke dimensie en metriek u wilt gebruiken en hebt u uiteindelijk uw eerste project gemaakt waarmee u uw gamegegevens kunt visualiseren en analyseren.
