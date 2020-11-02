---
description: Factoren die de prestaties en optimalisaties van de werkruimte beïnvloeden die u kunt maken
title: Analysis Workspace-prestatiefactoren en -optimalisatie
uuid: de51d03d-d555-4f0e-b19c-4a8f140770fc
translation-type: tm+mt
source-git-commit: fb7738a47818e62e8f90b9dd9e4c1abe842214d8
workflow-type: tm+mt
source-wordcount: '1791'
ht-degree: 0%

---


# Optimaliseren [!UICONTROL Analysis Workspace performance]

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
| Internetvertraging | Adobe verzendt in 10 testvraag wanneer de prestatiespagina wordt geopend. Dit vertegenwoordigt de hoeveelheid tijd het gemiddelde voor elke verzoek om naar Adobe te gaan en is teruggekeerd. Eenvoudiger gezegd, het is een maat voor hoe snel het internet is tussen uw locatie en Adobe. De richtlijn is &lt; 1 seconde. | De lokale netwerkkwesties, vele open browser lusjes, of de kwesties van de Adobe zullen deze factor beïnvloeden. | Controleer status.adobe.com om te controleren of er bekende problemen zijn met de service. Vervolgens valideert u uw lokale netwerkverbinding en sluit u ongebruikte browsertabbladen. |

## Browserfactoren

[!UICONTROL Help] > [!UICONTROL Performance] browserfactoren omvatten:

| Factor | Definitie | Beïnvloed door | Optimalisatie |
| --- | --- | --- | --- |
| Rekensnelheid | Hoe snel uw computer een verwerkingstest uitvoert. De richtlijn is &lt; 750 ms. | Deze factor wordt beïnvloed door uw hardware en door gelijktijdige programma&#39;s. | Open de Taakmanager (PC) of de Monitor van de Activiteit (MAC) van uw computer om te bepalen als om het even welke programma&#39;s kunnen worden gesloten. Sluit vervolgens ongebruikte browsertabbladen of andere programma&#39;s. <br><br>Als die acties niet helpen, bespreek de hardwaredetails met uw IT-team. |
| Gebruikt geheugen | Alleen beschikbaar voor Google Chrome. Op elk tabblad Werkruimte in een Google Chrome-browser wordt in totaal 4 GB geheugen gedeeld. Dit is het percentage van de geheugenruimte die wordt gebruikt door het huidige project. De richtlijn is 3500 MB, dat is het punt waarop de Werkruimte zal beginnen het blootstellen van geheugenfouten. | Door op meerdere tabbladen te werken of 50000 rijen gegevens te downloaden, neemt het geheugengebruik toe. | Als er een geheugenfout optreedt, sluit u de andere tabbladen van de werkruimte en/of voert u 50000 rijen tegelijk uit. |
| Lokale opslag gebruikt | Gegevens die lokaal op uw computer zijn opgeslagen voor gebruik in de browser. Elke oorsprong (bijvoorbeeld experience.adobe.com) heeft een recht van 10 MB. | Analysis Workspace gebruikt lokale opslagruimte voor verschillende functies, zoals voor het opslaan van automatisch opgeslagen (bestaande) projecten, gebruikersinstellingen en functiemarkeringen. | Om ervoor te zorgen dat de Analysis Workspace-functies niet worden verstoord, moet u de lokale opslag voor het domein experience.adobe.com wissen. |
| Rendersnelheid | FPS staat voor frames per seconde. Dit is het aantal keren per seconde dat de browser de pagina op uw scherm tekent. 24 FPS is wat het menselijk oog doorgaans kan waarnemen; als FPS lager is dan dat, zult u teruggevende kwesties in Werkruimte waarnemen. | FPS wordt beïnvloed door multitasking in veel Workspace-projecten tegelijk en de grootte van het project dat wordt weergegeven. Andere programma&#39;s die op uw computer worden uitgevoerd, kunnen gevolgen hebben, zoals streaming, achtergrondscanners, enzovoort. Bovendien heeft uw hardware invloed op deze factor. | Open de Taakmanager (PC) of de Monitor van de Activiteit (MAC) van uw computer om te bepalen als om het even welke programma&#39;s kunnen worden gesloten. Sluit vervolgens ongebruikte browsertabbladen of andere programma&#39;s. <br><br>Als die acties niet helpen, bespreek de hardwaredetails met uw IT-team. |

## Projectfactoren

[!UICONTROL Help] > [!UICONTROL Performance] de projectfactoren omvatten :

