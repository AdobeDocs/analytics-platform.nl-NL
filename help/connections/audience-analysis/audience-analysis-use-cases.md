---
title: Gebruiksscenario's voor analyse van publiek
description: Leer gebruiksgevallen voor Audience Analysis.
solution: Customer Journey Analytics
feature: Audiences
role: Admin
hide: true
hidefromtoc: true
source-git-commit: 974d8a269be15d3ea6fbbcf96f2ab5457d9c9554
workflow-type: tm+mt
source-wordcount: '1484'
ht-degree: 0%

---

# Gebruiksgevallen van de analyse van het publiek {#analyze-audiences-use-cases}

De Analyse van het publiek laat de rapportering van de gegevens van het het publiekslidmaatschap van Experience Platform in Customer Journey Analytics toe. Dit wordt bereikt door configuraties die via de de configuratietovenaar van de Analyse van de Publiek worden beheerd, die u helpt bepalen welke profieldataset u, naast andere parameters en configuratiedetails opneemt. (Voor meer gedetailleerde overzichtsinformatie, zie [&#x200B; Overzicht van de Analyse van de Analyse van het publiek &#x200B;](/help/connections/audience-analysis/audience-analysis-overview.md).)

Dit document bevat voorbeelden van gebruiksgevallen die de waarde markeren die Audience Analysis biedt. Voordat u de gebruiksgevallen herziet, dient u eerst de onderstaande rapporteringsoverwegingen te kennen. Het is belangrijk om deze overwegingen in mening te houden wanneer het gaan over uw gebruiksgevallen, aangezien zij de definitieve output van uw rapporten kunnen beïnvloeden.

## Rapporteringsoverwegingen

De eerste release van de Audience Analysis legt de basis voor het verwerken en opnemen van Experience Platform-publiek in Customer Journey Analytics. Bij het maken van uw analyse is het belangrijk om rekening te houden met verschillende factoren die van invloed kunnen zijn op uw resultaten in Workspace-projecten:

* **de lidmaatschapsgegevens van het publiek zijn nauwkeurig slechts voor de vorige dag (&quot;gisteren&quot;)**: De gegevens van het het lidmaatschapslidmaatschap van het publiek zullen altijd de recentste dataset van de profielmomentopname bevatten die door de Verenigde Dienst van het Profiel wordt geproduceerd. Deze profieldataset is een dagelijkse momentopname en is nauwkeurig slechts voor de vorige dag (&quot;gisteren&quot;), met het automatisch wordt opnieuw geproduceerd en elke nacht opnieuw verwerkt. De dimensies van het publiek zijn beschikbaar voor rapportering en onderverdelingen, niet voor het reconstrueren van historische publieksstaten.

   * Voorbeeld: ongeacht het gekozen rapportagetijdvenster zal het te rapporteren publiek van CJA altijd de status van het publiekslidmaatschap respecteren die aanwezig is in de nieuwste opgenomen profielmomentopname (&quot;gisteren&quot;).

      * Als u het venster met de rapporttijd bijvoorbeeld vergroot tot &quot;30 dagen geleden&quot;, worden er meer gebeurtenissen weergegeven en krijgt u de indruk dat de omvang van het publiek verandert. Nochtans, zal de het profielsamenstelling van het publiek altijd de momentopname van &quot;gisteren&quot;ongeacht het gekozen tijdvenster aanpassen.

* **de Afmetingen moeten een overeenkomstige gebeurtenis hebben om worden omvat**: De dimensies van de Analyse van het publiek kunnen slechts worden geanalyseerd waar de overeenkomstige gebeurtenissen in CJA bestaan. Als een gedrag-, kanaal- of levenscyclusmoment niet wordt weergegeven als een gebeurtenis in de CJA-verbinding, kan dit niet worden geanalyseerd.

   * Voorbeeld: een publiek dat wordt gebruikt om mensen met een advertentie als doelgroep te gebruiken, zou aanzienlijk meer mensen in het RTCDP-publiek dan in het CJA-publiek omvatten. Dit komt omdat het CJA-publiek beperkt is tot mensen die tijdens het rapportagevenster een gebeurtenis in CJA hebben gehad.

* **de resolutie van de Identiteit is uitsluitend gebaseerd op één enkele namespace**: De resolutie van de identiteit hangt volledig van geselecteerde identiteitsnamespace als deel van de configuratie van de Analyse van de Publiek af. De analyse zal aan genoemde identiteitsnamespace worden beperkt, met gebeurtenissen die buiten het vallen niet voor publieksanalyse het melden beschikbaar zijn.

   * Voorbeeld: voor een vastgemaakte gebeurtenisdataset die CRM en ECID combineert, en de configuratie van de Analyse van het Publiek gebruikt identiteitskaart van CRM, slechts rijen die een identiteitskaart van CRM bevatten zullen als deel van het te rapporteren publiek in CJA worden erkend. Daarom kan de resulterende publieksgrootte kleiner zijn dan verwacht.

## Voorbeelden van gebruiksgevallen

### Hoofdlettergebruik 1

Begrijp hoe een specifiek publiek zich in een bepaald kanaal (bijvoorbeeld, Web of app) gedraagt, om vragen als te beantwoorden:

* _&quot;Wat zijn leden van Hoogwaardige Vooruitzichten die momenteel op de plaats (pagina&#39;s, eigenschappen, trechters) doen?&quot;_

* _&quot;Welke campagnes en inhoud overindex voor dit publiek vergeleken met iedereen anders?&quot;_

#### Configuratiestroom

1. Vorm de Analyse van het Publiek in CJA voor één enkele identiteitsnamespace (b.v., ECID of CRM_ID) en een Web-based gegevensmening.

   * Hiermee worden de lidmaatschapsgegevens voor het publiek automatisch opgenomen in de door u gekozen verbinding via het exporteren van een momentopname voor dagelijkse profielen

   * Het wordt aanbevolen de naamruimte voor identiteiten te selecteren waarvan u denkt dat deze de meeste dekking heeft in uw gebeurtenisdataset

1. Bouw uw Workspace-projecten op:

   * De naam van het publiek opsplitsen op pagina, product, campagne, apparaat, enz.

   * Vergelijk publiek versus niet-publiek (of tegen een ander publiek) op metriek zoals zittingen, omzettingstarief, opbrengst per persoon.

1. Geef uw inzichten in kanaaloptimalisatiestrategieën door (bijvoorbeeld, richtend regels, inhoud of aanbieding het stemmen).

#### Overwegingen voor identiteitsoplossing

| Hoofdletters gebruiken | Kernzakelijke vraag | Overeenstemming over identiteitsresolutie | Hoog-auth/enig-namespace organisaties (gebeurtenissen reeds onder 1 persoonsidentiteitskaart, b.v. login /CRM) | Fragmented / multi-namespace instanties (gebeurtenissen onder ECID + CRM + anderen) |
|---------|----------|---------|---------|---------|
| Gedrag publiek met huidige status diep duik | _&quot;Wat doet publiek X momenteel in kanaal Y?&quot; (pagina&#39;s, treinen, inhoud, aanbiedingen)_ | Gebeurtenissen en profielen moeten één consistente naamruimte delen in de configuratie CJA-verbinding en Audience Analysis voor optimale dekking. | De meeste activiteit is al gekoppeld aan één login/CRM-id, zodat het publiek van AEP zich schitterend aansluit bij gedragsgegevens in CJA. <p>U krijgt een duidelijk beeld van wat elk publiek in een bepaald kanaal met minimale verwachte rapporteringshiaten doet.</p> | Zelfs wanneer verbonden met een verbonden dataset, zal het melden nog worden beperkt tot enige identiteit namespace die in de configuratie wordt gekozen. <p>Als sommige klanten onder andere IDs bestaan, zal hun gedrag niet worden omvat, wat in een gedeeltelijke mening tijdens het melden kan resulteren.</p> |

### Hoofdlettergebruik 2

Helpen marketers of reisontwerpers begrijpen welke soorten publiek overlappen, zodat ze ervaringen kunnen dedupliceren en conflicten tussen campagnes kunnen vermijden:

* _&quot;Hoeveel overlapping is er vandaag tussen Loyalty Leden, Kart Abandoner, en Hoge Volheid aan Churn?&quot;_

* _&quot;Welk publiek zal hoogstwaarschijnlijk aan de aanbiedingen van de hoge-waardebevordering deze week botsen?&quot;_

#### Configuratiestroom

1. Vorm de Analyse van het Publiek in CJA voor één enkele identiteitsnaamruimte die aan activering RTCDP/AJO wordt gericht (b.v., CRM_ID als de reizen op mensen-gebaseerd zijn).

   * Hiermee worden automatisch de lidmaatschapsgegevens voor het publiek opgenomen in de door u gekozen verbinding via het exporteren van momentopnamen voor dagelijkse profielen.

   * Dit kan worden gebruikt om een bestaande gegevensweergave te verrijken die al belangrijke betrokkenheid- en conversierapporten mogelijk maakt.

1. Gebruik het uit-van-de-doos malplaatje van het Overzicht van de Analyse van de Publiek en overlappende visualisaties:

   * Doorsnede maken van het publiek en over-/onderindexeringsweergaven uitvoeren (bijvoorbeeld % van de afgetekende kaartjes die ook in Loyalty Gold zitten).

   * Segmentoverlap op basis van kernafmetingen (bijv. apparaattype, productinteresse) om te begrijpen waar conflicten het belangrijkst zijn.

1. Gebruik de inzichten om kritieke aspecten te verfijnen, zoals:

   * Conflictregels of regels voor marketingacties aanbieden in RTCDP en AJO.

   * Poortverfijning (bijv. aanscherpende doeldefinities waarbij de overlapping te hoog is).

#### Overwegingen voor identiteitsoplossing

| Hoofdletters gebruiken | Kernzakelijke vraag | Overeenstemming over identiteitsresolutie | Hoog-auth/enig-namespace organisaties (gebeurtenissen reeds onder 1 persoonsidentiteitskaart, b.v. login /CRM) | Fragmented / multi-namespace instanties (gebeurtenissen onder ECID + CRM + anderen) |
|---------|----------|---------|---------|---------|
| Poortoverlapping en botsingdetectie | _&quot;Welk publiek overlapt vandaag zodat kunnen wij aanbiedingsbotsingen vermijden?&quot;_ | Overlappen wordt alleen berekend voor publiek dat dezelfde persoon-id gebruikt en met activiteit in de CJA-verbinding. | Omdat de meeste activiteit reeds aan één enkele login/identiteitskaart van CRM verbonden is, wordt dit verwacht om een betrouwbare overlappende kaart over publiek te verstrekken. <p>Met overlappende diagrammen krijgt u een betrouwbaar beeld van welke doelgroepen botsen en waar onderdrukkingen of prioriteitsregels moeten worden toegepast.</p> | Als delen van de reis onder andere IDs (b.v. anonieme ECID-Enige doorbladeren, vraag-centrum IDs) leven, zullen die gebeurtenissen niet in overlappende analyse verschijnen. <p>Mensen kunnen nog steeds in meerdere naamruimten voorkomen.</p><p>De overlapping wordt gebaseerd op de naamruimte van de identiteit die is opgenomen in de configuratie. Als sommige profielen nog over IDs verdelen, kan de overlapping ware botsingen onderrapporteren.</p> |

### Hoofdlettergebruik 3

Begrijp het gedrag van klanten die onlangs een zeer belangrijk publiek verlaten en wat zij rond die uitgang deden, om vragen als te beantwoorden:

* _&quot;Who enkel verlaten een zeer belangrijk publiek, en wat deden zij rond uitgang?&quot;_

* _&quot;Wat gebeurde er vlak voor het afsluiten? (fouten, lage betrokkenheid, prijsveranderingen).&quot;_

#### Configuratiestroom

1. Analyse van publiek in CJA configureren voor één naamruimte voor identiteit (bijvoorbeeld CRM_ID of aanmeldings-id) en de relevante gegevensweergaven (web, app, CRM, enz.).

   * Hierdoor worden automatisch de gegevens van het publiekslidmaatschap opgenomen in de door u gekozen verbinding via het exporteren van momentopnamen voor dagelijkse profielen.

   * Men adviseert dat u identiteitsnamespace selecteert die u de meeste dekking in uw gebeurtenisdataset gelooft.

1. In het het overzichtsmalplaatje van de Analyse/van het Publiek (dat aan _wordt bevestigd gisteren_), gebruik:

   * Huidige leden: nog steeds in het publiek

   * Verlaat publiek: die gisteren vertrok

1. Bouw uw Workspace-projecten op:

   * Filter naar profielen die Audience X gisteren weggingen, dan bekijk:

      * Hun gedrag dat tot uitgang leidt (laatste zittingen, fouten, prijs/aanbiedingsblootstelling, kanaalmix).

      * Hun gedrag na het afsluiten (schakelden ze over naar een ander product, verlagen ze, gaan ze in slaapstand).

   * Breek die verlaten cohort neer door gebied, apparaat, tenure, waarderij om high-impact zakken te vinden.

1. Gebruik de inzichten voor reis updates en win-back publieksconfiguraties in RTCDP of AJO.

#### Overwegingen voor identiteitsoplossing

| Hoofdletters gebruiken | Kernzakelijke vraag | Overeenstemming over identiteitsresolutie | Hoog-auth/enig-namespace organisaties (gebeurtenissen reeds onder 1 persoonsidentiteitskaart, b.v. login /CRM) | Fragmented / multi-namespace instanties (gebeurtenissen onder ECID + CRM + anderen) |
|---------|----------|---------|---------|---------|
| Geëxporteerde soorten publiek - chroonanalyse | _&quot;Who just left a key publiek?&quot;_ <p>_&quot;Wat deden zij rond uitgang?&quot;_</p> | De uitgang van het publiek wordt gevolgd bij zelfde persoon identiteitskaart die voor de verbinding en publieksconfiguratie wordt gebruikt. | Afsluiten gemeten op een stabiele login/CRM-id weerspiegelt doorgaans de werkelijke gedragswijziging. <p>Wanneer iemand een publiek verlaat op deze id, betekent dit meestal een echte verandering (klonen, downgraden, inactiviteit).</p><p>U kunt hun recente gedrag analyseren om reizen en win-back aanbiedingen met vertrouwen te verfijnen.</p> | Afsluiten is alleen zichtbaar waar profielen en gebeurtenissen de geconfigureerde id delen en dus een zorgvuldige interpretatie vereisen.<p>Gebruik verlaten cohorts als sterke wenk of signaal, maar het wordt geadviseerd dat u met andere gegevenspunten vóór kritieke besluiten kruist.</p> |

