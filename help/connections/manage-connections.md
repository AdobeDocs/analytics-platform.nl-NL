---
title: Verbindingen beheren in Customer Journey Analytics
description: Beschrijft hoe te om verbindingen aan de datasets van Experience Platform in Customer Journey Analytics (Customer Journey Analytics) te beheren.
mini-toc-levels: 3
exl-id: 0a87518c-3608-44ad-b5e3-976f97560433
solution: Customer Journey Analytics
feature: Connections
role: Admin
source-git-commit: 5311106f486a30dbc7f06b3ef60dc7e666d2fe03
workflow-type: tm+mt
source-wordcount: '4052'
ht-degree: 0%

---

# Verbindingen beheren

Zodra u [ creeerde of uitgegeven één of meerdere verbindingen ](/help/connections/create-connection.md) hebt, kunt u hen in **[!UICONTROL Connections]** beheren. Via verbindingen kunt u:

* Bekijk al uw verbindingen bij een blik, met inbegrip van de eigenaar, de zandbak, en wanneer de verbindingen werden gecreeerd en werden gewijzigd.
* Bewerk een verbinding.
* Een verbinding verwijderen.
* Maak een gegevensweergave via een verbinding.
* Alle gegevenssets weergeven in een verbinding.
* Controleer de status van de datasets van uw verbinding en de status van het innameproces. Wanneer zijn bijvoorbeeld uw gegevens beschikbaar, zodat u in Analysis Workspace kunt beginnen met rapporteren en analyseren.
* Identificeer om het even welke gegevensdiscrepanties toe te schrijven aan misconfiguration. Ontbreekt u rijen? Zo ja, welke rijen ontbreken en waarom? Hebt u verbindingen verkeerd geconfigureerd en ontbrekende gegevens veroorzaakt in Customer Journey Analytics?
* Krijg inzicht in het gebruik van ingeklapte en te melden rijen over al uw verbindingen.

