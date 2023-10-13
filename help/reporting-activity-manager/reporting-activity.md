---
title: Rapportactiviteiten weergeven in de rapportagManager
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
solution: Customer Journey Analytics
feature: Basics
source-git-commit: dba42bedd14c4c6d958feab9a1ebdc137d489f32
workflow-type: tm+mt
source-wordcount: '1728'
ht-degree: 1%

---

# Rapportactiviteiten weergeven in de rapportagManager

{{release-limited-testing}}

De [!UICONTROL Reporting Activity Manager] stelt beheerders in staat om problemen met de rapportcapaciteit tijdens piekrapportagetijden snel te diagnosticeren en op te lossen.

Voor meer informatie over het Melden van de Manager van de Activiteit, met inbegrip van zeer belangrijke voordelen en toestemmingsvereisten, zie [Overzicht van Activity Manager rapporteren](/help/reporting-activity-manager/reporting-activity-overview.md).

## Rapportactiviteiten voor alle verbindingen weergeven {#view-all-report-suites}

1. Ga in de Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]**.

   Er wordt een lijst met uw ingeschakelde basisverbindingen weergegeven.

   ![rapportwachtrij](assets/reporting-activity1.png)

1. (Optioneel) U kunt de lijst met verbindingen opzoeken of filteren:

   * Gebruik het zoekveld om te zoeken naar een specifieke verbinding. Typ de naam of de id van de verbinding en de lijst met updates van verbindingen terwijl u typt.

   * Selecteer de [!UICONTROL **Filter**] pictogram ![Filterpictogram](assets/filter-icon.png) om de lijst met filteropties uit te vouwen. U kunt filteren op [!UICONTROL **Favorieten**] of [!UICONTROL **Status**].

     Als u een verbinding als favoriet wilt markeren, selecteert u het sterpictogram links van de naam van de verbinding.

     <!-- (does this option still exist?) 1. (Optional) Select **[!UICONTROL Refresh]** at the top-right to refresh the data. -->

1. Gebruik informatie over elke verbinding weergeven. U kunt een kolomkop selecteren om de tabel op die kolom te sorteren.

   De volgende kolommen zijn beschikbaar:

   | UI-element | Beschrijving |
   | --- | --- |
   | **[!UICONTROL connection]** | De verbinding waarvan het melden activiteit u controleert. |
   | **[!UICONTROL Virtual report suites]** | Toont alle virtuele rapportsuites die in deze reeks van het basisrapport van toepassing zijn. De virtuele rapportsuites voegen ingewikkeldheid aan rapporteringsverzoeken toe toe toe te schrijven aan extra niveaus van toegepaste filtratie en segmentatie. Alle verzoeken die uit de virtuele rapportreeksen komen worden gecombineerd in de reeks van het basisrapport.<p>Bijvoorbeeld, als u 10 verzoeken hebt die uit 5 virtuele rapportreeksen komen, is dat 50 verzoeken bij de het rapportreeks van het basisniveau. Op deze manier kun je snel de capaciteit raken. |
   | **[!UICONTROL Capacity utilization]** | Het percentage van de rapporteringscapaciteit van de rapportreeks die, in echt - tijd wordt gebruikt. <p>**Opmerking** Een gebruikscapaciteit die 100% is, suggereert niet noodzakelijk dat u onmiddellijk begint rapporteringsverzoeken te annuleren. De gebruikscapaciteit van 100% kan gezond zijn als de gemiddelde wachttijd redelijk is. Anderzijds zou 100% van de gebruikscapaciteit een probleem kunnen suggereren als het aantal verzoeken in de wachtrij ook toeneemt.</p> |
   | **[!UICONTROL Queued requests]** | Het aantal verzoeken dat moet worden verwerkt. <!-- ??? --> |
   | **[!UICONTROL Queue wait time]** | De gemiddelde wachttijd alvorens de verzoeken beginnen te verwerken. <!-- ???? --> |
   | **[!UICONTROL Status]** | De mogelijke statussen zijn: <ul><li>[!UICONTROL **Actief**] (blauw): de rapporten zijn in werking gesteld op de rapportreeks en het wordt gecontroleerd op activiteit.</li><li>[!UICONTROL **Inactief**] (grijs): er zijn nooit rapporten uitgevoerd over de rapportsuite. Deze status wordt alleen weergegeven wanneer de rapportsuites voor het eerst worden gemaakt.</li></ul> |

   {style="table-layout:auto"}

## Rapportactiviteiten weergeven voor één rapportsuite

1. Selecteer in Customer Journey Analytics [!UICONTROL **Gereedschappen**] > [!UICONTROL **Activity Manager rapporteren**].

