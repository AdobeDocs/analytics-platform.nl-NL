---
description: Een overzicht van het gebruik van standaardsjablonen in Analysis Workspace.
title: Sjablonen gebruiken
feature: Workspace Basics
role: User, Admin
hide: true
hidefromtoc: true
exl-id: d61f215d-9089-4014-9c5a-97f5d7134f34
source-git-commit: 065230672137c98015680e4a033a2f5ac3a1bc24
workflow-type: tm+mt
source-wordcount: '19283'
ht-degree: 0%

---

# Sjablonen gebruiken

Sjablonen (of bedrijfssjablonen) in Analysis Workspace bieden snel inzicht in de meest voorkomende rapportscenario&#39;s. Hieronder volgen enkele voorbeelden van vragen die u kunt beantwoorden met sjablonen:

* Hoeveel personen bezoeken uw site
* Hoeveel van deze bezoekers zijn unieke bezoekers (slechts eenmaal geteld)
* Hoe ze naar de site kwamen (bijvoorbeeld of ze een link volgden of er direct naartoe kwamen)
* Trefwoorden die bezoekers hebben gebruikt om site-inhoud te zoeken
* Hoe lang bezoekers op een bepaalde pagina of op de gehele site verbleven
* Welke verbindingen bezoekers klikte, en wanneer zij de plaats verlieten
* Welke marketingkanalen het meest effectief zijn bij het genereren van inkomsten of conversiegebeurtenissen
* Hoeveel tijd hebben ze besteed aan het bekijken van een video
* Welke browsers en apparaten zij gebruikten om uw plaats te bezoeken

De volgende informatie beschrijft hoe u sjablonen kunt openen en gebruiken via het tabblad [!UICONTROL Templates] in Analysis Workspace.

## Een sjabloon openen en uitvoeren

1. In Analysis Workspace, selecteer [!UICONTROL **Workspace**] tabel.

   ![ lusjes van Malplaatjes ](assets/view-prebuilt-templates.png)

1. In de [!UICONTROL **sectie van Malplaatjes**], selecteer één van beiden van de volgende lusjes:

   * **[!UICONTROL Adobe templates]**: geeft alle sjablonen weer die door de Adobe worden aangeboden.

   * **[!UICONTROL _login_company_name _malplaatjes]**: Toont alle bedrijfmalplaatjes die voor uw organisatie zijn gecreeerd.

     De malplaatjes van het bedrijf kunnen slechts door een beheerder worden gecreeerd. Voor informatie over hoe te om een bedrijfmalplaatje tot stand te brengen, zie [ malplaatjes ](/help/analysis-workspace/templates/create-templates.md) creëren en beheren.

1. Gebruik een van de volgende opties om de weergave van de beschikbare sjablonen te wijzigen:

   * Kies of om malplaatjes in een kolommening of een kaartmening te bekijken door of het pictogram van de kolommening ![ kolommening ](assets/column-view-icon.png) of het pictogram van de kaartmening ![ kaartmening ](assets/card-view-icon.png) te selecteren.

   * Wanneer het gebruiken van het pictogram van de kaartmening ![ kaartmening ](assets/card-view-icon.png), kies van de volgende soortorden: **[!UICONTROL Most recently used]**, **[!UICONTROL Most popular]**, **[!UICONTROL Alphabetical]**, **[!UICONTROL Categorical]**.

