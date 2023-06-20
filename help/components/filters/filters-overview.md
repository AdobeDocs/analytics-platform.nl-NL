---
title: Overzicht van filters
description: Begrijp waarvoor filters worden gebruikt en hoe u een eenvoudig filter maakt.
exl-id: 21183e98-6593-4b22-99c7-4a03231acfe9
source-git-commit: e7e3affbc710ec4fc8d6b1d14d17feb8c556befc
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 1%

---


# Overzicht van filters {#overview}

Met Customer Journey Analytics kunt u krachtige, doelgerichte publieksfilters maken, beheren, delen en toepassen op uw rapporten. Met filters kunt u subsets van personen identificeren op basis van eigenschappen of interacties van websites. Filters zijn ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en met andere teamleden kunt delen.

Filters kunnen worden gebaseerd op

- kenmerken (browsertype, apparaat, aantal bezoeken, land, geslacht);
- interacties (campagnes, trefwoordzoekers, zoekmachines);
- uitgang en binnenkomst (personen uit Facebook;
- een gedefinieerde landingspagina, verwijzend domein);
- aangepaste variabelen (formulierveld, gedefinieerde categorieën, klant-id),
- en andere criteria.

U kunt filters bouwen en bewaren in de Bouwer van de Filter, of filters van een visualisatie van de Vallout (in Werkruimte) produceren. Bovendien kunnen filters samen als gestapelde filters worden gebruikt.

Filteren bevat de opdracht [Filter Builder](/help/components/filters/filter-builder.md) om filters te maken en een pretest uit te voeren, en [Filterbeheer](/help/components/filters/manage-filters.md) om filters te verzamelen, te etiketteren, goed te keuren, veiligheid te plaatsen, en over uw organisatie te delen.

Het maximumaantal filters dat u per IMS-organisatie kunt maken, is 50.000.

## Filtertypen {#types}

Voor informatie over de beschikbare typen filters en hoe u deze kunt maken, raadpleegt u [Filters maken](/help/components/filters/create-filters.md).

## Opeenvolgende filters {#sequential}

Met opeenvolgende filters kunt u personen identificeren op basis van navigatie en paginaweergave op de hele site. Zo beschikt u over een filter met gedefinieerde handelingen en interacties. Met behulp van opeenvolgende filters kunt u bepalen wat een persoon leuk vindt en wat een persoon vermijdt. Wanneer het bouwen van opeenvolgende filters, wordt de exploitant THEN gebruikt om persoonnavigatie te bepalen en te ordenen.

Hier volgt een voorbeeld:

<!--![](assets/sequential_fil.png)-->

| Sessie één | Sessie twee | Sessie drie |
| --- | --- | --- |
| De persoon ging naar hoofdlandingspagina A, sloot de campagnepagina B uit en keek vervolgens naar productpagina C. | De persoon ging opnieuw naar de hoofdbestemmingspagina A, sloot de campagnepagina B uit en ging opnieuw naar productpagina C en vervolgens naar een nieuwe pagina D. | De persoon heeft dezelfde weg ingeslagen en gevolgd als bij de eerste en tweede bezoeken, en vervolgens pagina F uitgesloten om rechtstreeks naar een bepaalde productpagina G te gaan. |

## Filtercontainers {#containers}

Filters zijn gebaseerd op een hiërarchie op Person-, Session- en Gebeurtenisniveau met behulp van een genest containermodel. Met de geneste containers kunt u persoonkenmerken en handelingen definiëren op basis van regels tussen en binnen de containers.


<table style="table-layout: fixed; border: none;">

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
>De container Person werd voorheen de container van de Bezoeker genoemd. De container van de Zitting werd genoemd de container van het Bezoek, en de container van de Gebeurtenis gebruikte om de container van het Actief te zijn.

Een filter stelt voorwaarden in om een persoon te filteren op basis van de kenmerken van de persoon of de interacties met uw site. Als u de voorwaarden in een filter wilt instellen, stelt u regels in voor het filteren van personen op basis van persoonlijke kenmerken en/of navigatiekenmerken. Als u persoonlijke gegevens verder wilt opsplitsen, kunt u filteren op basis van specifieke bezoeken en/of hits in de paginaweergave voor elke persoon. De Bouwer van de Filter verstrekt een eenvoudige architectuur om deze subsets te bouwen en regels als genestelde, hiërarchische Persoon, Zitting, of de containers van de Gebeurtenis toe te passen.

