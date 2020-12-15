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
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

>[!IMPORTANT]
>
>**[!UICONTROL Quick Insights]** momenteel wordt slechts beperkt getest. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

[!UICONTROL Quick Insights] biedt richtlijnen voor niet-analisten en nieuwe gebruikers van [!UICONTROL Analysis Workspace] over hoe ze zakelijke kwesties snel en eenvoudig kunnen beantwoorden. Het is ook een geweldig hulpmiddel voor geavanceerde gebruikers die snel een eenvoudige vraag willen beantwoorden zonder zelf een tabel te hoeven maken.

Wanneer u voor het eerst deze [!UICONTROL Analysis Workspace] gaat gebruiken, vraagt u zich wellicht af welke visualisaties het nuttigst zouden zijn, welke dimensies en metriek inzichten zouden kunnen vergemakkelijken, waar items moeten worden gesleept en neergezet, waar een segment moet worden gemaakt, enz.

Om dit te helpen, en gebaseerd op het gebruik van uw eigen bedrijf van gegevenscomponenten in [!UICONTROL Analysis Workspace], gebruikt [!UICONTROL Quick Insights] een algoritme dat u met de populairste afmetingen, metriek, segmenten, en datumwaaiers zal voorstellen uw bedrijf gebruikt. In feite, zult u afmetingen, metriek, en segmenten die als [!UICONTROL Popular] worden geëtiketteerd in de drop-down lijst zien, zoals hier getoond:

![](assets/popular-tag.png)

[!UICONTROL Quick Insights] helpt u

* U moet een gegevenstabel en een bijbehorende visualisatie op de juiste wijze maken in [!UICONTROL Analysis Workspace].
* Leer de terminologie en woordenschat voor basiscomponenten en stukken van [!UICONTROL Analysis Workspace].
* Doe eenvoudige onderverdelingen van dimensies, voeg veelvoudige metriek toe, of vergelijk segmenten gemakkelijk binnen [!UICONTROL Freeform table].
* U kunt verschillende visualisatietypen wijzigen of uitproberen om snel en intuïtief het zoekgereedschap voor uw analyse te vinden.

## Basistoets

Hier volgen enkele basistermen die u bekend moet maken. Elke gegevenslijst bestaat uit 2 of meer bouwstenen (componenten) die u gebruikt om uw gegevensverhaal te vertellen.

| Bouwsteen (component) | Definitie |
|---|---|
| [!UICONTROL Dimension] | Dimension zijn beschrijvingen of kenmerken van metrische gegevens die kunnen worden bekeken, opgesplitst en vergeleken in een project. Het zijn niet-numerieke waarden en datums die worden opgesplitst in dimensie-items. Bijvoorbeeld &#39;browser&#39; of &#39;pagina&#39; zijn afmetingen. |
| [!UICONTROL Dimension item] | Dimension-items zijn afzonderlijke waarden voor een dimensie. Dimensie-items voor de afmetingen van de browser zijn bijvoorbeeld &quot;Chrome&quot;, &quot;Firefox&quot;, &quot;Edge&quot;, enzovoort. |
| [!UICONTROL Metric] | De metriek zijn kwantitatieve informatie over bezoekersactiviteit, zoals meningen, klik-door, herladingen, gemiddelde bestede tijd, eenheden, orden, opbrengst, etc. |
| [!UICONTROL Visualization] | De werkruimte biedt [een aantal visualisaties](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) aan om visuele vertegenwoordiging van uw gegevens, zoals bar grafieken, donut grafieken, histogrammen, lijngrafieken, kaarten, scatterpercelen, en anderen te bouwen. |
| [!UICONTROL Dimension Breakdown] | Een afbraak van dimensies is een manier om een dimensie letterlijk op andere dimensies in te delen. In ons voorbeeld kunt u de VS-staten opsplitsen op mobiele apparaten om de bezoeken aan mobiele apparaten per status op te halen, of u kunt mobiele apparaten opsplitsen op typen mobiele apparaten, op regio&#39;s, op interne campagnes, enz. |
| [!UICONTROL Segment] | Met segmenten kunt u subsets van bezoekers identificeren op basis van kenmerken of interacties van websites. U kunt bijvoorbeeld [!UICONTROL Visitor]-segmenten maken op basis van kenmerken: browsertype, apparaat, aantal bezoeken, land, geslacht of op basis van interacties: campagnes, sleutelwoordonderzoek, onderzoeksmotor, of gebaseerd op uitgang en ingangen: bezoekers van Facebook, een gedefinieerde bestemmingspagina, een verwijzend domein of gebaseerd op aangepaste variabelen: formulierveld, gedefinieerde categorieën, klant-id. |

## Aan de slag met Quick Insights

