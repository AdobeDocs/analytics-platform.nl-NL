---
title: Customer Journey Analytics- en BI-oplossingen vergelijken
description: Customer Journey Analytics- en BI-oplossingen vergelijken
role: User
solution: Customer Journey Analytics
feature: Basics
exl-id: ae66cd06-7ec1-4174-a3cf-939c3a66b840
source-git-commit: 720751130d0f66bddffd13c6f160a85fcc7a7206
workflow-type: tm+mt
source-wordcount: '1648'
ht-degree: 0%

---

# Customer Journey Analytics- en BI-oplossingen vergelijken

Met de huidige nadruk op klantenervaring, vereisen de merken geavanceerde oplossingen om de holistische klantenreis beter te begrijpen. Het begrip van deze volledige klantenreis staat u toe om waardevolle inzichten in te analyseren en te bereiken hoe online en off-line kanalen klanten in dienst nemen en tot stijgende omzetting, behoud, en loyaliteit leiden. In dit verband kan een klant de eenvoudige online bestelling zijn van een maaltijd in een sushi voedselketen. Of de aankoop van een nieuwe auto, waarbij de klant online onderzoek combineert met bezoeken aan de showroom van de dealer, en een definitieve persoonlijk aankoop.

Vele organisaties hebben hun gegevens in het omni-kanaal geconsolideerd in een gegevenshoek of een datapakhuis. De bedrijfsintelligentie (BI) hulpmiddelen worden gebruikt bovenop deze gegevensopslag om de rapporten, visualisaties, en inzichten te verstrekken die de zaken vereisen om de klantenreis te begrijpen. Vaak is deze combinatie van oplossingen en hulpmiddelen van algemene aard en ontwerp en niet expliciet gericht op de klant. Customer Journey Analytics richt zich op het mondig maken van de verantwoordelijken voor de klantervaring, zoals marketers, data-analisten en data-wetenschappers. Het hulpmiddel staat hen toe om de klantenreis in volledige context over alle kanalen in echt - tijd zonder beperkingen te visualiseren die vele andere hulpmiddelen van BI hebben.

In dit gedeelte van de documentatie worden de fundamentele verschillen tussen Customer Journey Analytics en veelgebruikte BI-tools toegelicht. Daarbij wordt eerst gekeken naar de algemene workflow die wordt gebruikt om het hierboven vermelde doel te bereiken: inzicht in die reis van de klant. Dan verstrekt het meer details over hoe het gegeven wordt opgeslagen, verzameld, en verschillend gevraagd tussen Customer Journey Analytics en de hulpmiddelen van BI. Tot slot wordt hiermee uitgelegd wat de verschillen zijn in visualisatiemogelijkheden.

## Traditionele BI-workflow

Een veelvuldig obstakel voor de traditionele benadering van het analyseren van klantentransporten is dat het niet klantgericht is. Elk team verzamelt gegevens op locaties, analyseert en optimaliseert ervaringen op basis van de gegevens waartoe zij toegang hebben.

![ Traditionele BI werkschema zoals die in deze sectie wordt beschreven ](./assets/biworkflow.png)

Als u wilt begrijpen hoe een specifieke digitale campagne een off-line actie beïnvloedt die in een verschillende gegevenssilo wordt opgeslagen, geeft u een verzoek aan de rij van het team van BI uit. Het team van BI schrijft de vereiste vraag om de gegevens te verwerven en om te zetten. Zodra de ruwe gegevens worden teruggewonnen, leidt het team van BI tot visualisatie. De gegevens worden met u gedeeld en u besteedt tijd aan het doornemen van inzichten en het extraheren van gegevens voor activering in andere systemen.

Elk van deze stappen kan uren, dagen, of zelfs weken nemen. Als er vervolgvragen of problemen met de gevraagde gegevens zijn, kan het nog meer tijd duren voordat die vragen zijn beantwoord en de cyclus verdergaat. Voor aan de gang zijnde analyse, exploratie en begrip van de klantenreis, is dit proces inefficiënt en niet scalable. Ook, richten de teams van BI typisch meer dan enkel klant op reis-gerelateerde vragen.

## Customer Journey Analytics: gedemocratiseerde workflow voor online en offline gegevens

