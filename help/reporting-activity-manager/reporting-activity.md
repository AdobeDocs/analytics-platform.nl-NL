---
title: Rapportactiviteiten weergeven in de manager van de activiteit Rapportering
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
solution: Customer Journey Analytics
feature: Basics
exl-id: 1f5b2a42-162e-45a7-9fd4-8c1557f48bb8
role: Admin
source-git-commit: 31381cd397a821cc3ff1b3c15ae968a7260a6e9e
workflow-type: tm+mt
source-wordcount: '1989'
ht-degree: 0%

---

# Rapportactiviteiten weergeven {#view-reporting-activity}

Met [!UICONTROL Reporting Activity Manager] kunnen beheerders snel problemen met de rapportcapaciteit tijdens piekrapportagetijden opsporen en verhelpen.

Voor meer informatie over het Melden van de Manager van de Activiteit, met inbegrip van zeer belangrijke voordelen en toestemmingsvereisten, zie [ het Overzicht van de Manager van de Activiteit ](/help/reporting-activity-manager/reporting-activity-overview.md) melden.

## Voor alle verbindingen {#view-all-report-suites}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_tools_reportingactivitymanager_connections"
>title="Verbindingen"
>abstract="In deze tabel worden de verbindingen weergegeven waarvoor u rechten hebt om rapportactiviteiten te beheren. In elke kolom van de tabel is informatie beschikbaar over elke verbinding."

<!-- markdownlint-enable MD034 -->


1. Ga in Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]** .

   Er wordt een lijst met uw ingeschakelde basisverbindingen weergegeven.

   ![ het Melden van Activiteit die de rapportrij ](assets/reporting-activity1.png) toont

1. Om het totale aantal rapportverzoeken voor alle verbindingen in uw organisatie te bekijken, breid [!UICONTROL **uit tonen meer**] om de [!UICONTROL **Maandelijkse verzoeken van het rapport**] grafiek te bekijken.

   U kunt het aantal rapportverzoeken binnen uw organisatie voor de huidige maand en de vorige maand bekijken.

   ![ het Melden van Activiteit die de rapportrij ](assets/reporting-activity-monthly.png) toont

1. (Optioneel) U kunt de lijst met verbindingen opzoeken of filteren:

   * Gebruik het zoekveld om te zoeken naar een specifieke verbinding. Typ de naam of de id van de verbinding en de lijst met updates van verbindingen terwijl u typt.

   * Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om de lijst van filteropties uit te breiden. U kunt door [!UICONTROL **Favorieten**] of [!UICONTROL **Status**] filtreren.

     Als u een verbinding als favoriet wilt markeren, selecteert u het sterpictogram links van de naam van de verbinding.

     <!-- (does this option still exist?) 1. (Optional) Select **[!UICONTROL Refresh]** at the top-right to refresh the data. -->

1. Gebruik informatie over elke verbinding weergeven. De gegevens die in de tabel worden weergegeven, vertegenwoordigen de rapportactiviteit voor de verbinding op het moment dat de pagina voor het laatst werd geladen.

   De volgende kolommen zijn beschikbaar:

   | UI-element | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Connection]** | De verbinding waarvan het melden activiteit u controleert. |
   | **[!UICONTROL Data Views]** | Toont alle gegevensmeningen die de verbinding gebruiken. De configuratie van de mening van gegevens kan ingewikkeldheid aan het melden van verzoeken toevoegen. |
   | **[!UICONTROL Capacity utilization]** | Het percentage van de rapporteringscapaciteit van de verbinding die, in real time wordt gebruikt. <p>**Nota** de gebruikscapaciteit van A die bij 100% is stelt niet noodzakelijk voor dat u onmiddellijk zou moeten beginnen meldend verzoeken te annuleren. De gebruikscapaciteit van 100% kan gezond zijn als de gemiddelde wachttijd redelijk is. Anderzijds zou 100% van de gebruikscapaciteit een probleem kunnen suggereren als het aantal verzoeken in de wachtrij ook toeneemt.</p> |
   | **[!UICONTROL Queued requests]** | Het aantal verzoeken dat moet worden verwerkt. <!-- ??? --> |
   | **[!UICONTROL Queue wait time]** | De gemiddelde wachttijd alvorens de verzoeken beginnen te verwerken. <!-- ???? --> |
   | **[!UICONTROL Status]** | De mogelijke statussen zijn: <ul><li>[!UICONTROL **Actief**] (blauw): De rapporten zijn in werking gesteld op de verbinding in de laatste 2 uren. De gegevens in de tabel geven de rapportcapaciteit aan voor de verbinding op het moment dat de pagina voor het laatst werd geladen.</li><li>[!UICONTROL **Inactief**] (grijs): Geen rapporten zijn ooit in werking gesteld op de verbinding in de laatste 2 uren, zodat worden geen gegevens getoond voor de verbinding.</li></ul> |

   {style="table-layout:auto"}