1. Selecteer de gekoppelde titel van de rapportsuite waarvan u de details wilt weergeven.

   De gegevens van de rapportactiviteit worden getoond voor de rapportreeks die u selecteerde.

   <!-- Need to update this screenshot: ![report suite](assets/indiv-report-ste.png) -->

1. Gebruik de beschikbare grafieken en de lijst om rapporteringsactiviteit in de rapportreeks te begrijpen.

   * [Grafieken weergeven](#view-graphs)

   * [Tabel weergeven](#view-table)

### Grafieken weergeven

De volgende grafieken zijn beschikbaar om u te helpen de activiteit begrijpen die in de rapportreeks gebeurt.

Als grafieken niet zichtbaar zijn, selecteert u de optie [!UICONTROL **Grafieken tonen**] knop.

#### Gebruiksgrafiek {#utilization}

De grafiek van het Gebruik toont rapporteringsgebruik voor de geselecteerde rapportreeks over de laatste 2 uren.

Houd de cursor boven het diagram om punten in de tijd te bekijken waar het percentage van de gebruikscapaciteit het hoogst was gedurende die minuut.

* **X-as**: De capaciteit van het rapportagegebruik gedurende de laatste twee uur.
* **Y-as**: Het percentage van de rapportgebruikscapaciteit, door minuut.

  ![gebruikslijn](assets/utilization-graph.png)

#### Afzonderlijke gebruikersgrafiek

In de grafiek Afzonderlijke gebruikers wordt de rapportactiviteit voor de geselecteerde rapportsuite gedurende de laatste twee uur weergegeven.

Houd de cursor boven het diagram om punten in de tijd te bekijken waar het maximumaantal gebruikers het hoogst was gedurende die minuut.

* **X-as**: De rapportageactiviteit gedurende het laatste tijdkader van 2 uur.
* **Y-as**: Het aantal gebruikers dat rapportageverzoeken per minuut heeft ingediend.

  ![Afzonderlijke gebruikersgrafiek](assets/distinct-users-graph.png)

#### Verzoeken om grafiek

De grafiek van Verzoeken toont het aantal verwerkte en voltooide verzoeken voor de geselecteerde rapportreeks over de laatste twee uren.

Houd de cursor boven het diagram om punten in de tijd weer te geven waar het maximale aantal aanvragen het hoogst was voor die minuut.

* **X-as**: Het aantal verwerkte en voltooide verzoeken over het laatste 2 uurtijdkader.
* **Y-as**: Het aantal verwerkte aanvragen (in paars) en ingevulde aanvragen (in groen), per minuut.

  ![Afzonderlijke gebruikersgrafiek](assets/requests-graph.png)

#### Grafiek in wachtrij

De het Een rij vormen grafiek toont de gemiddelde rij wachttijd (in seconden) voor het melden van verzoeken voor de geselecteerde rapportreeks over de laatste 2 uren.

Houd de cursor boven het diagram om punten in de tijd te bekijken waar de maximale gemiddelde wachttijd het hoogst was voor die minuut.

* **X-as**: De gemiddelde rij wacht tijd op het melden van verzoeken over het laatste 2 uurtijdkader.
* **Y-as**: De gemiddelde wachttijd (in seconden).

  ![Afzonderlijke gebruikersgrafiek](assets/queueing-graph.png)

### Tabel weergeven {#view-table}

U kunt ervoor kiezen om gegevens weer te geven door een van de volgende tabbladen boven aan de gegevenstabel te kiezen: [!UICONTROL **Verzoek**], [!UICONTROL **Gebruiker**], [!UICONTROL **Project**], of [!UICONTROL **Toepassing**].

>[!TIP]
>
>U kunt [!UICONTROL **Grafieken verbergen**] alleen de tabel weergeven.

![tabbladen](assets/indiv-report-ste-table-tabs.png)

#### Gegevens op verzoek weergeven

Wanneer u [!UICONTROL **Verzoek**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Aanvraag-id**] | Kan voor het oplossen van problemendoeleinden worden gebruikt. |
| [!UICONTROL **Tijdsduur**] | Hoe lang de aanvraag is uitgevoerd. |
| [!UICONTROL **Begintijd**] | Wanneer de aanvraag is begonnen met de verwerking (op basis van de lokale tijd van de beheerder). |
| [!UICONTROL **Wacht op tijd**] | Hoe lang het verzoek heeft gewacht alvorens wordt verwerkt. Deze waarde staat doorgaans op &quot;0&quot; wanneer er voldoende capaciteit is. |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende afmetingen, Annotaties, Soorten publiek, enzovoort.</li><li>API-aanroepen van 1.4 of 2.0 API</li><li>Intelligente waarschuwingen</li></ul> |
| [!UICONTROL **Gebruiker**] | De gebruiker die de aanvraag heeft gestart. <p>**Opmerking:** Als de waarde van deze kolom [!UICONTROL **Niet herkend**], betekent dit dat de gebruiker zich in een login bedrijf bevindt waar u geen administratieve toestemmingen hebt.</p> |
| [!UICONTROL **Project**] | Opgeslagen projectnamen voor Workspace, API-rapport-id&#39;s, enz. (Metagegevens kunnen per toepassing verschillen.) |
| [!UICONTROL **Status**] | Statusindicatoren: <ul><li>**Wordt uitgevoerd**: Verzoek wordt momenteel verwerkt.</li><li>**In behandeling**: De aanvraag is in afwachting van verwerking.</li></ul> |
| [!UICONTROL **Complexiteit**] | Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken. <p>Mogelijke waarden zijn:</p> <ul><li>[!UICONTROL **Laag**]</li><li>[!UICONTROL **Normaal**]</li><li>[!UICONTROL **Hoog**]</li></ul>Deze waarde wordt beïnvloed door de waarden in de volgende kolommen:<ul><li>[!UICONTROL **Maandgrenzen**]</li><li>[!UICONTROL **Kolommen**]</li><li>[!UICONTROL **Segmenten**]</li></ul> |
| [!UICONTROL **Maandgrenzen**] | Het aantal maanden dat in een verzoek is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Kolommen**] | Het aantal metriek en onderverdelingen in het verzoek. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Segmenten**] | Het aantal segmenten dat op de aanvraag wordt toegepast. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