Customer Journey Analytics biedt een omgeving voor het online en offline verbinden van kanaalgegevens op overkoepelend klantniveau, uitsluitend om inzicht te krijgen in de reis van de klant. Het vereist aanvankelijke opstelling om [&#128279;](/help/connections/overview.md) te verbinden en [ meningen ](/help/data-views/data-views.md) aan de gegevens te bepalen u relevant kwalificeert. Zodra deze gegevens echter zijn voltooid, zijn ze gemakkelijk beschikbaar voor doorlopende analyse en exploratie. U kunt geleidelijk inzicht krijgen in en inzicht krijgen in de reizen van de klant. Door gecombineerde online en off-line gegevens te democratiseren, kunt u klant-reis-gerelateerde vragen in seconden beantwoorden.

![ het werkschema van Customer Journey Analytics zoals die in deze sectie ](./assets/cjaworkflow.png) wordt beschreven

U kunt Customer Journey Analytics gebruiken om vragen te stellen met de visuele Analysis Workspace-omgeving en bijna onmiddellijk inzichten te verkrijgen. De gegevens en rapporten van het dwars-kanaal zijn onmiddellijk beschikbaar, zonder SQL vereiste code. Extra query&#39;s en analyse kunnen worden uitgevoerd met een eenvoudige sleepbewerking en neerzetbewerking in de gebruikersinterface, met volledig gecorreleerde gegevens. U kunt vragen blijven stellen, geleidelijk meer details onderzoeken zoals u vereist. U kunt dan onmiddellijk actie ondernemen op de inzichten die u ontdekt, zoals het delen van publiek voor activering en orkest.

## Customer Journey Analytics krachtige rapporteringsengine

Customer Journey Analytics gebruikt een krachtige bedrijfseigen architectuur die analyse over honderden of zelfs duizenden servers verspreidt om gegevens in Analysis Workspace binnen seconden te tonen. Enkele opmerkelijke eigenschappen van deze verwerkingsarchitectuur zijn:

* **Geoptimaliseerd voor individuele op klant betrekking hebbende vragen**: Technisch, slaat Customer Journey Analytics de gegevens in een verdeelde rapporteringsmotor op die uitgebreid gebruik van caching maakt. Die motor wordt fijngemaakt voor ontvankelijke vragen over individueel-vlakke gebeurtenisgegevens, en als dusdanig perfect geoptimaliseerd voor klant-gerelateerde vragen. De rapportengine slaat gegevens op in kolomgeoriënteerde bitmapindexen die een snelle berekening van geaggregeerde gegevens ter plekke mogelijk maken. Het heeft een uitgebreide segmenteringsmotor die krachtige segmentatie/publieksanalyse toelaat. En het heeft een kernbegrip van de opeenvolging onder gegevenspunten die nuttig is in het analyseren van gedrag over die gegevenspunten (de orde dat de dingen voorkwamen) en voor het toewijzen van attributie gebruikend diverse, complexe modellen.

* **Snelle toepassing van complex het kleven en segmenten**: De rapportmotor werkt op gedeeltelijk bevolen, hiërarchische datasets (bijvoorbeeld, persoon -> zittingen -> gebeurtenissen). Alle gegevens voor een object op hoofdniveau (afzonderlijke profielen) bevinden zich op één verwerkingsknooppunt voor nauwkeurige resultaten. Dankzij deze partitionering kunt u complexe paden en segmenten snel toepassen. Complexe bewerkingen zoals sessionisatie, attributie, stateful persistentie van gegevenskenmerken en complexe opties voor gegevensmanipulatie worden op schaal met een snelle rapportagetijd uitgevoerd. In de wereld van BI, vereisen die soorten verrichtingen typisch nieuwe kubussen OLAP om voor elk gebruiksgeval worden gecreeerd. De Customer Journey Analytics die motor meldt staat onbeperkte toegang tot de volledige dataset op elke vraag toe, resulterend in volledig gecorreleerde gegevens zonder het vereisen van om het even welk coderen van tevoren.

* **Efficiënte vraag van complexe gegevensstromen**: Één van de grootste verschillen van de rapporterende motor van traditionele SQL en gegevensbestanden is zijn capaciteit om predikaten te bepalen die op opeenvolging-georiënteerde verhoudingen op een fundamenteel niveau worden gebaseerd. Deze fundamentele zoekbewerkingen kunnen de recordstream bekijken, die bestaat uit vele interleaved (en zelfs geneste) reeksen. Zij voeren een vraag tegen elk van deze onderling verweven stromen van gegevens met de efficiency van één enkele, aangrenzende opeenvolgingsverrichting uit.

* **Ontworpen om grote vragen** snel te beantwoorden: De rapporterende motor is niet zo algemeen doel zoals traditionele grote gegevenssystemen. Nochtans, wordt het specifiek ontworpen om vragen te beantwoorden die miljoenen of zelfs miljarden verslagen (gebeurtenisgegevens/ervaringsgebeurtenissen), over het algemeen in onder een seconde overspannen. In tegenstelling tot andere grote gegevenssystemen, doet het dit niet door de gegevens te bemonsteren of de antwoorden op alle vragen vooraf te berekenen die u zou kunnen stellen. In plaats daarvan kan het de antwoorden snel genoeg berekenen om interactieve vragen van gebruiksgevallen te steunen. Dit specifieke ontwerp van de Customer Journey Analytics-rapporteringsengine maakt het gemakkelijker om gegevens snel en snel beschikbaar te maken voor doorlopende analyse en exploratie, zodat u geleidelijk inzicht kunt krijgen in en inzicht kunt krijgen in klantreizen.

* **handelt als een headless oplossing van BI**: U bepaalt uw dimensies, metriek, segmenten op één plaats, en dan kan om het even welke cliënt van Customer Journey Analytics (met inbegrip van onze openbare Customer Journey Analytics API) tot die componenten toegang hebben. Dit onttrekt complexe vragen weg van eind - gebruikers en waarborgt dat de resultaten het zelfde zijn, geen kwestie die rapporteert of visualisatieclient u gebruikt.

## Unieke visualisatiefuncties van Customer Journey Analytics

De rapporteringsmotor is fundamenteel voor Customer Journey Analytics om u toe te staan om geleidelijk met alle gegevens van de klantenreis binnen die rapporteringsmotor in wisselwerking te staan en te handelen. Customer Journey Analytics wordt geleverd met een uitgebreide set componenten die u in staat stellen dit visueel en via slepen en neerzetten te doen. Met BI-visualisatieprogramma&#39;s kunt u zoeken binnen de grenzen van SQL-voorbereide gegevens (zoals gedefinieerd door IT). Met Customer Journey Analytics kunt u naar wens afsplitsen en segment-en-dice maken zonder dat u naar IT hoeft terug te keren om nog een SQL-weergave te bouwen.

&quot;Progressief&quot;is een zeer belangrijk concept hier: in tegenstelling tot de meeste visualisaties in de hulpmiddelen van BI, staat visuele belemmering-en-dalingsUI in Customer Journey Analytics u toe om uw gegevens voor uw specifieke behoeften onophoudelijk te breken: u kunt visuele vragen op interactieve wijze bouwen gebruikend relevante metriek, dimensies, segmenten, berekeningen, tijdlijnen, annotaties, en andere analysewaarden.

De volgende onderdelen van visualisatie zijn ingebouwd:

* **Virtuele analysefuncties** zoals [ Anomaly Detectie ](/help/analysis-workspace/c-anomaly-detection/anomaly-detection.md) die voorspellende algoritmen en machine het leren gebruiken om inzichten in te leveren wat ongewoon gedrag in uw gegevens drijft.

* **Geavanceerde analysefuncties** die specifiek op de inzichten van de klantenreis, als [ stroomdiagrammen ](/help/analysis-workspace/visualizations/c-flow/flow.md), [ het paneel van de Attributie ](/help/analysis-workspace/c-panels/attribution.md), [ fallout diagrammen ](/help/analysis-workspace/visualizations/fallout/fallout-flow.md), en [ afmetingsonderverdelingen ](/help/components/dimensions/t-breakdown-fa.md) worden geconcentreerd. Voorbeelden van out-of-the-box-visualisaties zijn:

   * [ analyse van het het behoud van de Klant via cohort/latentietabellen ](/help/analysis-workspace/visualizations/cohort-table/cohort-use-cases.md), waar u eenvoudig metriek/afmetingen in een bouwer sleept en u in minder dan 30 seconden wordt gedaan,

   * [ Uitval ](/help/analysis-workspace/visualizations/fallout/configuring-fallout.md) / [ stroom ](/help/analysis-workspace/visualizations/c-flow/create-flow.md) visualisaties. In minder dan een minuut instellen.

* **vermogen van de Segmentatie bij elke stap van uw progressieve exploratie**: wanneer u denkt het steek houdt, kunt u uw publiek terug in Experience Platform en van daar aan om het even welke gesteunde bestemmingen publiceren.

* **Sessionisatie** die volledig [&#128279;](/help/data-views/component-settings/persistence.md) aanpasbaar is: u bepaalt wanneer een zitting, als deel van een kanaal in een klantenreis, begint en beëindigt.

* **Curation en democratisering**: De dashboards die in Customer Journey Analytics worden gecreeerd kunnen zijn:

   * [ gekromde ](/help/analysis-workspace/curate-share/curate.md) aan andere individuen in de organisatie voor ononderbroken exploratie,
   * Geëxporteerd naar Excel met behulp van [ Report Builder ](/help/report-builder/rb-overview.md) (een toegewijde plug-in),
   * [ Gedeeld ](/help/analysis-workspace/curate-share/share-projects.md) in diverse formaten, met inbegrip van [ PDF ](/help/analysis-workspace/export/download-send.md), [ CSV ](/help/analysis-workspace/export/download-send.md) en door a [ specifieke mobiele app ](/help/mobile-app/home.md), aan die die in de definitieve rapporten en/of visualisaties geinteresseerd zijn.

Het is moeilijk om de Customer Journey Analytics-visualisatiemogelijkheden te vergelijken met de BI-gereedschappen vanwege de verschillende beschikbare visualisaties. Sommige hulpmiddelen van BI hebben geavanceerdere visualisaties, maar Customer Journey Analytics concentreert zich op interactieve en interoperabele klantenreis visualisaties die u toestaan om de gegevens binnen seconden te breken terwijl niet &quot;het in rekening brengen&quot;u voor elke extra vraag.


## Samenvatting

Customer Journey Analytics verschilt van BI-tools in de manier waarop het een uiterst geoptimaliseerde klantgerichte rapportageengine naadloos integreert met gebruiksvriendelijke tools en onderdelen om analyses uit te voeren en rapporten en geavanceerde visualisaties te maken. Allemaal vanuit één interface, zonder dat u heen en weer moet schakelen tussen de query-engine en de visualisatieomgeving.
