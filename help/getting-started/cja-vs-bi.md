---
title: CJA- en BI-oplossingen vergelijken
description: Customer Journey Analytics tot BI-oplossingen vergelijken
role: User
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 91cfd3ccfe1864b6a2a50a8881e73bd778a7848e
workflow-type: tm+mt
source-wordcount: '1615'
ht-degree: 0%

---


# CJA- en BI-oplossingen vergelijken

Met de huidige nadruk op klantenervaring, vereisen de merken geavanceerde oplossingen om de holistische klantenreis beter te begrijpen. Het begrip van deze volledige klantenreis staat u toe om waardevolle inzichten in te analyseren en te bereiken hoe online en off-line kanalen klanten in dienst nemen en tot stijgende omzetting, behoud, en loyaliteit leiden. In dit verband kan een klant de eenvoudige online bestelling zijn van een maaltijd in een sushi voedselketen. Of de aankoop van een nieuwe auto, waarbij de klant online onderzoek combineert met bezoeken aan de showroom van de dealer, en een definitieve persoonlijk aankoop.

Veel organisaties hebben hun omnichannel gegevens geconsolideerd in een data-meer of data-entrepot. De bedrijfsintelligentie (BI) hulpmiddelen worden gebruikt bovenop deze gegevensopslag om de rapporten, visualisaties, en inzichten te verstrekken die de zaken vereisen om de klantenreis te begrijpen. Vaak is deze combinatie van oplossingen en hulpmiddelen van algemene aard en ontwerp en niet expliciet gericht op de klant. Customer Journey Analytics (CJA) richt zich op het mondig maken van degenen die verantwoordelijk zijn voor de klantervaring, zoals marketers, gegevensanalisten, datamanamen. Het hulpmiddel staat hen toe om de klantenreis in volledige context over alle kanalen in echt - tijd zonder beperkingen te visualiseren die vele andere hulpmiddelen van BI hebben.

In dit gedeelte van de documentatie worden de fundamentele verschillen tussen CJA en veelgebruikte BI-gereedschappen toegelicht, waarbij eerst wordt gekeken naar de algemene workflow die wordt gebruikt om de hierboven vermelde doelstelling te verwezenlijken: inzicht in die reis van de klant. Dan verstrekt het meer details over hoe het gegeven wordt opgeslagen, verzameld, en verschillend gevraagd tussen hulpmiddelen CJA en BI. Tot slot wordt hiermee uitgelegd wat de verschillen zijn in visualisatiemogelijkheden.

## Traditionele BI-workflow

Een veelvuldig obstakel voor de traditionele benadering van het analyseren van klantentransporten is dat het niet klantgericht is. Elk team verzamelt gegevens op locaties, analyseert en optimaliseert ervaringen op basis van de gegevens waartoe zij toegang hebben.

![Normale BI-workflow](./assets/biworkflow.png)

Als u wilt begrijpen hoe een specifieke digitale campagne een off-line actie beïnvloedt die in een verschillende gegevenssilo wordt opgeslagen, geeft u een verzoek aan de rij van het team van BI uit. Het team van BI schrijft de vereiste vraag om de gegevens te verwerven en om te zetten. Zodra de ruwe gegevens worden teruggewonnen, leidt het team van BI tot visualisatie. De gegevens worden met u gedeeld en u besteedt tijd aan het doornemen van inzichten en het extraheren van gegevens voor activering in andere systemen.

Elk van deze stappen kan uren, dagen, of zelfs weken vergen. Als er vervolgvragen of problemen zijn met de gevraagde gegevens, kan het nog meer tijd duren voordat deze vragen worden behandeld en de cyclus wordt voortgezet. Voor aan de gang zijnde analyse, exploratie en begrip van de klantenreis, is dit proces inefficiënt en niet scalable. Ook, richten de teams van BI typisch meer dan enkel klant op reis-gerelateerde vragen.

## CJA: Gegerichte workflow voor online- en offlinegegevens

CJA verstrekt een milieu om online en off-line dwars-kanaalgegevens op het overkoepelende klantenniveau met het enige doel te verbinden om de klantenreis te begrijpen. Er is een eerste setup nodig om verbinding te maken en weergaven te definiëren voor de gegevens die u als relevant aanmerkt. Zodra deze gegevens echter zijn voltooid, zijn ze gemakkelijk beschikbaar voor doorlopende analyse en exploratie, wat resulteert in het geleidelijk verkrijgen van inzicht in en inzicht in de reizen van de klant. Door gecombineerde online en off-line gegevens te democratiseren, kunt u klant op reis-gerelateerde vragen in seconden beantwoorden.

![CJA-workflow](./assets/cjaworkflow.png)

