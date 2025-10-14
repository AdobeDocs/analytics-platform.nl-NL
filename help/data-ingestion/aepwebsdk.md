---
title: Gegevens verzamelen via de Adobe Experience Platform Web SDK
description: Uitleggen hoe gegevens in Customer Journey Analytics kunnen worden ingevoerd via de Adobe Experience Platform Web SDK en de Edge Network
solution: Customer Journey Analytics
feature: Basics
exl-id: 0b595e9e-0dcf-4c70-ac6d-5a2322824328
role: Admin
source-git-commit: bc2c959497230d7672d43d5cd409ca62d4627d6a
workflow-type: tm+mt
source-wordcount: '3222'
ht-degree: 0%

---

# Gegevens via Web SDK invoegen

In deze snelstartgids wordt uitgelegd hoe u gegevens voor het bijhouden van websites rechtstreeks in Adobe Experience Platform kunt invoeren met Adobe Experience Platform Web SDK en Edge Network en deze gegevens vervolgens kunt gebruiken in Customer Journey Analytics.

Hiervoor moet u:

- **opstelling een schema en dataset** in Adobe Experience Platform om het model (schema) van de gegevens te bepalen die u wilt verzamelen en waar te om de gegevens (dataset) eigenlijk te verzamelen.

- **opstelling een datastream** om Adobe Experience Platform Edge Network te vormen om uw verzamelde gegevens aan de dataset te leiden u in Adobe Experience Platform vormde.

- **Markeringen van het Gebruik** om regels en gegevenselementen tegen de gegevens in uw gegevenslaag op uw website gemakkelijk te vormen. Dan zorg ervoor dat de gegevens naar de datastream worden verzonden die op Adobe Experience Platform Edge Network wordt gevormd.

- **stelt en bevestigt** op. Zorg voor een omgeving waarin u de ontwikkeling van tags kunt doorlopen en publiceer deze live in uw productieomgeving als alles is gevalideerd.

- **opstelling een verbinding** in Customer Journey Analytics. Deze verbinding zou (minstens) uw dataset van Adobe Experience Platform moeten omvatten.

- **opstelling een gegevensmening** in Customer Journey Analytics om metriek en afmeting te bepalen die u in Analysis Workspace wilt gebruiken.

- **opstelling een project** in Customer Journey Analytics om uw rapporten en visualisaties te bouwen.

>[!NOTE]
>
> Deze handleiding voor snel starten is een vereenvoudigde gids voor het invoeren van gegevens die van uw site zijn verzameld in Adobe Experience Platform en voor gebruik in Customer Journey Analytics. Het wordt ten zeerste aanbevolen de aanvullende informatie te bestuderen wanneer deze wordt vermeld.


## Een schema en gegevensset instellen

Als u gegevens in Adobe Experience Platform wilt invoeren, moet u eerst definiëren welke gegevens u wilt verzamelen. Alle gegevens die in Adobe Experience Platform worden ingevoerd, moeten voldoen aan een standaard, gedenormaliseerde structuur, zodat deze kan worden herkend en kan worden toegepast door de mogelijkheden en functies op de downstreammarkt. Het Model van Gegevens van de ervaring (XDM) is het standaardkader dat deze structuur in de vorm van schema&#39;s verstrekt.

Zodra u een schema hebt bepaald, gebruikt u één of meerdere datasets om de inzameling van gegevens op te slaan en te beheren. Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens (typisch een lijst) die een schema (kolommen) en gebieden (rijen) bevat.

Alle gegevens die in Adobe Experience Platform worden opgenomen moeten met een vooraf gedefinieerd schema in overeenstemming zijn alvorens het als dataset kan worden voortgeduurd.

### Een schema instellen

U wilt enkele minimale gegevens bijhouden van profielen die uw website bezoeken, zoals paginanaam, identificatie.
U moet eerst een schema definiëren dat deze gegevens modelleert.

Uw schema instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Schemas]** within [!UICONTROL DATA MANAGEMENT] in het linkerspoor.

