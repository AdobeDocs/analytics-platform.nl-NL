---
title: Overzicht van filters
description: Begrijp waarvoor filters worden gebruikt en hoe u een eenvoudig filter maakt.
exl-id: 21183e98-6593-4b22-99c7-4a03231acfe9
source-git-commit: 3f1112ebd2a4dfc881ae6cb7bd858901d2f38d69
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 1%

---


# Overzicht van filters {#overview}

Met Customer Journey Analytics kunt u krachtige, doelgerichte publieksfilters maken, beheren, delen en toepassen op uw rapporten. Met filters kunt u subsets van personen identificeren op basis van eigenschappen of interacties van websites. Filters zijn ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en met andere teamleden kunt delen.

Filters kunnen worden gebaseerd op kenmerken (browsertype, apparaat, aantal bezoeken, land, geslacht), interacties (campagnes, trefwoordzoeker, zoekmachine), uitgangen en items (personen uit Facebook, een gedefinieerde bestemmingspagina, een verwijzingsdomein), aangepaste variabelen (formulierveld, gedefinieerde categorieën, de klant-id) en andere criteria.

U kunt filters bouwen en bewaren in de Bouwer van de Filter, of filters van een visualisatie van de Vallout (in Werkruimte) produceren. Bovendien kunnen filters samen als gestapelde filters worden gebruikt.

Filteren bevat de opdracht [Filter Builder](/help/components/filters/filter-builder.md) om filters te maken en een pretest uit te voeren, en [Filterbeheer](/help/components/filters/manage-filters.md) om filters te verzamelen, te etiketteren, goed te keuren, veiligheid te plaatsen, en over uw organisatie te delen.

Het maximumaantal filters dat u per IMS-organisatie kunt maken, is 50.000.

## Filtertypen {#types}

Voor informatie over de beschikbare typen filters en hoe u deze kunt maken, raadpleegt u [Filters maken](/help/components/filters/create-filters.md).

## Opeenvolgende filters {#sequential}

Met opeenvolgende filters kunt u personen identificeren op basis van navigatie en paginaweergave op de hele site. Zo beschikt u over een filter met gedefinieerde handelingen en interacties. Met behulp van opeenvolgende filters kunt u bepalen wat een persoon leuk vindt en wat een persoon vermijdt. Wanneer het bouwen van opeenvolgende filters, wordt de exploitant THEN gebruikt om persoonnavigatie te bepalen en te ordenen.

Hier volgt een voorbeeld:

![](assets/sequential_fil.png)

| Eén bezoeken | Twee bezoeken | Drie bezoeken |
| --- | --- | --- |
| De persoon ging naar de hoofdlandingspagina (A), sloot de campagnepagina (B) uit en bekeken de productpagina (C). | De persoon ging opnieuw naar de hoofdbestemmingspagina (A), sloot de campagnepagina (B) uit, en ging opnieuw naar de productpagina (C) en vervolgens naar een nieuwe pagina (D). | De persoon heeft dezelfde weg ingeslagen en gevolgd als bij de eerste en tweede bezoeken, en vervolgens pagina F uitgesloten om rechtstreeks naar een bepaalde productpagina (G) te gaan. |

## Filtercontainers {#containers}

Filters zijn gebaseerd op een hiërarchie op Person-, Session- en Gebeurtenisniveau met behulp van een genest containermodel. Met de geneste containers kunt u persoonkenmerken en handelingen definiëren op basis van regels tussen en binnen de containers.

>[!NOTE]
>De container Person werd voorheen de container van de Bezoeker genoemd. De container van de Zitting werd genoemd de container van het Bezoek, en de container van de Gebeurtenis gebruikte om de container van het Actief te zijn.

Een filter stelt voorwaarden in om een persoon te filteren op basis van zijn of haar kenmerken of interacties met uw site. Als u de voorwaarden in een filter wilt instellen, stelt u regels in voor het filteren van personen op basis van persoonlijke kenmerken en/of navigatiekenmerken. Als u persoonlijke gegevens verder wilt opsplitsen, kunt u filteren op basis van specifieke bezoeken en/of hits in de paginaweergave voor elke persoon. De Bouwer van de Filter verstrekt een eenvoudige architectuur om deze subsets te bouwen en regels als genestelde, hiërarchische Persoon, Zitting, of de containers van de Gebeurtenis toe te passen.

