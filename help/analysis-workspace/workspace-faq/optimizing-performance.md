---
description: 'null'
title: Analysis Workspace-prestaties optimaliseren
uuid: de51d03d-d555-4f0e-b19c-4a8f140770fc
translation-type: tm+mt
source-git-commit: d49e07d14d1b202d9cc12f42d60083c052a1c364
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 0%

---


# Analysis Workspace-prestaties optimaliseren

Bepaalde factoren kunnen de prestaties van een project binnen de Werkruimte van de Analyse beïnvloeden. Het is belangrijk om te weten wat die medewerkers zijn alvorens u begint een project te bouwen zodat u het project op de meest optimale manier kunt plannen en bouwen. Hieronder vindt u een lijst met factoren die van invloed zijn op de prestaties en best practices voor het optimaliseren van uw projecten. De prestaties van de Werkruimte van de analyse zijn één van de hoogste prioriteiten van Adobe en iets wij blijven elke dag verbeteren.

## Complexiteit van segmentlogica

De ingewikkelde segmenten kunnen een significante invloed op projectprestaties hebben. De factoren die ingewikkeldheid aan een segment (in dalende orde van invloed) toevoegen omvatten:

* Exploitanten van &quot;bevat&quot;, &quot;bevat een van&quot;, &quot;lucifers&quot;, &quot;begint met&quot; of &quot;eindigt met&quot;
* Sequentiële segmentatie, vooral wanneer afmetingsbeperkingen (binnen/na) worden gebruikt
* Het aantal unieke afmetingspunten binnen afmetingen die in het segment worden gebruikt (b.v., Pagina = &quot;A&quot;wanneer de Pagina 10 unieke punten heeft zal sneller zijn dan Pagina = &quot;A&quot;wanneer de Pagina 100000 unieke punten heeft)
* Het aantal verschillende dimensies dat wordt gebruikt (bv. Page = &#39;Home&#39; en Page = &#39;Zoekresultaten&#39; zal sneller zijn dan eVar 1 = &#39;rood&#39; en eVar 2 = &#39;blauw&#39;)
* Veel OF operatoren (in plaats van AND)
* Geneste containers met een verschillend toepassingsgebied (bv. &quot;Hit&quot; in &quot;Visit&quot; in &quot;Visitor&quot;)

**Beste praktijken voor logische complexiteit**

Terwijl sommige van de ingewikkeldheidsfactoren niet kunnen worden verhinderd, denk over kansen om de ingewikkeldheid van uw segmenten te verminderen. In het algemeen, specifieker kunt u met uw segmentcriteria zijn, beter. Bijvoorbeeld:

* Met containers, zal het gebruiken van één enkele container bij de bovenkant van het segment sneller dan een reeks genestelde containers zijn.
* Met exploitanten, zullen de &quot;gelijken&quot;sneller zijn dan &quot;bevat&quot;, en &quot;evenaart om het even welk van&quot;zal sneller zijn dan &quot;bevat om het even welk van&quot;.
* Met vele criteria, EN de exploitanten zullen sneller zijn dan een reeks OF exploitanten. Ook, zoek kansen om vele OF verklaringen in één enkele &quot;evenaart om het even welk van&quot;verklaring te verminderen.

Bovendien [classificaties](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html) kunt u helpen vele waarden in beknopte groepen consolideren waaruit u segmenten kunt maken. De segmentatie op classificatiegroepen verstrekt prestatiesvoordelen over segmenten die vele OF verklaringen bevatten of &quot;bevat&quot;criteria.

## Bereik van de gevraagde gegevens

De waaier van gegevens die door een project worden gevraagd zal de prestaties van de Werkruimte van de Analyse beïnvloeden.

**Beste praktijken voor datumbereiken**

Waar mogelijk, trek niet meer gegevens in dan u nodig hebt. Sluit de paneelkalender aan de relevante data voor uw analyse, of de componenten van het gebruiksdatumwaaier (paarse componenten) in uw vrije vormlijsten. De waaiers van de datum die in een lijst worden gebruikt treden de waaier van de paneeldatum met voeten. Bijvoorbeeld, kunt u vorige maand, vorige week en gisteren aan de lijstkolommen toevoegen om die specifieke waaiers van gegevens te verzoeken. Voor meer informatie bij het werken met datumwaaiers in de Werkruimte van de Analyse, horloge [deze video](https://www.youtube.com/watch?v=MIkT6FZ5gKk) .

Minimaliseer het aantal jaar-over-jaar vergelijkingen die in het project worden gebruikt. Bij de berekening van een vergelijking over de jaren heen, wordt gekeken naar de volledige 13 maanden van gegevens tussen de betrokken maanden. Dit heeft hetzelfde effect als het wijzigen van het bereik van de paneldatum in een periode van 13 maanden.

## Aantal visualisaties

Het aantal visualisaties in één project zal algemene ontvankelijkheid van de Werkruimte van de Analyse beïnvloeden. Dit is omdat elke visualisatie, of het een lijst of een grafiek is, een gegevensbron heeft die moet worden gevraagd.

**Beste praktijken voor het aantal visualisaties**

Verminder het aantal visualisaties in uw project. De Werkruimte van de analyse doet veel van verwerking achter de scènes voor elk visueel dat u toevoegt, zo voorrang geeft aan de beelden die voor de consument van het rapport het belangrijkst zijn en ondersteunende beelden in een afzonderlijk, meer gedetailleerd project uitbreken indien nodig.

## Complexiteit van visualisaties (segmenten, metriek, filters)

Het type visualisatie (bv. uitval versus een freeformlijst) dat aan een project zelf wordt toegevoegd beïnvloedt de projectprestaties niet zeer sterk. Het is de complexiteit van de visualisatie die de verwerkingstijd zal vergroten. De factoren die ingewikkeldheid aan een visualisatie toevoegen omvatten:

* Bereik van de gevraagde gegevens, zoals hierboven vermeld
* aantal toegepaste segmenten; bijvoorbeeld, segmenten die als rijen van een vrije vormlijst worden gebruikt
* Gebruik van ingewikkelde segmenten
* [Statisch item](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.html) rijen of kolommen in vrije vormlijsten
* Filters die op rijen in vrije vormlijsten worden toegepast
* Aantal inbegrepen metriek, vooral berekende metriek die segmenten gebruiken

**Beste praktijken voor visualisatiecomplexiteit**

Als u opmerkt dat uw projecten niet zo snel zoals u zou willen laden, probeer vervangend sommige segmenten met eVars en filters, waar mogelijk.

Als u constant gebruikend segmenten en berekende metriek voor gegevenspunten vindt die voor uw zaken belangrijk zijn, denk na verbeterend uw implementatie om deze gegevenspunten directer te vangen. Het gebruik van een markeringsmanager zoals de Lancering van het Platform van de Ervaring van Adobe en de verwerkingsregels van Adobe kunnen implementatieveranderingen snel en gemakkelijk aanbrengen om uit te voeren. Zie &#39;Complexiteit van Segmentlogica&#39; hierboven om beter te begrijpen hoe ingewikkelde segmenten kunnen worden vereenvoudigd.

## Aantal panelen

Één paneel kan vele visualisaties bevatten, en dientengevolge, kan het aantal panelen de algemene ontvankelijkheid van de Werkruimte van de Analyse ook beïnvloeden.

**Beste praktijken voor het aantal panelen**

Probeer niet om alles in één project toe te voegen, maar creeer afzonderlijke projecten die een specifiek doel of een groep belanghebbenden dienen. Gebruik tags om projecten in belangrijke thema&#39;s te organiseren en verwante projecten met groepen belanghebbenden te delen.

Als meer organisatie van projecten wordt gewenst, herinner dat [directe koppeling](https://www.youtube.com/watch?v=6IOEewflG2U) aan uw project is een optie. Creeer een interne index van projecten zodat de belanghebbenden gemakkelijker kunnen vinden wat zij nodig hebben.

Als vele panelen in één project nodig zijn, doen ineenstorten panelen alvorens en het delen te bewaren. Wanneer een project wordt geladen, zal de Werkruimte van de Analyse slechts inhoud voor de uitgebreide panelen laden. De samengevouwen panelen zullen niet worden geladen tot de gebruiker hen uitbreidt. Deze aanpak helpt op twee manieren:

* De samengevouwen panelen sparen op algemene ladingstijd van een project
* De samengevouwen panelen zijn een grote manier om uw projecten op een logische manier voor de consument van het rapport te organiseren

## Grootte van rapportsuite

De grootte van de rapportreeks kan als een drijvende factor schijnen, maar in werkelijkheid speelt het slechts een kleine rol in projectprestaties toe te schrijven aan hoe Adobe gegevensverwerking behandelt. Er kunnen uitzonderingen op deze regel zijn; overleg met uw implementatieteam of een deskundige van Adobe om te bepalen als er implementatieverbeteringen zijn die kunnen worden aangebracht om algemene ervaring in de Analyse van Adobe te verbeteren.

## Aantal gebruikers die gelijktijdig tot de Werkruimte van de Analyse toegang hebben

Het aantal gebruikers die tot de Werkruimte van de Analyse of specifieke projecten tezelfdertijd toegang hebben heeft geen wezenlijk effect op de prestaties van de Werkruimte van de Analyse, als de gebruikers tot verschillende rapportreeksen toegang hebben. Als de gezamenlijke gebruikers tot de zelfde rapportreeks toegang hebben, zullen de prestaties worden beïnvloed.

## Gemeenschappelijke foutenmeldingen in de Werkruimte van de Analyse

U kunt fouten ontmoeten wanneer het in wisselwerking staan met de Werkruimte van de Analyse. De fouten kunnen om verscheidene redenen voorkomen en hieronder vermeld zijn de gemeenschappelijkste.

| Foutmelding | Waarom gebeurt dit? |
|---|---|
| `The report suite is experiencing unusually heavy reporting. Please try again later.` | Uw organisatie probeert om teveel gezamenlijke verzoeken tegen een specifieke rapportreeks in werking te stellen. De contribuanten aan deze fout zijn API verzoeken, geplande projecten, geplande rapporten, gepland alarm, en gezamenlijke gebruikers die rapporteringsverzoeken indienen. Wij adviseren dat uw verzoeken en programma&#39;s voor de rapportreeks gelijkmatiger door de dag worden verspreid. |
| `A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.` | Adobe ervaart een kwestie die moet worden opgelost. We raden u aan de foutcode in te dienen via een aanvraag van Customer Care. |
| `The request is too complex.` | Uw rapportageaanvraag is te groot en kan niet worden uitgevoerd. De contribuanten aan deze fout zijn onderbrekingen toe te schrijven aan de grootte van het verzoek, teveel overeenkomende punten in een segment of een zoekfilter, teveel inbegrepen metriek, onverenigbare dimensie en metrische combinaties, enz. We raden je aan je aanvraag te vereenvoudigen. |
| `One of the segments or the search in this visualization contains a text search that returned too many results.` | We raden je aan je zoektekstcriteria te beperken en het verzoek opnieuw in te dienen. |
| `This dimension does not currently support non-default attribution models.` | Wij adviseren het vervangen van de afmeting in uw lijst met die compatibel is met [Attributie-IQ](../attribution/overview.md). |
| `Your request failed as a result of too many columns or pre-configured rows.` | Wij adviseren verwijderend sommige kolommen of rijen, of denk na verdelend hen in afzonderlijke visualisaties. |
