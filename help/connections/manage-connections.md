---
title: Hoe te om verbindingen in Customer Journey Analytics te beheren
description: Beschrijft hoe te om verbindingen aan de datasets van het Experience Platform in Customer Journey Analytics (Customer Journey Analytics) te beheren.
mini-toc-levels: 3
exl-id: 0a87518c-3608-44ad-b5e3-976f97560433
solution: Customer Journey Analytics
feature: Connections
role: Admin
source-git-commit: 5078d10fe55123e45c1b890cded36965bb5e039f
workflow-type: tm+mt
source-wordcount: '2564'
ht-degree: 0%

---

# Verbindingen beheren

Als u eenmaal [een of meer verbindingen hebben gemaakt of bewerkt](/help/connections/create-connection.md), kunt u deze beheren in **[!UICONTROL Connections]**. Via verbindingen kunt u:

* Bekijk al uw verbindingen bij een blik, met inbegrip van de eigenaar, de zandbak, en wanneer de verbindingen werden gecreeerd en werden gewijzigd.
* Bewerk een verbinding.
* Een verbinding verwijderen.
* Maak een gegevensweergave via een verbinding.
* Alle gegevenssets weergeven in een verbinding.
* Controleer de status van de datasets van uw verbinding en de status van het innameproces. Wanneer zijn bijvoorbeeld uw gegevens beschikbaar, zodat u in Analysis Workspace kunt beginnen met rapporteren en analyseren.
* Identificeer om het even welke gegevensdiscrepanties toe te schrijven aan misconfiguration. Ontbreekt u rijen? Zo ja, welke rijen ontbreken en waarom? Hebt u verbindingen verkeerd gevormd en ontbrekende gegevens in Customer Journey Analytics veroorzaakt?
* Krijg inzicht in gebruik van ingeklapte en te melden rijen over al uw verbindingen.