## Voor één verbinding

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Hulpmiddelen**] > [!UICONTROL **die de Manager van de Activiteit**] melden.

1. Selecteer de gekoppelde titel van de verbinding waarvoor u details wilt weergeven.

   Gegevens over de rapportactiviteit worden weergegeven voor de verbinding die u hebt geselecteerd.

1. (Optioneel) Wanneer een verbinding voor het eerst wordt geladen in Rapportagentenbeheer, vertegenwoordigen de weergegeven gegevens de huidige gebruiksmaatstaven. Om bijgewerkte metriek na de aanvankelijke lading te zien, selecteer [!UICONTROL **verfrissen**] knoop om de pagina manueel te verfrissen.

   <!-- Need to update this screenshot: ![connection](assets/indiv-report-ste.png) -->

1. Gebruik de beschikbare grafieken en de lijst om rapportactiviteit in de verbinding te begrijpen.

   * [Grafieken weergeven](#view-graphs)

   * [Tabel weergeven](#view-table)

### Grafieken weergeven

De volgende grafieken zijn beschikbaar om u te helpen de activiteit begrijpen die in de verbinding gebeurt.

Als de grafieken niet zichtbaar zijn, selecteer [!UICONTROL **tonen grafieken**] knoop.

#### Gebruiksgrafiek {#utilization}

De grafiek van het Gebruik toont rapporterend gebruik voor de geselecteerde verbinding in de laatste 2 uren.

Houd de cursor boven het diagram om punten in de tijd te bekijken waar het percentage van de gebruikscapaciteit het hoogst was gedurende die minuut.

* **x-as**: De rapporteringsgebruikscapaciteit over de laatste 2 uren.
* **y-as**: Het percentage van het rapportgebruikscapaciteit, door minuut.

  ![ gebruiks grafiek ](assets/utilization-graph.png)

#### Afzonderlijke gebruikersgrafiek

In de grafiek Afzonderlijke gebruikers wordt de rapportactiviteit voor de geselecteerde verbinding gedurende de laatste twee uur weergegeven.

Houd de cursor boven het diagram om punten in de tijd te bekijken waar het maximumaantal gebruikers het hoogst was gedurende die minuut.

* **x-as**: De rapporteringsactiviteit over het laatste 2 uur tijdkader.
* **y-as**: Het aantal gebruikers die rapportageverzoeken, door minuut hebben gemaakt.

  ![ de Afzonderlijke grafiek van Gebruikers ](assets/distinct-users-graph.png)

#### Verzoeken om grafiek

De grafiek Verzoeken toont het aantal verwerkte en een rij gevormde verzoeken voor de geselecteerde verbinding over de laatste 2 uren.

Beweeg over de grafiek om punten in tijd te bekijken waar het maximumaantal verzoeken voor die minuut het hoogst was.

* **x-as**: Het aantal verwerkte en een rij gevormde verzoeken over het laatste 2 uur tijdkader.
* **y-as**: Het aantal verwerkte verzoeken (in groen) en een rij gevormde verzoeken (in paars), door minuut.

  ![ de Afzonderlijke grafiek van Gebruikers ](assets/requests-graph.png)

#### Grafiek in wachtrij

De rij die grafiek toont de gemiddelde rij wacht tijd (in seconden) voor het melden van verzoeken om de geselecteerde verbinding over de laatste 2 uren.

Beweeg over de grafiek om punten in tijd te bekijken waar de maximumgemiddelde wachttijd hoogste voor die minuut was.

* **x-as**: De gemiddelde rij wacht tijd voor het melden van verzoeken over het laatste een tijdkader van 2 uur.
* **y-as**: De gemiddelde wachttijd (in seconden).

  ![ Afzonderlijke grafiek van Gebruikers ](assets/queueing-graph.png)

### Tabel weergeven {#view-table}

Houd rekening met het volgende wanneer u de tabel weergeeft:

* U kunt verkiezen om gegevens te bekijken door om het even welke volgende lusjes bij de bovenkant van de gegevenslijst te kiezen: [!UICONTROL **Verzoek**], [!UICONTROL **Gebruiker**], [!UICONTROL **Project**], of [!UICONTROL **Toepassing**].

* U kunt de lijst met verbindingen zoeken of filteren:

   * Gebruik het zoekveld om te zoeken naar een specifieke verbinding. Typ de naam of de id van de verbinding en de lijst met updates van verbindingen terwijl u typt.

   * Selecteer het [!UICONTROL **pictogram van de Filter**] pictogram ![ van de Filter ](assets/filter-icon.png) om de lijst van filteropties uit te breiden. U kunt door [!UICONTROL **Status**] filtreren, [!UICONTROL **Complexiteit**], [!UICONTROL **Toepassing**], [!UICONTROL **Gebruiker**], of [!UICONTROL **Project**].

   * U kunt [!UICONTROL **grafieken van de Verbergen**] selecteren om slechts de lijst te tonen.

![ lijstlusjes ](assets/report-activity-tabs.png)

#### Gegevens op verzoek weergeven

Wanneer u het [!UICONTROL **Verzoek**] lusje selecteert, zijn de volgende kolommen beschikbaar in de lijst:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **identiteitskaart van het Verzoek**] | Een unieke id die kan worden gebruikt voor probleemoplossingsdoeleinden. Om identiteitskaart te kopiëren, selecteer het verzoek, dan de optie, [!UICONTROL **verzoek IDs van het Exemplaar**]. |
| [!UICONTROL **looppas van de Tijd**] | Hoe lang de aanvraag is uitgevoerd. |
| [!UICONTROL **tijd van het Begin**] | Wanneer de aanvraag is begonnen met de verwerking (op basis van de lokale tijd van de beheerder). |
| [!UICONTROL **wacht tijd**] | Hoe lang het verzoek heeft gewacht alvorens wordt verwerkt. Deze waarde staat doorgaans op &quot;0&quot; wanneer er voldoende capaciteit is. |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Workspace-projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende metriek, Annotaties, Soorten publiek enzovoort.</li><li>API-aanroepen vanuit de 2.0-API</li><li>Waarschuwingen<li>Volledige tabelexport</li><li>Delen met koppelingen van anderen</li><li>Analyse met instructies</li><li>Een andere toepassing die de Analyse meldend motor vraagt</li></li></ul><p>**Nota:** als de waarde van deze kolom [!UICONTROL **Onbekend**] is, betekent dit dat de verzoekmeta-gegevens niet beschikbaar voor de gebruiker zijn.</p> |
| [!UICONTROL **Gebruiker**] | De gebruiker die de aanvraag heeft gestart. <p>**Nota:** als de waarde van deze kolom [!UICONTROL **Onbekend**] is, betekent dit dat de verzoekmeta-gegevens niet beschikbaar voor de gebruiker zijn.</p> |
| [!UICONTROL **Project**] | Opgeslagen Workspace-projectnamen, API-rapport-id&#39;s enzovoort. (Metagegevens kunnen per toepassing verschillen.)<p>**Nota:** als de waarde van deze kolom [!UICONTROL **Onbekend**] is, betekent dit dat het project niet is bewaard of dat de verzoekmeta-gegevens niet beschikbaar voor de gebruiker is.</p> |
| [!UICONTROL **Status**] | Statusindicatoren: <ul><li>**Lopend**: Het verzoek wordt momenteel verwerkt.</li><li>**Hangende**: Het verzoek wacht om te worden verwerkt.</li></ul> |
| [!UICONTROL **Complexiteit**] | Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken. <p>Mogelijke waarden zijn:</p> <ul><li>[!UICONTROL **Laag**]</li><li>[!UICONTROL **Normaal**]</li><li>[!UICONTROL **Hoog**]</li></ul>Deze waarde wordt beïnvloed door de waarden in de volgende kolommen:<ul><li>[!UICONTROL **grenzen van de Maand**]</li><li>[!UICONTROL **Kolommen**]</li><li>[!UICONTROL **Segmenten**]</li></ul> |
| [!UICONTROL **Maandgrenzen**] | Het aantal maanden dat in een verzoek is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Kolommen**] | Het aantal metrics en uitsplitsingen in de aanvraag. Meer kolommen vergroten de complexiteit van de aanvraag. |
| [!UICONTROL **Segmenten**] | Het aantal segmenten dat op de aanvraag wordt toegepast. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

