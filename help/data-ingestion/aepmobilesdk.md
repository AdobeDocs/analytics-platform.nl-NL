---
title: Gegevens verzamelen via de Adobe Experience Platform Mobile SDK
description: Uitleggen hoe u gegevens in Customer Journey Analytics kunt opnemen via de Adobe Experience Platform Mobile SDK en de Edge Network
solution: Customer Journey Analytics
feature: Basics
exl-id: fb48b031-e093-4490-b457-69dbb5debe8d
role: Admin
source-git-commit: 9849d686e886426124842ce210b423ac6c74fb89
workflow-type: tm+mt
source-wordcount: '3085'
ht-degree: 0%

---

# Gegevens verzamelen via de Mobile SDK

In deze handleiding voor snel starten wordt uitgelegd hoe u gegevens voor het bijhouden van mobiele apps rechtstreeks in Adobe Experience Platform kunt opnemen met de Adobe Experience Platform Mobile SDK en Edge Network. Gebruik die gegevens vervolgens in Customer Journey Analytics.

Hiervoor moet u:

- **opstelling een schema en dataset** in Adobe Experience Platform om het model (schema) van de gegevens te bepalen die u wilt verzamelen en waar te om de gegevens (dataset) eigenlijk te verzamelen.

- **opstelling een datastream** om de Edge Network van Adobe Experience Platform te vormen om uw verzamelde gegevens aan de dataset te leiden u in Adobe Experience Platform vormde.

- **Markeringen van het Gebruik** om regels en gegevenselementen tegen de gegevens in uw mobiele toepassing gemakkelijk te vormen. Dan zorg ervoor dat het gegeven wordt verzonden naar de datastream die op de Edge Network van Adobe Experience Platform wordt gevormd.

- **stelt en bevestigt** op. Zorg voor een omgeving waarin u de ontwikkeling van tags kunt doorlopen en publiceer deze live in uw productieomgeving als alles is gevalideerd.

- **opstelling een verbinding** in Customer Journey Analytics. Deze verbinding zou (minstens) uw dataset van Adobe Experience Platform moeten omvatten.

- **opstelling een gegevensmening** in Customer Journey Analytics om metriek en afmeting te bepalen die u in Analysis Workspace wilt gebruiken.

- **opstelling een project** in Customer Journey Analytics om uw rapporten en visualisaties te bouwen.

>[!NOTE]
>
>Deze handleiding voor snel starten is een vereenvoudigde gids voor het invoeren van gegevens die zijn verzameld van uw toepassing in Adobe Experience Platform en voor gebruik in Customer Journey Analytics. Het wordt ten zeerste aanbevolen de aanvullende informatie te bestuderen wanneer deze wordt vermeld.


## Een schema en gegevensset instellen

Als u gegevens in Adobe Experience Platform wilt invoeren, moet u eerst definiëren welke gegevens u wilt verzamelen. Alle gegevens die in Adobe Experience Platform worden ingevoerd, moeten voldoen aan een standaard, gedenormaliseerde structuur, zodat deze kan worden herkend en kan worden toegepast door de mogelijkheden en functies op de downstreammarkt. Het Model van Gegevens van de ervaring (XDM) is het standaardkader dat een structuur in de vorm van schema&#39;s verstrekt.

Zodra u een schema hebt bepaald, gebruikt u één of meerdere datasets om de inzameling van gegevens op te slaan en te beheren. Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens (typisch een lijst) die een schema (kolommen) en gebieden (rijen) bevat.

Alle gegevens die in Adobe Experience Platform worden opgenomen moeten met een vooraf gedefinieerd schema in overeenstemming zijn alvorens het als dataset kan worden voortgeduurd.

### Een schema instellen

U wilt enkele minimale gegevens van profielen bijhouden met uw mobiele app, bijvoorbeeld scènenaam en -identificatie.
U moet eerst een schema bepalen dat deze gegevens modelleert.

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

   1. Selecteer in het dialoogvenster [!UICONTROL Add fields groups] de veldgroep **[!UICONTROL AEP Mobile SDK ExperienceEvent]** in de lijst.

      ![ AEP Mobiele het gebiedsgroep van de Details van de Levenscyclus van de Levenscyclus ](./assets/select-aepmobilesdk-experienceevent.png)

      U kunt de voorvertoningsknop selecteren om een voorvertoning weer te geven van de velden die deel uitmaken van deze veldgroep, bijvoorbeeld `application > name` .

      ![ AEP Mobiele het gebiedsvoorproef van de Detailgroep van de Levenscyclus van de Levenscyclus ](./assets/aepmobilesdk-experienceevent-preview.png)

      Selecteer **[!UICONTROL Back]** om de voorvertoning te sluiten.

   1. Selecteer **[!UICONTROL Add field groups]** .

