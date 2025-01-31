---
title: Overzicht van productgebruik
description: Bekijk inzichten en rapporten over hoe uw organisatie Customer Journey Analytics gebruikt.
exl-id: 3806ca7c-ee90-4222-9ffd-2e791c4550e5
source-git-commit: e7534a1943307f5bbc92a845ddffe0651794b854
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Overzicht van productgebruik

Het gebruik van producten biedt uw organisatie de mogelijkheid om analysegegevens te bekijken over hoe uw organisatie Customer Journey Analytics gebruikt. Het is beschikbaar voor alle organisaties die Customer Journey Analytics gebruiken. Als deze optie is ingeschakeld, worden de volgende Adobe Experience Platform-componenten automatisch gemaakt en geactiveerd. Deze componenten zijn allemaal systeemeigendom, alleen-lezen en kunnen niet worden bewerkt.

* Een schema in Adobe Experience Platform
* Een dataset in Adobe Experience Platform
* Een verbinding in Customer Journey Analytics
* Een gegevensweergave in Customer Journey Analytics

Alle gegevensinzameling en opstelling worden automatisch gevormd voor u zodra toegelaten. Elke keer dat een gebruiker een actie uitvoert in Analysis Workspace, wordt die actie bijgehouden en beschikbaar voor rapportage.

>[!IMPORTANT]
>
>Deze functie telt mee voor je contractuele rijlimieten in Adobe Experience Platform. Zorg ervoor dat uw organisatie de gegevens kan aanpassen die door deze eigenschap worden geproduceerd alvorens het toe te laten.

## Productgebruik inschakelen

**[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL Product Usage]**

Het navigeren aan deze sectie van de interface in Customer Journey Analytics neemt u aan [ montages van Gegevens ](data-settings.md) waar u deze eigenschap kunt toelaten.

## Beschikbare afmetingen

Als u het productgebruik inschakelt, zijn de volgende afmetingen beschikbaar. Als u dimensie-instellingen wilt wijzigen, maakt u een kopie van de gegevensweergave die eigendom is van het systeem en gebruikt u de gekopieerde gegevensweergave in Analysis Workspace.

* **[!UICONTROL Action Name]**: Het type actie dat de gebruiker heeft uitgevoerd. U kunt deze dimensie als elke gewenste metrische waarde gebruiken door een kopie in de weergave-instellingen voor gegevens te maken. Tot de Dimensionen behoren:
   * [!UICONTROL Add attribution]
   * [!UICONTROL Add component]
   * [!UICONTROL Add panel]
   * [!UICONTROL Add visualization]
   * [!UICONTROL Create new guided analysis]
   * [!UICONTROL Create new project]
   * [!UICONTROL Curate components]
   * [!UICONTROL Download CSV]
   * [!UICONTROL Download PDF]
   * [!UICONTROL Load guided analysis]
   * [!UICONTROL Load project]
   * [!UICONTROL New scorecard loaded]
   * [!UICONTROL Open data dictionary]
   * [!UICONTROL Open intelligent captions]
   * [!UICONTROL Project share]
   * [!UICONTROL Run Experimentation panel]
   * [!UICONTROL Save project]
   * [!UICONTROL Scorecard saved]
   * [!UICONTROL Send file]
   * [!UICONTROL Send file on schedule]
   * [!UICONTROL Share project with anyone]
   * [!UICONTROL Share project with Workspace users]
* **[!UICONTROL Attribution Model Used]**: Het type attributiemodel dat de component gebruikt. Tot de Dimensionen behoren:
   * [!UICONTROL Last touch]
   * [!UICONTROL First touch]
   * [!UICONTROL Linear]
   * [!UICONTROL Participation]
   * [!UICONTROL Same touch]
   * [!UICONTROL U shaped]
   * [!UICONTROL J curve]
   * [!UICONTROL Inverse J]
   * [!UICONTROL Time decay]
   * [!UICONTROL Custom]
   * [!UICONTROL Algorithmic]
* **[!UICONTROL Component Name]**: De naam van de component die is toegevoegd, verwijderd of gewijzigd.
* **[!UICONTROL Component Type]**: Het type component dat is toegevoegd, verwijderd of gewijzigd. Tot de Dimensionen behoren:
   * [!UICONTROL Dimension]
   * [!UICONTROL Metric]
   * [!UICONTROL Filter]
   * [!UICONTROL Calculated metric]
   * [!UICONTROL Date range]
   * [!UICONTROL Annotation]
   * [!UICONTROL Alert]
* **[!UICONTROL Login User]**: De gebruiker die de handeling heeft uitgevoerd.
* **[!UICONTROL Panel Used]**: Het deelvenster waarin de component is toegevoegd, verwijderd of gewijzigd. Tot de Dimensionen behoren:
   * [!UICONTROL Attribution]
   * [!UICONTROL Blank panel]
   * [!UICONTROL Experimentation]
   * [!UICONTROL Freeform]
   * [!UICONTROL Next or previous item]
   * [!UICONTROL Quick insights]
   * [!UICONTROL Trends]
   * [!UICONTROL Funnel]
   * [!UICONTROL User growth]
   * [!UICONTROL Impact]
   * [!UICONTROL User stream]
   * [!UICONTROL Retention]
   * [!UICONTROL Feature matrix]
* **[!UICONTROL Project Name]**: De vriendelijke naam van het project.
* **[!UICONTROL Project Type]**: Het projecttype. Tot de Dimensionen behoren:
   * `workspace-projects`
   * `guided-analysis`
   * `mobile-scorecard-builder`
* **[!UICONTROL Visualization Used]**: De visualisatie die is toegevoegd, verwijderd of gewijzigd. Tot de Dimensionen behoren:
   * [!UICONTROL Freeform table]
   * [!UICONTROL Cohort table]
   * [!UICONTROL Fallout]
   * [!UICONTROL Flow]
   * [!UICONTROL Journey Canvas reportlet]
   * [!UICONTROL Area]
   * [!UICONTROL Area stacked]
   * [!UICONTROL Bar]
   * [!UICONTROL Bar stacked]
   * [!UICONTROL Bullet]
   * [!UICONTROL Combo]
   * [!UICONTROL Donut]
   * [!UICONTROL Histogram]
   * [!UICONTROL Horizontal bar]
   * [!UICONTROL Horizontal bar stacked]
   * [!UICONTROL Key metric summary]
   * [!UICONTROL Line]
   * [!UICONTROL Map]
   * [!UICONTROL Scatter]
   * [!UICONTROL Section header]
   * [!UICONTROL Summary change]
   * [!UICONTROL Summary number]
   * [!UICONTROL Text]
   * [!UICONTROL Treemap]
   * [!UICONTROL Venn]

Het gebruik van het product houdt geen individuele projectcomponenten bij wanneer een project slechts wordt geopend of bekeken. De gebruikersactie van het openen van een project wordt echter gevolgd.