1. Meld u aan bij Adobe Analytics met de gegevens die u hebt ontvangen.
1. Ga naar [!UICONTROL Workspace], klik **[!UICONTROL Create New Project]** en klik dan **[!UICONTROL Quick Insights]**. (U kunt dit deelvenster ook openen via het menu **[!UICONTROL Panel]** in de linkertrack.)

   ![](assets/qibuilder.png)

   ![](assets/qi-panel.png)

1. Wanneer u begint uit, doorloop de korte zelfstudie die u enkele basisbeginselen van [!UICONTROL Quick Insights panel] leert. Of klik op **[!UICONTROL Skip Tutorial]**.
1. Selecteer de bouwstenen (ook wel componenten genoemd): afmetingen (oranje), metriek (groen), segmenten (blauw), of datumwaaiers (paars) U moet minstens één afmeting en één metrisch selecteren voor een lijst die automatisch moet worden gebouwd.

   ![](assets/qibuilder2.png)

   U kunt de bouwstenen op drie manieren selecteren:
   * Sleep en zet ze neer vanaf de linkerspoorstaaf.
   * Als u weet wat u zoekt: Begin te typen en [!UICONTROL Quick Insights] vult de spaties voor u in.
   * Klik op de vervolgkeuzelijst en zoek in de lijst.

1. Wanneer u minstens één afmeting en één metrisch hebt toegevoegd, zal het volgende voor u worden gecreeerd:

   * Een tabel met vrije vorm met de afmetingen (hier, Amerikaanse staten) verticaal en de metrische waarde (hier, Visit) horizontaal boven. Bekijk deze tabel:

   ![](assets/qibuilder3.png)

   * Een begeleidende visualisatie, in dit geval a [bar grafiek](/help/analysis-workspace/visualizations/bar.md). De gegenereerde visualisatie is gebaseerd op het type gegevens dat u aan de tabel hebt toegevoegd. Op tijd gebaseerde gegevens (zoals [!UICONTROL Visits] per dag/maand) worden standaard ingesteld op een [!UICONTROL Line]-grafiek. Alle gegevens die niet op een tijdstip zijn gebaseerd (zoals [!UICONTROL Visits] per [!UICONTROL Device]) worden standaard ingesteld op een [!UICONTROL Bar]-grafiek. U kunt het type visualisatie wijzigen door op de vervolgkeuzepijl naast het visualisatietype te klikken.


1. (Optioneel) U kunt de dimensies uitvouwen en elementen van de dimensie bekijken door op de pijl-rechts naast de dimensie te klikken.

1. Voeg meer verfijningen toe zoals hieronder beschreven onder &quot;Meer tips.&quot;

1. Sla uw project op door op **[!UICONTROL Project > Save]** te klikken.

## Meer tips

Andere handige tips verschijnen in de [!UICONTROL Quick Insights Builder], sommige afhankelijk van de laatste handeling.

* Voltooi eerst de **[!UICONTROL More tips]**-zelfstudie: Via de Help (?) pictogram naast de [!UICONTROL Quick Insights] titel. Dit leerprogramma toont omhoog 24 uren nadat u een project met minstens één afmeting en één metrisch hebt gecreeerd.

   ![](assets/qibuilder4.png)

* **Uitsplitsing naar**: U kunt tot 3 niveaus van onderverdelingen op dimensies gebruiken om neer tot de gegevens te boren u echt nodig hebt.

   ![](assets/qibuilder5.png)

* **Meer metriek** toevoegen: U kunt tot 2 meer metriek toevoegen door te gebruiken EN exploitant om hen toe te voegen de lijst.

   ![](assets/qibuilder6.png)

* **Meer segmenten** toevoegen: U kunt maximaal twee segmenten toevoegen door de operatoren AND of OR te gebruiken om ze aan de tabel toe te voegen. Kijk wat er met de tabel gebeurt wanneer u mobiele gebruikers OF koninklijke bezoekers toevoegt. Ze zijn naast elkaar, boven de metriek. Als u Mobiele Gebruikers EN Weergavebezoekers toevoegt, ziet u de resultaten van beide segmenten samen en worden deze op elkaar gestapeld in de tabel.

   ![](assets/qibuilder7.png)

## Bekende beperkingen

Als u probeert om direct binnen de lijst uit te geven, zal het [!UICONTROL Quick Insights] paneel om uit synchroon worden. U kunt de vorige [!UICONTROL Quick Insights]-instellingen herstellen door op **[!UICONTROL Resync Builder]** rechtsboven in het deelvenster te klikken.

![](assets/qibuilder9.png)

Er verschijnt een waarschuwing voordat u iets rechtstreeks aan de tabel toevoegt:

![](assets/qibuilder8.png)

Anders, zal het bouwen direct de lijst ertoe brengen om zich nu als traditionele lijst van de Vrije vorm te gedragen, zonder de nuttige eigenschappen voor nieuwe gebruikers.