[!UICONTROL Connections] heeft twee interfaces: [[!UICONTROL List]](#list) en [[!UICONTROL Usage]](#usage) .


## Lijst

De interface [!UICONTROL List] is de standaardinterface voor verbindingen. Als deze optie niet is geselecteerd, selecteert u de tab **[!UICONTROL List]** voor toegang tot de interface.

![ lijstmening ](assets/list-view.png)

De interface [!UICONTROL List] toont een lijst van alle beschikbare verbindingen. U kunt snel naar een verbinding zoeken gebruikend het vakje van het Onderzoek ![ Onderzoek ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg).

De volgende kolommen of pictogrammen zijn beschikbaar in de tabel.

| Kolom of pictogram | Beschrijving |
| --- | --- |
| [!UICONTROL Name] | De vriendelijke naam van de verbinding. Als u de details van de verbinding wilt zien, selecteert u de naam van de hyperlink. Zie [ details van de Verbinding ](#connection-details). |
| ![ Informatie ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) | Om informatie over [!UICONTROL Datasets included], [!UICONTROL Sandbox], [!UICONTROL Owner], en meer te bekijken, selecteer ![ Informatie ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) naast de verbindingsnaam.<p>Een popup venster toont details. <p><img src="./assets/conn-info.png" alt="Verbindingsgegevens weergeven" width="400"/> |
| ![ mening van Gegevens ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) | Om [ een gegevensmening ](#create-a-data-view) voor de verbinding tot stand te brengen, uitgezochte ![ mening van Gegevens ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg). Dit pictogram wordt alleen weergegeven wanneer er al geen gegevensweergave is gekoppeld aan de verbinding. |
| ![ Meer ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) | Selecteer ![ Meer ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) aan: <p>![ geef ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) [ uit ](#edit-a-connection) een verbinding.<p>![ Schrap ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) [ schrapt ](#delete-a-connection) een verbinding.<p>![ mening van Gegevens ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) [ creeer nieuwe gegevensmening ](#create-a-data-view). Aanvullende gegevensweergaven maken voor de verbinding.<p>![ GraphPathing ](/help/assets/icons/GraphPathing.svg) kaart van de Verbinding. Een verbindingskaart voor de verbinding weergeven. |
| **[!UICONTROL Datasets]** | Één of meerdere verbindingen met de datasets die deel van de verbinding uitmaken. U kunt de datasethyperlink selecteren om de dataset in de verbinding te bekijken. Als meer datasets deel van de geselecteerde verbinding uitmaken, selecteer **[!UICONTROL +*x *meer]**om een **[!UICONTROL Datasets included]**paneel te tonen. Dit paneel toont verbindingen aan alle datasets en een optie om naar een specifieke dataset te zoeken die deel van de verbinding uitmaakt.<p><img src="./assets/datasets-included.png" alt="Bijbehorende gegevenselementen" width="400"/><p>Als u een naam van een gegevensset selecteert, wordt de gegevensset in de gebruikersinterface van Experience Platform op een nieuw tabblad geopend. |
| **[!UICONTROL Sandbox]** | De [ zandbak van Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) waarvan deze verbinding zijn datasets trekt. Deze sandbox werd geselecteerd toen u de verbinding voor het eerst maakte. Het kan niet worden gewijzigd. |
| **[!UICONTROL Owner]** | De persoon die de verbinding heeft gemaakt. |
| **[!UICONTROL Import new data]** | De status van het invoeren van nieuwe gegevens voor datasets: <p>![ groene Status ](assets/status-green.svg)    **[!UICONTROL _x _op]**voor datasets die worden gevormd om nieuwe gegevens in te voeren, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _x van_]** voor datasets niet gevormd om nieuwe gegevens in te voeren. |
| **[!UICONTROL Date created]** | De tijdstempel op het moment dat de verbinding werd gemaakt. |
| **[!UICONTROL Last modified]** | De tijdstempel wanneer de verbinding voor het laatst is bijgewerkt. |
| **[!UICONTROL Backfill data]** | De status voor backfill gegevens over datasets.<p>![ rode Status ](assets/status-red.svg)   **[!UICONTROL _x _ontbroken backfills]**voor aantal ontbroken backfills over datasets,<p>![ Oranje van de Status ](assets/status-orange.svg)   **[!UICONTROL _x _backfills verwerking]**voor aantal verwerkingsterugvullingen over datasets,<p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _voltooide backfills]**voor aantal voltooide backfills voor datasets, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _weg_]** voor het geval dat geen backfills voor de datasets in de verbinding worden bepaald. |

Om te vormen welke kolommen om te tonen selecteren ![ montages van de Kolom ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg), die **toont aanpassen lijst** dialoog die u toestaat om kolommen in of uit in de lijst te draaien.

### Een verbinding bewerken

Een verbinding bewerken:

1. Selecteer ![ Meer ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) naast de verbindingsnaam
1. Selecteer ![ uitgeven ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit]** van het contextmenu.

U kunt ook:

1. Selecteer de verbindingsrij.

1. Selecteer ![ uitgeven ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit]** van de blauwe bar.

Wanneer u een verbinding bewerkt, kunt u:

* Nieuwe gegevens beginnen en stoppen.
* Wijzig de naam van een verbinding.
* Vernieuw de gegevensset(s).
* Verwijder dataset/s uit de verbindingen.

Zie [ creeer of geef een verbinding ](create-connection.md) voor meer informatie uit.


### Een verbinding verwijderen {#connections-delete}

Een verbinding verwijderen:

1. Selecteer ![ Meer ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) naast de verbindingsnaam.
1. Selecteer ![ Schrapping ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Delete]**.

U kunt ook:

1. Selecteer de verbindingsrij.

1. Selecteer ![ Schrapping ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Delete]** van de blauwe bar.

Wanneer u een verbinding verwijdert, wordt in het deelvenster **[!UICONTROL Delete connection]** aangegeven welke gegevensweergaven worden verwijderd en welke werkruimteprojecten worden beïnvloed.

![ verbinding van de Schrapping ](assets/delete-connection.png)

Selecteer **[!UICONTROL Continue]** om de verbinding te verwijderen.

Zie [ implicaties van de Schrapping ](/help/technotes/deletion.md) voor meer informatie over het schrappen van een verbinding.


### Een gegevensweergave voor een verbinding maken

Een nieuwe gegevensweergave maken voor een verbinding

* Als er geen gegevensweergave is gekoppeld aan de verbinding:

   1. Selecteer ![ toevoegen gegevensmening ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) naast de verbindingsnaam.

* Als er al een of meer gegevensweergaven zijn gemaakt voor de verbinding:

   1. Selecteer ![ Meer ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) naast de verbindingsnaam.
   1. Selecteer ![ toevoegen gegevensmening ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) **[!UICONTROL Create new data view]**.

U kunt ook:

1. Selecteer de verbindingsrij.

1. Selecteer ![ toevoegen gegevensmening ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) **[!UICONTROL Create data view]** van de blauwe knoopbar.

Zie [ creeer of geef een gegevensmening ](/help/data-views/create-dataview.md) voor meer informatie uit.


### Een verbinding toewijzen

Om a [ verbindingskaart ](/help/connections/create-connection.md#connection-map) te bekijken die het verband tussen de datasets detailleert die deel van een verbinding uitmaken:

1. Selecteer ![ Meer ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) naast de verbindingsnaam.
1. Selecteer ![ GraphPathing ](/help/assets/icons/GraphPathing.svg) **[!UICONTROL Connection map]**.

### Verbindingsgegevens {#connection-detail}

Als u naar de gegevens voor een verbinding wilt gaan, selecteert u een verbindingsnaam in de tabel met verbindingen.

![ Al datasetvenster dat widgets en montages ](assets/conn-details.png) toont

De interface van de Details van Verbindingen verstrekt een gedetailleerde mening van de status van een verbinding. U kunt:

* Controleer de status van de datasets van uw verbinding en van het innameproces.
* Identificeer configuratieproblemen die overgeslagen of geschrapte verslagen kunnen veroorzaken.
* Zie wanneer de gegevens beschikbaar zijn voor rapportage.

| Gebruikersinterface | Beschrijving |
| --- | --- |
| ![ geef ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit Connection]** uit | Om de details van een verbinding uit te geven, uitgezocht ![ geef ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit Connection]** uit. Zie [ creeer of geef een verbinding ](create-connection.md) voor meer informatie uit. |
| **[!UICONTROL *de selecteur van de Dataset *]** | Hiermee kunt u een of alle gegevenssets in de verbinding kiezen. U kunt geen datasets selecteren. Wordt standaard ingesteld op **[!UICONTROL All datasets]** . |
| **[!UICONTROL *de bereikselecteur van de Datum *]** | Bewerk begindatum, einddatum, of selecteer ![ Kalender ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) om de selecteur van de datumwaaier te openen. Selecteer in de datumbereikkiezer een datumbereik met een van de vooraf gedefinieerde punten (bijvoorbeeld **[!UICONTROL Last 6 months]** ) of gebruik de kalender om de begin- en einddatum te selecteren. Selecteer **[!UICONTROL Apply]** om het nieuwe datumbereik toe te passen. |
| **[!UICONTROL Records of event data available]** | Het totale aantal rijen van de gebeurtenisdataset beschikbaar voor het melden, **voor de volledige verbinding**. Deze telling is onafhankelijk van enige kalendermontages. De telling verandert als u een dataset van de datasetselecteur selecteert of door een dataset in de lijst te selecteren. Als er gegevens zijn toegevoegd, is er een vertraging van 1-2 uur om de gegevens in de rapportage weer te geven. |
| [!UICONTROL **[!UICONTROL Metrics]**] | Geef een overzicht van de gebeurtenissen, opzoekactie, profielen en samenvattingsrecords die zijn toegevoegd, overgeslagen en verwijderd, en van het aantal toegevoegde batches. Deze metriek zijn gebaseerd op **de dataset en de datumwaaier u** hebt geselecteerd.<p>Selecteer **[!UICONTROL Check detail]** om de pop-up **[!UICONTROL Check skipped detail]** weer te geven. popup maakt een lijst van het aantal overgeslagen verslagen en de reden voor alle gebeurtenisdatasets of geselecteerde dataset.<p><img src="./assets/skipped-records.png" width="500"/><p>Selecteer ![ Pop-up Info ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) met meer informatie. Voor sommige overgeslagen redenen, zoals [!UICONTROL Empty visitor ID], toont popup Steekproef PSQL voor EQS (Experience Platform voor de Dienst van de Vraag) u in [ de Dienst van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/home) kunt gebruiken om voor de overgeslagen verslagen in de dataset te vragen. Selecteer ![ Exemplaar ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Copy_18_N.svg) **[!UICONTROL Copy sample PSQL for EQS]** om SQL te kopiëren. |
| **[!UICONTROL Records added]** | Wijst op hoeveel rijen in de geselecteerde tijdspanne, **voor de dataset en de datumwaaier werden toegevoegd u** hebt geselecteerd. Om de 10 minuten bijgewerkt. |
| **[!UICONTROL Records skipped]** | Wijst op hoeveel rijen in de geselecteerde tijdspanne, **voor de dataset en de datumwaaier werden overgeslagen u** hebt geselecteerd. De redenen voor het overslaan van verslagen omvatten: ontbrekende timestamps, ontbrekende of ongeldige of identiteitskaart van de Rekening [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, etc. Om de 10 minuten bijgewerkt. <p>Ongeldige id&#39;s (zoals `undefined` of `00000000` , of een combinatie van getallen en letters in een [!UICONTROL Person ID] die in een gebeurtenis meer dan 1 miljoen keer in een bepaalde maand voorkomen) zijn id&#39;s die niet aan een bepaalde gebruiker of persoon kunnen worden toegewezen. Deze rijen kunnen niet in het systeem worden opgenomen en in fout-prone opname en rapportering resulteren. Om ongeldige persoon IDs of identiteitskaarts van de Rekening [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} te bevestigen, hebt u 3 opties:<ul><li>Het gebruik [ Stitching ](/help/stitching/overview.md) om undefined of volledig-nul gebruiker te bevolken - identiteitskaarts met geldige gebruiker IDs.</li><li>Maak de gebruikersnaam leeg. Deze wordt overgeslagen tijdens het invoeren (voorkeur aan ongeldige of geen gebruikers-id&#39;s).</li><li>Corrigeer eventuele ongeldige gebruikers-id&#39;s in uw systeem voordat u de gegevens opneemt.</li></ul> |
| **[!UICONTROL Records deleted]** | Wijst op hoeveel rijen in de geselecteerde tijdspanne werden geschrapt, **voor de dataset en de datumwaaier u** hebt geselecteerd. Iemand heeft bijvoorbeeld een gegevensset verwijderd in [!DNL Experience Platform] . Om de 10 minuten bijgewerkt.<p>In sommige scenario&#39;s, kan deze waarde ook verslagen omvatten die, zoals met het stitching of sommige updates van de raadplegingsdataset worden vervangen. Bekijk dit voorbeeld:</p><ul><li>U uploadt één verslag aan een individuele dataset van het Profiel XDM, die Customer Journey Analytics wordt gevormd om als gegevens van de profielraadpleging in te voeren. In de verbindingsdetails, zou deze dataset 1 toegevoegde verslag tonen.</li><li>U uploadt een duplicaat van de oorspronkelijke record naar dezelfde AEP-gegevensset, die nu twee records bevat. Customer Journey Analytics neemt het extra verslag van het profiel of de rekening [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} raadplegingsdataset op. Aangezien een profiel of rekeningsverslag reeds in de verbinding voor die persoonsidentiteitskaart of rekeningsidentiteitskaart [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} wordt opgenomen, schrapt Customer Journey Analytics zijn vroegere versie en voegt de nieuwe profielgegevens toe. In de verbindingsdetails, zou deze actie 1 toegevoegd en 1 geschrapt verslag vertegenwoordigen, omdat Customer Journey Analytics slechts de meest recente gegevens van de profielraadpleging voor om het even welke ingebedde persoonsidentiteitskaart of rekeningsidentiteitskaart [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} behoudt.</li><li>In totaal bevat de AEP-gegevensset twee records die identiek zijn. Afzonderlijk, tonen de de verbindingsdetails van Customer Journey Analytics de status van zijn opgenomen gegevens: 2 verslagen toegevoegd en 1 verslag geschrapt voor deze profieldataset. </li></ul> |
| ![ Onderzoek ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) | Veld voor het zoeken naar gegevenssets. U kunt de datasetlijst door datasetnaam of [!UICONTROL Dataset ID] zoeken. |
| [!UICONTROL Datasets table] | Toont de datasets die deel van de verbinding uitmaken. Zie de onderstaande tabel voor verdere uitleg. |

De datasetlijst toont de volgende kolommen:

| Kolom | Beschrijving |
| --- | --- |
| **[!UICONTROL Datasets]** | De naam van de dataset die deel van de verbinding uitmaakt. U kunt de hyperlink selecteren om de dataset in Experience Platform UI op een nieuw lusje te openen. U kunt de rij of checkbox selecteren om details voor de geselecteerde dataset slechts te tonen. |
| **[!UICONTROL Dataset ID]** | Automatisch gegenereerd door Experience Platform. |
| **[!UICONTROL Records added]** | Het aantal datasetverslagen (rijen) die aan een verbinding tijdens het geselecteerde tijdinterval worden toegevoegd. |
| **[!UICONTROL Records skipped]** | Het aantal datasetverslagen (rijen) die tijdens gegevensoverdracht voor een verbinding tijdens het geselecteerde tijdinterval worden overgeslagen. |
| **[!UICONTROL Records deleted]** | Het aantal datasetverslagen (rijen) die uit een verbinding tijdens het geselecteerde tijdinterval worden verwijderd. |
| **[!UICONTROL Batches added]** | Het aantal gegevenssetpartijen is toegevoegd aan een verbinding. |
| **[!UICONTROL Last added]** | De tijdstempel van de laatste batch uit de dataset die is toegevoegd aan een verbinding. |
| **[!UICONTROL Data source type]** | Het brontype van de dataset. U definieert het brontype wanneer u een verbinding maakt. |
| **[!UICONTROL Dataset type]** | Het gegevenstype van de dataset voor deze dataset. Type kan [!UICONTROL Event], [!UICONTROL Profile], [!UICONTROL Lookup] of [!UICONTROL Summary] zijn. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) |
| **[!UICONTROL Schema]** | Het schema van Experience Platform waarop de dataset is gebaseerd. |
| **[!UICONTROL Import new data]** | De status van het invoeren van nieuwe gegevens voor de dataset: <p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _op]**als de dataset wordt gevormd om nieuwe gegevens in te voeren, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _x van_]** als de dataset wordt gevormd om nieuwe gegevensimport niet in te voeren. |
| **[!UICONTROL Transform data]** | De transformatiestatus van toepasselijke B2B-opzoekgegevenssets. Zie [ datasets van de Transformatie voor B2B raadplegingen ](transform-datasets-b2b-lookups.md) voor meer informatie.<p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _op]**voor toepasselijke datasets die voor transformatie worden toegelaten, <p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _x van_]** voor toepasselijke datasets niet toegelaten voor transformatie, en<p>**[!UICONTROL N/A]** voor alle andere gegevenssets, niet van toepassing voor transformatie. |
| **[!UICONTROL Backfill data]** | De status van backfill-gegevens voor de dataset.<p>![ rode Status ](assets/status-red.svg)   **[!UICONTROL _x _ontbroken backfills]**voor aantal ontbroken backfills,<p>![ rode Status ](assets/status-orange.svg)   **[!UICONTROL _x _backfills verwerking]**voor aantal verwerkings backfills,<p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _voltooide backfills]**voor aantal voltooide backfills, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _weg_]** in het geval de backfills niet worden gevormd. |
| **[!UICONTROL Import new data]** | De status van het invoeren van nieuwe gegevens voor de dataset: <p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _op]**als de dataset wordt gevormd om nieuwe gegevens in te voeren, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _x van_]** als de dataset wordt gevormd om nieuwe gegevens niet in te voeren. |
| **[!UICONTROL Backfill data]** | De status van backfill-gegevens voor de dataset.<p>![ rode Status ](assets/status-red.svg)   **[!UICONTROL _x _ontbroken backfills]**voor aantal ontbroken backfills,<p>![ rode Status ](assets/status-orange.svg)   **[!UICONTROL _x _backfills verwerking]**voor aantal verwerkings backfills,<p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _voltooide backfills]**voor aantal voltooide backfills, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _weg_]** voor het geval dat geen backfills wordt gevormd. |