U kunt CJA gebruiken om vragen te stellen met behulp van de werkruimte voor visuele analyse en bijna onmiddellijk inzichten te verkrijgen. De gegevens en rapporten die via meerdere kanalen worden weergegeven, zijn direct beschikbaar, zonder dat SQL-code is vereist. Extra query&#39;s en analyse kunnen worden uitgevoerd met een eenvoudige sleepbewerking en neerzetbewerking in de gebruikersinterface, met volledig gecorreleerde gegevens. U kunt vragen blijven stellen, geleidelijk meer details onderzoeken zoals u vereist. U kunt dan onmiddellijk actie ondernemen op de inzichten die u ontdekt, zoals het delen van publiek voor activering en orkest.

## De krachtige rapporteringsengine van CJA

CJA gebruikt een krachtige merkgebonden architectuur die analyse over honderden of zelfs duizenden servers verspreidt om gegevens in Analysis Workspace binnen seconden te tonen. Enkele opmerkelijke eigenschappen van deze verwerkingsarchitectuur zijn:

* **Geoptimaliseerd voor individuele klant-gerelateerde vragen**: Technisch, slaat CJA de gegevens in een verdeelde rapporteringsmotor op die uitgebreid gebruik van caching maakt. Die motor wordt bepaald voor ontvankelijke vragen over individueel-vlakke gebeurtenisgegevens, en als dusdanig perfect geoptimaliseerd voor klant-gerelateerde vragen. De rapportengine slaat gegevens op in kolomgeoriënteerde bitmapindexen die een snelle berekening van geaggregeerde gegevens ter plekke mogelijk maken. Het heeft een uitgebreide het filtreren motor die krachtige segmentatie/publieksanalyse toelaat. En het heeft een kernbegrip van de opeenvolging onder gegevenspunten die nuttig is in het analyseren van gedrag over die gegevenspunten (de orde dat de dingen voorkwamen) en voor het toewijzen van attributie gebruikend diverse, complexe modellen.

* **Snelle toepassing van complexe paden en filters**: De rapportengine werkt op gedeeltelijk geordende, hiërarchische gegevenssets (bijvoorbeeld persoonlijk -> sessies -> gebeurtenissen). Alle gegevens voor een object op hoofdniveau (afzonderlijke profielen) bevinden zich op één verwerkingsknooppunt voor nauwkeurige resultaten. Dankzij deze partitionering kunnen complexe paden en filters snel worden toegepast. Complexe bewerkingen zoals sessionisatie, attributie, stateful persistentie van gegevenskenmerken en complexe opties voor gegevensmanipulatie worden op schaal met een snelle rapportagetijd uitgevoerd. In de wereld van BI, vereisen die soorten verrichtingen typisch nieuwe kubussen OLAP om voor elk gebruiksgeval worden gecreeerd. De het melden motor van CJA staat onbeperkte toegang tot de volledige dataset op elke vraag toe, resulterend in volledig gecorreleerde gegevens zonder het vereisen van om het even welk coderen van tevoren.

* **Efficiënte query op complexe gegevensstromen**: Één van de grootste verschillen van de rapporteringsmotor van traditionele SQL en gegevensbestanden NoSQL is zijn capaciteit om predikaten te bepalen die op opeenvolgingsgeoriënteerde verhoudingen op een fundamenteel niveau worden gebaseerd. Deze fundamentele zoekbewerkingen kunnen de recordstream bekijken, die bestaat uit vele interleaved (en zelfs geneste) reeksen. Zij voeren een vraag tegen elk van deze onderling verweven stromen van gegevens met de efficiency van één enkele, aangrenzende opeenvolgingsverrichting uit.

* **Ontworpen om grote vragen snel te beantwoorden**: De rapportageengine is niet zo algemeen bedoeld als traditionele grote gegevenssystemen. Het is echter specifiek ontworpen om query&#39;s te beantwoorden die miljoenen of zelfs miljarden records (gebeurtenisgegevens/ervaringsgebeurtenissen), doorgaans in minder dan een seconde, beslaan. In tegenstelling tot andere grote gegevenssystemen, doet het dit niet door de gegevens te bemonsteren of de antwoorden op alle vragen vooraf te berekenen die u zou kunnen stellen. In plaats daarvan kan het de antwoorden snel genoeg berekenen om interactieve vragen van gebruiksgevallen te steunen. Dit specifieke ontwerp van de CJA-rapporteringsengine maakt het gemakkelijker om gegevens snel en snel beschikbaar te maken voor doorlopende analyse en exploratie, zodat u geleidelijk inzicht kunt krijgen in en inzicht kunt krijgen in klantreizen.

* **Handelen als een oplossing zonder kop**: U definieert de afmetingen, metriek, filters op één locatie en vervolgens kan elke CJA-client (inclusief onze openbare CJA API) toegang krijgen tot deze componenten. Dit onttrekt complexe vragen weg van eind - gebruikers en waarborgt dat de resultaten het zelfde zijn, geen kwestie die rapporteert of visualisatieclient u gebruikt.

