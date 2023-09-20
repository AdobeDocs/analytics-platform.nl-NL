---
title: Vergelijk Customer Journey Analytics met de oplossingen van BI
description: Vergelijk Customer Journey Analytics met de oplossingen van BI
role: User
solution: Customer Journey Analytics
feature: Basics
exl-id: ae66cd06-7ec1-4174-a3cf-939c3a66b840
source-git-commit: dd83785ea67a48e2051c60568e6fe5b436edf4db
workflow-type: tm+mt
source-wordcount: '1649'
ht-degree: 0%

---

# Vergelijk Customer Journey Analytics met de oplossingen van BI

Met de huidige nadruk op klantenervaring, vereisen de merken geavanceerde oplossingen om de holistische klantenreis beter te begrijpen. Het begrip van deze volledige klantenreis staat u toe om waardevolle inzichten in te analyseren en te bereiken hoe online en off-line kanalen klanten in dienst nemen en tot stijgende omzetting, behoud, en loyaliteit leiden. In dit verband kan een klant de eenvoudige online bestelling zijn van een maaltijd in een sushi voedselketen. Of de aankoop van een nieuwe auto, waarbij de klant online onderzoek combineert met bezoeken aan de showroom van de dealer, en een definitieve persoonlijk aankoop.

Vele organisaties hebben hun gegevens in het omni-kanaal geconsolideerd in een gegevenshoek of een datapakhuis. De bedrijfsintelligentie (BI) hulpmiddelen worden gebruikt bovenop deze gegevensopslag om de rapporten, visualisaties, en inzichten te verstrekken die de zaken vereisen om de klantenreis te begrijpen. Vaak is deze combinatie van oplossingen en hulpmiddelen van algemene aard en ontwerp en niet expliciet gericht op de klant. Customer Journey Analytics richt zich op het mondig maken van degenen die verantwoordelijk zijn voor de klantervaring, zoals marketers, gegevensanalisten, data wetenschappers. Het hulpmiddel staat hen toe om de klantenreis in volledige context over alle kanalen in echt - tijd zonder beperkingen te visualiseren die vele andere hulpmiddelen van BI hebben.

In dit gedeelte van de documentatie worden de fundamentele verschillen tussen Customer Journey Analytics en algemeen gebruikte BI-gereedschappen beschreven. Hiervoor wordt eerst gekeken naar de algemene workflow die wordt gebruikt om het hierboven vermelde doel te bereiken: inzicht in die reis van de klant. Dan verstrekt het meer details over hoe het gegeven wordt opgeslagen, verzameld, en verschillend gevraagd tussen Customer Journey Analytics en de hulpmiddelen van BI. Tot slot wordt hiermee uitgelegd wat de verschillen zijn in visualisatiemogelijkheden.

## Traditionele BI-workflow

Een veelvuldig obstakel voor de traditionele benadering van het analyseren van klantentransporten is dat het niet klantgericht is. Elk team verzamelt gegevens op locaties, analyseert en optimaliseert ervaringen op basis van de gegevens waartoe zij toegang hebben.

![Traditionele BI-workflow zoals beschreven in deze sectie](./assets/biworkflow.png)

Als u wilt begrijpen hoe een specifieke digitale campagne een off-line actie beïnvloedt die in een verschillende gegevenssilo wordt opgeslagen, geeft u een verzoek aan de rij van het team van BI uit. Het team van BI schrijft de vereiste vraag om de gegevens te verwerven en om te zetten. Zodra de ruwe gegevens worden teruggewonnen, leidt het team van BI tot visualisatie. De gegevens worden met u gedeeld en u besteedt tijd aan het doornemen van inzichten en het extraheren van gegevens voor activering in andere systemen.

Elk van deze stappen kan uren, dagen, of zelfs weken nemen. Als er vervolgvragen of problemen met de gevraagde gegevens zijn, kan het nog meer tijd duren voordat die vragen zijn beantwoord en de cyclus verdergaat. Voor aan de gang zijnde analyse, exploratie en begrip van de klantenreis, is dit proces inefficiënt en niet scalable. Ook, richten de teams van BI typisch meer dan enkel klant op reis-gerelateerde vragen.

## Customer Journey Analytics: gedemocratiseerde workflow voor online en offline gegevens

Customer Journey Analytics verstrekt een milieu om online en off-line dwars-kanaalgegevens op het overkoepelende klantenniveau met het enige doel te verbinden om de klantenreis te begrijpen. Hiervoor is een eerste installatie vereist [verbinden](/help/connections/overview.md) en [weergaven definiëren](/help/data-views/data-views.md) aan de gegevens die u als relevant aanmerkt. Zodra deze gegevens echter zijn voltooid, zijn ze gemakkelijk beschikbaar voor doorlopende analyse en exploratie. U kunt geleidelijk inzicht krijgen in en inzicht krijgen in de reizen van de klant. Door gecombineerde online en off-line gegevens te democratiseren, kunt u klant-reis-gerelateerde vragen in seconden beantwoorden.

