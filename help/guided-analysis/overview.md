---
title: Overzicht van geleide analyse
description: Een methode om gegevens in Customer Journey Analytics te analyseren die productteams snel inzichten van hoge kwaliteit laat krijgen.
keywords: productanalyse
exl-id: 1ac8157f-87e8-4d98-a2ca-f6beb68d9d6b
feature: Guided Analysis
role: User
source-git-commit: dbcc66e02f729547fcb129fe157af831ed6369f9
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---

# Overzicht van geleide analyse

Met een analyse met instructies kunnen gebruikers, van marketing tot product tot analisten, zelf hoogwaardige gegevens en inzichten bedienen over de reis van de klant via geleide workflows, gebaseerd op de kanaalgegevens van de Customer Journey Analytics. Gelijkaardig aan Analysis Workspace en Mobiele scorecards, Geleide analyse gebruikt gegevens van de mening van a [ Gegevens ](/help/data-views/data-views.md), die verwijzingen gegevens in Adobe Experience Platform door a [ Verbinding ](../connections/overview.md). Veel rapporten die zijn gemaakt in de analyse met instructies kunnen naadloos worden overgedragen naar Analysis Workspace voor aanvullend onderzoek.

De volgende analyses met instructies zijn beschikbaar:

| Pictogram | Analyse | Beschrijving |
| :----:|--- | --- |
| ![ PeopleGroup ](/help/assets/icons/PeopleGroup.svg) | [ Actieve groei ](types/active-growth.md) | Identificeer wie nieuw, behouden, terugkeren, of slapend is. |
| ![ ConversionTrens ](/help/assets/icons/ConversionTrends.svg) | [ trends van de Omzetting ](types/conversion-trends.md) | Wijzigingen in conversietarieven bijhouden in de loop van de tijd. |
| ![ EngagementGraph ](/help/assets/icons/EngagementGraph.svg) | [Engagement](types/engagement.md) | Begrijp de breedte en diepte van eigenschapbetrokkenheid. |
| ![ FirstUse ](/help/assets/icons/FirstUse.svg) | [ Eerste gebruikeffect ](types/first-use-impact.md) | Meet het effect van het gebruik van de eerste functie op sleutelindicatoren. |
| ![Histogram](/help/assets/icons/Histogram.svg) | [ Frequentie ](types/frequency.md) | Meet de betrokkenheid per gebruiksfrequentie. |
| ![ ConversionFunnel ](/help/assets/icons/ConversionFunnel.svg) | [ Trechter ](types/funnel.md) | Vergelijk de conversiesnelheden tussen de stappen. |
| ![ NetGrowth ](/help/assets/icons/NetGrowth.svg) | [ Netto groei ](types/net-growth.md) | Wint of verliest u gebruikers? |
| ![ Versie ](/help/assets/icons/Release.svg) | [ effect van de Versie ](types/release-impact.md) | Vergelijk de prestaties in gelijke perioden vóór en na de release. |
| ![ Behoud ](/help/assets/icons/Retention.svg) | [ Behoud ](types/retention.md) | Meet de doorlopende retourgewoonten van uw gebruikers. |
| ![ Chronologie ](/help/assets/icons/Timeline.svg) | [ Chronologie ](types/timeline.md) | Verken patronen in sessieactiviteiten. |
| ![ GraphTrend ](/help/assets/icons/GraphTrend.svg) | [ Trends ](types/trends.md) | Meet de betrokkenheid van de gebruiker in de loop van de tijd. |



## Toegang

U hebt toegang tot de analyse met instructies op de startpagina van de Customer Journey Analytics.

1. Selecteer **[!UICONTROL Guided analysis]** van de homepage, die u rechtstreeks aan de [ analyse van Trends ](types/trends.md) neemt.

   ![ het Bestaan paginatielijn ](assets/landing-page-tile.png){style="border:1px solid gray"}

1. Selecteer **[!UICONTROL Create new]** om de verschillende weergaveopties weer te geven en een ander beginpunt voor de analyse te kiezen.

   ![ creeer een nieuw modaal ](assets/create-new-modal.png){style="border:1px solid gray"}

U kunt ook de analyse met instructies openen vanuit een Analysis Workspace-project.