>[!IMPORTANT]
>
>Gegevens die vóór 13 augustus 2021 zijn ingevoerd, worden niet weerspiegeld in de interface [!UICONTROL Connections] .

#### Deelvenster Verbinding

Wanneer geen dataset in de datasetlijst wordt geselecteerd, toont een paneel op de rechterkant van de interface van Verbindingen verbindingsopties en details.

| Opties | Beschrijving |
| --- | --- |
| ![ verfrissen zich ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) [!UICONTROL Refresh] | Om de verbinding te verfrissen en onlangs toegevoegde verslagen toe te staan om worden weerspiegeld, uitgezocht ![ verfrist zich ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) **[!UICONTROL Refresh]**. |
| ![ Schrapping ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Delete]** | [ Schrap ](#delete-a-connection) deze verbinding. |
| ![ voeg gegevensmening ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) toe **[!UICONTROL Create data view]** | [ creeer een gegevensmening ](#create-a-data-view) die op deze verbinding wordt gebaseerd. Zie [ meningen van Gegevens ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views) voor meer informatie. |
| **[!UICONTROL Connection name]** | De vriendelijke naam van de verbinding. |
| **[!UICONTROL Connection description]** | Een meer gedetailleerde beschrijving die het doel van deze verbinding beschrijft. |
| **[!UICONTROL Sandbox]** | De [ zandbak van Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) waarvan deze verbinding zijn dataset/s trekt. Deze sandbox werd geselecteerd toen u de verbinding voor het eerst maakte. Het kan niet worden gewijzigd. |
| **[!UICONTROL Connection ID]** | Deze id wordt gegenereerd in Experience Platform. U kunt ![ Exemplaar ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Copy_18_N.svg) gebruiken om identiteitskaart te kopiëren. |
| **[!UICONTROL Data views using connection]** | Hier worden alle gegevensweergaven weergegeven die deze verbinding gebruiken. |
| **[!UICONTROL Import new data]** | De status van het invoeren van nieuwe gegevens voor datasets: <p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _op]**voor hoeveel datasets worden gevormd om nieuwe gegevens in te voeren, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _x van_]** voor hoeveel datasets de nieuwe gegevensinvoer wordt uitgezet. |
| **[!UICONTROL Backfill data]** | De status van backfill-gegevens voor datasets.<p>![ rode Status ](assets/status-red.svg)   **[!UICONTROL _x _ontbroken backfills]**voor aantal ontbroken backfills over datasets,<p>![ rode Status ](assets/status-orange.svg)   **[!UICONTROL _x _backfills verwerking]**voor aantal verwerkingsterugvullingen over datasets,<p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _voltooide backfills]**voor aantal voltooide backfills voor datasets, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _weg_]** voor het geval dat geen backfills voor de datasets in de verbinding worden bepaald. |
| **[!UICONTROL Transform data]** | De transformatiestatus van toepasselijke B2B-opzoekgegevenssets. Zie [ datasets van de Transformatie voor B2B raadplegingen ](transform-datasets-b2b-lookups.md) voor meer informatie.<p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _op]**voor aantal datasets die voor transformatie worden toegelaten. |
| **[!UICONTROL Created by]** | De naam van de persoon die de verbinding heeft gemaakt. |
| **[!UICONTROL Last modified]** | De tijdstempel van de laatste wijziging in de verbinding. |
| **[!UICONTROL Last modified by]** | De persoon die de verbinding als laatste heeft gewijzigd. |

