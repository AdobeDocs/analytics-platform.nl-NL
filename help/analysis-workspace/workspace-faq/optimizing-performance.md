---
description: 'null'
title: Analysis Workspace-prestaties optimaliseren
uuid: de51d03d-d555-4f0e-b19c-4a8f140770fc
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 0%

---


# Analysis Workspace-prestaties optimaliseren

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Bepaalde factoren kunnen van invloed zijn op de prestaties van een project in Analysis Workspace. Het is belangrijk om te weten wat die contribuanten zijn alvorens u begint een project te bouwen zodat u het project op de meest optimale manier kunt plannen en bouwen. Hieronder vindt u een lijst met factoren die van invloed zijn op de prestaties en aanbevolen procedures voor het optimaliseren van uw projecten. Analysis Workspace-prestaties zijn een van de belangrijkste prioriteiten van Adobe en we blijven elke dag verbeteren.

## Complexiteit van segmentlogica

De ingewikkelde segmenten kunnen een significante invloed op projectprestaties hebben. De factoren die ingewikkeldheid aan een segment (in dalende orde van effect) toevoegen omvatten:

* Operatoren van &quot;contains,&quot;, &quot;contains any of&quot;, &quot;match,&quot; &quot;start with&quot; of &quot;ends with&quot;
* Opeenvolgende segmentatie, vooral wanneer dimensiebeperkingen (Within/After) worden gebruikt
* Het aantal unieke dimensie-items binnen de dimensies die in het segment worden gebruikt (pagina = &#39;A&#39; als pagina 10 unieke items bevat, is sneller dan Pagina = &#39;A&#39; als pagina 100000 unieke items bevat)
* Aantal verschillende gebruikte afmetingen (bijvoorbeeld Pagina = &#39;Home&#39; en Pagina = &#39;Zoekresultaten&#39; zijn sneller dan eVar 1 = &#39;red&#39; en eVar 2 = &#39;blue&#39;)
* Veel OR-operatoren (in plaats van AND)
* Geneste containers met een verschillend bereik (bv. &quot;Actief&quot; in &quot;Bezoek&quot; in &quot;Bezoeker&quot;)

**Aanbevolen procedures voor logische complexiteit**

Hoewel sommige van de complexiteitsfactoren niet kunnen worden verhinderd, denk over mogelijkheden om de ingewikkeldheid van uw segmenten te verminderen. Over het algemeen geldt dat hoe specifieker u kunt zijn bij de criteria van uw segment, des te beter. Bijvoorbeeld:

* Bij containers is het gebruik van één container boven aan het segment sneller dan een reeks geneste containers.
* Met operatoren is &#39;equals&#39; sneller dan &#39;contains&#39; en is &#39;equals any of&#39; sneller dan &#39;contains any of&#39;.
* Met vele criteria, EN zullen de exploitanten sneller zijn dan een reeks van OF exploitanten. Ook, zoek kansen om vele OF verklaringen in één enkele &quot;evenaart om het even welk van&quot;verklaring te verminderen.

Bovendien kunnen [classificaties](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html) helpen vele waarden in beknopte groepen consolideren waarvan u dan segmenten kunt creëren. De segmentatie op classificatiegroepen verstrekt prestatiesvoordelen over segmenten die vele OF verklaringen bevatten of &quot;bevat&quot;criteria.

## Bereik van gevraagde gegevens

Het gegevensbereik dat in een project wordt aangevraagd, is van invloed op de Analysis Workspace-prestaties.

**Aanbevolen werkwijzen voor gegevensbereik**

Trek waar mogelijk niet meer gegevens in dan u nodig hebt.

Datumbereiken (paarse componenten) overschrijven het datumbereik van het deelvenster. Als u dus verschillende datumbereiken als kolommen gebruikt (bijvoorbeeld kolommen van vorige maand, vorige week en gisteren), hoeft het datumbereik van het deelvenster niet alle kolomdatumbereiken te beslaan. U kunt deze instelling gewoon instellen op gisteren, omdat de gegevensbereiken die in de tabel in vrije vorm worden gebruikt, het deelvenster overschrijven. Bekijk [deze video](https://www.youtube.com/watch?v=ybmv6EBmhn0) voor meer informatie over het werken met datumbereiken in Analysis Workspace.

Gebruik [datumvergelijkingsopties](/help/components/date-ranges/time-comparison.md) om de specifieke tijdsperioden van gegevens die u wilt vergelijken in te vullen. Als u bijvoorbeeld de gegevens van vorige maand wilt weergeven in vergelijking met die van dezelfde maand vorig jaar, in plaats van het paneel in te stellen op de laatste 13 maanden met gegevens, gebruikt u gewoon de optie voor de tijdsperioden van de vergelijking om de prestaties van jaar tot jaar weer te geven.

## Aantal visualisaties

Het aantal grafiekvisualisaties in één project zal algemene ontvankelijkheid van Analysis Workspace beïnvloeden.

**Aanbevolen werkwijze voor het aantal visualisaties**

Verlaag het aantal visualisaties in uw project. Analysis Workspace verwerkt veel achter de schermen voor elke visuele weergave die u toevoegt. Prioreert dus de visuele aspecten die het belangrijkst zijn voor de consument van het rapport en breekt zo nodig ondersteunende beelden uit in een afzonderlijk, gedetailleerder project.

## Complexiteit van visualisaties (segmenten, meetgegevens, filters)

Het type visualisatie (bijvoorbeeld fallout versus een vrije-vormlijst) dat op zich aan een project wordt toegevoegd beïnvloedt niet zeer veel projectprestaties. Het is de complexiteit van de visualisatie die de verwerkingstijd vergroot. Factoren die complexiteit toevoegen aan een visualisatie zijn:

* Bereik van gevraagde gegevens, zoals hierboven vermeld
* Aantal toegepaste segmenten; bijvoorbeeld segmenten die worden gebruikt als rijen van een vrije-vormtabel
* Gebruik van complexe segmenten
* Statische itemrijen of kolommen in vrije-vormtabellen
* Filters die worden toegepast op rijen in vrije-vormtabellen
* Aantal inbegrepen metriek, vooral berekende metriek die segmenten gebruiken

**Beste praktijken voor visualiseringsingewikkeldheid**

Als u merkt dat uw projecten niet zo snel laden zoals u zou willen, probeer vervangend sommige segmenten met steunen en filters, waar mogelijk.

Als u zich constant gebruikend segmenten en berekende metriek voor gegevenspunten vindt die voor uw zaken belangrijk zijn, denk na verbeterend uw implementatie om deze gegevenspunten directer te vangen. Door het gebruik van een tagbeheer zoals Starten van Adobe Experience Platforms en de verwerkingsregels van Adobe kunnen implementatiewijzigingen snel en eenvoudig worden geïmplementeerd. Zie &#39;Complexiteit van Segment Logic&#39; hierboven voor meer informatie over het vereenvoudigen van complexe segmenten.

## Aantal deelvensters

Eén deelvenster kan veel visualisaties bevatten. Het aantal deelvensters kan daarom ook van invloed zijn op de algehele reactiesnelheid van Analysis Workspace.

**Aanbevolen werkwijze voor het aantal deelvensters**

Probeer niet alles aan één project toe te voegen, maar creeer afzonderlijke projecten die een specifiek doel of een groep belanghebbenden dienen. Gebruik labels om projecten in hoofdthema&#39;s te ordenen en verwante projecten met groepen belanghebbenden te delen.

Als u meer projecten wilt organiseren, moet u niet vergeten dat [directe koppeling](https://www.youtube.com/watch?v=6IOEewflG2U) naar uw project een optie is. Een interne index van projecten maken, zodat belanghebbenden gemakkelijker kunnen vinden wat ze nodig hebben.

Als er in één werkruimte veel deelvensters nodig zijn, vouwt u deelvensters samen voordat u ze opslaat en deelt. Wanneer een project wordt geladen, laadt Analysis Workspace alleen inhoud voor de uitgebreide deelvensters. Samengevouwen deelvensters worden pas geladen wanneer de gebruiker deze uitbreidt. Deze aanpak helpt op twee manieren:

* Samengevouwen deelvensters besparen op de algemene laadtijd van een project
* Samengevouwen deelvensters zijn een goede manier om uw projecten op een logische manier te organiseren voor de consument van het rapport

## Grootte van rapportsuite

De grootte van de rapportsuite lijkt wellicht een drijvende kracht, maar speelt in werkelijkheid slechts een kleine rol in de prestaties van het project, omdat de gegevensverwerking door Adobe wordt verwerkt

## Aantal gebruikers dat tegelijkertijd Analysis Workspace opent

Het aantal gebruikers dat tegelijkertijd toegang krijgt tot Analysis Workspace of specifieke projecten heeft geen wezenlijk effect op de Analysis Workspace-prestaties als gebruikers toegang willen tot verschillende rapportsuite. Als gelijktijdige gebruikers toegang krijgen tot dezelfde rapportsuite, heeft dit gevolgen voor de prestaties.

## Algemene foutberichten in Analysis Workspace

Er kunnen fouten optreden bij de interactie met Analysis Workspace. Fouten kunnen om verschillende redenen optreden en worden hieronder vermeld.

| Foutbericht | Waarom gebeurt dit? |
|---|---|
| `The report suite is experiencing unusually heavy reporting. Please try again later.` | Uw organisatie probeert teveel gezamenlijke verzoeken tegen een specifieke rapportreeks in werking te stellen. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, geplande rapporten, geplande alarm, en gezamenlijke gebruikers die het melden verzoeken. Wij adviseren dat uw verzoeken en programma&#39;s voor de rapportreeks gelijkmatiger door de dag worden verspreid. |
| `A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.` | Adobe ondervindt een probleem dat moet worden opgelost. Wij adviseren dat u de foutencode door een verzoek van de Zorg van de Klant indient. |
| `The request is too complex.` | Uw rapportageaanvraag is te groot en kan niet worden uitgevoerd. Medewerkers aan deze fout zijn onderbrekingen wegens de grootte van het verzoek, teveel overeenkomende punten in een segment of een zoekfilter, teveel inbegrepen metriek, incompatibele afmeting en metrische combinaties, enz. We raden je aan je aanvraag te vereenvoudigen. |
| `One of the segments or the search in this visualization contains a text search that returned too many results.` | We raden u aan de zoektekstcriteria te verfijnen en het verzoek opnieuw in te dienen. |
| `This dimension does not currently support non-default attribution models.` | We raden u aan de dimensie in uw tabel te vervangen door een dimensie die compatibel is met [Attribution IQ](../attribution/overview.md). |
| `Your request failed as a result of too many columns or pre-configured rows.` | We raden u aan een aantal kolommen of rijen te verwijderen of te splitsen in afzonderlijke visualisaties. |
