---
title: Overzicht van filters
description: Begrijp waarvoor filters worden gebruikt en hoe u een eenvoudig filter maakt.
exl-id: 21183e98-6593-4b22-99c7-4a03231acfe9
source-git-commit: 4564b2d33e2222c7ad3e2db3c85b5a27d70d05ee
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 1%

---

# Overzicht van filters

Met Customer Journey Analytics kunt u krachtige, doelgerichte publieksfilters maken, beheren, delen en toepassen op uw rapporten. Met filters kunt u subsets van bezoekers identificeren op basis van eigenschappen of interacties van websites. Filters zijn ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en met andere teamleden kunt delen.

Filters kunnen worden gebaseerd op kenmerken (browsertype, apparaat, aantal bezoeken, land, geslacht), interacties (campagnes, trefwoordzoeker, zoekmachine), uitgangen en items (bezoekers uit Facebook, een gedefinieerde bestemmingspagina, verwijzingsdomein), aangepaste variabelen (formulierveld, gedefinieerde categorieën, klant-id) en andere criteria.

U kunt filters bouwen en bewaren in de Bouwer van de Filter, of filters van een visualisatie van de Vallout (in Werkruimte) produceren. Bovendien kunnen filters samen als gestapelde filters worden gebruikt.

Filteren omvat [Filter Builder](/help/components/filters/create-filters.md) om filters te construeren en een pretest in werking te stellen, en [de Manager van de Filter](/help/components/filters/manage-filters.md) om filters over uw organisatie te verzamelen, te etiketteren, goed te keuren, veiligheid te plaatsen, en te delen.

## Opeenvolgende filters

Met opeenvolgende filters kunt u bezoekers identificeren op basis van navigatie en paginaweergave op uw site. Zo beschikt u over een filter met gedefinieerde handelingen en interacties. Met behulp van opeenvolgende filters kunt u bepalen wat een bezoeker leuk vindt en wat een bezoeker vermijdt. Wanneer het bouw van opeenvolgende filters, wordt de exploitant THEN gebruikt om bezoekersnavigatie te bepalen en te ordenen.

Hier volgt een voorbeeld:

![](assets/sequential_fil.png)

| Eén bezoeken | Twee bezoeken | Drie bezoeken |
| --- | --- | --- |
| De bezoeker ging naar de hoofdlandingspagina (A), sloot de campagnepagina (B) uit en bekeken de productpagina (C). | De bezoeker ging opnieuw naar de hoofdbestemmingspagina (A), sluit de campagnepagina (B) uit, en ging opnieuw naar de productpagina (C) en vervolgens naar een nieuwe pagina (D). | De bezoeker ging en volgde hetzelfde pad als bij de eerste en tweede bezoeken, en sloot vervolgens pagina F uit om rechtstreeks naar een bepaalde productpagina (G) te gaan. |

## Filtercontainers

Filters zijn gebaseerd op een hiërarchie op Person-, Session- en Gebeurtenisniveau met behulp van een genest containermodel. Met de geneste containers kunt u persoonkenmerken en handelingen definiëren op basis van regels tussen en binnen de containers.

>[!NOTE]
>De container Person werd voorheen de container van de Bezoeker genoemd. De container van de Zitting werd genoemd de container van het Bezoek, en de container van de Gebeurtenis gebruikte om de container van het Actief te zijn.

Een filter stelt voorwaarden in om een bezoeker te filteren op basis van zijn of haar kenmerken of interacties met uw site. Als u voorwaarden in een filter wilt instellen, stelt u regels in om bezoekers te filteren op basis van de kenmerken van de bezoeker en/of navigatiekenmerken. Als u bezoekersgegevens verder wilt onderverdelen, kunt u filteren op basis van specifieke bezoeken en/of toeschouwers in de paginaweergave voor elke bezoeker. De Bouwer van de Filter verstrekt een eenvoudige architectuur om deze subsets te bouwen en regels als genestelde, hiërarchische Persoon, Zitting, of de containers van de Gebeurtenis toe te passen.