#### Deelvenster Gegevensset

Wanneer een datasetrij in de datasetlijst wordt geselecteerd, toont een paneel op de rechterkant van de interface van Verbindingen details voor de geselecteerde dataset.

| Details | Beschrijving |
| --- | --- |
| **[!UICONTROL Person ID]** | An identity that was defined in the dataset schema in the Experience Platform. Dit is de persoon-id die u hebt geselecteerd tijdens het maken van de verbinding. Als u een verbinding creeert die datasets met verschillende IDs omvat, weerspiegelt het melden dat. Om datasets samen te voegen, moet u zelfde identiteitskaart van de Persoon over datasets gebruiken. |
| **[!UICONTROL Key]** | De sleutel die u voor een raadplegingsdataset hebt gespecificeerd. |
| **[!UICONTROL Matching Key]** | De passende sleutel die u voor een raadplegingsdataset hebt gespecificeerd. |
| **[!UICONTROL Timestamp]** | De tijdstempel die is gedefinieerd voor een gebeurtenisgegevensset. |
| **[!UICONTROL Records available]** | Het totale aantal rijen dat voor deze dataset wordt opgenomen, voor de bepaalde tijdspanne die door de kalender wordt geselecteerd. Er is geen latentie in termen van het krijgen van de gegevens om in rapportering te verschijnen, zodra het wordt toegevoegd. Nochtans, wanneer u een gloednieuwe verbinding creeert, is er [ latentie ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-faq). |
| **[!UICONTROL Records added]** | Hoeveel rijen zijn toegevoegd in de geselecteerde tijdsperiode. |
| **[!UICONTROL Records deleted]** | Hoeveel records zijn verwijderd tijdens de geselecteerde tijdsperiode. |
| **[!UICONTROL Batches added]** | Hoeveel gegevensbatches zijn toegevoegd aan deze gegevensset. |
| **[!UICONTROL Records skipped]** | Hoeveel rijen zijn overgeslagen tijdens inname in de geselecteerde tijdsperiode.<p>De redenen voor het overslaan van verslagen omvatten: Ontbrekende timestamps, ontbrekende of ongeldige persoonidentiteitskaart of rekeningidentiteitskaart [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, etc. Om de 10 minuten bijgewerkt.<p>Ongeldige id&#39;s (zoals `undefined` of `00000000` , of een combinatie van getallen en letters in een [!UICONTROL Person ID] die in een gebeurtenis meer dan 1 miljoen keer in een bepaalde maand voorkomen) zijn id&#39;s die niet aan een bepaalde gebruiker of persoon kunnen worden toegewezen. Deze rijen kunnen niet in het systeem worden opgenomen en in fout-prone opname en rapportering resulteren. U kunt ongeldige personen-id&#39;s of account-id&#39;s corrigeren aan de hand van drie opties:<ul><li>Het gebruik [ Stitching ](/help/stitching/overview.md) om undefined of volledig-nul gebruiker te bevolken - identiteitskaarts met geldige gebruiker IDs.</li><li>Maak de gebruikersnaam leeg, die vervolgens tijdens de inname wordt overgeslagen (bij voorkeur aan ongeldige of helemaal geen gebruikers-id&#39;s).</li><li>Corrigeer eventuele ongeldige gebruikers-id&#39;s in uw systeem voordat u de gegevens opneemt.</li></ul> |
| **[!UICONTROL Last added]** | De tijdstempel van de laatste batch is toegevoegd. |
| **[!UICONTROL Import new data]** | De status van het invoeren van nieuwe gegevens voor de dataset: <p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _op]**als de dataset wordt gevormd om nieuwe gegevens in te voeren, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _x van_]** als de dataset wordt gevormd om nieuwe gegevens niet in te voeren. |
| **[!UICONTROL Backfill data]** | De status van backfill-gegevens voor de dataset.<p>![ rode Status ](assets/status-red.svg)   **[!UICONTROL _x _ontbroken backfills]**voor aantal ontbroken backfills,<p>![ rode Status ](assets/status-orange.svg)   **[!UICONTROL _x _backfills verwerking]**voor aantal verwerkings backfills,<p>![ groene Status ](assets/status-green.svg)   **[!UICONTROL _x _voltooide backfills]**voor aantal voltooide backfills, en<p>![ grijze Status ](assets/status-gray.svg)   **[!UICONTROL _weg_]** voor het geval dat geen backfills wordt gevormd.<p>Om een dialoog met een overzicht van de vroegere backfills voor de dataset te tonen, selecteer <img src="./assets/pastbackfill.svg" alt="Achtervullingen verleden" width="15"/> **[!UICONTROL Past backfills]**. |
| **[!UICONTROL Data source type]** | Het type van gegevensbron zoals bepaald toen het toevoegen van de dataset aan de verbinding. |
| **[!UICONTROL Dataset type]** | Ofwel [!UICONTROL Event] , [!UICONTROL Profile] , [!UICONTROL Lookup] of [!UICONTROL Summary] . [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) |
| **[!UICONTROL Schema]** | Het Experience Platform-schema waarop deze gegevensset is gebaseerd. |
| **[!UICONTROL Dataset ID]** | Deze gegevensset-id wordt gegenereerd in Experience Platform. |