#### Gegevens weergeven per gebruiker

Wanneer u het [!UICONTROL **lusje van de Gebruiker**] selecteert, zijn de volgende kolommen beschikbaar in de lijst:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Gebruiker**] | De gebruiker die de aanvraag heeft gestart. Als de waarde van deze kolom [!UICONTROL **Onerkend**] is, betekent dit dat de gebruiker in een login bedrijf is waar u geen administratieve toestemmingen hebt. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal aanvragen dat door de gebruiker wordt geïnitieerd. |
| [!UICONTROL **Aantal projecten**] | Het aantal projecten verbonden aan de gebruiker. <!-- ??? --> |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Workspace-projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende metriek, Annotaties, Soorten publiek enzovoort.</li><li>API-aanroepen vanuit de 2.0-API</li><li>Waarschuwingen<li>Volledige tabelexport</li><li>Delen met koppelingen van anderen</li><li>Analyse met instructies</li><li>Een andere toepassing die de Analyse meldend motor vraagt</li></li></ul> |
| [!UICONTROL **Avg Complexiteit**] | De gemiddelde ingewikkeldheid van verzoeken die door de gebruiker in werking worden gesteld. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p><ul><li>[!UICONTROL **Gem de grenzen van de Maand**]</li><li>[!UICONTROL **Avg Kolommen**]</li><li>[!UICONTROL **Avg Segmenten**]</li></ul> |
| [!UICONTROL **Gem de grenzen van de Maand**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Avg Kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Avg Segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

#### Gegevens weergeven per project

Wanneer u het [!UICONTROL **lusje van het Project**] selecteert, zijn de volgende kolommen beschikbaar in de lijst:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Project**] | Het project waar de verzoeken werden ingediend. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal verzoeken verbonden aan het project. |
| [!UICONTROL **Aantal gebruikers**] | Het aantal gebruikers dat aan het project is gekoppeld. <!-- ??? --> |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Workspace-projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende metriek, Annotaties, Soorten publiek enzovoort.</li><li>API-aanroepen vanuit de 2.0-API</li><li>Waarschuwingen<li>Volledige tabelexport</li><li>Delen met koppelingen voor iedereen</li><li>Analyse met instructies</li><li>Een andere toepassing die de Analyse meldend motor vraagt</li></li></ul> |
| [!UICONTROL **Avg Complexiteit**] | De gemiddelde complexiteit van aanvragen die in het project zijn opgenomen. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p><ul><li>[!UICONTROL **Gem de grenzen van de Maand**]</li><li>[!UICONTROL **Avg Kolommen**]</li><li>[!UICONTROL **Avg Segmenten**]</li></ul> |
| [!UICONTROL **Gem de grenzen van de Maand**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Avg Kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Avg Segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

#### Gegevens weergeven per toepassing

Wanneer u het [!UICONTROL **lusje van de Toepassing**] selecteert, zijn de volgende kolommen beschikbaar in de lijst:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Toepassing**] | De aanvraag waar de verzoeken zijn ingediend. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal aanvragen dat aan de toepassing is gekoppeld. |
| [!UICONTROL **Aantal gebruikers**] | Het aantal gebruikers dat aan de toepassing is gekoppeld. <!--???--> |
| [!UICONTROL **Aantal projecten**] | Het aantal projecten verbonden aan de toepassing. <!--???--> |
| [!UICONTROL **Avg Complexiteit**] | De gemiddelde ingewikkeldheid van verzoeken verbonden aan de toepassing. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:<ul><li>[!UICONTROL **Gem Maandgrenzen**]</li><li>[!UICONTROL **Avg Kolommen**]</li><li>[!UICONTROL **Avg Segmenten**]</li></ul> |
| [!UICONTROL **Gem de grenzen van de Maand**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Avg Kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Avg Segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

<!-- 

## Frequently asked questions {#faq}

| Question | Answer |
| --- | --- |
| | |

{style="table-layout:auto"}

-->
