---
title: Overzicht van geleide analyse
description: Een methode om gegevens in Customer Journey Analytics te analyseren die productteams snel inzichten van hoge kwaliteit laat krijgen.
keywords: productanalyse
exl-id: 1ac8157f-87e8-4d98-a2ca-f6beb68d9d6b
feature: Guided Analysis
role: User
source-git-commit: a7545c5a197bd318212328ef6344245b2026d401
workflow-type: tm+mt
source-wordcount: '1339'
ht-degree: 0%

---

# Overzicht van geleide analyse

Met een analyse met instructies kunnen gebruikers, van marketing tot product tot analisten, zelf hoogwaardige gegevens en inzichten bedienen over de reis van de klant via geleide workflows, gebaseerd op de kanaalgegevens van de Customer Journey Analytics. Gelijkaardig aan Analysis Workspace en Mobiele scorecards, gebruikt de geleide analyse gegevens van de mening van a [ Gegevens ](/help/data-views/data-views.md), die verwijzingen gegevens in Adobe Experience Platform door a [ Verbinding ](../connections/overview.md). Veel rapporten die zijn gemaakt met geleide analyse kunnen naadloos worden overgedragen naar Analysis Workspace voor aanvullend onderzoek.

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

U hebt toegang tot Analyse met instructies vanaf de startpagina van de Customer Journey Analytics.

1. Selecteer **[!UICONTROL Guided analysis]** van de homepage, die u rechtstreeks aan de [ mening van de tendensen van het Gebruik ](types/trends.md) neemt.

   ![ het Bestaan paginatielijn ](assets/landing-page-tile.png){style="border:1px solid gray"}

1. Selecteer **[!UICONTROL Create new]** om de verschillende weergaveopties weer te geven en een ander beginpunt voor de analyse te kiezen.

   ![ creeer een nieuw modaal ](assets/create-new-modal.png){style="border:1px solid gray"}

U kunt tot Geleide Analyse van binnen een project van Analysis Workspace ook toegang hebben.

1. Selecteer **[!UICONTROL Blank project]** op de startpagina om een leeg Workspace-project te maken.

   ![ creeer leeg project ](assets/blank-project.png){style="border:1px solid gray"}

1. Selecteer ![ Geleide analyse ](/help/assets/icons/GuidedAnalysis.svg) **[!UICONTROL Guided Analysis]** in het linkerspoor.

   ![ Workspace linkerspoor ](assets/workspace-left-rail.png){style="border:1px solid gray"}

1. Sleep een nieuwe analyse naar het Workspace-canvas en selecteer vervolgens **[!UICONTROL Create]** om de gewenste analyse te genereren (bijvoorbeeld: **[!UICONTROL Create Trends]** ). U kunt ook een bestaande analyse naar het Workspace-canvas slepen vanuit de sectie **[!UICONTROL Saved]** .

   ![ creeer paneel ](assets/create-guided-analysis-panel.gif)

## Interface

De interface voor geleide analyse volgt een vraag en antwoordformaat. Vorm uw vraag in vraagspoor, dan krijg een antwoord met een geschreven inzicht, grafiek, en lijst. Vervolgens kunt u de volgende vraag stellen met weergavetypen en visualisatie-instellingen.

De geleide analyse gebruikt de volgende elementen UI:

