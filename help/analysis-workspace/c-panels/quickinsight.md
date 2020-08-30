---
description: De snelle Inzichten zijn een hulpmiddel voor nieuwe gebruikers van de Werkruimte die hen in de bouw van gegevenslijsten en visualisaties begeleidt
title: deelvenster Snelle inzichten
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 2%

---


# deelvenster Snelle inzichten

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

>[!IMPORTANT]
>
>**[!UICONTROL Quick Insights]** het panel wordt momenteel beperkt getest . [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

[!UICONTROL Quick Insights] biedt richtlijnen voor niet-analisten en nieuwe gebruikers van [!UICONTROL Analysis Workspace] over hoe ze zakelijke kwesties snel en eenvoudig kunnen beantwoorden. Het is ook een geweldig hulpmiddel voor geavanceerde gebruikers die een eenvoudige vraag snel willen beantwoorden zonder het moeten zelf een lijst bouwen.

Wanneer u dit voor het eerst begint te gebruiken [!UICONTROL Analysis Workspace], zou u zich kunnen afvragen welke visualisaties het nuttigst zouden zijn, welke afmetingen en metriek inzicht zouden kunnen vergemakkelijken, waar te om punten te slepen en te laten vallen, waar te om een segment te creëren, enz.

Om hierbij te helpen, en gebaseerd op het gebruik van gegevenscomponenten in uw eigen bedrijf [!UICONTROL Analysis Workspace], [!UICONTROL Quick Insights] hefboomwerkingen een algoritme dat u met de populairste afmetingen, de metriek, de segmenten, en de datumwaaiers uw bedrijf zal voorstellen. In feite, zult u afmetingen, metriek, en segmenten zien die zoals worden geëtiketteerd [!UICONTROL Popular] in de vervolgkeuzelijst, zoals hieronder getoond:

![](assets/popular-tag.png)

[!UICONTROL Quick Insights] helpt u

* Stel op de juiste manier een datatabel en een bijbehorende visualisatie in [!UICONTROL Analysis Workspace].
* Leer de terminologie en de woordenschat voor basiscomponenten en stukken van [!UICONTROL Analysis Workspace].
* Doe eenvoudige onderverdelingen van afmetingen, voeg veelvoudige metriek toe, of vergelijk gemakkelijk segmenten binnen a [!UICONTROL Freeform table].
* Verander of probeer diverse visualisatietypen uit om het vondsthulpmiddel voor uw analyse snel en intuïtief te vinden.

## Basisterminologie

Na zijn enkele basistermijnen u met vertrouwd moet zijn. Elke gegevenslijst bestaat uit 2 of meer bouwstenen (componenten) die u gebruikt om uw gegevensverhaal te vertellen.

| Bouwsteen (component) | Definitie |
|---|---|
| [!UICONTROL Dimension] | De afmetingen zijn beschrijvingen of kenmerken van metrische gegevens die kunnen worden bekeken, worden verdeeld, en in een project worden vergeleken. Zij zijn niet-numerieke waarden en data die in afmetingspunten opsplitsen. Bijvoorbeeld, &quot;browser&quot;, of &quot;pagina&quot;zijn afmetingen. |
| [!UICONTROL Dimension item] | De punten van de dimensie zijn individuele waarden voor een afmeting. Bijvoorbeeld, zouden de afmetingspunten voor de browser afmeting &quot;Chrome&quot;, &quot;Firefox&quot;, &quot;Edge&quot;, enz. zijn. |
| [!UICONTROL Metric] | De metriek zijn kwantitatieve informatie over bezoekersactiviteit, zoals meningen, klik-door:sturen, herladingen, gemiddelde bestede tijd, eenheden, orden, opbrengst, etc. |
| [!UICONTROL Visualization] | Werkruimte biedt [een aantal visualisaties](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) om visuele vertegenwoordiging van uw gegevens, zoals bargrafieken, donutgrafieken, histogrammen, lijngrafieken, kaarten, scatterbanen, en anderen te bouwen. |
| [!UICONTROL Dimension Breakdown] | Een afbraak van de dimensie is een manier om een dimensie letterlijk door andere dimensies af te breken. In ons voorbeeld, kon u Amerikaanse Staten door Mobiele Apparaten onderbreken om de mobiele apparatenbezoeken per staat te krijgen, of u kon Mobiele Apparaten onderbreken door de Mobiele types van Apparaat, door Gebieden, door Interne Campagnes, enz. |
| [!UICONTROL Segment] | De segmenten laten u ondergroepen van bezoekers identificeren die op kenmerken of websiteinteractie worden gebaseerd. Bijvoorbeeld, kunt u bouwen [!UICONTROL Visitor] segmenten op basis van kenmerken: browser type, apparaat, aantal bezoeken, land, geslacht, of gebaseerd op interactie: campagnes, sleutelwoordonderzoek, zoekmachine, of gebaseerd op uitgangen en ingangen: bezoekers van Facebook, een bepaalde landingspagina, verwijzend domein, of gebaseerd op douanevariabelen: formulierveld, gedefinieerde categorieën, klant-id. |

## Aan de slag met Quick Insights

1. Login aan de Analyse van Adobe gebruikend de geloofsbrieven u met bent verstrekt.
1. Ga naar [!UICONTROL Workspace] en klik op **[!UICONTROL Create New Project]** en klik vervolgens op **[!UICONTROL Quick Insights]**. (U kunt tot dit paneel van het **[!UICONTROL Panel]** menu in de linkerspoorstaaf.)

   ![](assets/qibuilder.png)

   ![](assets/qi-panel.png)

1. Als je voor het eerst uitstapt, ga dan door de korte training die je een paar van de [!UICONTROL Quick Insights panel] basiskennis. Of, klik aan **[!UICONTROL Skip Tutorial]**.
1. Selecteer uw bouwstenen (ook wel componenten genoemd): afmetingen (oranje), metriek (groen), segmenten (blauw), of datumwaaiers (paars) U moet minstens één afmeting en één metrisch voor een lijst selecteren die automatisch moet worden gebouwd.

   ![](assets/qibuilder2.png)

   U hebt drie manieren om de bouwstenen te selecteren:
   * Sleep deze vanuit de linkerrail.
   * Als je weet wat je zoekt: Het typen van het begin en [!UICONTROL Quick Insights] zal de spaties voor je invullen.
   * Klik op de vervolgkeuzelijst en zoek de lijst.

1. Wanneer u minstens één afmeting en metrisch hebt toegevoegd, zal het volgende voor u worden gecreeerd:

   * Een lijst Freeform met de afmeting (hier, de Staten van de V.S.) verticaal en metrisch (hier, Bezoeken) horizontaal bij de bovenkant. Bekijk deze tabel:

   ![](assets/qibuilder3.png)

   * Een begeleidende visualisatie, in dit geval een [staafdiagram](/help/analysis-workspace/visualizations/bar.md). De visualisatie die wordt geproduceerd is gebaseerd op het type van gegevens u aan de lijst toevoegde. Om het even welke op tijd-gebaseerde gegevens (zoals [!UICONTROL Visits] per dag/maand) standaard op een [!UICONTROL Line] grafiek. Alle niet-tijdgebonden gegevens (zoals [!UICONTROL Visits] per [!UICONTROL Device]) standaard op een [!UICONTROL Bar] grafiek. U kunt het type visualisatie veranderen door op de drop-down pijl naast het visualisatietype te klikken.


1. (Facultatief) boor neer op afmetingen en zie afmetingspunten door de > juist-pijl naast de afmeting te klikken.

1. Probeer meer verfijningen toe te voegen zoals hieronder beschreven onder &quot;Meer tips.&quot;

1. Sparen uw project door te klikken **[!UICONTROL Project > Save]**.

## Meer tips

Andere nuttige wenken zullen in [!UICONTROL Quick Insights Builder], sommige afhankelijk van je laatste actie.

* Eerst, voltooi **[!UICONTROL More tips]** zelfstudie: Toegang tot het systeem via de Help (?) pictogram naast het [!UICONTROL Quick Insights] titel. Dit leerprogramma toont omhoog 24 uren nadat u een project met minstens één metrische dimensie en hebt gecreeerd.

   ![](assets/qibuilder4.png)

* **Uitsplitsing naar**: U kunt tot 3 niveaus van onderverdelingen op afmetingen gebruiken neer aan de gegevens boren u werkelijk wenst.

   ![](assets/qibuilder5.png)

* **Meer maatstaven toevoegen**: U kunt tot 2 meer metriek toevoegen door te gebruiken EN exploitant om hen de lijst toe te voegen.

   ![](assets/qibuilder6.png)

* **Meer segmenten toevoegen**: U kunt tot 2 meer segmenten toevoegen door TE gebruiken EN of OF exploitanten om hen de lijst toe te voegen. Bekijk wat aan de lijst gebeurt wanneer u Mobiele Gebruikers OF de Bezoekers van de Verbeelding toevoegt. Ze zijn naast elkaar, boven de maatstaven. Als u de Mobiele Gebruikers en de Bezoekers van de Vergroting toevoegde, zou u resultaten van beide segmenten samen zien, en zij zouden bovenop elkaar in de lijst worden gestapeld.

   ![](assets/qibuilder7.png)

## Bekende beperkingen

Als u probeert om direct binnen de lijst uit te geven, zal het veroorzaken [!UICONTROL Quick Insights] paneel om uit synchronisatie te raken. U kunt het terugzetten naar de vorige [!UICONTROL Quick Insights] instellingen door te klikken op **[!UICONTROL Resync Builder]** rechtsboven in het paneel.

![](assets/qibuilder9.png)

U zult een waarschuwing alvorens om het even wat aan de lijst direct toe te voegen krijgen:

![](assets/qibuilder8.png)

Anders, zal de bouw direct de lijst veroorzaken om zich nu als traditionele lijst Freeform, zonder de nuttige eigenschappen voor nieuwe gebruikers te gedragen.

