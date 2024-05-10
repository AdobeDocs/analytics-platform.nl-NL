---
title: Overzicht van geleide analyse
description: Een methode om gegevens in Customer Journey Analytics te analyseren die productteams snel inzichten van hoge kwaliteit laat krijgen. Wordt ook wel Product Analytics genoemd.
keywords: productanalyse
exl-id: 1ac8157f-87e8-4d98-a2ca-f6beb68d9d6b
feature: Guided Analysis
role: User
source-git-commit: 2b8afe1dbac5057f867437e2bfce27f3bd752d57
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---

# Overzicht van geleide analyse

Met een geleide analyse kunnen gebruikers zelf hoogwaardige gegevens en inzichten bedienen over de reis van de klant via geleide workflows, op basis van de kanaalgegevens van de Customer Journey Analytics. De interfunctionele teams, van marketing aan product, kunnen in echt - tijd verbinden om deze rapporten te gebruiken en te begrijpen.

>[!NOTE]
>
> Analyse met instructies is momenteel alleen beschikbaar als onderdeel van Adobe Product Analytics, wat een betaalde aanvulling op de Customer Journey Analytics is. Neem contact op met het accountteam van uw Adobe als uw organisatie deze reeks mogelijkheden wil gaan gebruiken.

Gelijkaardig aan Analysis Workspace en Mobiele scorecards, gebruikt de geleide analyse gegevens van een [Gegevens, weergave](../data-views/data-views.md), die verwijst naar gegevens in Adobe Experience Platform via een [Verbinding](../connections/overview.md). Veel rapporten die zijn gemaakt met geleide analyse kunnen naadloos worden overgedragen naar Analysis Workspace voor aanvullend onderzoek.

De volgende geleide analysemeningen zijn beschikbaar:

| Type analyse | Type weergave | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Feature matrix] | [Engagement](types/engagement.md) | Begrijp de breedte en breedte van de betrokkenheid van functies. |
| [!UICONTROL Funnel] | [Wrijving](types/friction.md) | Vergelijk de conversiesnelheden tussen de stappen. |
| [!UICONTROL Funnel] | [Conversietrends](types/conversion-trends.md) | Wijzigingen in conversietarieven bijhouden in de loop van de tijd. |
| [!UICONTROL Impact] | [Geen](types/release.md) | Vergelijk de prestaties in gelijke perioden vóór en na de release. |
| [!UICONTROL Impact] | [Eerste gebruik](types/first-use.md) | Meet het effect van het gebruik van de eerste functie op sleutelindicatoren. |
| [!UICONTROL Retention] | [Bewaarpercentages](types/retention-rates.md) | Meet de doorlopende retourgewoonten van uw gebruikers. |
| [!UICONTROL Trends] | [Gebruik](types/usage.md) | Meet de betrokkenheid van de gebruiker in de loop van de tijd. |
| [!UICONTROL Trends] | [Frequentie](types/frequency.md) | Meet de betrokkenheid per gebruiksfrequentie. |
| [!UICONTROL User growth] | [Actief](types/active.md) | Identificeer wie nieuw, behouden, terugkeren, of slapend is. |
| [!UICONTROL User growth] | [Netto groei](types/net-growth.md) | Wint of verliest u gebruikers? |
| [!UICONTROL User stream] | [Tijdlijn](types/timeline.md) | Verken patronen in sessieactiviteiten. |

{style="table-layout:auto"}

## Toegang

Als uw organisatie is voorzien voor geleide analyse, kunt u tot het van de homepage van de Customer Journey Analytics toegang hebben.

1. Klikken **[!UICONTROL Guided analysis]** vanaf de homepage, die u rechtstreeks naar de [Weergave trends gebruiken](types/usage.md).

   ![Landingspagina-element](assets/landing-page-tile.png){style="border:1px solid gray"}

1. Klikken **[!UICONTROL Create new]** om de verschillende weergaveopties weer te geven en een ander beginpunt voor de analyse te kiezen.

   ![Een nieuw modaal model maken](assets/create-new-modal.png){style="border:1px solid gray"}

Neem contact op met het accountteam van de Adobe als uw organisatie nog niet beschikt over instructies voor een geleide analyse.

## Interface

De interface voor geleide analyse volgt een vraag en antwoordformaat. Vorm uw vraag in vraagspoor, dan krijg een antwoord met een geschreven inzicht, grafiek, en lijst. Vervolgens kunt u de volgende vraag stellen met weergavetypen en visualisatie-instellingen.

