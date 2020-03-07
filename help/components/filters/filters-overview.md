---
title: Overzicht filters
description: Begrijp welke filters voor worden gebruikt en hoe te om een eenvoudige filter tot stand te brengen.
translation-type: tm+mt
source-git-commit: b521079bb9b3828ec3487b635366f5442f6fc4bd

---


# Overzicht filters

De Analyse van de Reis van de klant laat u, krachtige, geconcentreerde publieksfilters bouwen, beheren delen en toepassen op uw rapporten. De filters laten u ondergroepen van bezoekers identificeren die op kenmerken of websiteinteractie worden gebaseerd. De filters worden ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en delen met andere teamleden.

Filters kunnen worden gebaseerd op kenmerken (type browser, apparaat, aantal bezoeken, land, geslacht), interacties (campagnes, sleutelwoordzoekactie, zoekmachine), uitgangen en ingangen (bezoekers van Facebook, een bepaalde landingspagina, verwijzend domein), douanevariabelen (vormgebied, bepaalde categorieën, klantenidentiteitskaart), en andere criteria.

U kunt filters in de Bouwer van de Filter bouwen en bewaren, of filters van een visualisatie van de Uitloop produceren (in Werkruimte). Bovendien kunnen de filters samen als gestapelde filters worden gebruikt.

>[!IMPORTANT]
De filters zijn genoemd geworden &quot;segmenten&quot;in de Analyse van Adobe. Wij noemden segmenten aan filters anders omdat het Platform van de Ervaring van Adobe een verschillende definitie van &quot;segment&quot;heeft. Een segment in AEP verwijst naar...

Het filtreren omvat de Bouwer [van de](/help/components/filters/create-filters.md) Filter om filters te construeren en een pre-test in werking te stellen, en de Manager [van de](/help/components/filters/manage-filters.md) Filter om, veiligheidsfilters over uw organisatie te verzamelen, te etiketteren goed te keuren, te plaatsen en te delen.

## Sequentiële filters

De opeenvolgende filters laten u bezoekers identificeren die op navigatie en paginamening over uw plaats worden gebaseerd, die een filter van bepaalde acties en interactie verstrekken. De opeenvolgende segmenten helpen u identificeren wat een bezoeker houdt van en wat een bezoeker vermijdt. Wanneer de bouw van opeenvolgende filters, wordt de DEN exploitant gebruikt om bezoekersnavigatie te bepalen en te opdracht te geven.

Hier is een voorbeeld:

![](assets/sequential_fil.png)

| Bezoek One | Bezoek twee | Bezoek drie |
|---|---|---|
| De bezoeker ging naar de belangrijkste landingspagina (A), sloot de campagnepagina (B) uit, en bekeek dan de pagina van het Product (C). | De bezoeker ging opnieuw naar de belangrijkste landingspagina (A), sloot de campagnepagina (B) uit, en ging opnieuw naar de pagina van het Product (C), en toen naar een nieuwe pagina (D). | De bezoeker ging en volgde die zelfde weg zoals bij de eerste en tweede bezoeken, toen uitgesloten pagina F om rechtstreeks naar een gerichte productpagina (G) te gaan. |

## Filtercontainers

De filters zijn gebaseerd op een persoon, een zitting en een gebeurtenis-vlakke hiërarchie gebruikend een genesteld containermodel. De genestelde containers staan u toe om persoonattributen en acties te bepalen die op regels tussen en binnen de containers worden gebaseerd.

>[!NOTE]
>De container van de Persoon was vroeger bekend als de container van de Bezoeker. De container van de Zitting werd genoemd de container van het Bezoek, en de container van de Gebeurtenis was de container van de HAAR.

Een filter plaatst voorwaarden om een bezoeker te filtreren die op zijn of haar attributen of interactie met uw plaats wordt gebaseerd. Om voorwaarden in een filter te plaatsen, plaatst u regels aan filterbezoekers die op bezoekerskenmerken en/of navigatiekenmerken worden gebaseerd. Om bezoekersgegevens verder uit te splitsen, kunt u filteren op basis van specifieke bezoeken en/of paginamening hits voor elke bezoeker. De Bouwer van de Filter verstrekt een eenvoudige architectuur om deze ondergroepen te bouwen en regels toe te passen zoals genesteld, hiërarchische Persoon, Zitting, of de containers van de Gebeurtenis.

De containerarchitectuur die in de Bouwer van de Filter wordt gebruikt bepaalt Persoon als buitenste container, die overkoepelende gegevens bevat specifiek voor de bezoeker over bezoeken en paginameningen. Een genestelde container van de Zitting laat u regels plaatsen om de gegevens van de bezoeker te onderbreken die op zittingen worden gebaseerd, en een genestelde container van de Gebeurtenis laat u bezoekersinformatie onderbreken die op individuele paginameningen wordt gebaseerd. Elke container laat u over de geschiedenis van een bezoeker, interactie melden die door zittingen, of individuele gebeurtenissen worden uitgesplitst.

### Personen container

De container van de Persoon omvat elk bezoek en paginamening voor bezoekers binnen een gespecificeerd tijdkader. Een filter op het niveau van de Persoon keert de pagina terug die aan de voorwaarde plus alle andere pagina&#39;s voldoet die door de bezoeker worden bekeken (en slechts beperkt door bepaalde datumwaaiers). Als meest breed-bepaalde container, zullen de rapporten die op het de containerniveau van de Persoon worden geproduceerd paginameningen over alle bezoeken terugkeren en laat u een multi-bezoek analyse produceren. Bijgevolg is de container van de Persoon het meest vatbaar voor verandering die op bepaalde datumwaaiers wordt gebaseerd.
De containers van de persoon kunnen waarden omvatten die op de algemene geschiedenis van een bezoeker worden gebaseerd:

* Dagen vóór eerste aankoop

* Oorspronkelijke invoerpagina

* Oorspronkelijke verwijzende Domeinen

### Sessiecontainer

De container van de Zitting laat u paginainteractie, campagnes, of omzettingen voor een specifieke zitting identificeren. De container van de Zitting is de het meest meestal gebruikte container omdat het gedrag voor de volledige bezoekzitting vangt zodra de regel wordt ontmoet en u laat bepalen welke zittingen u in de bouw van en het toepassen van een segment wilt omvatten of uitsluiten. Het kan u helpen deze vragen beantwoorden:

* Hoeveel bezoekers bekeken de sectie van het Nieuws en van de Sport in de zelfde zitting?

* Welke pagina&#39;s droegen tot een succesvolle omzetting aan een verkoop bij?

De containers van de zitting omvatten waarden die op voorkomen per zitting worden gebaseerd:

* Sessienummer

* Entry Page

* Retourfrequentie

* Deelnamemetriek

* Lineariteit toegewezen metriek

### Gebeurteniscontainer

De container van de Gebeurtenis bepaalt welke paginagebeurtenissen u van een filter zou willen omvatten of uitsluiten. Het is het smal van de beschikbare containers om u te laten specifieke kliks en paginamening identificeren waar een voorwaarde waar is, latend u één enkele het volgen code bekijken, of gedrag binnen een bepaalde sectie van uw plaats isoleren. U kunt een specifieke waarde ook willen aanwijzen wanneer een actie, zoals het marketing kanaal voorkomt wanneer een orde werd geplaatst.

De containers van de gebeurtenis omvatten waarden gebaseerde enige paginaonderverdelingen:

* Producten

* Props voor lijst

* Afmetingen lijst

* Merchandising-dimensies (in het kader van gebeurtenissen)