| Factor | Definitie | Optimalisatie |
| --- | --- | --- |
| Aantal query&#39;s | Het totale aantal vragen (verzoeken) die aan Adobe worden gemaakt om gegevens terug te winnen die in het project worden getoond. De vragen omvatten gerangschikte verzoeken om lijsten, anomalieopsporing, vonklines, componenten die in het linkerspoor worden getoond, en meer. Hiermee sluit u samengevouwen deelvensters en visualisaties uit. Het richtsnoer is 100. | Vereenvoudig je project waar mogelijk door data op te splitsen in verschillende projecten die een specifiek doel of een groep belanghebbenden dienen. Tags gebruiken om projecten in thema&#39;s te ordenen en [directe koppeling](/help/analysis-workspace/curate-share/shareable-links.md) een interne inhoudsopgave op te stellen zodat belanghebbenden gemakkelijker kunnen vinden wat zij nodig hebben . |
| Uitgebreide deelvensters (buiten totaal) | Het aantal uitgevouwen deelvensters in het totale aantal deelvensters in het project. Het richtsnoer is 5. | Nadat u stappen hebt ondernomen om uw project te vereenvoudigen, vouwt u deelvensters in uw project samen die niet hoeven te worden weergegeven tijdens het laden. Als het project wordt geopend, worden alleen uitgevouwen deelvensters verwerkt. Samengevouwen deelvensters worden pas verwerkt nadat de gebruiker ze heeft uitgevouwen. |
| Uitgebreide visualisaties (van totale visualisaties) | Het aantal uitgebreide tabellen en visualisaties uit het totaal in het project, inclusief verborgen gegevensbronnen. Het richtsnoer is 15. | Nadat u stappen hebt ondernomen om uw project te vereenvoudigen, vouwt u visualisaties in uw project samen die niet tijdens het laden hoeven te worden weergegeven. Prioriteit geven aan de visuals die het belangrijkst zijn voor de consument van het rapport en zo nodig ondersteunende visuals opsplitsen in een apart, gedetailleerder panel of project. |
| Aantal cellen in vrije vorm | Het totale aantal cellen van de Freeform-tabel in het project, berekend door rijen * kolommen over alle tabellen. Verborgen gegevensbronnen uitsluiten. Het richtsnoer is 4000. | Verminder het aantal kolommen in uw tabel tot alleen de meest relevante gegevenspunten. Verminder het aantal rijen in de tabel door het aantal weergegeven rijen aan te passen, een tabelfilter toe te passen of een segment toe te passen. |
| Beschikbare componenten | Het totale aantal componenten dat in het linkerspoor van het project, over alle rapportsuites in het project wordt teruggewonnen. Het richtsnoer is 2000. | Praat met uw productbeheerder over het maken van een beheerde virtuele rapportsuite met een meer op maat gemaakte set componenten. |
| Gebruikte componenten | Het totale aantal componenten dat in het project wordt gebruikt. Het richtsnoer is 100. | Het aantal gebruikte componenten is geen directe invloed op de prestaties. De complexiteit van deze componenten zal echter bijdragen tot de prestaties van het project. Zie optimalisaties in de sectie &quot;Aanvullende factoren&quot; hieronder. |
| Langste datumbereik | Deze factor geeft het langste datumbereik weer dat in het project wordt gebruikt. Het richtsnoer is één jaar. | Trek waar mogelijk niet meer data in dan nodig is. Verfijn de deelvensterkalender met de relevante datums voor uw analyse of gebruik componenten van het datumbereik (paarse componenten) in uw vrije-vormtabellen. De datumbereiken die in een tabel worden gebruikt, overschrijven het datumbereik van het deelvenster. U kunt bijvoorbeeld vorige maand, vorige week en gisteren toevoegen aan de tabelkolommen om die specifieke gegevensbereiken aan te vragen. Voor meer informatie over het werken met datumbereiken in Analysis Workspace bekijkt u [deze video](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/date-ranges-and-calendar-in-analysis-workspace.html). <br><br>Bovendien moet u het aantal jaar-op-jaar-vergelijkingen minimaliseren dat in het project wordt gebruikt. Wanneer een jaar-over-jaar vergelijking wordt berekend, kijkt het over de volledige 13 maanden van gegevens tussen de maanden van belang. Dit heeft hetzelfde effect als het wijzigen van het datumbereik van het deelvenster in een datumbereik van 13 maanden. |

## Aanvullende factoren

Aanvullende factoren die niet zijn opgenomen in Help > Prestaties zijn:

