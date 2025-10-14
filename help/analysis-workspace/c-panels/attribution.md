---
title: Deelvenster Kenmerken
description: Leer hoe u het deelvenster Kenmerken in Analysis Workspace kunt gebruiken en interpreteren.
feature: Panels
exl-id: 7fdec05b-5d99-48d1-ac1b-c243cb64e487
role: User
source-git-commit: ce4a21b1a1e89f14316a92fbdce38281db61e666
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 8%

---

# Kenmerk, deelvenster {#attribution-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_attribution_button"
>title="Attributie"
>abstract="Vergelijk en visualiseer snel om het even welk aantal attributiemodellen gebruikend succes metrisch, kanaal en raadplegingsvenster."
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Attribution IQ-deelvenster"

>[!CONTEXTUALHELP]
>id="workspace_attribution_panel"
>title="Kenmerk, deelvenster"
>abstract="Vergelijk en visualiseer snel om het even welk aantal attributiemodellen voor een succes metrisch. Selecteer het kanaal (afmetingen), de modellen om en het terugkijkvenster op te nemen."
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Attribution IQ-deelvenster"

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

_Dit artikel documenteert het paneel van de Attributie in_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**&#x200B;_.<br/>_zie [&#x200B; het paneel van de Attributie &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/panels/attribution) voor_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics** versie van dit artikel._

>[!ENDSHADEBOX]

Het deelvenster **[!UICONTROL Attribution]** is een eenvoudige manier om een analyse te maken waarin verschillende attributiemodellen worden vergeleken. In het deelvenster vindt u een speciale werkruimte voor het gebruik en vergelijken van attributiemodellen.

Customer Journey Analytics verbetert de attributie door het volgende te laten:

* Bepaal attributie voorbij betaalde media: Om het even welke afmeting, metrisch, kanaal of gebeurtenis kan op modellen (bijvoorbeeld, intern onderzoek) worden toegepast, niet alleen marketing campagnes.
* Gebruik een onbeperkte vergelijkingsmodelvergelijking: vergelijk dynamisch zoveel modellen als u wilt.
* Vermijd implementatieveranderingen: Met rapport-tijd verwerking en context-bewuste zittingen, kan de context van de klantenreis binnen worden gebouwd en bij runtime worden toegepast.
* Construeer de sessie die het beste overeenkomt met uw attributiescenario.
* Uitsplitsing naar kenmerk per segment: vergelijk eenvoudig de prestaties van uw marketingkanalen voor elk belangrijk segment (bijvoorbeeld New vs. Repeat-klanten, Product X versus Product Y, Loyalty level of CLV).
* Controle dankzij &#39;channel cross-over&#39; en multi-touchanalyse: gebruik Venn-diagrammen en histogrammen en volg de trends in attributieresultaten.
* Visuele analyse van belangrijke marketingreeksen: werk met visuele methoden die leiden tot conversie, zoals flows voor meerdere knooppunten en uitvalvisualisaties.
* Stel berekende standaarden samen: gebruik een willekeurig aantal toewijzingsmethoden voor attributie.

## Gebruiken

Een deelvenster **[!UICONTROL Attribution]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Attribution]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [&#x200B; een paneel &#x200B;](panels.md#create-a-panel) creëren.

1. Specificeer de [&#x200B; input &#x200B;](#panel-input) voor het paneel.

1. Neem de [&#x200B; output &#x200B;](#panel-output) voor het paneel waar.

### Deelvensterinvoer

U kunt het deelvenster Kenmerken configureren met de volgende invoerinstellingen:

1. Voeg een **[!UICONTROL Success metric]** en een dimensie van **[!UICONTROL Channel]** toe waarop u het kenmerk wilt toepassen. Voorbeelden zijn Marketingkanalen of aangepaste afmetingen, zoals interne promoties.

   ![&#x200B; het het paneelvenster van de Attributie dat verscheidene geselecteerde afmetingen en metriek toont.](assets/attribution-panel.png)

1. Selecteer één of meerdere [&#x200B; attributiemodellen &#x200B;](#attribution-models) van **[!UICONTROL Included models]**, de [&#x200B; container &#x200B;](#container) van **[!UICONTROL Container]**, en a [&#x200B; raadplegingsvenster &#x200B;](#lookback-window) van **[!UICONTROL Lookback window]** dat u voor vergelijking wilt gebruiken.

1. Selecteer **[!UICONTROL Build]** om de visualisaties in het deelvenster samen te stellen.

### Deelvensteruitvoer

Het deelvenster **[!UICONTROL Attribution]** retourneert een uitgebreide set gegevens en visualisaties die de kenmerk voor de geselecteerde dimensie en de metrische waarde met elkaar vergelijken.

![&#x200B; het paneel van de Attributie visualisaties die geselecteerde metriek en dimensies vergelijken.](assets/attr_panel_vizs.png)

### Attributievisualisaties

De volgende visualisatie maakt deel uit van de paneeluitvoer.

* **Totaal metrisch**: Het totale aantal omzettingen die over het rapporteringstijdvenster voorkwamen, en aan de afmeting worden toegeschreven u selecteerde.
* **de Vergelijkingsbar van de Attributie**: Vergelijkt visueel de toegeschreven omzettingen over elk van de afmetingspunten van uw geselecteerde afmeting. Elke staafkleur vertegenwoordigt een afzonderlijk attributiemodel.
* **Lijst van de Vergelijking van de Attributie**: Toont de zelfde gegevens zoals het staafdiagram, dat als lijst wordt vertegenwoordigd. Als u verschillende kolommen of rijen in deze tabel selecteert, wordt het staafdiagram en een aantal andere visualisaties in het deelvenster geselecteerd. Deze lijst doet gelijkaardig aan een andere lijst van Freeform in Workspace - toestaand u om componenten zoals metriek, segmenten, of onderverdelingen toe te voegen.
* **Overlap Diagram**: Een beeld die van de Venn de hoogste drie afmetingspunten toont en hoe vaak zij gezamenlijk aan een omzetting deelnemen. Bijvoorbeeld, wijst de grootte van de bel overlapping erop hoe vaak omzettingen voorkwamen wanneer een persoon aan beide afmetingspunten werd blootgesteld. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Detail van Prestaties**: Een spreidingsvisualisatie om tot drie attributiemodellen visueel te vergelijken.
* **Getweende Prestaties**: Toont de trend van toegeschreven omzettingen voor het hoogste afmetingspunt. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Stroom**: Laat u zien welke kanalen met het meest algemeen in wisselwerking staan, en in welke orde over de reis van een persoon.

## Attributiemodel

{{attribution-models-details}}

## Container

{{attribution-container}}

## Venster Opzoeken

{{attribution-lookback-window}}

## Voorbeeld

{{attribution-example}}

>[!MORELIKETHIS]
>
> [&#x200B; creeer een paneel &#x200B;](/help/analysis-workspace/c-panels/panels.md#create-a-panel)
>