1. Selecteer **[!UICONTROL +]** naast de naam van het schema in het deelvenster [!UICONTROL Structure] .

   ![ het Schema van het Voorbeeld voegt de knoop van het Gebied toe ](./assets/example-mobileschema-plus.png)

1. Typ in het deelvenster [!UICONTROL Field Properties] `identification` als de [!UICONTROL Field name] , **[!UICONTROL Identification]** als de [!UICONTROL Display name] , selecteer **[!UICONTROL Object]** als de [!UICONTROL Type] en selecteer **[!UICONTROL ExperienceEvent Core v2.1]** als de [!UICONTROL Field Group] .

   >[!NOTE]
   >
   >Als die veldgroep niet beschikbaar is, zoekt u naar een andere veldgroep met identiteitsvelden. Of [ creeer een nieuwe gebiedsgroep ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/field-groups.html) en [ voeg nieuwe identiteitsgebieden ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/fields/identity.html#define-a-identity-field) (als `ecid`, `crmId`, en anderen toe u) aan de gebiedsgroep nodig hebt en selecteer die nieuwe gebiedsgroep.

   ![ Voorwerp van de Identificatie ](./assets/identification-field-mobile.png)

   Het identificatieobject voegt id-mogelijkheden toe aan uw schema. In uw geval wilt u profielen identificeren met uw mobiele app aan de hand van de Experience Cloud-id en het e-mailadres. Er zijn vele andere eigenschappen beschikbaar om de identificatie van uw persoon te volgen (bijvoorbeeld klant identiteitskaart, loyalty identiteitskaart).

   Selecteer **[!UICONTROL Apply]** om dit object aan uw schema toe te voegen.

1. Selecteer het veld **[!UICONTROL ecid]** in het identificatieobject dat u net hebt toegevoegd en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Primary Identity]** en **[!UICONTROL ECID]** in de lijst [!UICONTROL Identity namespace] in het rechterdeelvenster.

   ![ specificeer ECID als identiteit ](./assets/specify-identity-mobile.png)

   U geeft de Experience Cloud Identity op als de primaire identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (aan te sluiten) met dezelfde ECID.

   Selecteer **[!UICONTROL Apply]** . U ziet dat er een vingerafdrukpictogram wordt weergegeven in het ecid-kenmerk.

1. Selecteer het veld **[!UICONTROL email]** in het identificatieobject dat u net hebt toegevoegd en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Email]** in de lijst [!UICONTROL Identity namespace] in het deelvenster [!UICONTROL Field Properties] .

   ![ specificeer e-mail als identiteit ](./assets/specify-email-identity-mobile.png)

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

U hebt een minimumschema gemaakt dat de gegevens modelleert die u van uw mobiele toepassing kunt vangen. Met het schema kunnen profielen worden geïdentificeerd aan de hand van de identiteit en het e-mailadres van het Experience Cloud. Door het schema voor profiel in te schakelen, zorgt u ervoor dat gegevens die zijn vastgelegd vanuit uw mobiele toepassing, worden toegevoegd aan het realtime-klantprofiel.

Naast gedragsgegevens kunt u ook profielkenmerkgegevens vastleggen vanuit uw mobiele toepassing (bijvoorbeeld gegevens over profielen die zijn geabonneerd op een nieuwsbrief).

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

Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web van Adobe Experience Platform en Mobiele SDKs. Bij het verzamelen van gegevens met de SDK&#39;s van Adobe Experience Platform worden gegevens naar de Adobe Experience Platform-Edge Network verzonden. Het is de gegevensstroom die bepaalt aan welke diensten dat de gegevens door:sturen.

In uw opstelling, wilt u de gegevens die u van mobiele app verzamelt worden verzonden naar uw dataset in Adobe Experience Platform.

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

Uw gegevensstroom is nu geconfigureerd om de gegevens die zijn verzameld in uw mobiele app door te sturen naar uw gegevensset in Adobe Experience Platform.

Zie [ Overzicht van gegevensstromen ](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html) voor meer informatie over hoe te om een gegevensstroom te vormen en hoe te om gevoelige gegevens te behandelen.



## Tags gebruiken

Als u code op uw site wilt implementeren om gegevens te verzamelen, gebruikt u de functie Codes in Adobe Experience Platform. Met deze oplossing voor tagbeheer kunt u code naast andere coderingsvereisten implementeren. Tags bieden naadloze integratie met Adobe Experience Platform met de Adobe Experience Platform Mobile SDK-extensie.