[!UICONTROL Connections] heeft twee interfaces: [[!UICONTROL List]](#list) en [[!UICONTROL Usage]](#usage).


## Lijst

De [!UICONTROL List] interface is de standaardinterface voor Verbindingen. Als deze optie niet is geselecteerd, selecteert u **[!UICONTROL List]** om de interface te openen.

De [!UICONTROL List] de interface toont een lijst van alle beschikbare verbindingen. U kunt snel naar een verbinding zoeken met de zoekfunctie ![Zoeken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) doos.

De volgende kolommen/pictogrammen zijn beschikbaar in de tabel.

| Kolom/pictogram | Beschrijving |
| --- | --- |
| [!UICONTROL Name] | De vriendelijke naam van de verbinding. Als u de details van de verbinding wilt zien, selecteert u de naam van de hyperlink. Zie [Verbindingsgegevens](#connection-details). |
| ![Informatie](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) | Informatie weergeven over [!UICONTROL Datasets included], [!UICONTROL Sandbox], [!UICONTROL Owner]en meer selecteert u ![Informatie](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) naast de verbindingsnaam.<p>Een popup venster toont details. <p><img src="./assets/conn-info.png" alt="Verbindingsgegevens weergeven" width="400"/> |
| ![Gegevens, weergave](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) | Naar [een gegevensweergave maken](#create-a-data-view) voor de verbinding selecteert u ![Gegevens, weergave](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) . Dit pictogram wordt alleen weergegeven wanneer er al geen gegevensweergave is gekoppeld aan de verbinding. |
| ![Meer](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) | Selecteren ![Meer](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) tot: <p>![Bewerken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) [Bewerken](#edit-a-connection) een verbinding.<p>![Verwijderen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) [Verwijderen](#delete-a-connection) een verbinding.<p>![Gegevens, weergave](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) [Nieuwe gegevensweergave maken](#create-a-data-view). Gebruik dit om extra gegevensmeningen voor de verbinding tot stand te brengen. |
| [!UICONTROL Datasets] | Toont één of meerdere verbindingen aan de datasets die deel van de verbinding uitmaken. U kunt de datasethyperlink selecteren om de dataset in de verbinding te bekijken. Als meer datasets deel van de geselecteerde verbinding uitmaken, selecteer **[!UICONTROL +*x *meer]**om een **[!UICONTROL Datasets included]**deelvenster. Dit paneel toont verbindingen aan alle datasets en een optie om naar een specifieke dataset te zoeken die deel van de verbinding uitmaakt.<p><img src="./assets/datasets-included.png" alt="Bijbehorende gegevenselementen" width="400"/><p>Het selecteren van een datasetnaam opent de dataset in Experience Platform UI in een nieuw lusje. |
| [!UICONTROL Sandbox] | Hiermee wordt het dialoogvenster [Experience Platform sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=nl) waarvan deze verbinding zijn datasets trekt. Deze sandbox werd geselecteerd toen u de verbinding voor het eerst maakte. Het kan niet worden gewijzigd. |
| [!UICONTROL Owner] | De persoon die de verbinding heeft gemaakt. |
| [!UICONTROL Import new data] | Toont het statuut van het invoeren van nieuwe gegevens voor datasets: <p><span style="color:green">●</span>   **[!UICONTROL _x _Aan]**voor hoeveel datasets worden gevormd om nieuwe gegevens in te voeren, en&lt;/<p><span style="color:gray">●</span>   **[!UICONTROL _x uit_]** voor hoeveel datasets de nieuwe gegevensimport wordt uitgezet. |
| [!UICONTROL Date created] | De tijdstempel op het moment dat de verbinding werd gemaakt. |
| [!UICONTROL Last modified] | De tijdstempel wanneer de verbinding voor het laatst is bijgewerkt. |
| [!UICONTROL Backfill data] | Toont de status voor backfill gegevens over datasets.<p><span style="color:red">●</span>   **[!UICONTROL _x _backfills mislukt]**voor het aantal mislukte backfills in verschillende gegevensreeksen,<p><span style="color:orange">●</span>   **[!UICONTROL _x _backfills-verwerking]**voor het aantal verwerkingsbackfills over gegevensreeksen,<p><span style="color:green">●</span>   **[!UICONTROL _x _terugvullingen voltooid]**voor het aantal voltooide terugvullingen voor datasets, en<p><span style="color:grey">●</span>   **[!UICONTROL _Uit_]** als er geen backfills zijn gedefinieerd voor de gegevenssets in de verbinding. |

U kunt configureren welke kolommen u wilt weergeven ![Kolominstellingen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg). Dit toont de **Tabel aanpassen** waarmee u kolommen in de tabel kunt in- of uitschakelen.

### Een verbinding bewerken

Hiermee kunnen beheerders de verbinding bewerken.

1. Selecteren ![Meer](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) naast de verbindingsnaam
1. Selecteren ![Bewerken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit]** in het contextmenu.

U kunt ook:

1. Selecteer de verbindingsrij.

1. Selecteren ![Bewerken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit]** in de blauwe balk.

Wanneer u een verbinding bewerkt, kunt u:

* Nieuwe gegevens beginnen en stoppen.
* Wijzig de naam van een verbinding.
* Vernieuw de gegevensset(s).
* Verwijder dataset/s uit de verbindingen.

Zie [Verbinding maken of bewerken](create-connection.md) voor meer informatie .


### Een verbinding verwijderen {#connections-delete}

Hiermee kunnen beheerders de verbinding verwijderen.

1. Selecteren ![Meer](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) naast de verbindingsnaam.
1. Selecteren ![Verwijderen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Delete]**.

U kunt ook:

1. Selecteer de verbindingsrij.

1. Selecteren ![Verwijderen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Delete]** in de blauwe balk.

Wanneer u een verbinding verwijdert, wordt een **[!UICONTROL Delete connection]** geeft aan welke gegevensweergaven worden verwijderd en welke werkruimteprojecten worden beïnvloed.

<img src="./assets/delete-connection.png" alt="Verbinding verwijderen" width="400"/>

Selecteren **[!UICONTROL Continue]** om de verbinding te verwijderen.

Zie [Gevolgen verwijderen](/help/admin/cja-deletion.md) voor meer informatie over de gevolgen van het verwijderen van een verbinding.


### Een gegevensweergave maken

Hiermee kunnen beheerders een gegevensweergave voor de verbinding maken.

* Als er geen gegevensweergave is gekoppeld aan de verbinding:

   1. Selecteren ![Gegevensweergave toevoegen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) naast de verbindingsnaam.

* Als er al een of meer gegevensweergaven zijn gemaakt voor de verbinding:

   1. Selecteren ![Meer](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) naast de verbindingsnaam.
   1. Selecteren ![Gegevensweergave toevoegen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) **[!UICONTROL Create new data view]**.

U kunt ook:

1. Selecteer de verbindingsrij.

1. Selecteren ![Gegevensweergave toevoegen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) **[!UICONTROL Create data view]** in de blauwe knopbalk.

Zie [Een gegevensweergave maken of bewerken](/help/data-views/create-dataview.md) voor meer informatie .

### Verbindingsgegevens {#connection-detail}

Als u naar de gegevens voor een verbinding wilt gaan, selecteert u een verbindingsnaam in de tabel met verbindingen.

![Alle datasetvenster die widgets en montages tonen](assets/conn-details.png)

De interface van de Details van Verbindingen verstrekt een gedetailleerde mening van de status van een verbinding. U kunt:

* Controleer de status van de datasets van uw verbinding en van het innameproces.
* Identificeer configuratieproblemen die overgeslagen of geschrapte verslagen kunnen veroorzaken.
* Zie wanneer de gegevens beschikbaar zijn voor rapportage.

| Gebruikersinterface | Beschrijving |
| --- | --- |
| ![Bewerken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) [!UICONTROL Edit Connection] | Als u de gegevens van een verbinding wilt bewerken, selecteert u ![Bewerken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit Connection]** . Zie [Verbinding maken of bewerken](create-connection.md) voor meer informatie . |
| Gegevensset selecteren | Hiermee kunt u een of alle gegevenssets in de verbinding kiezen. U kunt geen datasets selecteren. Standaardwaarden: [!UICONTROL All datasets]. |
| Selector datumbereik | Begin- en/of einddatum bewerken of ![Kalender](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) om de gegevensbereikkiezer te openen. Selecteer in de datumbereikkiezer een datumbereik met een van de vooraf gedefinieerde punten (bijvoorbeeld **[!UICONTROL Last 6 months]**) of gebruik de kalender om de begin- en einddatum te selecteren. Selecteren **[!UICONTROL Apply]** om het nieuwe gegevensbereik toe te passen. |
| [!UICONTROL Records of event data available] | Vertegenwoordigt het totale aantal rijen van de gebeurtenisdataset beschikbaar voor rapportering, **voor de volledige verbinding**. Deze telling is onafhankelijk van enige kalendermontages. De telling verandert als u een dataset van de datasetselecteur selecteert of door een dataset in de lijst te selecteren. Als er gegevens zijn toegevoegd, is er een vertraging van 1-2 uur om de gegevens in de rapportage weer te geven. |
| [!UICONTROL Metrics] | Hiermee geeft u een overzicht van de gebeurtenisrecords die zijn toegevoegd/overgeslagen/verwijderd en het aantal toegevoegde batches, **voor de dataset en de datumwaaier u hebt geselecteerd**.<p>Selecteren **[!UICONTROL Check detail]** om de **[!UICONTROL Check skipped detail]** popup, een lijst van alle gebeurtenisdatasets of geselecteerde dataset het aantal overgeslagen verslagen en de reden.<p><img src="./assets/skipped-records.png" width="500"/><p>Selecteren ![Info](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) popup met meer informatie. Om sommige overgeslagen redenen, zoals [!UICONTROL Empty visitor ID], toont popup Steekproef PSQL voor EQS (Experience Platform voor de Dienst van de Vraag) u kunt gebruiken binnen [Query-service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl) om voor de overgeslagen verslagen in de dataset te vragen. Selecteren ![Kopiëren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Copy_18_N.svg) **[!UICONTROL Copy sample PSQL for EQS]** om de SQL te kopiëren. |
| [!UICONTROL Records added] | Geeft aan hoeveel rijen zijn toegevoegd in de geselecteerde tijdsperiode. **voor de dataset en de datumwaaier u hebt geselecteerd**. Om de 10 minuten bijgewerkt. |
| [!UICONTROL Records skipped] | Geeft aan hoeveel rijen zijn overgeslagen in de geselecteerde tijdsperiode. **voor de dataset en de datumwaaier u hebt geselecteerd**. Redenen voor het overslaan van records zijn onder andere: ontbrekende tijdstempels, ontbrekende of ongeldige personen-id enzovoort. Om de 10 minuten bijgewerkt. <p>Ongeldige personen-id&#39;s (zoals &quot;undefined&quot; of &quot;00000000&quot; of een willekeurige combinatie van cijfers en letters in een [!UICONTROL Person ID] die in een gebeurtenis meer dan 1 miljoen keer in een bepaalde maand voorkomt) kan niet aan een specifieke gebruiker of persoon worden toegeschreven. Ze kunnen niet in het systeem worden opgenomen en leiden tot foutgevoelige inname en rapportage. U kunt ongeldige personen-id&#39;s corrigeren aan de hand van drie opties:<ul><li>Gebruiken [Stiksel](/help/stitching/overview.md) om de ongedefinieerde of helemaal geen gebruikers-id te vullen met geldige gebruikers-id&#39;s.</li><li>Blanco de gebruikersnaam. Deze wordt overgeslagen tijdens inname (voorkeur boven ongeldige of geen gebruikersnaam).</li><li>Corrigeer eventuele ongeldige gebruikers-id&#39;s in uw systeem voordat u de gegevens opneemt.</li></ul> |
| [!UICONTROL Records] verwijderd | Geeft aan hoeveel rijen zijn verwijderd in de geselecteerde tijdsperiode. **voor de dataset en de datumwaaier u hebt geselecteerd**. Iemand heeft bijvoorbeeld een dataset in Experience Platform verwijderd. Om de 10 minuten bijgewerkt. |
| ![Zoeken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) _Naam of id van gegevensset zoeken_ | Veld voor het zoeken naar gegevenssets. U kunt de datasetlijst door datasetnaam zoeken of [!UICONTROL Dataset ID]. |
| [!UICONTROL Datasets table] | Toont de datasets die deel van de verbinding uitmaken. |
| [!UICONTROL Datasets] | Toont de naam van de dataset die deel van de verbinding uitmaakt. U kunt de hyperlink selecteren om de dataset in Experience Platform UI op een nieuw lusje te openen. U kunt de rij of checkbox selecteren om details voor de geselecteerde dataset slechts te tonen. |
| [!UICONTROL Dataset ID] | Automatisch gegenereerd door Experience Platform. |
| [!UICONTROL Records added] | Het aantal datasetverslagen/rijen die aan een verbinding tijdens het geselecteerde tijdinterval worden toegevoegd. |
| [!UICONTROL Records skipped] | Het aantal datasetverslagen/rijen die tijdens gegevensoverdracht voor een verbinding tijdens het geselecteerde tijdinterval worden overgeslagen. |
| [!UICONTROL Records deleted] | Het aantal datasetverslagen/rijen die uit een verbinding tijdens het geselecteerde tijdinterval worden verwijderd. |
| [!UICONTROL Batches added] | Het aantal gegevenssetbatches is toegevoegd aan een verbinding. |
| [!UICONTROL Last added] | De tijdstempel van de laatste batch uit de gegevensset die is toegevoegd aan een verbinding. |
| [!UICONTROL Data source type] | Het brontype van de dataset. U definieert het brontype wanneer u een verbinding maakt. |
| [!UICONTROL Dataset type] | Het gegevenstype van de dataset voor deze dataset. Type kan [!UICONTROL Event], [!UICONTROL Lookup], of [!UICONTROL Profile]. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html#configure-dataset) |
| Schema | Het schema van het Experience Platform waarop de dataset is gebaseerd. |
| [!UICONTROL Import new data] | Toont het statuut van het invoeren van nieuwe gegevens voor de dataset: <p><span style="color:green">●</span>   **[!UICONTROL _x _Aan]**als de dataset wordt gevormd om nieuwe gegevens in te voeren, en<p><span style="color:gray">●</span>   **[!UICONTROL _x uit_]** als de dataset wordt gevormd om nieuwe gegevensimport niet in te voeren. |
| [!UICONTROL Backfill data] | Toont het statuut van backfill gegevens voor de dataset.<p><span style="color:red">●</span>   **[!UICONTROL _x _backfills mislukt]**voor het aantal mislukte backfills,<p><span style="color:orange">●</span>   **[!UICONTROL _x _backfills-verwerking]**voor het aantal backfills-verwerkingen,<p><span style="color:green">●</span>   **[!UICONTROL _x _terugvullingen voltooid]**voor het aantal voltooide backfills, en<p><span style="color:grey">●</span>   **[!UICONTROL _Uit_]** als er geen backfills zijn geconfigureerd. |

>[!IMPORTANT]
>
>Gegevens die vóór 13 augustus 2021 zijn ingevoerd, worden niet weergegeven in de [!UICONTROL Connections] interface.

#### Deelvenster Verbinding

Wanneer geen dataset in de datasetlijst wordt geselecteerd, toont een paneel op de rechterkant van de interface van Verbindingen verbindingsopties en details.

| Opties/details | Beschrijving |
| --- | --- |
| ![Vernieuwen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) [!UICONTROL Refresh] | Als u de verbinding wilt vernieuwen en wilt toestaan dat recent toegevoegde records worden gereflecteerd, selecteert u ![Vernieuwen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) **[!UICONTROL Refresh]**. |
| ![Verwijderen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Delete]** | [Verwijderen](#delete-a-connection) deze verbinding. |
| ![Gegevensweergave toevoegen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataAdd_18_N.svg) **[!UICONTROL Create data view]** | [Een gegevensweergave maken](#create-a-data-view) op basis van deze verbinding. Zie [Gegevensweergaven](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html) voor meer informatie . |
| [!UICONTROL Connection name] | Toont de vriendschappelijke naam van de verbinding. |
| [!UICONTROL Connection description] | Toont een meer gedetailleerde beschrijving die het doel van deze verbinding beschrijft. |
| [!UICONTROL Sandbox] | De [Experience Platform sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=nl) van waaruit deze verbinding zijn dataset(s) trekt. Deze sandbox werd geselecteerd toen u de verbinding voor het eerst maakte. Het kan niet worden gewijzigd. |
| [!UICONTROL Connection ID] | Deze id wordt gegenereerd in Experience Platform. U kunt ![Kopiëren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Copy_18_N.svg) om de id te kopiëren. |
| [!UICONTROL Data views using connection] | Hier worden alle gegevensweergaven weergegeven die deze verbinding gebruiken. |
| [!UICONTROL Import new data] | Toont het statuut van het invoeren van nieuwe gegevens voor datasets: <p><span style="color:green">●</span>   **[!UICONTROL _x _Aan]**voor hoeveel datasets worden gevormd om nieuwe gegevens in te voeren, en<p><span style="color:gray">●</span>   **[!UICONTROL _x uit_]** voor hoeveel datasets de nieuwe gegevensimport wordt uitgezet. |
| [!UICONTROL Backfill data] | Toont het statuut van backfill gegevens voor datasets.<p><span style="color:red">●</span>   **[!UICONTROL _x _backfills mislukt]**voor het aantal mislukte backfills in verschillende gegevensreeksen,<p><span style="color:orange">●</span>   **[!UICONTROL _x _backfills-verwerking]**voor het aantal verwerkingsbackfills over gegevensreeksen,<p><span style="color:green">●</span>   **[!UICONTROL _x _terugvullingen voltooid]**voor het aantal voltooide terugvullingen voor datasets, en<p><span style="color:grey">●</span>   **[!UICONTROL _Uit_]** als er geen backfills zijn gedefinieerd voor de gegevenssets in de verbinding. |
| [!UICONTROL Created by] | Hiermee wordt de naam weergegeven van de persoon die de verbinding heeft gemaakt. |
| [!UICONTROL Last modified] | Hier wordt het tijdstempel van de laatste wijziging in de verbinding weergegeven. |
| [!UICONTROL Last modified by] | Toont de persoon die de verbinding het laatst heeft gewijzigd. |

#### Deelvenster Gegevensset

Wanneer een dataset in de datasetlijst wordt geselecteerd, toont een paneel op de rechterkant van de interface van Verbindingen details voor de geselecteerde dataset.

| Details | Beschrijving |
| --- | --- |
| [!UICONTROL Person ID] | Toont een identiteit die in het datasetschema in het Experience Platform werd bepaald. Dit is de persoon-id die u hebt geselecteerd tijdens het maken van de verbinding. Als u een verbinding creeert die datasets met verschillende IDs omvat, weerspiegelt het melden dat. Om datasets samen te voegen, moet u zelfde Persoon identiteitskaart over datasets gebruiken. |
| [!UICONTROL Key] | Toont de sleutel die u voor een raadplegingsdataset hebt gespecificeerd. |
| [!UICONTROL Matching Key] | Toont de passende sleutel die u voor een raadplegingsdataset hebt gespecificeerd. |
| [!UICONTROL Timestamp] | Toon timestamp voor een gebeurtenisdataset wordt bepaald die. |
| [!UICONTROL Records available] | Vertegenwoordigt het totale aantal rijen die voor deze dataset, voor de bepaalde tijdspanne worden opgenomen die door de kalender wordt geselecteerd. Er is geen latentie in termen van het krijgen van de gegevens om in rapportering te verschijnen, zodra het wordt toegevoegd. Wanneer u echter een gloednieuwe verbinding maakt, worden [latentie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html#3.-getting-data-into-customer-trip-analytics). |
| [!UICONTROL Records added] | Geeft aan hoeveel rijen zijn toegevoegd in de geselecteerde tijdsperiode. |
| [!UICONTROL Records deleted] | Hiermee wordt aangegeven hoeveel records tijdens de geselecteerde tijdsperiode zijn verwijderd. |
| [!UICONTROL Batches added] | Geeft aan hoeveel gegevensbatches zijn toegevoegd aan deze gegevensset. |
| [!UICONTROL Records skipped] | Hiermee geeft u aan hoeveel rijen zijn overgeslagen tijdens het invoeren in de geselecteerde tijdsperiode.<p>Redenen voor het overslaan van records zijn onder andere: ontbrekende tijdstempels, ontbrekende of ongeldige personen-id enzovoort. Om de 10 minuten bijgewerkt.<p>Ongeldige personen-id&#39;s (zoals &quot;undefined&quot; of &quot;00000000&quot; of een willekeurige combinatie van cijfers en letters in een [!UICONTROL Person ID] die in een gebeurtenis meer dan 1 miljoen keer in een bepaalde maand voorkomt) kan niet aan een specifieke gebruiker of persoon worden toegeschreven. Ze kunnen niet in het systeem worden opgenomen en leiden tot foutgevoelige inname en rapportage. U kunt ongeldige personen-id&#39;s corrigeren aan de hand van drie opties:<ul><li>Gebruiken [Stiksel](/help/stitching/overview.md) om de ongedefinieerde of helemaal geen gebruikers-id te vullen met geldige gebruikers-id&#39;s.</li><li>Maak de gebruikersnaam leeg, die vervolgens tijdens de inname wordt overgeslagen (bij voorkeur aan ongeldige of helemaal geen gebruikers-id&#39;s).</li><li>Corrigeer eventuele ongeldige gebruikers-id&#39;s in uw systeem voordat u de gegevens opneemt.</li></ul> |
| [!UICONTROL Last added] | Geeft aan wanneer de laatste batch is toegevoegd. |
| [!UICONTROL Import new data] | Toont het statuut van het invoeren van nieuwe gegevens voor de dataset: <p><span style="color:green">●</span>   **[!UICONTROL _x _Aan]**als de dataset wordt gevormd om nieuwe gegevens in te voeren, en<p><span style="color:gray">●</span>   **[!UICONTROL _x uit_]** als de dataset wordt gevormd om nieuwe gegevensimport niet in te voeren. |
| [!UICONTROL Backfill data] | Toont het statuut van backfill gegevens voor de dataset.<p><span style="color:red">●</span>   **[!UICONTROL _x _backfills mislukt]**voor het aantal mislukte backfills,<p><span style="color:orange">●</span>   **[!UICONTROL _x _backfills-verwerking]**voor het aantal backfills-verwerkingen,<p><span style="color:green">●</span>   **[!UICONTROL _x _terugvullingen voltooid]**voor het aantal voltooide backfills, en<p><span style="color:grey">●</span>   **[!UICONTROL _Uit_]** als er geen backfills zijn geconfigureerd.<p>Om een dialoog met een overzicht van de vroegere backfills voor de dataset te tonen, selecteer <img src="./assets/pastbackfill.svg" alt="Achtervullingen verleden" width="15"/> **[!UICONTROL Past backfills]**. |
| [!UICONTROL Data source type] | Het type van gegevensbron zoals bepaald toen het toevoegen van dataset aan de verbinding. |
| [!UICONTROL Dataset type] | Willekeurig [!UICONTROL Event], [!UICONTROL Lookup], of [!UICONTROL Profile]. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html#configure-dataset) |
| [!UICONTROL Schema] | Toont het schema van het Experience Platform dat deze dataset op gebaseerd is. |
| [!UICONTROL Dataset ID] | Deze dataset-id wordt gegenereerd in Experience Platform. |


## Gebruik

De [!UICONTROL Usage] de interface toont het gebruik van ingeklapte en te melden rijen over alle verbindingen. Deze interface steunt u om te bepalen of uw gebruik van de Customer Journey Analytics voldoet aan wat contractueel is overeengekomen.

Selecteer de **[!UICONTROL Usage]** om de interface te openen.

Over het gebruik rapporteren:

1. Selecteer een **[!UICONTROL Time range]**. U kunt kiezen tussen **[!UICONTROL Last 6 months]**, **[!UICONTROL Year to date]**, of **[!UICONTROL Last 2 Years]**.
1. Selecteer een **[!UICONTROL Interval]**. U kunt kiezen tussen **[!UICONTROL Monthly]** of **[!UICONTROL Quarterly]**.

Voor [!UICONTROL Ingested rows]:

* een vakje toont [!UICONTROL Total] Aantal opgenomen rijen.
* een vakje toont het aantal ingeklapte rijen voor [!UICONTROL Last month] en de wijziging in % (aangegeven met <span style="color:green">tij</span> of <span style="color:c64545">▼ ▼ M</span>) van de vorige maand.
* een lijngrafiek toont  <span style="color:53b2ad">◼︎</span> Cumulatieve ingeslikte rijen en <span style="color:4046c3">◼︎</span> Maandelijkse gegeneerde rijen.<br/>U kunt de muisaanwijzer boven elk gegevenspunt voor elke regel in de lijngrafiek plaatsen om een pop-up met datum en het aantal rijen voor het geselecteerde gegevenspunt weer te geven.


Voor [!UICONTROL Reportable rows]:

* een vak verschijnt [!UICONTROL Total] aantal te rapporteren rijen.
* een vak bevat het aantal te rapporteren rijen voor de [!UICONTROL Last month] en de wijziging in % (aangegeven met <span style="color:green">tij</span> of <span style="color:c64545">▼ ▼ M</span>) van de vorige maand.
* een lijngrafiek toont  <span style="color:53b2ad">◼︎</span> Gecumuleerde te rapporteren rijen en <span style="color:4046c3">◼︎</span> Maandelijkse te rapporteren rijen.<br/>U kunt de muisaanwijzer boven elk gegevenspunt voor elke regel in de lijngrafiek plaatsen om een pop-up met datum en het aantal rijen voor het geselecteerde gegevenspunt weer te geven.


>[!MORELIKETHIS]
>
>[Verbindingsinstellingen weergeven, problemen oplossen en wijzigen](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/connections/connections-details-experience-in-cja.html) zelfstudie.
