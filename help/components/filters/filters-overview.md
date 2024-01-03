---
title: Overzicht van filters
description: Begrijp waarvoor filters worden gebruikt en hoe u een eenvoudig filter maakt.
exl-id: 21183e98-6593-4b22-99c7-4a03231acfe9
feature: Filters
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 0%

---


# Overzicht van filters {#overview}

Met Customer Journey Analytics kunt u krachtige, doelgerichte publieksfilters maken, beheren, delen en toepassen op uw rapporten. Met filters kunt u subsets van personen identificeren op basis van kenmerken of interacties. Filters zijn ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en met andere teamleden kunt delen.

Filters kunnen worden gebaseerd op

- kenmerken (browsertype, apparaat, aantal bezoeken, land, geslacht);
- interacties (campagnes, trefwoordzoekers, zoekmachines);
- uitgang en binnenkomst (personen uit Facebook, een bepaalde landingspagina, verwijzend domein, gebeurtenis geofence);
- aangepaste variabelen (formulierveld, gedefinieerde categorieën, klant-id),
- en andere criteria.

U kunt filters bouwen en bewaren in de Bouwer van de Filter, of filters van een visualisatie van de Vallout (in Werkruimte) produceren. Bovendien kunnen filters samen als gestapelde filters worden gebruikt.

Filteren bevat de opdracht [Filter Builder](/help/components/filters/filter-builder.md) om filters te maken en een pretest uit te voeren, en [Filterbeheer](/help/components/filters/manage-filters.md) om filters te verzamelen, te etiketteren, goed te keuren, veiligheid te plaatsen, en over uw organisatie te delen.

Het maximumaantal filters dat u per IMS-organisatie kunt maken, is 50.000.

## Filtertypen {#types}

Voor informatie over de beschikbare typen filters en hoe u deze kunt maken, raadpleegt u [Filters maken](/help/components/filters/create-filters.md).

## Opeenvolgende filters {#sequential}

Met opeenvolgende filters kunt u personen identificeren op basis van navigatie (paginaweergaven op uw site, interactie met scènes in uw mobiele app of via een menu in een set-top box). De opeenvolgende filters verstrekken een filter van bepaalde acties en interactie en helpen u identificeren wat een persoon houdt en wat een persoon vermijdt. Wanneer het bouwen van opeenvolgende filters, wordt de exploitant THEN gebruikt om persoonnavigatie te bepalen en te ordenen.

>[!IMPORTANT]
>
>U moet beschikken over **Selecteren** pakket maken om opeenvolgende filters voor meerdere kanalen te maken. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

Hier volgt een voorbeeld:

| Sessie één | Sessie twee | Sessie drie |
| --- | --- | --- |
| De persoon ging naar hoofdlandingspagina A, sloot de campagnepagina B uit en keek vervolgens naar productpagina C. | De persoon ging opnieuw naar de hoofdbestemmingspagina A, sloot de campagnepagina B uit en ging opnieuw naar productpagina C en vervolgens naar een nieuwe pagina D. | De persoon heeft dezelfde weg ingeslagen en gevolgd als bij de eerste en tweede bezoeken, en vervolgens pagina F uitgesloten om rechtstreeks naar een bepaalde productpagina G te gaan. |

## Filtercontainers {#containers}

Filters zijn gebaseerd op een hiërarchie op persoon-, sessie- en gebeurtenisniveau met behulp van een genest containermodel. Met de geneste containers kunt u persoonkenmerken en handelingen definiëren op basis van regels tussen en binnen de containers.


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
>De Person container werd voorheen de Bezoeker container genoemd. De container van de Zitting werd genoemd de container van het Bezoek, en de container van de Gebeurtenis gebruikte om de container van het Actief te zijn.

Een filter stelt voorwaarden in om een persoon te filteren op basis van de kenmerken of interacties van die persoon met uw site, mobiele app of een ander apparaattype waarvan u gegevens hebt verzameld. Als u de voorwaarden in een filter wilt instellen, stelt u regels in voor het filteren van personen op basis van persoonlijke kenmerken en/of navigatiekenmerken. Als u de persoongegevens verder wilt opsplitsen, kunt u filteren op basis van specifieke bezoeken en/of treffers in de paginaweergave, schermtikken en menuopties in een set-top box voor elke persoon. Maar filter ook op attributen die u van een CRM of loyaliteitssysteem hebt gegeten. De Bouwer van de Filter verstrekt een eenvoudige architectuur om deze subsets te bouwen en regels als genestelde, hiërarchische Persoon, Zitting, of de containers van de Gebeurtenis toe te passen.

