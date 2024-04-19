---
title: Rapportactiviteiten weergeven in de rapportagManager
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
solution: Customer Journey Analytics
feature: Basics
exl-id: 1f5b2a42-162e-45a7-9fd4-8c1557f48bb8
role: Admin
source-git-commit: cbff0bc58150373df041f9e1594feee0b5bcc2ce
workflow-type: tm+mt
source-wordcount: '1980'
ht-degree: 0%

---

# Rapportactiviteiten weergeven in de rapportagManager

De [!UICONTROL Reporting Activity Manager] stelt beheerders in staat om problemen met de rapportcapaciteit tijdens piekrapportagetijden snel te diagnosticeren en op te lossen.

Voor meer informatie over het Melden van de Manager van de Activiteit, met inbegrip van zeer belangrijke voordelen en toestemmingsvereisten, zie [Overzicht van Activity Manager rapporteren](/help/reporting-activity-manager/reporting-activity-overview.md).

## Rapportactiviteiten voor alle verbindingen weergeven {#view-all-report-suites}

1. Ga in de Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]**.

   Er wordt een lijst met uw ingeschakelde basisverbindingen weergegeven.

   ![Rapporteringsactiviteit die de rapportenrij toont](assets/reporting-activity1.png)

1. Om het totale aantal rapportverzoeken voor alle verbindingen in uw organisatie te bekijken, breid uit [!UICONTROL **Meer weergeven**] om de [!UICONTROL **Maandelijkse verzoeken om rapporten**] grafiek.

   U kunt het aantal rapportverzoeken binnen uw organisatie voor de huidige maand en de vorige maand bekijken.

   ![Rapporteringsactiviteit die de rapportenrij toont](assets/reporting-activity-monthly.png)

1. (Optioneel) U kunt de lijst met verbindingen opzoeken of filteren:

   * Gebruik het zoekveld om te zoeken naar een specifieke verbinding. Typ de naam of de id van de verbinding en de lijst met updates van verbindingen terwijl u typt.

   * Selecteer de [!UICONTROL **Filter**] pictogram ![Filterpictogram](assets/filter-icon.png) om de lijst met filteropties uit te vouwen. U kunt filteren op [!UICONTROL **Favorieten**] of [!UICONTROL **Status**].

     Als u een verbinding als favoriet wilt markeren, selecteert u het sterpictogram links van de naam van de verbinding.

     <!-- (does this option still exist?) 1. (Optional) Select **[!UICONTROL Refresh]** at the top-right to refresh the data. -->

1. Gebruik informatie over elke verbinding weergeven. De gegevens die in de tabel worden weergegeven, vertegenwoordigen de rapportactiviteit voor de verbinding op het moment dat de pagina voor het laatst werd geladen.

   De volgende kolommen zijn beschikbaar:

   | UI-element | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Connection]** | De verbinding waarvan het melden activiteit u controleert. |
   | **[!UICONTROL Data Views]** | Toont alle gegevensmeningen die de verbinding gebruiken. De configuratie van de mening van gegevens kan ingewikkeldheid aan het melden van verzoeken toevoegen. |
   | **[!UICONTROL Capacity utilization]** | Het percentage van de rapporteringscapaciteit van de verbinding die, in real time wordt gebruikt. <p>**Opmerking** Een gebruikscapaciteit die 100% is, suggereert niet noodzakelijk dat u onmiddellijk begint rapporteringsverzoeken te annuleren. De gebruikscapaciteit van 100% kan gezond zijn als de gemiddelde wachttijd redelijk is. Anderzijds zou 100% van de gebruikscapaciteit een probleem kunnen suggereren als het aantal verzoeken in de wachtrij ook toeneemt.</p> |
   | **[!UICONTROL Queued requests]** | Het aantal verzoeken dat moet worden verwerkt. <!-- ??? --> |
   | **[!UICONTROL Queue wait time]** | De gemiddelde wachttijd alvorens de verzoeken beginnen te verwerken. <!-- ???? --> |
   | **[!UICONTROL Status]** | De mogelijke statussen zijn: <ul><li>[!UICONTROL **Actief**] (blauw): in de afgelopen twee uur zijn rapporten uitgevoerd op de verbinding. De gegevens in de tabel geven de rapportcapaciteit aan voor de verbinding op het moment dat de pagina voor het laatst werd geladen.</li><li>[!UICONTROL **Inactief**] (grijs): er zijn de afgelopen 2 uur geen rapporten over de verbinding uitgevoerd, zodat er geen gegevens voor de verbinding worden weergegeven.</li></ul> |

   {style="table-layout:auto"}

## Rapportactiviteiten voor één verbinding weergeven

