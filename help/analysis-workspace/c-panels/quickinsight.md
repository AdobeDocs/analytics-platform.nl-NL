---
description: Quick Insights is een hulpmiddel voor nieuwe Workspace-gebruikers dat hen begeleidt bij het samenstellen van gegevenstabellen en -visualisaties
title: Deelvenster Snelle inzichten
feature: Panels
exl-id: 09ebc3af-34ac-4f1f-8a5d-90da008f8697
role: User
source-git-commit: a62ac798da9d66fa3d88262ef7d04aa4bf6a3303
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 1%

---

# Deelvenster Snelle inzichten {#quick-insights-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_quickinsights_button"
>title="Snelle inzichten"
>abstract="Maak een deelvenster om snel een vrije-vormtabel te maken en de bijbehorende visualisatie om inzichten sneller te analyseren en zichtbaar te maken."

<!-- markdownlint-enable MD034 -->


[!UICONTROL Quick Insights] biedt richtlijnen voor niet-analisten en nieuwe gebruikers van [!UICONTROL Analysis Workspace] over hoe ze zakelijke kwesties snel en eenvoudig kunnen beantwoorden. Het is ook een geweldig hulpmiddel voor geavanceerde gebruikers die snel een eenvoudige vraag willen beantwoorden zonder zelf een tabel te hoeven maken.

Wanneer u deze [!UICONTROL Analysis Workspace] voor het eerst gebruikt, vraagt u zich misschien af:

* welke visualisaties het nuttigst zouden zijn,
* welke dimensies en maatstaven inzichten zouden kunnen vergemakkelijken;
* waar items moeten worden gesleept en neergezet,
* de plaats waar een filter moet worden gemaakt;
* en meer.

Om met deze vragen te helpen, [!UICONTROL Quick insights] hefboomwerkingen een algoritme dat u met de populairste dimensies, metriek, filters, en datumwaaiers uw bedrijfgebruik voorstelt. Dit algoritme is gebaseerd op het gebruik van gegevenscomponenten in [!UICONTROL Analysis Workspace] door uw eigen bedrijf. In feite ziet u dimensies, metriek en filter getagd met [!UICONTROL POPULAR] in de vervolgkeuzelijst, zoals u hier ziet:

![ het Snelle paneel van Inzichten.](assets/popular-tag.png)

[!UICONTROL Quick Insights] helpt u

* U moet een gegevenstabel en een bijbehorende visualisatie op de juiste wijze maken in [!UICONTROL Analysis Workspace] .
* Leer de terminologie en woordenschat voor basiscomponenten en stukken van [!UICONTROL Analysis Workspace].
* Voer eenvoudige dimensies uit, voeg meerdere metriek toe of vergelijk filters eenvoudig binnen een [!UICONTROL Freeform table] .
* U kunt verschillende visualisatietypen wijzigen of uitproberen om snel en intuïtief het zoekgereedschap voor uw analyse te vinden.

## Basistoets

Hieronder volgen enkele basistermen die u bekend moet maken. Elke gegevenslijst bestaat uit 2 of meer bouwstenen (componenten) die u gebruikt om uw gegevensverhaal te vertellen.

| Bouwsteen (component) | Definitie |
|---|---|
| **[!UICONTROL Dimension]** | Dimensionen zijn beschrijvingen of kenmerken van metrische gegevens die kunnen worden bekeken, opgesplitst en vergeleken in een project. Het zijn niet-numerieke waarden en datums die worden opgesplitst in dimensie-items. Bijvoorbeeld, *browser* of *pagina* is een afmeting. |
| **[!UICONTROL Dimension item]** | Items van een Dimension zijn afzonderlijke waarden voor een dimensie. Bijvoorbeeld, zouden de afmetingspunten voor de browser afmeting *Chrome* zijn, *Firefox*, *Edge*, of anderen. |
| [!UICONTROL Metric] | De metriek zijn kwantitatieve informatie over persoonactiviteit, zoals meningen, klik-door, herladingen, gemiddelde tijd besteed, eenheden, orden, opbrengst, etc. |
| **[!UICONTROL Visualization]** | Workspace biedt [ een aantal visualisaties ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) aan om visuele vertegenwoordiging van uw gegevens te bouwen. Bijvoorbeeld staafgrafieken, donutgrafieken, histogrammen, lijngrafieken, kaarten, scatterpercelen en andere. |
| **[!UICONTROL Dimension Breakdown]** | Een uitsplitsing naar dimensie is een manier om een dimensie naar andere dimensies uit te splitsen. U kunt bijvoorbeeld de VS-staten opdelen door Mobiele apparaten om de bezoeken aan mobiele apparaten per status op te halen. Of u kunt mobiele apparaten onderbreken op typen mobiele apparaten, op regio&#39;s, op interne campagnes en nog veel meer. |
| **[!UICONTROL Filter]** | Met filters kunt u subsets van personen identificeren op basis van eigenschappen of interacties van websites. U kunt bijvoorbeeld [!UICONTROL People] -filters maken op basis van <li>kenmerken: browsertype, apparaat, aantal bezoeken, land, geslacht of</li><li>interacties: campagnes, sleutelwoordzoeker, zoekmachine, of</li><li>uitgang en binnenkomst: personen uit Facebook, een bepaalde landingspagina, een verwijzend domein, of</li><li> aangepaste variabelen: formulierveld, gedefinieerde categorieën, klant-id. |

## Gebruiken

