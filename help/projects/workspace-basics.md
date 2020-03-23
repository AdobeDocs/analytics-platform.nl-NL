---
title: Beginselen van de werkruimte
description: Beschrijft hoe te om basisrapporten in Werkruimte te trekken
translation-type: tm+mt
source-git-commit: eba2b60496976eb6027d58e0ce231ee046c8fc02

---


# Beginselen van de werkruimte

Als u nog niet bekend bent met het gereedschap Werkruimte, kunt u de volgende tips gebruiken.

Werkruimte is het belangrijkste hulpmiddel van Adobe om op gegevens gebaseerde beslissingen voor uw organisatie te nemen. De gemeenschappelijkste visualisatie, de vrije vormlijst, laat u gemakkelijk aangepaste rapporten creëren gebruikend afmetingen, metriek, segmenten, en datumwaaiers.

## Een rapport met een standaardpositie in Workspace samenstellen

Een gerangschikt rapport geeft een geaggregeerde totaalweergave van elke waarde van de dimensie weer, waarbij eerst de grootste waarden worden weergegeven. Deze typen rapporten zijn handig om te zien welke componenten van uw site het meest effectief zijn, zoals welke pagina&#39;s het meeste verkeer krijgen of welke producten het meest verkopen.

1. Controleer of u bent aangemeld bij [analytics.adobe.com](https://analytics.adobe.com).
1. Klik op de bovenste navigatiebalk **[!UICONTROL Workspace]**.
1. Klik op **[!UICONTROL Create New Project]**.
1. Controleer of Leeg project is geselecteerd in het modaal pop-upmenu en klik vervolgens op **[!UICONTROL Create]**.
1. Links ziet u een lijst met dimensies, metriek, segmenten en datumbereiken. Zoek de pagina-afmetingen (oranje gekleurd) en sleep deze naar het canvas waar de tekst &#39;Een dimensie hier neerzetten&#39; staat.
1. Een rapport met de toppagina&#39;s voor deze maand kunt u zien. De Werkruimte van de analyse bevolkte automatisch het rapport met metrische [Voorvallen](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-occurrences.html) .
1. Zoek de metrische (gekleurde groene) bezoekerslijst en sleep deze **boven** of **naast** de metrische koptekst Voorkomt (en plaats deze niet boven de metrische koptekst). Als u metrisch van Bezoekingen bovenop Voorkomen sleept, wordt metrisch vervangen in rapportering. Als u metrisch van Bezoekingen naast Voorkomen sleept, worden beide metriek getoond zij aan zij.
1. Als u uw project wilt bewaren, klik **[!UICONTROL Project][!UICONTROL Save]**> in het hogere linkermenu.

## Trek een fundamenteel trendrapport in Werkruimte

Een trended-rapport toont een weergave van metrische gegevens die de geselecteerde datumreeks gebruiken in de tijd. Deze types van rapporten zijn nuttig om tendensen in tijd te identificeren, en kunnen worden gebruikt om succes of mislukking van bedrijfsbesluiten te meten die worden genomen. Bijvoorbeeld, kon u een rapport bekijken van de paginameningen dat in tijd wordt trended om te zien of hielp een plaatsherontwerp verkeer verhogen of verminderen.

1. Controleer of u bent aangemeld bij [analytics.adobe.com](https://analytics.adobe.com).
1. Klik op de bovenste navigatiebalk **[!UICONTROL Workspace]**.
1. Klik op **[!UICONTROL Create New Project]**.
1. Controleer of Leeg project is geselecteerd in het modaal pop-upmenu en klik vervolgens op **[!UICONTROL Create]**.
1. Links ziet u een lijst met dimensies, metriek, segmenten en datumbereiken. Zoek de afmetingen voor de paginaweergaven en sleep deze naar de kleine ruimte op het canvas met het label **[!UICONTROL Drop a Metric Here]**. Vermijd het weglaten in de ruimte die is gereserveerd voor afmetingen (tenminste voor deze oefening).
1. Merk op dat als de rapportreeks gegevens heeft, u een rapport van de basispaginameningen over de huidige maand trended zou moeten zien. De Werkruimte van de analyse wordt automatisch gebracht in de de datumwaaier van &quot;Dag&quot;zodat kunt u de trend van paginameningen voor de huidige maand zien.
1. Zoek het datumbereik van de week (paars gekleurd) in de lijst met componenten voor het datumbereik aan de linkerkant. Klik op de titel van het datumbereik om alle componenten van het datumbereik uit te vouwen en weer te geven, of gebruik de zoekbalk.
1. Sleep het datumbereik van de week boven op de kop van het datumbereik van Dag op het canvas om het te vervangen.
1. Let op: uw trended-rapport wordt nu geaggregeerd per week in plaats van per dag.
1. Als u uw project wilt bewaren, klik **[!UICONTROL Project][!UICONTROL Save]**> in het hogere linkermenu.

## Experimenteren met het gereedschap

Aangezien Workspace een rapportagehulpprogramma is, heeft dit geen invloed op het verzamelen van gegevens. Er zijn geen gevolgen om zonder onderscheid componenten naar een project te slepen om te zien wat werkt. Sleep verschillende combinaties van dimensies en metriek in uw werkruimteproject om te zien wat beschikbaar aan u is.

Als u per ongeluk een ongeldige component naar uw werkruimteproject sleept of een stap wilt terugkeren, drukt u op ctrl+Z (Windows) of cmd+Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door op **[!UICONTROL Project][!UICONTROL New]**> in het menu linksboven te klikken.

## Problemen oplossen

### Wanneer ik metrisch over sleep, zegt het &quot;Ongeldige gegevens&quot;.

Ongeldige gegevens betekenen dat Adobe geen gegevens kan retourneren met de combinatie van afmetingen en metriek die in het rapport wordt gebruikt. Twee metriek die bijvoorbeeld boven op elkaar zijn gestapeld, kunnen niet als gegevens worden geretourneerd, omdat er geen manier is om twee metriek op die manier weer te geven. Plaats de metriek in plaats daarvan naast elkaar.

### Wanneer ik metrisch over sleep, zie ik geen daadwerkelijke gegevens - enkel nul.

Als u met succes een werkruimterapport creeert maar er geen gegevens zijn, kunt u een paar dingen controleren:

* Controleer de rapportsuite en zorg ervoor dat deze is gevuld met gegevens.
* Als u een segment in uw rapport gebruikt, zouden de segmentcriteria geen gegevens kunnen aanpassen. Probeer het segment te verwijderen of de segmentdefinitie aan te passen.
* Controleer de datumwaaier in hoger recht en zorg ervoor het aan een waarde wordt geplaatst die u zou verwachten.
* Navigeer naar uw website en gebruik Foutopsporing om te controleren of er gegevens worden verzameld.

## Aanvullende bronnen

De volgende bronnen kunnen verwijzen naar het gebruik van Workspace in het traditionele Adobe Analytics-product, niet in Customer Journey Analytics.

* Blogberichten:
   * [Organisaties meer mogelijkheden bieden met slimmere analyse](https://theblog.adobe.com/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/)
   * [Analyse van werkruimte: De geheime saus krijgt taster](https://theblog.adobe.com/analysis-workspace-secret-sauce-getting-tastier/)
   * [Waarom u de werkruimte Analyse moet gebruiken](https://theblog.adobe.com/why-you-should-be-using-analysis-workspace-in-adobe-analytics/)
   * [5 tips om uw productiviteit te maximaliseren met analysewerkruimte](https://theblog.adobe.com/5-tips-maximize-productivity-analysis-workspace/)

## Volgende stappen

Er zijn veel richtingen om uw begrip van Werkruimte te verdiepen. Hier volgen enkele basisbeginselen die door Adobe worden aanbevolen:

### Voor eindgebruikers die kennis willen uitbreiden over het gebruik van de werkruimte

* [Gegevens over de interface](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/t-freeform-project.html)van de werkruimte: Nu u een basisrapport hebt gecreeerd, wordt vertrouwd met de rest van de interface.
* [Visualisaties in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html): De lijsten van de vrije vorm zijn slechts één type van visualisatie in de Werkruimte van de Analyse. Leer hoe u andere visualisaties gebruikt, zoals lijngrafieken, staafgrafieken en geo-overzichten.
* [Afmetingen in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.html): Meer weten over welke afmetingen en hoe u deze kunt gebruiken in meer dan alleen gerangschikte rapporten?
* [Metrische gegevens in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/apply-create-metrics.html): Leer meer over welke metriek zijn en hoe te om hen in andere delen van vrije vormlijsten te gebruiken.
* [Inleiding tot segmentatie](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html): Leer over welke segmenten zijn en trek een basisrapport gebruikend een segment.
* [Datumbereiken in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html): Leer over relatieve en roldata, en gebruik hen in werkruimteprojecten.
* [Projecten](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html) delen in Workspace: Toon uw collega het fantastische project van de Werkruimte u creeerde.

### Voor analisten en beheerders die de kwaliteit van de werkruimte in hun organisatie willen verbeteren

* [Machtigingen voor](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html)analysewerkruimte: Wijs gebruikersmachtigingen toe aan Workspace via de Adobe Admin Console.
* [Sjablonen in werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html): Creeer malplaatjes zodat kunnen uw collega&#39;s met een projectruimte beginnen die aan hun behoeften wordt aangepast.
* [Werkruimte krommen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html): Maak een project dat beschikbare componenten beperkt, waardoor de werkruimte toegankelijker wordt voor minder bekende gebruikers