## De unieke visualisatiemogelijkheden van CJA

De rapporteringsmotor is fundamenteel voor CJA om u toe te staan om geleidelijk met alle gegevens van de klantenreis binnen die rapporteringsmotor in wisselwerking te staan en te handelen. CJA wordt geleverd met een uitgebreide set componenten die u in staat stellen dit visueel en via slepen en neerzetten te doen. Met BI-visualisatieprogramma&#39;s kunt u zoeken binnen de grenzen van SQL-voorbereide gegevens (zoals gedefinieerd door IT). Met CJA kunt u zo veel mogelijk splitsen en segmenteren, zonder dat u weer een SQL-weergave hoeft te maken.

&quot;Progressief&quot; is hier een sleutelbegrip: in tegenstelling tot de meeste visualisaties in de hulpmiddelen van BI, staat visuele belemmering-en-dalings UI in CJA u toe om onophoudelijk uw gegevens voor uw specifieke behoeften te breken: bouwen interactief vragen visueel gebruikend relevante metriek, dimensies, filters (segmenten), berekeningen, tijdlijnen, annotaties, en andere analysewaarden.

De volgende onderdelen van visualisatie zijn ingebouwd:

* **Functies van virtuele analisten** zoals [Anomaly Detection](/help/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) die voorspellende algoritmen en machinaal leren gebruiken om inzicht te krijgen in wat ongewoon gedrag in uw gegevens drijft.

* **Geavanceerde analysefuncties** die specifiek op de inzichten van de klantenreis gericht zijn, zoals [stroomdiagrammen](/help/analysis-workspace/visualizations/c-flow/flow.md), [toewijzing-IQ](/help/analysis-workspace/attribution/overview.md), [herfstschema&#39;s](/help/analysis-workspace/visualizations/fallout/fallout-flow.md), en [uitsplitsingen naar dimensie](/help/components/dimensions/t-breakdown-fa.md). Voorbeelden van out-of-the-box-visualisaties zijn:

   * [Analyse van het behoud van klanten via cohort-/latentietabellen](/help/analysis-workspace/visualizations/cohort-table/cohort-use-cases.md), waar u eenvoudig metriek/afmetingen sleept en neerzet in een bouwer en u wordt gedaan in minder dan 30 seconden,

   * [Fallout](/help/analysis-workspace/visualizations/fallout/configuring-fallout.md) / [stroom](/help/analysis-workspace/visualizations/c-flow/create-flow.md) visualisaties. binnen een minuut

   * [Attributiemodellen](/help/analysis-workspace/attribution/algorithmic.md) zoals eerste aanraking, laatste aanraking, deelname, tijdverlies, zelfs aangepaste, die een paar klikken aan opstelling nemen,

* **Segmenteringsmogelijkheden in elke stap van uw progressieve exploratie**: wanneer u denkt het steek houdt, kunt u uw publiek terug in Experience Platform en van daar aan om het even welke gesteunde bestemmingen publiceren;

* **Sessionering** dat is volledig [aanpasbaar](/help/data-views/component-settings/persistence.md): u bepaalt wanneer een zitting, als deel van een kanaal in een klantenreis, begint en beëindigt.

* **Cursus en democratisering**: De dashboards die in CJA worden gecreeerd kunnen zijn:

   * [Gekromd](/help/analysis-workspace/curate-share/curate.md) aan andere personen in de organisatie voor doorlopende exploratie;
   * Geëxporteerd naar Excel met [Report Builder](/help/report-builder/report-buider-overview.md) (een specifieke insteekmodule),
   * [Gedeeld](/help/analysis-workspace/curate-share/share-projects.md) in verschillende vormen, waaronder [PDF](/help/analysis-workspace/curate-share/download-send.md), [CSV](/help/analysis-workspace/curate-share/download-send.md) en via een [speciale mobiele app](/help/mobile-app/home.md), aan degenen die geïnteresseerd zijn in de eindverslagen en/of visualisaties.

Het vergelijken van de visualisatiemogelijkheden van CJA met welke hulpmiddelen van BI is moeilijk wegens de verscheidenheid van beschikbare visualisaties. Sommige hulpmiddelen van BI hebben geavanceerdere visualisaties, maar CJA concentreert zich op interactieve en interoperabele de reisvisualisaties van de klant die u toestaan om de gegevens binnen seconden te breken terwijl niet het &quot;in rekening brengen&quot;u voor elke extra vraag.


## Samenvatting

CJA verschilt van de hulpmiddelen van BI in hoe het een hoogst geoptimaliseerde klant-reis-geconcentreerde rapporteringsmotor naadloos met gebruikersvriendelijke hulpmiddelen en componenten integreert om analyses uit te voeren en rapporten en geavanceerde visualisaties te bouwen. Allemaal vanuit één interface, zonder dat u als gebruiker heen en weer moet schakelen tussen de query-engine en de visualisatieomgeving.

