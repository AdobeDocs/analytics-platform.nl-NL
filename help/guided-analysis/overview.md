---
title: Overzicht van geleide analyse
description: Een methode om gegevens in Customer Journey Analytics te analyseren die productteams snel inzichten van hoge kwaliteit laat krijgen. Wordt ook wel Product Analytics genoemd.
exl-id: 6a8a92db-f030-424e-af9b-f8f6502084f6
feature: Guided Analysis
source-git-commit: 4ed5acc2c9bb1a530d16d9c3ce8f5e9243bfa1f2
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 0%

---

# Overzicht van geleide analyse

De geleide analyse is een rapporteringsformaat dat productteams toestaat om hun gegevensbehoeften snel zelf-te dienen zodat zij high-quality inzicht snel kunnen krijgen en meer gegeven-gedreven productbesluiten kunnen nemen. Interfunctionele teams kunnen in real time verbinding maken om deze rapporten te gebruiken en te begrijpen.

Net als Analysis Workspace en Mobile-scorecards gebruikt een analyserapport met instructies gegevens van een [Gegevens, weergave](../data-views/data-views.md), die verwijst naar gegevens in Adobe Experience Platform via een [Verbinding](../connections/overview.md). Alle rapporten die zijn gemaakt in de analyse met instructies kunnen naadloos worden overgedragen naar Analysis Workspace voor aanvullend onderzoek.

De geleide analyse verstrekt veelvoudige manieren om gegevens te analyseren en te bekijken. Weergavetypen kunnen dezelfde gegevens op verschillende manieren weergeven, wat leidt tot verschillende inzichten met dezelfde gebeurtenissen en segmenten. U krijgt verschillende vraagrails en visualisatie montages afhankelijk van de mening die u kiest. U kunt vrij tussen meningen schakelen, en om het even welke toepasselijke vraagspoorcomponenten dragen over als de mening hen steunt.

De geleide analyse categoriseert meningstypes in **Typen analyses**. De volgende analyse- en weergavetypen zijn beschikbaar:

| Type analyse | Type weergave | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Impact] | [Geen](types/release.md) | Vergelijk de prestaties in gelijke perioden vóór en na de release. |
| [!UICONTROL Impact] | [Eerste gebruik](types/first-use.md) | Meet het effect van het gebruik van de eerste functie op sleutelindicatoren. |
| [!UICONTROL Funnel] | [Wrijving](types/friction.md) | Vergelijk de conversiesnelheden tussen de stappen. |
| [!UICONTROL Funnel] | [Conversietrends](types/conversion-trends.md) | Wijzigingen in conversietarieven bijhouden in de loop van de tijd. |
| [!UICONTROL User growth] | [Actief](types/active.md) | Identificeer wie nieuw, behouden, terugkeren, of slapend is. |
| [!UICONTROL Net growth] | [Netto groei](types/net-growth.md) | Wint of verliest u gebruikers? |
| [!UICONTROL Trends] | [Gebruik](types/usage.md) | Meet de betrokkenheid van de gebruiker in de loop van de tijd. |

{style="table-layout:auto"}

## Toegang

Als uw organisatie is ingericht voor geleide analyse, kunt u tot het van de homepage van de Customer Journey Analytics toegang hebben.

1. Klikken **[!UICONTROL Guided analysis]** van de startpagina om rechtstreeks naar de [Weergave trends gebruiken](types/usage.md).

   ![Landingspagina-element](assets/landing-page-tile.png)

1. Klikken **[!UICONTROL Create new]** om de verschillende weergaveopties weer te geven en een ander beginpunt voor de analyse te kiezen.

   ![Een nieuw modaal model maken](assets/create-new-modal.png)

## Interface

De interface voor Analyse met instructies, ongeacht het type analyse, bestaat uit de volgende hoofdelementen van de gebruikersinterface:

| Interfacevoorvertoning | UI-element | Beschrijving |
| --- | --- | --- |
| ![Query-rail](assets/query-rail.png) | Query-rail | Vorm de gewenste componenten (gebeurtenissen, eigenschappen, en segmenten) die omhoog een analyse maken. Elk analysetype dwingt verschillende grenzen aan het aantal gebeurtenissen en segmenten af die u kunt vormen. Als u op een nieuw analysetype schakelt, worden uw vraagselecties gehandhaafd binnen de toegestane grenzen voor dat analysetype. |
| ![Diagram](assets/chart.png) | Diagram | Een visualisatie van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Welke visualisatie u ziet hangt van de mening en de montages boven de grafiek af. De beschikbare meningen hangen van het analysetype boven vraagspoor af. Het diagram bevat ook: <ul><li>**Knopinfo**: Houd de muisaanwijzer boven een gegevenspunt van een diagram om knopinfo met meer informatie weer te geven.</li><li>**Legenda**: Houd de cursor boven de legenda van het diagram om reeksdefinities beschikbaar te maken, indien beschikbaar.</li><li>**Handelingen klikken**: Maak beschikbare volgende acties zichtbaar door op een gegevenspunt te klikken. Opties omvatten **Segment opslaan**.</li></ul> |
| ![Tabel](assets/table.png) | Tabel | Een tabelweergave van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Kolommen in de tabel zijn afhankelijk van het weergavetype boven het diagram. De beschikbare meningen hangen van het analysetype boven vraagspoor af. De tabel bevat ook: <ul><li>**Handelingen klikken**: Beschikbare volgende handelingen weergeven door op de knop **[!UICONTROL More]** -menu. Opties omvatten **Segment opslaan**.</li></ul> |
| ![Visualisatie-instellingen](assets/visualization-settings.png) | Visualisatie-instellingen | Verscheidene opties boven de grafiek die u toestaan om aan te passen hoe de grafiek en de lijst gegevens terugkeren.<ul><li>**Type weergave**: Een keuzelijst waarmee u gegevens voor een bepaald analysetype op een andere manier kunt presenteren.</li><li>**Diagraminstellingen**: Perfectioneer wat uw grafiek en lijstvertoning. Welke opties beschikbaar zijn, is afhankelijk van de geselecteerde weergave.</li><li>**Datumbereik**: Een kalenderkiezer waarmee u het datumbereik van de analyse kunt bepalen. U kunt ook een interval selecteren voor georiënteerde weergaven, zoals dag, week of maand.</li><li>**Inzichten**: Contextuele inzichten afhankelijk van de analyse u bekijkt. Met de pijlen kunt u extra inzichten weergeven of verbergen met het gloeilamppictogram rechtsboven.</li></ul> |
| ![Menu](assets/menu.png) | Menu | Opdrachten in de rechterbovenhoek van de analyse met instructies bieden overkoepelende acties voor uw analyse.<ul><li>**Selector gegevensweergave**: Wijzig de gegevensweergave die in de analyse wordt gebruikt. Wanneer u de gegevensmening verandert, veranderen de beschikbare componenten in vraagspoor ook.</li><li>**Opslaan**: Hiermee slaat u de analyse op. Als u een nieuwe analyse opslaat, verschijnt een modaal venster dat om een naam en een beschrijving verzoekt.</li><li>**Opslaan als**: Hiermee slaat u de analyse los van de huidige analyse op en maakt u een kopie. Er wordt een modaal venster weergegeven met een nieuwe naam en beschrijving.</li><li>**Openen in werkruimte**: Herstelt de huidige analyse met instructies in Analysis Workspace. Het project Workspace wordt op een nieuw tabblad gemaakt, zodat onderbreking wordt voorkomen tijdens het werken in de analyse Met instructies. Het is een kopie van de analyse en blijft niet synchroon met de oorspronkelijke geleide analyse als deze eenmaal is geopend. Gebruik deze opdracht als u de gegevens naar het analyseteam wilt verplaatsen of dieper wilt duiken in de gegevens dan in de analyse met instructies is toegestaan.</li><li>**Kopiëren naar klembord**: Hiermee kopieert u de diagramafbeelding naar het klembord, die u in andere toepassingen wilt plakken. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**PNG downloaden**: Hiermee downloadt u de diagramafbeelding als een `.png`. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**CSV downloaden**: Hiermee worden de tabelgegevens gedownload als een `.csv`. De queryrail en -grafiek worden niet in het bestand opgenomen.</li></ul> |

{style="table-layout:auto"}

## Inrichting

Analyse met instructies maakt deel uit van Adobe Product Analytics, dat een betaalde aanvulling op Customer Journey Analytics is. Neem contact op met het accountteam van uw Adobe als uw organisatie deze reeks mogelijkheden wil gaan gebruiken.

Als uw organisatie is ingericht voor de analyse met instructies, kunnen beheerders van productprofielen er toegang toe toevoegen of verwijderen in de Adobe Admin Console.

1. Aanmelden bij de [Adobe Admin Console](https://adminconsole.adobe.com).
1. Selecteren **[!UICONTROL Customer Journey Analytics]** in de lijst van producten.
1. Selecteer het gewenste productprofiel voor de machtigingen die u wilt bewerken.
1. Klik op de knop **[!UICONTROL Permissions]** tab, en klik vervolgens op **[!UICONTROL Edit]** krachtens [!UICONTROL Reporting Tools].
1. Klik op het plusteken naast **[!UICONTROL Guided Analysis Access]** in de lijst van [!UICONTROL Available Permission Items], die het aan de lijst van [!UICONTROL Included Permission Items].
1. Klik op **[!UICONTROL Save]**.

>[!TIP]
>
>Sommige beheerders schakelen de analyse met instructies liever in en schakelen Analysis Workspace voor nieuwe gebruikers uit om te Customer Journey Analytics. Als deze gebruikers klaar zijn met het product en uw organisatorische gegevens, kunt u vervolgens toegang tot Analysis Workspace inschakelen.
