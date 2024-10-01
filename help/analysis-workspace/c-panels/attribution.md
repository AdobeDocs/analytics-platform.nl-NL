---
title: Kenmerk, deelvenster
description: Het toewijzingspaneel in Analysis Workspace gebruiken en interpreteren.
feature: Panels
exl-id: 7fdec05b-5d99-48d1-ac1b-c243cb64e487
role: User
source-git-commit: 5b441472a21db99728d012c19f12d98f984086f5
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 8%

---

# Kenmerk, deelvenster {#attribution-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_workspace_attribution_button"
>title="Attributie"
>abstract="Vergelijk en visualiseer snel om het even welk aantal attributiemodellen gebruikend om het even welke afmeting en omzettingsmetrisch"
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Deelvenster Attribution IQ"

>[!CONTEXTUALHELP]
>id="cja_workspace_attribution_panel"
>title="Kenmerk, deelvenster"
>abstract="Vergelijk en visualiseer snel om het even welk aantal attributiemodellen gebruikend om het even welke afmeting en omzettingsmetrisch.<br/><br/>**Parameters **<br/>**Kanaal**<br/> de afmeting tegen attributen. Deze dimensie kan afzetkanalen, campagnes, of een andere dimensie zijn.<br/>**Modellen**<br/> het model bepaalt hoe het krediet aan touchpoints wordt toegewezen.<br/>**venster van de Lookback**<br/> Dit het plaatsen bepaalt het venster van gegevensattributie dat op elke omzetting van toepassing is."
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Deelvenster Attribution IQ"

<!-- markdownlint-enable MD034 -->


Het deelvenster **[!UICONTROL Attribution]** is een eenvoudige manier om een analyse te maken waarin verschillende attributiemodellen worden vergeleken. In het deelvenster vindt u een speciale werkruimte voor het gebruik en vergelijken van attributiemodellen.

Customer Journey Analytics verbetert de attributie door u te laten:

* Bepaal attributie voorbij betaalde media: Om het even welke afmeting, metrisch, kanaal of gebeurtenis kan op modellen (bijvoorbeeld, intern onderzoek) worden toegepast, niet alleen marketing campagnes.
* Gebruik een onbeperkte vergelijkingsmodelvergelijking: vergelijk dynamisch zoveel modellen als u wilt.
* Vermijd implementatieveranderingen: Met rapport-tijd verwerking en context-bewuste zittingen, kan de context van de klantenreis binnen worden gebouwd en bij runtime worden toegepast.
* Construeer de sessie die het beste overeenkomt met uw attributiescenario.
* Verdeling naar filters: vergelijk eenvoudig de prestaties van uw marketingkanalen met elk belangrijk filter (bijvoorbeeld New versus Repeat-klanten, Product X versus Product Y, Loyalty level of CLV).
* Controle dankzij &#39;channel cross-over&#39; en multi-touchanalyse: gebruik Venn-diagrammen en histogrammen en volg de trends in attributieresultaten.
* Visuele analyse van belangrijke marketingreeksen: werk met visuele methoden die leiden tot conversie, zoals flows voor meerdere knooppunten en uitvalvisualisaties.
* Stel berekende standaarden samen: gebruik een willekeurig aantal toewijzingsmethoden voor attributie.

## Gebruiken

Een deelvenster **[!UICONTROL Attribution]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Attribution]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [ een paneel ](panels.md#create-a-panel) creëren.

1. Specificeer de [ input ](#panel-input) voor het paneel.

1. Neem de [ output ](#panel-output) voor het paneel waar.

### Deelvensterinvoer

U kunt het deelvenster Kenmerken configureren met de volgende invoerinstellingen:

1. Voeg een **[!UICONTROL Success metric]** en een dimensie van **[!UICONTROL Channel]** toe waarop u het kenmerk wilt toepassen. Voorbeelden zijn Marketingkanalen of aangepaste afmetingen, zoals interne promoties.

   ![ het het paneelvenster van de Attributie dat verscheidene geselecteerde afmetingen en metriek toont.](assets/attribution-panel.png)

1. Selecteer één of meerdere [ attributiemodellen ](#attribution-models) van **[!UICONTROL Included models]** en a [ raadplegingsvenster ](#lookback-window) van **[!UICONTROL Lookback window]** dat u voor vergelijking wilt gebruiken.

1. Selecteer **[!UICONTROL Build]** om de visualisaties in het deelvenster samen te stellen.

### Deelvensteruitvoer

Het deelvenster **[!UICONTROL Attribution]** retourneert een uitgebreide set gegevens en visualisaties die de kenmerk voor de geselecteerde dimensie en de metrische waarde met elkaar vergelijken.

![ het paneel van de Attributie visualisaties die geselecteerde metriek en dimensies vergelijken.](assets/attr_panel_vizs.png)

### Attributievisualisaties

De volgende visualisatie maakt deel uit van de paneeluitvoer.

* **Totaal metrisch**: Het totale aantal omzettingen die over het rapporteringstijdvenster voorkwamen, en aan de afmeting worden toegeschreven u selecteerde.
* **de Vergelijkingsbar van de Attributie**: Vergelijkt visueel de toegeschreven omzettingen over elk van de afmetingspunten van uw geselecteerde afmeting. Elke staafkleur vertegenwoordigt een afzonderlijk attributiemodel.
* **Lijst van de Vergelijking van de Attributie**: Toont de zelfde gegevens zoals het staafdiagram, dat als lijst wordt vertegenwoordigd. Wanneer u verschillende kolommen of rijen in deze tabel selecteert, worden het staafdiagram en diverse andere visualisaties in het deelvenster gefilterd. Deze tabel werkt op dezelfde manier als elke andere Freeform-tabel in Workspace, zodat u componenten kunt toevoegen, zoals metriek, filters of indelingen.
* **Overlap Diagram**: Een beeld die van de Venn de hoogste drie afmetingspunten toont en hoe vaak zij gezamenlijk aan een omzetting deelnemen. Bijvoorbeeld, wijst de grootte van de bel overlapping erop hoe vaak omzettingen voorkwamen wanneer een persoon aan beide afmetingspunten werd blootgesteld. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Detail van Prestaties**: Een spreidingsvisualisatie om tot drie attributiemodellen visueel te vergelijken.
* **Getweende Prestaties**: Toont de trend van toegeschreven omzettingen voor het hoogste afmetingspunt. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Stroom**: Laat u zien welke kanalen met het meest algemeen in wisselwerking staan, en in welke orde over de reis van een persoon.

## Attributiemodellen

{{attribution-models-details}}

## Venster Opzoeken

{{attribution-lookback-window}}

>[!MORELIKETHIS]
>
> [ creeer een paneel ](/help/analysis-workspace/c-panels/panels.md#create-a-panel)
>