1. Selecteer **[!UICONTROL Blank project]** op de startpagina om een leeg Workspace-project te maken.

   ![ creeer leeg project ](assets/blank-project.png){style="border:1px solid gray"}

1. Selecteer ![ Geleide analyse ](/help/assets/icons/GuidedAnalysis.svg) **[!UICONTROL Guided Analysis]** in het linkerspoor.

   ![ Workspace linkerspoor ](assets/workspace-left-rail.png){style="border:1px solid gray"}

1. Sleep een nieuwe analyse naar het Workspace-canvas en selecteer vervolgens **[!UICONTROL Create]** om de gewenste analyse te genereren (bijvoorbeeld: **[!UICONTROL Create Trends]** ). U kunt ook een bestaande analyse naar het Workspace-canvas slepen vanuit de sectie **[!UICONTROL Saved]** .

   ![ creeer paneel ](assets/create-guided-analysis-panel.gif)

## Interface

De interface voor Analyse met instructies volgt een vraag- en antwoordindeling. Vorm uw vraag in vraagspoor, dan krijg een antwoord met een geschreven inzicht, grafiek, en lijst. Vervolgens kunt u de volgende vraag stellen met analyses en visualisatie-instellingen.

De geleide analyse gebruikt de volgende elementen UI:

| Interfacevoorvertoning | UI-element | Beschrijving |
| --- | --- | --- |
| ![ spoorweg van de Vraag ](assets/query-rail.png){style="border:1px solid gray"} | **[!UICONTROL Query rail]** | Vorm uw *vraag* door de gewenste componenten (gebeurtenissen, eigenschappen, en segmenten) te selecteren die omhoog een analyse maken. De volgende opties zijn beschikbaar voor alle analyses, met extra instellingen per weergave. <ul><li>**Mening**: Selecteer van de opties om aan een nieuwe analyse over te schakelen. Uw vraagselecties worden gehandhaafd binnen de toegestane grenzen voor de nieuwe analyse.</li><li>**Gebeurtenissen**: De gebeurtenissen die u wilt meten. Elke analyse dwingt verschillende grenzen aan het aantal gebeurtenissen af die u kunt vormen.  Gebeurtenissen krijgen soms het label **[!UICONTROL Start and return events]**, **[!UICONTROL Steps]** of **[!UICONTROL Key indicators]** . De gebeurtenissen worden geïdentificeerd in de analyse gebruikend 1, 2,.. <br/> Uitgezochte ![ ](/help/assets/icons/Add.svg) **[!UICONTROL Add an event]** om nieuwe gebeurtenissen toe te voegen.</li><li>**[!UICONTROL Factors]**: Indien beschikbaar kunt u factoren opgeven, zoals de datum sinds en de eerste keer dat de gebeurtenis plaatsvindt.</li><li>**die als** wordt geteld: De tellende methode die u op de geselecteerde gebeurtenissen wilt toepassen. Selecteer een optie in het vervolgkeuzemenu.</li><li>**Segmenten**: De segmenten die u wilt meten. Elke analyse dwingt verschillende grenzen aan het aantal segmenten af die u kunt vormen. De segmenten worden geïdentificeerd in de analyse gebruikend A, B,.. <br/> Uitgezochte ![ ](/help/assets/icons/Add.svg) **[!UICONTROL Add a segment]** om nieuwe segmenten toe te voegen.</li><li>**[!UICONTROL Breakdown]**: Indien beschikbaar, de uitsplitsing die u wilt toepassen op de analyse.</li></ul>Op sommige van de montages, is de extra configuratie beschikbaar.<ul><li>**Filters**: De Filter van het gebruik ![ ](assets/filter.png) om gebeurtenissen of segmenten door specifieke afmetingen te versmallen. Wanneer een afmeting is geselecteerd, zijn zowel de standaardfiltercriteria (zoals **[!UICONTROL Equals]** , **[!UICONTROL Contains]** of **[!UICONTROL Ends with]** ) als de bovenste 1000-afmetingswaarden beschikbaar.<br/> Uitgezochte ![ Filter ](/help/assets/icons/Filter.svg) om extra filters toe te voegen.<br/> Uitgezochte ![ verwijder ](/help/assets/icons/Remove.svg) om een filter te verwijderen.</li><li>**Meer acties**: Gebruik ![ meer ](/help/assets/icons/More.svg) om acties, als<ul><li>![ noem ](/help/assets/icons/Rename.svg) anders **[!UICONTROL Rename]**: om een gebeurtenis of een segment anders te noemen.</li><li>![ Dupliceer ](/help/assets/icons/Duplicate.svg) **[!UICONTROL Duplicate]**: om een gebeurtenis of een segment te dupliceren.</li><li>![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Remove]**: om een gebeurtenis, een segment of een mislukking te verwijderen.</li><li>![ geef segment ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit segment]** uit: om een segment in de [ bouwer van de Filter uit te geven ](/help/components/filters/filter-builder.md).</li><li>![ Ster ](/help/assets/icons/Star.svg) **[!UICONTROL Add to favorites]**: om het segment aan de lijst van favoriete filters in de [ manager van de Filter ](/help/components/filters/manage-filters.md) toe te voegen.</li><li>![ SaveAsFloppy ](/help/assets/icons/SaveAsFloppy.svg) **[!UICONTROL Save as]**: om het segment als nieuwe component te bewaren. In het dialoogvenster **[!UICONTROL Save segments to components]** kunt u een segmentnaam en een beschrijving opgeven. U kunt ![ StarOutline ](/help/assets/icons/StarOutline.svg) selecteren om het nieuwe segment als favoriet te merken. Selecteer **[!UICONTROL Save]** om het segment op te slaan als een nieuw filter.</li><li>![ Verbinding ](/help/assets/icons/Link.svg) **[!UICONTROL Link start and return events]**.: om begin te verbinden en gebeurtenissen in a [ Behoud ](types/retention.md) analyse terug te keren.</li><li>![ ontkoppelen ](/help/assets/icons/Unlink.svg) **[!UICONTROL Unlink start and return events]**: om begin en terugkeergebeurtenissen in a [ Behoud ](types/retention.md) analyse los te maken.</li></ul></li></ul> |
| ![ Grafiek ](assets/chart.png){style="border:1px solid gray"} | **[!UICONTROL Chart]** | Een visualisatie van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Welke visualisatie u ziet hangt van de mening en de montages boven de grafiek af. Het diagram bevat ook: <ul><li>**Knopinfo**: Beweeg over om het even welk punt van grafiekgegevens om tooltip met meer informatie bloot te stellen.</li><li>**Legend**: Beweeg over de reeks van de grafieklegenda om definities te bekijken waar beschikbaar, nadruk op die reeks, en tijdelijk andere reeksen te verbergen. Selecteer een reeks in de legenda om de reeks te verbergen.</li><li>**Annotaties**: Toepasselijke [ annotaties ](../components/annotations/overview.md) zijn zichtbaar tussen de visualisatie en de legenda. Het wordt getoond als pictogram van de a ![ Annotatie ](assets/annotation.png) in de gevormde kleur van de annotatie. Analyseert die gegevens in tijd tonen plaats het ![ pictogram van de Annotatie ](assets/annotation.png) onder de gevormde datum of datumwaaier. Analyseert die geen gegevens in tijd tonen tonen toont het ![ pictogram van de Annotatie ](assets/annotation.png) in de lagere juiste hoek van de grafiek.</li><li>**Uitgezochte acties**: Maak de volgende beschikbare acties bloot door om het even welk gegevenspunt te selecteren. De opties omvatten **sparen segment**.</li></ul> |
| ![ Lijst ](assets/table.png){style="border:1px solid gray"} | **[!UICONTROL Table]** | Een tabelweergave van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Rijen in de tabel die ter referentie gebeurtenis (1, 2, ...) en segment-id&#39;s (A, B, ...) gebruiken. De kolommen in de tabel zijn afhankelijk van de analyse boven het diagram. De tabel bevat ook voor elke rij: <ul><li>**Uitgezochte acties**: Wissel ![ tonen verborgen pictogram ](assets/hide-in-chart.png) om een grafiekreeks voor een rij te verbergen of bloot te stellen. Selecteer ![ Meer ](/help/assets/icons/More.svg) voor extra acties. De opties omvatten **sparen segment**.</li></ul> |
| ![ Visualisatie montages ](assets/visualization-settings.png){style="border:1px solid gray"} | **[!UICONTROL Visualization settings]** | Opties boven het diagram waarmee u de volgende vraag kunt stellen en aanpassen hoe het diagram en de tabel worden geretourneerd. De volgende opties zijn beschikbaar voor alle analyses, met extra instellingen per analyse. <ul><li>![ GraphTrend ](/help/assets/icons/GraphTrend.svg) **de montages van de Grafiek**: Beoordeel wat uw grafiek en lijstvertoning. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.</li><li>![ Laag ](/help/assets/icons/Layer.svg) **de montages van de Bedekking**: Voeg een bedekking toe. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.</li><li>![ Emmertje ](/help/assets/icons/Bucket.svg) **[!UICONTROL Bucket settings]**: Auto emmertje of pas de montages van de douaneemmer op de gegevens toe. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.<li>![ DataCorrelated ](/help/assets/icons/DataCorrelated.svg) **[!UICONTROL Compare settings]**: Vergelijk gegevens met een specifieke datumwaaier. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.</li><li>![ Voetstappen ](/help/assets/icons/Footsteps.svg) **[!UICONTROL Display settings]**: Selecteer hoe te om de gegevens te tonen. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde analyse.<li>![ Kalender ](/help/assets/icons/Calendar.svg) **waaier van de Datum**: Een kalenderplukker die u toestaat om de datumwaaier van de analyse te bepalen. U kunt ook een interval selecteren voor uitgevoerde analyses, zoals dagelijks, wekelijks of maandelijks.</li><li>![ LightBulb ](/help/assets/icons/LightBulb.svg) **Inzichten**: Contextuele inzichten afhankelijk van de analyse die u bekijkt. Deze inzichten geven opmerkingen voor de huidige analyse. Als er meerdere inzichten beschikbaar zijn, kunt u deze weergeven met de pijlen aan de rechterkant. U kunt de zichtbaarheid van dit vak in- en uitschakelen met het gloeilamppictogram rechtsboven.</li></ul> |
| ![ pictogram van het Menu ](assets/menu.png){style="border:1px solid gray"} | **[!UICONTROL Menu]**<br/>Beschikbaar in een project van de Geleide analyse | Opdrachten in de rechterbovenhoek van een analyseproject met instructies die overkoepelende acties voor uw analyse bieden.<ul><li>![ het pictogram van Gegevens ](/help/assets/icons/Data.svg) ***Naam van gegevensmening***: Verander de gegevensmening die de analyse gebruikt. Wanneer u de gegevensmening verandert, veranderen de beschikbare componenten in vraagspoor ook.</li><li>![ het pictogram van de Verbinding ](/help/assets/icons/Link.svg) **verbinding van het Exemplaar**: Kopieert een verbinding aan de analyse aan uw klembord. U wordt gevraagd op te slaan voordat u gaat delen.</li><li>**Aandeel**: Opent het delen modaal, met verdere opties voor het delen aan individuele gebruikers of groepen. U kunt een analyse met andere gebruikers delen, of een verbinding produceren om met iedereen te delen.</li><li>**sparen**: Slaat de analyse op. Als u een nieuwe analyse opslaat, wordt het dialoogvenster **[!UICONTROL Save analysis]** weergegeven waarin u een naam en beschrijving kunt opgeven. Nadat u een **[!UICONTROL Analysis saved]** -dialoogvenster hebt opgeslagen, kunt u uw analyse delen.</li><li>![ voeg aan het pictogram van Workspace toe ](/help/assets/icons/MultipleAdd.svg) **[!UICONTROL Add to Workspace]**: toont beschikbare projecten van Workspace die u deze analyse kunt toevoegen aan. Als u een Workspace-project selecteert, wordt dat Workspace-project op een nieuw tabblad geopend en wordt de analyse onder aan het project toegevoegd.</li></ul>Selecteer ![ Meer pictogram ](/help/assets/icons/More.svg) voor meer acties, als:<ul><li>**[!UICONTROL Save as]**: slaat de analyse los van de huidige analyse op en maakt een kopie. Er wordt een dialoogvenster weergegeven waarin u een nieuwe naam en beschrijving kunt opgeven.</li><li>**[!UICONTROL Export to Workspace]**: maakt de huidige query voor analyse met instructies in Analysis Workspace opnieuw. Het Workspace-project wordt op een nieuw tabblad gemaakt, zodat onderbreking wordt voorkomen tijdens het werken in de analyse met instructies. Het is een kopie van de analyse en blijft na opening niet synchroon met de oorspronkelijke analyse. Gebruik dit bevel wanneer u aan uw analyst team wilt afleveren, of dieper in de gegevens duiken dan wat de analyse toestaat.</li><li>**[!UICONTROL Copy chart to clipboard]**: kopieert de diagramafbeelding naar het klembord, zodat deze in andere toepassingen kan worden geplakt. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**[!UICONTROL Download PNG]** : hiermee downloadt u de diagramafbeelding als een `.png` . De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**[!UICONTROL Download CSV]** : downloadt de tabelgegevens als een `.csv` . De queryrail en -grafiek worden niet in het bestand opgenomen.</li></ul> |
| ![ visualisatie van het Menu ](assets/menu-visualization.png){style="border:1px solid gray"} | **<br/>Beschikbaar 1} Menu in een Geleide analyse visualisatie in de werkruimte van de Analyse.** | Opdrachten in een Begeleide analyse visualisatie in de werkruimte van de Analyse.<ul><li>![ GraphScatter ](/help/assets/icons/GraphScatter.svg) **[!UICONTROL Chart]**: om slechts de grafiek van de analyse te tonen.</li><li>![ Lijst ](/help/assets/icons/Table.svg) **[!UICONTROL Table]**: om slechts de lijst van de analyse te tonen.</li><li>![ TableAndChart ](/help/assets/icons/TableAndChart.svg) **[!UICONTROL All]**: om grafiek en lijst van de analyse te tonen.</li><li>![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** uit: om de configuratie van de analyse uit te geven</li><li>![ Kalender ](/help/assets/icons/Calendar.svg) **[!UICONTROL *waaier van de Datum *]**: om de datumwaaier voor de analyse te vormen.</li></ul> |


## Inrichting

Analyses met instructies worden als volgt in pakketten Customers Journey Analytics opgenomen:

| Pakket | Beschikbare analyses |
| --- | --- |
| [!UICONTROL Customer Journey Analytics add-ons] | Actieve groei, Conversietrends, Frequentie, Trechter, Netto groei, Behoud, Trends |
| [!UICONTROL Customer Journey Analytics Foundation] | Trends |
| [!UICONTROL Customer Journey Analytics Select] | De meningen van de stichting + Actieve groei, de tendensen van de Omzetting, Frequentie, Trechter, Netto groei, Behoud |
| [!UICONTROL Customer Journey Analytics Prime] | Weergaven selecteren + Betrokkenheid, impact eerste gebruik, impact release, tijdlijn |
| [!UICONTROL Customer Journey Analytics Ultimate] | Prime-weergaven |

{style="table-layout:auto"}

Beheerders van productprofielen kunnen toegang tot de analyse met instructies in de Adobe Admin Console toevoegen of verwijderen.

1. Login aan [ Adobe Admin Console ](https://adminconsole.adobe.com).
1. Selecteer **[!UICONTROL Customer Journey Analytics]** in de lijst met producten.
1. Selecteer het gewenste productprofiel voor de machtigingen die u wilt bewerken.
1. Selecteer de tab **[!UICONTROL Permissions]** en klik vervolgens op **[!UICONTROL Edit]** onder [!UICONTROL Reporting Tools] .
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) naast **[!UICONTROL Guided Analysis Access]** in de lijst van [!UICONTROL Available Permission Items], die het aan de lijst van [!UICONTROL Included Permission Items] toevoegt.
1. Selecteer **[!UICONTROL Save]** .

Zie [ het niveautoegang van de Gebruiker ](/help/technotes/access-control.md#user-level-access) voor meer informatie.

>[!TIP]
>
>Sommige beheerders schakelen de analyse met instructies liever in en schakelen Analysis Workspace voor nieuwe gebruikers uit om te Customers Journey Analytics. Als deze gebruikers klaar zijn met het product en uw organisatorische gegevens, kunt u vervolgens toegang tot Analysis Workspace inschakelen.
