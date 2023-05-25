---
description: Factoren die van invloed zijn op CJA en de prestaties en optimalisaties van de Werkruimte die u kunt maken
title: CJA- en Analysis Workspace-prestaties optimaliseren
feature: FAQ
exl-id: ad00e476-6f19-462b-ba53-d72ddd949802
source-git-commit: d99796920f361eb325f55c1b1035a163cb23c790
workflow-type: tm+mt
source-wordcount: '1858'
ht-degree: 0%

---

# CJA optimaliseren en [!UICONTROL Analysis Workspace] prestaties

Verschillende factoren kunnen de algemene CJA-prestaties en de prestaties van een project in Analysis Workspace beïnvloeden. In Workspace krijgt u mogelijk een foutbericht met de tekst &quot;Dit rapport is te complex.&quot; [Is dit de exacte formulering van de boodschap?] Dit onderwerp bespreekt welke factoren tot deze fout kunnen leiden en hoe te om het rapport/project te vereenvoudigen.

## Algemene CJA-prestaties

Deze factoren beïnvloeden de algehele CJA prestatie:

| Factor | Definitie | Beïnvloed door | Optimalisatie |
| --- | --- | --- | --- |
| **Filtercomplexiteit** | Ingewikkelde filters kunnen een aanzienlijke invloed hebben op de projectprestaties. | Factoren die een filter complexer maken (in aflopende volgorde van impact) zijn: <ul><li>Operatoren van &quot;contains,&quot;, &quot;contains any of&quot;, &quot;match,&quot; &quot;start with&quot; of &quot;ends with&quot; </li><li>Opeenvolgend filteren, vooral wanneer dimensiebeperkingen (Within/After) worden gebruikt </li><li>Het aantal unieke dimensie-items binnen de afmetingen die in het filter worden gebruikt (pagina = &#39;A&#39; als pagina 10 unieke items bevat, is sneller dan Pagina = &#39;A&#39; als pagina 100000 unieke items bevat) </li><li>Aantal verschillende gebruikte afmetingen (bijvoorbeeld Pagina = &#39;Home&#39; en Pagina = &#39;Zoekresultaten&#39; zijn sneller dan eVar 1 = &#39;red&#39; en eVar 2 = &#39;blue&#39;)</li><li>Veel OR-operatoren (in plaats van AND)</li><li>Geneste containers die binnen het bereik variëren (bijv. &quot;Gebeurtenis&quot; in &quot;Sessie&quot; in &quot;Persoon&quot;)</li></ul> | Sommige complexiteitsfactoren kunnen niet worden voorkomen, maar zoeken naar mogelijkheden om de complexiteit van uw filters te verminderen. Over het algemeen geldt dat hoe specifieker u kunt zijn met uw filtercriteria, des te beter. Bijvoorbeeld:<ul><li>Bij containers is het gebruik van één container boven aan het filter sneller dan een reeks geneste containers.</li><li>Met operatoren is &#39;equals&#39; sneller dan &#39;contains&#39; en is &#39;equals any of&#39; sneller dan &#39;contains any of&#39;.</li><li>Met vele criteria, EN operatoren is sneller dan een reeks OF exploitanten.</li></ul> Zoek naar kansen om vele OF verklaringen in één enkele &quot;evenaart om het even welk van&quot;verklaring te verminderen.<br> |
| **Visualisatie-complexiteit** (filters, meetgegevens, filters) | Het type visualisatie (bv. fallout versus een vrije-vormlijst) dat op zich aan een project wordt toegevoegd, heeft niet veel invloed op de projectprestaties. Het is de complexiteit van de visualisatie die de verwerkingstijd verhoogt. | Factoren die complexiteit toevoegen aan een visualisatie zijn:<ul><li>Bereik van gevraagde gegevens</li><li>Aantal toegepaste filters; filters die bijvoorbeeld worden gebruikt als rijen van een vrije-vormtabel</li><li>Gebruik van complexe filters</li><li>[Statisch item](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) rijen of kolommen in vrije-vormtabellen</li><li>Filters die worden toegepast op rijen in vrije-vormtabellen</li><li>Aantal inbegrepen metriek, vooral berekende metriek die filters gebruiken</li></ul> |
| **Capaciteit datacenter** | De hoeveelheid rapporteringscapaciteit u en andere klanten binnen een Adobe gegevenscentrum delen. | Dit wordt beïnvloed door het aantal gezamenlijke vragen die door uw organisatie en andere organisaties binnen uw gegevenscentrum worden gemaakt. | Uw organisatie heeft recht op een ingestelde capaciteit en als het systeem onder een lichte belasting staat, zal Adobe meer capaciteit naar u verschuiven, boven en boven uw recht op vergoeding. |
| **Gelijktijdige query&#39;s** | Het aantal vragen dat tegelijkertijd door uw organisatie wordt gevraagd. Elke organisatie heeft recht op een minimum van 5 gelijktijdige vragen? Als een rapport lange tijd neemt, typisch is het toe te schrijven aan het feit dat het in een rij met andere rapporten is. Dit betekent dat uw organisatie een groot aantal gelijktijdige aanvragen probeert uit te voeren in een specifieke gegevensweergave. De vragen kunnen van API verzoeken, rapporteringsUIs (Analysis Workspace, Report Builder, enz.), geplande projecten, gepland alarm, en gezamenlijke gebruikers komen die rapporteringsverzoeken indienen. Verspreid uw verzoeken en programma&#39;s voor de gegevensmening gelijkmatiger door de dag. Verplaats uw verzoeken waar mogelijk naar tijden buiten de piek. Maandochtenden, dinsdagochtend en de eerste van elke maand zijn de hoogste rapportagetijden. |
| **Grootte gegevensweergave??** | De hoeveelheid gegevens die in de gegevensweergave is verzameld. |  | Raadpleeg uw implementatieteam of CJA-expert om te bepalen of er implementatieverbeteringen zijn die kunnen worden aangebracht om de algemene ervaring in CJA te verbeteren. |

## [!UICONTROL Help] > [!UICONTROL Performance] in Analysis Workspace

Verschillende factoren kunnen de prestaties van een project in Analysis Workspace beïnvloeden. Het is belangrijk om te weten wat die contribuanten zijn alvorens u begint een project te bouwen zodat u het project op de meest optimale manier kunt plannen en bouwen. Deze sectie bevat een lijst met factoren die van invloed zijn op de prestaties en optimalisaties die u kunt maken om ervoor te zorgen dat de prestaties in Analysis Workspace optimaal zijn.

Onder **Analysis Workspace > [!UICONTROL Help] >[!UICONTROL Performance]**, kunt u factoren zien die de prestaties van uw project, met inbegrip van netwerk, browser, en projectfactoren beïnvloeden. Voor de nauwkeurigste resultaten, sta het project toe om volledig te laden alvorens de pagina van Prestaties te openen.

* De Huidige kolom van het Project toont de resultaten voor uw huidige project en gebruikersmilieu.
* In de kolom met hulplijnen wordt de aanbevolen drempelwaarde voor elke factor weergegeven.

Bovendien kunt u **Downloaden als CSV** de prestatiegegevens om eenvoudig te delen met de Adobe-klantenservice of uw interne IT-teams.

>[!NOTE]
>
>De informatie op de pagina Prestaties varieert telkens wanneer het modaal wordt geopend, aangezien de factoren aan verandering onderworpen zijn. Bovendien zal Adobe de verstrekte richtsnoeren blijven verfijnen wanneer meer gegevens beschikbaar komen.

![](assets/performance-modal.png)

## Netwerkfactoren

[!UICONTROL Help] > [!UICONTROL Performance] netwerkfactoren omvatten :

| Factor | Definitie | Beïnvloed door | Optimalisatie |
| --- | --- | --- | --- |
| Verbinding met Adobe | Adobe verzendt in 10 testvraag wanneer de prestatiespagina wordt geopend. Dit vertegenwoordigt het percentage van die vraag aan Adobe die slaagt. | De lokale netwerkkwesties of de kwesties van de Adobe zullen deze factor beïnvloeden. | Controleer status.adobe.com of er bekende problemen zijn met de service. Vervolgens valideert u uw lokale netwerkverbinding. |
| Internetbandbreedte | Alleen beschikbaar voor Google Chrome. De schatting door uw browser van de bandbreedte op uw locatie. De richtlijn is 2.0 MB/s. | Deze factor wordt beïnvloed door uw lokale netwerkverbinding. | Valideer uw lokale netwerkverbinding. |
| Internetvertraging | Adobe verzendt in 10 testvraag wanneer de prestatiespagina wordt geopend. Dit vertegenwoordigt de hoeveelheid tijd het gemiddelde voor elke verzoek om naar Adobe te gaan en is teruggekeerd. Eenvoudiger gezegd, het is een maat voor hoe snel het internet is tussen uw locatie en Adobe. De richtlijn is &lt; 1 seconde. | De lokale netwerkkwesties, vele open browser lusjes, of de kwesties van de Adobe zullen deze factor beïnvloeden. | Controleer status.adobe.com of er bekende problemen zijn met de service. Vervolgens valideert u uw lokale netwerkverbinding en sluit u ongebruikte browsertabbladen. |

## Browserfactoren

[!UICONTROL Help] > [!UICONTROL Performance] browserfactoren zijn onder andere:

| Factor | Definitie | Beïnvloed door | Optimalisatie |
| --- | --- | --- | --- |
| Rekensnelheid | Hoe snel uw computer een verwerkingstest uitvoert. De richtlijn is &lt; 750 ms. | Deze factor is van invloed op uw hardware en gelijktijdige programma&#39;s. | Open Taakbeheer (PC) of Activiteitencontrole (Mac) van uw computer om te bepalen of programma&#39;s kunnen worden gesloten. Sluit vervolgens ongebruikte browsertabbladen of andere programma&#39;s. <br><br>Als die acties niet helpen, bespreek hardwaredetails met uw team van IT. |
| Gebruikt geheugen | Alleen beschikbaar voor Google Chrome. Op elk tabblad Werkruimte in een Google Chrome-browser wordt in totaal 4 GB geheugen gedeeld. Dit vertegenwoordigt het percentage van dat geheugentoelage dat door het huidige project wordt verbruikt. De richtlijn is 3500 MB, dat is het punt waarop de Werkruimte zal beginnen die geheugenfouten te overwinnen. | Als u op meerdere tabbladen werkt of 50000 rijen gegevens downloadt, wordt er meer geheugen gebruikt. | Als er een geheugenfout optreedt, sluit u de andere tabbladen van de werkruimte en/of voert u 50000 rijen uit. |
| Lokale opslag gebruikt | Gegevens die lokaal op de computer zijn opgeslagen voor gebruik in de browser. Elke oorsprong (bijvoorbeeld experience.adobe.com) heeft een recht van 10 MB. | Analysis Workspace gebruikt lokale opslag voor verschillende functies, waaronder voor het opslaan van automatisch opgeslagen (bestaande) projecten, gebruikersinstellingen en functiemarkeringen. | Om ervoor te zorgen dat de Analysis Workspace-functies niet worden verstoord, moet u de lokale opslag voor het domein Experience.adobe.com wissen. |
| Rendersnelheid | FPS staat voor frames per seconde. Dit is het aantal keren per seconde dat de browser de pagina op het scherm tekent. 24 FPS is algemeen wat het menselijke oog kan waarnemen; als FPS lager is dan dat, zult u teruggevende kwesties in Werkruimte waarnemen. | FPS wordt beïnvloed door multitasking over vele projecten van de Werkruimte in één keer en grootte van het project dat wordt bekeken. Andere programma&#39;s die op uw computer worden uitgevoerd, kunnen gevolgen hebben, zoals streaming, achtergrondscanners, enzovoort. Bovendien heeft uw hardware invloed op deze factor. | Open Taakbeheer (PC) of Activiteitencontrole (Mac) van uw computer om te bepalen of programma&#39;s kunnen worden gesloten. Sluit vervolgens ongebruikte browsertabbladen of andere programma&#39;s. <br><br>Als die acties niet helpen, bespreek hardwaredetails met uw team van IT. |

## Projectfactoren

[!UICONTROL Help] > [!UICONTROL Performance] de projectfactoren omvatten :

| Factor | Definitie | Optimalisatie |
| --- | --- | --- |
| Aantal vragen | Het totale aantal vragen (verzoeken) die aan Adobe worden gemaakt om gegevens terug te winnen die in het project worden getoond. De vragen omvatten gerangschikte verzoeken om lijsten, anomalieopsporing, sparklines, componenten die in de linkerspoorstaaf worden getoond, en meer. Hiermee sluit u samengevouwen deelvensters en visualisaties uit. Het richtsnoer is 100. | Vereenvoudig waar mogelijk uw project door gegevens op te splitsen in verschillende projecten die een specifiek doel of een groep belanghebbenden dienen. Gebruik labels om projecten in thema&#39;s te ordenen en ze te gebruiken [directe koppeling](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html) een interne inhoudsopgave te maken, zodat belanghebbenden gemakkelijker kunnen vinden wat zij nodig hebben. |
| Uitgebreide deelvensters (van totaal aantal deelvensters) | Het aantal uitgevouwen deelvensters in verhouding tot het totale aantal deelvensters in het project. Het richtsnoer is 5. | Nadat u stappen hebt ondernomen om uw project te vereenvoudigen, vouwt u deelvensters in uw project samen die u tijdens het laden niet hoeft te bekijken. Als het project wordt geopend, worden alleen uitgebreide deelvensters verwerkt. Samengevouwen deelvensters worden pas verwerkt wanneer de gebruiker deze uitbreidt. |
| Uitgebreide visualisaties (van totale visualisaties) | Het aantal uitgevouwen tabellen en visualisaties van het totaal in het project, inclusief verborgen gegevensbronnen. Het richtsnoer is 15. | Nadat u stappen hebt ondernomen om uw project te vereenvoudigen, vouwt u visualisaties in uw project samen die niet tijdens het laden hoeven te worden bekeken. Prioriteit geven aan de visuals die het belangrijkst zijn voor de consument van het rapport en ondersteunende beelden zo nodig opsplitsen in een apart, gedetailleerder panel of project. |
| Aantal cellen voor vrije vorm | Het totale aantal cellen van de Freeform- lijst in het project, dat door rijen * kolommen over alle lijsten wordt berekend. Verborgen gegevensbronnen uitsluiten. Het richtsnoer is 4000. | Verlaag het aantal kolommen in de tabel tot alleen de meest relevante gegevenspunten. Verminder het aantal rijen in de tabel door het aantal rijen aan te passen dat wordt weergegeven, een tabelfilter toe te passen of een filter toe te passen. |
| Gebruikte componenten | Het totale aantal componenten dat in het project wordt gebruikt. Het richtsnoer is 100. | Het aantal gebruikte componenten is geen directe invloed op de prestaties. De complexiteit van deze componenten zal echter bijdragen tot de prestaties van het project. Zie de optimalisaties in de sectie &quot;Aanvullende factoren&quot; hieronder. |
| Langste datumbereik | Deze factor toont de langste datumwaaier gebruikte het project. Het richtsnoer is één jaar. | Trek waar mogelijk niet meer gegevens in dan u nodig hebt. Verfijn de paneelkalender aan de relevante data voor uw analyse of gebruik datumwaaiercomponenten (paarse componenten) in uw vrije vormlijsten. Datumbereiken die in een tabel worden gebruikt, overschrijven het datumbereik van het deelvenster. U kunt bijvoorbeeld vorige maand, vorige week en gisteren toevoegen aan de tabelkolommen om die specifieke gegevensbereiken aan te vragen. Kijk voor meer informatie over het werken met datumbereiken in Analysis Workspace [deze video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/date-ranges-and-calendar-in-analysis-workspace.html). <br><br>Bovendien moet het aantal jaar-over-jaar vergelijkingen die in het project worden gebruikt, tot een minimum worden beperkt. Wanneer een jaar-over-jaar vergelijking wordt berekend, kijkt het over de volledige 13 maanden van gegevens tussen de maanden van rente. Dit heeft hetzelfde effect als het wijzigen van het datumbereik van het deelvenster in een datumbereik van 13 maanden. |