1. Selecteer in Customer Journey Analytics [!UICONTROL **Gereedschappen**] > [!UICONTROL **Activity Manager rapporteren**].

1. Selecteer de gekoppelde titel van de verbinding waarvoor u details wilt weergeven.

   Gegevens over de rapportactiviteit worden weergegeven voor de verbinding die u hebt geselecteerd.

1. (Optioneel) Wanneer een verbinding voor het eerst wordt geladen in Rapportagentenbeheer, vertegenwoordigen de weergegeven gegevens de huidige gebruiksmaatstaven. Selecteer de optie [!UICONTROL **Vernieuwen**] de pagina handmatig vernieuwen.

   <!-- Need to update this screenshot: ![connection](assets/indiv-report-ste.png) -->

1. Gebruik de beschikbare grafieken en de lijst om rapportactiviteit in de verbinding te begrijpen.

   * [Grafieken weergeven](#view-graphs)

   * [Tabel weergeven](#view-table)

### Grafieken weergeven

De volgende grafieken zijn beschikbaar om u te helpen de activiteit begrijpen die in de verbinding gebeurt.

Als grafieken niet zichtbaar zijn, selecteert u de optie [!UICONTROL **Grafieken tonen**] knop.

#### Gebruiksgrafiek {#utilization}

De grafiek van het Gebruik toont rapporterend gebruik voor de geselecteerde verbinding in de laatste 2 uren.

Houd de cursor boven het diagram om punten in de tijd te bekijken waar het percentage van de gebruikscapaciteit het hoogst was gedurende die minuut.

* **X-as**: De capaciteit van het rapportagegebruik gedurende de laatste twee uur.
* **Y-as**: Het percentage van de rapportgebruikscapaciteit, door minuut.

  ![gebruikslijn](assets/utilization-graph.png)

#### Afzonderlijke gebruikersgrafiek

In de grafiek Afzonderlijke gebruikers wordt de rapportactiviteit voor de geselecteerde verbinding gedurende de laatste twee uur weergegeven.

Houd de cursor boven het diagram om punten in de tijd te bekijken waar het maximumaantal gebruikers het hoogst was gedurende die minuut.

* **X-as**: De rapportageactiviteit gedurende het laatste tijdkader van 2 uur.
* **Y-as**: Het aantal gebruikers dat rapportageverzoeken per minuut heeft ingediend.

  ![Afzonderlijke gebruikersgrafiek](assets/distinct-users-graph.png)

#### Verzoeken om grafiek

De grafiek van Verzoeken toont het aantal verwerkte en een rij gevormde verzoeken voor de geselecteerde verbinding over de laatste 2 uren.

Houd de cursor boven het diagram om punten in de tijd weer te geven waar het maximale aantal aanvragen het hoogst was voor die minuut.

* **X-as**: Het aantal verwerkte en een rij gevormde verzoeken over het laatste tijdkader van 2 uur.
* **Y-as**: Het aantal verwerkte verzoeken (in groen) en een rij gevormde verzoeken (in paars), door minuut.

  ![Afzonderlijke gebruikersgrafiek](assets/requests-graph.png)

#### Grafiek in wachtrij

De rij die grafiek toont de gemiddelde rij wacht tijd (in seconden) voor het melden van verzoeken om de geselecteerde verbinding over de laatste 2 uren.

Houd de cursor boven het diagram om punten in de tijd te bekijken waar de maximale gemiddelde wachttijd het hoogst was voor die minuut.

* **X-as**: De gemiddelde rij wacht tijd op het melden van verzoeken over het laatste 2 uurtijdkader.
* **Y-as**: De gemiddelde wachttijd (in seconden).

  ![Afzonderlijke gebruikersgrafiek](assets/queueing-graph.png)

### Tabel weergeven {#view-table}

Houd rekening met het volgende wanneer u de tabel weergeeft:

* U kunt ervoor kiezen om gegevens weer te geven door een van de volgende tabbladen boven aan de gegevenstabel te kiezen: [!UICONTROL **Verzoek**], [!UICONTROL **Gebruiker**], [!UICONTROL **Project**], of [!UICONTROL **Toepassing**].

* U kunt de lijst met verbindingen zoeken of filteren:

   * Gebruik het zoekveld om te zoeken naar een specifieke verbinding. Typ de naam of de id van de verbinding en de lijst met updates van verbindingen terwijl u typt.

   * Selecteer de [!UICONTROL **Filter**] pictogram ![Filterpictogram](assets/filter-icon.png) om de lijst met filteropties uit te vouwen. U kunt filteren op [!UICONTROL **Status**], [!UICONTROL **Complexiteit**], [!UICONTROL **Toepassing**], [!UICONTROL **Gebruiker**], of [!UICONTROL **Project**].

   * U kunt [!UICONTROL **Grafieken verbergen**] alleen de tabel weergeven.

![tabbladen](assets/report-activity-tabs.png)

#### Gegevens op verzoek weergeven

Wanneer u [!UICONTROL **Verzoek**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Aanvraag-id**] | Een unieke id die kan worden gebruikt voor probleemoplossingsdoeleinden. Als u de id wilt kopiëren, selecteert u de aanvraag en selecteert u de optie. [!UICONTROL **Aanvraag-id&#39;s kopiëren**]. |
| [!UICONTROL **Tijdsduur**] | Hoe lang de aanvraag is uitgevoerd. |
| [!UICONTROL **Begintijd**] | Wanneer de aanvraag is begonnen met de verwerking (op basis van de lokale tijd van de beheerder). |
| [!UICONTROL **Wacht op tijd**] | Hoe lang het verzoek heeft gewacht alvorens wordt verwerkt. Deze waarde staat doorgaans op &quot;0&quot; wanneer er voldoende capaciteit is. |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende metriek, Annotaties, Soorten publiek enzovoort.</li><li>API-aanroepen vanuit de 2.0-API</li><li>Intelligente waarschuwingen<li>Volledige tabelexport</li><li>Delen met koppelingen van anderen</li><li>Analyse met instructies</li><li>Een andere toepassing die de Analyse meldend motor vraagt</li></li></ul><p>**Opmerking:** Als de waarde van deze kolom [!UICONTROL **Onbekend**], betekent dit dat de aanvraagmetagegevens niet beschikbaar zijn voor de gebruiker.</p> |
| [!UICONTROL **Gebruiker**] | De gebruiker die de aanvraag heeft gestart. <p>**Opmerking:** Als de waarde van deze kolom [!UICONTROL **Onbekend**], betekent dit dat de aanvraagmetagegevens niet beschikbaar zijn voor de gebruiker.</p> |
| [!UICONTROL **Project**] | Opgeslagen projectnamen voor Workspace, API-rapport-id&#39;s enzovoort. (Metagegevens kunnen per toepassing verschillen.)<p>**Opmerking:** Als de waarde van deze kolom [!UICONTROL **Onbekend**], betekent dit dat het project niet is opgeslagen of dat de aanvraagmetagegevens niet beschikbaar zijn voor de gebruiker.</p> |
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
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende metriek, Annotaties, Soorten publiek enzovoort.</li><li>API-aanroepen vanuit de 2.0-API</li><li>Intelligente waarschuwingen<li>Volledige tabelexport</li><li>Delen met koppelingen van anderen</li><li>Analyse met instructies</li><li>Een andere toepassing die de Analyse meldend motor vraagt</li></li></ul> |
| [!UICONTROL **Gem-complexiteit**] | De gemiddelde ingewikkeldheid van verzoeken die door de gebruiker in werking worden gesteld. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p><ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

#### Gegevens weergeven per project

Wanneer u [!UICONTROL **Project**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Project**] | Het project waar de verzoeken werden ingediend. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal verzoeken verbonden aan het project. |
| [!UICONTROL **Aantal gebruikers**] | Het aantal gebruikers dat aan het project is gekoppeld. <!-- ??? --> |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende metriek, Annotaties, Soorten publiek enzovoort.</li><li>API-aanroepen vanuit de 2.0-API</li><li>Intelligente waarschuwingen<li>Volledige tabelexport</li><li>Delen met koppelingen van anderen</li><li>Analyse met instructies</li><li>Een andere toepassing die de Analyse meldend motor vraagt</li></li></ul> |
| [!UICONTROL **Gem-complexiteit**] | De gemiddelde complexiteit van aanvragen die in het project zijn opgenomen. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p><ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

#### Gegevens weergeven per toepassing

Wanneer u [!UICONTROL **Toepassing**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Toepassing**] | De aanvraag waar de verzoeken zijn ingediend. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal aanvragen dat aan de toepassing is gekoppeld. |
| [!UICONTROL **Aantal gebruikers**] | Het aantal gebruikers dat aan de toepassing is gekoppeld. <!--???--> |
| [!UICONTROL **Aantal projecten**] | Het aantal projecten verbonden aan de toepassing. <!--???--> |
| [!UICONTROL **Gem-complexiteit**] | De gemiddelde ingewikkeldheid van verzoeken verbonden aan de toepassing. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:<ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Meer maandgrenzen vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Meer kolommen maken de aanvraag complexer. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Meer segmenten maken de aanvraag complexer. |

{style="table-layout:auto"}

<!-- 

## Frequently asked questions {#faq}

| Question | Answer |
| --- | --- |
| | |

{style="table-layout:auto"}

-->