## Gebruik {#connections-usage}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_usage_keyusagemetrics"
>title="Metingen van sleutelgebruik"
>abstract="Maandelijkse en totale gegevens verstrekken voor kern- en historische te rapporteren rijen."
<!-- markdownlint-enable MD034 -->


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_usage_monthlyingestedrows"
>title="Maandelijkse gegeneerde rijen"
>abstract="Hiermee wordt het totale aantal records gemeten dat maandelijks aan het systeem wordt toegevoegd om inzicht te verschaffen in de groei van gegevens en de innamesnelheden."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_usage_monthlyreportablerows"
>title="Maandelijkse te rapporteren rijen"
>abstract="Tracks the number of rows available for reporting. Te rapporteren rijen zijn de ingesloten rijen min de rijen die tijdens inname worden overgeslagen en verwijderd. Te rapporteren rijen fungeren als een belangrijke metrische factor voor facturering en gegevensgebruik."
<!-- markdownlint-enable MD034 -->


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_usage_detailbreakdown"
>title="Gedetailleerde uitsplitsing."
>abstract="U kunt gedetailleerde metriek door verbinding, dataset, zandbak, en markeringen bekijken, met de optie om een Csv- dossier van de gegevens te downloaden."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_usage_otherdatasets"
>title="Andere gegevenssets"
>abstract="Voor de maanden vóór September 2024, werden de gegevens verzameld op het datasetniveau en als *Andere datasets* voor duidelijkheid getoond. Beginnend van September 2024, wordt het gegeven verzameld op een korrelig datasetniveau, en *Andere datasets* zullen niet meer verschijnen."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_usage_unknowndatasetsorconnections"
>title="Onbekende datasets of verbindingen"
>abstract="Onbekende datasets of verbindingen worden getoond gebruikend hun IDs."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_usage_datanotavailable"
>title="Gegevens niet beschikbaar"
>abstract="Historische gegevens van vóór september 2024 zijn niet beschikbaar vanwege systeembeperkingen. Metrische gegevens worden verzameld en weergegeven vanaf september 2024. Het diagram toont de laatste 18 maanden op de tijdlijn en toekomstige gegevens worden weergegeven wanneer de gegevens beschikbaar komen."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_corereportablerows"
>title="Vermelde kernrijen"
>abstract="Hiermee geeft u het totale aantal rijen weer dat beschikbaar is in de afgelopen 13 maanden. Op 1 februari 2024 toont het getal bijvoorbeeld het totale aantal rijen dat beschikbaar is met een tijdstempel voor een gebeurtenis van januari 2023 tot januari 2024."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_connections_historicalreportablerows"
>title="Historische te rapporteren rijen"
>abstract="Geeft het totale aantal rijen weer dat beschikbaar is voor de periode ouder dan 13 maanden. Op 1 februari 2024 toont het getal bijvoorbeeld het totaal aan rijen dat beschikbaar is met een tijdstempel voor een gebeurtenis die ouder is dan januari 2023."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_usage_keyusagemetrics"
>title="Metingen van sleutelgebruik"
>abstract="Maandelijkse en totale gegevens verstrekken voor kern- en historische te rapporteren rijen."
<!-- markdownlint-enable MD034 -->


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_usage_monthlyingestedrows"
>title="Maandelijkse gegeneerde rijen"
>abstract="Hiermee wordt het totale aantal records gemeten dat maandelijks aan het systeem wordt toegevoegd om inzicht te verschaffen in de groei van gegevens en de innamesnelheden."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_usage_monthlyreportablerows"
>title="Maandelijkse te rapporteren rijen"
>abstract="Tracks the number of rows available for reporting. Te rapporteren rijen zijn de ingesloten rijen min de rijen die tijdens inname worden overgeslagen en verwijderd. Te rapporteren rijen fungeren als een belangrijke metrische factor voor facturering en gegevensgebruik."
<!-- markdownlint-enable MD034 -->


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_usage_detailbreakdown"
>title="Gedetailleerde uitsplitsing."
>abstract="U kunt gedetailleerde metriek door verbinding, dataset, zandbak, en markeringen bekijken, met de optie om een Csv- dossier van de gegevens te downloaden."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_usage_otherdatasets"
>title="Andere gegevenssets"
>abstract="Voor de maanden vóór September 2024, werden de gegevens verzameld op het datasetniveau en als *Andere datasets* voor duidelijkheid getoond. Beginnend van September 2024, wordt het gegeven verzameld op een korrelig datasetniveau, en *Andere datasets* zullen niet meer verschijnen."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_usage_unknowndatasetsorconnections"
>title="Onbekende datasets of verbindingen"
>abstract="Onbekende datasets of verbindingen worden getoond gebruikend hun IDs."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_usage_datanotavailable"
>title="Gegevens niet beschikbaar"
>abstract="Historische gegevens van vóór september 2024 zijn niet beschikbaar vanwege systeembeperkingen. Metrische gegevens worden verzameld en weergegeven vanaf september 2024. Het diagram toont de laatste 18 maanden op de tijdlijn en toekomstige gegevens worden weergegeven wanneer de gegevens beschikbaar komen."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_corereportablerows"
>title="Vermelde kernrijen"
>abstract="Hiermee geeft u het totale aantal rijen weer dat beschikbaar is in de afgelopen 13 maanden. Op 1 februari 2024 toont het getal bijvoorbeeld het totale aantal rijen dat beschikbaar is met een tijdstempel voor een gebeurtenis van januari 2023 tot januari 2024."
<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_historicalreportablerows"
>title="Historische te rapporteren rijen"
>abstract="Geeft het totale aantal rijen weer dat beschikbaar is voor de periode ouder dan 13 maanden. Op 1 februari 2024 toont het getal bijvoorbeeld het totaal aan rijen dat beschikbaar is met een tijdstempel voor een gebeurtenis die ouder is dan januari 2023."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="connections_breakdown_corereportablerows"
>title="Vermelde kernrijen"
>abstract="De kern rapporteerde rijen zijn momentopnamegrenzen, niet samengevoegde totalen. Deze waarden worden dynamisch bijgewerkt op basis van de laatste maand in het geselecteerde datumbereik. Als een klant Januari - Maart selecteert, zullen de waarden op de momentopname van Maart wijzen."