De containerarchitectuur die in de Bouwer van de Filter wordt gebruikt bepaalt Persoon als buitenste container, die overkoepelende gegevens specifiek voor de bezoeker over bezoeken en paginameningen bevat. Met een geneste container voor sessies kunt u regels instellen om de gegevens van de bezoeker op basis van sessies op te splitsen. Met een geneste container voor gebeurtenissen kunt u bezoekersinformatie opsplitsen op basis van afzonderlijke paginaweergaven. Met elke container kunt u de geschiedenis van een bezoeker, interacties die zijn opgesplitst naar sessie, of afzonderlijke gebeurtenissen onderverdelen.

### Persoonscontainer

De container Person bevat elk bezoek en elke paginaweergave voor bezoekers binnen een opgegeven tijdsperiode. Een filter op het niveau van de Persoon keert de pagina terug die aan de voorwaarde plus alle andere pagina&#39;s voldoet die door de bezoeker (en slechts beperkt door bepaalde datumwaaiers) worden bekeken. Als meest breed-bepaalde container, zullen de rapporten die op het niveau van de container van de Persoon worden geproduceerd paginameningen over alle bezoeken terugkeren en laat u een multi-bezoek analyse produceren. Daarom is de container van de Persoon het meest vatbaar om te veranderen gebaseerd op bepaalde datumwaaiers.
De containers van de persoon kunnen waarden omvatten die op de algemene geschiedenis van een bezoeker worden gebaseerd:

* Dagen vóór eerste aankoop
* Oorspronkelijke invoerpagina
* Oorspronkelijke verwijzende domeinen

### Sessiecontainer

Met de container Sessie kunt u paginainteracties, campagnes of conversies voor een specifieke sessie identificeren. De container van de Zitting is de gemeenschappelijkste gebruikte container omdat het gedrag voor de volledige bezoekzitting vangt zodra de regel wordt ontmoet en u laat bepalen welke zittingen u in de bouw en het toepassen van een filter wilt omvatten of uitsluiten. Het kan u helpen deze vragen beantwoorden:

* Hoeveel bezoekers hebben de sectie Nieuws en Sport in dezelfde sessie bekeken?
* Welke pagina&#39;s hebben bijgedragen tot een geslaagde omzetting in een uitverkoop?

Sessiecontainers bevatten waarden die zijn gebaseerd op de aanwezigheid per sessie:

* Sessienummer
* Itempagina
* Retourfrequentie
* Deelnamemetriek
* Lineaire toegewezen metriek

### Gebeurteniscontainer

In de container Event wordt gedefinieerd welke paginagebeurtenissen u wilt opnemen in of uitsluiten van een filter. Het is het meest smalle van de beschikbare containers om u specifieke kliks en paginamening te laten identificeren waar een voorwaarde waar is, latend u één enkele het volgen code bekijken, of gedrag binnen een bepaalde sectie van uw plaats isoleren. U kunt ook een specifieke waarde aanwijzen wanneer een handeling plaatsvindt, zoals het marketingkanaal wanneer een order is geplaatst.

Gebeurteniscontainers bevatten op waarden gebaseerde uitsplitsingen van één pagina:

* Producten
* Props weergeven
* Lijstafmetingen
* Merchandising-afmetingen (in de context van gebeurtenissen)

## Filtersjabloon buiten de box

Traditionele analyse wordt geleverd met veel out-of-the-box sjabloonfilters (filters) en berekende meetgegevens. Veel van deze regels zijn niet van toepassing op CJA of moeten worden hernoemd of opnieuw worden gemaakt. Andere zullen van een oplossing voor context-bewuste variabelen in CJA afhangen.

| Filternaam | Beschrijving |
| --- | --- |
| Alle gegevens | Dit is een vereist filter dat dynamisch aan het melden wordt toegevoegd wanneer metrisch aan de rij van een lijst Freeform wordt toegevoegd. |