| Interfacevoorvertoning | UI-element | Beschrijving |
| --- | --- | --- |
| ![ spoorweg van de Vraag ](assets/query-rail.png){style="border:1px solid gray"} | Query-rail | Vorm uw &quot;vraag&quot;zijn het selecteren van de gewenste componenten (gebeurtenissen, eigenschappen, en segmenten) die omhoog een analyse maken. De volgende opties zijn beschikbaar voor alle weergavetypen, met extra instellingen per weergave. <ul><li>**de selecteur van de Analyse**: Een drop-down die u aan een nieuw analysetype laat schakelen. Uw vraagselecties worden gehandhaafd binnen de toegestane grenzen voor het nieuwe analysetype.</li><li>**Gebeurtenissen**: De gebeurtenissen die u wilt meten. Elk weergavetype past verschillende limieten toe op het aantal gebeurtenissen dat u kunt configureren.</li><li>**Filters**: Gebruik het ![ pictogram van de Filter ](assets/filter.png) in de sectie van Gebeurtenissen of van Segmenten om door specifieke dimensies neer te versmallen. Wanneer een afmeting is geselecteerd, zijn zowel de standaardfiltercriteria (zoals [!UICONTROL Equals] , [!UICONTROL Contains] of [!UICONTROL Ends with] ) als de bovenste 1000-afmetingswaarden beschikbaar.</li><li>**die als** wordt geteld: De tellende methode die u op de geselecteerde gebeurtenissen wilt toepassen.</li><li>**Segmenten**: De segmenten die u wilt meten. Elk meningstype dwingt verschillende grenzen aan het aantal segmenten af die u kunt vormen.</li></ul> |
| ![ Grafiek ](assets/chart.png){style="border:1px solid gray"} | Diagram | Een visualisatie van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Welke visualisatie u ziet hangt van de mening en de montages boven de grafiek af. Het diagram bevat ook: <ul><li>**Knopinfo**: Beweeg over om het even welk punt van grafiekgegevens om tooltip met meer informatie bloot te stellen.</li><li>**Legend**: Beweeg over de reeks van de grafieklegenda om definities te bekijken waar beschikbaar, nadruk op die reeks, en tijdelijk andere reeksen te verbergen. Verberg een reeks in de legenda door erop te klikken.</li><li>**Annotaties**: Toepasselijke [ annotaties ](../components/annotations/overview.md) zijn zichtbaar tussen de visualisatie en de legenda. Het wordt getoond als pictogram van de a ![ Annotatie ](assets/annotation.png) in de gevormde kleur van de annotatie. De types van mening die gegevens in tijd tonen plaatsen het ![ pictogram van de Annotatie ](assets/annotation.png) onder de gevormde datum of datumwaaier. De types van mening die geen gegevens in tijd tonen tonen tonen tonen het ![ pictogram van de Annotatie ](assets/annotation.png) in de lagere juiste hoek van de grafiek.</li><li>**Uitgezochte acties**: blootstellings beschikbare volgende acties door om het even welk gegevenspunt te selecteren. De opties omvatten **sparen segment**.</li></ul> |
| ![ Lijst ](assets/table.png){style="border:1px solid gray"} | Tabel | Een tabelweergave van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Kolommen in de tabel zijn afhankelijk van het weergavetype boven het diagram. De tabel bevat ook: <ul><li>**Uitgezochte acties**: Verberg of stel een grafiekreeks bloot door het ![ tonen verborgen pictogram ](assets/hide-in-chart.png) pictogram in elke rij van een knevel te voorzien. Aanvullende handelingen zijn beschikbaar door het menu **[!UICONTROL More]** te selecteren. De opties omvatten **sparen segment**.</li></ul> |
| ![ Visualisatie montages ](assets/visualization-settings.png){style="border:1px solid gray"} | Visualisatie-instellingen | Opties boven het diagram waarmee u de volgende vraag kunt stellen en aanpassen hoe het diagram en de tabel worden geretourneerd. De volgende opties zijn beschikbaar voor alle weergavetypen, met extra instellingen per weergave. <ul><li>**de montages van de Grafiek**: Fijnt wat uw grafiek en lijstvertoning. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde weergave.</li><li>**waaier van de Datum**: Een kalenderplukker die u toestaat om de datumwaaier van de analyse te bepalen. U kunt ook een interval selecteren voor georiënteerde weergaven, zoals dag, week of maand.</li><li>**Inzichten**: Contextuele inzichten afhankelijk van de analyse die u bekijkt. Deze inzichten geven opmerkingen voor de huidige analyse. Als er meerdere inzichten beschikbaar zijn, kunt u deze weergeven met de pijlen aan de rechterkant. U kunt de zichtbaarheid van dit vak in- en uitschakelen met het gloeilamppictogram rechtsboven.</li></ul> |
| ![ Menu ](assets/menu.png){style="border:1px solid gray"} | Menu | Opdrachten in de rechterbovenhoek van geleide analyse die overkoepelende acties voor uw analyse bieden.<ul><li>**de meningsselecteur van Gegevens**: Verander de gegevensmening die de analyse gebruikt. Wanneer u de gegevensmening verandert, veranderen de beschikbare componenten in vraagspoor ook.</li><li>**verbinding van het Exemplaar**: Kopieert een verbinding aan de analyse aan uw klembord. U wordt gevraagd op te slaan voordat u gaat delen.</li><li>**Aandeel**: Opent het delen modaal, met verdere opties voor het delen aan individuele gebruikers of groepen. U kunt een analyse met andere gebruikers delen, of een verbinding produceren om met iedereen te delen.</li><li>**sparen**: Slaat de analyse op. Als u een nieuwe analyse opslaat, verschijnt een modaal venster dat om een naam en een beschrijving verzoekt.</li><li>**sparen als**: Slaat de analyse los van de huidige analyse, die tot een exemplaar leidt. Er wordt een modaal venster weergegeven met een nieuwe naam en beschrijving.</li><li>**Uitvoer naar Workspace**: Herstelt de huidige geleide analysevraag in Analysis Workspace. Het Workspace-project wordt op een nieuw tabblad gemaakt, zodat onderbreking wordt voorkomen tijdens het werken met een geleide analyse. Het is een kopie van de analyse en blijft niet synchroon met de oorspronkelijke geleide analyse als deze eenmaal is geopend. Gebruik deze opdracht wanneer u de gegevens naar uw analyseteam wilt verplaatsen of dieper wilt duiken in de gegevens dan in de geleide analyse is toegestaan.</li><li>**Exemplaar aan klembord**: Kopieert grafiekgrafisch aan uw klembord, dat in andere toepassingen moet worden gekleefd. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**Download PNG**: Downloadt grafisch grafiek als a `.png`. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**download CSV**: Downloadt de lijstgegevens als a `.csv`. De queryrail en -grafiek worden niet in het bestand opgenomen.</li></ul> |