>[!CONTEXTUALHELP]
>id="connections_breakdown_historicalreportablerows"
>title="Historische te rapporteren rijen"
>abstract="Historische te rapporteren rijen zijn momentopnamewaarden, niet samengevoegde totalen. Deze waarden worden dynamisch bijgewerkt op basis van de laatste maand in het geselecteerde datumbereik. Als een klant Januari - Maart selecteert, zullen de waarden op de momentopname van Maart wijzen."

>[!CONTEXTUALHELP]
>id="connections_breakdown_cumulativereportablerows"
>title="Cumulatieve te rapporteren rijen"
>abstract="Cumulatieve te rapporteren rijen zijn momentopnamewaarden, niet samengevoegde totalen. Deze waarden worden dynamisch bijgewerkt op basis van de laatste maand in het geselecteerde datumbereik. Als een klant Januari - Maart selecteert, zullen de waarden op de momentopname van Maart wijzen."

<!-- markdownlint-enable MD034 -->



De interface [!UICONTROL Usage] toont het gebruik van ingebedde en te melden rijen over alle verbindingen. Als deze optie niet is geselecteerd, selecteert u de tab **[!UICONTROL Usage]** voor toegang tot de interface.

Deze interface ondersteunt u om te bepalen of uw Customer Journey Analytics-gebruik voldoet aan wat contractueel is overeengekomen. Naast controledoeleinden kunt u de interface van het Gebruik gebruiken om uw Customer Journey Analytics vergunningsvernieuwing te plannen.