1. Selecteer **[!UICONTROL Create schema]** .
.
1. In Uitgezocht een klassenstap van de Create schematovenaar:

   1. Selecteer **[!UICONTROL Experience Event]** .

      ![&#x200B; creeer een schema dat de Gebeurtenis van de Ervaring benadrukt &#x200B;](./assets/create-ee-schema-wizard-step-1.png)

      >[!INFO]
      >
      >    Een schema van de Gebeurtenis van de Ervaring wordt gebruikt om het _gedrag_ van een profiel (als scènenaam, drukknop te modelleren om aan wagentje toe te voegen). Een individueel schema van het Profiel wordt gebruikt om de profiel _attributen_ (zoals naam, e-mail, geslacht) te modelleren.

   1. Selecteer **[!UICONTROL Next]** .


1. In het gedeelte [!UICONTROL Name and review step] van de wizard [!UICONTROL Create schema] :

   1. Voer een **[!UICONTROL Schema display name]** in voor uw schema en (optioneel) een **[!UICONTROL Description]** .

      ![&#x200B; creeer schemavenster dat de Naam toont uw schemagebieden &#x200B;](./assets/create-ee-schema-wizard-step-2.png)

   1. Selecteer **[!UICONTROL Finish]** .

1. Op het tabblad Structuur van het voorbeeldschema:

   1. Selecteer **[!UICONTROL + Add]** in [!UICONTROL Field groups] .

      ![&#x200B; voeg gebiedsgroep &#x200B;](./assets/add-field-group-button.png) toe

      Veldgroepen zijn herbruikbare verzamelingen van objecten en kenmerken waarmee u het schema eenvoudig kunt uitbreiden.

   1. Selecteer in het dialoogvenster [!UICONTROL Add fields groups] de veldgroep **[!UICONTROL AEP Web SDK ExperienceEvent]** in de lijst.

      ![&#x200B; AEP Web SDK ExperienceEvent gebiedsgroup &#x200B;](./assets/select-aepwebsdk-experienceevent.png)

      U kunt de voorvertoningsknop selecteren om een voorvertoning weer te geven van de velden die deel uitmaken van deze veldgroep, bijvoorbeeld `web > webPageDetails > name` .

      ![&#x200B; AEP Web SDK ExperienceEvent gebiedsgroepvoorproef &#x200B;](./assets/aepwebsdk-experiencevent-preview.png)

      Selecteer **[!UICONTROL Back]** om de voorvertoning te sluiten.

   1. Selecteer **[!UICONTROL Add field groups]** .

1. Selecteer **[!UICONTROL +]** naast de naam van het schema in het deelvenster [!UICONTROL Structure] .

   ![&#x200B; het Schema van het Voorbeeld voegt de knoop van het Gebied toe &#x200B;](./assets/example-schema-plus.png)

1. Typ in het deelvenster [!UICONTROL Field Properties] `Identification` als de naam, **[!UICONTROL Identification]** als de [!UICONTROL Display name] , selecteer **[!UICONTROL Object]** als de [!UICONTROL Type] en selecteer **[!UICONTROL ExperienceEvent Core v2.1]** als de [!UICONTROL Field Group] .

   >[!NOTE]
   >
   >Als die veldgroep niet beschikbaar is, zoekt u naar een andere veldgroep met identiteitsvelden. Of [&#x200B; creeer een nieuwe gebiedsgroep &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/field-groups.html?lang=nl-NL) en [&#x200B; voeg nieuwe identiteitsgebieden &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/fields/identity.html?lang=nl-NL#define-a-identity-field) (als `ecid`, `crmId`, en anderen toe u) aan de gebiedsgroep nodig hebt en selecteer die nieuwe gebiedsgroep.

   ![&#x200B; Voorwerp van de Identificatie &#x200B;](./assets/identification-field.png)

   Het identificatieobject voegt id-mogelijkheden toe aan uw schema. In uw geval wilt u profielen identificeren die uw site bezoeken met de Experience Cloud-id en het e-mailadres. Er zijn vele andere eigenschappen beschikbaar om de identificatie van uw persoon te volgen (bijvoorbeeld klant identiteitskaart, loyalty identiteitskaart).

   Selecteer **[!UICONTROL Apply]** om dit object aan uw schema toe te voegen.

1. Selecteer het veld **[!UICONTROL ecid]** in het identificatieobject dat u net hebt toegevoegd en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Primary Identity]** en **[!UICONTROL ECID]** in de lijst [!UICONTROL Identity namespace] in het rechterdeelvenster.

   ![&#x200B; specificeer ECID als identiteit &#x200B;](./assets/specify-identity.png)

   U geeft de Experience Cloud Identity op als de primaire identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen met dezelfde ECID te combineren (aansluiten).

   Selecteer **[!UICONTROL Apply]** . U ziet dat er een vingerafdrukpictogram wordt weergegeven in het ecid-kenmerk.

1. Selecteer het veld **[!UICONTROL email]** in het identificatieobject dat u net hebt toegevoegd en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Email]** in de lijst [!UICONTROL Identity namespace] in het deelvenster [!UICONTROL Field Properties] .

   ![&#x200B; specificeer e-mail als identiteit &#x200B;](./assets/specify-email-identity.png)

   U geeft het e-mailadres op als een andere identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (naaien).

   Selecteer **[!UICONTROL Apply]** . U ziet dat er een vingerafdrukpictogram wordt weergegeven in het e-mailkenmerk.

   Selecteer **[!UICONTROL Save]** .

1. Selecteer het hoofdelement van het schema met de naam van het schema en selecteer vervolgens de **[!UICONTROL Profile]** switch.

   U wordt gevraagd het schema in te schakelen voor het profiel. Zodra toegelaten, wanneer het gegeven in datasets wordt opgenomen die op dit schema worden gebaseerd, worden die gegevens samengevoegd in het Real-Time Profiel van de Klant.

   Zie [&#x200B; het schema voor gebruik in het Profiel van de Klant in real time &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=nl-NL#profile) voor meer informatie toelaten.

   >[!IMPORTANT]
   >
   >    Nadat u een schema hebt opgeslagen dat is ingeschakeld voor profiel, kan het niet meer worden uitgeschakeld voor profiel.

   ![&#x200B; laat schema voor profiel &#x200B;](./assets/enable-for-profile.png) toe

1. Selecteer **[!UICONTROL Save]** om het schema op te slaan.

U hebt een minimumschema gemaakt dat de gegevens modelleert die u van uw website kunt vastleggen. In het schema kunnen profielen worden geïdentificeerd met Experience Cloud Identity en e-mailadres. Door het schema voor profiel in te schakelen, zorgt u ervoor dat gegevens die vanaf uw website zijn vastgelegd, worden toegevoegd aan het realtime-klantprofiel.

Naast gedragsgegevens kunt u ook profielkenmerkgegevens van uw site vastleggen (bijvoorbeeld gegevens over profielen die zijn geabonneerd op een nieuwsbrief).

Als u deze profielgegevens wilt vastleggen, doet u het volgende:

- Maak een schema op basis van de klasse Individueel profiel XDM.

- Voeg de het gebiedsgroep van de Kern van het Profiel v2 aan het schema toe.

- Voeg een identificatieobject toe op basis van de veldgroep Profile Core v2.

- Experience Cloud-id definiëren als primaire id en e-mailadres als id.

- Het schema inschakelen voor profiel

Zie [&#x200B; schema&#39;s in UI &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=nl-NL) voor meer informatie creëren en uitgeven bij het toevoegen van en het verwijderen van gebiedsgroepen en individuele gebieden aan een schema.

### Een gegevensset instellen

Met uw schema, hebt u uw gegevensmodel bepaald. U moet nu de constructie bepalen om die gegevens op te slaan en te beheren, die door datasets wordt gedaan.

Uw gegevensset instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Datasets]** within [!UICONTROL DATA MANAGEMENT] in het linkerspoor.

2. Selecteer **[!UICONTROL Create dataset]** .

   ![&#x200B; creeer dataset &#x200B;](./assets/create-dataset.png)

3. Selecteer **[!UICONTROL Create dataset from schema]** .

   ![&#x200B; creeer dataset van schema &#x200B;](./assets/create-dataset-from-schema.png)

4. Selecteer het schema dat u eerder hebt gemaakt en selecteer **[!UICONTROL Next]** .

5. Geef uw gegevensset een naam en (optioneel) geef een beschrijving op.

   ![&#x200B; dataset van de Naam &#x200B;](./assets/name-your-datatest.png)

6. Selecteer **[!UICONTROL Finish]** .

7. Selecteer de **[!UICONTROL Profile]** schakelaar.

   U wordt ertoe aangezet om de dataset voor profiel toe te laten. Zodra toegelaten, verrijkt de dataset klantenprofielen in real time met zijn opgenomen gegevens.

   >[!IMPORTANT]
   >
   >    U kunt een dataset voor profiel slechts toelaten wanneer het schema, waaraan de dataset voldoet, ook voor profiel wordt toegelaten.

   ![&#x200B; laat schema voor profiel &#x200B;](./assets/aepwebsdk-dataset-profile.png) toe

Zie {de gids UI van de Datasets van 0} [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=nl) voor veel meer informatie over hoe te bekijken, voorproef, tot stand brengen, een dataset schrappen.  En hoe te om een dataset voor het Profiel van de Klant in real time toe te laten.

## Een gegevensstroom instellen

Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web van Adobe Experience Platform en Mobiele SDKs. Bij het verzamelen van gegevens met de SDK&#39;s van Adobe Experience Platform worden gegevens naar de Adobe Experience Platform Edge Network verzonden. Het is de gegevensstroom die bepaalt aan welke diensten dat de gegevens door:sturen.

In uw opstelling, wilt u de gegevens die u van de website verzamelt worden verzonden naar uw dataset in Adobe Experience Platform.

Uw gegevensstroom instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform **[!UICONTROL Datastreams]** in [!UICONTROL DATA COLLECTION] in de linkertrack.

2. Selecteer **[!UICONTROL New Datastream]** .

3. Geef een naam en beschrijf de gegevensstroom. Selecteer het schema in de lijst [!UICONTROL Event Schema] .

   ![&#x200B; Nieuwe DataStream &#x200B;](./assets/new-datastream.png)

4. Selecteer **[!UICONTROL Save]** .

5. Selecteer **[!UICONTROL Add Service]** .

6. In de lus [!UICONTROL Add Service screen] :

   1. Selecteer **[!UICONTROL Adobe Experience Platform]** in de lijst [!UICONTROL Service] .

   2. Zorg ervoor dat **[!UICONTROL Enabled]** is geselecteerd.

   3. Selecteer de gegevensset in de lijst [!UICONTROL Event Dataset] .

      ![&#x200B; De dienst van AEP DataStream &#x200B;](./assets/datastream-aep-service.png)

   4. Laat de andere instellingen staan en selecteer **[!UICONTROL Save]** om de gegevensstroom op te slaan.

Uw gegevensstroom is nu geconfigureerd om de gegevens die van uw website zijn verzameld door te sturen naar uw gegevensset in Adobe Experience Platform.

Zie [&#x200B; Overzicht van gegevensstromen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=nl-NL) voor meer informatie over hoe te om een gegevensstroom te vormen en hoe te om gevoelige gegevens te behandelen.



## Tags gebruiken

Als u code op uw site wilt implementeren om gegevens daadwerkelijk te verzamelen, gebruikt u de functie Codes in Adobe Experience Platform. Met deze oplossing voor tagbeheer kunt u code naast andere coderingsvereisten implementeren. Tags bieden naadloze integratie met Adobe Experience Platform via de Adobe Experience Platform Web SDK-extensie.

### Uw tag maken

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Tags]** within [!UICONTROL DATA COLLECTION] in het linkerspoor.

2. Selecteer **[!UICONTROL New Property]** .

   Geef de tag een naam, selecteer **[!UICONTROL Web]** en voer een domeinnaam in. Selecteer **[!UICONTROL Save]** om door te gaan.

   ![&#x200B; creeer een bezit &#x200B;](./assets/create-property.png)

### Uw tag configureren

Nadat u de tag hebt gemaakt, moet u deze configureren met de juiste extensies en gegevenselementen en -regels configureren op basis van de manier waarop u uw site wilt bijhouden en gegevens naar Adobe Experience Platform wilt verzenden.

Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om deze te openen.


#### **Uitbreidingen**

Om ervoor te zorgen dat u gegevens naar Adobe Experience Platform kunt verzenden (via uw gegevensstroom), voegt u de extensie Adobe Platform Web SDK toe aan uw tag.

U kunt als volgt de Adobe Experience Platform Web SDK-extensie maken en configureren:

1. Selecteer **[!UICONTROL Extensions]** in het linkerspoor.

2. Selecteer **[!UICONTROL Catalog]** in de bovenste balk.

3. Zoek of blader naar de extensie Adobe Experience Platform Web SDK en selecteer **[!UICONTROL Install]** om de extensie te installeren.

   <img src="./assets/aepwebsdk-extension.png" width="35%"/>

4. Selecteer de sandbox en de eerder gemaakte gegevensstroom voor de [!UICONTROL Production Environment] en (optioneel) [!UICONTROL Staging Environment] en [!UICONTROL Development Environment] .

   ![&#x200B; de uitbreidingsconfiguratie van SDK van het Web van AEP &#x200B;](./assets/aepwebsk-extension-datastreams.png)

   Selecteer **[!UICONTROL Save]** .

Zie [&#x200B; de uitbreiding van SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=nl-NL) voor meer informatie vormen.

De Web SDK omvat [!UICONTROL Adobe Experience Cloud ID Service] native, zodat te hoeven u niet om de de dienstuitbreiding van identiteitskaart aan uw markering toe te voegen.

#### **Elementen van Gegevens**

Gegevenselementen zijn de bouwstenen voor uw gegevenswoordenboek (of gegevenskaart). Gebruik gegevenselementen om gegevens te verzamelen, te organiseren en te leveren over marketing- en advertentietechnologie. U stelt gegevenselementen in uw tag in die worden gelezen van uw gegevenslaag en die kunnen worden gebruikt om gegevens naar Adobe Experience Platform te verzenden.

Er zijn verschillende typen gegevenselementen. U stelt eerst een gegevenselement in om de paginanaam vast te leggen die personen op uw site bekijken.

Een gegevenselement voor de paginanaam definiëren:

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteer **[!UICONTROL Add Data Element]** .

3. In het dialoogvenster [!UICONTROL Create Data Element] :

   - Geef uw gegevenselement een naam, bijvoorbeeld `Page Name` .

   - Selecteer **[!UICONTROL Core]** in de lijst [!UICONTROL Extension] .

   - Selecteer **[!UICONTROL Page Info]** in de lijst [!UICONTROL Data Element Type] .

   - Selecteer **[!UICONTROL Title]** in de lijst [!UICONTROL Attribute] .

     ![&#x200B; creeer het Element van de Datum gebruikend Info van de Pagina &#x200B;](./assets/create-dataelement-1.png)

     U had ook de waarde van een variabele in uw gegevenslaag kunnen gebruiken, bijvoorbeeld `pageName` en het gegevenstype [!UICONTROL JavaScript Variable] voor gegevenselementen om het gegevenselement te definiëren.

     ![&#x200B; creeer het Element van Gegevens gebruikend Variabele JavaScript &#x200B;](./assets/create-dataelement-2.png)

   - Selecteer **[!UICONTROL Save]** .

U wilt nu een gegevenselement instellen dat verwijst naar de Experience Cloud-id die automatisch wordt verstrekt door de Adobe Experience Platform Web SDK en beschikbaar is via de Experience Cloud ID Service-extensie.

Een ECID-gegevenselement definiëren:

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteer **[!UICONTROL Add Data Element]** .

3. In het dialoogvenster [!UICONTROL Create Data Element] :

   - Geef uw gegevenselement een naam, bijvoorbeeld `ECID` .

   - Selecteer **[!UICONTROL Experience Cloud ID Service]** in de lijst [!UICONTROL Extension] .

   - Selecteer **[!UICONTROL ECID]** in de lijst [!UICONTROL Data Element Type] .

     ![&#x200B; ECID het Element van Gegevens &#x200B;](./assets/ecid-dataelement.png)

   - Selecteer **[!UICONTROL Save]** .

Tot slot wilt u nu om het even welke specifieke gegevenselementen aan het schema in kaart brengen u vroeger bepaalde. U definieert een ander gegevenselement dat een representatie van uw XDM-schema biedt.

Een XDM-objectelement definiëren:

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteer **[!UICONTROL Add Data Element]** .

3. In het dialoogvenster [!UICONTROL Create Data Element] :

   - Geef uw gegevenselement een naam, bijvoorbeeld `XDM - Page View` .

   - Selecteer **[!UICONTROL Adobe Experience Platform Web SDK]** in de lijst [!UICONTROL Extension] .

   - Selecteer **[!UICONTROL XDM Object]** in de lijst [!UICONTROL Data Element Type] .

   - Selecteer de sandbox in de lijst [!UICONTROL Sandbox] .

   - Selecteer het schema in de lijst [!UICONTROL Schema] .

   - Wijs het kenmerk `identification > core > ecid`, dat in uw schema is gedefinieerd, toe aan het gegevenselement ECID. Selecteer het cilinderpictogram om het ECID-gegevenselement gemakkelijk te kiezen in de lijst met gegevenselementen.

     ![&#x200B; Uitgezocht ECID het Element van Gegevens &#x200B;](./assets/pick-ecid-dataelement.png)

     ![&#x200B; het Element van Gegevens van de Kaart ECID &#x200B;](./assets/map-ecid.png)


   - Wijs het kenmerk `web > webPageDetails > name`, dat in uw schema is gedefinieerd, toe aan het gegevenselement Paginanaam.

     ![&#x200B; het Element van de Gegevens van de Naam van de Pagina van de Kaart &#x200B;](./assets/map-pagename.png)

   - Selecteer **[!UICONTROL Save]** .


#### **Regels**

Tags in Adobe Experience Platform volgen een op regels gebaseerd systeem. Zij zoeken gebruikersinteractie en bijbehorende gegevens. Wanneer aan de criteria die in uw regels worden geschetst wordt voldaan, teweegbrengt de regel de uitbreiding, het manuscript, of cliënt-zijcode in werking u identificeerde. U kunt regels gebruiken om gegevens (zoals een voorwerp XDM) naar Adobe Experience Platform te verzenden gebruikend de uitbreiding van SDK van het Web van Adobe Experience Platform.

Een regel definiëren:

1. Selecteer **[!UICONTROL Rules]** in het linkerspoor.

2. Selecteer **[!UICONTROL Create New Rule]** .

3. In het dialoogvenster [!UICONTROL Create Rule] :

   - Geef de regel een naam, bijvoorbeeld `Page View` .

   - Selecteer **[!UICONTROL + Add]** onder [!UICONTROL Events] .

   - In het dialoogvenster [!UICONTROL Event Configuration] :

      - Selecteer **[!UICONTROL Core]** in de lijst [!UICONTROL Extension] .

      - Selecteer **[!UICONTROL Window Loaded]** in de lijst [!UICONTROL Event Type] .

        ![&#x200B; Regel - de Configuratie van de Gebeurtenis &#x200B;](./assets/event-windowloaded-pageview.png)

      - Selecteer **[!UICONTROL Keep Changes]** .



   - Selecteer **[!UICONTROL + Add]** onder [!UICONTROL Actions] .

   - In het dialoogvenster [!UICONTROL Action Configuration] :

      - Selecteer **[!UICONTROL Adobe Experience Platform Web SDK]** in de lijst [!UICONTROL Extension] .

      - Selecteer **[!UICONTROL Send Event]** in de lijst [!UICONTROL Action Type] .

      - Selecteer **[!UICONTROL web.webpagedetails.pageViews]** in de lijst [!UICONTROL Type] .

      - Selecteer het cilinderpictogram naast [!UICONTROL XDM data] en selecteer **[!UICONTROL XDM - Page View]** in de lijst met gegevenselementen.

     ![&#x200B; Regel - de Configuratie van de Actie &#x200B;](./assets/action-pageview-xdm.png)

      - Selecteer **[!UICONTROL Keep Changes]** .

   - Uw regel moet er als volgt uitzien:

     ![&#x200B; creeer Regel &#x200B;](assets/rule-pageview.png)

   - Selecteer **[!UICONTROL Save]** .

Het bovenstaande is slechts een voorbeeld van het definiëren van een regel die XDM-gegevens met waarden uit andere gegevenselementen naar Adobe Experience Platform verzendt.

U kunt regels op verschillende manieren in uw tag gebruiken om variabelen te bewerken (met behulp van uw gegevenselementen).

Zie [&#x200B; Regels &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=nl-NL) voor meer informatie.

### Uw tag maken en publiceren

Nadat u gegevenselementen en regels hebt gedefinieerd, moet u de tag maken en publiceren. Wanneer u een bibliotheek maakt, moet u deze toewijzen aan een omgeving. De uitbreidingen, de regels, en de gegevenselementen van de bouwstijl worden dan gecompileerd en in het toegewezen milieu geplaatst. Elke omgeving bevat een unieke insluitcode waarmee u de toegewezen build in uw site kunt integreren.

Om uw markering te bouwen en te publiceren:

1. Selecteer **[!UICONTROL Publishing Flow]** in het linkerspoor.

2. Selecteer **[!UICONTROL Select a working library]** , gevolgd door **[!UICONTROL Add Library…]** .

3. In het dialoogvenster [!UICONTROL Create Library] :

   - Geef de bibliotheek een naam.

   - Selecteer **[!UICONTROL Development (development)]** in de lijst [!UICONTROL Environment] .

   - Selecteer **[!UICONTROL + Add All Changed Resources]** .

     ![&#x200B; publiceer - creeer Bibliotheek &#x200B;](./assets/create-library-aep.png)

   - Selecteer **[!UICONTROL Save & Build to Development]** .

   Uw tag wordt opgeslagen en gemaakt voor uw ontwikkelomgeving. Een groene stip geeft aan dat uw tag met succes is opgebouwd in uw ontwikkelomgeving.

4. U kunt **[!UICONTROL ...]** selecteren om de bibliotheek opnieuw samen te stellen of de bibliotheek naar een testomgeving of productieomgeving te verplaatsen.

   ![&#x200B; publiceer - bouwt Bibliotheek &#x200B;](./assets/build-library.png)

Adobe Experience Platform-tags ondersteunen eenvoudige tot complexe publicatieworkflows die geschikt zijn voor uw implementatie van Adobe Experience Platform Web SDK.

Zie [&#x200B; het Publiceren overzicht &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=nl-NL) voor meer informatie.


### De tagcode ophalen

Tot slot moet u de tag installeren op de website die u wilt bijhouden. Dit houdt in dat code in de kopteksttag van de sjabloon van uw website wordt geplaatst.

De code ophalen die naar de tag verwijst:

1. Selecteer **[!UICONTROL Environments]** in het linkerspoor.

2. Selecteer de juiste installatieknop in de lijst met omgevingen.

   Selecteer in het dialoogvenster [!UICONTROL Web Install Instructions] de knop Kopiëren naast de scriptcode die als volgt moet worden gelezen:

   ```
   <script src="https://assets.adobedtm.com/2a518741ab24/.../launch-...-development.min.js" async></script>>
   ```

   ![&#x200B; Milieu &#x200B;](./assets/environment.png)

3. Selecteer **[!UICONTROL Close]** .

In plaats van de code voor de ontwikkelomgeving, zou u een andere omgeving (het opvoeren, de productie) kunnen selecteren die op waar wordt gebaseerd u bezig bent om het Web SDK van Adobe Experience Platform op te stellen.

Zie [&#x200B; Milieu&#39;s &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?lang=nl-NL&) voor meer informatie.

## Implementeren en valideren

U kunt de code nu implementeren in de ontwikkelingsversie van uw website binnen de tag `<head>` . Wanneer uw website wordt geïmplementeerd, worden gegevens verzameld in Adobe Experience Platform.

Valideer uw implementatie, verbeter het waar nodig, en zodra correct, stel het in uw het opvoeren en productiemilieu gebruikend de het publiceren werkschemafunctie van Markeringen op.

## Een verbinding instellen

Als u de Adobe Experience Platform-gegevens in Customer Journey Analytics wilt gebruiken, maakt u een verbinding die de gegevens bevat die het resultaat zijn van het instellen van het schema, de gegevensset en de workflow.

Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over deze datasets te rapporteren, moet u eerst een verband tussen datasets in Adobe Experience Platform en Workspace vestigen.

Om uw verbinding tot stand te brengen:

1. Selecteer in de gebruikersinterface van Customer Journey Analytics de optie **[!UICONTROL Connections]** (optioneel in **[!UICONTROL Data management]** ) in het bovenste menu.

2. Selecteer **[!UICONTROL Create new connection]** .

3. In het [!UICONTROL Untitled connection] -scherm:

   Geef een naam en beschrijf de verbinding in [!UICONTROL Connection Settings] .

   Selecteer de juiste sandbox in de lijst [!UICONTROL Sandbox] in [!UICONTROL Data settings] en selecteer het aantal dagelijkse gebeurtenissen in de lijst [!UICONTROL Average number of daily events] .

   ![&#x200B; de Montages van de Verbinding &#x200B;](./assets/cja-connections-1.png)

   Selecteer **[!UICONTROL Add datasets]** .

   In de stap [!UICONTROL Select datasets] in [!UICONTROL Add datasets] :

   - Selecteer de dataset die u vroeger (`Example dataset`) creeerde en om het even welke andere dataset u in uw verbinding wilt omvatten.

     ![&#x200B; voeg datasets &#x200B;](./assets/cja-connections-2b.png) toe

   - Selecteer **[!UICONTROL Next]** .

   In de stap [!UICONTROL Datasets settings] in [!UICONTROL Add datasets] :

   - Voor elke gegevensset:

      - Selecteer een [!UICONTROL Person ID] van de beschikbare identiteiten die in de datasetschema&#39;s in Adobe Experience Platform worden bepaald.

      - Selecteer de juiste gegevensbron in de lijst [!UICONTROL Data source type] . Als u **[!UICONTROL Other]** opgeeft, voegt u een beschrijving voor de gegevensbron toe.

      - Stel **[!UICONTROL Import all new data]** en **[!UICONTROL Dataset backfill existing data]** in op basis van uw voorkeuren.

     ![&#x200B; vorm datasets &#x200B;](./assets/cja-connections-3b.png)

   - Selecteer **[!UICONTROL Add datasets]** .

   Selecteer **[!UICONTROL Save]** .

Zie [&#x200B; Overzicht van Verbindingen &#x200B;](../connections/overview.md) voor meer informatie over om een verbinding tot stand te brengen en te beheren en datasets te selecteren en te combineren.

## Een gegevensweergave instellen

Een gegevensweergave is een container specifiek voor Customer Journey Analytics waarmee u kunt bepalen hoe gegevens van een verbinding moeten worden geïnterpreteerd. Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

Uw gegevensweergave maken:

1. Selecteer in de gebruikersinterface van Customer Journey Analytics de optie **[!UICONTROL Data views]** (optioneel in **[!UICONTROL Data management]** ) in het bovenste menu.

2. Selecteer **[!UICONTROL Create new data view]** .

3. In de stap [!UICONTROL Configure] :

   Selecteer de verbinding in de lijst [!UICONTROL Connection] .

   Naam en (optioneel) beschrijf uw verbinding.

   ![&#x200B; de mening van Gegevens vormt &#x200B;](./assets/cja-dataview-1.png)

   Selecteer **[!UICONTROL Save and continue]** .

4. In de stap [!UICONTROL Components] :

   Voeg schemagebieden en/of standaardcomponent toe die u aan de [!UICONTROL METRICS] of [!UICONTROL DIMENSIONS] componentenvakjes wilt omvatten.

   ![&#x200B; de meningscomponenten van Gegevens &#x200B;](./assets/cja-dataview-2.png)

   Selecteer **[!UICONTROL Save and continue]** .

5. In de stap [!UICONTROL Settings] :

   ![&#x200B; de meningsmontages van Gegevens &#x200B;](./assets/cja-dataview-3.png)

   Laat de instellingen ongewijzigd en selecteer **[!UICONTROL Save and finish]** .

Zie [&#x200B; overzicht van de meningen van Gegevens &#x200B;](../data-views/data-views.md) voor meer informatie over om een gegevensmening tot stand te brengen en uit te geven, welke componenten voor u aan gebruik in uw gegevensmening en hoe te segment en zittingsmontages te gebruiken beschikbaar zijn.


## Een project instellen

Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen op basis van uw gegevens. U gebruikt de projecten van Workspace om gegevenscomponenten, lijsten, en visualisaties te combineren om uw analyse te bundelen en met iedereen in uw organisatie te delen.

Uw project maken:

1. Selecteer in de gebruikersinterface van Customer Journey Analytics de optie **[!UICONTROL Projects]** in het bovenste menu.

2. Selecteer **[!UICONTROL Projects]** in de linkernavigatie.

3. Selecteer **[!UICONTROL Create project]** .

   ![&#x200B; Project van Workspace &#x200B;](./assets/cja-projects-1.png)

   Selecteer **[!UICONTROL Blank project]** .

   ![&#x200B; Workspace - Leeg Project &#x200B;](./assets/cja-projects-2.png)

4. Selecteer de gegevensweergave in de lijst.

   ![&#x200B; de Uitgezochte mening van Gegevens van Workspace &#x200B;](./assets/cja-projects-3.png).

5. Als u uw eerste rapport wilt maken, sleept u de afmetingen en metriek op de [!UICONTROL Freeform table] in de [!UICONTROL Panel] . Sleep bijvoorbeeld `Program Points Balance` en `Page View` als metriek en `email` als dimensie om een snel overzicht te krijgen van profielen die uw website hebben bezocht en deel uitmaken van het loyaliteitsprogramma dat loyaliteitspunten verzamelt.

   ![&#x200B; Workspace - Eerste Rapport &#x200B;](./assets/cja-projects-5.png)

Zie [&#x200B; overzicht van Analysis Workspace &#x200B;](../analysis-workspace/home.md) voor meer informatie over hoe te om projecten tot stand te brengen en uw analyse te bouwen gebruikend componenten, visualisaties, en panelen.

>[!SUCCESS]
>
>U hebt alle stappen uitgevoerd. Eerst definieert u welke gegevens u wilt verzamelen (schema) en waar u deze wilt opslaan (dataset) in Adobe Experience Platform. Vervolgens hebt u een gegevensstroom geconfigureerd op de Edge Network om ervoor te zorgen dat gegevens naar die gegevensset kunnen worden doorgestuurd. Vervolgens hebt u de tag gedefinieerd en geïmplementeerd die de extensies (Adobe Experience Platform Web SDK, Experience Cloud ID Service), gegevenselementen en regels bevat voor het vastleggen van gegevens van uw website en het verzenden van die gegevens naar uw gegevensstroom. U hebt in Customer Journey Analytics een verbinding gedefinieerd om uw website-volggegevens en andere gegevens te gebruiken. Met de definitie van uw gegevensweergave kunt u opgeven welke dimensie en metriek u wilt gebruiken en ten slotte hebt u uw eerste project gemaakt waarin uw gegevens worden gevisualiseerd en geanalyseerd.