De geleide analyse gebruikt de volgende elementen UI:

| Interfacevoorvertoning | UI-element | Beschrijving |
| --- | --- | --- |
| ![Query-rail](assets/query-rail.png){style="border:1px solid gray"} | Query-rail | Vorm uw &quot;vraag&quot;zijn het selecteren van de gewenste componenten (gebeurtenissen, eigenschappen, en segmenten) die omhoog een analyse maken. De volgende opties zijn beschikbaar voor alle weergavetypen, met extra instellingen per weergave. <ul><li>**Analyse-kiezer**: Een vervolgkeuzelijst waarmee u naar een nieuw type analyse kunt schakelen. Uw vraagselecties worden gehandhaafd binnen de toegestane grenzen voor het nieuwe analysetype.</li><li>**Selector weergeven**: Een drop-down die u aan een nieuwe mening (&quot;antwoord&quot;) voor de vraag laat schakelen u vormde. Uw vraagselecties worden gehandhaafd binnen de toegestane grenzen voor het nieuwe meningstype.</li><li>**Gebeurtenissen**: De gebeurtenissen die u wilt meten. Elk weergavetype past verschillende limieten toe op het aantal gebeurtenissen dat u kunt configureren.</li><li>**Filters**: Gebruik de ![Filter](assets/filter.png) in de sectie Gebeurtenissen of Segmenten om te versmallen op basis van specifieke eigenschappen. Wanneer een eigenschap is geselecteerd, worden beide standaardfiltercriteria (zoals [!UICONTROL Equals], [!UICONTROL Contains], of [!UICONTROL Ends with]) en zijn de bovenste 1000-eigenschapswaarden beschikbaar.</li><li>**Afgeteld als**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen.</li><li>**Segmenten**: De segmenten die u wilt meten. Elk meningstype dwingt verschillende grenzen aan het aantal segmenten af die u kunt vormen.</li></ul> |
| ![Diagram](assets/chart.png){style="border:1px solid gray"} | Diagram | Een visualisatie van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Welke visualisatie u ziet hangt van de mening en de montages boven de grafiek af. Het diagram bevat ook: <ul><li>**Knopinfo**: Houd de muisaanwijzer boven een gegevenspunt van een diagram om knopinfo met meer informatie weer te geven.</li><li>**Legenda**: Houd de cursor boven de kaartlegendenreeks om definities te bekijken waar deze beschikbaar is, focus op die reeks en verberg tijdelijk andere reeksen. Verberg een reeks in de legenda door erop te klikken.</li><li>**Annotaties**: Van toepassing [annotaties](../components/annotations/overview.md) zijn zichtbaar tussen de visualisatie en de legenda. Het wordt weergegeven als een ![Annotatiepictogram](assets/annotation.png) in de geconfigureerde kleur van de aantekening. De types van mening die gegevens in tijd tonen plaats ![Annotatiepictogram](assets/annotation.png) onder de geconfigureerde datum of datumbereik. De types van mening die geen gegevens in tijd tonen tonen tonen tonen tonen ![Annotatiepictogram](assets/annotation.png) in de rechterbenedenhoek van het diagram.</li><li>**Handelingen klikken**: Maak beschikbare volgende handelingen beschikbaar door met de linkermuisknop op een gegevenspunt te klikken. Opties omvatten **Segment opslaan**.</li></ul> |
| ![Tabel](assets/table.png){style="border:1px solid gray"} | Tabel | Een tabelweergave van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Kolommen in de tabel zijn afhankelijk van het weergavetype boven het diagram. De tabel bevat ook: <ul><li>**Handelingen klikken**: Verberg of stel een grafiekreeks bloot door van een knevel te voorzien ![Pictogram voor verbergen tonen](assets/hide-in-chart.png) in elke rij. Aanvullende handelingen zijn beschikbaar door op de knop **[!UICONTROL More]** -menu. Opties omvatten **Segment opslaan**.</li></ul> |
| ![Visualisatie-instellingen](assets/visualization-settings.png){style="border:1px solid gray"} | Visualisatie-instellingen | Opties boven het diagram waarmee u de volgende vraag kunt stellen en aanpassen hoe het diagram en de tabel worden geretourneerd. De volgende opties zijn beschikbaar voor alle weergavetypen, met extra instellingen per weergave. <ul><li>**Diagraminstellingen**: Stel nauwkeurig in wat uw diagram en tabel worden weergegeven. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde weergave.</li><li>**Datumbereik**: Een kalenderkiezer waarmee u het datumbereik van de analyse kunt bepalen. U kunt ook een interval selecteren voor georiënteerde weergaven, zoals dag, week of maand.</li><li>**Inzichten**: Contextuele inzichten afhankelijk van de analyse die u bekijkt. Deze inzichten geven opmerkingen voor de huidige analyse. Als er meerdere inzichten beschikbaar zijn, kunt u deze weergeven met de pijlen aan de rechterkant. U kunt de zichtbaarheid van dit vak in- en uitschakelen met het gloeilamppictogram rechtsboven.</li></ul> |
| ![Menu](assets/menu.png){style="border:1px solid gray"} | Menu | Opdrachten in de rechterbovenhoek van geleide analyse die overkoepelende acties voor uw analyse bieden.<ul><li>**Selector gegevensweergave**: Wijzig de gegevensweergave die de analyse gebruikt. Wanneer u de gegevensmening verandert, veranderen de beschikbare componenten in vraagspoor ook.</li><li>**Koppeling kopiëren**: Kopieert een koppeling naar de analyse naar het klembord. U wordt gevraagd op te slaan voordat u gaat delen.</li><li>**Delen**: Hiermee opent u de modus voor delen, met verdere opties voor het delen naar afzonderlijke gebruikers of groepen. U kunt een analyse met andere gebruikers delen, of een verbinding produceren om met iedereen te delen.</li><li>**Opslaan**: slaat de analyse op. Als u een nieuwe analyse opslaat, verschijnt een modaal venster dat om een naam en een beschrijving verzoekt.</li><li>**Opslaan als**: Hiermee slaat u de analyse los van de huidige analyse op en maakt u een kopie. Er wordt een modaal venster weergegeven met een nieuwe naam en beschrijving.</li><li>**Openen in werkruimte**: Herstelt de huidige geleide analyse in Analysis Workspace. Het project Workspace wordt op een nieuw tabblad gemaakt, zodat onderbreking wordt voorkomen tijdens het werken met een geleide analyse. Het is een kopie van de analyse en blijft niet synchroon met de oorspronkelijke geleide analyse als deze eenmaal is geopend. Gebruik deze opdracht wanneer u de gegevens naar uw analyseteam wilt verplaatsen of dieper wilt duiken in de gegevens dan in de geleide analyse is toegestaan.</li><li>**Kopiëren naar klembord**: Hiermee kopieert u de grafiekafbeelding naar het klembord, die u in andere toepassingen wilt plakken. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**PNG downloaden**: Hiermee downloadt u de diagramafbeelding als een `.png`. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**CSV downloaden**: Hiermee worden de tabelgegevens gedownload als een `.csv`. De queryrail en -grafiek worden niet in het bestand opgenomen.</li></ul> |

