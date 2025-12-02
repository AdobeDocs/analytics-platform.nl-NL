---
title: Content Analytics-rapportage
description: Hoe rapporteren over Content Analytics
solution: Customer Journey Analytics
feature: Content Analytics
role: User
exl-id: 6e756ae8-b969-46f1-95b8-d8fbb0d058ed
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 0%

---

# Overzicht van Content Analytics-rapportage

U rapporteert, voert analyse uit en krijgt inzicht in Content Analytics binnen [&#x200B; Analysis Workspace &#x200B;](/help/analysis-workspace/home.md). Een specifiek Workspace [&#x200B; malplaatje &#x200B;](#template) is beschikbaar, zodat kunt u tot een pre-bevolkt project van Workspace met relevante inhoudsinzichten onmiddellijk toegang hebben.

Volledige rapportage over Content Analytics starten:

1. [&#x200B; creeer een nieuw &#x200B;](/help/analysis-workspace/build-workspace-project/create-projects.md) of [&#x200B; open een bestaand &#x200B;](/help/analysis-workspace/build-workspace-project/open-projects.md) project in Workspace.
1. Verzeker u [&#x200B; selecteert een gegevensmening &#x200B;](/help/analysis-workspace/c-panels/panels.md#data-view) voor Content Analytics rapporterend. Content Analytics het melden is slechts beschikbaar voor gegevensmeningen die [&#x200B; &#x200B;](/help/content-analytics/config/configuration.md) voor Content Analytics worden gevormd.
1. Sleep a ![&#x200B; Lijst &#x200B;](/help/assets/icons/Table.svg) [&#x200B; vrije vormlijst &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) visualisatie op het canvas.
1. Het gebruik [&#x200B; specifieke componenten van Content Analytics &#x200B;](components.md) en andere generische [&#x200B; componenten &#x200B;](/help/components/overview.md) (als segmenten, datumwaaiers, annotaties) om uw inzichten van Content Analytics te bouwen.

## Miniaturen

Op basis van de Content Analytics-specifieke afmetingen die u in uw project gebruikt, worden miniaturen weergegeven voor elementen en dimensies.

![&#x200B; de duimnagels van Content Analytics &#x200B;](../assets/aca-thumbnails.png)

Standaard worden miniaturen weergegeven voor relevante Content Analytics-afmetingen. De weergave van miniaturen configureren voor een Content Analytics-dimensie:

* Houd de muisaanwijzer boven een koptekstrij voor een Content Analytics-dimensie. Bijvoorbeeld **[!UICONTROL Asset IDs]** of **[!UICONTROL Experience IDs]** .
* Selecteer ![&#x200B; Plaatsend &#x200B;](/help/assets/icons/Setting.svg).
* Schakel **[!UICONTROL Row setting]** onder **[!UICONTROL Settings]** in de pop-up **[!UICONTROL Show Thumbnails]** in of uit.


## Voorvertoningen

Voor rijen van een Content Analytics-afmeting die miniaturen weergeven, kunt u een voorvertoningsvenster openen.

U opent de voorvertoning met de volgende details:

* Selecteer ![&#x200B; InfoOutline &#x200B;](/help/assets/icons/InfoOutline.svg). U ziet de volgende details.

  | Voorvertoning van ervaring | Voorvertoning van element |
  |---|---|
  | ![&#x200B; de voorproef van de Ervaring van Content Analytics &#x200B;](../assets/aca-experience-preview.png) | ![&#x200B; Voorproef van de Activa van Content Analytics &#x200B;](../assets/aca-asset-preview.png) |
  | Naam van de dimensie (bijvoorbeeld, **[!UICONTROL Experience ID])** | Naam van de afmeting van het element (bijvoorbeeld, **[!UICONTROL Asset ID])** |
  | **[!UICONTROL Impressions (all time)]**: aantal indrukken voor de ervaring. | **[!UICONTROL Impressions (all times)]**: aantal afbeeldingen voor het element. |
  | **[!UICONTROL Assets]**: Het aantal elementen dat deze ervaring bevat. <br/> Uitgezochte ![&#x200B; Uitsplitsing &#x200B;](/help/assets/icons/Breakdown.svg) **[!UICONTROL Breakdown]** om de activa te inspecteren. | **[!UICONTROL Experiences]**: Aantal ervaringen waarin dit element wordt weergegeven. <br/> Uitgezochte ![&#x200B; Uitsplitsing &#x200B;](/help/assets/icons/Breakdown.svg) **[!UICONTROL Breakdown]** om de activa te inspecteren. |
  | **[!UICONTROL First impression]**: Datum waarop de ervaring voor het eerst wordt weergegeven. | **[!UICONTROL First impression]**: Datum waarop het element voor het eerst wordt weergegeven. |
  | **[!UICONTROL &#x200B; Most recent impression]**: Datum van de meest recente indruk van de ervaring. | **[!UICONTROL Most recent impression]**: Datum van meest recente indruk van het element. |
  | **[!UICONTROL Experience attributes]**: De [&#x200B; attributen &#x200B;](/help/content-analytics/report/components.md#experience-attributes) van de ervaring. | **[!UICONTROL Asset attributes]**: De [&#x200B; attributen &#x200B;](/help/content-analytics/report/components.md#asset-attributes) van de activa. |


## Sjabloon

Een Content Analytics [&#x200B; malplaatje &#x200B;](/help/analysis-workspace/templates/use-templates.md) is beschikbaar om u te helpen welke inhoud en inhoudsattributen het best presteren. Het malplaatje maakt deel uit van het [&#x200B; kanaal van het Web en het gebruiksgeval van de Betrokkenheid &#x200B;](/help/analysis-workspace/templates/use-templates.md#web-engagement) en details hoe uw inhoud op een korrelig niveau presteert. U kunt kijken naar de prestaties van afzonderlijke elementen of naar specifieke kenmerken.

Gebaseerd op wat je leert, kun je een aantal dingen doen. Net als bij het promoten van hoogwaardige, goed presterende elementen op uw homepage, kunt u de inhoud voor specifieke segmenten personaliseren om de kenmerken voor hoge prestaties op te nemen, of inhoud roteren die geleidelijk aan is gaan groeien.

De sjabloon gebruiken:

1. Selecteer **[!UICONTROL Workspace]** in het hoofdmenu.
1. Controleer of u een gegevensweergave hebt geselecteerd die is geconfigureerd voor Content Analytics.
1. Zoek naar, of gebruik segmenten (**[!UICONTROL Web]** voor **[!UICONTROL Channel]** en **[!UICONTROL Engagement]** voor **&#x200B; [!UICONTROL Use Case] &#x200B;** s) om het **[!UICONTROL Content Analytics]** malplaatje te vinden en te selecteren.
1. Selecteer **[!UICONTROL Use template]**.
1. Selecteer in het dialoogvenster **[!UICONTROL Set up your template]** een metrische waarde in het dialoogvenster **[!UICONTROL Select a conversion metric]** . Bijvoorbeeld **[!UICONTROL Asset CTR]** .
1. Selecteer **[!UICONTROL Continue]**.

Een **[!UICONTROL Content Analytics Overview]** project opent in [&#x200B; Analysis Workspace &#x200B;](/help/analysis-workspace/home.md). Het project bestaat uit vier [&#x200B; panelen &#x200B;](/help/analysis-workspace/c-panels/panels.md), waar elk paneel [&#x200B; vrije vormlijsten &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) en [&#x200B; visualisaties &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) verstrekt om een specifieke vraag te beantwoorden:

* **Welke inhoud voert het beste uit?**
Dit paneel helpt u te begrijpen welke ervaringen en welke middelen in die ervaringen de drijvende kracht zijn achter betrokkenheid en conversie. Ervaringen zijn een volledige webpagina, die op een bepaald moment wordt vastgelegd. Een ervaring kan zowel tekst als meerdere afzonderlijke afbeeldingselementen bevatten. Een element is een afzonderlijke afbeelding.

  Het deelvenster bestaat uit de volgende visualisaties:

   * **Ervaringen**.

     >[!NOTE]
     >
     >Deze visualisaties tonen slechts wanneer u [&#x200B; inbegrepen ervaringen &#x200B;](/help/content-analytics/config/guided.md#experience-capture-and-definition) in uw configuratie van Content Analytics hebt.
     > 

      * **Ervaring CTR**: a [&#x200B; summiere verandering &#x200B;](/help/analysis-workspace/visualizations/summary-number-change.md) visualisatie, tonend Ervaring CTR.
      * **Hoogste het omzetten ervaringen**: A [&#x200B; horizontale bar &#x200B;](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die bovenkant het omzetten ervaringen tonen die op geselecteerde metrische omzetting worden gebaseerd.
      * **Hoogst uitvoerend ervaringen**: A [&#x200B; vrije lijst van de vorm &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) (met inbegrip van [&#x200B; duimnagels &#x200B;](#thumbnails) en [&#x200B; voorproeven &#x200B;](#previews)) voor de hoogste uitvoerend ervaringen.

   * **Assets**

      * **Activum CTR**
A [&#x200B; summiere verandering &#x200B;](/help/analysis-workspace/visualizations/summary-number-change.md) visualisatie die Activum CTR toont.
      * **Hoogste het omzetten activa**
A [&#x200B; horizontale bar &#x200B;](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die bovenkant het omzetten activa toont die op geselecteerde metrische omzetting worden gebaseerd.
      * **Hoogst uitvoerend activa**
A [&#x200B; vrije vormlijst &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) (met inbegrip van [&#x200B; duimnagels &#x200B;](#thumbnails) en [&#x200B; voorproeven &#x200B;](#previews)) voor de hoogste uitvoerend activa.
      * **Assets - meningen tegenover omzetting.**
A [&#x200B; scatterplot &#x200B;](/help/analysis-workspace/visualizations/scatterplot.md) visualisatie die een spreidingsplot van activameningen tegenover activa omzettingen toont.

* **Welke activa attributen dragen aan omzettingen bij?**
Content Analytics gebruikt AI en GenAI om automatisch metagegevens van elk element toe te wijzen, zoals onderwerpen, scènes, voorgrondkleuren, enzovoort. Een kenmerk is een door AI toegewezen metagegevenstag waarmee wordt beschreven wat zich in een element of ervaring bevindt. Bijvoorbeeld: <code> voorgrondkleur: rood</code> is een automatisch toegewezen attribuut. Met behulp van de visualisaties kunt u bepalen welke kenmerken van uw elementen het meest bijdragen aan de conversie.

  Het deelvenster bestaat uit de volgende visualisaties:

   * **Hoogste het omzetten activaattributen**
A [&#x200B; horizontale bar &#x200B;](/help/analysis-workspace/visualizations/horizontal-bar.md) die de bovenkant toont die activaattributen die op geselecteerde metrische omzetting worden gebaseerd.
   * **Hoogste het omzetten activa attributen tegenover voorafgaande 30 dagen**
A [&#x200B; horizontale bar &#x200B;](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die de hoogste het omzetten activaattributen toont, in vergelijking met voorafgaande 30 dagen, die op geselecteerde metrische omzetting worden gebaseerd.
   * **Hoogste het omzetten gegevens van activa attribuut**
A [&#x200B; vrije lijst van de vorm &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) die de hoogste omzettingsattributen toont die op geselecteerde metrische omzetting worden gebaseerd. Selecteer een rij in de lijst om de trendvisualisatie van Attributen bij te werken.
   * **trend van Attributen**
A [&#x200B; lijn &#x200B;](/help/analysis-workspace/visualizations/line.md) visualisatie die de kenmerktrend voor de geselecteerde hoogste het omzetten activa attributen tonen.
   * **Voorgrondkleur van Activa**
Een voorbeeld [&#x200B; vrije lijst &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) die de prestaties van punten van één enkele categorie van activaattributen vergelijkt: Voorgrondkleuren. U kunt dit elementkenmerk vervangen door andere klassendimensies van het elementkenmerk.

* **Welke ervaringsattributen dragen aan omzettingen bij?**

  >[!NOTE]
  >
  >Dit paneel toont slechts wanneer u [&#x200B; inbegrepen ervaringen &#x200B;](/help/content-analytics/config/guided.md#experience-capture-and-definition) in uw configuratie van Content Analytics hebt.
  > 

  Elementkenmerken zijn vooral gericht op de visuele kwaliteiten van afbeeldingen, terwijl kenmerken de tekst van de pagina beïnvloeden. Met de onderstaande visualisaties kunt u nagaan welke ervaringskenmerken bijdragen aan de conversie. Deze kenmerken worden ook automatisch toegewezen met behulp van AI- en GenAI-modellen.

  Het deelvenster bestaat uit de volgende visualisaties:

   * **Hoogste het omzetten ervaringsattributen**
A [&#x200B; horizontale bar &#x200B;](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die de hoogste het omzetten ervaringsattributen toont die op geselecteerde metrische omzetting worden gebaseerd.
   * **Hoogste het omzetten ervaringsattributen versus voorafgaande 30 dagen**
A [&#x200B; horizontale bar &#x200B;](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die de hoogste het omzetten ervaringsattributen toont, in vergelijking met voorafgaande 30 dagen, die op geselecteerde metrische omzetting worden gebaseerd.
   * **Hoogste het omzetten gegevens van ervaringsattributen**
A [&#x200B; vrije vormlijst &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) die de hoogste het omzetten ervaringen toont die op geselecteerde metrische omzetting worden gebaseerd. Selecteer een rij in de tabel om de lijnvisualisatie bij te werken.
   * **Lijn**
A [&#x200B; lijn &#x200B;](/help/analysis-workspace/visualizations/line.md) visualisatie die de trend voor de geselecteerde hoogste het omzetten ervaringsattributen toont.
   * **de sleutelwoorden van de Ervaring**
A [&#x200B; vrije lijst van de vrije vorm &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) die de hoogste ervaringstrefwoorden toont die op geselecteerde metrische omzetting worden gebaseerd.

* **waar verschijnen de activa op mijn plaats?**
Een deelvenster dat bestaat uit één vrije-vormtabel waarin de meest bekeken elementen op uw site worden weergegeven.

  Het paneel bestaat uit één visualisatie:

   * **waar verschijnen de meest bekeken activa?**
U kunt elk element onderverdelen op basis van afmetingen, zodat u beter begrijpt waar de afbeelding voorkomt.

     In de voorbeeld [&#x200B; vrije vormlijst &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) (met inbegrip van [&#x200B; duimnagels &#x200B;](#thumbnails) en [&#x200B; voorproeven &#x200B;](#previews)), **[!UICONTROL Asset Perception ID]** wordt gebruikt in plaats van [!UICONTROL Asset Id]. Soms kan exact dezelfde afbeelding op uw site worden gedupliceerd met een andere afbeeldings-URL. Met het kenmerk [!UICONTROL Asset Perception ID] kunt u deze duplicaten groeperen onder één id.

     Omdat elementen op een pagina kunnen veranderen, wordt elk element uitgesplitst door **[!UICONTROL Experience Id]** om te bepalen op welke versie van die pagina het element is weergegeven. U kunt [!UICONTROL Experience Id] vervangen door andere afmetingen die u helpen de locatie van een element op uw site te begrijpen. Bijvoorbeeld [!UICONTROL Page name] , [!UICONTROL Page URL] of [!UICONTROL Site section] .

     U kunt [!UICONTROL Asset Perception ID] ook omwisselen met [!UICONTROL Asset Id] om een record te verkrijgen waarin wordt aangegeven waar naar specifieke afbeeldings-URL&#39;s wordt verwezen.


>[!MORELIKETHIS]
>
>[&#x200B; de componenten van Content Analytics &#x200B;](components.md)
>[Sjablonen gebruiken &#x200B;](/help/analysis-workspace/templates/use-templates.md#web-engagement)
>
