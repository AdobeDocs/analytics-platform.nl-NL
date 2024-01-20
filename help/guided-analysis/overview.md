---
title: Overzicht van geleide analyse
description: Een methode om gegevens in Customer Journey Analytics te analyseren die productteams snel inzichten van hoge kwaliteit laat krijgen. Wordt ook wel Product Analytics genoemd.
keywords: productanalyse
exl-id: 1ac8157f-87e8-4d98-a2ca-f6beb68d9d6b
feature: Guided Analysis
role: User
source-git-commit: 6f80a1aa4ec9142d75fe1abb2f268dc60c7dd245
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# Overzicht van geleide analyse

Adobe Product Analytics stelt productteams in staat zelf gegevens en inzichten over hun productervaring te bedienen door middel van geleide analyseworkflows, gebaseerd op de kanaalgegevens van de Customer Journey Analytics. De geleide analyse is een rapporteringsformaat dat productteams toestaat om hun gegevensbehoeften snel zelf-te dienen zodat zij high-quality inzicht snel kunnen krijgen en meer gegeven-gedreven productbesluiten kunnen nemen. Interfunctionele teams kunnen in real time verbinding maken om deze rapporten te gebruiken en te begrijpen.

Net als Analysis Workspace en Mobile-scorecards gebruikt een analyserapport met instructies gegevens van een [Gegevens, weergave](../data-views/data-views.md), die verwijst naar gegevens in Adobe Experience Platform via een [Verbinding](../connections/overview.md). Alle rapporten die zijn gemaakt in de analyse met instructies kunnen naadloos worden overgedragen naar Analysis Workspace voor aanvullend onderzoek.

De geleide analyse verstrekt veelvoudige manieren om gegevens te analyseren en te bekijken. Weergavetypen kunnen dezelfde gegevens op verschillende manieren weergeven, wat leidt tot verschillende inzichten met dezelfde gebeurtenissen en segmenten. U krijgt verschillende vraagrails en visualisatie montages afhankelijk van de mening die u kiest. U kunt vrij tussen meningen schakelen, en om het even welke toepasselijke vraagspoorcomponenten dragen over als de mening hen steunt.

De geleide analyse categoriseert meningstypes in **Analysetypen**. De volgende analyse- en weergavetypen zijn beschikbaar:

| Type analyse | Type weergave | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Impact] | [Geen](types/release.md) | Vergelijk de prestaties in gelijke perioden vóór en na de release. |
| [!UICONTROL Impact] | [Eerste gebruik](types/first-use.md) | Meet het effect van het gebruik van de eerste functie op sleutelindicatoren. |
| [!UICONTROL Funnel] | [Wrijving](types/friction.md) | Vergelijk de conversiesnelheden tussen de stappen. |
| [!UICONTROL Funnel] | [Conversietrends](types/conversion-trends.md) | Wijzigingen in conversietarieven bijhouden in de loop van de tijd. |
| [!UICONTROL User growth] | [Actief](types/active.md) | Identificeer wie nieuw, behouden, terugkeren, of slapend is. |
| [!UICONTROL User growth] | [Netto groei](types/net-growth.md) | Wint of verliest u gebruikers? |
| [!UICONTROL Trends] | [Gebruik](types/usage.md) | Meet de betrokkenheid van de gebruiker in de loop van de tijd. |
| [!UICONTROL Trends] | [Frequentie](types/frequency.md) | Meet de betrokkenheid per gebruiksfrequentie. |

{style="table-layout:auto"}

## Toegang

Als uw organisatie is voorzien voor geleide analyse, kunt u tot het van de homepage van de Customer Journey Analytics toegang hebben.

1. Klikken **[!UICONTROL Guided analysis]** vanaf de homepage, die u rechtstreeks naar de [Weergave trends gebruiken](types/usage.md).

   ![Landingspagina-element](assets/landing-page-tile.png)

