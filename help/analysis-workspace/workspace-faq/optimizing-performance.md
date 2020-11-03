---
description: Factoren die de prestaties en optimalisaties van de werkruimte beïnvloeden die u kunt maken
title: Analysis Workspace-prestatiefactoren en -optimalisatie
uuid: de51d03d-d555-4f0e-b19c-4a8f140770fc
translation-type: tm+mt
source-git-commit: a991dce6abaf90cbca06de75606a2517cb5b6484
workflow-type: tm+mt
source-wordcount: '1826'
ht-degree: 0%

---


# Optimaliseren [!UICONTROL Analysis Workspace performance]

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset wijkt enigszins af van [Analysis Workspace in het traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Verschillende factoren kunnen de prestaties van een project in Analysis Workspace beïnvloeden. Het is belangrijk om te weten wat die contribuanten zijn alvorens u begint een project te bouwen zodat u het project op de meest optimale manier kunt plannen en bouwen. Deze pagina bevat een lijst met factoren die van invloed zijn op de prestaties en optimalisaties die u kunt maken voor optimale prestaties in Analysis Workspace.

>[!IMPORTANT]
>
>De pagina Prestaties in Analysis Workspace is in beperkte versie. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

## [!UICONTROL Help] > [!UICONTROL Performance] in Analysis Workspace

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
| Rekensnelheid | Hoe snel uw computer een verwerkingstest uitvoert. De richtlijn is &lt; 750 ms. | Deze factor is van invloed op uw hardware en gelijktijdige programma&#39;s. | Open Taakbeheer van uw computer (PC) of Activiteitenmonitor (Mac) om te bepalen of programma&#39;s kunnen worden gesloten. Sluit vervolgens ongebruikte browsertabbladen of andere programma&#39;s. <br><br>Als die acties niet helpen, bespreek hardwaredetails met uw team van IT. |
| Gebruikt geheugen | Alleen beschikbaar voor Google Chrome. Op elk tabblad Werkruimte in een Google Chrome-browser wordt in totaal 4 GB geheugen gedeeld. Dit vertegenwoordigt het percentage van dat geheugentoelage dat door het huidige project wordt verbruikt. De richtlijn is 3500 MB, dat is het punt waarop de Werkruimte zal beginnen die geheugenfouten te overwinnen. | Als u op meerdere tabbladen werkt of 50000 rijen gegevens downloadt, wordt er meer geheugen gebruikt. | Als er een geheugenfout optreedt, sluit u de andere tabbladen van de werkruimte en/of voert u 50000 rijen uit. |
| Lokale opslag gebruikt | Gegevens die lokaal op de computer zijn opgeslagen voor gebruik in de browser. Elke oorsprong (bijvoorbeeld experience.adobe.com) heeft een recht van 10 MB. | Analysis Workspace gebruikt lokale opslag voor verschillende functies, waaronder voor het opslaan van automatisch opgeslagen (bestaande) projecten, gebruikersinstellingen en functiemarkeringen. | Om ervoor te zorgen dat de Analysis Workspace-functies niet worden verstoord, moet u de lokale opslag voor het domein Experience.adobe.com wissen. |
| Rendersnelheid | FPS staat voor frames per seconde. Dit is het aantal keren per seconde dat de browser de pagina op het scherm tekent. 24 FPS is algemeen wat het menselijke oog kan waarnemen; als FPS lager is dan dat, zult u teruggevende kwesties in Werkruimte waarnemen. | FPS wordt beïnvloed door multitasking over vele projecten van de Werkruimte in één keer en grootte van het project dat wordt bekeken. Andere programma&#39;s die op uw computer worden uitgevoerd, kunnen van invloed zijn, zoals streaming, achtergrondscanners, enzovoort. Bovendien heeft uw hardware invloed op deze factor. | Open Taakbeheer van uw computer (PC) of Activiteitenmonitor (Mac) om te bepalen of programma&#39;s kunnen worden gesloten. Sluit vervolgens ongebruikte browsertabbladen of andere programma&#39;s. <br><br>Als die acties niet helpen, bespreek hardwaredetails met uw team van IT. |

## Projectfactoren

[!UICONTROL Help] > [!UICONTROL Performance] de projectfactoren omvatten :

| Factor | Definitie | Optimalisatie |
| --- | --- | --- |
| Aantal vragen | Het totale aantal vragen (verzoeken) die aan Adobe worden gemaakt om gegevens terug te winnen die in het project worden getoond. De vragen omvatten gerangschikte verzoeken om lijsten, anomalieopsporing, sparklines, componenten die in de linkerspoorstaaf worden getoond, en meer. Hiermee sluit u samengevouwen deelvensters en visualisaties uit. Het richtsnoer is 100. | Vereenvoudig waar mogelijk uw project door gegevens op te splitsen in verschillende projecten die een specifiek doel of een groep belanghebbenden dienen. Gebruik labels om projecten in thema&#39;s te ordenen en ze te gebruiken [directe koppeling](/help/analysis-workspace/curate-share/shareable-links.md) een interne inhoudsopgave te maken, zodat belanghebbenden gemakkelijker kunnen vinden wat zij nodig hebben. |
| Uitgebreide deelvensters (van totaal aantal deelvensters) | Het aantal uitgevouwen deelvensters in verhouding tot het totale aantal deelvensters in het project. Het richtsnoer is 5. | Nadat u stappen hebt ondernomen om uw project te vereenvoudigen, vouwt u deelvensters in uw project samen die u tijdens het laden niet hoeft te bekijken. Als het project wordt geopend, worden alleen uitgebreide deelvensters verwerkt. Samengevouwen deelvensters worden pas verwerkt wanneer de gebruiker deze uitbreidt. |
| Uitgebreide visualisaties (van totale visualisaties) | Het aantal uitgevouwen tabellen en visualisaties van het totaal in het project, inclusief verborgen gegevensbronnen. Het richtsnoer is 15. | Nadat u stappen hebt ondernomen om uw project te vereenvoudigen, vouwt u visualisaties in uw project samen die niet tijdens het laden hoeven te worden bekeken. Prioriteit geven aan de visuals die het belangrijkst zijn voor de consument van het rapport en ondersteunende beelden zo nodig opsplitsen in een apart, gedetailleerder panel of project. |
| Aantal cellen voor vrije vorm | Het totale aantal cellen van de Freeform- lijst in het project, dat door rijen * kolommen over alle lijsten wordt berekend. Verborgen gegevensbronnen uitsluiten. Het richtsnoer is 4000. | Verlaag het aantal kolommen in de tabel tot alleen de meest relevante gegevenspunten. Verminder het aantal rijen in uw lijst door het aantal getoonde rijen aan te passen, een lijstfilter toe te passen, of een segment toe te passen. |
| Beschikbare componenten | Het totale aantal componenten dat in de linkerspoorstaaf van het project wordt opgehaald, over alle rapportagesets in het project. Het richtsnoer is 2000. | Bespreek met uw productbeheerder of er een virtuele rapportsuite met een meer op maat gemaakte set componenten moet worden gemaakt. |
| Gebruikte componenten | Het totale aantal componenten dat in het project wordt gebruikt. Het richtsnoer is 100. | Het aantal gebruikte componenten is geen directe invloed op de prestaties. De complexiteit van deze componenten zal echter bijdragen tot de prestaties van het project. Zie de optimalisaties in de sectie &quot;Aanvullende factoren&quot; hieronder. |
| Langste datumbereik | Deze factor toont de langste datumwaaier gebruikte het project. Het richtsnoer is één jaar. | Trek waar mogelijk niet meer gegevens in dan u nodig hebt. Verfijn de paneelkalender aan de relevante data voor uw analyse of gebruik datumwaaiercomponenten (paarse componenten) in uw vrije vormlijsten. Datumbereiken die in een tabel worden gebruikt, overschrijven het datumbereik van het deelvenster. U kunt bijvoorbeeld vorige maand, vorige week en gisteren toevoegen aan de tabelkolommen om die specifieke gegevensbereiken aan te vragen. Kijk voor meer informatie over het werken met datumbereiken in Analysis Workspace [deze video](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/date-ranges-and-calendar-in-analysis-workspace.html). <br><br>Bovendien moet het aantal jaar-over-jaar vergelijkingen die in het project worden gebruikt tot een minimum worden beperkt. Wanneer een jaar-over-jaar vergelijking wordt berekend, kijkt het over de volledige 13 maanden van gegevens tussen de maanden van rente. Dit heeft hetzelfde effect als het wijzigen van het datumbereik van het deelvenster in een datumbereik van 13 maanden. |

## Aanvullende factoren

Aanvullende factoren die niet zijn opgenomen in Help > Prestaties zijn onder andere:

| Factor | Definitie | Beïnvloed door | Optimalisatie |
| --- | --- | --- | --- |
| Complexiteit segment | De ingewikkelde segmenten kunnen een significante invloed op projectprestaties hebben. | De factoren die ingewikkeldheid aan een segment (in dalende orde van effect) toevoegen omvatten: <ul><li>Operatoren van &quot;contains,&quot;, &quot;contains any of&quot;, &quot;match,&quot; &quot;start with&quot; of &quot;ends with&quot; </li><li>Opeenvolgende segmentatie, vooral wanneer dimensiebeperkingen (Within/After) worden gebruikt </li><li>Het aantal unieke dimensie-items binnen de dimensies die in het segment worden gebruikt (pagina = &#39;A&#39; als pagina 10 unieke items bevat, is sneller dan Pagina = &#39;A&#39; als pagina 100000 unieke items bevat) </li><li>Aantal verschillende gebruikte afmetingen (bijvoorbeeld Pagina = &#39;Home&#39; en Pagina = &#39;Zoekresultaten&#39; zijn sneller dan eVar 1 = &#39;red&#39; en eVar 2 = &#39;blue&#39;)</li><li>Veel OR-operatoren (in plaats van AND)</li><li>Geneste containers met een verschillend bereik (bv. &quot;Actief&quot; in &quot;Bezoek&quot; in &quot;Bezoeker&quot;)</li></ul> | Hoewel sommige van de complexiteitsfactoren niet kunnen worden verhinderd, zoek mogelijkheden om de ingewikkeldheid van uw segmenten te verminderen. Over het algemeen geldt dat hoe specifieker u kunt zijn bij de criteria van uw segment, des te beter. Bijvoorbeeld:<ul><li>Bij containers is het gebruik van één container boven aan het segment sneller dan een reeks geneste containers.</li><li>Met operatoren is &#39;equals&#39; sneller dan &#39;contains&#39; en is &#39;equals any of&#39; sneller dan &#39;contains any of&#39;.</li><li>Met vele criteria, EN zullen de exploitanten sneller zijn dan een reeks van OF exploitanten.</li></ul> Zoek naar kansen om vele OF verklaringen in één enkele &quot;evenaart om het even welk van&quot;verklaring te verminderen.<br><br>[Classificaties](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html) U kunt ook helpen om vele waarden in beknopte groepen te consolideren waaruit u dan segmenten kunt creëren. De segmentatie op classificatiegroepen verstrekt prestatiesvoordelen over segmenten die vele OF verklaringen bevatten of &quot;bevat&quot;criteria. |
| Complexiteit van visualisatie (segmenten, meetgegevens, filters) | Het type visualisatie (bijvoorbeeld fallout versus een vrije-vormlijst) dat op zich aan een project wordt toegevoegd beïnvloedt niet zeer veel projectprestaties. Het is de complexiteit van de visualisatie die de verwerkingstijd vergroot. | Factoren die complexiteit toevoegen aan een visualisatie zijn:<ul><li>Bereik van gevraagde gegevens</li><li>Aantal toegepaste segmenten; bijvoorbeeld segmenten die worden gebruikt als rijen van een vrije-vormtabel</li><li>Gebruik van complexe segmenten</li><li>[Statisch item](/help/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md) rijen of kolommen in vrije-vormtabellen</li><li>Filters die worden toegepast op rijen in vrije-vormtabellen</li><li>Aantal inbegrepen metriek, vooral berekende metriek die segmenten gebruiken</li></ul> | Als u merkt dat uw projecten niet zo snel laden zoals u zou willen, probeer vervangend sommige segmenten met steunen en filters, waar mogelijk.<br><br>Als u zich voortdurend gebruikend segmenten en berekende metriek voor gegevenspunten vindt die voor uw zaken belangrijk zijn, denk na verbeterend uw implementatie om deze gegevenspunten directer te vangen. Als u tagbeheer gebruikt zoals Adobe Experience Platform Launch en verwerkingsregels voor Adobe, kunt u snel en gemakkelijk implementatiewijzigingen doorvoeren. |
| Grootte van rapportsuite | De hoeveelheid gegevens die in uw rapportsuite wordt verzameld. | - | Raadpleeg uw implementatieteam of een Adobe-expert om te bepalen of er implementatieverbeteringen zijn die kunnen worden aangebracht om de algehele ervaring in Adobe Analytics te verbeteren. |
