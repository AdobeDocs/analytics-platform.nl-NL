---
title: Kenmerk, deelvenster
description: Het toewijzingspaneel in Analysis Workspace gebruiken en interpreteren.
feature: Panels
exl-id: 7fdec05b-5d99-48d1-ac1b-c243cb64e487
role: User
source-git-commit: c89a28323c9d40a7265cd22994a0d1c484f4c7ee
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 14%

---

# Kenmerk, deelvenster {#attribution-panel}

>[!CONTEXTUALHELP]
>id="cja_workspace_attribution_button"
>title="Attributie"
>abstract="Vergelijk en visualiseer snel om het even welk aantal attributiemodellen gebruikend om het even welke afmeting en omzettingsmetrisch"
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Deelvenster Attribution IQ"

>[!CONTEXTUALHELP]
>id="cja_workspace_attribution_panel"
>title="Kenmerk, deelvenster"
>abstract="Vergelijk en visualiseer snel om het even welk aantal attributiemodellen gebruikend om het even welke afmeting en omzettingsmetrisch.<br/><br/>**Parameters **<br/>**Kanaal**<br/> de afmeting tegen attributen. Dit kunnen marketingkanalen, campagnes of andere dimensies zijn.<br/>**Modellen**<br/> het model bepaalt hoe het krediet aan touchpoints wordt toegewezen.<br/>**venster van de Lookback**<br/> Dit het plaatsen bepaalt het venster van gegevensattributie dat op voor elke omzetting zal worden toegepast."
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Deelvenster Attribution IQ"


Het deelvenster [!UICONTROL Attribution] is een eenvoudige manier om een analyse te maken waarin verschillende attributiemodellen worden vergeleken. Het is een functie die u een specifieke werkruimte biedt voor het gebruik en vergelijken van attributiemodellen.

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
1. Sleep het deelvenster [!UICONTROL Attribution] naar uw Analysis Workspace-project.

   ![ het Nieuwe venster van het Project dat het paneel van de Attributie benadrukt.](assets/Attribution_Panel_1.png)

1. Voeg metrisch toe dat u om het even welke afmeting aan attributen wilt kenmerken en toevoegen tegen. Voorbeelden zijn Marketingkanalen of aangepaste afmetingen, zoals interne promoties.

   ![ het het paneelvenster van de Attributie dat verscheidene geselecteerde afmetingen en metriek toont.](assets/attribution_panel2.png)

1. Selecteer de kenmerken en het terugzoekvenster die u wilt vergelijken.

1. Het deelvenster Kenmerken retourneert een uitgebreide set gegevens en visualisaties die de kenmerk voor de geselecteerde dimensie en metrisch vergelijken.

   ![ het paneel van de Attributie visualisaties die geselecteerde metriek en dimensies vergelijken.](assets/attr_panel_vizs.png)

## Attributievisualisaties

* **Totaal metrisch**: Het totale aantal omzettingen die over het rapporteringstijdvenster voorkwamen. Dit zijn de omzettingen die over de afmeting worden toegeschreven u selecteerde.
* **de Vergelijkingsbar van de Attributie**: Vergelijkt visueel de toegeschreven omzettingen over elk van de afmetingspunten van uw geselecteerde afmeting. Elke staafkleur vertegenwoordigt een afzonderlijk attributiemodel.
* **Lijst van de Vergelijking van de Attributie**: Toont de zelfde gegevens zoals het staafdiagram, dat als lijst wordt vertegenwoordigd. Wanneer u verschillende kolommen of rijen in deze tabel selecteert, worden het staafdiagram en diverse andere visualisaties in het deelvenster gefilterd. Deze tabel werkt op dezelfde manier als elke andere Freeform-tabel in Workspace, zodat u componenten kunt toevoegen, zoals metriek, filters of indelingen.
* **Overlap Diagram**: Een Diagram van de Plaats die de hoogste drie afmetingspunten tonen en hoe vaak zij gezamenlijk aan een omzetting deelnemen. Bijvoorbeeld, wijst de grootte van de bel overlapping erop hoe vaak omzettingen voorkwamen wanneer een persoon aan beide afmetingspunten werd blootgesteld. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Detail van Prestaties**: Laat u tot drie attributiemodellen vergelijken visueel gebruikend een verstrooiingsperceel.
* **Getweende Prestaties**: Toont de trend van toegeschreven omzettingen voor het hoogste afmetingspunt. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Stroom**: Laat u zien welke kanalen met het meest algemeen in wisselwerking staan, en in welke orde over de reis van een persoon.