De interface van het Gebruik gebruikt de volgende metriek

| Metrische naam | Beschrijving |
|---|---|
| Historische te rapporteren rijen | Aantal rijen voor de periode ouder dan 13 maanden. |
| Vermelde kernrijen | Aantal rijen over de laatste 13 maanden. |
| Verbruikte rijen | Hoeveel rijen worden opgenomen voor de specifieke periode. |
| Te rapporteren rijen | Hoeveel rijen van gegevens hebt u als deel van de verbinding voor de specifieke periode. |
| Cumulatieve rijen | Hoeveel rijen worden opgenomen tot de specifieke maand. |

>[!NOTE]
>
>Gegevens worden verzameld, vanaf juli 2024 voor de kern-, historische en totale gegevens. Neem contact op met uw accountmanager voor eerdere historische gegevens.
>



De interface van het Gebruik bestaat uit twee panelen:

* Het deelvenster **[!UICONTROL Key usage metrics]**: bevat kerngegevens en historische gegevens die worden gerapporteerd in rijen. Het deelvenster houdt ook percentagewijzigingen bij ten opzichte van de vorige maand voor zowel kern- als historische gegevensrijen.

  Het deelvenster wordt weergegeven in een visualisatie:

   * **[!UICONTROL Core data reportable rows]**.

     Hoeveel te rapporteren rijen hebt u in de afgelopen 13 maanden. Het samenvattingsnummer is het aantal core te rapporteren rijen (bijvoorbeeld 741M) voor de laatste maand (bijvoorbeeld december 2024).

   * **[!UICONTROL Historical data reportable rows]**.

     Hoeveel te rapporteren rijen hebt u voor de periode ouder dan 13 maanden. Het samenvattingsnummer is het aantal historische te rapporteren rijen (bijvoorbeeld 127M) voor de laatste maand (bijvoorbeeld december 2024).

  Wanneer u de muisaanwijzer boven een gestapelde balk in de visualisatie houdt, ziet u het aantal rijen voor dat specifieke gedeelte van de balk (bijvoorbeeld).


  ![ Metriek van het Sleutelgebruik ](assets/usage-key-usage-metrics.png)