1. Typ in het zoekveld de naam van de sjabloon die u wilt zoeken en selecteer deze in de lijst met sjablonen.

   of

   Selecteer de sjablooncategorie die u wilt weergeven en selecteer vervolgens de sjabloon in de lijst met sjablonen.

   >[!TIP]
   >
   >Als u met de pijltoetsen door het menu wilt navigeren, drukt u op de toets Volgende schuine streep (/) en vervolgens op de toets Pijl-omlaag. Druk op Enter om de geselecteerde sjabloon te laden.

   Voor een lijst van malplaatjes die beschikbaar zijn, zie de [ Beschikbare malplaatjes ](#available-templates) hieronder sectie.

1. (Optioneel) U kunt sjablonen weergeven die componenten bevatten die niet beschikbaar zijn in de gegevensweergave. (Door gebrek, worden de malplaatjes getoond slechts als zij componenten gebruiken die in uw gegevensmening beschikbaar zijn.)

   >[!NOTE]
   >
   >   Voordat u deze sjablonen kunt gebruiken, moet een beheerder eerst de vereiste contextlabels voor deze ontbrekende componenten toevoegen aan de gegevensweergave. Voor meer informatie, zie [ ontbrekende componenten aan de gegevensmening voor een bepaald malplaatje ](/help/analysis-workspace/templates/create-templates.md#add-missing-components-to-the-data-view-for-a-given-template) in [ malplaatjes van het Gebruik ](/help/analysis-workspace/templates/create-templates.md) toevoegen.

   1. Selecteer het filterpictogram.

   1. Selecteer **[!UICONTROL Not ready for use]** om sjablonen weer te geven waarvoor extra componenten nodig zijn.

      ![ Gebruik een malplaatje dat componenten ](assets/template-not-ready.png) mist

1. Selecteer het malplaatje om een rapport tot stand te brengen dat op het malplaatje wordt gebaseerd u koos.

1. (Voorwaardelijk) Als de sjabloon componenten bevat die niet beschikbaar zijn in de gegevensweergave, wordt het dialoogvenster Niet-compatibele gegevensweergave weergegeven. Hierin wordt aangegeven dat de gegevensweergave niet compatibel is met de sjabloon en wordt aangegeven welke componenten ontbreken.

   Voer een van de volgende handelingen uit:

   * Kies een andere gegevensweergave in de vervolgkeuzelijst **[!UICONTROL Change data view]** .

   * Selecteer **[!UICONTROL Continue anyway]** om de sjabloon met de ontbrekende componenten weer te geven.

## Een project maken op basis van een sjabloon {#use-reports}

Een sjabloon past mogelijk niet precies aan uw wensen aan, maar het kan u sluiten. In deze gevallen kunt u de sjabloon gebruiken als beginpunt voor uw project en deze vervolgens aanpassen aan uw specifieke doelen.

Als u na het aanbrengen van wijzigingen weg navigeert van een sjabloon, wordt u gevraagd om de wijzigingen op te slaan of te negeren. Als u wijzigingen in een sjabloon opslaat, wordt de sjabloon als een nieuw project opgeslagen.

Een sjabloon aanpassen en opslaan als project:

1. In Customer Journey Analytics, selecteer [!UICONTROL **Workspace**] tabel.

1. Selecteer de [!UICONTROL **Malplaatjes**] tabel.

1. Selecteer de sjabloon die u wilt weergeven. Bijvoorbeeld, onder [!UICONTROL **het populairste**], selecteer het [!UICONTROL **malplaatje van Pagina&#39;s**].

   Het malplaatje van Pagina&#39;s, zoals getoond in Analysis Workspace, toont twee [ visualisaties ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) ([ grafiek van de Bar ](/help/analysis-workspace/visualizations/bar.md) en [ Samenvattingsaantal ](/help/analysis-workspace/visualizations/summary-number-change.md)) en a [ lijst van de Vrije vorm ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md). De gebruikte metrische waarde is Voorvallen.

   <!--update screenshot. The following is AA -->

   ![ malplaatje van Pagina&#39;s ](assets/pages-report.png)

1. Voer een van de volgende handelingen uit:

   * De sjabloon weergeven.
   * Sleep een of meer filters naar de neerzetzone van het filter bovenaan. Bijvoorbeeld, sleep de filter [!UICONTROL **Mobiele Klanten**] en bekijk de resultaten.
   * Wijzig het datumbereik door naar de kalender in de rechterbovenhoek te gaan.
   * Voeg afmetingsonderverdelingen toe, sleep in andere metriek, en pas over het algemeen het malplaatje aan uw behoeften aan.

1. (Facultatief) sparen het malplaatje als project door [!UICONTROL **Project**] te selecteren > [!UICONTROL **sparen**].

   De sjabloon wordt als een nieuw project opgeslagen; de bestaande sjabloon wordt niet gewijzigd. Voor meer informatie over het bewaren van projecten, zie [ projecten ](/help/analysis-workspace/build-workspace-project/save-projects.md) sparen.

## Beschikbare sjablonen

Alle beschikbare vooraf gebouwde sjablonen openen:

1. In Adobe Analytics, selecteer het [!UICONTROL **Workspace**] lusje, dan selecteren de [!UICONTROL **Malplaatjes**] tabel.

   Vooraf samengestelde sjablonen worden ingedeeld per categorie.

   <!--add screenshot-->

1. Selecteer een categorie om de sjablonen in die categorie weer te geven.

   De volgende secties komen overeen met de beschikbare categorieën en verschaffen informatie over elke template.

   * [[!UICONTROL ](#most-popular)

   * [[!UICONTROL ](#engagement)

   * [[!UICONTROL ](#web-conversion)

   * [[!UICONTROL ](#web-audience)

   * [[!UICONTROL ](#web-acquisition)

   * [[!UICONTROL ](#mobile-mobile-app)

   * [[!UICONTROL ](#mobile-mobile-device-information)

   * [[!UICONTROL ](#time-parting)

   * [[!UICONTROL ](#cross-channel)

   * [[!UICONTROL ](#other-channels)

   * [[!UICONTROL ](#ajo)

### Meest populair {#most-popular}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--unitsOvertimeReport"
>title="Geef het totale aantal eenheden weer dat is aangeschaft binnen alle bestellingen. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden."
>abstract="**dit kan u helpen** beter begrijpen hoe de eenheidsverkoop in tijd stijgt of daalt. U zou een segment kunnen toepassen om te leren welke klanten of geographies de meeste eenheden kopen en hoe die eenheidsverkoop in tijd trending.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door eenheidsverkoop vóór en na de gelanceerde campagne te vergelijken. Of je vergelijkt de jaaromzet per eenheid tijdens de vakantie.<br/> Dit malplaatje gebruikt de afmeting van de Dag en metrische Eenheden."

<!-- markdownlint-enable MD034 -->

<!--both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--training"
>title="Sjabloon voor trainingszelfstudie"
>abstract="Leer algemene Analysis Workspace-terminologie en stappen voor het maken van uw eerste analyse."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--pagesRankedReport"
>title="Identificeer de populairste en minst populaire pagina&#39;s."
>abstract="**dit kan u helpen** beter uw publiek en het soort informatie begrijpen zij het meest geinteresseerd zijn in.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals paginadetagegevens aanpassen om zicht op minder bekeken pagina&#39;s te verhogen, of tijd doorbrengen die de inhoud van uw meest bekeken pagina&#39;s verbetert.<br/> Dit malplaatje gebruikt de afmeting van de Pagina en metrische de Mening van de Pagina."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--pageViewsOvertimeReport"
>title="Het totale aantal paginaweergaven weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. "
>abstract="**dit kan u helpen** beter begrijpen hoe het verkeer op uw plaats in tijd zou kunnen stijgen of verminderen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door plaatsverkeer vóór en na de gelanceerde campagne te vergelijken. Of je zou jaar-over-jaar vakantieverkeer kunnen vergelijken.<br/> Dit malplaatje gebruikt de afmeting van de Dag en metrische de Meningen van de Pagina."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--visitsOvertimeReport"
>title="Het totale aantal bezoeken weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden."
>abstract="**dit kan u helpen** beter begrijpen hoe het verkeer op uw plaats in tijd zou kunnen stijgen of verminderen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door plaatsverkeer vóór en na de gelanceerde campagne te vergelijken. Of je zou jaar-over-jaar vakantieverkeer kunnen vergelijken.<br/> Dit malplaatje gebruikt de afmeting van de Dag en metrische bezoeken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--visitorsOvertimeReport"
>title="Het totale aantal unieke bezoekers weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. "
>abstract="**dit kan u helpen** beter begrijpen hoe het bereik en de publieksgrootte van uw plaats in tijd of vergeleken met een vroegere periode stijgt of daalt.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of een onlangs gelanceerde marketing campagne succesvol was in het aantrekken van nieuwe mensen aan de plaats door unieke bezoekers vóór en na de gelanceerde campagne te vergelijken. Of je vergelijkt het aantal mensen dat de site bezoekt tijdens de vakantie van jaar tot jaar.<br/> Dit malplaatje gebruikt de afmeting van de Dag en de Unieke metrische Bezoekers. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--keyMetricsReport"
>title="Bekijk een rapport waarin de paginaweergaven, bezoeken en unieke bezoekersstatistieken naast elkaar worden weergegeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden."
>abstract="**dit kan u helpen** deze belangrijke metriek vergelijken om een vollediger beeld van het aantal unieke mensen te bereiken die de plaats bezoeken, het aantal tijden werden de pagina&#39;s bezocht, en het aantal zittingen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als het gemiddelde aantal pagina&#39;s beoordelen elke bekeken persoon wanneer het bezoeken van de plaats in een bepaalde week of een maand, en hoe dat tijdens bepaalde tijden van het jaar of vóór en na marketing campagnes veranderde in werking werden gesteld. <br/> Dit malplaatje gebruikt de afmeting van de Dag, metrische de Mening van de Pagina, metrische Bezoekers, en de Unieke metrische Bezoekers."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--siteSectionRankedReport"
>title="Bekijk de populairste of best presterende gedeelten van uw site."
>abstract="**dit kan u** helpen beter begrijpen welke secties van uw plaats het bezochte meest zijn.<br>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen welke producten of de diensten die u de meeste rente produceert.<br/> Dit malplaatje gebruikt de afmeting van de Sectie van de Plaats en metrische Bebezoeken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--next-page-report"
>title="Bekijk de meest gangbare plaatsen die mensen direct na het bezoeken van een bepaalde pagina bezoeken."
>abstract="**dit kan u helpen** beter gebruikersgedrag na het bezoeken van een bepaalde pagina begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen of het paginaontwerp of de lay-out zouden kunnen worden geoptimaliseerd om mensen aan wenselijke pagina&#39;s, zoals een pagina te leiden om een aankoop te maken of een overzicht te verlaten.<br/> Dit malplaatje gebruikt de afmeting van de Pagina en metrische Gebeurtenissen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--previous-page-report"
>title="Bekijk de meest gangbare plaatsen die mensen direct bezoeken voordat ze een bepaalde pagina bezoeken."
>abstract="**dit kan u helpen** beter begrijpen welke pagina&#39;s het meeste verkeer aan een bepaalde pagina leiden.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of de pagina&#39;s die niet verschijnen aangezien vorige pagina&#39;s prominentere verbindingen aan de huidige pagina nodig hebben."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--campaignRankedReport"
>title="Bekijk de koppelingen die het meest succesvol zijn geweest in het besturen van verkeer naar uw site."
>abstract="**dit kan u helpen** beter begrijpen welke het volgen codes (en de verbindingen zij met) worden geassocieerd het meest gebruikt in de toegang tot van uw plaats.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw strategie aanpassen waar u verbindingen aan uw plaats toevoegt.<br/> Dit malplaatje gebruikt de het Volgen dimensie van de Code en metrische bezoeken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--productsRankedReport"
>title="Bekijk het aantal bestellingen per product. Gegevens worden weergegeven over een tijdsperiode."
>abstract="**dit kan u helpen** begrijpen welke producten in de hoogste of laagste vraag zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw marketing strategieën aanpassen om hoog-presterende producten te bevorderen of te verbeteren of te beëindigen ondermaatse producten. U kunt ook de productvoorraad aanpassen op basis van uw analyse van de gegevens.<br/> Dit malplaatje gebruikt de afmeting van het Product en metrische Orden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--lastTouchChannelRankedReport"
>title="Bekijk de meest recente marketingkanalen waarmee bezoekers te maken hebben tijdens hun serviceperiode (standaard 30 dagen)."
>abstract="**dit kan u helpen** begrijpen welke marketing kanalen het meest effectief in het brengen van mensen aan uw plaats waren die in omzettingen resulteren.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer middelen toewijzen aan hoog-presterende kanalen, of minder middelen toewijzen aan ondermaatse kanalen.<br/> Dit malplaatje gebruikt de Afmeting van het Kanaal van de Laatste Aanraking en de Unieke metrische Bezoekers."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--lastTouchChannelDetailRankedReport"
>title="Gegevens over de meest recente marketingkanalen waarmee bezoekers te maken hebben tijdens hun serviceperiode (standaard 30 dagen)."
>abstract="**dit kan u helpen** niet alleen begrijpen welke marketing kanalen het meest effectief in het brengen van mensen aan uw plaats waren die in omzettingen, maar details over die marketing kanalen resulteren. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer middelen toewijzen aan hoog-presterende kanalen, of minder middelen toewijzen aan ondermaatse kanalen.<br/> Dit malplaatje gebruikt de Laatste meta van het Detail van het Kanaal van de Aanraking en de Unieke metrische Bezoekers. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--revenueOvertimeReport"
>title="Geef het geldbedrag weer van de producten die in alle bestellingen zijn aangeschaft. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden."
>abstract="**dit kan u helpen** begrijpen hoe de opbrengst in tijd stijgt of daalt. U kunt deze metrisch met om het even welke afmeting combineren om te leren welke afmetingspunten aan opbrengst droegen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als de opbrengst van de projecttoekomst die op vorige tendensen wordt gebaseerd. U zou een andere dimensie, zoals de het Volgen codedimensie, kunnen ook toevoegen om te leren welke campagnes de meeste opbrengst produceren.<br/> Dit malplaatje gebruikt de afmeting van de Dag en metrische Opbrengst."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--ordersOvertimeReport"
>title="Het totale aantal aankoopgebeurtenissen weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden."
>abstract="**dit kan u helpen** beter begrijpen hoe de belangstelling in uw producten en de diensten in tijd stijgt of daalt. U kon een segment toepassen om te leren welke klanten of geographies de meeste orden plaatsen en hoe die orden in tijd trending.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door orden vóór en na de gelanceerde campagne te vergelijken. Of je kunt vakantiebestellingen van jaar tot jaar vergelijken.<br/> Dit malplaatje gebruikt de afmeting van de Dag en metrische Orden."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **het leerprogramma van de Opleiding**] | Meer algemene Analysis Workspace-terminologie en -stappen voor het maken van uw eerste analyse |
| [!UICONTROL **Pagina&#39;s**] | <!--duplicated in Engagement section--> Identificeer de populairste en minst populaire pagina&#39;s. <p>**dit kan u helpen** beter uw publiek en het soort informatie begrijpen zij het meest geinteresseerd zijn in.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals paginadetagegevens aanpassen om zicht op minder bekeken pagina&#39;s te verhogen, of tijd doorbrengen die de inhoud van uw meest bekeken pagina&#39;s verbetert.</p><p>Deze sjabloon gebruikt de afmetingen Pagina en Paginaweergaven.</p> |
| [!UICONTROL **de meningen van de Pagina**] | <!--duplicated in Engagement section--> Het totale aantal paginaweergaven weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** beter begrijpen hoe het verkeer op uw plaats in tijd zou kunnen stijgen of verminderen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door plaatsverkeer vóór en na de gelanceerde campagne te vergelijken. Of je zou jaar-over-jaar vakantieverkeer kunnen vergelijken.</p><p>Deze sjabloon gebruikt de afmetingen Dag en Paginaweergaven metrisch.</p> |
| [!UICONTROL **bezoeken van het Web**] | <!--duplicated in Engagement section--> Het totale aantal bezoeken weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** beter begrijpen hoe het verkeer op uw plaats in tijd zou kunnen stijgen of verminderen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door plaatsverkeer vóór en na de gelanceerde campagne te vergelijken. Of je zou jaar-over-jaar vakantieverkeer kunnen vergelijken.</p><p>Deze sjabloon gebruikt de dimensie Dag en de metrische weergave Bezoekingen.</p> |
| [!UICONTROL **de bezoekers van het Web**] | <!--duplicated in Engagement section--> Het totale aantal unieke bezoekers weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** beter begrijpen hoe het bereik en de publieksgrootte van uw plaats in tijd of vergeleken met een vroegere periode stijgt of daalt.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of een onlangs gelanceerde marketing campagne succesvol was in het aantrekken van nieuwe mensen aan de plaats door unieke bezoekers vóór en na de gelanceerde campagne te vergelijken. Of je vergelijkt het aantal mensen dat de site bezoekt tijdens de vakantie van jaar tot jaar.</p><p>Deze sjabloon gebruikt de dimensie Dag en de metrische waarde voor Unieke bezoekers.</p> |
| [!UICONTROL **Zeer belangrijke metriek**] | <!--duplicated in Engagement section--> Bekijk een rapport waarin de paginaweergaven, bezoeken en unieke bezoekersstatistieken naast elkaar worden weergegeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** deze belangrijke metriek vergelijken om een vollediger beeld van het aantal unieke mensen te bereiken die de plaats bezoeken, het aantal tijden werden de pagina&#39;s bezocht, en het aantal zittingen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als het gemiddelde aantal pagina&#39;s beoordelen elke bekeken persoon wanneer het bezoeken van de plaats in een bepaalde week of een maand, en hoe dat tijdens bepaalde tijden van het jaar of vóór en na marketing campagnes veranderde in werking werden gesteld. </p><p>Deze sjabloon gebruikt de afmetingen Dag, de metrische weergave van de Paginaweergave, de metrische weergave van bezoekers en de metrische waarde van de unieke bezoekers.</p> |
| [!UICONTROL **secties van de Plaats**] | Bekijk de populairste of best presterende gedeelten van uw site. <p>**dit kan u** helpen beter begrijpen welke secties van uw plaats het bezochte meest zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen welke producten of de diensten die u de meeste rente produceert.</p> <p>Deze sjabloon gebruikt de dimensie Site-sectie en de metrische weergave Bezoekingen.</p> |
| [!UICONTROL **Volgende pagina**] | Bekijk de meest gangbare plaatsen die mensen direct na het bezoeken van een bepaalde pagina bezoeken. <p>**dit kan u helpen** beter gebruikersgedrag na het bezoeken van een bepaalde pagina begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen of het paginaontwerp of de lay-out zouden kunnen worden geoptimaliseerd om mensen aan wenselijke pagina&#39;s, zoals een pagina te leiden om een aankoop te maken of een overzicht te verlaten.</p> <p>In deze sjabloon worden de afmetingen Pagina en Gebeurtenissen gebruikt.</p> |
| [!UICONTROL **Vorige pagina**] | Bekijk de meest gangbare plaatsen die mensen direct bezoeken voordat ze een bepaalde pagina bezoeken. <p>**dit kan u helpen** beter begrijpen welke pagina&#39;s het meeste verkeer aan een bepaalde pagina leiden.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of de pagina&#39;s die niet verschijnen aangezien vorige pagina&#39;s prominentere verbindingen aan de huidige pagina nodig hebben.</p><p>In deze sjabloon worden de afmetingen Pagina en Gebeurtenissen gebruikt.</p> |
| [!UICONTROL **het Volgen code**] | Bekijk de koppelingen die het meest succesvol zijn geweest in het besturen van verkeer naar uw site. <p>**dit kan u helpen** beter begrijpen welke het volgen codes (en de verbindingen zij met) worden geassocieerd het meest gebruikt in de toegang tot van uw plaats.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw strategie aanpassen waar u verbindingen aan uw plaats toevoegt.</p><p>Deze sjabloon gebruikt de dimensie Tracking Code en de metrische bezoekers.</p> |
| [!UICONTROL **Producten**] | Bekijk het aantal bestellingen per product. Gegevens worden weergegeven over een tijdsperiode. <p>**dit kan u helpen** begrijpen welke producten in de hoogste of laagste vraag zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw marketing strategieën aanpassen om hoog-presterende producten te bevorderen of te verbeteren of te beëindigen ondermaatse producten. U kunt ook de productvoorraad aanpassen op basis van uw analyse van de gegevens.</p><p>Deze malplaatje gebruikt de afmeting van het Product en de metrische Orden.</p> |
| [!UICONTROL **Laatste aanrakingskanaal**] | Bekijk de meest recente marketingkanalen waarmee bezoekers te maken hebben tijdens hun serviceperiode (standaard 30 dagen).<p>**dit kan u helpen** begrijpen welke marketing kanalen het meest effectief in het brengen van mensen aan uw plaats waren die in omzettingen resulteren.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer middelen toewijzen aan hoog-presterende kanalen, of minder middelen toewijzen aan ondermaatse kanalen.</p><p>Deze sjabloon gebruikt de afmeting Laatste aanraakkanaal en de metrische waarde Unieke bezoekers.</p> |
| [!UICONTROL **Laatste detail van het aanrakingskanaal**] | Gegevens over de meest recente marketingkanalen waarmee bezoekers te maken hebben tijdens hun serviceperiode (standaard 30 dagen).<p>**dit kan u helpen** niet alleen begrijpen welke marketing kanalen het meest effectief in het brengen van mensen aan uw plaats waren die in omzettingen, maar details over die marketing kanalen resulteren. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer middelen toewijzen aan hoog-presterende kanalen, of minder middelen toewijzen aan ondermaatse kanalen.</p><p>Deze sjabloon gebruikt de dimensie Laatste aanraakkanaaldetails en de metrische waarde Unieke bezoekers.</p> |
| [!UICONTROL **Omzet**] | <!--duplicated in Web Conversion section-->Geef het geldbedrag weer van de producten die in alle bestellingen zijn aangeschaft. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden.<p>**dit kan u helpen** begrijpen hoe de opbrengst in tijd stijgt of daalt. U kunt deze metrisch met om het even welke afmeting combineren om te leren welke afmetingspunten aan opbrengst droegen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als de opbrengst van de projecttoekomst die op vorige tendensen wordt gebaseerd. U zou een andere dimensie, zoals de het Volgen codedimensie, kunnen ook toevoegen om te leren welke campagnes de meeste opbrengst produceren.</p><p>Deze sjabloon gebruikt de dimensie Dag en de maatstaf van Inkomsten.</p> |
| [!UICONTROL **Orders**] | <!--duplicated in Web Conversion section-->Het totale aantal aankoopgebeurtenissen weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** beter begrijpen hoe de belangstelling in uw producten en de diensten in tijd stijgt of daalt. U kon een segment toepassen om te leren welke klanten of geographies de meeste orden plaatsen en hoe die orden in tijd trending.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door orden vóór en na de gelanceerde campagne te vergelijken. Of je kunt vakantiebestellingen van jaar tot jaar vergelijken.</p><p>Deze malplaatje gebruikt de afmeting van de Dag en metrische Orden.</p> |

### web: betrokkenheid {#web-engagement}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--real-time"
>title="Bekijk de afmetingen en metriek die momenteel op uw site worden verzameld."
>abstract="**dit kan u helpen** beter begrijpen wat op uw plaats trending is.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als antwoorden aan en actief de prestaties van uw huidige marketing inhoud en campagnes beheren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeSpentVisitOvertimeReport"
>title="Bekijk de gemiddelde tijd die bezoekers tijdens elk bezoek aan uw site doorbrengen. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden."
>abstract="**dit kan u** helpen de niveaus van de bezoekersbetrokkenheid beter begrijpen en hoeveel tijd bezoekers aan de plaats uitgeven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of de veranderingen in uw plaats in bezoekers resulteren die meer tijd op de plaats doorbrengen.<br/> Dit malplaatje gebruikt de afmeting van de Dag en de Tijd die per (seconden) metrisch van het Bezoek besteedt."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timePriorRankedReport"
>title="Geef de gemiddelde tijd weer die gebruikers doorbrengen voordat een geslaagde gebeurtenis plaatsvindt."
>abstract="**dit kan u helpen** beter begrijpen hoeveel tijd het bezoekers neemt om een gewenste actie uit te voeren, zoals het maken van een aankoop.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of de veranderingen in uw plaats bezoekers&#39; capaciteit verbeteren om een succesgebeurtenis snel te bereiken.<br/> Dit malplaatje gebruikt de Tijd voorafgaand aan de afmeting van de Gebeurtenis en de Unieke metrische Bezoekers."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--falloutReport"
>title="Bekijk waar mensen een vooraf gedefinieerde reeks pagina&#39;s verlaten of doorlopen."
>abstract="**dit kan u helpen** beter begrijpen waar de mensen uit de gebruikersreis vallen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals omzettingspercentages door specifieke processen op uw plaats (zoals een aankoop of registratieproces) analyseren, of correlaties tussen gebeurtenissen op uw plaats analyseren. (Bijvoorbeeld, welk percentage van mensen die naar uw privacybeleid keken ging om een product te kopen.) U kunt dit malplaatje ook gebruiken om zij aan zij vergelijkingen van twee verschillende segmenten in het zelfde rapport uit te voeren.<br/> Dit malplaatje gebruikt de visualisatie van de Vallout."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cross-device-analysis"
>title="Bekijk welke apparaten mensen over alle punten van de reis gebruikten."
>abstract="**dit kan u helpen** beter begrijpen hoeveel mensen met uw merk, de soorten apparaten interactie aangaan zij gebruiken, en hoe hun gebruik van veelvoudige apparaten hun ervaring beïnvloedt. Bijvoorbeeld, hoe vaak beginnen de mensen een taak op een mobiel apparaat en dan later naar een Desktop gaan om een taak te voltooien? Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze? En zo verder.<br/>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als bepaalde delen van de gebruikersreis voor een mobiele ervaring optimaliseren.<br/> Dit malplaatje gebruikt de visualisatie van de Stroom, de visualisatie van de Vallout, de analyse van de Cohort, metrische Mensen, en de Unieke metrische apparaten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--web-retention"
>title="Bekijk wie uw loyale gebruikers zijn en wat zij op uw plaats doen."
>abstract="**dit kan u helpen** beter begrijpen het aantal tijden de gemiddelde persoon uw plaats bezoekt, de frequentie waarmee de mensen aan de plaats terugkeren, en het aantal dagen tussen terugkeerbezoeken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als analyseert welke inhoud het meest effectief in het brengen van mensen terug naar de plaats is.<br/> Dit malplaatje gebruikt metrische Bebezoeken en de Unieke bezoekers metrische."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--audio-consumption-template"
>title="De trends en de belangrijkste meetwaarden voor het audioverbruik van media op alle digitale apparaten bekijken."
>abstract="**dit kan u helpen** beter begrijpen hoe de bezoekers audio inhoud op uw plaats verbruiken.<br/>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als analyseren welke inhoud het meest wordt verbruikt.<br/> Dit malplaatje gebruikt metrische Bebezoeken en de Unieke bezoekers metrische."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--media-recency-frequency-loyalty"
>title="De trends en de belangrijkste meetwaarden van het mediaconsumptie op alle digitale apparaten bekijken."
>abstract="**dit kan u helpen** beter begrijpen het aantal tijden de gemiddelde persoon uw plaats bezoekt, de frequentie waarmee de mensen aan de plaats terugkeren, en het aantal dagen tussen terugkeerbezoeken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als analyseert welke inhoud het meest effectief in het brengen van mensen terug naar de plaats is.<br/> Dit malplaatje gebruikt metrische Bebezoeken en de Unieke bezoekers metrische."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--reloadsRankedReport"
>title="Bekijk het aantal tijden een afmetingspunt tijdens een herlading aanwezig was. Een bezoeker die zijn browser vernieuwt, is de meest gebruikelijke manier om een nieuwe laadbewerking te starten."
>abstract="**dit kan u helpen** identificeren wanneer de kwesties op een bepaalde pagina zouden kunnen voorkomen die een bezoeker zou ertoe aanzetten om de pagina opnieuw te laden.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen welke pagina&#39;s kwesties hebben die moeten worden gericht.<br/> Dit malplaatje gebruikt metrisch opnieuw laden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeSpentPageRankedReport"
>title="Bekijk de gemiddelde tijd die bezoekers tijdens elk bezoek aan uw site doorbrengen. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden."
>abstract="**dit kan u** helpen de niveaus van de bezoekersbetrokkenheid beter begrijpen en hoeveel tijd bezoekers aan de plaats uitgeven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of de veranderingen in uw plaats in bezoekers resulteren die meer tijd op de plaats doorbrengen.<br/> Dit malplaatje gebruikt de afmeting van de Dag en de Tijd die per (seconden) metrisch van het Bezoek besteedt."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--entryPageOriginalRankedReport"
>title="Bekijk de bovenste pagina&#39;s waartoe mensen toegang hebben wanneer ze uw site voor het eerst bezoeken gedurende de levensduur van een bezoeker."
>abstract="**dit kan u helpen** beter begrijpen welke pagina&#39;s het meeste verkeer aan uw plaats drijven of meer over de eerste impressiebezoekers op uw plaats begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer de aanvankelijke ervaring mensen op de plaats krijgen, of ervoor zorgen dat de pagina&#39;s mensen eerst zien bij het ingaan van uw plaats welkomend en de noodzakelijke verbindingen aan andere gebieden van uw plaats verstrekken.<br/> Dit malplaatje gebruikt metrische Sessies. Het gebruikt ook de Bar visualisatie en de Freeform lijstvisualisatie."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--singlePageVisitsRankedReport"
>title="Bekijk het aantal bezoeken dat uit één enkele unieke pagina bestond."
>abstract="**dit kan u** helpen de niveaus van de bezoekersbetrokkenheid beter begrijpen en hoeveel tijd bezoekers aan de plaats uitgeven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of de veranderingen in uw plaats in bezoekers resulteren die meer tijd op de plaats doorbrengen.<br/> Dit malplaatje gebruikt de Enige dimensie van paginabezoeken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--sitePerformanceOverview"
>title="Geef prestatiegegevens voor je Adobe Experience Manager-site weer."
>abstract="**dit kan u helpen** beter waarderealisatie van Adobe Experience Manager begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer uw montages van de Experience Manager."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--formsPerformanceOverview"
>title="Geef prestatiegegevens voor uw Adobe Experience Manager-formulieren weer."
>abstract="**dit kan u helpen** beter waarderealisatie van Adobe Experience Manager begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer uw montages van de Experience Manager."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--itp-impact"
>title="De effecten van Intelligent Tracking Prevention (ITP) op gegevensverzameling en -rapportage weergeven en analyseren."
>abstract="**dit kan u** beter begrijpen potentieel gegevensverlies toe te schrijven aan koekjesbeperkingen die door ITP worden opgelegd.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw analytische opstelling aanpassen om het effect van ITP te minimaliseren."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_template_time_spent"
>title="Bekijk de gemiddelde tijd die bezoekers doorbrengen aan uw site tijdens elk bezoek en de gemiddelde tijd die gebruikers doorbrengen voordat een geslaagde gebeurtenis plaatsvindt. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden."
>abstract="**dit kan u helpen** beter de niveaus van de bezoekersbetrokkenheid begrijpen en hoeveel tijd het bezoekers neemt om een gewenste actie uit te voeren, zoals het maken van een aankoop.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of de veranderingen in uw plaats bezoekers&#39; capaciteit verbeteren om een succesgebeurtenis snel te bereiken.<br/> Dit malplaatje gebruikt de afmeting van de Dag en de Tijd die per (seconden) metrisch van het Bezoek, de afmeting van de Dag, en de Tijd die per (seconden) metrisch van het Bezoek wordt uitgegeven."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-content-consumption"
>title="Bekijk welke webinhoud het meest wordt verbruikt en aantrekkelijke gebruikers is."
>abstract="**dit kan u helpen** beter begrijpen waar de mensen op eerste het ingaan van de plaats gaan, welke secties van de plaatsmensen het meest bezoeken, en welke pagina&#39;s hoogstwaarschijnlijk mensen weg van de plaats zullen drijven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als evalueert welke wegen op de plaats mensen tot de belangrijkste pagina&#39;s drijven, en welke pagina&#39;s eerder mensen buiten de plaats zullen leiden.<br/> Dit malplaatje gebruikt de afmeting van de Pagina en metrische de Weergaven van de Pagina, metrische Bezoekingen, de Unieke metrische Bezoekers, de metrische het Tarief van de Ingang, metrische het Tarief van de Stuitstempel, metrische het Tarief van de Uitgang, en metrische de Snelheid van de Inhoud. Het gebruikt ook de visualisaties van de Stroom voor ingang, uitgang, en hoogste secties."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--media-content-consumption"
>title="Bekijk welke media-inhoud het meest wordt verbruikt en aantrekkelijke gebruikers zijn."
>abstract="**dit kan u helpen** beter begrijpen waar de mensen op eerste het ingaan van de plaats gaan, welke secties van de plaatsmensen het meest bezoeken, en welke pagina&#39;s hoogstwaarschijnlijk mensen weg van de plaats zullen drijven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als evalueert welke wegen op de plaats mensen tot de belangrijkste pagina&#39;s drijven, en welke pagina&#39;s eerder mensen buiten de plaats zullen leiden.<br/> Dit malplaatje gebruikt de afmeting van de Pagina en metrische de Weergaven van de Pagina, metrische Bezoekingen, de Unieke metrische Bezoekers, de metrische het Tarief van de Ingang, metrische het Tarief van de Stuitstempel, metrische het Tarief van de Uitgang, en metrische de Snelheid van de Inhoud. Het gebruikt ook de visualisaties van de Stroom voor ingang, uitgang, en hoogste secties; een visualisatie van het Satterplot die paginameningen voor de gemeenschappelijkste pagina&#39;s toont; een Staafvisualisatie die paginameningen door buckette tijd toont; en een visualisatie van de Lijn die een trended mening van de gemiddelde tijd toont die aan de plaats wordt doorgebracht."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--flowreport"
>title="Bekijk de meest gangbare plaatsen die mensen direct na het bezoeken of vlak voor het bezoeken van een bepaalde plaats bezoeken."
>abstract="**dit kan u helpen** begrijpen hoe het verkeer zich van een bepaalde pagina naar andere delen van uw plaats beweegt, en de wegen begrijpt die de mensen nemen om bij een bepaalde pagina aan te komen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen of het paginaontwerp of de lay-out zouden kunnen worden geoptimaliseerd om mensen aan wenselijke pagina&#39;s, zoals een pagina te leiden om een aankoop te maken of een overzicht te verlaten. Of ga na of de informatie op de huidige pagina waarschijnlijk de richting(en) aangeeft waarnaar mensen op zoek zijn wanneer ze van vorige pagina&#39;s komen. Of u zou kunnen beoordelen of de pagina&#39;s die niet zoals vorige pagina&#39;s verschijnen prominentere verbindingen aan de huidige pagina nodig hebben.<br/> Dit malplaatje gebruikt het Volgende of vorige puntpaneel."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--page-summary-report"
>title="Belangrijke informatie over om het even welke pagina over uw eigenschappen bekijken. Toont paginameningen, een trendlijn, een stroomvisualisatie, en meer."
>abstract="**dit kan u helpen** beter begrijpen hoe de mensen met een bepaalde pagina in wisselwerking staan.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als de prestaties van de pagina over een periode analyseren of beter begrijpen wat verkeer aan de pagina drijft.<br/> Dit malplaatje gebruikt metrisch de Meningen van de Pagina. Het gebruikt ook de Lijnvisualisatie en de visualisatie van de Stroom."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--entryPageRankedReport"
>title="Bekijk de bovenste pagina&#39;s waartoe mensen toegang hebben wanneer ze uw site voor het eerst bezoeken."
>abstract="**dit kan u helpen** beter begrijpen welke pagina&#39;s het meeste verkeer aan uw plaats drijven of meer over de eerste impressiebezoekers op uw plaats begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer de aanvankelijke ervaring mensen op de plaats krijgen, of ervoor zorgen dat de pagina&#39;s mensen eerst zien bij het ingaan van uw plaats welkomend en de noodzakelijke verbindingen aan andere gebieden van uw plaats verstrekken.<br/> Dit malplaatje gebruikt metrische Sessies. Het gebruikt ook de Bar visualisatie en de Freeform lijstvisualisatie."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--exitPageRankedReport"
>title="Bekijk de bovenste pagina&#39;s die mensen direct openen voordat ze uw site verlaten."
>abstract="**dit kan u** helpen beter begrijpen welke pagina&#39;s mensen weg van de plaats leiden. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gemeenschappelijke eindpagina&#39;s bijwerken om de ervaring te optimaliseren krijgen de mensen alvorens zij verlaten, of inhoud of verbindingen omvatten om mensen aan te moedigen om op uw plaats te blijven.<br/> Dit malplaatje gebruikt metrische Sessies. Het gebruikt ook de Bar visualisatie en de Freeform lijstvisualisatie."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Zeer belangrijke metriek**] | <!--duplicated in Most popular section--> Bekijk een rapport waarin de paginaweergaven, bezoeken en unieke bezoekersstatistieken naast elkaar worden weergegeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** deze belangrijke metriek vergelijken om een vollediger beeld van het aantal unieke mensen te bereiken die de plaats bezoeken, het aantal tijden werden de pagina&#39;s bezocht, en het aantal zittingen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als het gemiddelde aantal pagina&#39;s beoordelen elke bekeken persoon wanneer het bezoeken van de plaats in een bepaalde week of een maand, en hoe dat tijdens bepaalde tijden van het jaar of vóór en na marketing campagnes veranderde in werking werden gesteld. </p><p>Deze sjabloon gebruikt de afmetingen Dag, de metrische weergave van de Paginaweergave, de metrische weergave van bezoekers en de metrische waarde van de unieke bezoekers.</p> |
| [!UICONTROL **de meningen van de Pagina**] | <!--duplicated in Most popular section-->Het totale aantal paginaweergaven weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** beter begrijpen hoe het verkeer op uw plaats in tijd zou kunnen stijgen of verminderen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door plaatsverkeer vóór en na de gelanceerde campagne te vergelijken. Of je zou jaar-over-jaar vakantieverkeer kunnen vergelijken.</p><p>Deze sjabloon gebruikt de afmetingen Dag en Paginaweergaven metrisch.</p> |
| [!UICONTROL **Pagina&#39;s**] | <!--duplicated in Most popular section-->Identificeer de populairste en minst populaire pagina&#39;s. <p>**dit kan u helpen** beter uw publiek en het soort informatie begrijpen zij het meest geinteresseerd zijn in.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals paginadetagegevens aanpassen om zicht op minder bekeken pagina&#39;s te verhogen, of tijd doorbrengen die de inhoud van uw meest bekeken pagina&#39;s verbetert.</p><p>Deze sjabloon gebruikt de afmetingen Pagina en Paginaweergaven.</p> |
| [!UICONTROL **Bezoeken**] | <!--duplicated in Most popular section-->Het totale aantal bezoeken weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** beter begrijpen hoe het verkeer op uw plaats in tijd zou kunnen stijgen of verminderen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling van de doeltreffendheid van onlangs gelanceerde marketing campagne door plaatsverkeer vóór en na de gelanceerde campagne te vergelijken. Of je zou jaar-over-jaar vakantieverkeer kunnen vergelijken.</p><p>Deze sjabloon gebruikt de dimensie Dag en de metrische weergave Bezoekingen.</p> |
| [!UICONTROL **Bezoekers**] | <!--duplicated in Most popular section-->Het totale aantal unieke bezoekers weergeven. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** beter begrijpen hoe het bereik en de publieksgrootte van uw plaats in tijd of vergeleken met een vroegere periode stijgt of daalt.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of een onlangs gelanceerde marketing campagne succesvol was in het aantrekken van nieuwe mensen aan de plaats door unieke bezoekers vóór en na de gelanceerde campagne te vergelijken. Of je vergelijkt het aantal mensen dat de site bezoekt tijdens de vakantie van jaar tot jaar.</p><p>Deze sjabloon gebruikt de dimensie Dag en de metrische waarde voor Unieke bezoekers.</p> |
| [!UICONTROL **bestede Tijd**] | Bekijk de gemiddelde tijd die bezoekers doorbrengen aan uw site tijdens elk bezoek en de gemiddelde tijd die gebruikers doorbrengen voordat een geslaagde gebeurtenis plaatsvindt. Gegevens worden over een bepaalde periode weergegeven en vergeleken met eerdere perioden. <p>**dit kan u helpen** beter de niveaus van de bezoekersbetrokkenheid begrijpen en hoeveel tijd het bezoekers neemt om een gewenste actie uit te voeren, zoals het maken van een aankoop.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordeling of de veranderingen in uw plaats bezoekers&#39; capaciteit verbeteren om een succesgebeurtenis snel te bereiken.</p><p>Deze sjabloon gebruikt de afmetingen van de Dag en de metrische waarde van de Tijd die per Bezoek (seconden) wordt uitgegeven, de dimensie van de Dag, en de metrische waarde van de Tijd die per Bezoek (seconden) wordt uitgegeven.</p> |
| [!UICONTROL **secties van de Plaats**] | <!--duplicated in Most popular section-->Bekijk de populairste of best presterende gedeelten van uw site. <p>**dit kan u** helpen beter begrijpen welke secties van uw plaats het bezochte meest zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen welke producten of de diensten die u de meeste rente produceert.</p> <p>Deze sjabloon gebruikt de dimensie Site-sectie en de metrische weergave Bezoekingen.</p> |
| [!UICONTROL **de inhoudsconsumptie van het Web**] | Bekijk welke webinhoud het meest wordt verbruikt en aantrekkelijke gebruikers is.<p>**dit kan u helpen** beter begrijpen waar de mensen op eerste het ingaan van de plaats gaan, welke secties van de plaatsmensen het meest bezoeken, en welke pagina&#39;s hoogstwaarschijnlijk mensen weg van de plaats zullen drijven.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen welke wegen op de plaats mensen tot de belangrijkste pagina&#39;s drijven, en welke pagina&#39;s mensen uit de plaats <!-- not sure about these takeaways... --> eerder zullen leiden.</p> <p>Deze sjabloon gebruikt de afmetingen van de Pagina en de metrische weergave van de Pagina, de metrische bezoekers, de metrische waarde van de Unieke bezoekers, de maateenheid van de Invoersnelheid, de meeteenheid voor Stuitsnelheid, de maateenheid Afsluitingsfrequentie en de metrische waarde voor Inhoudssnelheid. Het gebruikt ook de visualisaties van de Stroom voor ingang, uitgang, en hoogste secties.</p> |
| [!UICONTROL **de inhoudsconsumptie van Media**] | Bekijk welke media-inhoud het meest wordt verbruikt en aantrekkelijke gebruikers zijn.<p>**dit kan u helpen** beter begrijpen waar de mensen op eerste het ingaan van de plaats gaan, welke secties van de plaatsmensen het meest bezoeken, en welke pagina&#39;s hoogstwaarschijnlijk mensen weg van de plaats zullen drijven.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen welke wegen op de plaats mensen tot de belangrijkste pagina&#39;s drijven, en welke pagina&#39;s mensen uit de plaats <!-- not sure about these takeaways... --> eerder zullen leiden.</p> <p>Deze sjabloon gebruikt de afmetingen van de Pagina en de metrische weergave van de Pagina, de metrische bezoekers, de metrische waarde van de Unieke bezoekers, de maateenheid van de Invoersnelheid, de meeteenheid voor Stuitsnelheid, de maateenheid Afsluitingsfrequentie en de metrische waarde voor Inhoudssnelheid. Het gebruikt ook de visualisaties van de Stroom voor ingang, uitgang, en hoogste secties; een visualisatie van het Satterplot die paginameningen voor de gemeenschappelijkste pagina&#39;s toont; een Staafvisualisatie die paginameningen door buckette tijd toont; en een visualisatie van de Lijn die een trended mening van de gemiddelde tijd toont die aan de plaats wordt doorgebracht.</p> |
| [!UICONTROL **Volgende en vorige paginastroom**] | Bekijk een stroomvisualisatie van de meest gangbare plaatsen die mensen direct na het bezoeken en vlak voordat ze een bepaalde pagina bezoeken. <p>**dit kan u helpen** begrijpen hoe het verkeer zich van een bepaalde pagina naar andere delen van uw plaats beweegt, en de wegen begrijpt die de mensen nemen om bij een bepaalde pagina aan te komen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als beoordelen of het paginaontwerp of de lay-out zouden kunnen worden geoptimaliseerd om mensen aan wenselijke pagina&#39;s, zoals een pagina te leiden om een aankoop te maken of een overzicht te verlaten. Of ga na of de informatie op de huidige pagina waarschijnlijk de richting(en) aangeeft waarnaar mensen op zoek zijn wanneer ze van vorige pagina&#39;s komen. Of u zou kunnen beoordelen of de pagina&#39;s die niet zoals vorige pagina&#39;s verschijnen prominentere verbindingen aan de huidige pagina nodig hebben.</p><p>Deze sjabloon gebruikt het deelvenster Volgende of Vorige item.</p> |
| **Overzicht van de Pagina** | Belangrijke informatie over om het even welke pagina over uw eigenschappen bekijken. Toont paginameningen, een trendlijn, een stroomvisualisatie, en meer.  <p>**dit kan u helpen** beter begrijpen hoe de mensen met een bepaalde pagina in wisselwerking staan.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als de prestaties van de pagina over een periode analyseren of beter begrijpen wat verkeer aan de pagina drijft.</p><p>Deze sjabloon gebruikt de metrische weergave van paginaweergaven. Het gebruikt ook de Lijnvisualisatie en de visualisatie van de Stroom.</p> |
| **pagina&#39;s van de Ingang** | Bekijk de bovenste pagina&#39;s waartoe mensen toegang hebben wanneer ze uw site voor het eerst bezoeken. <p>**dit kan u helpen** beter begrijpen welke pagina&#39;s het meeste verkeer aan uw plaats drijven of meer over de eerste impressiebezoekers op uw plaats begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer de aanvankelijke ervaring mensen op de plaats krijgen, of ervoor zorgen dat de pagina&#39;s mensen eerst zien bij het ingaan van uw plaats welkomend en de noodzakelijke verbindingen aan andere gebieden van uw plaats verstrekken.</p><p>Deze sjabloon gebruikt metrische sessies. Het gebruikt ook de Bar visualisatie en de Freeform lijstvisualisatie.</p> |
| **Pagina&#39;s van de uitgang** | Bekijk de bovenste pagina&#39;s die mensen direct openen voordat ze uw site verlaten.<p>**dit kan u** helpen beter begrijpen welke pagina&#39;s mensen weg van de plaats leiden. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gemeenschappelijke eindpagina&#39;s bijwerken om de ervaring te optimaliseren krijgen de mensen alvorens zij verlaten, of inhoud of verbindingen omvatten om mensen aan te moedigen om op uw plaats te blijven.</p><p>Deze sjabloon gebruikt metrische sessies. Het gebruikt ook de Bar visualisatie en de Freeform lijstvisualisatie.</p> |

### Web: Conversie {#web-conversion}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--categoryRankedReport"
>title="Bekijk het aantal bezoeken voor elke productcategorie op uw site. Dit is nuttig voor implementaties die de productvariabele gebruiken en metriek rond productcategorie willen zien. De dimensie die deze sjabloon vult, kan opzettelijk leeg zijn als u geen producten op uw site hebt."
>abstract="**dit kan u** helpen beter top-selling of de meesten-bekeken producten begrijpen. &lt;/br/> **Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als maatregel de doeltreffendheid van een marketing campagne voor een bepaald product.<br/> Dit malplaatje gebruikt de afmeting van de Categorie en metrische Bezoekingen. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--commerce-and-marketing-management"
>title="Bekijk vooraf gebouwde inzichten voor detailhandelaren over uw handelsactiviteiten om verkoop te helpen verbeteren. Dit is gericht op gebruikers van Magento, maar kan door om het even welke online detailhandelaar worden gebruikt."
>abstract="**dit kan u helpen** beter begrijpen hoe uw handelsactiviteiten aan verkoopaantallen bijdragen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als begrotingen aanpassen aan activiteiten die het meeste ROI krijgen."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--productConversionReport"
>title="Bekijk de productomzetting in een trechter-visualisatie die winkelwagentjes, kassa&#39;s en bestellingen toont. U kunt ook conversiepercentages, inkomstengemiddelden, eenheidsgemiddelden en ordergemiddelden zien."
>abstract="**dit kan u helpen** beter begrijpen hoe de mensen door en weggaan tijdens het omzettingsproces.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw website verbeteren om een vlotter controleproces te vergemakkelijken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--retail-products-template"
>title="Bekijk welke producten het best presteren."
>abstract="**dit kan u helpen** beter begrijpen welke producten het meest succesvol zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals verhoging van financiering aan succesvolle producten en vermindering financiering aan minder succesvolle producten.<br/> dit malplaatje gebruikt de Weergaven van het Product, de Toevoegingen van de Kar, Orden, Inkomsten, en de metriek van Eenheden. Het gebruikt ook de dimensie van het Product."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartConversionReport"
>title="Bekijk het aantal keren dat mensen toetsafhandelingsgebeurtenissen hebben uitgevoerd, zoals het toevoegen van items aan hun winkelwagentje, het bekijken van hun winkelwagentje, het verwijderen van items uit hun winkelwagentje en het uitchecken."
>abstract="**dit kan u helpen** beter begrijpen welke delen van het controleproces trechter die tot omzetting leiden en die aan kartontroeping vatbaarder zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als vermindering wrijving bij bepaalde stappen van het controleproces.<br/> Dit malplaatje gebruikt"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartsOvertimeReport"
>title="Bekijk het aantal personen dat een product aan hun winkelwagentje heeft toegevoegd."
>abstract="**dit kan u helpen** beter het aantal mensen begrijpen die een product aan hun kar, in tegenstelling tot het algemene aantal producten toevoegen die aan een kar worden toegevoegd.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als maatregel de doeltreffendheid van uw productpagina&#39;s.<br/> Dit malplaatje gebruikt metrische Waren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartViewsOvertimeReport"
>title="Bekijk het aantal keren dat mensen hun winkelwagentje bekeken."
>abstract="**dit kan u helpen** beter de controleervaring in een inspanning begrijpen om het tarief van de kartontroeping te verminderen, of de tijd tussen karttoevoegingen en controles onder verschillende producten te analyseren.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals aanbiedingsbevorderingen voor producten die in winkelwagentjes het langst blijven en bij het grootste risico voor verlaten zijn.<br/> Dit malplaatje gebruikt metrische de Meningen van het Kart."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartAdditionsOvertimeReport"
>title="Bekijk het aantal keren dat mensen iets aan hun winkelwagen hebben toegevoegd."
>abstract="**dit kan u helpen** beter het deel van de omzettrechter begrijpen waar de klanteninteresse in een product hoog genoeg is dat zij het aan hun kar toevoegen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als productaanbevelingen voor alle klanten verbeteren. Dit kan worden gedaan door te analyseren welke producten vaak aan dezelfde karretjes worden toegevoegd en door verwante producten voor te stellen op basis van producten die al in de kar staan."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartRemovalsOvertimeReport"
>title="Bekijk het aantal keren dat mensen iets uit hun winkelwagentje hebben verwijderd."
>abstract="**dit kan u helpen** beter het deel van de omzettrechter begrijpen waar de klanten niet meer in een product geinteresseerd zijn, of het kan u helpen begrijpen waar de problemen in het controleproces zouden kunnen bestaan.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als om het even welke potentiële barrières verwijderen die in het controleproces, zoals een gecompliceerde gebruikerservaring zouden kunnen bestaan.<br/> Dit malplaatje gebruikt metrische de Verwijderingen van de Kar."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--purchaseConversionReport"
>title="De aanschafconversie weergeven in een trechter-visualisatie met sessies, winkelwagentjes en bestellingen. U kunt ook conversiepercentages, inkomstengemiddelden, eenheidsgemiddelden en ordergemiddelden zien."
>abstract="**dit kan u helpen** beter begrijpen hoe de mensen door en weggaan tijdens het omzettingsproces.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw website verbeteren om een vlotter controleproces te vergemakkelijken."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Trechter van de Productomzetting van het Product**] | Bekijk de productomzetting in een trechter-visualisatie die winkelwagentjes, kassa&#39;s en bestellingen toont. U kunt ook conversiepercentages, inkomstengemiddelden, eenheidsgemiddelden en ordergemiddelden zien.<p>**dit kan u helpen** beter begrijpen hoe de mensen door en weggaan tijdens het omzettingsproces.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw website verbeteren om een vlotter controleproces te vergemakkelijken.</p> |
| **Producten** | Bepalen welke producten de drijvende kracht zijn achter de belangrijkste maatstaven, zoals de beste verkopers of de meeste weergegeven verkopers. <p>**dit kan u helpen** beter begrijpen welke producten het meest succesvol zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals verhoging van financiering aan succesvolle producten en vermindering financiering aan minder succesvolle producten.</p><p>Deze malplaatje gebruikt metrische Orden en de afmeting van het Product. |
| **Prestaties van het Product** | Bekijk welke producten het best presteren.<p>**dit kan u helpen** beter begrijpen welke producten het meest succesvol zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals verhoging van financiering aan succesvolle producten en vermindering financiering aan minder succesvolle producten.</p><p>Deze sjabloon gebruikt de metriek Productweergaven, Toevoegingen voor winkelwagentjes, Bestellingen, Opbrengsten en Eenheden. Het gebruikt ook de dimensie van het Product. |
| **de omzettingstekens van de Kar** | Bekijk het aantal keren dat mensen toetsafhandelingsgebeurtenissen hebben uitgevoerd, zoals het toevoegen van items aan hun winkelwagentje, het bekijken van hun winkelwagentje, het verwijderen van items uit hun winkelwagentje en het uitchecken. <p>**dit kan u helpen** beter begrijpen welke delen van het controleproces trechter die tot omzetting leiden en die aan kartontroeping vatbaarder zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als vermindering wrijving bij bepaalde stappen van het controleproces.</p> |
| **Houtskaarten** | Bekijk het aantal personen dat een product aan hun winkelwagentje heeft toegevoegd.<p>**dit kan u helpen** beter het aantal mensen begrijpen die een product aan hun kar, in tegenstelling tot het algemene aantal producten toevoegen die aan een kar worden toegevoegd.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als maatregel de doeltreffendheid van uw productpagina&#39;s.</p><p>In deze sjabloon wordt de metrische kaart gebruikt. |
| {de meningen van 0} Kaart **** | Bekijk het aantal keren dat mensen hun winkelwagentje bekeken. <p>**dit kan u helpen** beter de controleervaring in een inspanning begrijpen om het tarief van de kartontroeping te verminderen, of de tijd tussen karttoevoegingen en controles onder verschillende producten te analyseren.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals aanbiedingsbevorderingen voor producten die in winkelwagentjes het langst blijven en bij het grootste risico voor verlaten zijn.</p><p>In deze sjabloon wordt de metrische weergave van winkelwagentjes gebruikt. |
| **toevoegingen van de Kaart** | Bekijk het aantal keren dat mensen iets aan hun winkelwagen hebben toegevoegd. <p>**dit kan u helpen** beter het deel van de omzettrechter begrijpen waar de klanteninteresse in een product hoog genoeg is dat zij het aan hun kar toevoegen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als productaanbevelingen voor alle klanten verbeteren. Dit kan worden gedaan door te analyseren welke producten vaak aan dezelfde karretjes worden toegevoegd en door verwante producten voor te stellen op basis van producten die al in de kar staan. |
| **de verwijderingen van de Kar** | Bekijk het aantal keren dat mensen iets uit hun winkelwagentje hebben verwijderd.<p>**dit kan u helpen** beter het deel van de omzettrechter begrijpen waar de klanten niet meer in een product geinteresseerd zijn, of het kan u helpen begrijpen waar de problemen in het controleproces zouden kunnen bestaan.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als om het even welke potentiële barrières verwijderen die in het controleproces, zoals een gecompliceerde gebruikerservaring zouden kunnen bestaan.</p><p>Deze sjabloon gebruikt de metrische gegevens voor winkelwagentjes. |
| **de conversietrechter van de Aankoop** | De aanschafconversie weergeven in een trechter-visualisatie met sessies, winkelwagentjes en bestellingen. U kunt ook conversiepercentages, inkomstengemiddelden, eenheidsgemiddelden en ordergemiddelden zien.<p>**dit kan u helpen** beter begrijpen hoe de mensen door en weggaan tijdens het omzettingsproces.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw website verbeteren om een vlotter controleproces te vergemakkelijken.</p> |
| **Omzet** | <!--duplicated in Most popular section-->Geef het geldbedrag weer van de producten die in alle bestellingen zijn aangeschaft.<p>**dit kan u** helpen beter begrijpen welke afmetingspunten aan opbrengst, door metrische Inkomsten met om het even welke afmeting te combineren bijdroegen. Bijvoorbeeld, kon u de hoogste campagnes zien (gebruikend de het Volgen codedimensie) die tot opbrengst bijdroegen. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals campagnes aanpassen die niet de opbrengstdoelstellingen ontmoeten u zou verwachten.</p><p>In deze sjabloon wordt de maatstaf voor inkomsten gebruikt. |
| **Orders** | <!--duplicated in Most popular section-->Geef het totale aantal aankoopgebeurtenissen op uw site weer. <p>**dit kan u helpen** beter begrijpen welke afmetingspunten aan een orde droegen, door metrische Orden met om het even welke afmeting te combineren. U kunt bijvoorbeeld de beste campagnes (met de dimensie Trackingcode) zien die hebben bijgedragen aan aankopen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals campagnes aanpassen die niet de aankoopdoelstellingen ontmoeten u zou verwachten. </p><p>Deze sjabloon gebruikt metrische opdrachten. |

### Web: Publiek {#web-audience}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--people"
>title="Bekijk het aantal mensen dat met uw merk communiceert."
>abstract="**dit kan u** helpen gebruikstendensen op uw plaats beter begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als maatregel de doeltreffendheid van recente marketing inspanningen in het produceren van nieuwe bezoekers aan uw plaats."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--bots"
>title="Bekijk paginaweergaven en trends met betrekking tot beide verkeer op uw site."
>abstract="**dit kan u helpen** beter de hoeveelheid beide verkeer begrijpen die van uw rapportering, volgens de beide regels wordt gefiltreerd u hebt gevormd.<br/>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als blijven beide activiteit controleren om nieuwe patronen te identificeren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstvsrepeatvisitors"
>title="Een vergelijking weergeven van nieuwe bezoekers die voor het eerst bezoekers willen herhalen."
>abstract="**dit kan u helpen** beter begrijpen de doeltreffendheid van uw plaats in het behouden van klantenloyaliteit, of het tarief waartegen u nieuwe klanten verwerft.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als aansporingen voor toekomstige aankopen aan eerste-tijdbezoekers aanbieden om hen te dwingen terug te keren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--personid"
>title="Bekijk het gedrag van de gebruiker op verschillende kanalen."
>abstract="**dit kan u helpen** beter de volledige klantenreis en interactie over veelvoudige aanraakpunten begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als het personaliseren van marketinginspanningen om gebruikersinstellingen beter te richten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeZoneRankedReport"
>title="Bekijk de bovenste tijdzones van bezoekers die uw site openen."
>abstract="**dit kan u helpen** beter begrijpen waarin tijdstreken uw bezoekers leven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals plaatsonderhoud op tijden aanpassen die het minste aantal mensen zullen beïnvloeden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--location"
>title="Bekijk een overzicht van de locatie van de bezoeker in een kaartvisualisatie."
>abstract="**dit kan u helpen** beter begrijpen waar de bezoekers worden gevestigd die uw plaats bezoeken. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing middelen in de plaatsen waar u de meeste interesse en de kans ziet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--domainRankedReport"
>title="Bekijk de bovenste domeinen van bezoekers die uw site openen."
>abstract="**dit kan u** helpen beter begrijpen welke organisaties uw bezoekers uit komen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als doel uw inhoud bij uw grootste klanten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--topLevelDomainRankedReport"
>title="Bekijk de bovenste domeinen van bezoekers die uw site openen."
>abstract="**dit kan u** helpen beter begrijpen welke organisaties uw bezoekers uit komen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als doel uw inhoud bij uw grootste klanten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--browserWidthRankedReport"
>title="Geef de bovenste browserbreedten weer die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u helpen** beter begrijpen hoe de inhoudsvertoningen aan bezoekers.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend de gemeenschappelijkste browser breedten. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd.<br/> Dit malplaatje gebruikt de Browser afmeting."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--browserHeightRankedReport"
>title="De hoogste browserhoogten weergeven die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u helpen** beter begrijpen hoe de inhoudsvertoningen aan bezoekers.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend de gemeenschappelijkste browser hoogten. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd.<br/> Dit malplaatje gebruikt de Browser afmeting. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--operatingSystemRankedReport"
>title="Geef de naam weer van de besturingssystemen en de versie die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u helpen** beter de gemeenschappelijkste werkende systemen en de versies begrijpen die bezoekers gebruiken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend de hoogste werkende systemen en de versie. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--operatingSystemTypeRankedReport"
>title="Geef de naam weer van de besturingssystemen die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u helpen** beter de gemeenschappelijkste werkende systemen begrijpen die de bezoekers gebruiken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend de hoogste werkende systemen. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--returnFrequencyRankedReport"
>title="Bekijk het telecommunicatiebedrijf dat cellulaire netwerkconnectiviteit aan de mobiele apparaten verstrekt.die de mensen gebruiken om tot uw plaats toegang te hebben."
>abstract="**dit kan u** helpen beter begrijpen welke mobiele dragers het populairst onder uw gebruikersbasis zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw inhoudslevering aanpassen die op de netwerkmogelijkheden van verschillende dragers wordt gebaseerd om een vlotte gebruikerservaring te verzekeren.<br/> Dit malplaatje gebruikt de Mobiele afmeting van de Drager."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--returnVisitorsOvertimeReport"
>title="Bekijk het telecommunicatiebedrijf dat cellulaire netwerkconnectiviteit aan de mobiele apparaten verstrekt.die de mensen gebruiken om tot uw plaats toegang te hebben."
>abstract="**dit kan u** helpen beter begrijpen welke mobiele dragers het populairst onder uw gebruikersbasis zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw inhoudslevering aanpassen die op de netwerkmogelijkheden van verschillende dragers wordt gebaseerd om een vlotte gebruikerservaring te verzekeren.<br/> Dit malplaatje gebruikt de Mobiele afmeting van de Drager."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--visitNumberRankedReport"
>title="Bekijk hoe vaak een bezoeker de site heeft bezocht."
>abstract="**dit kan u helpen** beter begrijpen hoe betrokken bezoekers wanneer het terugkeren naar uw plaats zijn. Dit geldt voor de levensduur van de bezoeker, ongeacht het datumbereik van het project.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals het aanpassen van marketing inspanningen voor frequente bezoekers.<br/> Dit malplaatje gebruikt de het aantalafmeting van het Bezoek."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--customerLoyaltyRankedReport"
>title="Bekijk het aantal bezoekers van uw site dat 0 eerdere aankopen, 1 eerdere aankoop, 2 eerdere aankopen of 3+ eerdere aankopen heeft gedaan."
>abstract="**dit kan u** helpen beter begrijpen hoe uw plaats het kopen gedrag beïnvloedt. .<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk op bezoekers die terugkeren om een aankoop te maken, zodat u gelijkaardig gedrag voor nieuwe bezoekers kunt aanmoedigen.<br/> Dit malplaatje gebruikt de dimensie van de klantenloyaliteit."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--daysBeforeFirstPurchaseRankedReport"
>title="Bekijk het aantal dagen dat verstrijkt tussen de eerste keer dat een bezoeker uw site bereikt en het moment dat hij of zij een aankoop doet. Als een bezoeker bijvoorbeeld één dag na de eerste visite een aankoop doet, behoort een volgend bezoek of evenement tot het item met de dimensie 1 dag."
>abstract="**dit kan u helpen** beter begrijpen hoe lang het bezoekers duurt om een aankoop te maken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als update uw plaats om snellere verwerving aan te moedigen.<br/> Dit malplaatje gebruikt de Dagen vóór eerste koopdimensie."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--daysSinceLastPurchaseRankedReport"
>title="Bekijk de hoeveelheid tijd die is verstreken tussen de huidige treffer van de bezoeker en de meest recente aankoop op dat moment."
>abstract="**dit kan u** helpen bezoekersgedrag beter begrijpen na het kopen van iets op uw plaats.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als update uw plaats om opvolgingsaankopen aan te moedigen.<br/> Dit malplaatje gebruikt de Dagen sinds laatste aankoopafmeting."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenSizeRankedReport"
>title="Bekijk de grootten voor mobiele schermen die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u helpen** beter begrijpen hoe de inhoudsvertoningen aan bezoekers.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend de gemeenschappelijkste mobiele het schermgrootte. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenHeightRankedReport"
>title="Hoogten van mobiele schermen bovenaan weergeven die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u helpen** beter begrijpen hoe de inhoudsvertoningen aan bezoekers.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend de gemeenschappelijkste mobiele het schermhoogten. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenWidthRankedReport"
>title="De bovenste breedten van mobiele schermen weergeven die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u helpen** beter begrijpen hoe de inhoudsvertoningen aan bezoekers.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend de gemeenschappelijkste mobiele het schermbreedten. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--countryGeoReport"
>title="Bekijk het land van oorsprong van de bezoekers van de site."
>abstract="**dit kan u** helpen beter begrijpen wat de populairste landbezoekers van wie uw plaats bezoeken voortkomen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in deze landen te concentreren, of ervoor te zorgen dat uw plaatservaring optimaal in landen is die verschillende primaire talen hebben.<br/> Dit malplaatje gebruikt de dimensie van Landen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--stateGeoReport"
>title="Bekijk de staat (in de Verenigde Staten) waaruit mensen die de site bezoeken, zijn ontstaan. Dit is vergelijkbaar met de Geo Regions template, behalve dat deze specifiek is voor de Verenigde Staten."
>abstract="**dit kan u** helpen beter begrijpen de populairste staten van de V.S. bezoekers van wie uw plaats bezoeken voortkomen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in deze staten te concentreren.<br/> Dit malplaatje gebruikt de dimensie van Staten van de VS."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--regionGeoReport"
>title="Bekijk het geografische gebied van waaruit de bezoekers van de site afkomstig zijn. Een regio is een geografisch gebied dat kleiner is dan een land maar groter dan een stad. In sommige landen is een regio een staat, provincie of prefectuur. In andere gebieden is het een deelland, afdeling of metropolitane regio. "
>abstract="**dit kan u helpen** beter begrijpen de populairste gebiedsbezoekers voortkomen uit wie uw plaats bezoeken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in deze gebieden te concentreren, of ervoor te zorgen dat uw plaatservaring optimaal in gebieden is die verschillende primaire talen hebben. <br/> Dit malplaatje gebruikt identiteitskaart (variabelen/geocountry) en Gebieden dimensies. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cityGeoReport"
>title="Bekijk de stad van waar mensen die de site bezoeken, vandaan komen."
>abstract="**dit kan u** helpen beter begrijpen de populairste stadsbezoekers voortkomen uit wie uw plaats bezoeken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in deze steden te concentreren. <br/> Dit malplaatje gebruikt de dimensie van Steden"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--dmaGeoReport"
>title="Geef de aangewezen marketinggebieden (DMA&#39;s) in de Verenigde Staten weer van waaruit mensen die de site bezoeken, afkomstig zijn."
>abstract="**dit kan u helpen** beter begrijpen de populairste gebiedsbezoekers voortkomen uit wie uw plaats bezoeken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in de meest succesvolle gebieden te concentreren. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--languageRankedReport"
>title="Bekijk de bovenste talen waarin bezoekers inhoud liever zien."
>abstract="**dit kan u helpen** beter de vaakst aangewezen talen van bezoekers begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals de inspanningen van de focuslokalisatie of marketing voor de populairste talen.<br/> Dit malplaatje gebruikt de afmeting van de Taal."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-technology-template"
>title="Informatie weergeven over de technologie die mensen gebruiken om toegang te krijgen tot uw site, zoals besturingssystemen, browsers en apparaten."
>abstract="**dit kan u helpen** beter begrijpen welke technologieën het vaakst wanneer het toegang tot van uw plaats worden gebruikt.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer uw plaats voor de technologieën die worden gebruikt."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--browserRankedReport"
>title="Bekijk de naam en versie van de bovenste browsers die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u helpen** beter begrijpen de gemeenschappelijkste browsers die bezoekers gebruiken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend hoogste browsers. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd.<br/> Dit malplaatje gebruikt de Browser afmeting."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--browserTypeRankedReport"
>title="Geef de namen weer van de organisaties die de beste browsers hebben gemaakt die mensen gebruiken om toegang te krijgen tot uw site. Dit verschilt van het Browser malplaatje in zoverre dat het geen verschillende versies van zelfde browser zoals afzonderlijke afmetingspunten opsomt."
>abstract="**dit kan u helpen** beter de gemeenschappelijkste browsers begrijpen die bezoekers <br/>**gebruiken Gebaseerd op wat u leert, zou u om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend hoogste browsers.** Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd. <br/> Dit malplaatje gebruikt de Browser typeafmeting. "

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Eerste vs herhaal bezoekers**] | Een vergelijking weergeven van nieuwe bezoekers die voor het eerst bezoekers willen herhalen. <p>**dit kan u helpen** beter begrijpen de doeltreffendheid van uw plaats in het behouden van klantenloyaliteit, of het tarief waartegen u nieuwe klanten verwerft.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als aansporingen voor toekomstige aankopen aan eerste-tijdbezoekers aanbieden om hen te dwingen terug te keren.</p><!-- This template uses the --> |
| **identiteitskaart van de Persoon** | Bekijk het gedrag van de gebruiker op verschillende kanalen.<p>**dit kan u helpen** beter de volledige klantenreis en interactie over veelvoudige aanraakpunten begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als het personaliseren van marketinginspanningen om gebruikersinstellingen beter te richten.</p><!-- This template uses the --> |
| **Geo landen** | Bekijk het land van oorsprong van de bezoekers van de site.<p>**dit kan u** helpen beter begrijpen wat de populairste landbezoekers van wie uw plaats bezoeken voortkomen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in deze landen te concentreren, of ervoor te zorgen dat uw plaatservaring optimaal in landen is die verschillende primaire talen hebben.</p><p>In deze sjabloon wordt de landendimensie gebruikt. </p> |
| **Geo de staten van de V.S.** | Bekijk de staat (in de Verenigde Staten) waaruit mensen die de site bezoeken, zijn ontstaan. Dit is vergelijkbaar met de Geo Regions template, behalve dat deze specifiek is voor de Verenigde Staten.<p>**dit kan u** helpen beter begrijpen de populairste staten van de V.S. bezoekers van wie uw plaats bezoeken voortkomen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in deze staten te concentreren.</p><p>Deze sjabloon gebruikt de Amerikaanse dimensie Staten. </p> |
| **Geo gebieden** | Bekijk het geografische gebied van waaruit de bezoekers van de site afkomstig zijn. Een regio is een geografisch gebied dat kleiner is dan een land maar groter dan een stad. In sommige landen is een regio een staat, provincie of prefectuur. In andere gebieden is het een deelland, afdeling of metropolitane regio. <p>**dit kan u helpen** beter begrijpen de populairste gebiedsbezoekers voortkomen uit wie uw plaats bezoeken.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in deze gebieden te concentreren, of ervoor te zorgen dat uw plaatservaring optimaal in gebieden is die verschillende primaire talen hebben. </p><p>Deze sjabloon gebruikt de afmetingen ID(variabelen/geocountry) en Gebieden. </p> |
| **Geo steden** | Bekijk de stad van waar mensen die de site bezoeken, vandaan komen. <p>**dit kan u** helpen beter begrijpen de populairste stadsbezoekers voortkomen uit wie uw plaats bezoeken.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in deze steden te concentreren. </p><p>Deze sjabloon gebruikt de dimensie Steden. </p> |
| **Geo US DMA** | Geef de aangewezen marketinggebieden (DMA&#39;s) in de Verenigde Staten weer van waaruit mensen die de site bezoeken, afkomstig zijn.<p>**dit kan u helpen** beter begrijpen de populairste gebiedsbezoekers voortkomen uit wie uw plaats bezoeken.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als gebruik de gegevens om zich op marketing inspanningen in de meest succesvolle gebieden te concentreren. </p><!-- This template uses the --> |
| **Talen** | Bekijk de bovenste talen waarin bezoekers inhoud liever zien. <p>**dit kan u helpen** beter de vaakst aangewezen talen van bezoekers begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals de inspanningen van de focuslokalisatie of marketing voor de populairste talen.</p><p>Deze sjabloon gebruikt de taaldimensie.</p> |
| **Overzicht van de Technologie** | Informatie weergeven over de technologie die mensen gebruiken om toegang te krijgen tot uw site, zoals besturingssystemen, browsers en apparaten. <p>**dit kan u helpen** beter begrijpen welke technologieën het vaakst wanneer het toegang tot van uw plaats worden gebruikt.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer uw plaats voor de technologieën die worden gebruikt.</p> |
| **Browsers** | Bekijk de naam en versie van de bovenste browsers die mensen gebruiken om toegang te krijgen tot uw site.<p>**dit kan u helpen** beter begrijpen de gemeenschappelijkste browsers die bezoekers gebruiken.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend hoogste browsers. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd.</p><p>Deze sjabloon gebruikt de browserdimensie. </p> |
| **Browser types** | Geef de namen weer van de organisaties die de beste browsers hebben gemaakt die mensen gebruiken om toegang te krijgen tot uw site. Dit verschilt van het Browser malplaatje in zoverre dat het geen verschillende versies van zelfde browser zoals afzonderlijke afmetingspunten opsomt.<p>**dit kan u** helpen beter begrijpen gemeenschappelijkste browsers die de bezoekers gebruiken</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als plaatskwaliteit verbeteren door nieuwe versies van uw plaats te testen gebruikend hoogste browsers. Zo kunnen de inspanningen op het gebied van kwaliteitscontrole worden gemaximaliseerd. </p><p>Deze sjabloon gebruikt de afmetingen voor het browsertype. </p> |

### Web: Verwerving {#web-acquisition}

<!--CJA only-->

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-acquisition-template"
>title="Bekijk hoe uw website bezoekers op mobiele apparaten verkrijgt."
>abstract="**dit kan u helpen** beter meer over de diverse factoren begrijpen die tot verwerving, zoals onderzoekshoofdwoorden, verwijzend domein, etc. leiden.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen in de meest efficiënte kanalen.<br/> Dit malplaatje gebruikt metrische het Tarief van de Stuitage en metrische Bounces. Het gebruikt ook de afmeting van de Motor van het Onderzoek, de afmeting van het Sleutelwoord van het Onderzoek, de afmeting van de Pagina van de Ingang, de afmeting van het Verwijzen van het Domein, het Volgen van de afmeting van de Code, en de afmeting van de Referateur."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--advertisingAnalyticsPaidSearch"
>title="Bekijk al je gegevens voor Google en Bing Paid Search naast elkaar."
>abstract="**dit kan u helpen** beter begrijpen de hoeveelheid verkeer dat naar uw plaats wordt verzonden en of de klanten converteren.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als schatting van de kosteneffectiviteit van een advertentiecampagne."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--searchEngineRankRankedReport"
>title="Bekijk welke pagina met zoekresultaten een bezoeker op uw site heeft geklikt. Als uw site bijvoorbeeld op de tweede pagina van de zoekresultaten van een zoekmachine wordt weergegeven, is Pagina 2 zoeken het dimensie-item voor deze variabele."
>abstract="**dit kan u helpen** beter begrijpen hoe hoog uw pagina&#39;s in onderzoeksresultaten rangschikken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, uw strategie van ZOO verbeteren om ervoor te zorgen dat uw inhoud op de eerste pagina van onderzoeksresultaten verschijnt."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--marketing-channel-overview-template"
>title="Wanneer u aangepaste kenmerk gebruikt, wordt in deze sjabloon getoond hoe bezoekers op uw site aankomen."
>abstract="**dit kan u helpen** beter begrijpen welke van uw marketing kanalen het meest efficiënt zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als zou zwaarder in efficiënte marketing kanalen investeren en van minder het uitvoeren van marketing kanalen afstoten.<br/> Dit malplaatje gebruikt identiteitskaart (variabelen/het marketingkanaal) afmeting en metrisch van de Opbrengst."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstouchChannelRankedReport"
>title="Bekijk het eerste marketingkanaal waarmee een bezoeker tijdens de aanspreekperiode van die bezoeker overeenkomt (standaard 30 dagen)."
>abstract="**dit kan u helpen** beter begrijpen welke marketing kanalen aanvankelijke verkeer aan uw plaats drijven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op gebieden die het meest effectief zijn.<br/> Dit malplaatje gebruikt de Eerste dimensie van het Kanaal van de Aanraking."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstouchChannelDetailRankedReport"
>title="Bekijk details over het eerste marketingkanaal waarmee een bezoeker tijdens de aanspreekperiode van die bezoeker overeenkomt (standaard 30 dagen)."
>abstract="**dit kan u helpen** beter begrijpen wat aan de slag aanpassing een marketing kanaal bijdroeg. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op gebieden die het meest effectief zijn.<br/> Dit malplaatje gebruikt de Eerste dimensie van het Detail van het Kanaal van de Aanraking."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--campaignConversionReport"
>title="Bekijk het aantal klikcontroles en kassen voor uw campagnes."
>abstract="**dit kan u helpen** beter begrijpen hoe de marketing campagnes omzetting drijven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als bepalen welke marketing campagnes het meeste ROI produceren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--retail-campaign-performance-template"
>title="Bekijk details over hoe je marketingcampagnes presteren."
>abstract="**dit kan u** helpen meer over de diverse succesindicatoren begrijpen verbonden aan campagnes, zoals opbrengst, productmeningen, orden, etc.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op de campagnes die de meeste opbrengst drijven. <br/> Dit malplaatje gebruikt metrische de Inkomsten, metrische de Kijken van het Product, metrische de Toevoegingen van de Kar, Metrische Orden, en metrische Eenheden. Het gebruikt ook de het Volgen dimensie van de Code en de Verwijzende dimensie van het Domein."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-acquisition-template"
>title="Bekijk hoe uw website bezoekers verkrijgt."
>abstract="**dit kan u helpen** beter meer over de diverse factoren begrijpen die tot verwerving, zoals onderzoekshoofdwoorden, verwijzend domein, etc. leiden.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen in de meest efficiënte kanalen.<br/> Dit malplaatje gebruikt metrische het Tarief van de Stuitage en metrische Bounces. Het gebruikt ook de afmeting van de Motor van het Onderzoek, de afmeting van het Sleutelwoord van het Onderzoek, de afmeting van de Pagina van de Ingang, de afmeting van het Verwijzen van het Domein, het Volgen van de afmeting van de Code, en de afmeting van de Referateur."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchKeywordRankedReport"
>title="Bekijk de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken, ongeacht of deze betaald of natuurlijk is."
>abstract="**dit kan u helpen** beter de sleutelwoorden begrijpen mensen in onderzoeken gebruiken die in plaatsverkeer resulteren. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als identificeer en vul SEO hiaten tussen sleutelwoorden die worden gebruikt en die die plaatsverkeer drijven.<br/> Dit malplaatje gebruikt de afmeting van het Sleutelwoord van het Onderzoek."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchPaidKeywordRankedReport"
>title="Bekijk de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken. Deze trefwoorden komen overeen met gevonden zoekopdrachten."
>abstract="**dit kan u helpen** beter de sleutelwoorden begrijpen mensen in onderzoeken gebruiken die in plaatsverkeer resulteren.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als identificeer en vul SEO hiaten tussen sleutelwoorden die worden gebruikt en die die plaatsverkeer drijven. <br/> Dit malplaatje gebruikt het Trefwoord van het Onderzoek - Betaalde afmeting. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchNaturalKeywordRankedReport"
>title="Bekijk de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken. Deze trefwoorden komen niet overeen met gevonden zoekopdrachten."
>abstract="**dit kan u helpen** beter de sleutelwoorden begrijpen mensen in onderzoeken gebruiken die in plaatsverkeer resulteren.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als identificeer en vul SEO hiaten tussen sleutelwoorden die worden gebruikt en die die plaatsverkeer drijven.<br/> Dit malplaatje gebruikt het Sleutelwoord van het Onderzoek - Natuurlijke afmeting. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchRankedReport"
>title="Bekijk de zoekprogramma&#39;s die bezoekers gebruiken om uw site te bereiken, ongeacht of ze betaald of natuurlijk zijn."
>abstract="**dit kan u helpen** beter begrijpen de onderzoeksmotoren mensen gebruiken die in plaatsverkeer resulteren. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als nadruk uw inspanningen SEO op de onderzoeksmotoren die het meeste verkeer aan de plaats drijven.<br/> Dit malplaatje gebruikt de afmeting van de Motor van het Onderzoek. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchPaidRankedReport"
>title="Bekijk de zoekprogramma&#39;s die bezoekers gebruiken om uw site te bereiken en die overeenkomen met betaalde zoekdetectie."
>abstract="**dit kan u helpen** beter begrijpen de onderzoeksmotoren mensen gebruiken die in plaatsverkeer resulteren.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als nadruk uw inspanningen SEO op de onderzoeksmotoren die het meeste verkeer aan de plaats drijven. <br/> Dit malplaatje gebruikt de Motor van het Onderzoek - Betaalde afmeting."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchNaturalRankedReport"
>title="Bekijk de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken. Deze trefwoorden komen niet overeen met gevonden zoekopdrachten."
>abstract="**dit kan u helpen** beter begrijpen de onderzoeksmotoren mensen gebruiken die in plaatsverkeer resulteren.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als nadruk uw inspanningen SEO op de onderzoeksmotoren die het meeste verkeer aan de plaats drijven.<br/> Dit malplaatje gebruikt de Motor van het Onderzoek - Natuurlijke afmeting."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referringDomainRankedReport"
>title="Bekijk welke domeinen mensen door klikken om uw plaats te bereiken."
>abstract="**dit kan u helpen** beter begrijpen welke derdeplaatsen het meeste verkeer aan u drijven. (Er moet een koppeling bestaan op de externe site en een bezoeker moet erop klikken om het dimensie-item weer te geven.)<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als creeer of pas inhoud aan beter zich aan de belangen van bezoekers die uit hoogste verwijzende domeinen komen. <br/> Dit malplaatje gebruikt de Verwijzende dimensie van het Domein."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referringDomainOriginalRankedReport"
>title="Bekijk het eerste verwijzende domein dat mensen door klikte om uw plaats te bereiken. (Nadat deze is ingesteld, bevat deze dezelfde waarde voor de gehele levensduur van de desbetreffende bezoekersidentiteitskaart.)"
>abstract="**dit kan u helpen** beter begrijpen welke derdeplaatsen oorspronkelijk verkeer aan uw plaats drijven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als creeer of pas inhoud aan beter zich aan de belangen van bezoekers die uit hoogste originele verwijzende domeinen komen. <br/> Dit malplaatje gebruikt de Originele Verwijzende dimensie van het Domein."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referrerRankedReport"
>title="Bekijk welke URL&#39;s bezoekers hadden toen u door klikte om uw site te bereiken. (De externe URL moet een koppeling bevatten en een bezoeker moet erop klikken om het dimensie-item weer te geven.)"
>abstract="**dit kan u helpen** beter begrijpen welke specifieke URLs het meeste verkeer aan uw plaats drijven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als creeer of pas inhoud aan beter zich aan de belangen van bezoekers die van hoogste URLs komen. <br/> Dit malplaatje gebruikt de Verwijzende dimensie van het Domein.</p>"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referrerTypeRankedReport"
>title="Bekijk welke algemene kanalen bezoekers hebben doorgeklikt om op uw site te komen. Adobe handhaaft de regels voor elk kanaal. Mogelijke kanalen zijn zoekprogramma&#39;s, sociale netwerken, andere websites, vaste schijf of e-mail."
>abstract="**dit kan u helpen** beter begrijpen welk type van verwijzers het meeste verkeer aan uw plaats drijven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als creeer of pas inhoud aan beter zich aan de belangen van bezoekers die van een bepaald kanaal komen.<br/> Dit malplaatje gebruikt de afmeting van het Type van Referateur."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **de kanalen van de Marketing**] > [!UICONTROL **het overzichtsrapport van het Kanaal**] | Wanneer u aangepaste kenmerk gebruikt, wordt in deze sjabloon getoond hoe bezoekers op uw site aankomen.<p>**dit kan u helpen** beter begrijpen welke van uw marketing kanalen het meest efficiënt zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als zou zwaarder in efficiënte marketing kanalen investeren en van minder het uitvoeren van marketing kanalen afstoten.</p><p>Deze sjabloon gebruikt de dimensie ID(variables/marketing channel) en de maatstaf van de Opbrengst.</p> |
| [!UICONTROL **de kanalen van de Marketing**] > [!UICONTROL **Eerste aanrakingskanaal**] | Bekijk het eerste marketingkanaal waarmee een bezoeker tijdens de aanspreekperiode van die bezoeker overeenkomt (standaard 30 dagen). <p>**dit kan u helpen** beter begrijpen welke marketing kanalen aanvankelijke verkeer aan uw plaats drijven.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op gebieden die het meest effectief zijn.</p><p>Deze sjabloon gebruikt de dimensie Eerste aanraakkanaal.</p> |
| [!UICONTROL **de kanalen van de Marketing**] > [!UICONTROL **Eerste detail van het aanrakingskanaal**] | Bekijk details over het eerste marketingkanaal waarmee een bezoeker tijdens de aanspreekperiode van die bezoeker overeenkomt (standaard 30 dagen).<p>**dit kan u helpen** beter begrijpen wat aan de slag aanpassing een marketing kanaal bijdroeg. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op gebieden die het meest effectief zijn.</p><p>In deze sjabloon wordt de dimensie Details eerste aanraakkanaal gebruikt.</p> |
| [!UICONTROL **de kanalen van de Marketing**] > [!UICONTROL **Laatste aanrakingskanaal**] | Bekijk het meest recente marketingkanaal waarmee een bezoeker tijdens de aanspreekperiode van die bezoeker overeenkomt (standaard 30 dagen).<p>**dit kan u helpen** beter begrijpen welke marketing kanalen verkeer aan uw plaats drijven die in omzettingen resulteren.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op gebieden die het meest effectief zijn.</p><p>Deze sjabloon gebruikt de afmeting Laatste aanraakkanaal.  </p> |
| [!UICONTROL **de kanalen van de Marketing**] > [!UICONTROL **Laatste detail van het aanrakingskanaal**] | Details weergeven over het meest recente marketingkanaal waarmee een bezoeker tijdens de aanspreekperiode van die bezoeker overeenkomt (standaard 30 dagen)<p>**dit kan u helpen** beter begrijpen wat aan de slag aanpassing een marketing kanaal bijdroeg. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op gebieden die het meest effectief zijn. </p><p>In deze sjabloon wordt de dimensie Details laatste aanraakkanaal gebruikt. </p> |
| [!UICONTROL **Campagnes**] > [!UICONTROL **het Volgen code**] | Geef de namen van trackingcodes op uw site weer. U kunt koppelingen met verschillende parameterwaarden voor queryreeksen op verschillende locaties op internet plaatsen.<p>**dit kan u helpen** beter begrijpen welke verbindingen het meest succesvol in het drijven van verkeer aan uw plaats waren. Tekenreeksen voor bijhouden van code worden vaak toegevoegd in e-mails, advertenties, berichten op sociale media en andere marketingactiviteiten die uw organisatie gebruikt</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op de campagnes die de meeste opbrengst drijven.</p><p>Deze sjabloon gebruikt de dimensie Trackingcode. </p> |
| [!UICONTROL **Campagnes**] > [!UICONTROL **de conversietrechter van de Campagne**] | Bekijk het aantal klikcontroles en kassen voor uw campagnes. <p>**dit kan u helpen** beter begrijpen hoe de marketing campagnes omzetting drijven.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als bepalen welke marketing campagnes het meeste ROI produceren.</p> |
| [!UICONTROL **Campagnes**] > [!UICONTROL **prestaties van de Campagne**] | Bekijk details over hoe je marketingcampagnes presteren.<p>**dit kan u** helpen meer over de diverse succesindicatoren begrijpen verbonden aan campagnes, zoals opbrengst, productmeningen, orden, etc.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op de campagnes die de meeste opbrengst drijven. </p><p>Deze sjabloon gebruikt metrische inkomsten, Metrische productweergaven, Metrische optellingen van kunsttoevoegingen, Metrische Orden, en metrische eenheden. Het gebruikt ook de het Volgen dimensie van de Code en de Verwijzende dimensie van het Domein. </p> |
| **de aanwinst van het Web** | Bekijk hoe uw website bezoekers verkrijgt.<p>**dit kan u helpen** beter meer over de diverse factoren begrijpen die tot verwerving, zoals onderzoekshoofdwoorden, verwijzend domein, etc. leiden.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen in de meest efficiënte kanalen.</p><p>Deze sjabloon gebruikt de metrische waarde Bounce Rate en de metrische waarde Bounces. Het gebruikt ook de afmeting van de Motor van het Onderzoek, de afmeting van het Sleutelwoord van het Onderzoek, de afmeting van de Pagina van de Ingang, de afmeting van het Verwijzen van het Domein, het Volgen van de afmeting van de Code, en de afmeting van de Referateur.  </p> |
| **de wachtwoorden van het Onderzoek - allen** | Bekijk de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken, ongeacht of deze betaald of natuurlijk is. <p>**dit kan u helpen** beter de sleutelwoorden begrijpen mensen in onderzoeken gebruiken die in plaatsverkeer resulteren. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als identificeer en vul SEO hiaten tussen sleutelwoorden die worden gebruikt en die die plaatsverkeer drijven.</p><p>Deze sjabloon gebruikt de dimensie Trefwoord zoeken. </p> |
| **de sleutelwoorden van het Onderzoek - betaalde** | Bekijk de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken. Deze trefwoorden komen overeen met gevonden zoekopdrachten.<p>**dit kan u helpen** beter de sleutelwoorden begrijpen mensen in onderzoeken gebruiken die in plaatsverkeer resulteren.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als identificeer en vul SEO hiaten tussen sleutelwoorden die worden gebruikt en die die plaatsverkeer drijven. </p><p>Deze sjabloon gebruikt de afmeting Trefwoord zoeken - Betaald. </p> |
| **de sleutelwoorden van het Onderzoek - natuurlijk** | Bekijk de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken. Deze trefwoorden komen niet overeen met gevonden zoekopdrachten.<p>**dit kan u helpen** beter de sleutelwoorden begrijpen mensen in onderzoeken gebruiken die in plaatsverkeer resulteren.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als identificeer en vul SEO hiaten tussen sleutelwoorden die worden gebruikt en die die plaatsverkeer drijven.</p><p>Deze sjabloon gebruikt het trefwoord Zoeken - Natuurlijk. </p> |
| **motoren van het Onderzoek - allen** | Bekijk de zoekprogramma&#39;s die bezoekers gebruiken om uw site te bereiken, ongeacht of ze betaald of natuurlijk zijn. <p>**dit kan u helpen** beter begrijpen de onderzoeksmotoren mensen gebruiken die in plaatsverkeer resulteren. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als nadruk uw inspanningen SEO op de onderzoeksmotoren die het meeste verkeer aan de plaats drijven.</p><p>Deze sjabloon gebruikt de dimensie Zoekmachine. </p> |
| **de motoren van het Onderzoek - betaalde** | Bekijk de zoekprogramma&#39;s die bezoekers gebruiken om uw site te bereiken en die overeenkomen met betaalde zoekdetectie.<p>**dit kan u helpen** beter begrijpen de onderzoeksmotoren mensen gebruiken die in plaatsverkeer resulteren.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als nadruk uw inspanningen SEO op de onderzoeksmotoren die het meeste verkeer aan de plaats drijven. </p><p>Deze sjabloon gebruikt de afmeting Zoekmachine - Betaald. </p> |
| **Duidelijkheden van het Onderzoek - natuurlijk** | Bekijk de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken. Deze trefwoorden komen niet overeen met gevonden zoekopdrachten.<p>**dit kan u helpen** beter begrijpen de onderzoeksmotoren mensen gebruiken die in plaatsverkeer resulteren.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als nadruk uw inspanningen SEO op de onderzoeksmotoren die het meeste verkeer aan de plaats drijven.</p><p>Deze sjabloon gebruikt de zoekengine - Natuurlijke dimensie. </p> |
| **Verwijzend domeinen** | Bekijk welke domeinen mensen door klikken om uw plaats te bereiken.<p>**dit kan u helpen** beter begrijpen welke derdeplaatsen het meeste verkeer aan u drijven. (Er moet een koppeling bestaan op de externe site en een bezoeker moet erop klikken om het dimensie-item weer te geven.)</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als creeer of pas inhoud aan beter zich aan de belangen van bezoekers die uit hoogste verwijzende domeinen komen. </p><p>Deze sjabloon gebruikt de dimensie Refererend domein. </p> |
| **Origineel verwijzende domeinen** | Bekijk het eerste verwijzende domein dat mensen door klikte om uw plaats te bereiken. (Nadat deze is ingesteld, bevat deze dezelfde waarde voor de gehele levensduur van de desbetreffende bezoekersidentiteitskaart.)<p>**dit kan u helpen** beter begrijpen welke derdeplaatsen oorspronkelijk verkeer aan uw plaats drijven.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als creeer of pas inhoud aan beter zich aan de belangen van bezoekers die uit hoogste originele verwijzende domeinen komen. </p><p>Deze sjabloon gebruikt de dimensie Origineel verwijzend domein. </p> |
| **Referrers** | Bekijk welke URL&#39;s bezoekers hadden toen u door klikte om uw site te bereiken. (De externe URL moet een koppeling bevatten en een bezoeker moet erop klikken om het dimensie-item weer te geven.)  <p>**dit kan u helpen** beter begrijpen welke specifieke URLs het meeste verkeer aan uw plaats drijven.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als creeer of pas inhoud aan beter zich aan de belangen van bezoekers die van hoogste URLs komen. </p><p>Deze sjabloon gebruikt de dimensie Refererend domein </p><p>Deze sjabloon gebruikt de dimensie Referrer. </p> |
| **de types van Refererder** | Bekijk welke algemene kanalen bezoekers hebben doorgeklikt om op uw site te komen. Adobe handhaaft de regels voor elk kanaal. Mogelijke kanalen zijn zoekprogramma&#39;s, sociale netwerken, andere websites, vaste schijf of e-mail.<p>**dit kan u helpen** beter begrijpen welk type van verwijzers het meeste verkeer aan uw plaats drijven.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als creeer of pas inhoud aan beter zich aan de belangen van bezoekers die van een bepaald kanaal komen.</p><p>Deze sjabloon gebruikt de dimensie Type referentie.</p> |

### Mobiel: mobiele toepassing {#mobile-app}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileappscreens"
>title="Bekijk het aantal gebeurtenissen, sessies en personen dat aan elk scherm op de mobiele app is gekoppeld."
>abstract="**dit kan u** helpen beter begrijpen welke schermen op uw plaats het populairst zijn.<br/>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als inhoud op de populairste schermen verbeteren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileappactions"
>title="Bekijk de acties die mensen uitvoeren op uw mobiele app."
>abstract="**dit kan u helpen** beter begrijpen hoe de mensen uw app en de waarde gebruiken zij uit het krijgen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als ontwikkelt eigenschappen die aanvullen of op die verbeteren die het populairst zijn."

<!-- markdownlint-enable MD034 -->

<!--CJA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-lifecycle-metrics-app-usage-template"
>title="Bekijk het aantal gebruikers, startende gebruikers en wordt de app voor het eerst gestart, plus de gemiddelde sessielengte."
>abstract="**dit kan u** helpen beter begrijpen hoeveel uw app wordt gebruikt. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als toepassingsprestaties verbeteren zodat kan het aan de hoeveelheid gebruik schrapen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-journeys"
>title="Bekijk de opvallende gebruikspatronen voor uw mobiele app."
>abstract="**dit kan u** helpen beter begrijpen hoe de mensen uw app gebruiken. <br/>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als verbeteren hoe de mensen van één scherm aan een andere kunnen krijgen om de gemeenschappelijkste werkschema&#39;s te richten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-key-metrics"
>title="Bekijk enkele van de meest gangbare maatstaven voor mobiele apps."
>abstract="**dit kan u** helpen basisprestaties van uw mobiele app beter begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals de algemene gezondheid en de prestaties van uw app beoordelen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-messaging"
>title="Geef prestatiegegevens weer voor berichten in de app en pushberichten voor uw app."
>abstract="**dit kan u** helpen beter begrijpen hoe de mensen in-app overseinenmogelijkheden gebruiken, evenals hoe effectief duwen berichten verkeer aan uw app drijven.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als verbeteren de ervaring van het in-app overseinenpushbericht."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-performance-template"
>title="Bekijk hoe uw app presteert en waar gebruikers problemen ondervinden."
>abstract="**dit kan u helpen** beter begrijpen als de mensen die uw app gebruiken langzame of degraded prestaties tegenkomen. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als moeilijke situatie bestaande kwesties of verbetert app prestaties alvorens de kwesties voorkomen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-retention"
>title="Bekijk welke gebruikers de meest loyale gebruikers van uw app zijn en wat ze in de app doen."
>abstract="**dit kan u helpen** beter begrijpen hoe uw meest loyale gebruikers uw app gebruiken.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw marketing inspanningen voor de eigenschappen verbeteren die uw meest loyale gebruikers gebruiken."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Mobiele toepassingsschermen**] | Bekijk het aantal gebeurtenissen, sessies en personen dat aan elk scherm op de mobiele app is gekoppeld.<p>**dit kan u** helpen beter begrijpen welke schermen op uw plaats het populairst zijn.</p><p>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als inhoud op de populairste schermen verbeteren.</p><p>Deze sjabloon gebruikt de metriek voor gebeurtenissen, sessies, personen en percentage. Ook wordt de dimensie Paginatitel gebruikt.</p> |
| **Mobiele toepassingsacties** | Bekijk de acties die mensen uitvoeren op uw mobiele app. <p>**dit kan u helpen** beter begrijpen hoe de mensen uw app en de waarde gebruiken zij uit het krijgen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als ontwikkelt eigenschappen die aanvullen of op die verbeteren die het populairst zijn.</p><p>Deze sjabloon gebruikt de metriek voor gebeurtenissen, sessies, personen en percentage. |
| **Mobiel toepassingsgebruik** | Bekijk het aantal gebruikers, startende gebruikers en wordt de app voor het eerst gestart, plus de gemiddelde sessielengte.<p>**dit kan u** helpen beter begrijpen hoeveel uw app wordt gebruikt. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als toepassingsprestaties verbeteren zodat kan het aan de hoeveelheid gebruik schrapen.</p><!-- This template uses the --> |
| **Mobiele app reizen** | Bekijk de opvallende gebruikspatronen voor uw mobiele app. <p>**dit kan u** helpen beter begrijpen hoe de mensen uw app gebruiken. </p><p>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als verbeteren hoe de mensen van één scherm aan een andere kunnen krijgen om de gemeenschappelijkste werkschema&#39;s te richten. </p><!-- This template uses the --> |
| **Mobiele toepassingsmetriek** | Bekijk enkele van de meest gangbare maatstaven voor mobiele apps. <p>**dit kan u** helpen basisprestaties van uw mobiele app beter begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals de algemene gezondheid en de prestaties van uw app beoordelen.</p><!-- This template uses the --> |
| **Mobiel app overseinen** | Geef prestatiegegevens weer voor berichten in de app en pushberichten voor uw app.<p>**dit kan u** helpen beter begrijpen hoe de mensen in-app overseinenmogelijkheden gebruiken, evenals hoe effectief duwen berichten verkeer aan uw app drijven.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als verbeteren de ervaring van het in-app overseinenpushbericht.</p><!-- This template uses the --> |
| **Mobiele toepassingsprestaties** | Bekijk hoe uw app presteert en waar gebruikers problemen ondervinden. <p>**dit kan u helpen** beter begrijpen als de mensen die uw app gebruiken langzame of degraded prestaties tegenkomen. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als moeilijke situatie bestaande kwesties of verbetert app prestaties alvorens de kwesties voorkomen.</p><!-- This template uses the --> |
| **Mobiele toepassingsbehoud** | Bekijk welke gebruikers de meest loyale gebruikers van uw app zijn en wat ze in de app doen. <p>**dit kan u helpen** beter begrijpen hoe uw meest loyale gebruikers uw app gebruiken.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw marketing inspanningen voor de eigenschappen verbeteren die uw meest loyale gebruikers gebruiken.</p><!-- This template uses the --> |

### Mobiel: informatie over mobiele apparaten {#mobile-devices}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileCarrierRankedReport"
>title="Bekijk het telecommunicatiebedrijf dat cellulaire netwerkconnectiviteit aan de mobiele apparaten verstrekt.die de mensen gebruiken om tot uw plaats toegang te hebben."
>abstract="**dit kan u** helpen beter begrijpen welke mobiele dragers het populairst onder uw gebruikersbasis zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw inhoudslevering aanpassen die op de netwerkmogelijkheden van verschillende dragers wordt gebaseerd om een vlotte gebruikerservaring te verzekeren.<br/> Dit malplaatje gebruikt de Mobiele afmeting van de Drager."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileDeviceNameRankedReport"
>title="Bekijk het merk en het model van mobiele apparaten die mensen gebruiken om toegang te krijgen tot uw site."
>abstract="**dit kan u** helpen beter begrijpen welke mobiele apparaten het populairst onder uw gebruikersbasis zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer het teruggeven van uw plaats voor de gemeenschappelijkste mobiele apparaten.<br/> Dit malplaatje gebruikt de Mobiele dimensie van de Naam van het Apparaat."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileDeviceTypeRankedReport"
>title="Bekijk de typen mobiele apparaten die mensen gebruiken om toegang te krijgen tot uw site, zoals telefoons en tablets."
>abstract="**dit kan u helpen** beter de diverse soorten mobiele apparaten begrijpen die worden gebruikt om tot uw plaats toegang te hebben.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer uw plaats voor de types van mobiele apparaten die het meest worden gebruikt.<br/> Dit malplaatje gebruikt de Mobiele dimensie van het Type van Apparaat."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileManufacturerRankedReport"
>title="Bekijk welke fabrikanten de mobiele apparaten produceren die mensen gebruiken om uw site te openen, zoals Apple en Samsung."
>abstract="**dit kan u** helpen beter begrijpen welke fabrikanten onder uw gebruikersbasis populairst zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw inhoudslevering aanpassen die op de capaciteiten van verschillende fabrikanten wordt gebaseerd om een vlotte gebruikerservaring te verzekeren.<br/> Dit malplaatje gebruikt de Mobiele afmeting van de Fabrikant."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Mobiele drager**] | Bekijk het telecommunicatiebedrijf dat cellulaire netwerkconnectiviteit aan de mobiele apparaten verstrekt.die de mensen gebruiken om tot uw plaats toegang te hebben.<p>**dit kan u** helpen beter begrijpen welke mobiele dragers het populairst onder uw gebruikersbasis zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw inhoudslevering aanpassen die op de netwerkmogelijkheden van verschillende dragers wordt gebaseerd om een vlotte gebruikerservaring te verzekeren.</p><p>Deze sjabloon gebruikt de dimensie Mobiele drager.</p> |
| **Apparaten** | Bekijk het merk en het model van mobiele apparaten die mensen gebruiken om toegang te krijgen tot uw site.<p>**dit kan u** helpen beter begrijpen welke mobiele apparaten het populairst onder uw gebruikersbasis zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer het teruggeven van uw plaats voor de gemeenschappelijkste mobiele apparaten.</p><p>Deze sjabloon gebruikt de dimensie Mobiele apparaatnaam.</p> |
| **Type van Apparaat** | Bekijk de typen mobiele apparaten die mensen gebruiken om toegang te krijgen tot uw site, zoals telefoons en tablets.<p>**dit kan u helpen** beter de diverse soorten mobiele apparaten begrijpen die worden gebruikt om tot uw plaats toegang te hebben.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer uw plaats voor de types van mobiele apparaten die het meest worden gebruikt.</p><p>Deze sjabloon gebruikt de dimensie Mobiel apparaattype.</p> |
| **Fabrikant** | Bekijk welke fabrikanten de mobiele apparaten produceren die mensen gebruiken om uw site te openen, zoals Apple en Samsung.<p>**dit kan u** helpen beter begrijpen welke fabrikanten onder uw gebruikersbasis populairst zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw inhoudslevering aanpassen die op de capaciteiten van verschillende fabrikanten wordt gebaseerd om een vlotte gebruikerservaring te verzekeren.</p><p>Deze sjabloon gebruikt de dimensie Mobiele fabrikant.</p> |

### Tijd delen {#time-parting}

<!--CJA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--minuteOfHour"
>title="Bekijk het aantal gebeurtenissen, sessies en personen op uw site, opgesplitst per minuut. Bijvoorbeeld, als u een rapport met een rapporteringstimeframe van één enkele dag hebt, wordt de eerste minuut van elk uur in de dag gegroepeerd in het zelfde afmetingspunt."
>abstract="**dit kan u helpen** beter tendensen op een korrelig niveau begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer middelen voor piektijden, neer aan de minuut.<br/> Dit malplaatje gebruikt het Minuut van de afmeting van het Uur."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--hourOfDay"
>title="Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar uur van de dag. Bijvoorbeeld, als u een rapport hebt dat 1 Januari - 7 overspant, wordt het eerste uur van elke dag gegroepeerd in het zelfde afmetingspunt."
>abstract="**dit kan u helpen** beter de tijd van dag begrijpen wanneer uw plaats het vaakst en minst vaak wordt bezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer gegevensverwerkingsmiddelen aan uw plaats tijdens hoog-verkeersuren toewijzen.<br/> Dit malplaatje gebruikt de dimensie van het Uur van Dag."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--am-pm"
>title="Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar AM en PM. Bijvoorbeeld, als u een rapport hebt dat 1 Januari - 7 overspant, worden de uren AM van elke dag gegroepeerd in het zelfde afmetingspunt."
>abstract="***dit kan u helpen** beter begrijpen de tijd van dag wanneer uw plaats het vaakst en minst vaak wordt bezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer gegevensverwerkingsmiddelen aan uw plaats tijdens hoog-verkeersuren toewijzen.<br/> Dit malplaatje gebruikt de dimensie AM/PM."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--dayOfWeek"
>title="Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar dag van de week. Bijvoorbeeld, als u een rapport hebt dat de maand van Januari overspant, wordt elke dag van de week gegroepeerd in het zelfde afmetingspunt."
>abstract="**dit kan u** helpen beter begrijpen welke dagen van de week uw plaats het vaakst en minst vaak wordt bezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersdagen.<br/> Dit malplaatje gebruikt de dimensie van de Dag van Week."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--dayOfMonth"
>title="Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar dag van de maand. Bijvoorbeeld, als u een rapport hebt dat een volledig jaar overspant, wordt elke dag van de maand gegroepeerd in het zelfde afmetingspunt."
>abstract="**dit kan u** helpen beter begrijpen welke dagen van elke maand uw plaats het vaakst en minst vaak wordt bezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersdagen.<br/> Dit malplaatje gebruikt de dimensie van de Dag van Maand."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--dayOfYear"
>title="Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar dag van het jaar. Bijvoorbeeld, als u een rapport hebt dat veelvoudige jaren overspant, wordt elke dag van het jaar gegroepeerd in het zelfde afmetingspunt."
>abstract="**dit kan u** helpen beter begrijpen welke dagen van elk jaar uw plaats het vaakst en minst vaak wordt bezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersdagen.<br/> Dit malplaatje gebruikt de dimensie van Dag van Jaar."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--weekdayWeekend"
>title="Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar weekdagen en weekends. Bijvoorbeeld, als u een rapport hebt dat de maand van Januari overspannen, worden de weekdagen en weekends gegroepeerd in afzonderlijke afmetingspunten."
>abstract="**dit kan u helpen** beter de verschillen in plaatsverkeer voor weekdagen tegenover weekends begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum zwaarder op weekends, als het rapport erop wijst dat de weekends meer dan weekdagen zijn.<br/> Dit malplaatje gebruikt de dimensie Weekday/Weekend."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--weekOfYear"
>title="Bekijk gebeurtenissen, sessies en personen op uw site, uitgesplitst naar week van het jaar. Bijvoorbeeld, als u een rapport hebt dat veelvoudige jaren overspant, wordt elke week gegroepeerd in het zelfde afmetingspunt."
>abstract="**dit kan u** helpen beter begrijpen welke weken van het jaar uw plaats het vaakst en minst vaak wordt bezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersweken, zoals tijdens de vakanties.<br/> Dit malplaatje gebruikt de Week van de dimensie van het Jaar."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--monthOfYear"
>title="Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar maand van het jaar. Bijvoorbeeld, als u een rapport hebt dat veelvoudige jaren overspant, wordt elke maand gegroepeerd in het zelfde afmetingspunt."
>abstract="**dit kan u** helpen beter begrijpen welke maanden uw plaats het vaakst en het minst vaak wordt bezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersmaanden, zoals tijdens de vakanties.<br/> Dit malplaatje gebruikt de Maand van de afmeting van het Jaar."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--quarterOfYear"
>title="Bekijk gebeurtenissen, sessies en personen op uw site, uitgesplitst naar kwart van het jaar. Bijvoorbeeld, als u een rapport hebt dat veelvoudige jaren overspant, wordt elk kwartaal gegroepeerd in het zelfde afmetingspunt."
>abstract="**dit kan u** helpen beter begrijpen welke kwarten uw plaats het vaakst en het minst vaak wordt bezocht.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals tijd de lancering van producten om historisch laag-verkeerskwarten op te voeren.<br/> Dit malplaatje gebruikt het Kwartaal van de afmeting van het Jaar."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Minuut van uur**] | Bekijk het aantal gebeurtenissen, sessies en personen op uw site, opgesplitst per minuut. Bijvoorbeeld, als u een rapport met een rapporteringstimeframe van één enkele dag hebt, wordt de eerste minuut van elk uur in de dag gegroepeerd in het zelfde afmetingspunt.<p>**dit kan u helpen** beter tendensen op een korrelig niveau begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer middelen voor piektijden, neer aan de minuut.</p><p>Deze sjabloon gebruikt het Minuut van de dimensie van het Uur.</p> |
| **Uur van dag** | Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar uur van de dag. Bijvoorbeeld, als u een rapport hebt dat 1 Januari - 7 overspant, wordt het eerste uur van elke dag gegroepeerd in het zelfde afmetingspunt.<p>**dit kan u helpen** beter de tijd van dag begrijpen wanneer uw plaats het vaakst en minst vaak wordt bezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer gegevensverwerkingsmiddelen aan uw plaats tijdens hoog-verkeersuren toewijzen.</p><p>Deze sjabloon gebruikt de dimensie Uur van Dag.</p> |
| **AM/PM** | Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar AM en PM. Bijvoorbeeld, als u een rapport hebt dat 1 Januari - 7 overspant, worden de uren AM van elke dag gegroepeerd in het zelfde afmetingspunt.<p>**dit kan u helpen** beter begrijpen de tijd van dag wanneer uw plaats het vaakst en minst vaak wordt bezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer gegevensverwerkingsmiddelen aan uw plaats tijdens hoog-verkeersuren toewijzen.</p><p>Deze sjabloon gebruikt de dimensie AM/PM.</p> |
| **Dag van week** | Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar dag van de week. Bijvoorbeeld, als u een rapport hebt dat de maand van Januari overspant, wordt elke dag van de week gegroepeerd in het zelfde afmetingspunt. <p>**dit kan u** helpen beter begrijpen welke dagen van de week uw plaats het vaakst en minst vaak wordt bezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersdagen.</p><p>Deze sjabloon gebruikt de dimensie Dag van de Week.</p> |
| **Dag van maand** | Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar dag van de maand. Bijvoorbeeld, als u een rapport hebt dat een volledig jaar overspant, wordt elke dag van de maand gegroepeerd in het zelfde afmetingspunt. <p>**dit kan u** helpen beter begrijpen welke dagen van elke maand uw plaats het vaakst en minst vaak wordt bezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersdagen.</p><p>Deze sjabloon gebruikt de dimensie Dag van Maand.</p> |
| **Dag van jaar** | Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar dag van het jaar. Bijvoorbeeld, als u een rapport hebt dat veelvoudige jaren overspant, wordt elke dag van het jaar gegroepeerd in het zelfde afmetingspunt. <p>**dit kan u** helpen beter begrijpen welke dagen van elk jaar uw plaats het vaakst en minst vaak wordt bezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersdagen.</p><p>Deze sjabloon gebruikt de dimensie Dag van Jaar.&lt;/> |
| **Weekdag/Weekend** | Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar weekdagen en weekends. Bijvoorbeeld, als u een rapport hebt dat de maand van Januari overspannen, worden de weekdagen en weekends gegroepeerd in afzonderlijke afmetingspunten. <p>**dit kan u helpen** beter de verschillen in plaatsverkeer voor weekdagen tegenover weekends begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum zwaarder op weekends, als het rapport erop wijst dat de weekends meer dan weekdagen zijn.</p><p>Deze sjabloon gebruikt de dimensie Weekdag/Weekend.</p> |
| **Week van jaar** | Bekijk gebeurtenissen, sessies en personen op uw site, uitgesplitst naar week van het jaar. Bijvoorbeeld, als u een rapport hebt dat veelvoudige jaren overspant, wordt elke week gegroepeerd in het zelfde afmetingspunt.<p>**dit kan u** helpen beter begrijpen welke weken van het jaar uw plaats het vaakst en minst vaak wordt bezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersweken, zoals tijdens de vakanties.</p><p>Deze sjabloon gebruikt de Week van Jaar dimensie.</p> |
| **Maand van jaar** | Gebeurtenissen, sessies en personen op uw site weergeven, uitgesplitst naar maand van het jaar. Bijvoorbeeld, als u een rapport hebt dat veelvoudige jaren overspant, wordt elke maand gegroepeerd in het zelfde afmetingspunt.<p>**dit kan u** helpen beter begrijpen welke maanden uw plaats het vaakst en het minst vaak wordt bezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als personeel uw vraagcentrum geschikter voor hoog-verkeersmaanden, zoals tijdens de vakanties.</p><p>In deze sjabloon wordt de maand van het jaar gebruikt.</p> |
| **Kwartaal van jaar** | Bekijk gebeurtenissen, sessies en personen op uw site, uitgesplitst naar kwart van het jaar. Bijvoorbeeld, als u een rapport hebt dat veelvoudige jaren overspant, wordt elk kwartaal gegroepeerd in het zelfde afmetingspunt.<p>**dit kan u** helpen beter begrijpen welke kwarten uw plaats het vaakst en het minst vaak wordt bezocht.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals tijd de lancering van producten om historisch laag-verkeerskwarten op te voeren.</p><p>Deze sjabloon gebruikt de dimensie Kwartaal van jaar.</p> |

### Kanaal overschrijden {#cross-channel}

<!--CJA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--multiChannelOverview"
>title="Bekijk de distributie van verkeer over veelvoudige kanalen."
>abstract="**dit kan u** helpen beter begrijpen welke kanalen met succes verkeer en overeenkomst drijven. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op de kanalen die het hoogste rendement op investering bereiken.<br/> Dit malplaatje gebruikt de gebruiker, de zitting, en gebeurtenismetriek."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--callCenterDeflection"
>title="Bekijk hoe het Webverkeer het verkeer van het vraagcentrum beïnvloedt."
>abstract="**dit kan u helpen** beter begrijpen hoe met succes de zelfbediening inhoud op uw website verkeer aan uw vraagcentrum afleidt.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als zelfbediening inhoud verbeteren om verkeer aan uw vraagcentrum te verminderen, of ROI van uw zelfbediening inhoud te meten door het bedrag te berekenen dat door minder steunvraag wordt bewaard.<br/> dit malplaatje gebruikt de Sessies van het Web, Mobiele Toepassingen, en Web+App de metriek van de Zittingen van het Kanaal."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--webAppTemplate"
>title="Bekijk het webverkeer en het mobiele verkeer samen."
>abstract="**dit kan u helpen** beter de distributie van Web en mobiel verkeer aan uw plaats begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer middelen aan uw mobiele toepassingservaring wijden wanneer het een bepaald niveau van verkeer bereikt.<br/> dit malplaatje gebruikt de Sessies van het Web, Mobiele Toepassingen, en Web+App de metriek van de Zittingen van het Kanaal."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--onlineOffline"
>title="Online en offline verkeer samen weergeven."
>abstract="**dit kan u helpen** beter de distributie van online en off-line verkeer aan uw plaats begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer middelen aan uw online ervaring wijden wanneer het een bepaald niveau van verkeer bereikt."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Multikanaal overzicht**] | Bekijk de distributie van verkeer over veelvoudige kanalen. <p>**dit kan u** helpen beter begrijpen welke kanalen met succes verkeer en overeenkomst drijven. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, zoals nadruk marketing inspanningen op de kanalen die het hoogste rendement op investering bereiken.</p><p>Deze sjabloon gebruikt de metriek van gebruiker, sessie en gebeurtenis.</p> |
| **Web+App** | Bekijk het webverkeer en het mobiele verkeer samen.<p>**dit kan u helpen** beter de distributie van Web en mobiel verkeer aan uw plaats begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer middelen aan uw mobiele toepassingservaring wijden wanneer het een bepaald niveau van verkeer bereikt.</p><p>Deze sjabloon gebruikt de metriek Websessies, Mobiele App-sessies en Web+App voor verschillende sessies.</p> |
| **Online/Off-line** | Online en offline verkeer samen weergeven.<p>**dit kan u helpen** beter de distributie van online en off-line verkeer aan uw plaats begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer middelen aan uw online ervaring wijden wanneer het een bepaald niveau van verkeer bereikt.</p><!-- This template uses the ... --> |
| **de centrumvervorming van de Vraag** | Bekijk hoe het Webverkeer het verkeer van het vraagcentrum beïnvloedt.<p>**dit kan u helpen** beter begrijpen hoe met succes de zelfbediening inhoud op uw website verkeer aan uw vraagcentrum afleidt.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als zelfbediening inhoud verbeteren om verkeer aan uw vraagcentrum te verminderen, of ROI van uw zelfbediening inhoud te meten door het bedrag te berekenen dat door minder steunvraag wordt bewaard.</p><p>Deze sjabloon gebruikt de metriek Websessies, Mobiele App-sessies en Web+App voor verschillende sessies.</p> |

### Andere kanalen {#other-channels}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--callcenterdashboard"
>title="De gegevens van het vraagcentrum van de mening, met inbegrip van waarom de klanten en het aantal tijden riepen."
>abstract="**dit kan u helpen** beter begrijpen waar de klanten problemen ervaren en waar de middelen van het vraagcentrum worden besteed.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen, zoals de kwesties van het adresproduct kunnen doen die het hogere verkeer van het vraagcentrum drijven, uiteindelijk verbeterend productrentabiliteit."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--pointOfSale"
>title="Transactiegegevens van verkooppunten weergeven, inclusief verdiende inkomsten, uitgevoerde orders en verkochte eenheden. Deze sjabloon bevat ook visualisaties die informatie weergeven over winkels, producten van topniveau en de belangrijkste productcategorieën, en ook online versus offline verkoop."
>abstract="**dit kan u** helpen beter begrijpen welke uw top-verkopende producten over opslagplaats en online zijn.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer marketing middelen aan uw best-presterende producten en kanalen toewijzen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--ajo-email"
>title="Bekijk hoe de e-mails die u ontwerpt en verzendt met Adobe Journey Optimizer, nieuwe lidmaatschappen, loyaliteitsleden en mogelijkheden voor kruisverkoop genereren."
>abstract="**dit kan u helpen** beter de doeltreffendheid van e-mails begrijpen die u ontwerpt en verzendt gebruikend Adobe Journey Optimizer.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw e-mailstrategie voor een bepaalde e-mailcampagne aanpassen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--survey"
>title="Bekijk de betrokkenheid van gebruikers voor uw enquêtes. Bekijk het aantal start- en voltooiingsopdrachten, de bovenste vragen en antwoorden en het aantal eerste versus vorige deelnemers."
>abstract="**dit kan u** helpen de betrokkenheidsniveaus en het succestarief van uw onderzoeken beter begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als toekomstige onderzoeken aanpassen om betere participatie te produceren."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **het centrum dashboard van de Vraag**] | De gegevens van het vraagcentrum van de mening, met inbegrip van waarom de klanten en het aantal tijden riepen. <p>**dit kan u helpen** beter begrijpen waar de klanten problemen ervaren en waar de middelen van het vraagcentrum worden besteed.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen, zoals de kwesties van het adresproduct kunnen doen die het hogere verkeer van het vraagcentrum drijven, uiteindelijk verbeterend productrentabiliteit.</p> |
| **Punt van verkoop** | Transactiegegevens van verkooppunten weergeven, inclusief verdiende inkomsten, uitgevoerde orders en verkochte eenheden. Deze sjabloon bevat ook visualisaties die informatie weergeven over winkels, producten van topniveau en de belangrijkste productcategorieën, en ook online versus offline verkoop. <p>**dit kan u** helpen beter begrijpen welke uw top-verkopende producten over opslagplaats en online zijn.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als meer marketing middelen aan uw best-presterende producten en kanalen toewijzen.</p><p>In deze sjabloon worden de metriek Gebruikers, Opbrengsten en Bestellingen gebruikt.</p> |
| **Journey Optimizer e-mailanalyse** | Bekijk hoe de e-mails die u ontwerpt en verzendt met Adobe Journey Optimizer, nieuwe lidmaatschappen, loyaliteitsleden en mogelijkheden voor kruisverkoop genereren. <p>**dit kan u helpen** beter de doeltreffendheid van e-mails begrijpen die u ontwerpt en verzendt gebruikend Adobe Journey Optimizer.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw e-mailstrategie voor een bepaalde e-mailcampagne aanpassen.</p> |
| **Onderzoek** | Bekijk de betrokkenheid van gebruikers voor uw enquêtes. Bekijk het aantal start- en voltooiingsopdrachten, de bovenste vragen en antwoorden en het aantal eerste versus vorige deelnemers.<p>**dit kan u** helpen de betrokkenheidsniveaus en het succestarief van uw onderzoeken beter begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als toekomstige onderzoeken aanpassen om betere participatie te produceren.</p><p>In deze sjabloon worden de volgende cijfers gebruikt: Gebruikers, Gebeurtenissen, Begin van enquête, Voltooien van enquête en Eindpercentage van enquête.</p> |

### Journey Optimizer {#AJO-templates}

<!--CJA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--ajo-campaign"
>title="Bekijk essentiële gegevens voor uw Journey Optimizer-campagnes, zoals e-mailcampagnes, experimenten, in-app, SMS en meer."
>abstract="**dit kan u helpen** beter details zoals het aantal kliks en het aantal geleverde berichten begrijpen, die een uitvoerig inzicht in de doeltreffendheid van uw campagne en niveau van overeenkomst aanbieden.<br/>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw campagnes aanpassen die op de betrokkenheidsniveaus van uw doelpubliek worden gebaseerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--ajo-journey"
>title="Bekijk essentiële gegevens voor uw Journey Optimizer-reizen, zoals e-mailreizen, experimenten, in-app, SMS en meer."
>abstract="**dit kan u helpen** beter details zoals het aantal kliks en aantal geleverde berichten begrijpen, die een uitvoerig inzicht in de doeltreffendheid van uw reis en niveau van overeenkomst aanbieden.<br/>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw campagnes aanpassen die op de betrokkenheidsniveaus van uw doelpubliek worden gebaseerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--ajo-landing-page"
>title="Bekijk gebruikersgedrag, betrokkenheidspatronen, conversietarieven en andere belangrijke meetgegevens."
>abstract="**dit kan u helpen** beter de doeltreffendheid van uw het landen pagina begrijpen. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer uw het landen paginaprestaties."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--ajo-channel"
>title="Bekijk een uitgebreide samenvatting van verkeers- en betrokkenheidsgegevens voor alle campagnes en reizen binnen uw omgeving."
>abstract="**dit kan u helpen** beter de doeltreffendheid op hoog niveau van uw campagnes en reizen begrijpen. <br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw campagnes en reizen aanpassen die op de betrokkenheidsniveaus van uw doelpubliek worden gebaseerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--ajo-subscription"
>title="Abonnementen en abonnementen van profielen voor bepaalde lijsten weergeven."
>abstract="**dit kan u** helpen beter de doeltreffendheid van verschillende abonnementscampagnes en initiatieven in het drijven overeenkomst en omzettingen begrijpen.<br/>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw abonnementscampagnes aanpassen die op de betrokkenheidsniveaus van uw doelpubliek worden gebaseerd."

<!-- markdownlint-enable MD034 -->

De volgende sjablonen zijn beschikbaar:

| Sjabloonnaam | Waarom deze sjabloon gebruiken <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **campagnes van Journey Optimizer**] | Bekijk essentiële gegevens voor uw Journey Optimizer-campagnes, zoals e-mailcampagnes, experimenten, in-app, SMS en meer.<p>**dit kan u helpen** beter details zoals het aantal kliks en het aantal geleverde berichten begrijpen, die een uitvoerig inzicht in de doeltreffendheid van uw campagne en niveau van overeenkomst aanbieden.</p><p>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw campagnes aanpassen die op de betrokkenheidsniveaus van uw doelpubliek worden gebaseerd.</p> |
| **reizen van Journey Optimizer** | Bekijk essentiële gegevens voor uw Journey Optimizer-reizen, zoals e-mailreizen, experimenten, in-app, SMS en meer.<p>**dit kan u helpen** beter details zoals het aantal kliks en aantal geleverde berichten begrijpen, die een uitvoerig inzicht in de doeltreffendheid van uw reis en niveau van overeenkomst aanbieden.</p><p>**gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw campagnes aanpassen die op de betrokkenheidsniveaus van uw doelpubliek worden gebaseerd.</p> |
| **Journey Optimizer landende pagina&#39;s** | Bekijk gebruikersgedrag, betrokkenheidspatronen, conversietarieven en andere belangrijke meetgegevens.<p>**dit kan u helpen** beter de doeltreffendheid van uw het landen pagina begrijpen. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als optimaliseer uw het landen paginaprestaties.</p> |
| **het overzichtsrapport van Journey Optimizer** | Bekijk een uitgebreide samenvatting van verkeers- en betrokkenheidsgegevens voor alle campagnes en reizen binnen uw omgeving.<p>**dit kan u helpen** beter de doeltreffendheid op hoog niveau van uw campagnes en reizen begrijpen. </p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw campagnes en reizen aanpassen die op de betrokkenheidsniveaus van uw doelpubliek worden gebaseerd.</p> |
| **Journey Optimizer abonnementen** | Abonnementen en abonnementen van profielen voor bepaalde lijsten weergeven.<p>**dit kan u** helpen beter de doeltreffendheid van verschillende abonnementscampagnes en initiatieven in het drijven overeenkomst en omzettingen begrijpen.</p><p>**Gebaseerd op wat u leert, zou u** om het even welk aantal dingen kunnen doen, als uw abonnementscampagnes aanpassen die op de betrokkenheidsniveaus van uw doelpubliek worden gebaseerd.</p> |

