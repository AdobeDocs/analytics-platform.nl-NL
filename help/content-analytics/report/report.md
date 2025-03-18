---
title: Rapportage van content Analytics
description: Over het rapporteren van Content Analytics
solution: Customer Journey Analytics
feature: Content Analytics
role: User
hide: true
hidefromtoc: true
exl-id: 6e756ae8-b969-46f1-95b8-d8fbb0d058ed
source-git-commit: df3a877feed82f6cbd181561da68837373bdafb8
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---

# Overzicht van rapportage voor inhoudsanalyse

>[!WARNING]
>
>Dit artikel is een voorlopige niet-officiële ontwerpversie van een toekomstige definitieve versie en maakt deel uit van de documentatie van Content Analytics. Alle inhoud kan worden gewijzigd en er kunnen geen wettelijke verplichtingen uit de huidige versie van dit artikel worden afgeleid.
>

{{release-limited-testing}}

De rapportage over Content Analytics vindt plaats in Analysis Workspace. Een specifiek Workspace [ malplaatje ](#template) is beschikbaar, zodat kunt u tot een pre-bevolkt project van Workspace met relevante inhoudsinzichten onmiddellijk toegang hebben.

Rapporten over inhoudanalyse vanaf nul starten:

1. [ creeer een nieuw ](/help/analysis-workspace/build-workspace-project/create-projects.md) of [ open een bestaand ](/help/analysis-workspace/build-workspace-project/open-projects.md) project in Workspace.
1. Verzeker u [ selecteert een gegevensmening ](/help/analysis-workspace/c-panels/panels.md#data-view) voor Content Analytics rapporterend. Content Analytics het melden is slechts beschikbaar voor gegevensmeningen die [ ](/help/content-analytics/config/configuration.md) voor Content Analytics worden gevormd.
1. Sleep a ![ Lijst ](/help/assets/icons/Table.svg) [ vrije vormlijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) visualisatie op het canvas.
1. Gebruik [ specifieke componenten van de Analyse van de Inhoud ](components.md) en andere generische [ componenten ](/help/components/overview.md) (als filters, datumwaaiers, annotaties) om uw inzichten van de inhoudsanalyse te bouwen. Alternatief, gebruik het [ analytische malplaatje van de Inhoud ](#template).

## Miniaturen

Op basis van de specifieke afmetingen voor inhoudsanalyse die u in uw project gebruikt, worden miniaturen weergegeven voor elementen en dimensies.

![ de duimnagels van de Analytics van de Inhoud ](../assets/aca-thumbnails.png)

## Voorvertoningen

Voor afmetingen met miniaturen (zoals Naam element, Naam ervaring en andere) kunt u een voorvertoningsvenster openen.

U opent de voorvertoning met de volgende details:

* Selecteer ![ InfoOutline ](/help/assets/icons/InfoOutline.svg). U ziet de volgende details.

  | Voorvertoning van ervaring | Voorvertoning van element |
  |---|---|
  | ![ de Ervaring van de Analyse van de Inhoud ](../assets/aca-experience-preview.png) | ![ Voorproef van de Activa van de Analyse van de Inhoud ](../assets/aca-asset-preview.png) |
  | **[!UICONTROL Name of the experience]** | **[!UICONTROL Name of the asset]** |
  | **[!UICONTROL Impressions (all times)]**: aantal indrukken voor de ervaring. | **[!UICONTROL Impressions (all times)]**: aantal afbeeldingen voor het element. |
  | **[!UICONTROL Assets]**: Het aantal elementen dat deze ervaring bevat. Selecteer ![ Uitsplitsing ](/help/assets/icons/Breakdown.svg) **[!UICONTROL Breakdown]** om de activa te inspecteren. | **[!UICONTROL Experiences]**: Aantal ervaringen waarin dit element wordt weergegeven. ![ Uitsplitsing ](/help/assets/icons/Breakdown.svg) **[!UICONTROL Breakdown]** om de activa te inspecteren. |
  | **[!UICONTROL First impression]**: Datum waarop de ervaring voor het eerst wordt weergegeven. | **[!UICONTROL First impression]**: Datum waarop het element voor het eerst wordt weergegeven. |
  | **[!UICONTROL  Most recent impression]**: Datum van de meest recente indruk van de ervaring. | **[!UICONTROL Most recent impression]**: Datum van meest recente indruk van het element. |
  | **[!UICONTROL Experience attributes]**: De kenmerken van de ervaring. | **[!UICONTROL Asset attributes]**: De kenmerken van het element. |


## Sjabloon

A Content analytics [ malplaatje ](/help/analysis-workspace/templates/use-templates.md) is beschikbaar om u te helpen welke inhoud en inhoudsattributen het best presteren. Het malplaatje maakt deel uit van het [ kanaal van het Web en het gebruiksgeval van de Betrokkenheid ](/help/analysis-workspace/templates/use-templates.md#web-engagement) en details hoe uw inhoud op een korrelig niveau presteert. U kunt kijken naar de prestaties van afzonderlijke elementen of naar specifieke kenmerken.

Gebaseerd op wat je leert, kun je een aantal dingen doen. Net als bij het promoten van hoogwaardige, goed presterende elementen op uw homepage, kunt u de inhoud voor specifieke segmenten personaliseren om de kenmerken voor hoge prestaties op te nemen, of inhoud roteren die geleidelijk aan is gaan groeien.

De sjabloon gebruiken:

1. Selecteer **[!UICONTROL Workspace]** in het hoofdmenu.
1. Controleer of u een gegevensweergave hebt geselecteerd die is geconfigureerd voor Content Analytics.
1. Zoek naar, of gebruik filters (**[!UICONTROL Web]** voor **[!UICONTROL Channel]** en **[!UICONTROL Engagement]** voor ** [!UICONTROL Use Case] **s) om het **[!UICONTROL Content analytics]** malplaatje te vinden en te selecteren.
1. Selecteer **[!UICONTROL Use template]** .
1. Selecteer in het dialoogvenster **[!UICONTROL Set up your template]** een metrische waarde in het dialoogvenster **[!UICONTROL Select a conversion metric]** . Bijvoorbeeld **[!UICONTROL Asset CTR]** .
1. Selecteer **[!UICONTROL Continue]** .

Er wordt een **[!UICONTROL Content Analytics Overview]** -project geopend in Workspace. Het project bestaat uit vier panels, die elk specifieke vragen beantwoorden:

* **Welke inhoud voert het beste uit?**
Dit paneel helpt u te begrijpen welke ervaringen en welke middelen in die ervaringen de drijvende kracht zijn achter betrokkenheid en conversie. Ervaringen zijn een volledige webpagina, die op een bepaald moment wordt vastgelegd. Een ervaring kan zowel tekst als meerdere afzonderlijke afbeeldingselementen bevatten. Een element is een afzonderlijke afbeelding.

  Het deelvenster bestaat uit de volgende visualisaties:

   * **Ervaringen**

      * **Ervaring CTR**: een summiere verandering visualisatie, tonend Ervaring CTR.
      * **Hoogste het omzetten ervaringen**: Een horizontale visualisatie van het staafdiagram die hoogste het omzetten ervaringen tonen die op geselecteerde metrische omzetting worden gebaseerd.
      * **Hoogst uitvoerend ervaringen**: Een vrije vormlijst (met inbegrip van duimnagels en voorproeven) voor de hoogste het uitvoeren ervaringen.

   * **Assets**

      * **Activum CTR**
A [ summiere verandering ](/help/analysis-workspace/visualizations/summary-number-change.md) visualisatie die Activum CTR toont.
      * **Hoogste het omzetten activa**
A [ horizontale bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die bovenkant het omzetten activa toont die op geselecteerde metrische omzetting worden gebaseerd.
      * **Hoogst uitvoerend activa**
A [ vrije vormlijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) (met inbegrip van [ duimnagels ](#thumbnails) en [ voorproeven ](#previews)) voor de hoogste uitvoerend activa.
      * **Assets - meningen tegenover omzetting.**
A [ scatterplot ](/help/analysis-workspace/visualizations/scatterplot.md) visualisatie die een spreidingsplot van activameningen tegenover activa omzettingen toont.

* **Welke activa attributen dragen aan omzettingen bij?**
Content Analytics gebruikt AI en GenAI om automatisch metagegevens van elk element toe te wijzen, zoals onderwerpen, scènes, voorgrondkleuren, enzovoort. Een kenmerk is een door AI toegewezen metagegevenstag waarmee wordt beschreven wat zich in een element of ervaring bevindt. Bijvoorbeeld: <code> voorgrondkleur: rood</code> is een automatisch toegewezen attribuut. Met behulp van de visualisaties kunt u bepalen welke kenmerken van uw elementen het meest bijdragen aan de conversie.

  Het deelvenster bestaat uit de volgende visualisaties:

   * **Hoogste het omzetten activaattributen**
A [ horizontale bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) die de bovenkant toont die activaattributen die op geselecteerde metrische omzetting worden gebaseerd.
   * **Hoogste het omzetten activa attributen tegenover voorafgaande 30 dagen**
A [ horizontale bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die de hoogste het omzetten activaattributen toont, in vergelijking met voorafgaande 30 dagen, die op geselecteerde metrische omzetting worden gebaseerd.
   * **Hoogste het omzetten gegevens van activa attribuut**
A [ vrije lijst van de vorm ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) die de hoogste omzettingsattributen toont die op geselecteerde metrische omzetting worden gebaseerd. Selecteer een rij in de lijst om de trendvisualisatie van Attributen bij te werken.
   * **trend van Attributen**
A [ lijn ](/help/analysis-workspace/visualizations/line.md) visualisatie die de kenmerktrend voor de geselecteerde hoogste het omzetten activa attributen tonen.
   * **Voorgrondkleur van Activa**
Een voorbeeld [ vrije lijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) die de prestaties van punten van één enkele categorie van activaattributen vergelijkt: Voorgrondkleuren. U kunt dit elementkenmerk vervangen door andere klassendimensies van het elementkenmerk.

* **Welke ervaringsattributen dragen tot omzettingen bij?**
Elementkenmerken zijn vooral gericht op de visuele kwaliteiten van afbeeldingen, terwijl kenmerken de tekst van de pagina beïnvloeden. Met de onderstaande visualisaties kunt u nagaan welke ervaringskenmerken bijdragen aan de conversie. Deze kenmerken worden ook automatisch toegewezen met behulp van AI- en GenAI-modellen.

  Het deelvenster bestaat uit de volgende visualisaties:

   * **Hoogste het omzetten ervaringsattributen**
A [ horizontale bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die de hoogste het omzetten ervaringsattributen toont die op geselecteerde metrische omzetting worden gebaseerd.
   * **Hoogste het omzetten ervaringsattributen versus voorafgaande 30 dagen**
A [ horizontale bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die de hoogste het omzetten ervaringsattributen toont, in vergelijking met voorafgaande 30 dagen, die op geselecteerde metrische omzetting worden gebaseerd.
   * **Hoogste het omzetten gegevens van ervaringsattributen**
A [ vrije vormlijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) die de hoogste het omzetten ervaringen toont die op geselecteerde metrische omzetting worden gebaseerd. Selecteer een rij in de tabel om de lijnvisualisatie bij te werken.
   * **Lijn**
A [ lijn ](/help/analysis-workspace/visualizations/line.md) visualisatie die de trend voor de geselecteerde hoogste het omzetten ervaringsattributen toont.
   * **de sleutelwoorden van de Ervaring**
A [ vrije lijst van de vrije vorm ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) die de hoogste ervaringstrefwoorden toont die op geselecteerde metrische omzetting worden gebaseerd.

* **waar verschijnen de activa op mijn plaats?**
Een deelvenster dat bestaat uit één vrije-vormtabel waarin wordt aangegeven waar de meeste weergaveelementen op uw site worden weergegeven.

  Het paneel bestaat uit één visualisatie:

   * **waar verschijnen de meest bekeken activa?**
U kunt elke identificatie voor middelen opsplitsen op basis van afmetingen die u helpen beter te begrijpen waar die afbeelding voorkomt.

     In dit voorbeeld [ vrije vormlijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) (met inbegrip van [ duimnagels ](#thumbnails) en [ voorproeven ](#previews)), [!UICONTROL *identiteitskaart van de Perceptie van Activa*] wordt gebruikt in plaats van [!UICONTROL *identiteitskaart van Activa*]. Soms kan exact dezelfde afbeelding op uw site worden gedupliceerd met een andere afbeeldings-URL. De _]attribuut van de Waarneming van activa 0} {helpt deze duplicaten onder één enkele identiteitskaart groeperen.[!UICONTROL _ Omdat de activa op een pagina kunnen veranderen, wordt elk element verdeeld door [!UICONTROL _identiteitskaart van de Ervaring_], om te identificeren welke versie van die pagina die activa verschenen.

     U kunt [!UICONTROL _identiteitskaart van de Ervaring_] met andere afmetingen vervangen die u helpen de plaats van een activaplaats op uw plaats begrijpen. Bijvoorbeeld, {de naam van de 0} Pagina _],[!UICONTROL _ Pagina URL _], of[!UICONTROL _ sectie van de Plaats _].[!UICONTROL _

     U kunt ook uit [!UICONTROL _identiteitskaart van de Perceptie_] met [!UICONTROL _identiteitskaart van Activa_] ruilen om een verslag te krijgen van waar specifiek beeld URLs wordt van verwijzingen voorzien.


>[!MORELIKETHIS]
>
>{de componenten van Analytics van 0} Inhoud ](components.md)[
>[Sjablonen gebruiken ](/help/analysis-workspace/templates/use-templates.md#web-engagement)
>
