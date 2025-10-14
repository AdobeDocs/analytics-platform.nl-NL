---
title: Overzicht van geleide analyse
description: Een methode voor het analyseren van gegevens in Customer Journey Analytics waarmee productteams snel inzichten van hoge kwaliteit kunnen krijgen.
keywords: productanalyse
exl-id: 1ac8157f-87e8-4d98-a2ca-f6beb68d9d6b
feature: Guided Analysis
role: User
source-git-commit: 38be838fccf896a12da3fbadac50e578081312ba
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---

# Overzicht van geleide analyse

Met een analyse met instructies kunnen gebruikers, van marketing tot product tot analisten, zelf hoogwaardige gegevens en inzichten bedienen over de reis van klanten door geleide workflows, gebaseerd op de kanaalgegevens van Customer Journey Analytics. Gelijkaardig aan Analysis Workspace en Mobiele scorecards, Geleide analyse gebruikt gegevens van de mening van a [&#x200B; Gegevens &#x200B;](/help/data-views/data-views.md), die verwijzingen gegevens in Adobe Experience Platform door a [&#x200B; Verbinding &#x200B;](../connections/overview.md). Veel rapporten die zijn gemaakt in de analyse met instructies kunnen naadloos worden overgedragen naar Analysis Workspace voor aanvullend onderzoek.

De volgende analyses met instructies zijn beschikbaar:

| Pictogram | Analyse | Beschrijving |
| :----:|--- | --- |
| ![&#x200B; PeopleGroup &#x200B;](/help/assets/icons/PeopleGroup.svg) | [&#x200B; Actieve groei &#x200B;](types/active-growth.md) | Identificeer wie nieuw, behouden, terugkeren, of slapend is. |
| ![&#x200B; ConversionTrens &#x200B;](/help/assets/icons/ConversionTrends.svg) | [&#x200B; trends van de Omzetting &#x200B;](types/conversion-trends.md) | Wijzigingen in conversietarieven bijhouden in de loop van de tijd. |
| ![&#x200B; EngagementGraph &#x200B;](/help/assets/icons/EngagementGraph.svg) | [Engagement](types/engagement.md) | Begrijp de breedte en diepte van eigenschapbetrokkenheid. |
| ![&#x200B; FirstUse &#x200B;](/help/assets/icons/FirstUse.svg) | [&#x200B; Eerste gebruikeffect &#x200B;](types/first-use-impact.md) | Meet het effect van het gebruik van de eerste functie op sleutelindicatoren. |
| ![Histogram](/help/assets/icons/Histogram.svg) | [&#x200B; Frequentie &#x200B;](types/frequency.md) | Meet de betrokkenheid per gebruiksfrequentie. |
| ![&#x200B; ConversionFunnel &#x200B;](/help/assets/icons/ConversionFunnel.svg) | [&#x200B; Trechter &#x200B;](types/funnel.md) | Vergelijk de conversiesnelheden tussen de stappen. |
| ![&#x200B; NetGrowth &#x200B;](/help/assets/icons/NetGrowth.svg) | [&#x200B; Netto groei &#x200B;](types/net-growth.md) | Wint of verliest u gebruikers? |
| ![&#x200B; Versie &#x200B;](/help/assets/icons/Release.svg) | [&#x200B; effect van de Versie &#x200B;](types/release-impact.md) | Vergelijk de prestaties in gelijke perioden vóór en na de release. |
| ![&#x200B; Behoud &#x200B;](/help/assets/icons/Retention.svg) | [&#x200B; Behoud &#x200B;](types/retention.md) | Meet de doorlopende retourgewoonten van uw gebruikers. |
| ![&#x200B; Chronologie &#x200B;](/help/assets/icons/Timeline.svg) | [&#x200B; Chronologie &#x200B;](types/timeline.md) | Verken patronen in sessieactiviteiten. |
| ![&#x200B; GraphTrend &#x200B;](/help/assets/icons/GraphTrend.svg) | [&#x200B; Trends &#x200B;](types/trends.md) | Meet de betrokkenheid van de gebruiker in de loop van de tijd. |



## Toegang

Via de Customer Journey Analytics-startpagina hebt u toegang tot de analyse met instructies.

1. Selecteer **[!UICONTROL Guided analysis]** van de homepage, die u rechtstreeks aan de [&#x200B; analyse van Trends &#x200B;](types/trends.md) neemt.

   ![&#x200B; het Bestaan paginatielijn &#x200B;](assets/landing-page-tile.png){style="border:1px solid gray"}

1. Selecteer **[!UICONTROL Create new]** om de verschillende weergaveopties weer te geven en een ander beginpunt voor de analyse te kiezen.

   ![&#x200B; creeer een nieuw modaal &#x200B;](assets/create-new-modal.png){style="border:1px solid gray"}

U kunt ook de analyse met instructies openen vanuit een Analysis Workspace-project.

1. Selecteer **[!UICONTROL Blank project]** op de startpagina om een leeg Workspace-project te maken.

   ![&#x200B; creeer leeg project &#x200B;](assets/blank-project.png){style="border:1px solid gray"}

1. Selecteer ![&#x200B; Geleide analyse &#x200B;](/help/assets/icons/GuidedAnalysis.svg) **[!UICONTROL Guided Analysis]** in het linkerspoor.

   ![&#x200B; Workspace linkerspoor &#x200B;](assets/workspace-left-rail.png){style="border:1px solid gray"}

1. Sleep een nieuwe analyse naar het Workspace-canvas en selecteer vervolgens **[!UICONTROL Create]** om de gewenste analyse te genereren (bijvoorbeeld: **[!UICONTROL Create Trends]** ). U kunt ook een bestaande analyse naar het Workspace-canvas slepen vanuit de sectie **[!UICONTROL Saved]** .

   ![&#x200B; creeer paneel &#x200B;](assets/create-guided-analysis-panel.gif)

## Interface

De interface voor Analyse met instructies volgt een vraag- en antwoordindeling. Vorm uw vraag in vraagspoor, dan krijg een antwoord met geschreven insight, grafiek, en lijst. Vervolgens kunt u de volgende vraag stellen met analyses en visualisatie-instellingen.

De geleide analyse gebruikt de volgende elementen UI:

| Interfacevoorvertoning | UI-element | Beschrijving |
| --- | --- | --- |
| ![&#x200B; spoorweg van de Vraag &#x200B;](assets/query-rail.png){style="border:1px solid gray"} | **[!UICONTROL Query rail]** | Vorm uw *vraag* door de gewenste componenten (gebeurtenissen, eigenschappen, en segmenten) te selecteren die omhoog een analyse maken. De volgende opties zijn beschikbaar voor alle analyses, met extra instellingen per weergave. <ul><li>**Mening**: Selecteer van de opties om aan een nieuwe analyse over te schakelen. Uw vraagselecties worden gehandhaafd binnen de toegestane grenzen voor de nieuwe analyse.</li><li>**Gebeurtenissen**: De gebeurtenissen die u wilt meten. Elke analyse dwingt verschillende grenzen aan het aantal gebeurtenissen af die u kunt vormen.  Gebeurtenissen krijgen soms het label **[!UICONTROL Start and return events]**, **[!UICONTROL Steps]** of **[!UICONTROL Key indicators]** . De gebeurtenissen worden geïdentificeerd in de analyse gebruikend 1, 2,.. <br/> Uitgezochte ![&#x200B; &#x200B;](/help/assets/icons/Add.svg) **[!UICONTROL Add an event]** om nieuwe gebeurtenissen toe te voegen.</li><li>**[!UICONTROL Factors]**: Indien beschikbaar kunt u factoren opgeven, zoals de datum sinds en de eerste keer dat de gebeurtenis plaatsvindt.</li><li>**die als** wordt geteld: De tellende methode die u op de geselecteerde gebeurtenissen wilt toepassen. Selecteer een optie in het keuzemenu.</li><li>**Segmenten**: De segmenten die u wilt meten. Elke analyse dwingt verschillende grenzen aan het aantal segmenten af die u kunt vormen. De segmenten worden geïdentificeerd in de analyse gebruikend A, B,.. <br/> Uitgezochte ![&#x200B; &#x200B;](/help/assets/icons/Add.svg) **[!UICONTROL Add a segment]** om nieuwe segmenten toe te voegen.</li><li>**[!UICONTROL Breakdown]**: Indien beschikbaar, de uitsplitsing die u wilt toepassen op de analyse.</li></ul>Op sommige van de montages, is de extra configuratie beschikbaar.<ul><li>**Filters**: De Filter van het gebruik ![&#x200B; &#x200B;](assets/filter.png) om gebeurtenissen of segmenten door specifieke afmetingen te versmallen. Wanneer een afmeting is geselecteerd, zijn zowel de standaardfiltercriteria (zoals **[!UICONTROL Equals]** , **[!UICONTROL Contains]** of **[!UICONTROL Ends with]** ) als de bovenste 1000-afmetingswaarden beschikbaar.<br/> Uitgezochte ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) om extra filters toe te voegen.<br/> Uitgezochte ![&#x200B; verwijder &#x200B;](/help/assets/icons/Remove.svg) om een filter te verwijderen.</li><li>**Meer acties**: Gebruik ![&#x200B; meer &#x200B;](/help/assets/icons/More.svg) om acties, als<ul><li>![&#x200B; noem &#x200B;](/help/assets/icons/Rename.svg) anders **[!UICONTROL Rename]**: om een gebeurtenis of een segment anders te noemen.</li><li>![&#x200B; Dupliceer &#x200B;](/help/assets/icons/Duplicate.svg) **[!UICONTROL Duplicate]**: om een gebeurtenis of een segment te dupliceren.</li><li>![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) **[!UICONTROL Remove]**: om een gebeurtenis, een segment of een mislukking te verwijderen.</li><li>![&#x200B; geef segment &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit segment]** uit: om een segment in de [&#x200B; bouwer van het Segment &#x200B;](/help/components/segments/seg-builder.md) uit te geven.</li><li>![&#x200B; Ster &#x200B;](/help/assets/icons/Star.svg) **[!UICONTROL Add to favorites]**: om het segment aan de lijst van favoriete segmenten in de [&#x200B; manager van het Segment &#x200B;](/help/components/segments/seg-manage.md) toe te voegen.</li><li>![&#x200B; SaveAsFloppy &#x200B;](/help/assets/icons/SaveAsFloppy.svg) **[!UICONTROL Save as]**: om het segment als nieuwe component te bewaren. In het dialoogvenster **[!UICONTROL Save segments to components]** kunt u een segmentnaam en een beschrijving opgeven. U kunt ![&#x200B; StarOutline &#x200B;](/help/assets/icons/StarOutline.svg) selecteren om het nieuwe segment als favoriet te merken. Selecteer **[!UICONTROL Save]** om het segment op te slaan als een nieuw segment.</li><li>![&#x200B; Verbinding &#x200B;](/help/assets/icons/Link.svg) **[!UICONTROL Link start and return events]**.: om begin te verbinden en gebeurtenissen in a [&#x200B; Behoud &#x200B;](types/retention.md) analyse terug te keren.</li><li>![&#x200B; ontkoppelen &#x200B;](/help/assets/icons/Unlink.svg) **[!UICONTROL Unlink start and return events]**: om begin en terugkeergebeurtenissen in a [&#x200B; Behoud &#x200B;](types/retention.md) analyse los te maken.</li></ul></li></ul> |
| ![&#x200B; Grafiek &#x200B;](assets/chart.png){style="border:1px solid gray"} | **[!UICONTROL Chart]** | Een visualisatie van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Welke visualisatie u ziet hangt van de mening en de montages boven de grafiek af. Het diagram bevat ook: <ul><li>**Knopinfo**: Beweeg over om het even welk punt van grafiekgegevens om tooltip met meer informatie bloot te stellen.</li><li>**Legend**: Beweeg over de reeks van de grafieklegenda om definities te bekijken waar beschikbaar, nadruk op die reeks, en tijdelijk andere reeksen te verbergen. Selecteer een reeks in de legenda om de reeks te verbergen.</li><li>**Annotaties**: Toepasselijke [&#x200B; annotaties &#x200B;](../components/annotations/overview.md) zijn zichtbaar tussen de visualisatie en de legenda. Het wordt getoond als pictogram van de a ![&#x200B; Annotatie &#x200B;](assets/annotation.png) in de gevormde kleur van de annotatie. Analyseert die gegevens in tijd tonen plaats het ![&#x200B; pictogram van de Annotatie &#x200B;](assets/annotation.png) onder de gevormde datum of datumwaaier. Analyseert die geen gegevens in tijd tonen tonen toont het ![&#x200B; pictogram van de Annotatie &#x200B;](assets/annotation.png) in de lagere juiste hoek van de grafiek.</li><li>**Uitgezochte acties**: Maak de volgende beschikbare acties bloot door om het even welk gegevenspunt te selecteren. De opties omvatten **sparen segment**.</li></ul> |
| ![&#x200B; Lijst &#x200B;](assets/table.png){style="border:1px solid gray"} | **[!UICONTROL Table]** | Een tabelweergave van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Rijen in de tabel die ter referentie gebeurtenis (1, 2, ...) en segment-id&#39;s (A, B, ...) gebruiken. De kolommen in de tabel zijn afhankelijk van de analyse boven het diagram. De tabel bevat ook voor elke rij: <ul><li>**Uitgezochte acties**: Wissel ![&#x200B; tonen verborgen pictogram &#x200B;](assets/hide-in-chart.png) om een grafiekreeks voor een rij te verbergen of bloot te stellen. Selecteer ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) voor extra acties. De opties omvatten **sparen segment**.</li></ul> |
| ![&#x200B; Visualisatie montages &#x200B;](assets/visualization-settings.png){style="border:1px solid gray"} | **[!UICONTROL Visualization settings]** | Opties boven het diagram waarmee u de volgende vraag kunt stellen en aanpassen hoe het diagram en de tabel worden geretourneerd. De volgende opties zijn beschikbaar voor alle analyses, met extra instellingen per analyse. <ul><li>![&#x200B; GraphTrend &#x200B;](/help/assets/icons/GraphTrend.svg) **de montages van de Grafiek**: Beoordeel wat uw grafiek en lijstvertoning. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.</li><li>![&#x200B; Laag &#x200B;](/help/assets/icons/Layer.svg) **de montages van de Bedekking**: Voeg een bedekking toe. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.</li><li>![&#x200B; Emmertje &#x200B;](/help/assets/icons/Bucket.svg) **[!UICONTROL Bucket settings]**: Auto emmertje of pas de montages van de douaneemmer op de gegevens toe. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.<li>![&#x200B; DataCorrelated &#x200B;](/help/assets/icons/DataCorrelated.svg) **[!UICONTROL Compare settings]**: Vergelijk gegevens met een specifieke datumwaaier. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.</li><li>![&#x200B; Voetstappen &#x200B;](/help/assets/icons/Footsteps.svg) **[!UICONTROL Display settings]**: Selecteer hoe te om de gegevens te tonen. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.<li>![&#x200B; Kalender &#x200B;](/help/assets/icons/Calendar.svg) **waaier van de Datum**: Een kalenderplukker die u toestaat om de datumwaaier van de analyse te bepalen. U kunt ook een interval selecteren voor uitgevoerde analyses, zoals dagelijks, wekelijks of maandelijks.</li><li>![&#x200B; LightBulb &#x200B;](/help/assets/icons/LightBulb.svg) **Inzichten**: Contextuele inzichten afhankelijk van de analyse die u bekijkt. Deze inzichten geven opmerkingen voor de huidige analyse. Als er meerdere inzichten beschikbaar zijn, kunt u deze weergeven met de pijlen aan de rechterkant. U kunt de zichtbaarheid van dit vak in- en uitschakelen met het gloeilamppictogram rechtsboven.</li></ul> |
| ![&#x200B; pictogram van het Menu &#x200B;](assets/menu.png){style="border:1px solid gray"} | **[!UICONTROL Menu]**<br/>Beschikbaar in een project van de Geleide analyse | Opdrachten in de rechterbovenhoek van een analyseproject met instructies die overkoepelende acties voor uw analyse bieden.<ul><li>![&#x200B; het pictogram van Gegevens &#x200B;](/help/assets/icons/Data.svg) ***Naam van gegevensmening***: Verander de gegevensmening die de analyse gebruikt. Wanneer u de gegevensmening verandert, veranderen de beschikbare componenten in vraagspoor ook.</li><li>![&#x200B; het pictogram van de Verbinding &#x200B;](/help/assets/icons/Link.svg) **verbinding van het Exemplaar**: Kopieert een verbinding aan de analyse aan uw klembord. U wordt gevraagd op te slaan voordat u gaat delen.</li><li>**Aandeel**: Opent het delen modaal, met verdere opties voor het delen aan individuele gebruikers of groepen. U kunt een analyse met andere gebruikers delen, of een verbinding produceren om met iedereen te delen.</li><li>**sparen**: Slaat de analyse op. Als u een nieuwe analyse opslaat, wordt het dialoogvenster **[!UICONTROL Save analysis]** weergegeven waarin u een naam en beschrijving kunt opgeven. Nadat u een **[!UICONTROL Analysis saved]** -dialoogvenster hebt opgeslagen, kunt u uw analyse delen.</li><li>![&#x200B; voeg aan het pictogram van Workspace toe &#x200B;](/help/assets/icons/MultipleAdd.svg) **[!UICONTROL Add to Workspace]**: toont beschikbare projecten van Workspace die u deze analyse kunt toevoegen aan. Als u een Workspace-project selecteert, wordt dat Workspace-project op een nieuw tabblad geopend en wordt de analyse onder aan het project toegevoegd.</li></ul>Selecteer ![&#x200B; Meer pictogram &#x200B;](/help/assets/icons/More.svg) voor meer acties, als:<ul><li>**[!UICONTROL Save as]**: slaat de analyse los van de huidige analyse op en maakt een kopie. Er wordt een dialoogvenster weergegeven waarin u een nieuwe naam en beschrijving kunt opgeven.</li><li>**[!UICONTROL Export to Workspace]**: maakt de huidige query voor analyse met instructies in Analysis Workspace opnieuw. Het Workspace-project wordt op een nieuw tabblad gemaakt, zodat onderbreking wordt voorkomen tijdens het werken in de analyse met instructies. Het is een kopie van de analyse en blijft na opening niet synchroon met de oorspronkelijke analyse. Gebruik dit bevel wanneer u aan uw analyst team wilt afleveren, of dieper in de gegevens duiken dan wat de analyse toestaat.</li><li>**[!UICONTROL Copy chart to clipboard]**: kopieert de diagramafbeelding naar het klembord, zodat deze in andere toepassingen kan worden geplakt. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**[!UICONTROL Download PNG]** : hiermee downloadt u de diagramafbeelding als een `.png` . De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**[!UICONTROL Download CSV]** : downloadt de tabelgegevens als een `.csv` . De queryrail en -grafiek worden niet in het bestand opgenomen.</li></ul> |
| ![&#x200B; visualisatie van het Menu &#x200B;](assets/menu-visualization.png){style="border:1px solid gray"} | **<br/>Beschikbaar 1&rbrace; Menu in een Geleide analyse visualisatie in de werkruimte van de Analyse.** | Opdrachten in een Begeleide analyse visualisatie in de werkruimte van de Analyse.<ul><li>![&#x200B; GraphScatter &#x200B;](/help/assets/icons/GraphScatter.svg) **[!UICONTROL Chart]**: om slechts de grafiek van de analyse te tonen.</li><li>![&#x200B; Lijst &#x200B;](/help/assets/icons/Table.svg) **[!UICONTROL Table]**: om slechts de lijst van de analyse te tonen.</li><li>![&#x200B; TableAndChart &#x200B;](/help/assets/icons/TableAndChart.svg) **[!UICONTROL All]**: om grafiek en lijst van de analyse te tonen.</li><li>![&#x200B; geef &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** uit: om de configuratie van de analyse uit te geven</li><li>![&#x200B; Kalender &#x200B;](/help/assets/icons/Calendar.svg) **[!UICONTROL *waaier van de Datum *]**: om de datumwaaier voor de analyse te vormen.</li></ul> |


## Inrichting

Analyses met instructies worden als volgt in Customer Journey Analytics-pakketten opgenomen:

| Pakket | Beschikbare analyses |
| --- | --- |
| [!UICONTROL Customer Journey Analytics add-ons] | Actieve groei, Conversietrends, Frequentie, Trechter, Netto groei, Behoud, Trends |
| [!UICONTROL Customer Journey Analytics Foundation] | Trends |
| [!UICONTROL Customer Journey Analytics Select] | De meningen van de stichting + Actieve groei, de tendensen van de Omzetting, Frequentie, Trechter, Netto groei, Behoud |
| [!UICONTROL Customer Journey Analytics Prime] | Weergaven selecteren + Betrokkenheid, impact eerste gebruik, impact release, tijdlijn |
| [!UICONTROL Customer Journey Analytics Ultimate] | Prime-weergaven |

{style="table-layout:auto"}

Beheerders van productprofielen kunnen toegang tot de analyse met instructies in de Adobe Admin Console toevoegen of verwijderen.

1. Login aan [&#x200B; Adobe Admin Console &#x200B;](https://adminconsole.adobe.com).
1. Selecteer **[!UICONTROL Customer Journey Analytics]** in de lijst met producten.
1. Selecteer het gewenste productprofiel voor de machtigingen die u wilt bewerken.
1. Selecteer de tab **[!UICONTROL Permissions]** en klik vervolgens op **[!UICONTROL Edit]** onder [!UICONTROL Reporting Tools] .
1. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) naast **[!UICONTROL Guided Analysis Access]** in de lijst van [!UICONTROL Available Permission Items], die het aan de lijst van [!UICONTROL Included Permission Items] toevoegt.
1. Selecteer **[!UICONTROL Save]** .

Zie [&#x200B; het niveautoegang van de Gebruiker &#x200B;](/help/technotes/access-control.md#user-level-access) voor meer informatie.

>[!TIP]
>
>Sommige beheerders schakelen de functie Analyse met instructies liever in en schakelen Analysis Workspace voor nieuwe gebruikers uit naar Customer Journey Analytics. Als deze gebruikers klaar zijn met het product en uw organisatorische gegevens, kunt u vervolgens toegang tot Analysis Workspace inschakelen.