{style="table-layout:auto"}

## Inrichting

Analyse met instructies maakt deel uit van het Adobe Product Analytics, dat een betaalde aanvulling op de Customer Journey Analytics is. Neem contact op met het accountteam van uw Adobe als uw organisatie deze reeks mogelijkheden wil gaan gebruiken.

Als uw organisatie is ingericht voor een geleide analyse, kunnen beheerders van productprofielen er toegang toe toevoegen of verwijderen in de Adobe Admin Console.

1. Aanmelden bij de [Adobe Admin Console](https://adminconsole.adobe.com).
1. Selecteren **[!UICONTROL Customer Journey Analytics]** in de lijst van producten.
1. Selecteer het gewenste productprofiel voor de machtigingen die u wilt bewerken.
1. Klik op de knop **[!UICONTROL Permissions]** tab, en klik vervolgens op **[!UICONTROL Edit]** krachtens [!UICONTROL Reporting Tools].
1. Klik op het plusteken naast **[!UICONTROL Guided Analysis Access]** in de lijst van [!UICONTROL Available Permission Items], die het aan de lijst van [!UICONTROL Included Permission Items].
1. Klik op **[!UICONTROL Save]**.

>[!TIP]
>
>Sommige beheerders willen geleide analyses inschakelen en Analysis Workspace voor nieuwe gebruikers uitschakelen voor Customer Journey Analytics. Als deze gebruikers klaar zijn met het product en uw organisatorische gegevens, kunt u vervolgens toegang tot Analysis Workspace inschakelen.