1. Klikken **[!UICONTROL Create new]** om de verschillende weergaveopties weer te geven en een ander beginpunt voor de analyse te kiezen.

   ![Een nieuw modaal model maken](assets/create-new-modal.png)

Neem contact op met het accountteam van de Adobe als uw organisatie nog niet beschikt over instructies voor een geleide analyse.

## Interface

De interface voor geleide analyse volgt een vraag en antwoordformaat. Vorm uw vraag in vraagspoor, dan krijg een antwoord met een geschreven inzicht, grafiek, en lijst. Vervolgens kunt u de volgende vraag stellen met de visualisatie-instellingen en weergavetypen.

Ongeacht het type analyse, gebruikt de geleide analyse de volgende elementen UI:

| Interfacevoorvertoning | UI-element | Beschrijving |
| --- | --- | --- |
| ![Query-rail](assets/query-rail.png) | Query-rail | Vorm de gewenste componenten (gebeurtenissen, eigenschappen, en segmenten) die omhoog een analyse maken. Elk analysetype dwingt verschillende grenzen aan het aantal gebeurtenissen en segmenten af die u kunt vormen.<p>Gebruik het filterpictogram om omlaag te versmallen door specifieke gebeurteniseigenschappen of om segmenten te creëren op de vlucht. Wanneer een eigenschap is geselecteerd, bevat en eindigt deze met standaardfiltercriteria, zoals equals, een lijst met de bovenste 1000-eigenschapswaarden die snel kunnen worden gefilterd.<p>Als u op een nieuw analysetype schakelt, worden uw vraagselecties gehandhaafd binnen de toegestane grenzen voor dat analysetype. |
| ![Diagram](assets/chart.png) | Diagram | Een visualisatie van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Welke visualisatie u ziet hangt van de mening en de montages boven de grafiek af. Het diagram bevat ook: <ul><li>**Knopinfo**: Houd de muisaanwijzer boven een gegevenspunt van een diagram om knopinfo met meer informatie weer te geven.</li><li>**Legenda**: Houd de cursor boven de kaartlegendenreeks om definities te bekijken waar deze beschikbaar is, focus op die reeks en verberg tijdelijk andere reeksen. Verberg een reeks in de legenda door erop te klikken.</li><li>**Annotaties**: Van toepassing [annotaties](../components/annotations/overview.md) zijn zichtbaar tussen de visualisatie en de legenda. Het wordt weergegeven als een ![Annotatiepictogram](assets/annotation.png) in de geconfigureerde kleur van de aantekening. De types van mening die gegevens in tijd tonen plaats ![Annotatiepictogram](assets/annotation.png) onder de geconfigureerde datum of datumbereik. De types van mening die geen gegevens in tijd tonen tonen tonen tonen tonen ![Annotatiepictogram](assets/annotation.png) in de rechterbenedenhoek van het diagram.</li><li>**Handelingen klikken**: Maak beschikbare volgende handelingen beschikbaar door met de linkermuisknop op een gegevenspunt te klikken. Opties omvatten **Segment opslaan**.</li></ul> |
| ![Tabel](assets/table.png) | Tabel | Een tabelweergave van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Kolommen in de tabel zijn afhankelijk van het weergavetype boven het diagram. De tabel bevat ook: <ul><li>**Handelingen klikken**: Verberg of stel een grafiekreeks bloot door van een knevel te voorzien ![Pictogram voor verbergen tonen](assets/hide-in-chart.png) in elke rij. Aanvullende handelingen zijn beschikbaar door op de knop **[!UICONTROL More]** -menu. Opties omvatten **Segment opslaan**.</li></ul> |
| ![Visualisatie-instellingen](assets/visualization-settings.png) | Visualisatie-instellingen | Opties boven het diagram waarmee u de volgende vraag kunt stellen en aanpassen hoe het diagram en de tabel worden geretourneerd. De volgende opties zijn beschikbaar voor alle weergavetypen, met extra instellingen per weergave. <ul><li>**Type weergave**: Een keuzelijst waarmee u gegevens voor een bepaald analysetype op een andere manier kunt presenteren.</li><li>**Diagraminstellingen**: Stel nauwkeurig in wat uw diagram en tabel worden weergegeven. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde weergave.</li><li>**Datumbereik**: Een kalenderkiezer waarmee u het datumbereik van de analyse kunt bepalen. U kunt ook een interval selecteren voor georiënteerde weergaven, zoals dag, week of maand.</li><li>**Inzichten**: Contextuele inzichten afhankelijk van de analyse die u bekijkt. Met de pijlen kunt u extra inzichten weergeven of verbergen met het gloeilamppictogram rechtsboven.</li></ul> |
| ![Menu](assets/menu.png) | Menu | Opdrachten in de rechterbovenhoek van geleide analyse die overkoepelende acties voor uw analyse bieden.<ul><li>**Selector gegevensweergave**: Wijzig de gegevensweergave die de analyse gebruikt. Wanneer u de gegevensmening verandert, veranderen de beschikbare componenten in vraagspoor ook.</li><li>**Opslaan**: slaat de analyse op. Als u een nieuwe analyse opslaat, verschijnt een modaal venster dat om een naam en een beschrijving verzoekt.</li><li>**Opslaan als**: Hiermee slaat u de analyse los van de huidige analyse op en maakt u een kopie. Er wordt een modaal venster weergegeven met een nieuwe naam en beschrijving.</li><li>**Openen in werkruimte**: Hiermee maakt u de huidige analyse met instructies in Analysis Workspace opnieuw. Het project Workspace wordt op een nieuw tabblad gemaakt, zodat onderbreking wordt voorkomen tijdens het werken in de analyse Met instructies. Het is een kopie van de analyse en blijft niet synchroon met de oorspronkelijke geleide analyse als deze eenmaal is geopend. Gebruik deze opdracht als u de gegevens naar het analyseteam wilt verplaatsen of dieper wilt duiken in de gegevens dan in de analyse met instructies is toegestaan.</li><li>**Kopiëren naar klembord**: Hiermee kopieert u de grafiekafbeelding naar het klembord, die u in andere toepassingen wilt plakken. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**PNG downloaden**: Hiermee downloadt u de diagramafbeelding als een `.png`. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**CSV downloaden**: Hiermee worden de tabelgegevens gedownload als een `.csv`. De queryrail en -grafiek worden niet in het bestand opgenomen.</li></ul> |

