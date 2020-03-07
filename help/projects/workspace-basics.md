---
title: Grondbeginselen werkruimte
description: Beschrijft hoe te om basisrapporten in Werkruimte te trekken
translation-type: tm+mt
source-git-commit: eba2b60496976eb6027d58e0ce231ee046c8fc02

---


# Grondbeginselen werkruimte

Als u nog niet vertrouwd bent met het werkruimtehulpmiddel, zijn hier sommige uiteinden om u begonnen te krijgen.

De werkruimte is het belangrijkste hulpmiddel van Adobe om uitvoerbare op gegevens-gebaseerde besluiten voor uw organisatie te nemen. De gemeenschappelijkste visualisatie, de freeformlijst, laat u gemakkelijk aangepaste rapporten tot stand brengen gebruikend afmetingen, metriek, segmenten, en datumwaaiers.

## Trek een basisgerangschikt rapport in Werkruimte

Een gerangschikt rapport toont een geaggregeerde totale mening van elke afmetingswaarde, die de grootste waarden eerst toont. Deze types van rapporten zijn nuttig om te zien welke componenten van uw plaats het meest efficiënt zijn, zoals welke pagina&#39;s het meeste verkeer krijgen of welke producten het meest verkopen.

1. Zorg ervoor u aan [analytics.adobe.com](https://analytics.adobe.com)het programma wordt geopend.
1. Klik in de navigatiebalk bovenaan op **[!UICONTROL Workspace]**.
1. Klik op **[!UICONTROL Create New Project]**.
1. In modale popup, zorg ervoor het &quot;Lege Project&quot;wordt geselecteerd, dan klik **[!UICONTROL Create]**.
1. Voor de linkerzijde, zou u een lijst van afmetingen, metriek, segmenten, en datumwaaiers moeten zien. Bepaal de plaats van de afmeting van Pagina&#39;s (gekleurd oranje), en sleep het over aan het canvas waar het &quot;Daling een Afmeting hier&quot;zegt.
1. Een rapport dat de hoogste pagina&#39;s voor deze maand toont kan worden gezien. De Werkruimte van de analyse bevolkte automatisch het rapport met metrisch [Voorkomen](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-occurrences.html) .
1. Bepaal de plaats van de Bezoeken metrisch (gekleurde groen), en sleep het of **over** of **naast** de metrische kopbal van Voorkomen (vermijd plaatsend het boven metrisch). Als u metrisch Bezoeken bovenop Voorkomen sleept, wordt metrisch vervangen in rapportering. Als u metrisch Bezoeken naast Voorkomen sleept, worden beide metriek getoond zij aan zij.
1. Als u uw project zou willen bewaren, klik **[!UICONTROL Project]>[!UICONTROL Save]**in het hogere linkermenu.

## Trek een fundamenteel trending rapport in Werkruimte

Een trending rapport toont een over-tijd mening van metriek gebruikend de geselecteerde datumwaaier. Deze soorten rapporten zijn nuttig om tendensen in tijd te identificeren, en kunnen worden gebruikt om succes of mislukking van bedrijfsbesluiten te meten die worden genomen. Bijvoorbeeld, kon u een rapport bekijken van de paginameningen dat in tijd wordt trended om te zien of hielp een plaatsredesign verkeer verhogen of verminderen.

1. Zorg ervoor u aan [analytics.adobe.com](https://analytics.adobe.com)het programma wordt geopend.
1. Klik in de navigatiebalk bovenaan op **[!UICONTROL Workspace]**.
1. Klik op **[!UICONTROL Create New Project]**.
1. In modale popup, zorg ervoor het &quot;Lege Project&quot;wordt geselecteerd, dan klik **[!UICONTROL Create]**.
1. Voor de linkerzijde, zou u een lijst van afmetingen, metriek, segmenten, en datumwaaiers moeten zien. Bepaal de plaats van de afmeting van de Meningen van de Pagina, en sleep het aan de kleine ruimte op het geëtiketteerde canvas **[!UICONTROL Drop a Metric Here]**. Vermijd het laten vallen in de ruimte die voor afmetingen (minstens voor deze oefening) wordt gereserveerd.
1. Merk op dat als de rapportreeks gegevens heeft, u een basisrapport zou moeten zien van de paginameningen dat over de huidige maand wordt geknepen. De Werkruimte van de analyse die automatisch in de de datumwaaier van de &#39;Dag&#39; wordt gebracht zodat kunt u de trend van paginameningen voor de huidige maand zien.
1. Bepaal de plaats van de de datumwaaier van de Week (gekleurde paars) in de lijst van de componenten van het datumbereik op de linkerzijde. Klik de titel van de datumwaaier om alle componenten van de datumwaaier uit te breiden en te zien, of de onderzoeksbar te gebruiken.
1. Sleep de de datumwaaier van de Week bovenop de de datumwaaier van de Dag op het canvas om het te vervangen.
1. Merk op dat uw trending rapport nu door week in plaats van dag wordt bijeengevoegd.
1. Als u uw project zou willen bewaren, klik **[!UICONTROL Project]>[!UICONTROL Save]**in het hogere linkermenu.

## Experimenteren met het gereedschap

Aangezien de Werkruimte een rapporteringshulpmiddel is, heeft het geen invloed op gegevensinzameling. Er zijn geen gevolgen om zonder onderscheid componenten in een project te slepen om te zien wat werkt. Sleep verschillende combinaties van afmetingen en metriek in uw werkruimteproject om te zien wat aan u beschikbaar is.

Als u toevallig een ongeldige component aan uw werkruimteproject sleept of zou willen terugkeren een stap, ctrl+Z (Vensters) of cmd+Z (MAC) drukken om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door **[!UICONTROL Project]>[!UICONTROL New]**in het hogere linkermenu te klikken.

## Probleemoplossing

### Wanneer ik metrisch over sleep, zegt het &quot;Ongeldige gegevens&quot;.

De ongeldige gegevens betekenen dat Adobe geen gegevens kan terugkeren gebruikend de combinatie afmetingen en metriek die in het rapport worden gebruikt. Bijvoorbeeld, kunnen twee metriek die bovenop elkaar worden gestapeld niet als gegevens zijn teruggekeerd, aangezien er geen manier is om twee metriek te tonen die manier. In plaats daarvan, plaats de metriek zij aan zij.

### Wanneer ik metrisch over sleep, zie ik geen daadwerkelijke gegevens - enkel nul.

Als u met succes een werkruimterapport creeert maar er geen gegevens zijn, zijn er een paar dingen u kunt controleren:

* Controleer de rapportreeks tweemaal en zorg ervoor het met gegevens bevolkt is.
* Als u een segment in uw rapport gebruikt, zouden de segmentcriteria geen gegevens kunnen aanpassen. Probeer verwijderend het segment of aanpassend de segmentdefinitie.
* Controleer de datumwaaier in het hogere recht en zorg ervoor het aan een waarde wordt geplaatst die u zou verwachten.
* Navigeer aan uw website en gebruik Debugger om te bevestigen dat het gegeven wordt verzameld.

## Extra middelen

Merk op dat de volgende middelen naar het gebruiken van Werkruimte in het traditionele product van de Analyse van Adobe, niet in de Analyse van de Reis van de Klant kunnen verwijzen.

* Blogberichten:
   * [Organisaties mondiger maken met slimmere analyse](https://theblog.adobe.com/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/)
   * [Analysewerkruimte: De geheime saus krijgt &#39;n tastier](https://theblog.adobe.com/analysis-workspace-secret-sauce-getting-tastier/)
   * [Waarom u de Werkruimte van de Analyse zou moeten gebruiken](https://theblog.adobe.com/why-you-should-be-using-analysis-workspace-in-adobe-analytics/)
   * [5 tips om uw productiviteit te maximaliseren met analysewerkruimte](https://theblog.adobe.com/5-tips-maximize-productivity-analysis-workspace/)

## Volgende stappen

Er zijn veel richtingen te gaan om uw begrip van Werkruimte te verdiepen. Hier zijn sommige grondbeginselen die Adobe adviseert:

### Voor eind - gebruikers die kennis willen uitbreiden over hoe te om Werkruimte te gebruiken

* [Details over de Werkruimte UI](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/t-freeform-project.html): Nu u een basisrapport hebt gecreeerd, word meer vertrouwd met de rest van de interface.
* [Visualisaties in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html): De lijsten van de vrije vorm zijn slechts één type van visualisatie in de Werkruimte van de Analyse. Leer hoe te om andere visualisaties, zoals lijngrafieken, bargrafieken, en geo kaarten te gebruiken.
* [Afmetingen in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.html): Meer weten over welke dimensies en hoe u ze in meer dan alleen gerangschikte rapporten kunt gebruiken?
* [Metriek in Werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/apply-create-metrics.html): Leer meer over welke metriek zijn en hoe te om hen in andere delen van vrije vormlijsten te gebruiken.
* [Inleiding tot segmentering](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html): Leer over welke segmenten zijn en trek een basisrapport gebruikend een segment.
* [Datumbereiken in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html): Leer over relatieve en het rollen data, en gebruik hen in werkruimteprojecten.
* [Projecten](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html) delen in werkruimte: Toon uw collega het geweldige project van de Werkruimte u creeerde.

### Voor analisten en admins die de kwaliteit van werkruimte in hun organisatie willen verbeteren

* [Toestemmingen](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html)voor analysewerkruimte: Wijs gebruikerstoestemmingen aan Werkruimte via de Console van Adobe toe Admin.
* [Sjablonen in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html): Creeer malplaatjes zodat kunnen uw collega&#39;s met een projectruimte beginnen die aan hun behoeften wordt aangepast.
* [De kromming](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html)van de werkruimte: Creeer een project dat beschikbare componenten beperkt, die werkruimte voor hen toegankelijker maken minder vertrouwd met het hulpmiddel