De containerarchitectuur die in de Bouwer van de Filter wordt gebruikt bepaalt Persoon als buitenste container. De container bevat overkoepelende gegevens die specifiek zijn voor de persoon in verschillende bezoeken en paginaweergaven, mobiele toepassingsschermen of menuschermen in een set-top box. Met een geneste Session-container kunt u regels instellen om de gegevens van de persoon op basis van sessies te splitsen. Met een geneste Event-container kunt u de persoonlijke gegevens op basis van individuele interacties onderbreken. Elke container laat u over de geschiedenis van een persoon, interactie melden die door zittingen worden verdeeld, of individuele ervaringsgebeurtenissen onderverdelen.

### Persoonscontainer {#person}

De container van de Persoon omvat elk bezoek en paginamening, mobiel toepassingsscherm, reeks-hoogste doos, of console-spel interactie voor personen binnen een gespecificeerd tijdkader. In feite, elke ervaringsgebeurtenis die deel van de datasets uitmaakt die u binnen uw verbinding van de Customer Journey Analytics hebt bepaald. Een filter op Personniveau retourneert de paginaweergaven, de mobiele app of de set-top box schermen die aan de voorwaarde voldoen. Plus alle andere interactie door die zelfde persoon over online en off-line kanalen (en slechts beperkt door bepaalde datumwaaiers). Als meest algemeen bepaalde container, keert de rapporten die op het niveau van de container van de Persoon worden geproduceerd paginameningen, mobiele toepassingsschermen, en meer, over alle bezoeken terug en laat u een multi-bezoek kanaalanalyse produceren. Daarom is de container van de Persoon het meest vatbaar om te veranderen gebaseerd op bepaalde datumwaaiers.
De containers van de persoon kunnen waarden omvatten die op de algemene geschiedenis van een persoon worden gebaseerd:

- Dagen vóór eerste aankoop
- Oorspronkelijke instappagina of het startscherm van de mobiele toepassing
- Oorspronkelijke verwijzende domeinen

### Sessiecontainer {#session}

Met de Sessiecontainer kunt u paginainteracties of mobiele toepassingsinteracties, campagnes of conversies voor een specifieke sessie identificeren. De container van de Zitting is de gemeenschappelijkste gebruikte container omdat het gedrag voor de volledige bezoekzitting vangt zodra de regel wordt ontmoet. Met de container Sessie kunt u ook definiëren welke sessies u wilt opnemen in het samenstellen en toepassen van een filter. Het kan u helpen de volgende vragen beantwoorden:

- Hoeveel zittingen betrokken met zowel Web als de gegevensbronnen van het Centrum van de Vraag?
- Welke pagina&#39;s hebben bijgedragen tot een geslaagde omzetting in een uitverkoop?

Sessiecontainers bevatten waarden die zijn gebaseerd op de aanwezigheid per sessie:

- Sessietype
- Itempagina
- Geretourneerde frequentie
- Deelnamemetriek
- Lineaire toegewezen metriek

Met gegevensweergaven in Customer Journey Analytics kunt u bepalen hoe lang een sessie duurt, maar ook wanneer een nieuwe sessie moet worden gemaakt. U kunt bijvoorbeeld een nieuwe mobiele-toepassingssessie definiëren op basis van elke keer dat een gebruiker uw mobiele app start. Zie [Sessieinstellingen](/help/data-views/session-settings.md) voor meer informatie .

### Gebeurteniscontainer {#event}

De container van de Gebeurtenis bepaalt welke pagina, mobiele toepassing, of ander type van gebeurtenissen die u van een filter zou willen omvatten of uitsluiten. Het is het smaakst van de beschikbare containers om u specifieke kliks, paginamening, tikt op knoop in een mobiele app te identificeren waar een voorwaarde waar is. Met de container Event kunt u één trackingcode weergeven of gedrag isoleren binnen een bepaald gebied van uw mobiele app. U kunt ook een specifieke waarde aanwijzen wanneer een handeling plaatsvindt, zoals het marketingkanaal wanneer een order is geplaatst.

Gebeurteniscontainers bevatten op waarde gebaseerde uitsplitsingen van één pagina voor:

- Producten
- Props weergeven
- Lijstafmetingen
- Merchandising-afmetingen (in de context van gebeurtenissen)

## Filtersjabloon buiten de box {#template}

De traditionele Analytics komt met talrijke out-of-the-box malplaatjes en berekende metriek. Veel van deze regels zijn niet van toepassing in de Customer Journey Analytics of moeten worden hernoemd of opnieuw worden gemaakt. Andere zijn afhankelijk van een oplossing voor contextgevoelige variabelen in de Customer Journey Analytics.

| Filternaam | Beschrijving |
| --- | --- |
| Alle gegevens | Alle gegevens zijn een vereist filter dat dynamisch aan het melden wordt toegevoegd wanneer metrisch aan de rij van een lijst Freeform wordt toegevoegd. |