{style="table-layout:auto"}

## Inrichting

Analyses met instructies worden als volgt in pakketten Customers Journey Analytics opgenomen:

| Pakket | Beschikbare analyses |
| --- | --- |
| [!UICONTROL Customer Journey Analytics add-ons] | Actieve groei, Conversietrends, Frequentie, Trechter, Netto groei, Behoud, Trends |
| [!UICONTROL Customer Journey Analytics Foundation] | Trends |
| [!UICONTROL Customer Journey Analytics Select] | De meningen van de stichting + Actieve groei, de tendensen van de Omzetting, Frequentie, Trechter, Netto groei, Behoud |
| [!UICONTROL Customer Journey Analytics Prime] | Weergaven selecteren + Betrokkenheid, impact eerste gebruik, impact release, tijdlijn |
| [!UICONTROL Customer Journey Analytics Ultimate] | Eerste weergaven |

{style="table-layout:auto"}

Beheerders van productprofielen kunnen toegang tot geleide analyse toevoegen of verwijderen in de Adobe Admin Console.

1. Login aan [ Adobe Admin Console ](https://adminconsole.adobe.com).
1. Selecteer **[!UICONTROL Customer Journey Analytics]** in de lijst met producten.
1. Selecteer het gewenste productprofiel voor de machtigingen die u wilt bewerken.
1. Selecteer de tab **[!UICONTROL Permissions]** en klik vervolgens op **[!UICONTROL Edit]** onder [!UICONTROL Reporting Tools] .
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) naast **[!UICONTROL Guided Analysis Access]** in de lijst van [!UICONTROL Available Permission Items], die het aan de lijst van [!UICONTROL Included Permission Items] toevoegt.
1. Selecteer **[!UICONTROL Save]** .

Zie [ het niveautoegang van de Gebruiker ](/help/technotes/access-control.md#user-level-access) voor meer informatie.

>[!TIP]
>
>Sommige beheerders willen geleide analyses inschakelen en Analysis Workspace voor nieuwe gebruikers uitschakelen voor Customer Journey Analytics. Als deze gebruikers klaar zijn met het product en uw organisatorische gegevens, kunt u vervolgens toegang tot Analysis Workspace inschakelen.