De containerarchitectuur die in de Bouwer van de Filter wordt gebruikt bepaalt Persoon als buitenste container, die overkoepelende gegevens specifiek voor de persoon over bezoeken en paginameningen bevat. Met een geneste Session-container kunt u regels instellen om de gegevens van de persoon op basis van sessies te splitsen. Met een geneste Event-container kunt u de persoonlijke gegevens op basis van de afzonderlijke paginaweergaven onderbreken. Elke container laat u over de geschiedenis van een persoon, interactie melden die door zittingen worden verdeeld, of individuele gebeurtenissen onderverdelen.

### Persoonscontainer {#person}

De container van de Persoon omvat elk bezoek en paginamening voor personen binnen een gespecificeerd tijdkader. Een filter op het niveau van de Persoon keert de pagina terug die aan de voorwaarde plus alle andere pagina&#39;s voldoet die door de persoon (en slechts beperkt door bepaalde datumwaaiers) worden bekeken. Als meest breed-bepaalde container, zullen de rapporten die op het niveau van de container van de Persoon worden geproduceerd paginameningen over alle bezoeken terugkeren en laat u een multi-bezoek analyse produceren. Daarom is de container van de Persoon het meest vatbaar om te veranderen gebaseerd op bepaalde datumwaaiers.
De containers van de persoon kunnen waarden omvatten die op de algemene geschiedenis van een persoon worden gebaseerd:

* Dagen vóór eerste aankoop
* Oorspronkelijke invoerpagina
* Oorspronkelijke verwijzende domeinen

### Sessiecontainer {#session}

Met de container Sessie kunt u paginainteracties, campagnes of conversies voor een specifieke sessie identificeren. De container van de Zitting is de gemeenschappelijkste gebruikte container omdat het gedrag voor de volledige bezoekzitting vangt zodra de regel wordt ontmoet en u laat bepalen welke zittingen u in de bouw en het toepassen van een filter wilt omvatten of uitsluiten. Het kan u helpen deze vragen beantwoorden:

* Hoeveel zittingen betrokken met zowel Web als de gegevensbronnen van het Centrum van de Vraag?
* Welke pagina&#39;s hebben bijgedragen tot een geslaagde omzetting in een uitverkoop?

Sessiecontainers bevatten waarden die zijn gebaseerd op de aanwezigheid per sessie:

* Type sessie
* Itempagina
* Retourfrequentie
* Deelnamemetriek
* Lineaire toegewezen metriek

### Gebeurteniscontainer {#event}

In de container Event wordt gedefinieerd welke paginagebeurtenissen u wilt opnemen in of uitsluiten van een filter. Het is het meest smalle van de beschikbare containers om u specifieke kliks en paginamening te laten identificeren waar een voorwaarde waar is, latend u één enkele het volgen code bekijken, of gedrag binnen een bepaalde sectie van uw plaats isoleren. U kunt ook een specifieke waarde aanwijzen wanneer een handeling plaatsvindt, zoals het marketingkanaal wanneer een order is geplaatst.

Gebeurteniscontainers bevatten op waarden gebaseerde uitsplitsingen van één pagina:

* Producten
* Props weergeven
* Lijstafmetingen
* Merchandising-afmetingen (in de context van gebeurtenissen)

## Filtersjabloon buiten de box {#template}

Traditionele analyse wordt geleverd met veel out-of-the-box sjabloonfilters (filters) en berekende meetgegevens. Veel van deze regels zijn niet van toepassing op CJA of moeten worden hernoemd of opnieuw worden gemaakt. Andere zullen van een oplossing voor context-bewuste variabelen in CJA afhangen.

| Filternaam | Beschrijving |
| --- | --- |
| Alle gegevens | Dit is een vereist filter dat dynamisch aan het melden wordt toegevoegd wanneer metrisch aan de rij van een lijst Freeform wordt toegevoegd. |