* Een gecombineerd deelvenster met drie subdeelvensters voor:

+++ Verbruikte rijen

  Het subdeelvenster **[!UICONTROL Ingested rows]** meet het totale aantal records dat maandelijks aan het systeem wordt toegevoegd, zodat u inzicht krijgt in de groei van gegevens en de innamesnelheden. Het subdeelvenster bevat een overzicht van het totaal aantal opgenomen rijen van deze maand en de wijziging ten opzichte van de vorige maand.

  ![ Ingested rijen ](assets/usage-ingested-rows.png)

  U kunt de muisaanwijzer boven gegevenspunten in de visualisatie plaatsen en een pop-up met meer details weergeven.

+++

+++ Te rapporteren rijen

  De **[!UICONTROL Reportable rows]** visualisatie houdt het aantal rijen bij beschikbaar voor rapportering door overgeslagen en geschrapte rijen van ingebedde rijen af te trekken, die als zeer belangrijke metrisch voor het facturerings en gegevensgebruik dienen. Het subdeelvenster bevat twee samenvattingen:

   * **[!UICONTROL Last month total]**: Een overzicht van het totaal aantal te rapporteren rijen tot deze maand.
   * **[!UICONTROL This month]**: Een overzicht van het totaal aantal te rapporteren rijen van deze maand en de wijziging ten opzichte van de vorige maand.

  ![ Te Rapporteren rijen ](assets/usage-reportable-rows.png)

  U kunt de muisaanwijzer boven gegevenspunten in de visualisaties plaatsen om een pop-up met meer details weer te geven.

+++

+++ Gedetailleerde uitsplitsing

  U kunt de tabel **[!UICONTROL Detail breakdown]** gebruiken om gedetailleerde metriek weer te geven op basis van verbinding, gegevensset, sandbox en tags. Datasets worden gerapporteerd met id&#39;s in plaats van met namen, omdat de namen van gegevenssets tijdens een rapportageperiode kunnen worden gewijzigd. Onbekende gegevenssets of verbindingen worden gerapporteerd met id&#39;s.

  Voor de maanden vóór september 2024 werden gegevens verzameld op het niveau van de gegevensset en voor de duidelijkheid weergegeven als [!UICONTROL Other datasets] . Vanaf september 2024 worden gegevens verzameld op niveau van een granulaire gegevensset en wordt [!UICONTROL Other datasets] niet meer weergegeven.

   * Selecteer een combinatie voor **[!UICONTROL View by]** en **[!UICONTROL Breakdown by]** om de indeling te wijzigen.

     | **[!UICONTROL View by]** opties | **[!UICONTROL Breakdown by]** opties |
     |---|---|
     | **[!UICONTROL Connection]** | **[!UICONTROL -]** en **[!UICONTROL Dataset]** |
     | **[!UICONTROL Dataset]** | **[!UICONTROL -]** |
     | **[!UICONTROL Sandbox]** | **[!UICONTROL Connection]** |
     | **[!UICONTROL Tag]** | **[!UICONTROL Connection]** |

  ![ de mislukking van het Detail ](assets/usage-detail-breakdown.png)

+++

  U kunt een **[!UICONTROL Time range]** in maanden definiëren om over te rapporteren. Gebruik ![ Kalender ](/help/assets/icons/Calendar.svg) om de tijdwaaier te selecteren.

>[!MORELIKETHIS]
>
>[ Mening, los problemen op, en wijzig verbindingsmontages ](https://experienceleague.adobe.com/en/docs/customer-journey-analytics-learn/tutorials/connections/connections-details-experience-in-cja) leerprogramma.
>[Je Customer Journey Analytics-gebruik beheren ](/help/technotes/estimate-usage.md)
>
