---
title: Overzicht van filters
description: Begrijp waarvoor filters worden gebruikt en hoe u een eenvoudig filter maakt.
exl-id: 21183e98-6593-4b22-99c7-4a03231acfe9
feature: Filters
role: User
source-git-commit: 5fbb228fc02304be2246f0b49cb49de7f160b227
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%

---


# Overzicht van filters

Met Customer Journey Analytics kunt u krachtige, doelgerichte publieksfilters maken, beheren, delen en toepassen op uw rapporten. Met filters kunt u subsets van personen, sessies of gebeurtenissen identificeren op basis van kenmerken of interacties. Filters zijn ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en met andere teamleden kunt delen.

Filters kunnen worden gebaseerd op:

- kenmerken (browsertype, apparaat, aantal bezoeken, land, geslacht);
- interacties (campagnes, trefwoordzoekers, zoekmachines);
- uitgang en binnenkomst (personen uit Facebook, een bepaalde landingspagina, verwijzend domein, gebeurtenis geofence);
- aangepaste variabelen (formulierveld, gedefinieerde categorieën, klant-id),
- en andere criteria.

Zie [ filters ](/help/components/filters/create-filters.md) voor de diverse beschikbare opties creëren om filters tot stand te brengen. U bouwt dan, wijzigt, en bewaart de definitie van een filter in de [ bouwer van de Filter ](filter-builder.md). Alternatief, kunt u snelle filters tot stand brengen gebruikend de [ Snelle filtermeester ](quick-filters.md). En u kunt filters van visualisaties in Workspace ook produceren, bijvoorbeeld gebruikend de [ Vallout ](/help/analysis-workspace/visualizations/fallout/configuring-fallout.md#context-menu) visualisatie.

U gebruikt de [ manager van Filters ](manage-filters.md) om filters te beheren.

## Abonnementsfilters

Vooral als beheerder verhoogt de juiste planning van filters de kans dat de filters worden gebruikt. Houd rekening met het volgende wanneer u filters plant:

- **Publiek**: Wie zal uw filters gebruiken? Zorg ervoor dat u een goede filterbeschrijving opgeeft, zodat het publiek begrijpt:
   - Wanneer is dit filter nuttig?

   - Wanneer moet ik dit filter gebruiken?

- **Reikwijdte**: Welke [ container van de Filter ](#filter-containers) beste vertegenwoordigt de gegevens u na bent? Gebruik de kleinst mogelijke container.

- **Componenten**: Beslis welke componenten om in de filterdefinitie te omvatten, en tegen welke waarden de voorwaarden zouden moeten bevestigen.

- **Proces**: Overweeg een goedkeuringsproces voor uw filter. Er is geen goedkeuringswerkstroom in Customer Journey Analytics maar u kunt wel een proces organiseren om te bepalen of u een filter goedkeurt of niet.

- **Modulariteit**: Bepaal filters met modulariteit in mening. Zo, kunnen de gebruikers van uw filters gemakkelijk [ stapelfilters ](filter-builder.md#stack-filters) creëren om krachtige nieuwe filters tot stand te brengen.


## Filtertypen

U kunt drie typen filters maken:

### Snelle filters

De snelle filters staan u toe om gegevens binnen een bepaald project van Workspace gemakkelijk te onderzoeken, zonder de behoefte om een filter in de [ Bouwer van de Filter ](/help/components/filters/create-filters.md) tot stand te brengen. U definieert het filter rechtstreeks in de Workspace-interface. Zie [ Snelle filters ](quick-filters.md) voor meer informatie.

### Gewone filters

Met de standaardfilters kunt u gegevens (personen, sessies, gebeurtenissen) identificeren op basis van een of meer voorwaarden. Als er meerdere voorwaarden zijn, gebruikt u logische operatoren als And en Of om het filter verder te definiëren. U kunt containers gebruiken om voorwaarden te groeperen en complexere filters te bouwen. Zie [ Bouwer van de Filter ](filter-builder.md) voor meer informatie.

### Opeenvolgende filters

>[!IMPORTANT]
>
>U moet het **Uitgezochte** pakket hebben om dwars-kanaal opeenvolgende filters tot stand te brengen. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

Met opeenvolgende filters kunt u gegevens (personen, sessies, gebeurtenissen) identificeren op basis van navigatie (paginaweergaven op uw site, interactie met scènes in uw mobiele app of via een menu in een set-top box). Met behulp van opeenvolgende filters kunt u bijvoorbeeld vaststellen wat een persoon leuk vindt en wat een persoon vermijdt. U gebruikt dan logische exploitant om een opeenvolgend filter te bepalen. Zie [ Opeenvolgende filters ](seg-sequential-build.md) voor meer informatie.


<!--
An example of a complex sequential filter if you want to find the persons that 

| Session One | Session Two | Session Three |
| --- | --- | --- |
| The person went to the main landing page A, excluded the campaign page B, and then viewed the Product page C.| The person again went to the main landing page A, excluded the campaign page B, and went again to the Product page C, and then to a new page D. | The person entered and followed that same path as in the first and second visits, then excluded page F to go directly to a targeted product on page G. |
-->

## Filtercontainers {#containers}

Filters zijn gebaseerd op een hiërarchie op persoon-, sessie- en gebeurtenisniveau met behulp van een genest containermodel. Met de geneste containers kunt u voorwaarden definiëren tussen en binnen de containers.


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

Met een filter worden voorwaarden ingesteld voor het filteren van personen, sessies of gebeurtenissen op basis van voorwaarden. Bijvoorbeeld voorwaarden om personen te filteren op basis van persoonseigenschappen en navigatiekenmerken. Als u de gegevens verder wilt opsplitsen, kunt u filteren op specifieke sessies, paginaweergavegebeurtenissen, schermtikken, menuopties in een set-top box en meer. Maar filter ook op attributen die u van een CRM of loyaliteitssysteem hebt gegeten. De [ bouwer van de Filter ](/help/components/filters/filter-builder.md) verstrekt een eenvoudige interface om deze subsets te bouwen en voorwaarden in genestelde, hiërarchische Persoon, Zitting, of de containers van de Gebeurtenis toe te passen.

De containerarchitectuur die in de [ bouwer van de Filter ](/help/components/filters/filter-builder.md) wordt gebruikt bepaalt Persoon als buitenste container. De container bevat overkoepelende gegevens die specifiek zijn voor de persoon in sessies en gebeurtenissen zoals paginaweergaven, mobiele toepassingsschermen of menuschermen in een set-top box. Met een geneste Session-container kunt u regels instellen om de gegevens van de persoon op basis van sessies te splitsen. Met een geneste gebeurtenissencontainer kunt u de persoonlijke gegevens opsplitsen op basis van individuele interacties. Elke container laat u over de geschiedenis van een persoon, interactie melden die door zittingen worden verdeeld, of individuele gebeurtenissen onderverdelen.

### Persoonscontainer

De container van de Persoon omvat elke zitting en elke gebeurtenis voor de personen die voor de voorwaarde in de container worden gespecificeerd in aanmerking komen. Wanneer u een filter definieert met een eenvoudige voorwaarde zoals `Page Name equals Checkout` , wordt de container Person omgezet in:

- Alle personen die de pagina met naam `Checkout` hebben bezocht.
- Alle sessies voor deze personen.
- Alle gebeurtenisgegevens voor deze personen.

Als meest algemeen bepaalde container, keert de rapporten die op het containerniveau van de Persoon worden geproduceerd gebeurtenissen en zittingen voor alle personen terug die voor de filter kwalificeren. De container van de Persoon is het meest vatbaar om te veranderen gebaseerd op bepaalde datumwaaiers.
De containers van de persoon kunnen waarden omvatten die op de algemene geschiedenis van een persoon worden gebaseerd:

- Dagen vóór de eerste aankoop.
- Oorspronkelijke startpagina of startscherm van mobiele app.
- Oorspronkelijke verwijzende domeinen.

### Sessiecontainer

Met de Sessiecontainer kunt u paginainteracties of mobiele toepassingsinteracties, campagnes of conversies voor een specifieke sessie identificeren. De container van de Zitting is de gemeenschappelijkste gebruikte container omdat het gedrag voor de volledige zitting vangt zodra de regel wordt ontmoet. Met de container Sessie kunt u ook definiëren welke sessies u wilt opnemen in het samenstellen en toepassen van een filter.  Wanneer u een filter definieert met een eenvoudige voorwaarde zoals `Page Name equals Checkout` , wordt de Session-container omgezet in:

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

De container van de Gebeurtenis bepaalt welke pagina, mobiele toepassing, of ander type van gebeurtenissen die u van een filter zou willen omvatten of uitsluiten. Het is het smaakst van de beschikbare containers om u specifieke kliks, paginamening, tikt op knoop in een mobiele app te identificeren waar een voorwaarde waar is. Met de container Event kunt u één trackingcode weergeven of gedrag isoleren binnen een bepaald gebied van uw mobiele app. U kunt ook een specifieke waarde aanwijzen wanneer een handeling plaatsvindt, zoals het marketingkanaal wanneer een order is geplaatst. Wanneer u een filter definieert met een eenvoudige voorwaarde zoals `Page Name equals Checkout` , wordt de Event-container omgezet in:

- Alle paginaweergavegebeurtenissen waarbij de paginanaam gelijk is aan `Checkout` .

Gebeurteniscontainers bevatten op waarde gebaseerde uitsplitsingen van één pagina voor:

- Producten
- Props weergeven
- Lijstafmetingen
- Merchandising-afmetingen (in de context van gebeurtenissen)


### Logische-groepscontainer

Met de Logic Group kunt u voorwaarden groeperen in één controlepunt voor opeenvolgende filters. Als onderdeel van de reeks wordt de logica die is gedefinieerd in de container die als [!UICONTROL Logic Group] is geïdentificeerd, geëvalueerd na een eventueel eerder opeenvolgend controlepunt en vóór een volgend opeenvolgend controlepunt. Zie [ Logische Groep ](seg-sequential-build.md#logic-group) voor meer informatie.

### Nest containers

Wanneer u containers in andere containers maakt, maakt u een filter in feite. De volgende logica wordt toegepast op geneste containers:

1. Bepaal welke gegevens worden opgenomen met de buitenste container. Om het even welke gegevens die deze buitenregel niet aanpassen worden verworpen in het rapport.
2. Pas de geneste filterdefinitie toe op de resterende gegevens. De geneste filterdefinitie is NIET van toepassing op gegevens die de eerste definitie heeft verwijderd.
3. Herhaal deze bewerking totdat alle geneste containerfilterdefinities zijn berekend. De overige gegevens worden vervolgens in het resultaat opgenomen en voor rapportage gebruikt.

>[!NOTE]
>
>Wanneer u een filter negeert binnen een filter (bijvoorbeeld wanneer u een filter uit het deelvenster Componenten naar de filterdefinitie sleept), wordt een container gemaakt met een kopie (geen referentie) van de gesleepte filterdefinitie.

<!--
You can use nesting between containers and between conditions within a container. Here is what you can nest in each container:


| Container | What container you can nest inside |
| Event | Only event conditions |
| Session | Session


## Out-of-the-box filter template {#template}

Traditional Analytics comes with numerous out-of-the-box templates and calculated metrics. Many of them do not apply in Customer Journey Analytics, or have to be renamed or recreated. Others depend on a solution for context-aware variables in Customer Journey Analytics.

| Filter Name | Description |
| --- | --- |
| All Data | All Data is a required filter that gets dynamically added to reporting when a metric is added to the row of a Freeform table. |
-->

>[!MORELIKETHIS]
>
>[ creeer filters ](create-filters.md)
>[Filter Builder ](filter-builder.md)
>[Snelle filters ](quick-filters.md)
>[Opeenvolgende filters ](seg-sequential-build.md)
>[Filters beheren ](manage-filters.md)
>