Een deelvenster **[!UICONTROL Quick insights]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Quick insights]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [ een paneel ](panels.md#create-a-panel) creëren.

1. Wanneer u een **[!UICONTROL Quick insights]** -deelvenster voor het eerst gebruikt, wilt u wellicht de korte [!UICONTROL Intro tutorial] doorlopen die u een aantal basisbeginselen leert. Selecteer ![ HelpOutline ](/help/assets/icons/HelpOutline.svg) naast de Snelle titel van het deelvenster Inzichten en selecteer **[!UICONTROL Intro tutorial]** van popup.

1. Specificeer de [ input ](#panel-input) voor het paneel.

1. Neem de [ output ](#panel-output) voor het paneel waar.


### Deelvensterinvoer

Selecteer uw bouwstenen:

* **[!UICONTROL Analyze]** - specificeer een afmeting (oranje)
* **[!UICONTROL by]** - geef een metrische waarde op (groen)
* **[!UICONTROL filter by]** - een filter opgeven (blauw)
* **[!UICONTROL on]** - geef een datumbereik op (paars).

U moet ten minste één afmeting en één metrisch selecteren om de visualisatie goed te laten functioneren.



U kunt de bouwstenen op drie manieren specificeren:

* Componenten slepen en neerzetten vanuit het linkerdeelvenster.
* Begin in één van de bouwsteengebieden te typen. Wanneer invoer wordt gevonden, vult het bouwsteengebied met mogelijke waarden automatisch.
* Specificeer een bouwsteendrop-down (bijvoorbeeld `Country` in **[!UICONTROL Analyze]**) en onderzoek de lijst van mogelijke waarde (gebruikend ![ ChevronRight ](/help/assets/icons/ChevronRight.svg)) voor de waarde u (bijvoorbeeld, **[!UICONTROL Country code]**) wilt gebruiken.

Selecteer **[!UICONTROL Clear]** om alle invoervelden te wissen.


### Deelvensteruitvoer

1. Wanneer u minstens één afmeting en één metrisch hebt toegevoegd, kunt u de resultaten zien.

   ![ de Freeform lijst die de afmeting verticaal en metrisch horizontaal toont.](assets/quick-insights-output.png)

   * Een tabel met vrije vorm met de afmetingen (landcode) en metrisch (sessies), gefilterd door websessies voor de laatste twaalf maanden.

   * Een begeleidende visualisatie, in dit geval a [ staafgrafiek ](/help/analysis-workspace/visualizations/bar.md). De gegenereerde visualisatie is gebaseerd op het type gegevens dat u aan de tabel hebt toegevoegd. Op tijd gebaseerde gegevens (zoals [!UICONTROL Sessions] per dag/maand) worden standaard ingesteld op een [!UICONTROL Line] -diagram. Niet-tijdgebonden gegevens (zoals [!UICONTROL Sessions] per [!UICONTROL Device] ) worden standaard omgezet in een [!UICONTROL Bar] -grafiek. U kunt het type visualisatie wijzigen door op de vervolgkeuzepijl naast het visualisatietype te klikken.

1. Probeer toevoegend sommige meer verfijningen zoals hieronder beschreven onder [ Meer uiteinden ](#more-tips)

1. Mogelijk wilt u uw project opslaan met **[!UICONTROL Project > Save]** .

## Meer tips

Er verschijnen andere handige tips in de [!UICONTROL Quick Insights Builder] , waarvan sommige afhankelijk zijn van de laatste handeling.

* Eerst wilt u mogelijk de zelfstudie van **[!UICONTROL More tips]** voltooien. Dit leerprogramma toont omhoog 24 uren nadat u een project met minstens één afmeting en één metrisch hebt gecreeerd. Selecteer ![ HelpOutline ](/help/assets/icons/HelpOutline.svg) naast de Snelle titel van het deelvenster Inzichten en selecteer **[!UICONTROL More tips]** van popup.

  ![ het Snelle bericht van het Comité van Inzichten getoond nadat u het pictogram van de Hulp selecteert.](assets/qibuilder4.png)

* U kunt meerdere afmetingen en maatstaven analyseren, filters combineren of vergelijken en een datumbereik opgeven:

  ![ het Resultaat van de Bouwer van Snelle Inzichten ](assets/qibuilder-result.png)

   * **[!UICONTROL Analyze]** afmetingen **[!UICONTROL Broken-Down by]** : u kunt maximaal 3 niveaus van onderverdelingen op dimensies gebruiken om naar de gegevens te gaan die u echt nodig hebt. Zie ➊, ➋ en ➌.

   * Meer metriek toevoegen **[!UICONTROL by]**: u kunt maximaal twee metriek toevoegen. Zie ➍ en ➎.

   * **[!UICONTROL filter by]**: u kunt maximaal twee filters toevoegen. Voeg bijvoorbeeld Boeken als filter toe en combineer dat filter met de filters Frequent Bookers en First Time Flyers die u vergelijkt. Zie ➏, ➐ en ➑.

   * op: U kunt het datumbereik opgeven. Zie ➒.

## Bekende beperkingen

Als u probeert rechtstreeks in de tabel te bewerken, is het deelvenster [!UICONTROL Quick Insights] mogelijk niet meer synchroon. Selecteer **[!UICONTROL Resync Builder]** rechtsboven in het deelvenster om de vorige [!UICONTROL Quick Insights] -instellingen te herstellen.

U krijgt een waarschuwing voordat u iets rechtstreeks aan de tabel toevoegt:

![ De de optieswaarschuwing van de Bouwer van de Wedersynchronisatie.](assets/qibuilder-outofsync.png)

Anders, veroorzaakt het bouwen direct de lijst om zich als traditionele lijst van de Vrije vorm te gedragen, zonder de nuttige eigenschappen voor nieuwe gebruikers.


>[!MORELIKETHIS]
>
>[ creeer een paneel ](/help/analysis-workspace/c-panels/panels.md#create-a-panel)
>