### Uw tag maken

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Tags]** within [!UICONTROL DATA COLLECTION] in het linkerspoor.

2. Selecteer **[!UICONTROL New Property]** .

   Geef de tag een naam, selecteer **[!UICONTROL Mobile]** . Selecteer **[!UICONTROL Save]** om door te gaan.

   ![ creeer een bezit ](./assets/create-mobile-property.png)

### Uw tag configureren

Nadat u de tag hebt gemaakt, moet u deze configureren met de juiste extensies en gegevenselementen en -regels configureren op basis van de manier waarop u uw site wilt bijhouden en gegevens naar Adobe Experience Platform wilt verzenden.

Als u de nieuwe tag wilt configureren, selecteert u deze in de lijst met [!UICONTROL Tag Properties] .


#### **Uitbreidingen**

Voeg de extensie Adobe Platform Edge Network toe aan de tag om ervoor te zorgen dat u gegevens naar Adobe Experience Platform kunt verzenden (via uw gegevensstroom).

U kunt als volgt de extensie Adobe Experience Platform Mobile SDK maken en configureren:

1. Selecteer **[!UICONTROL Extensions]** in het linkerspoor. U ziet dat de extensies Mobiele kern en Profiel al beschikbaar zijn.

1. Selecteer **[!UICONTROL Catalog]** in de bovenste balk.

1. Zoek naar of blader naar de extensie **[!UICONTROL Adobe Experience Platform Edge Network]** en selecteer **[!UICONTROL Install]** in het rechterdeelvenster om de extensie te installeren.

1. Selecteer de sandbox en de eerder gemaakte gegevensstroom voor de [!UICONTROL Production Environment] en (optioneel) [!UICONTROL Staging Environment] en [!UICONTROL Development Environment] .

   ![ AEP Mobiele de uitbreidingsconfiguratie van SDK ](./assets/aepmobilesdk-extension-datastream.png)

1. Voer de **[!UICONTROL Edge Network domain]** onderliggende waarde [!UICONTROL Domain configuration] in. Gebruik doorgaans `<organizationName>.data.adobedc.net` .

1. Selecteer **[!UICONTROL Save]** .

