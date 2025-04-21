---
title: Overzicht van segmentatie
description: Begrijp welke segmenten worden gebruikt voor en hoe te om een eenvoudig segment tot stand te brengen.
exl-id: 21183e98-6593-4b22-99c7-4a03231acfe9
feature: Filters
role: User
source-git-commit: 976f481b6886a4f260f44854a30c47ab0dad7955
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---


# Overzicht van segmentatie

Met Customer Journey Analytics kunt u krachtige, doelgerichte publiekssegmenten maken, beheren, delen en toepassen op uw rapporten. Met segmenten kunt u subsets van personen, sessies of gebeurtenissen identificeren op basis van kenmerken of interacties. De segmenten worden ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en delen met andere teamleden.

Segmenten kunnen worden gebaseerd op:

- kenmerken (browsertype, apparaat, aantal bezoeken, land, geslacht);
- interacties (campagnes, trefwoordzoekers, zoekmachines);
- uitgang en binnenkomst (personen van Facebook, een gedefinieerde landingspagina, verwijzend domein, geofence-gebeurtenis);
- aangepaste variabelen (formulierveld, gedefinieerde categorieën, klant-id),
- en andere criteria.

Zie [ segmenten ](/help/components/filters/create-filters.md) voor de diverse beschikbare opties creëren om segmenten tot stand te brengen. U bouwt dan, wijzigt, en bewaart de definitie van een segment in de [ bouwer van het Segment ](filter-builder.md). Alternatief, kunt u snelle segmenten tot stand brengen gebruikend de [ Snelle segmentbouwer ](quick-filters.md). En u kunt segmenten van visualisaties in Workspace ook produceren, bijvoorbeeld gebruikend de [ Vallout ](/help/analysis-workspace/visualizations/fallout/configuring-fallout.md#context-menu) visualisatie.

U gebruikt de [ manager van het Segment ](manage-filters.md) om segmenten te beheren.

## Elementen plannen

Vooral, als beheerder, verbetert de juiste planning van segmenten de kansen dat de segmenten worden gebruikt. Overweeg het volgende wanneer het plannen van segmenten:

- **Publiek**: Wie zal uw segmenten gebruiken? Zorg ervoor dat u een goede segmentbeschrijving opgeeft, zodat het publiek begrijpt:
   - Waar is dit segment nuttig voor?

   - Wanneer moet ik dit segment gebruiken?

- **Reikwijdte**: Welke [ container van het Segment ](#filter-containers) beste vertegenwoordigt de gegevens u na bent? Gebruik de kleinst mogelijke container.

- **Componenten**: Beslis welke componenten om in de segmentdefinitie te omvatten, en tegen welke waarden de voorwaarden zouden moeten bevestigen.

- **Proces**: Overweeg een goedkeuringsproces voor uw segmenten. Er is geen goedkeuringswerkstroom in Customer Journey Analytics, maar u kunt wel een proces organiseren om te bepalen of u een segment goedkeurt of niet.

- **Modulariteit**: Bepaal segmenten met modulariteit in mening. De gebruikers van uw segmenten zouden [ stapelsegmenten ](filter-builder.md#stack-filters) gemakkelijk moeten kunnen {maken om krachtige nieuwe segmenten tot stand te brengen.


## Segmenttypen

U kunt drie typen segmenten maken:

### Snelle segmenten

De snelle segmenten staan u toe om gegevens binnen een bepaald project van Workspace gemakkelijk te onderzoeken, zonder de behoefte om een segment in de [ Bouwer van het Segment ](/help/components/filters/create-filters.md) tot stand te brengen. U definieert het segment rechtstreeks in de Workspace-interface. Zie [ Snelle segmenten ](quick-filters.md) voor meer informatie.

### Gewone segmenten

Met gewone segmenten kunt u gegevens (personen, sessies, gebeurtenissen) identificeren op basis van een of meer voorwaarden. Als u meer dan één voorwaarde hebt, gebruikt u logische operatoren als And en Of om het segment verder te definiëren. U kunt containers gebruiken om voorwaarden te groeperen en complexere segmenten te bouwen. Zie [ de bouwer van het Segment ](filter-builder.md) voor meer informatie.

### Sequentiële segmenten

>[!IMPORTANT]
>
>U moet het **Uitgezochte** pakket hebben om dwars-kanaal opeenvolgende segmenten tot stand te brengen. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

Met opeenvolgende segmenten kunt u gegevens (personen, sessies, gebeurtenissen) identificeren op basis van navigatie (paginaweergaven op uw site, interactie met scènes in uw mobiele app of via een menu in een set-top box). De opeenvolgende segmenten helpen u, bijvoorbeeld, identificeren wat een persoon houdt en wat een persoon vermijdt. U gebruikt dan logische exploitant om een opeenvolgend segment te bepalen. Zie [ Opeenvolgende segmenten ](seg-sequential-build.md) voor meer informatie.


<!--
An example of a complex sequential segment if you want to find the persons that 

| Session One | Session Two | Session Three |
| --- | --- | --- |
| The person went to the main landing page A, excluded the campaign page B, and then viewed the Product page C.| The person again went to the main landing page A, excluded the campaign page B, and went again to the Product page C, and then to a new page D. | The person entered and followed that same path as in the first and second visits, then excluded page F to go directly to a targeted product on page G. |
-->

## Segmentcontainers {#containers}

Segmenten zijn gebaseerd op een hiërarchie op Person-, Sessie- en Gebeurtenisniveau met behulp van een genest containermodel. Met de geneste containers kunt u voorwaarden definiëren tussen en binnen de containers.


<table style="table-layout: fixed; border: none;" width="100%">

<tr>
<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Persoon</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Sessie</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Gebeurtenis</td>
</tr>
</table>

>[!NOTE]
>
>Voor Adobe Analytics-gebruikers:
> 
> - De **container van 0} Persoon {is gekend in Adobe Analytics als** bezoeker **container.**
> - De **container van de Zitting** is gekend in Adobe Analytics als **bezoek** container.
> - De **container van de Gebeurtenis** is gekend in Adobe Analytics als **Actief** container.
>

In een segment worden voorwaarden ingesteld voor het segmenteren van personen, sessies of gebeurtenissen op basis van voorwaarden. Voorwaarden voor personen segmenteren zijn bijvoorbeeld gebaseerd op eigenschappen van personen en navigatiemogelijkheden. Als u de gegevens verder wilt opsplitsen, kunt u segmenteren op specifieke sessies, paginaweergavegebeurtenissen, schermtikken, menuopties op een set-top box en meer. U kunt op attributen ook segmenteren die u van een CRM of loyaliteitssysteem hebt ingegeten. De [ bouwer van het Segment ](/help/components/filters/filter-builder.md) verstrekt een eenvoudige interface om deze subsets te bouwen en voorwaarden in genestelde, hiërarchische Persoon, Zitting, of de containers van de Gebeurtenis toe te passen.

De containerarchitectuur die in de [ bouwer van het Segment ](/help/components/filters/filter-builder.md) wordt gebruikt bepaalt Persoon als buitenste container. Deze container bevat overkoepelende gegevens die specifiek zijn voor de persoon in sessies en gebeurtenissen zoals paginaweergaven, mobiele toepassingsschermen of menuschermen in een set-top box. Met een geneste Session-container kunt u regels instellen om de gegevens van de persoon op basis van sessies te splitsen. Met een geneste gebeurtenissencontainer kunt u de persoonlijke gegevens opsplitsen op basis van individuele interacties. Elke container laat u over de geschiedenis van een persoon, interactie melden die door zittingen worden verdeeld, of individuele gebeurtenissen onderverdelen.

### Persoonscontainer

De container van de Persoon omvat elke zitting en elke gebeurtenis voor de personen die voor de voorwaarde in de container worden gespecificeerd in aanmerking komen. Wanneer u een segment definieert met een eenvoudige voorwaarde zoals `Page Name equals Checkout` , wordt de container Person omgezet in:

- Alle personen die de pagina met naam `Checkout` hebben bezocht.
- Alle sessies voor deze personen.
- Alle gebeurtenisgegevens voor deze personen.

Als meest algemeen bepaalde container, rapporten die op het niveau van de container van de Persoon worden geproduceerd terugkeergebeurtenissen en zittingen voor alle personen die voor het segment kwalificeren. De container van de Persoon is het meest vatbaar om te veranderen gebaseerd op bepaalde datumwaaiers.
De containers van de persoon kunnen waarden omvatten die op de algemene geschiedenis van een persoon worden gebaseerd:

- Dagen vóór de eerste aankoop.
- Oorspronkelijke startpagina of startscherm van mobiele app.
- Oorspronkelijke verwijzende domeinen.

### Sessiecontainer

Met de Sessiecontainer kunt u paginainteracties of mobiele toepassingsinteracties, campagnes of conversies voor een specifieke sessie identificeren. De container van de Zitting is de gemeenschappelijkste gebruikte container omdat het gedrag voor de volledige zitting vangt zodra de regel wordt ontmoet. Met de container Sessie kunt u ook definiëren welke sessies u wilt opnemen in het samenstellen en toepassen van een segment.  Wanneer u een segment definieert met een eenvoudige voorwaarde zoals `Page Name equals Checkout` , wordt de container Session omgezet in:

- Alle sessies waarbij een pagina met de naam `Checkout` wordt bezocht.
- Alle gebeurtenisgegevens voor die sessies.

De sessiecontainer kan u helpen de volgende vragen te beantwoorden:

- Hoeveel zittingen impliceerden zowel Web als de gegevensbronnen van het vraagcentrum?
- Welke pagina&#39;s hebben bijgedragen tot een geslaagde omzetting in een uitverkoop?

Sessiecontainers bevatten waarden die zijn gebaseerd op gebeurtenissen per sessie:

- Type sessie.
- Itempagina.
- Retourfrequentie.
- Deelnamemetriek.
- Lineaire toegewezen metriek.

Met gegevensweergaven in Customer Journey Analytics kunt u bepalen hoe lang een sessie duurt, maar ook wanneer een nieuwe sessie moet worden gemaakt. U kunt bijvoorbeeld een nieuwe mobiele-toepassingssessie definiëren op basis van elke keer dat een gebruiker uw mobiele app start. Zie [ montages van de Zitting ](/help/data-views/session-settings.md) voor meer informatie.

### Gebeurteniscontainer

De container van de Gebeurtenis bepaalt welke pagina, mobiele toepassing, of ander type van gebeurtenissen u van een segment zou willen omvatten of uitsluiten. Het is het meest smalle van de beschikbare containers. Hiermee kunt u specifieke kliks, paginaweergave, tikken op een knop in een mobiele app identificeren waar een voorwaarde waar is. Met de container Event kunt u één trackingcode weergeven of gedrag isoleren binnen een bepaald gebied van uw mobiele app. U kunt ook een specifieke waarde aanwijzen wanneer een handeling plaatsvindt, zoals het marketingkanaal wanneer een order is geplaatst. Wanneer u een segment definieert met een eenvoudige voorwaarde zoals `Page Name equals Checkout` , wordt de Event-container omgezet in:

- Alle paginaweergavegebeurtenissen waarbij de paginanaam gelijk is aan `Checkout` .

Gebeurteniscontainers bevatten op waarde gebaseerde uitsplitsingen van één pagina voor:

- Producten
- Props weergeven
- Lijstafmetingen
- Merchandising-afmetingen (in de context van gebeurtenissen)


### Logische-groepscontainer

Met de Logische groep kunt u voorwaarden groeperen in één controlepunt voor opeenvolgende segmenten. Als onderdeel van de reeks wordt de logica die is gedefinieerd in de container die als [!UICONTROL Logic Group] is geïdentificeerd, geëvalueerd na een eventueel eerder opeenvolgend controlepunt en vóór een volgend opeenvolgend controlepunt. Zie [ Logische Groep ](seg-sequential-build.md#logic-group) voor meer informatie.

### Nest containers

Wanneer u containers binnen andere containers maakt, maakt u eigenlijk een segment binnen een segment. De volgende logica wordt toegepast op geneste containers:

1. Bepaal welke gegevens worden opgenomen met de buitenste container. Om het even welke gegevens die deze buitenregel niet aanpassen worden verworpen in het rapport.
2. Pas de geneste segmentdefinitie toe op de resterende gegevens. De geneste segmentdefinitie is NIET van toepassing op gegevens die de eerste definitie heeft verwijderd.
3. Herhaal deze bewerking totdat alle geneste-containersegmentdefinities zijn berekend. De overige gegevens worden vervolgens in het resultaat opgenomen en voor rapportage gebruikt.

>[!NOTE]
>
>Wanneer u een segment neest binnen een segment (bijvoorbeeld, sleept u een segment van het paneel van Componenten op uw segmentdefinitie), wordt een container gecreeerd met een exemplaar (niet een verwijzing) van de gesleepte segmentdefinitie.

<!--
You can use nesting between containers and between conditions within a container. Here is what you can nest in each container:


| Container | What container you can nest inside |
| Event | Only event conditions |
| Session | Session


## Out-of-the-box segment template {#template}

Traditional Analytics comes with numerous out-of-the-box templates and calculated metrics. Many of them do not apply in Customer Journey Analytics, or have to be renamed or recreated. Others depend on a solution for context-aware variables in Customer Journey Analytics.

| Segment Name | Description |
| --- | --- |
| All Data | All Data is a required segment that gets dynamically added to reporting when a metric is added to the row of a Freeform table. |
-->

>[!MORELIKETHIS]
>
>[ creeer segmenten ](create-filters.md)
>[Segmentbuilder ](filter-builder.md)
>[Snelle segmenten ](quick-filters.md)
>[Opeenvolgende segmenten ](seg-sequential-build.md)
>[Segmenten beheren ](manage-filters.md)
>
