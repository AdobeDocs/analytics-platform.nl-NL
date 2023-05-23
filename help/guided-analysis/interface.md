---
title: Interface voor analyse met instructies
description: Leer over de algemene structuur van het Geleide analyseproject UI.
source-git-commit: d73dc0eb1740f28c0cd0b7b64fee86069c402b63
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# De interface van de Analyse van de gids

{{release-limited-testing}}

De interface voor een project van de Analyse met instructies, ongeacht het analysetype, omvat de volgende belangrijkste elementen UI:

* **Query-rail**: Gebruik deze rail links van uw project om uw analyse te bouwen.
* **Diagram**: Zodra u de gewenste gebeurtenissen, mensen, of stappen selecteert, wordt een grafiek getoond op het recht die de gegevens visualiseert.
* **Tabel**: Een tabel onder het diagram waarin de getallen worden weergegeven die in de visualisatie worden gebruikt.
* **Instellingen en inzichten**: Verschillende UI-elementen boven het diagram waarmee u de geretourneerde gegevens kunt aanpassen.

[Screenshot van UI]

## Query-rail

[Schermafbeelding van queryrails]

Het vraagspoor is waar u de gewenste componenten vormt die omhoog een rapport maken. De verschillende analysetypen delen verscheidene vraagopties; als twee analystypes vraagopties delen, dragen zij over wanneer het schakelen van analysetypen. Zie [Typen analyses](analysis-types/overview.md) voor meer informatie over vraagopties voor elk respectieve analysetype.

## Diagram

[Schermafbeelding van diagram]

Een visualisatie van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Welke visualisatie u ziet hangt van het meningstype boven de grafiek af. Welke weergavetypen beschikbaar zijn, is afhankelijk van de [Type analyse](analysis-types/overview.md) boven de queryrail.

## Tabel

[Schermafbeelding van tabel]

Een tabelweergave van de geretourneerde gegevens op basis van uw invoer van de queryregels en -instellingen. Kolommen in de tabel zijn afhankelijk van het weergavetype boven het diagram. Welke weergavetypen beschikbaar zijn, is afhankelijk van de [Type analyse](analysis-types/overview.md) boven de queryrail.

## Instellingen

[Schermafbeelding van instellingen]

Verscheidene opties boven de grafiek die u toestaan om aan te passen hoe de grafiek en de lijst gegevens terugkeren.

* **Type weergave**: Een keuzelijst waarmee u gegevens voor een bepaalde [Type analyse](analysis-types/overview.md) op een andere manier. Elk analysetype heeft minstens twee meningstypes.
* **Diagraminstellingen**: Stel nauwkeurig in hoe uw diagram eruitziet en welke gebeurtenissen u wilt gebruiken. Welke opties beschikbaar zijn, is afhankelijk van het geselecteerde weergavetype.
* **Datumbereik**: Een kalenderkiezer die u toestaat om de datumwaaier van het rapport te bepalen. Sommige analysetypen staan ook intervallen toe, zoals dagelijks, wekelijks of maandelijks.
* **Inzichten**: Verstrekt contextuele inzichten afhankelijk van het rapport dat u bekijkt. U kunt deze inzichten tonen of verbergen gebruikend het gloeilamppictogram in het hoogste recht.

## Het menu Project

[Screenshot van projectmenu]

Opdrachten in de rechterbovenhoek van het project die overkoepelende acties bieden.

* **Selector gegevensweergave**: Wijzig de gegevensweergave die in dit project wordt gebruikt. Wanneer u de gegevensmening verandert, veranderen de beschikbare componenten in vraagspoor ook.
* **Opslaan**: Hiermee slaat u het project op. Als u een nieuw project opslaat, verschijnt een modaal venster dat om een naam en een beschrijving verzoekt.
* **Opslaan als**: Hiermee slaat u het project apart van het huidige project op en maakt u een kopie. Er wordt een modaal venster weergegeven met een nieuwe naam en beschrijving.
* **Openen in werkruimte**: Herstelt het huidige Guided analysis project in Analysis Workspace. Het werkruimteproject wordt gecreeerd op een nieuw lusje, verhinderend onderbreking terwijl het werken aan uw Geleide analyseproject. Gebruik dit bevel wanneer de Geleide Analyse u niet behoorlijk de flexibiliteit of het specifieke inzicht geeft dat u zoekt. U wilt bijvoorbeeld een [Trends](analysis-types/trends.md) rapport dat Zittingen voor één segment, en Mensen voor een ander segment gebruikt.
* **PNG downloaden**: Hiermee downloadt u de diagramafbeelding als een `.png`. De queryrail en -tabel worden niet in de afbeelding opgenomen.
* **SVG downloaden**: Hiermee downloadt u de diagramafbeelding als een `.svg`. De queryrail en -tabel worden niet in de afbeelding opgenomen.
