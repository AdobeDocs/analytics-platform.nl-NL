---
title: Deelvenster voor attributie
description: Het toewijzingspaneel in Analysis Workspace gebruiken en interpreteren.
feature: Panels
exl-id: 7fdec05b-5d99-48d1-ac1b-c243cb64e487
source-git-commit: 3f1112ebd2a4dfc881ae6cb7bd858901d2f38d69
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 22%

---

# Deelvenster voor attributie

De [!UICONTROL Attribution] is een gemakkelijke manier om een analyse te maken waarin verschillende attributiemodellen worden vergeleken. Het is een functie die u een specifieke werkruimte biedt voor het gebruik en vergelijken van attributiemodellen.

Customer Journey Analytics verbetert de attributie door u te laten:

* Definitie van attributie die verder gaat dan &#39;paid media&#39;: hiermee kan elke dimensie of gebeurtenis, en elke metric of elk kanaal worden toegepast op modellen (bijvoorbeeld intern zoeken), niet alleen marketingcampagnes.
* Een onbeperkt aantal attributiemodellen vergelijken: vergelijk dynamisch zoveel modellen als u wilt.
* Geen late wijzigingen tijdens de implementatie: met de functies voor verwerking van de rapporttijd en context-bewuste sessies, kan de context van het klanttraject worden ingebouwd voor toepassing tijdens runtime.
* Construeer de sessie die het beste overeenkomt met uw attributiescenario.
* Verdeling van kenmerken door filters: Vergelijk eenvoudig de prestaties van uw marketingkanalen met elk belangrijk filter (bijvoorbeeld Nieuwe of Herhaalde klanten, Product X versus Product Y, Loyalty level of CLV).
* Controle dankzij &#39;channel cross-over&#39; en multi-touchanalyse: gebruik Venn-diagrammen en histogrammen en volg de trends in attributieresultaten.
* Visuele analyse van belangrijke marketingreeksen: werk met visuele methoden die leiden tot conversie, zoals flows voor meerdere knooppunten en uitvalvisualisaties.
* Stel berekende standaarden samen: gebruik een willekeurig aantal toewijzingsmethoden voor attributie.

## Een deelvenster met kenmerken maken

1. Klik op het deelvensterpictogram aan de linkerkant.
1. Sleep de [!UICONTROL Attribution] in uw Analysis Workspace-project.

   ![Nieuw deelvenster voor kenmerken](assets/Attribution_Panel_1.png)

1. Voeg metrisch toe dat u om het even welke afmeting aan attributen wilt kenmerken en toevoegen tegen. Voorbeelden zijn Marketingkanalen of aangepaste afmetingen, zoals interne promoties.

   ![Dimensie en metrisch selecteren](assets/attribution_panel2.png)

1. Selecteer de kenmerken en het terugzoekvenster die u wilt vergelijken.

1. Het deelvenster Kenmerken retourneert een uitgebreide set gegevens en visualisaties die de kenmerk voor de geselecteerde dimensie en de metrische waarde met elkaar vergelijken.

   ![Attributievisualisaties](assets/attr_panel_vizs.png)

## Attributievisualisaties

* **Totaal metrisch**: Het totale aantal omzettingen dat zich tijdens het rapporttijdvenster voordeed. Dit zijn de omzettingen die over de afmeting worden toegeschreven u selecteerde.
* **Vergelijkingsbalk voor kenmerken**: Vergelijkt visueel de toegeschreven omzettingen over elk van de afmetingspunten van uw geselecteerde afmeting. Elke staafkleur vertegenwoordigt een afzonderlijk attributiemodel.
* **Vergelijkingstabel voor kenmerken**: Hiermee worden dezelfde gegevens weergegeven als het staafdiagram, dat als een tabel wordt weergegeven. Wanneer u verschillende kolommen of rijen in deze tabel selecteert, worden het staafdiagram en diverse andere visualisaties in het deelvenster gefilterd. Deze lijst doet gelijkaardig aan een andere Lijst Freeform in Werkruimte - toestaand u om componenten zoals metriek, filters, of onderverdelingen toe te voegen.
* **Diagram overlappen**: Een tekening van Venn die de hoogste drie afmetingspunten toont en hoe vaak zij gezamenlijk aan een omzetting deelnemen. Bijvoorbeeld, wijst de grootte van de bel overlapping erop hoe vaak omzettingen voorkwamen wanneer een persoon aan beide afmetingspunten werd blootgesteld. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Prestatiegegevens**: Hiermee kunt u maximaal drie kenmerkingsmodellen visueel vergelijken met behulp van een spreidingsgrafiek.
* **Trende prestaties**: Toont de trend van toegeschreven omzettingen voor het hoogste afmetingspunt. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Stroom**: Hiermee kunt u zien welke kanalen het meest worden gebruikt, en in welke volgorde op de reis van een persoon.