#### Gegevens weergeven per gebruiker

Wanneer u [!UICONTROL **Gebruiker**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Gebruiker**] | De gebruiker die de aanvraag heeft gestart. Als de waarde van deze kolom [!UICONTROL **Niet herkend**], betekent dit dat de gebruiker zich in een login bedrijf bevindt waar u geen administratieve toestemmingen hebt. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal aanvragen dat door de gebruiker wordt geïnitieerd. |
| [!UICONTROL **Aantal projecten**] | Het aantal projecten verbonden aan de gebruiker. <!-- ??? --> |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende afmetingen, Annotaties, Soorten publiek, enzovoort.</li><li>API-aanroepen van 1.4 of 2.0 API</li><li>Intelligente waarschuwingen</li></ul> |
| [!UICONTROL **Gemiddelde complexiteit**] | De gemiddelde ingewikkeldheid van verzoeken die door de gebruiker in werking worden gesteld. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p><ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

#### Gegevens weergeven per project

Wanneer u [!UICONTROL **Project**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Project**] | Het project waar de vragen werden geïnitieerd. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal verzoeken verbonden aan het project. |
| [!UICONTROL **Aantal gebruikers**] | Het aantal gebruikers dat aan het project is gekoppeld. <!-- ??? --> |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende afmetingen, Annotaties, Soorten publiek, enzovoort.</li><li>API-aanroepen van 1.4 of 2.0 API</li><li>Intelligente waarschuwingen</li></ul> |
| [!UICONTROL **Gemiddelde complexiteit**] | De gemiddelde complexiteit van aanvragen die in het project zijn opgenomen. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p><ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

#### Gegevens weergeven per toepassing

Wanneer u [!UICONTROL **Toepassing**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Toepassing**] | De toepassing waar de query&#39;s zijn gestart. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal aanvragen dat aan de toepassing is gekoppeld. |
| [!UICONTROL **Aantal gebruikers**] | Het aantal gebruikers dat aan de toepassing is gekoppeld. <!--???--> |
| [!UICONTROL **Aantal projecten**] | Het aantal projecten verbonden aan de toepassing. <!--???--> |
| [!UICONTROL **Gemiddelde complexiteit**] | De gemiddelde ingewikkeldheid van verzoeken verbonden aan de toepassing. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:<ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

<!--

### Filter

You can filter the table by Application (see list in the table below), by User, and by Project.

![filter](/help/admin/admin/assets/filter.png)

### Summary Numbers {#summary}

![filter](/help/admin/admin/assets/summary_numbers.png)

The Summary Numbers show the following information:

| Summary Number | Description |
| --- | --- |
| [!UICONTROL **Users**] | The number of users that are currently sending reporting requests to this report suite. |
| [!UICONTROL **Projects**] | Workspace projects, Report Builder workbooks, etc.  | 
| [!UICONTROL **Queries**] | The number of queries currently running. |
| [!UICONTROL **Average Wait Time**] | The average wait time for all running queries.  |
| [!UICONTROL **Usage Capacity**] | The current usage capacity for this report suite. |

{style="table-layout:auto"}

-->