De containerarchitectuur die in de Bouwer van de Filter wordt gebruikt bepaalt Persoon als buitenste container, die overkoepelende gegevens specifiek voor de persoon over bezoeken en paginameningen bevat. Met een geneste Session-container kunt u regels instellen om de gegevens van de persoon op basis van sessies te splitsen. Met een geneste Event-container kunt u de persoonlijke gegevens op basis van de afzonderlijke paginaweergaven onderbreken. Elke container laat u over de geschiedenis van een persoon, interactie melden die door zittingen worden verdeeld, of individuele gebeurtenissen onderverdelen.

### Persoonscontainer {#person}

De container van de Persoon omvat elk bezoek en paginamening voor personen binnen een gespecificeerd tijdkader. Een filter op het niveau van de Persoon keert de pagina terug die aan de voorwaarde plus alle andere pagina&#39;s voldoet die door de persoon (en slechts beperkt door bepaalde datumwaaiers) worden bekeken. Als meest breed bepaalde container, keert de rapporten die op het niveau van de container van de Persoon worden geproduceerd paginameningen over alle bezoeken terug en laat u een multi-bezoek analyse produceren. Daarom is de container van de Persoon het meest vatbaar om te veranderen gebaseerd op bepaalde datumwaaiers.
De containers van de persoon kunnen waarden omvatten die op de algemene geschiedenis van een persoon worden gebaseerd:

- Dagen vóór eerste aankoop
- Oorspronkelijke invoerpagina
- Oorspronkelijke verwijzende domeinen

### Sessiecontainer {#session}

Met de container Sessie kunt u paginainteracties, campagnes of conversies voor een specifieke sessie identificeren. De container van de Zitting is de gemeenschappelijkste gebruikte container omdat het gedrag voor de volledige bezoekzitting vangt zodra de regel wordt ontmoet. Met de container Sessie kunt u ook definiëren welke sessies u wilt opnemen in het samenstellen en toepassen van een filter. Het kan u helpen de volgende vragen beantwoorden:

- Hoeveel zittingen betrokken met zowel Web als de gegevensbronnen van het Centrum van de Vraag?
- Welke pagina&#39;s hebben bijgedragen tot een geslaagde omzetting in een uitverkoop?

Sessiecontainers bevatten waarden die zijn gebaseerd op de aanwezigheid per sessie:

- Type sessie
- Itempagina
- Retourfrequentie
- Deelnamemetriek
- Lineaire toegewezen metriek

### Gebeurteniscontainer {#event}

De container van de Gebeurtenis bepaalt welke paginagebeurtenissen u van een filter zou willen omvatten of uitsluiten. Het is het meest smalle van de beschikbare containers om u specifieke kliks en paginamening te laten identificeren waar een voorwaarde waar is. Met de container Event kunt u één code voor bijhouden weergeven of gedrag in een bepaald gedeelte van uw site isoleren. U kunt ook een specifieke waarde aanwijzen wanneer een handeling plaatsvindt, zoals het marketingkanaal wanneer een order is geplaatst.

Gebeurteniscontainers bevatten op waarden gebaseerde uitsplitsingen van één pagina:

- Producten
- Props weergeven
- Lijstafmetingen
- Merchandising-afmetingen (in de context van gebeurtenissen)

## Filtersjabloon buiten de box {#template}

De traditionele Analytics komt met talrijke uit-van-de-doos malplaatjefilters (filters) en berekende metriek. Veel van deze regels zijn niet van toepassing in Customer Journey Analytics of moeten worden hernoemd of opnieuw worden gemaakt. Andere zijn afhankelijk van een oplossing voor contextgevoelige variabelen in Customer Journey Analytics.

| Filternaam | Beschrijving |
| --- | --- |
| Alle gegevens | Alle gegevens zijn een vereist filter dat dynamisch aan het melden wordt toegevoegd wanneer metrisch aan de rij van een lijst Freeform wordt toegevoegd. |
