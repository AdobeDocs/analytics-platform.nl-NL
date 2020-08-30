---
title: Overzicht filters
description: Begrijp welke filters voor worden gebruikt en hoe te om een eenvoudige filter tot stand te brengen.
translation-type: tm+mt
source-git-commit: 09dcb36b96d95276b357e0f1308a977f5db5d711
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 1%

---


# Overzicht filters

Met de analyse van de reis van de klant kunt u krachtige, gerichte publieksfilters op uw rapporten bouwen, beheren, delen en toepassen. De filters laten u ondergroepen van bezoekers identificeren die op kenmerken of websiteinteractie worden gebaseerd. De filters worden ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en delen met andere teamleden.

Filters kunnen gebaseerd zijn op kenmerken (browsertype, apparaat, aantal bezoeken, land, geslacht), interacties (campagnes, trefwoordzoekers, zoekmachine), uitgangen en ingangen (bezoekers van Facebook, een gedefinieerde landingspagina, verwijzend domein), aangepaste variabelen (formulierveld, gedefinieerde categorieën, klantnummer) en andere criteria.

U kunt filters in de Bouwer van de Filter bouwen en bewaren, of filters van een visualisatie van de Uitloop (in Werkruimte) produceren. Bovendien kunnen de filters samen als gestapelde filters worden gebruikt.

>[!IMPORTANT]
>De filters zijn genoemd geworden &quot;segmenten&quot;in de Analyse van Adobe. Wij noemden segmenten aan filters anders omdat het Platform van de Ervaring van Adobe een verschillende definitie van &quot;segment&quot; heeft.

Het filteren omvat [Filter ontwerper](/help/components/filters/create-filters.md) om filters te construeren en een voortest uit te voeren, en [Filter Manager](/help/components/filters/manage-filters.md) om filters over uw organisatie te verzamelen, te etiketteren, goed te keuren, te plaatsen en te delen.

## Sequentiële filters

De opeenvolgende filters laten u bezoekers identificeren die op navigatie en paginamening over uw plaats worden gebaseerd, die een filter van bepaalde acties en interactie verstrekken. De opeenvolgende segmenten helpen u identificeren wat een bezoeker houdt van en wat een bezoeker vermijdt. Wanneer de bouw van opeenvolgende filters, wordt de DEN exploitant gebruikt om bezoekersnavigatie te bepalen en opdracht te geven.

Hier is een voorbeeld:

![](assets/sequential_fil.png)

| Bezoek één | Bezoek twee | Bezoek drie |
|---|---|---|
| De bezoeker ging naar de belangrijkste landingspagina (A), sloot de campagnepagina (B) uit, en bekeek dan de pagina van het Product (C). | De bezoeker ging opnieuw naar de belangrijkste landingspagina (A), sloot de campagnepagina (B) uit, en ging opnieuw naar de pagina van het Product (C), en toen naar een nieuwe pagina (D). | De bezoeker ging en volgde dezelfde weg als bij de eerste en tweede bezoeken, en sloot vervolgens pagina F uit om rechtstreeks naar een gerichte productpagina (G) te gaan. |

## Filtercontainers

De filters zijn gebaseerd op een Person-, Zitting- en Gebeurtenis-vlakke hiërarchie gebruikend een genesteld containermodel. De genestelde containers staan u toe om persoonattributen en acties te bepalen die op regels tussen en binnen de containers worden gebaseerd.

>[!NOTE]
>De container van de Persoon was vroeger gekend als de container van de Bezoeker. De container van de Zitting werd genoemd de container van het Bezoek, en de container van de Gebeurtenis die werd gebruikt om de container van de HAAR te zijn.

Een filter plaatst voorwaarden om een bezoeker te filtreren die op zijn of haar attributen of interactie met uw plaats wordt gebaseerd. Om voorwaarden in een filter te plaatsen, plaatst u regels aan filterbezoekers die op de kenmerken van de bezoeker en/of navigatiekenmerken worden gebaseerd. Om bezoekersgegevens verder uit te splitsen, kunt u filteren op basis van specifieke bezoeken en/of paginamening hits voor elke bezoeker. De ontwerper van de Filter verstrekt een eenvoudige architectuur om deze ondergroepen te bouwen en regels toe te passen zoals genestelde, hiërarchische Persoon, Zitting, of de containers van de Gebeurtenis.

De containerarchitectuur die in de Bouwer van de Filter wordt gebruikt bepaalt Persoon als buitenste container, die overkoepelende gegevens bevat specifiek voor de bezoeker over bezoeken en paginameningen. Een genestelde container van de Zitting laat u regels plaatsen om de gegevens van de bezoeker te onderbreken die op zittingen worden gebaseerd, en een genestelde container van de Gebeurtenis laat u bezoekersinformatie onderbreken die op individuele paginameningen wordt gebaseerd. Elke container laat u over de geschiedenis van een bezoeker, interactie melden die door zittingen, of individuele gebeurtenissen worden verdeeld.

### Personcontainer

De container van de Persoon omvat elk bezoek en paginamening voor bezoekers binnen een gespecificeerd tijdkader. Een filter op het niveau van de Persoon keert de pagina terug die aan de voorwaarde plus alle andere pagina&#39;s voldoet die door de bezoeker worden bekeken (en slechts beperkt door bepaalde datumwaaiers). Als meest breed-bepaalde container, zullen de rapporten die op het de containerniveau van de Persoon worden geproduceerd paginameningen over alle bezoeken terugkeren en laat u een multi-bezoek analyse produceren. Bijgevolg is de container van de Persoon het meest vatbaar voor verandering die op bepaalde datumwaaiers wordt gebaseerd.
De containers van de persoon kunnen waarden omvatten die op de algemene geschiedenis van een bezoeker worden gebaseerd:

* Dagen vóór eerste aankoop

* Oorspronkelijke invoerpagina

* Oorspronkelijke verwijzende domeinen

### Sessiecontainer

De container van de Zitting laat u paginainteractie, campagnes, of omzettingen voor een specifieke zitting identificeren. De container van de Zitting is de het meest meestal gebruikte container omdat het gedrag voor de volledige bezoekzitting vangt zodra de regel wordt ontmoet en u laat bepalen welke zittingen u in de bouw van en het toepassen van een segment wilt omvatten of uitsluiten. Het kan u helpen deze vragen beantwoorden:

* Hoeveel bezoekers bekeken de sectie van het Nieuws en van de Sport in de zelfde zitting?

* Welke pagina&#39;s droegen bij tot een succesvolle omzetting in een verkoop?

De containers van de zitting omvatten waarden die op voorkomen per zitting worden gebaseerd:

* Sessienummer

* Entry Page

* Retourfrequentie

* Deelnamemetriek

* lineaire toegewezen maatstaven

### Gebeurteniscontainer

De container van de Gebeurtenis bepaalt welke paginagebeurtenissen u van een filter zou willen omvatten of uitsluiten. Het is het meest smalle van de beschikbare containers om u specifieke kliks en paginamening te laten identificeren waar een voorwaarde waar is, latend u één enkele het volgen code bekijken, of gedrag binnen een bepaalde sectie van uw plaats isoleren. U kunt een specifieke waarde ook willen aanwijzen wanneer een actie, zoals het op de markt brengende kanaal voorkomt wanneer een orde werd geplaatst.

De containers van de gebeurtenis omvatten waarden gebaseerde enige paginaonderverdelingen:

* Producten

* Props voor lijst

* Lijstafmetingen

* Merchandising-dimensies (in het kader van gebeurtenissen)