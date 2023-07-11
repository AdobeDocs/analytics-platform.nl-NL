---
title: Overzicht van geleide analyse
description: Een methode om gegevens in Customer Journey Analytics te analyseren die productteams gemakkelijk rapporten en inzichten laat produceren.
exl-id: 6a8a92db-f030-424e-af9b-f8f6502084f6
feature: Guided Analysis
source-git-commit: f48d17cf975ce7d069ac90f9685b96669a29eaff
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 0%

---

# Overzicht van geleide analyse

{{release-limited-testing}}

De geleide analyse is een rapporteringsformaat dat productteams toestaat om hun gegevensbehoeften snel zelf-te dienen zodat zij meer gegeven-gedreven productbesluiten kunnen nemen. Interfunctionele teams kunnen in real time verbinding maken om deze rapporten te gebruiken en te begrijpen.

Net als Analysis Workspace en Mobile-scorecards gebruikt een analyserapport met instructies gegevens van een [Gegevens, weergave](../data-views/data-views.md), die verwijst naar gegevens in Adobe Experience Platform via een [Verbinding](../connections/overview.md). Alle rapporten die zijn gemaakt in de analyse met instructies kunnen naadloos worden overgedragen naar Analysis Workspace voor aanvullend onderzoek.

Met instructies kunt u gegevens op verschillende manieren analyseren. Deze weergavetypen kunnen dezelfde gegevens op verschillende manieren weergeven, wat leidt tot verschillende inzichten met dezelfde gebeurtenissen en segmenten. U krijgt verschillende vraagrails en visualisatieopties afhankelijk van het meningstype dat u kiest. U kunt vrij schakelen tussen meningstypes, en om het even welke toepasselijke componenten van vraagspoorwegen dragen over als het meningstype hen steunt.

De geleide analyse categoriseert meningstypes in **Typen analyses**. De volgende analyse- en weergavetypen zijn beschikbaar:

| Type analyse | Type weergave | Beschrijving |
| --- | --- | --- |
| Gevolgen | [Geen](types/release.md) | Vergelijk de prestaties in gelijke perioden vóór en na de release. |
| Gevolgen | [Eerste gebruik](types/first-use.md) | Meet het effect van het gebruik van de eerste functie op sleutelindicatoren. |
| Trechter | [Wrijving](types/friction.md) | Vergelijk de conversiesnelheden tussen de stappen. |
| Trechter | [Conversietrends](types/conversion-trends.md) | Wijzigingen in conversietarieven bijhouden in de loop van de tijd. |
| Groei van gebruikers | [Actief](types/active.md) | Meet de groei van uw gebruikersbasis. |
| Groei van gebruikers | [Netto groei](types/net-growth.md) | Winsten en verliezen van gebruikers in balans brengen. |
| Trends | [Gebruik](types/usage.md) | Meet de betrokkenheid van de gebruiker in de loop van de tijd. |

{style="table-layout:auto"}

## Interface

De interface voor Analyse met instructies, ongeacht het type analyse, bestaat uit de volgende hoofdelementen van de gebruikersinterface:

1. **Query-rail**: Gebruik deze rail links om uw analyse uit te bouwen.
1. **Diagram**: Zodra u de gewenste gebeurtenissen, mensen, of stappen selecteert, wordt een grafiek getoond op het recht die de gegevens visualiseert.
1. **Tabel**: Een tabel onder het diagram waarin de getallen worden weergegeven die in de visualisatie worden gebruikt.
1. **Instellingen en inzichten**: Verschillende UI-elementen boven het diagram waarmee u de geretourneerde gegevens kunt aanpassen.

[Screenshot van UI]

De geleide analyse bevat de volgende interfacedelen:

| Interfacevoorvertoning | UI-element | Beschrijving |
| --- | --- | --- |
| [Schermafbeelding van queryrails] | Query-rail | Vorm de gewenste componenten die omhoog een rapport maken. De verschillende analysetypen delen verscheidene vraagopties; als twee analystypes vraagopties delen, dragen zij over wanneer het schakelen van analysetypen. |
| [Schermafbeelding van diagram] | Diagram | Een visualisatie van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Welke visualisatie u ziet hangt van het meningstype boven de grafiek af. De beschikbare meningstypes hangen van het type van Analyse boven vraagspoor af. |
| [Schermafbeelding van tabel] | Tabel | Een tabelweergave van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Kolommen in de tabel zijn afhankelijk van het weergavetype boven het diagram. De beschikbare meningstypes hangen van het type van Analyse boven vraagspoor af. |
| [Schermafbeelding van instellingen] | Instellingen | Verscheidene opties boven de grafiek die u toestaan om aan te passen hoe de grafiek en de lijst gegevens terugkeren.<ul><li>**Type weergave**: Een drop-down selecteur die u gegevens voor een bepaald type van Analyse op een verschillende manier laat voorstellen. Elk analysetype heeft minstens twee meningstypes.</li><li>**Diagraminstellingen**: Stel nauwkeurig in hoe uw diagram eruitziet en welke gebeurtenissen u wilt gebruiken. Welke opties beschikbaar zijn, is afhankelijk van het geselecteerde weergavetype.</li><li>**Datumbereik**: Een kalenderkiezer die u toestaat om de datumwaaier van het rapport te bepalen. Sommige analysetypen staan ook intervallen toe, zoals dagelijks, wekelijks of maandelijks.</li><li>**Inzichten**: Verstrekt contextuele inzichten afhankelijk van het rapport dat u bekijkt. U kunt deze inzichten tonen of verbergen gebruikend het gloeilamppictogram in het hoogste recht.</li></ul> |
| [Screenshot van het analysemenu] | Menu Analyse | Opdrachten in de rechterbovenhoek van de analyse met instructies die overkoepelende acties bieden.<ul><li>**Selector gegevensweergave**: Wijzig de gegevensweergave die in deze analyse wordt gebruikt. Wanneer u de gegevensmening verandert, veranderen de beschikbare componenten in vraagspoor ook.</li><li>**Opslaan**: Hiermee slaat u de analyse op. Als u een nieuwe analyse opslaat, verschijnt een modaal venster dat om een naam en een beschrijving verzoekt.</li><li>**Opslaan als**: Hiermee slaat u de analyse los van de huidige analyse op en maakt u een kopie. Er wordt een modaal venster weergegeven met een nieuwe naam en beschrijving.</li><li>**Openen in werkruimte**: Herstelt de huidige analyse met instructies in Analysis Workspace. Het project Workspace wordt op een nieuw tabblad gemaakt, zodat onderbreking wordt voorkomen tijdens het werken in de analyse Met instructies. Gebruik deze opdracht wanneer de analyse met instructies u niet de flexibiliteit of het specifieke inzicht geeft die u zoekt. U wilt bijvoorbeeld een [Gebruik](types/usage.md) rapport dat Zittingen voor één segment, en Mensen voor een ander segment gebruikt.</li><li>**PNG downloaden**: Hiermee downloadt u de diagramafbeelding als een `.png`. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li><li>**SVG downloaden**: Hiermee downloadt u de diagramafbeelding als een `.svg`. De queryrail en -tabel worden niet in de afbeelding opgenomen.</li></ul> |

{style="table-layout:auto"}

## Inrichting

Analyse met instructies maakt deel uit van Adobe Product Analytics, dat een betaalde aanvulling op Customer Journey Analytics is. Neem contact op met het accountteam van Adobe als uw organisatie deze functie wil gaan gebruiken.

Zodra uw organisatie is ingericht voor de analyse met instructies, kunnen beheerders van productprofielen er toegang toe verlenen in de Adobe Admin Console.

1. Aanmelden bij de [Adobe-beheerconsole](https://adminconsole.adobe.com).
1. Selecteren **[!UICONTROL Customer Journey Analytics]** in de lijst van producten.
1. Selecteer het gewenste productprofiel om machtigingen te bewerken.
1. Klik op de knop **[!UICONTROL Permissions]** tab, en klik vervolgens op **[!UICONTROL Edit]** krachtens [!UICONTROL Reporting Tools].
1. Klik op het plusteken naast **[!UICONTROL Guided Analysis Access]** in de lijst van [!UICONTROL Available Permission Items] om het aan de lijst van [!UICONTROL Included Permission Items].
1. Klik op **[!UICONTROL Save]**.