| Factor | Definitie | Beïnvloed door | Optimalisatie |
| --- | --- | --- | --- |
| Segmentcomplexiteit | De ingewikkelde segmenten kunnen een significante invloed op projectprestaties hebben. | Factoren die een segment complexer maken (in aflopende volgorde van impact) zijn: <ul><li>Operatoren van &quot;contains,&quot;, &quot;contains any of&quot;, &quot;matches,&quot; &quot;starts with&quot; of &quot;ends with&quot; </li><li>Opeenvolgende segmentatie, vooral wanneer dimensiebeperkingen (Within/After) worden gebruikt </li><li>Het aantal unieke dimensie-items binnen de afmetingen die in het segment worden gebruikt (bijvoorbeeld Pagina = &#39;A&#39; als Pagina 10 unieke items heeft, is sneller dan Pagina = &#39;A&#39; als Pagina 100000 unieke items heeft) </li><li>Aantal gebruikte afmetingen (bijvoorbeeld Pagina = &#39;Home&#39; en Pagina = &#39;Zoekresultaten&#39; zijn sneller dan eVar 1 = &#39;red&#39; en eVar 2 = &#39;blue&#39;)</li><li>Veel OR-operatoren (in plaats van AND)</li><li>Geneste containers met een verschillend bereik (bijvoorbeeld &quot;Actief&quot; in &quot;Bezoek&quot; in &quot;Bezoeker&quot;)</li></ul> | Hoewel sommige complexiteitsfactoren niet kunnen worden voorkomen, zoek dan naar mogelijkheden om de complexiteit van je segmenten te verminderen. Over het algemeen geldt dat hoe specifieker u kunt zijn bij de criteria voor uw segment, hoe beter. Bijvoorbeeld:<ul><li>Bij containers is het gebruik van één container boven aan het segment sneller dan een reeks geneste containers.</li><li>Met operatoren is &#39;equals&#39; sneller dan &#39;contains&#39; en is &#39;equals any of&#39; sneller dan &#39;contains any of&#39;.</li><li>Met veel criteria, EN zullen de exploitanten sneller zijn dan een reeks OF exploitanten.</li></ul> Zoek naar mogelijkheden om veel OR-instructies te reduceren tot één &quot;is gelijk aan een van&quot;-instructies.<br><br>[Classificaties](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html) kunt u ook helpen om een groot aantal waarden samen te voegen tot bondige groepen waaruit u vervolgens segmenten kunt maken. De segmentatie op classificatiegroepen verstrekt prestatiesvoordelen over segmenten die vele OF verklaringen bevatten of &quot;bevat&quot;criteria. |
| Vereenvoudiging van visualisatie (segmenten, metrics, filters) | Het type visualisatie (bijv. uitval vs. een vrije-vormtabel) dat op zichzelf aan een project wordt toegevoegd, heeft geen grote invloed op de projectprestaties. Het is de complexiteit van de visualisatie die de verwerkingstijd zal vergroten. | Tot de factoren die een visualisatie complexer maken, behoren:<ul><li>Bereik van aangevraagde gegevens</li><li>Aantal toegepaste segmenten; bijvoorbeeld segmenten die worden gebruikt als rijen van een vrije-vormtabel</li><li>Gebruik van complexe segmenten</li><li>[Statisch item](/help/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md) rijen of kolommen in vrije-vormtabellen</li><li>Filters die worden toegepast op rijen in vrije-vormtabellen</li><li>Aantal meegeleverde metrics, vooral berekende metrics die gebruikmaken van segmenten</li></ul> | Als je merkt dat je projecten niet zo snel laden als je wilt, kun je, waar mogelijk, bepaalde segmenten vervangen door eVars en filters.<br><br>Als u zich voortdurend het gebruiken van segmenten en berekende metriek voor gegevenspunten vindt die voor uw zaken belangrijk zijn, denk na verbeterend uw implementatie om deze gegevenspunten directer te vangen. Dankzij tagmanager zoals Adobe Experience Platform Launch en verwerkingsregels voor Adobe kunnen implementatiewijzigingen snel en eenvoudig worden geïmplementeerd. |
| Grootte van rapportsuite | De hoeveelheid gegevens die in uw rapportsuite wordt verzameld. | - | Overleg met uw implementatieteam of een Adobe-expert om te bepalen of er implementatieverbeteringen zijn die kunnen worden aangebracht om de algehele ervaring in Adobe Analytics te verbeteren. |