Zie [ de uitbreiding van de Edge Network van Adobe Experience Platform ](https://developer.adobe.com/client-sdks/documentation/edge-network) voor meer informatie vormen.

U wilt ook de volgende extra extensies instellen vanuit de catalogus:

- Identiteit.
- AEP Assurance.
- Toestemming.

Zie [ een markeringsbezit ](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/initial-configuration/configure-tags.html) in het Mobiele Leerprogramma van de App voor het platform van de Ervaring voor veel meer informatie over uitbreidingen en hun configuratie vormen.

#### **Elementen van Gegevens**

Gegevenselementen zijn de bouwstenen voor uw gegevenswoordenboek (of gegevenskaart). Gebruik gegevenselementen om gegevens te verzamelen, te organiseren en te leveren over marketing- en advertentietechnologie. U stelt gegevenselementen in uw tag in die gegevens of gebeurtenissen van mobiele apps lezen en die kunnen worden gebruikt om gegevens naar Adobe Experience Platform te verzenden.

U wilt bijvoorbeeld de naam van de provider verzamelen van de mobiele app.

Een gegevenselement met de naam van een drager definiëren:

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteer **[!UICONTROL Add Data Element]** .

3. In het dialoogvenster [!UICONTROL Create Data Element] :

   - Geef uw gegevenselement een naam, bijvoorbeeld `Carrier Name` .

   - Selecteer **[!UICONTROL Mobile Core]** in de lijst [!UICONTROL Extension] .

   - Selecteer **[!UICONTROL Carrier Name]** in de lijst [!UICONTROL Data Element Type] .


     ![ creeer het Element van de Datum gebruikend Info van de Pagina ](./assets/create-dataelement-mobile.png)

   - Selecteer **[!UICONTROL Save]** .

U kunt zoveel gegevenselementen maken als u wilt en deze gebruiken in regels.


#### **Regels**

Tags in Adobe Experience Platform volgen een op regels gebaseerd systeem. Zij zoeken gebruikersinteractie en bijbehorende gegevens. Wanneer aan de criteria die in uw regels worden geschetst wordt voldaan, teweegbrengt de regel de uitbreiding, het manuscript, of cliënt-zijcode in werking u identificeerde. U kunt regels gebruiken om gegevens (zoals een XDM-object) naar Adobe Experience Platform te verzenden met de extensie Adobe Experience Platform Edge Network.

U wilt bijvoorbeeld gebeurtenisgegevens verzenden wanneer de mobiele app wordt gebruikt (op de voorgrond) en wanneer de mobiele app niet wordt gebruikt (teruggeduwd naar de achtergrond).

Een regel definiëren:

1. Selecteer **[!UICONTROL Rules]** in het linkerspoor.

2. Selecteer **[!UICONTROL Create New Rule]** .

3. In het dialoogvenster [!UICONTROL Create Rule] :

   - Geef de regel een naam, bijvoorbeeld `Application Status` .

   - Selecteer **[!UICONTROL + Add]** onder [!UICONTROL Events] .

   - In het dialoogvenster [!UICONTROL Event Configuration] :

      - Selecteer **[!UICONTROL Mobile Core]** in de lijst [!UICONTROL Extension] .

      - Selecteer **[!UICONTROL Foreground]** in de lijst [!UICONTROL Event Type] .

      - Selecteer **[!UICONTROL Keep Changes]** .

   - Klik ![ plus ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_AddCircle_18_N.svg) naast [!UICONTROL Mobile Core - Foreground].

      - Selecteer **[!UICONTROL Mobile Core]** in de lijst [!UICONTROL Extension] .

      - Selecteer **[!UICONTROL Background]** in de lijst [!UICONTROL Event Type] .

      - Selecteer **[!UICONTROL Keep Changes]** .

   - Klik ![ plus ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_AddCircle_18_N.svg) toevoegen onder [!UICONTROL ACTIONS]. In het dialoogvenster [!UICONTROL Action Configuration] :

      - Selecteer **[!UICONTROL Adobe Experience Platform Edge Network]** in de lijst [!UICONTROL Extension] .

      - Selecteer **[!UICONTROL Forward event to Edge Network]** in de lijst [!UICONTROL Action Type] .

      - Selecteer **[!UICONTROL Keep Changes]** .

   - Uw regel moet er als volgt uitzien:

     ![ creeer Regel ](assets/rule-appstatus.png)

   - Selecteer **[!UICONTROL Save]** .

Het bovenstaande is slechts een voorbeeld van het definiëren van een regel die XDM-gegevens met toepassingsstatus naar het Adobe Edge-netwerk en naar Adobe Experience Platform verzendt.

U kunt regels op verschillende manieren in uw tag gebruiken om variabelen te bewerken (met behulp van uw gegevenselementen).

Zie [ Regels ](https://developer.adobe.com/client-sdks/documentation/lifecycle-for-edge-network/#configure-a-rule-to-forward-lifecycle-metrics-to-platform) voor meer informatie.

### Uw tag maken en Publish

Nadat u gegevenselementen en regels hebt gedefinieerd, moet u de tag maken en publiceren. Wanneer u een bibliotheek maakt, moet u deze toewijzen aan een omgeving. De uitbreidingen, de regels, en de gegevenselementen van de bouwstijl worden dan gecompileerd en in het toegewezen milieu geplaatst. Elke omgeving bevat een unieke insluitcode waarmee u de toegewezen build in uw site kunt integreren.

Om uw markering te bouwen en te publiceren:

1. Selecteer **[!UICONTROL Publishing Flow]** in het linkerspoor.

2. Selecteer **[!UICONTROL Select a working library]** , gevolgd door **[!UICONTROL Add Library…]** .

3. In het dialoogvenster [!UICONTROL Create Library] :

   - Geef de bibliotheek een naam.

   - Selecteer **[!UICONTROL Development (development)]** in de lijst [!UICONTROL Environment] .

   - Selecteer **[!UICONTROL + Add All Changed Resources]** .

     ![ Publish - creeer Bibliotheek ](./assets/build-library-mobile.png)

   - Selecteer **[!UICONTROL Save & Build to Development]** .

   Uw tag wordt opgeslagen en gemaakt voor uw ontwikkelomgeving. Een groene stip geeft aan dat uw tag met succes is opgebouwd in uw ontwikkelomgeving.

4. U kunt **[!UICONTROL ...]** selecteren om de bibliotheek opnieuw samen te stellen of de bibliotheek naar een testomgeving of productieomgeving te verplaatsen.

Adobe Experience Platform-tags bieden ondersteuning voor eenvoudige tot complexe publicatieworkflows die geschikt zijn voor uw implementatie van de Adobe Experience Platform-Edge Network.

Zie [ het Publiceren overzicht ](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/#publish-the-configuration) voor meer informatie.


### De tagcode ophalen

Tot slot moet u uw tag gebruiken in de mobiele app die u wilt bijhouden.

U kunt als volgt code-instructies opvragen waarin wordt uitgelegd hoe u uw mobiele app instelt en uw tag in de app gebruikt:

1. Selecteer **[!UICONTROL Environments]** in het linkerspoor.

2. Van de lijst van milieu&#39;s, selecteer correcte installeer ![ doos ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Box_18_N.svg) knoop.

   Selecteer in het dialoogvenster [!UICONTROL Mobile Install Instructions] het juiste platform ( [!UICONTROL iOS] , [!UICONTROL Android] ). Dan gebruik het exemplaar ![ exemplaar ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Copy_18_N.svg) knoop naast elk van de relevante codefragmenten die u aan opstelling wilt gebruiken en uw mobiele app initialiseren:

   ![ Milieu ](./assets/environment-mobile.png)

3. Selecteer **[!UICONTROL Close]** .

In plaats van de code voor de ontwikkelomgeving, had u een andere omgeving (staging, productie) kunnen selecteren op basis van waar u bezig bent met het implementeren van de Adobe Experience Platform Mobile SDK.

Zie [ Milieu&#39;s ](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?) voor meer informatie.

## Implementeren en valideren

U kunt de code nu implementeren in uw mobiele app. Wanneer deze wordt geïmplementeerd, begint uw mobiele app gegevens te verzamelen in Adobe Experience Platform.

Valideer uw implementatie, verbeter het waar nodig, en zodra correct, stel het in uw het opvoeren en productiemilieu gebruikend de het publiceren werkschemafunctie van Markeringen op.

Zie [ Adobe Experience Cloud in mobiele apps uitvoeren zelfstudie ](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/overview.html) voor veel meer gedetailleerde informatie.

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

   - Selecteer datasets die u eerder hebt gemaakt en/of andere relevante datasets die u wilt opnemen in uw verbinding (bijvoorbeeld Gegevens van gebeurtenissen voor het bijhouden van push-ervaringen en gegevens van het pushprofiel uit Adobe Journey Optimizer)

     ![ voeg datasets ](./assets/cja-connections-ajopush.png) toe

   - Selecteer **[!UICONTROL Next]** .

   In de stap [!UICONTROL Datasets settings] in [!UICONTROL Add datasets] :

   - Voor elke gegevensset:

      - Selecteer een [!UICONTROL Person ID] van de beschikbare identiteiten die in de datasetschema&#39;s in Adobe Experience Platform worden bepaald.

      - Selecteer de juiste gegevensbron in de lijst [!UICONTROL Data source type] . Als u **[!UICONTROL Other]** opgeeft, voegt u een beschrijving voor de gegevensbron toe.

      - Stel **[!UICONTROL Import all new data]** en **[!UICONTROL Dataset backfill existing data]** in op basis van uw voorkeuren.

     ![ vorm datasets ](./assets/cja-connections-ajopushid.png)

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

   ![ de meningscomponenten van Gegevens ](./assets/cja-dataview-2-mobile.png)

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

5. Als u uw eerste rapport wilt maken, sleept u de afmetingen en metriek op de [!UICONTROL Freeform table] in de [!UICONTROL Panel] . Sleep bijvoorbeeld `Events` als metriek en `Push Title` als dimensie, uitgesplitst naar `Event Type` voor een overzicht van uw pushberichten voor uw mobiele app en wat er met hen is gebeurd.

   ![ Workspace - Eerste Rapport ](./assets/cja-projects-5-mobile.png)

Zie [ overzicht van Analysis Workspace ](../analysis-workspace/home.md) voor meer informatie over hoe te om projecten tot stand te brengen en uw analyse te bouwen gebruikend componenten, visualisaties, en panelen.

>[!SUCCESS]
>
>U hebt alle stappen uitgevoerd. Beginnend door te bepalen welke gegevens u (schema) wilt verzamelen en waar om het (dataset) in Adobe Experience Platform op te slaan, vormde u een gegevensstroom op de Edge Network om ervoor te zorgen dat de gegevens aan die dataset kunnen door:sturen. Vervolgens hebt u de tag gedefinieerd en geïmplementeerd die de extensies (Adobe Experience Platform Edge Network en andere), gegevenselementen en regels bevat voor het vastleggen van gegevens van uw mobiele app en het verzenden van die gegevens naar uw gegevensstroom. U hebt een verbinding in Customer Journey Analytics gedefinieerd om gegevens voor het bijhouden van pushmeldingen voor uw mobiele app en andere gegevens te gebruiken. Met de definitie van uw gegevensweergave kunt u opgeven welke dimensie en metriek u wilt gebruiken. Ten slotte hebt u uw eerste project gemaakt waarmee u uw gegevens van uw mobiele app kunt visualiseren en analyseren.