![Workflow voor Customers Journey Analytics zoals beschreven in deze sectie](./assets/cjaworkflow.png)

U kunt Customer Journey Analytics gebruiken om vragen te stellen gebruikend het visuele milieu van Analysis Workspace en inzichten bijna onmiddellijk te verkrijgen. De gegevens en rapporten van het dwars-kanaal zijn onmiddellijk beschikbaar, zonder SQL vereiste code. Extra query&#39;s en analyse kunnen worden uitgevoerd met een eenvoudige sleepbewerking en neerzetbewerking in de gebruikersinterface, met volledig gecorreleerde gegevens. U kunt vragen blijven stellen, geleidelijk meer details onderzoeken zoals u vereist. U kunt dan onmiddellijk actie ondernemen op de inzichten die u ontdekt, zoals het delen van publiek voor activering en orkest.

## De krachtige rapporteringsengine van de Customer Journey Analytics

Customer Journey Analytics gebruikt een krachtige bedrijfseigen architectuur die analyse over honderden of zelfs duizenden servers aan vertoningsgegevens in Analysis Workspace binnen seconden verspreidt. Enkele opmerkelijke eigenschappen van deze verwerkingsarchitectuur zijn:

* **Geoptimaliseerd voor individuele klant-gerelateerde vragen**: Technisch, slaat de Customer Journey Analytics de gegevens in een verdeelde rapporteringsmotor op die uitgebreid gebruik van caching maakt. Die motor wordt fijngemaakt voor ontvankelijke vragen over individueel-vlakke gebeurtenisgegevens, en als dusdanig perfect geoptimaliseerd voor klant-gerelateerde vragen. De rapportengine slaat gegevens op in kolomgeoriënteerde bitmapindexen die een snelle berekening van geaggregeerde gegevens ter plekke mogelijk maken. Het heeft een uitgebreide het filtreren motor die krachtige segmentatie/publieksanalyse toelaat. En het heeft een kernbegrip van de opeenvolging onder gegevenspunten die nuttig is in het analyseren van gedrag over die gegevenspunten (de orde dat de dingen voorkwamen) en voor het toewijzen van attributie gebruikend diverse, complexe modellen.

* **Snelle toepassing van complexe paden en filters**: De rapportengine werkt op gedeeltelijk geordende, hiërarchische gegevenssets (bijvoorbeeld persoonlijk -> sessies -> gebeurtenissen). Alle gegevens voor een object op hoofdniveau (afzonderlijke profielen) bevinden zich op één verwerkingsknooppunt voor nauwkeurige resultaten. Dankzij deze partitionering kunnen complexe paden en filters snel worden toegepast. Complexe bewerkingen zoals sessionisatie, attributie, stateful persistentie van gegevenskenmerken en complexe opties voor gegevensmanipulatie worden op schaal met een snelle rapportagetijd uitgevoerd. In de wereld van BI, vereisen die soorten verrichtingen typisch nieuwe kubussen OLAP om voor elk gebruiksgeval worden gecreeerd. De Customer Journey Analytics die motor meldt staat onbelemmerde toegang tot de volledige dataset op elke vraag toe, resulterend in volledig gecorreleerde gegevens zonder het vereisen van om het even welk coderen van tevoren.

* **Efficiënte query op complexe gegevensstromen**: Een van de grootste verschillen tussen de meldende engine en traditionele SQL- en NoSQL-databases is dat deze in staat is om voorspellingen te bepalen op basis van volgorde-georiënteerde relaties op een fundamenteel niveau. Deze fundamentele zoekbewerkingen kunnen de recordstream bekijken, die bestaat uit vele interleaved (en zelfs geneste) reeksen. Zij voeren een vraag tegen elk van deze onderling verweven stromen van gegevens met de efficiency van één enkele, aangrenzende opeenvolgingsverrichting uit.

* **Ontworpen om grote vragen snel te beantwoorden**: De rapportageengine is niet zo algemeen bedoeld als traditionele grote gegevenssystemen. Nochtans, wordt het specifiek ontworpen om vragen te beantwoorden die miljoenen of zelfs miljarden verslagen (gebeurtenisgegevens/ervaringsgebeurtenissen), over het algemeen in onder een seconde overspannen. In tegenstelling tot andere grote gegevenssystemen, doet het dit niet door de gegevens te bemonsteren of de antwoorden op alle vragen vooraf te berekenen die u zou kunnen stellen. In plaats daarvan kan het de antwoorden snel genoeg berekenen om interactieve vragen van gebruiksgevallen te steunen. Dit specifieke ontwerp van de Customer Journey Analytics die motor meldt vergemakkelijkt het gemakkelijk en aan hoge snelheid beschikbaar zijn voor aan de gang zijnde analyse en exploratie, zodat u geleidelijk inzicht en inzicht in klantenreizen kunt verwerven.

* **Werkt als een oplossing zonder kop**: U definieert de afmetingen, metriek, filters op één locatie en elke Customer Journey Analytics-client (inclusief de openbare Customer Journey Analytics-API) heeft toegang tot deze componenten. Dit onttrekt complexe vragen weg van eind - gebruikers en waarborgt dat de resultaten het zelfde zijn, geen kwestie die rapporteert of visualisatieclient u gebruikt.

