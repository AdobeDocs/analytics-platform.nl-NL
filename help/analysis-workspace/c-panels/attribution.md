---
title: Kenmerk, deelvenster
description: Het toewijzingspaneel in Analysis Workspace gebruiken en interpreteren.
feature: Panels
exl-id: 7fdec05b-5d99-48d1-ac1b-c243cb64e487
role: User
source-git-commit: 4ed05334a3866ec784901d273fcb13bd24b2d449
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 16%

---

# Kenmerk, deelvenster {#attribution-panel}

>[!CONTEXTUALHELP]
>id="cja_workspace_attribution"
>title="Attributie"
>abstract="Vergelijk en visualiseer snel om het even welk aantal attributiemodellen gebruikend om het even welke afmeting en omzettingsmetrisch"
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Deelvenster Attribution IQ"


De [!UICONTROL Attribution] is een gemakkelijke manier om een analyse te maken waarin verschillende attributiemodellen worden vergeleken. Het is een functie die u een specifieke werkruimte biedt voor het gebruik en vergelijken van attributiemodellen.

Customer Journey Analytics verbetert de attributie door u te laten:

* Definitie van attributie die verder gaat dan &#39;paid media&#39;: hiermee kan elke dimensie of gebeurtenis, en elke metric of elk kanaal worden toegepast op modellen (bijvoorbeeld intern zoeken), niet alleen marketingcampagnes.
* Een onbeperkt aantal attributiemodellen vergelijken: vergelijk dynamisch zoveel modellen als u wilt.
* Vermijd implementatieveranderingen: Met rapport-tijd verwerking en context-bewuste zittingen, kan de context van de klantenreis binnen worden gebouwd en bij runtime worden toegepast.
* Construeer de sessie die het beste overeenkomt met uw attributiescenario.
* Verdeling van kenmerken naar filters: vergelijk eenvoudig de prestaties van uw marketingkanalen over een belangrijk filter (bijvoorbeeld Nieuwe klanten vs. klanten herhalen, product X vs. product Y, Loyalty level of CLV).
* Controle dankzij &#39;channel cross-over&#39; en multi-touchanalyse: gebruik Venn-diagrammen en histogrammen en volg de trends in attributieresultaten.
* Visuele analyse van belangrijke marketingreeksen: werk met visuele methoden die leiden tot conversie, zoals flows voor meerdere knooppunten en uitvalvisualisaties.
* Stel berekende standaarden samen: gebruik een willekeurig aantal toewijzingsmethoden voor attributie.

## Een deelvenster met kenmerken maken

1. Klik op het deelvensterpictogram aan de linkerkant.
1. Sleep de [!UICONTROL Attribution] in uw Analysis Workspace-project.

   ![Het venster Nieuw project markeert het deelvenster Kenmerken.](assets/Attribution_Panel_1.png)

1. Voeg metrisch toe dat u om het even welke afmeting aan attributen wilt kenmerken en toevoegen tegen. Voorbeelden zijn Marketingkanalen of aangepaste afmetingen, zoals interne promoties.

   ![Het venster van het deelvenster Kenmerken dat verschillende geselecteerde afmetingen en metriek toont.](assets/attribution_panel2.png)

1. Selecteer de kenmerken en het terugzoekvenster die u wilt vergelijken.

1. Het deelvenster Kenmerken retourneert een uitgebreide set gegevens en visualisaties die de kenmerk voor de geselecteerde dimensie en metrisch vergelijken.

   ![De visualisaties in het deelvenster Kenmerken die geselecteerde metriek en dimensies vergelijken.](assets/attr_panel_vizs.png)

## Attributievisualisaties

* **Totaal metrisch**: Het totale aantal conversies dat zich tijdens het rapportagetijdvenster heeft voorgedaan. Dit zijn de omzettingen die over de afmeting worden toegeschreven u selecteerde.
* **Vergelijkingsbalk voor kenmerken**: Vergelijkt visueel de toegeschreven omzettingen over elk van de afmetingspunten van uw geselecteerde afmeting. Elke staafkleur vertegenwoordigt een afzonderlijk attributiemodel.
* **Vergelijkingstabel voor kenmerken**: Hiermee geeft u dezelfde gegevens weer als het staafdiagram, dat als een tabel wordt weergegeven. Wanneer u verschillende kolommen of rijen in deze tabel selecteert, worden het staafdiagram en diverse andere visualisaties in het deelvenster gefilterd. Deze tabel werkt op dezelfde manier als elke andere Freeform-tabel in Workspace, zodat u componenten kunt toevoegen, zoals metriek, filters of indelingen.
* **Diagram overlappen**: Een tekening van Venn die de hoogste drie afmetingspunten toont en hoe vaak zij gezamenlijk aan een omzetting deelnemen. Bijvoorbeeld, wijst de grootte van de bel overlapping erop hoe vaak omzettingen voorkwamen wanneer een persoon aan beide afmetingspunten werd blootgesteld. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Prestatiegegevens**: Hiermee kunt u maximaal drie kenmerkmodellen visueel vergelijken met een spreidingsperceel.
* **Trende prestaties**: Geeft de trend weer van toegewezen omzettingen voor het bovenste dimensie-item. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Stroom**: Hiermee kunt u zien welke kanalen het meest worden gebruikt en in welke volgorde op de reis van een persoon.
