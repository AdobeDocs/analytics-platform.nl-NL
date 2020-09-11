---
description: Snelle inzichten zijn een hulpmiddel voor nieuwe gebruikers van de Werkruimte die hen in de bouw van gegevenslijsten en visualisaties begeleiden
title: Deelvenster Snelle inzichten
translation-type: tm+mt
source-git-commit: 468f1f3bbe8ed555e944be49ec3bf3dcc577a23e
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 2%

---


# Deelvenster Snelle inzichten

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset wijkt enigszins af van [Analysis Workspace in het traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

>[!IMPORTANT]
>
>**[!UICONTROL Quick Insights]** momenteel wordt slechts beperkt getest. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

[!UICONTROL Quick Insights] biedt richtlijnen voor niet-analisten en nieuwe gebruikers van [!UICONTROL Analysis Workspace] over hoe ze zakelijke kwesties snel en eenvoudig kunnen beantwoorden. Het is ook een geweldig hulpmiddel voor geavanceerde gebruikers die snel een eenvoudige vraag willen beantwoorden zonder zelf een tabel te hoeven maken.

Wanneer u deze voor het eerst gebruikt [!UICONTROL Analysis Workspace]Misschien vraagt u zich af wat visualisaties het nuttigst zijn, welke dimensies en metriek inzichten zouden kunnen vergemakkelijken, waar te om punten te slepen en te laten vallen, waar te om een segment te creëren, etc.

Om dit te helpen en op basis van het gebruik van gegevenscomponenten door uw eigen bedrijf in [!UICONTROL Analysis Workspace], [!UICONTROL Quick Insights] leverages een algoritme dat u met de populairste afmetingen, metriek, segmenten, en datumwaaiers zal voorstellen uw bedrijf gebruikt. In feite zult u afmetingen, metriek, en segmenten zien die zoals worden geëtiketteerd [!UICONTROL Popular] in de vervolgkeuzelijst, zoals u hier ziet:

![](assets/popular-tag.png)

[!UICONTROL Quick Insights] helpt u

* Een gegevenstabel en een bijbehorende visualisatie op de juiste wijze samenstellen in [!UICONTROL Analysis Workspace].
* Leer de terminologie en woordenschat voor basiscomponenten en stukken [!UICONTROL Analysis Workspace].
* Doe eenvoudige onderverdelingen van dimensies, voeg veelvoudige metriek toe of vergelijk segmenten gemakkelijk binnen een [!UICONTROL Freeform table].
* U kunt verschillende visualisatietypen wijzigen of uitproberen om snel en intuïtief het zoekgereedschap voor uw analyse te vinden.

## Basistoets

Hier volgen enkele basistermen die u bekend moet maken. Elke gegevenslijst bestaat uit 2 of meer bouwstenen (componenten) die u gebruikt om uw gegevensverhaal te vertellen.

| Bouwsteen (component) | Definitie |
|---|---|
| [!UICONTROL Dimension] | Dimension zijn beschrijvingen of kenmerken van metrische gegevens die kunnen worden bekeken, opgesplitst en vergeleken in een project. Het zijn niet-numerieke waarden en datums die worden opgesplitst in dimensie-items. Bijvoorbeeld &#39;browser&#39; of &#39;pagina&#39; zijn afmetingen. |
| [!UICONTROL Dimension item] | Dimension-items zijn afzonderlijke waarden voor een dimensie. Dimensie-items voor de afmetingen van de browser zijn bijvoorbeeld &quot;Chrome&quot;, &quot;Firefox&quot;, &quot;Edge&quot;, enzovoort. |
| [!UICONTROL Metric] | De metriek zijn kwantitatieve informatie over bezoekersactiviteit, zoals meningen, klik-door, herladingen, gemiddelde bestede tijd, eenheden, orden, opbrengst, etc. |
| [!UICONTROL Visualization] | Werkruimte biedt [een aantal visualisaties](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) om visuele weergaven van uw gegevens te maken, zoals staafdiagrammen, donutgrafieken, histogrammen, lijngrafieken, kaarten, scatterpercelen en andere. |
| [!UICONTROL Dimension Breakdown] | Een afbraak van dimensies is een manier om een dimensie letterlijk op andere dimensies in te delen. In ons voorbeeld kunt u de VS-staten opsplitsen op mobiele apparaten om de bezoeken aan mobiele apparaten per status op te halen, of u kunt mobiele apparaten opsplitsen op typen mobiele apparaten, op regio&#39;s, op interne campagnes, enz. |
| [!UICONTROL Segment] | Met segmenten kunt u subsets van bezoekers identificeren op basis van kenmerken of interacties van websites. U kunt bijvoorbeeld [!UICONTROL Visitor] segmenten op basis van kenmerken: browsertype, apparaat, aantal bezoeken, land, geslacht of op basis van interacties: campagnes, sleutelwoordonderzoek, onderzoeksmotor, of gebaseerd op uitgang en ingangen: bezoekers van Facebook, een gedefinieerde bestemmingspagina, een verwijzend domein of gebaseerd op aangepaste variabelen: formulierveld, gedefinieerde categorieën, klant-id. |

## Aan de slag met Quick Insights

1. Meld u aan bij Adobe Analytics met de gegevens die u hebt ontvangen.
1. Ga naar [!UICONTROL Workspace] en klik op **[!UICONTROL Create New Project]** en klik vervolgens op **[!UICONTROL Quick Insights]**. (U kunt dit deelvenster ook openen via het dialoogvenster **[!UICONTROL Panel]** in de linkerspoorstaaf.)

   ![](assets/qibuilder.png)

   ![](assets/qi-panel.png)

1. Wanneer u voor het eerst begint, doorloopt u de korte zelfstudie die u een aantal van de [!UICONTROL Quick Insights panel] basisbeginselen. Of klik op **[!UICONTROL Skip Tutorial]**.
1. Selecteer de bouwstenen (ook wel componenten genoemd): afmetingen (oranje), metriek (groen), segmenten (blauw), of datumwaaiers (paars) U moet minstens één afmeting en één metrisch selecteren voor een lijst die automatisch moet worden gebouwd.

   ![](assets/qibuilder2.png)

   U kunt de bouwstenen op drie manieren selecteren:
   * Sleep en zet ze neer vanaf de linkerspoorstaaf.
   * Als u weet wat u zoekt: Begin met typen en [!UICONTROL Quick Insights] vult de spaties voor u in.
   * Klik op de vervolgkeuzelijst en zoek in de lijst.

1. Wanneer u minstens één afmeting en één metrisch hebt toegevoegd, zal het volgende voor u worden gecreeerd:

   * Een tabel met vrije vorm met de afmetingen (hier, Amerikaanse staten) verticaal en de metrische waarde (hier, Visit) horizontaal boven. Bekijk deze tabel:

   ![](assets/qibuilder3.png)

   * Een begeleidende visualisatie, in dit geval een [staafdiagram](/help/analysis-workspace/visualizations/bar.md). De gegenereerde visualisatie is gebaseerd op het type gegevens dat u aan de tabel hebt toegevoegd. Op tijd gebaseerde gegevens (zoals [!UICONTROL Visits] per dag/maand) standaardinstellingen [!UICONTROL Line] grafiek. Alle gegevens die niet op tijd zijn gebaseerd (zoals [!UICONTROL Visits] per [!UICONTROL Device]) is standaard ingesteld op een [!UICONTROL Bar] grafiek. U kunt het type visualisatie wijzigen door op de vervolgkeuzepijl naast het visualisatietype te klikken.


1. (Optioneel) U kunt de dimensies uitvouwen en elementen van de dimensie bekijken door op de pijl-rechts naast de dimensie te klikken.

1. Voeg meer verfijningen toe zoals hieronder beschreven onder &quot;Meer tips.&quot;

1. Uw project opslaan door op **[!UICONTROL Project > Save]**.

## Meer tips

Andere handige tips worden weergegeven in het dialoogvenster [!UICONTROL Quick Insights Builder], sommige afhankelijk van uw laatste handeling.

* Voer eerst de **[!UICONTROL More tips]** zelfstudie: Via de Help (?) pictogram naast [!UICONTROL Quick Insights] titel. Dit leerprogramma toont omhoog 24 uren nadat u een project met minstens één afmeting en één metrisch hebt gecreeerd.

   ![](assets/qibuilder4.png)

* **Uitsplitsing naar**: U kunt tot 3 niveaus van onderverdelingen op dimensies gebruiken om neer tot de gegevens te boren u echt nodig hebt.

   ![](assets/qibuilder5.png)

* **Meer metriek toevoegen**: U kunt tot 2 meer metriek toevoegen door te gebruiken EN exploitant om hen toe te voegen de lijst.

   ![](assets/qibuilder6.png)

* **Meer segmenten toevoegen**: U kunt maximaal twee segmenten toevoegen door de operatoren AND of OR te gebruiken om ze aan de tabel toe te voegen. Kijk wat er met de tabel gebeurt wanneer u mobiele gebruikers OF koninklijke bezoekers toevoegt. Ze zijn naast elkaar, boven de metriek. Als u Mobiele Gebruikers EN Weergavebezoekers toevoegt, ziet u de resultaten van beide segmenten samen en worden deze op elkaar gestapeld in de tabel.

   ![](assets/qibuilder7.png)

## Bekende beperkingen

Als u rechtstreeks in de tabel probeert te bewerken, wordt de opdracht [!UICONTROL Quick Insights] niet meer gesynchroniseerd. U kunt de vorige versie herstellen [!UICONTROL Quick Insights] instellingen door te klikken **[!UICONTROL Resync Builder]** rechtsboven in het deelvenster.

![](assets/qibuilder9.png)

Er verschijnt een waarschuwing voordat u iets rechtstreeks aan de tabel toevoegt:

![](assets/qibuilder8.png)

Anders, zal het bouwen direct de lijst ertoe brengen om zich nu als traditionele lijst van de Vrije vorm te gedragen, zonder de nuttige eigenschappen voor nieuwe gebruikers.