## De unieke visualisatiemogelijkheden van de Customer Journey Analytics

De rapporteringsmotor is fundamenteel voor Customer Journey Analytics om u toe te staan om geleidelijk met alle gegevens van de klantenreis binnen die rapporteringsmotor in wisselwerking te staan en te handelen. Customer Journey Analytics wordt geleverd met een uitgebreide set componenten die u in staat stellen dit visueel en via slepen en neerzetten te doen. Met BI-visualisatieprogramma&#39;s kunt u zoeken binnen de grenzen van SQL-voorbereide gegevens (zoals gedefinieerd door IT). Met Customer Journey Analytics kunt u zo veel mogelijk splitsen en segmenteren, zonder dat u weer een SQL-weergave hoeft te maken.

&quot;Progressief&quot;is een zeer belangrijk concept hier: in tegenstelling tot de meeste visualisaties in de hulpmiddelen van BI, staat visuele belemmering-en-daling UI in Customer Journey Analytics u toe om uw gegevens voor uw specifieke behoeften onophoudelijk te breken: u kunt visuele vragen op interactieve wijze bouwen gebruikend relevante metriek, dimensies, filters (segmenten), berekeningen, tijdlijnen, annotaties, en andere analysewaarden.

De volgende onderdelen van visualisatie zijn ingebouwd:

* **Functies van virtuele analisten** zoals [Anomaly Detection](/help/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) die voorspellende algoritmen en machinaal leren gebruiken om inzicht te krijgen in wat ongewoon gedrag in uw gegevens drijft.

* **Geavanceerde analysefuncties** die specifiek op de inzichten van de klantenreis gericht zijn, zoals [stroomdiagrammen](/help/analysis-workspace/visualizations/c-flow/flow.md), [Kenmerk, deelvenster](/help/analysis-workspace/c-panels/attribution.md), [herfstschema&#39;s](/help/analysis-workspace/visualizations/fallout/fallout-flow.md), en [uitsplitsingen dimensie](/help/components/dimensions/t-breakdown-fa.md). Voorbeelden van out-of-the-box-visualisaties zijn:

   * [Analyse van het behoud van klanten via cohort-/latentietabellen](/help/analysis-workspace/visualizations/cohort-table/cohort-use-cases.md), waar u eenvoudig metriek/afmetingen sleept en neerzet in een bouwer en u wordt gedaan in minder dan 30 seconden,

   * [Fallout](/help/analysis-workspace/visualizations/fallout/configuring-fallout.md) / [stroom](/help/analysis-workspace/visualizations/c-flow/create-flow.md) visualisaties. In minder dan een minuut instellen.

* **Segmenteringsmogelijkheden in elke stap van uw progressieve exploratie**: wanneer u het zinvol vindt, kunt u uw publiek weer in het Experience Platform publiceren en van daaruit naar een van de ondersteunde bestemmingen.

* **Sessionering** dat volledig [aanpasbaar](/help/data-views/component-settings/persistence.md): u bepaalt wanneer een zitting, als deel van een kanaal in een klantenreis, begint en beëindigt.

* **Cursus en democratisering**: De dashboards die in Customer Journey Analytics worden gecreeerd kunnen zijn:

   * [Gekromd](/help/analysis-workspace/curate-share/curate.md) aan andere personen in de organisatie voor doorlopende exploratie;
   * Geëxporteerd naar Excel met [Report Builder](/help/report-builder/report-buider-overview.md) (een specifieke insteekmodule),
   * [Gedeeld](/help/analysis-workspace/curate-share/share-projects.md) in verschillende vormen, waaronder [PDF](/help/analysis-workspace/export/download-send.md), [CSV](/help/analysis-workspace/export/download-send.md) en via een [speciale mobiele app](/help/mobile-app/home.md), aan degenen die geïnteresseerd zijn in de eindverslagen en/of visualisaties.

Het vergelijken van de visualisatiemogelijkheden van de Customer Journey Analytics met welke hulpmiddelen van BI is moeilijk wegens de verscheidenheid van beschikbare visualisaties. Sommige hulpmiddelen van BI hebben geavanceerdere visualisaties, maar de Customer Journey Analytics concentreert zich op interactieve en interoperabele de reisvisualisaties van de klant die u toestaan om de gegevens binnen seconden te breken terwijl niet het &quot;in rekening brengen&quot;u voor elke extra vraag.


## Samenvatting

Customer Journey Analytics verschilt van de hulpmiddelen van BI in hoe het een hoogst geoptimaliseerde klant-reis-geconcentreerde rapporteringsmotor naadloos met gebruikersvriendelijke hulpmiddelen en componenten integreert om analyse uit te voeren en rapporten en geavanceerde visualisaties te bouwen. Allemaal vanuit één interface, zonder dat u heen en weer moet schakelen tussen de query-engine en de visualisatieomgeving.