{style="table-layout:auto"}

## Inrichting

Analyse met instructies maakt deel uit van het Adobe Product Analytics, dat een betaalde aanvulling op de Customer Journey Analytics is. Neem contact op met het accountteam van uw Adobe als uw organisatie deze reeks mogelijkheden wil gaan gebruiken.

Als uw organisatie is ingericht voor de analyse met instructies, kunnen beheerders van productprofielen er toegang toe toevoegen of verwijderen in de Adobe Admin Console.

1. Aanmelden bij de [Adobe Admin Console](https://adminconsole.adobe.com).
1. Selecteren **[!UICONTROL Customer Journey Analytics]** in de lijst van producten.
1. Selecteer het gewenste productprofiel voor de machtigingen die u wilt bewerken.
1. Klik op de knop **[!UICONTROL Permissions]** tab, en klik vervolgens op **[!UICONTROL Edit]** krachtens [!UICONTROL Reporting Tools].
1. Klik op het plusteken naast **[!UICONTROL Guided Analysis Access]** in de lijst van [!UICONTROL Available Permission Items], die het aan de lijst van [!UICONTROL Included Permission Items].
1. Klik op **[!UICONTROL Save]**.

>[!TIP]
>
>Sommige beheerders schakelen de analyse met instructies liever in en schakelen Analysis Workspace voor nieuwe gebruikers uit om te Customers Journey Analytics. Als deze gebruikers klaar zijn met het product en uw organisatorische gegevens, kunt u vervolgens toegang tot Analysis Workspace inschakelen.
