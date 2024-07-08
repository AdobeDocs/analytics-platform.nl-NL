---
title: Verbinding maken of bewerken
description: Beschrijft om een verbinding aan een dataset van de Experience Platform in Customer Journey Analytics tot stand te brengen of uit te geven.
exl-id: b4ac37ca-213b-4118-85e1-8e8f98553c6c
solution: Customer Journey Analytics
feature: Connections
role: Admin
source-git-commit: 8fe3fb966f559aa12f3203e02a1766436e45a24a
workflow-type: tm+mt
source-wordcount: '3029'
ht-degree: 1%

---

# Verbinding maken of bewerken

De verbindings verwezenlijking en geeft werkschemaervaring uit brengt alle dataset en montages van de verbindingsconfiguratie aan het centrum van het scherm met een hulpwerkschema uit. Het verstrekt gedetailleerde datasetselectie, configuratie, en overzichtservaring. En staat u toe om kritieke informatie zoals datasettype, grootte, schema, dataset identiteitskaart, partijstatus, backfill status, Persoon IDs, en veel meer te specificeren, om het risico van verkeerde verbindingsconfiguratie te verminderen. Hier volgt een overzicht van de mogelijkheden:

* U kunt het rollen venster van het gegevensbehoud toelaten wanneer u de verbinding creeert.
* U kunt datasets toevoegen aan en verwijderen uit een verbinding. (Als u een gegevensset verwijdert, wordt deze uit de verbinding verwijderd en worden de bijbehorende gegevensweergaven en onderliggende Analysis Workspace-projecten beïnvloed.)
* U kunt terugvullingsgegevens per dataset toelaten en verzoeken.
* U kunt datasets uitgeven, bijvoorbeeld om een andere backfill te verzoeken.
* U kunt bestaande gegevens per dataset importeren.

>[!VIDEO](https://video.tv.adobe.com/v/343044/?quality=12&learn=on)

## Vereisten

Het maximumaantal datasets u aan een verbinding kunt toevoegen wordt beperkt tot 100. De mix is afhankelijk van het Customer Journey Analytics dat uw bedrijf heeft aangeschaft.

Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

| **Selecteren** package | **Stichting** package |
| --- | --- |
| Om het even welke combinatie gebeurtenis/profiel/raadplegingsdatasets, die tot 100 optellen | Eén gebeurtenisgegevensset per verbinding |
|  | Maximaal 99 profiel- of opzoekgegevenssets per verbinding |

{style="table-layout:auto"}

## Verbinding maken en configureren {#create-connection}

1. Selecteer in Customer Journey Analytics de optie **[!UICONTROL Connections]** tab.
1. Selecteren **[!UICONTROL Create new connection]**.

   ![Naamloze verbindingsinstellingen](assets/create-conn1.png)

1. Configureer de verbindingsinstellingen.

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Connection name]** | Voer een unieke naam in voor de verbinding. |
   | **[!UICONTROL Connection description]** | Beschrijf het doel van deze verbinding. |
   | **[!UICONTROL Sandbox]** | Kies een sandbox in het Experience Platform die de gegevensset of gegevenssets bevat waarnaar u een verbinding wilt maken.<p>Adobe Experience Platform biedt [sandboxs](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) waarmee één platforminstantie wordt gepartitionaliseerd in afzonderlijke virtuele omgevingen om zo toepassingen voor een digitale ervaring te helpen ontwikkelen en evolueren. U kunt sandboxen zien als &#39;gegevenssilo&#39;s&#39; die gegevenssets bevatten. Sandboxs worden gebruikt om de toegang tot gegevenssets te beheren.<p>Nadat u de sandbox hebt geselecteerd, worden in het linkerpaneel alle gegevenssets in die sandbox weergegeven waaruit u kunt halen. |
   | **[!UICONTROL Enable rolling data window]** | Als u dit selectievakje inschakelt, kunt u de gegevensbewaring van de Customer Journey Analytics definiëren als een schuivend venster in maanden (1 maand, 3 maanden, 6 maanden enzovoort) op verbindingsniveau.<p>Het behoud van gegevens is gebaseerd op tijdstempels van de gebeurtenisdataset en is alleen van toepassing op datasets van gebeurtenissen. Er bestaat geen instelling voor het schuivende gegevensvenster voor profiel- of opzoekgegevenssets, omdat er geen relevante tijdstempels zijn. Als uw verbinding echter profiel- of opzoekgegevenssets bevat (naast een of meer gebeurtenissensets), worden die gegevens gedurende dezelfde periode bewaard.<p> Het belangrijkste voordeel is dat u alleen gegevens opslaat of rapporteert die van toepassing zijn en nuttig zijn, en oudere gegevens verwijdert die niet meer nuttig zijn. Het helpt u onder uw contractgrenzen te blijven en vermindert het risico van overage kosten.<p>Als u de standaardinstelling (uitgeschakeld) verlaat, wordt de bewaarperiode vervangen door de bewaarinstelling voor Adobe Experience Platform-gegevens. Als je 25 maanden aan gegevens in Experience Platform hebt, krijgt Customer Journey Analytics 25 maanden aan gegevens door backfill. Als u 10 van die maanden in Platform schrapte, zou de Customer Journey Analytics de resterende 15 maanden behouden. |
   | **[!UICONTROL Add datasets]** (zie hieronder) | Voeg datasets toe als geen datasets in uw datasetlijst verschijnen. |
   | **[!UICONTROL Dataset name]** | Selecteer één of meerdere datasets die u in Customer Journey Analytics wilt trekken en selecteren **[!UICONTROL Add]**.<p>(Als u uit veel gegevenssets kunt kiezen, kunt u zoeken naar de juiste gegevensset met behulp van de zoekbalk voor gegevenssets boven de lijst met gegevenssets.) |
   | **[!UICONTROL Last updated]** | Alleen voor gebeurtenisgegevenssets wordt deze instelling automatisch ingesteld op het standaardtijdstempelveld vanuit op gebeurtenissen gebaseerde schema&#39;s in Experience Platform. &quot;N.v.t.&quot; betekent dat deze gegevensset geen gegevens bevat. |
   | **[!UICONTROL Schema]** | De [schema](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition) op basis waarvan de gegevensset in Adobe Experience Platform is gemaakt. |
   | **[!UICONTROL Dataset type]** | Voor elke dataset die u aan deze verbinding toevoegde, plaatst de Customer Journey Analytics automatisch het datasettype dat op de gegevens wordt gebaseerd die binnen komen. Er zijn drie verschillende gegevenstypen: gebeurtenisgegevens, profielgegevens en opzoekgegevens. Zie de tabel hieronder voor een uitleg van de typen gegevenssets. |
   | **[!UICONTROL Person ID]** | Selecteer een persoon-id in de vervolgkeuzelijst met beschikbare identiteiten. Deze identiteiten werden bepaald in het datasetschema in het Experience Platform. Zie hieronder voor informatie over het gebruik van Identiteitskaart als Persoon identiteitskaart<p>BELANGRIJK: Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer personen-id&#39;s niet zijn gedefinieerd in het schema. Weergave [deze video](https://www.youtube.com/watch?v=G_ttmGl_LRU) over het definiëren van een identiteit in Experience Platform. |
   | **[!UICONTROL Key]** | Alleen voor opzoekgegevenssets (zoals _id). |
   | **[!UICONTROL Matching Key]** | Alleen voor opzoekgegevenssets (zoals _id). |
   | **[!UICONTROL Import new data]** | Instellen op Aan of Uit. |
   | **[!UICONTROL Backfill data]** | U kunt verzoeken om back-up te maken van de gegevens in een gegevensset op basis van tijdstempels van gebeurtenissen. U kunt bijvoorbeeld een verzoek indienen om een back-up te maken van de gegevens van de laatste 7 dagen. Vorm juiste Persoon identiteitskaart en test uw verbinding. Als alles er goed uitziet, kunt u eenvoudig back-ups maken van alle resterende gegevens.<p>Bovendien kunt u de invoer van nieuwe gegevens door dataset toelaten. |
   | **[!UICONTROL Backfill status]** | Deze status geeft aan of er backfill-gegevens worden verwerkt. |

   {style="table-layout:auto"}

## Gegevenssets toevoegen en configureren {#add-dataset}

Met de nieuwe workflow kunt u een gegevensset voor Experience Platforms toevoegen wanneer u een verbinding maakt.

1. Selecteer in het dialoogvenster Verbindingsinstellingen **[!UICONTROL Add datasets]**.

1. In de [!UICONTROL Select datasets] stap, ziet u een lijst van de datasets van het Experience Platform.

   ![Gegevenssets selecteren](assets/select-datasets.png)

   Voor elke dataset, toont de lijst:

   | Kolom | Beschrijving |
   |---|---|
   | Gegevensset | Naam van de gegevensset. Selecteer de naam om u naar de dataset in Experience Platform te leiden. Selecteren ![Info](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) om popup met meer details voor de dataset te tonen. In de pop-up kunt u selecteren **[!UICONTROL Edit in Platform]** om de dataset direct in Experience Platform uit te geven. |
   | Het type DataSet | Het type gegevensset: Gebeurtenis, Profiel of Opzoeken. |
   | Aantal records | The total records in the previous month for the dataset in Experience Platform. |
   | Schema | Het schema waarop de dataset is gebaseerd. Selecteer de naam om u naar het schema in Experience Platform te leiden. |
   | Laatste batch | De status van de laatste batch die in het Experience Platform is opgenomen. Zie [Batchstaten](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/batch/troubleshooting#batch-states) meer informatie . |
   | Dataset-id | De id van de gegevensset. |
   | Laatst bijgewerkt | De laatst bijgewerkte tijdstempel van de gegevensset. |


1. Selecteer een of meer datasets en selecteer **[!UICONTROL Next]**. Minstens één gebeurtenisdataset moet deel van de verbinding uitmaken.
   * Als u de kolommen wilt wijzigen die worden weergegeven voor de lijst met gegevenssets, selecteert u ![Kolominstellingen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg) en selecteer de kolommen die moeten worden weergegeven in het dialoogvenster [!UICONTROL Customize table] in.
   * Om naar een specifieke dataset te zoeken, gebruik ![Zoeken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) zoekveld.
   * Selecteer ![Selecteren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SelectBoxAll_18_N.svg) **[!UICONTROL Hide selected]** of **[!UICONTROL Show selected]**.
   * Om een dataset uit de lijst van geselecteerde datasets te verwijderen, gebruik ![Sluiten](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Close_18_N.svg). Als u alle geselecteerde gegevenssets wilt verwijderen, selecteert u **[!UICONTROL Clear all]**.




1. Nu, vorm de datasets één voor één.

   ![Gegevenssets configureren](assets/add-dataset.png)

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Person ID]** | Alleen beschikbaar voor gebeurtenis- en profieldatasets. Selecteer een persoon-id in de vervolgkeuzelijst met beschikbare identiteiten. Deze identiteiten werden bepaald in het datasetschema in het Experience Platform. Zie hieronder voor informatie over het gebruik van Identiteitskaart als Persoon ID.<p>Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer persoon-id&#39;s niet zijn gedefinieerd in het schema. Zie [Identiteitsvelden definiëren in de gebruikersinterface](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie . <p>De waarde voor de geselecteerde persoon-id wordt als hoofdlettergevoelig beschouwd. Bijvoorbeeld: `abc123` en `ABC123` Dit zijn twee verschillende waarden. |
   | **[!UICONTROL Timestamp]** | Alleen voor gebeurtenisgegevenssets wordt deze instelling automatisch ingesteld op het standaardtijdstempelveld van op gebeurtenissen gebaseerde schema&#39;s in Experience Platform. |
   | **[!UICONTROL Key]** | Alleen beschikbaar voor opzoekgegevenssets. De sleutel aan gebruik voor een dataset van de Opzoeken. |
   | **[!UICONTROL Matching key]** | Alleen beschikbaar voor opzoekgegevenssets. De passende sleutel om zich aan te sluiten in één van de gebeurtenisdatasets. Als deze lijst leeg is, hebt u waarschijnlijk geen gebeurtenisdataset toegevoegd of gevormd. |
   | **[!UICONTROL Data source type]** | Selecteer een type gegevensbron. <br/>Tot de typen gegevensbronnen behoren: <ul><li>[!UICONTROL Web data]</li><li>[!UICONTROL Mobile App data]</li><li>[!UICONTROL POS data]</li><li>[!UICONTROL CRM data]</li><li>[!UICONTROL Survey data]</li><li>[!UICONTROL Call Center data]</li><li>[!UICONTROL Product data]</li><li> [!UICONTROL Accounts data]</li><li> [!UICONTROL Transaction data]</li><li>[!UICONTROL Customer Feedback data]</li><li> [!UICONTROL Other]</li></ul>Dit veld wordt gebruikt om de typen gebruikte gegevensbronnen te controleren. |
   | **[!UICONTROL Import new data]** | Selecteer deze optie als u een aan de gang zijnde verbinding wilt vestigen, zodat om het even welke nieuwe gegevensbatches die aan de datasets in deze verbinding worden toegevoegd automatisch in Workspace stromen. Kan worden ingesteld op [!UICONTROL On] of [!UICONTROL Off]. |
   | **[!UICONTROL Dataset backfill]** | Inschakelen **[!UICONTROL Backfill all existing data]** om ervoor te zorgen dat er een back-up wordt gemaakt van alle bestaande gegevens.<br/><br/>Selecteren **[!UICONTROL Request backfill]** historische gegevens voor een bepaalde periode te herstellen. U kunt tot 10 periodes van de datasetbackfill bepalen.<ol><li>De periode definiëren door begin- en eindgegevens in te voeren of datums te selecteren ![Kalender](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg).</li><li>Selecteren **[!UICONTROL Queue backfill]** om de backfill aan de lijst toe te voegen, of **[!UICONTROL Cancel]** om te annuleren.</li></ol>Selecteer voor elk item ![Bewerken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) om de punt te bewerken of selecteer ![Verwijderen](https://spectrum.adobe.com/static/icons/ui_18/CrossSize500.svg) om de vermelding te verwijderen.<br/><br/>Op terugvullingen:<ul><li>U kunt elke dataset afzonderlijk terugvullen.</li><li>U geeft voorrang aan nieuwe gegevens die aan een dataset in de verbinding worden toegevoegd, zodat heeft dit nieuwe gegeven de laagste latentie.</li><li>Alle backfill (historische) gegevens worden langzamer geïmporteerd. De latentie wordt beïnvloed door hoeveel historische gegevens u hebt.</li><li>De bronschakelaar van de Analyse voert tot 13 maanden van gegevens (ongeacht grootte) voor productiesandboxen in. De back-up van niet-productiesandboxen is beperkt tot 3 maanden.</li></ul> |
   | **[!UICONTROL Transform dataset]** | Voor specifieke B2B raadplegingsdatasets kunt u de transformatie van een dataset voor juiste B2B op persoon-gebaseerde rapporteringsscenario&#39;s toelaten. Zie [Gegevenssets transformeren voor B2B-zoekopdrachten](transform-datasets-b2b-lookups.md) voor meer informatie . |
   | **[!UICONTROL Backfill status]** | Mogelijke statusindicatoren zijn:<ul><li>Succes</li><li>X backfill(s) verwerken</li><li>Uit</li></ul> |
   | **[!UICONTROL Dataset ID]** | Deze id wordt automatisch gegenereerd. |
   | **[!UICONTROL Description]** | De beschrijving die aan deze dataset werd gegeven toen het werd gecreeerd. |
   | **[!UICONTROL Dataset size]** | De grootte van de gegevensset. |
   | **[!UICONTROL Schema]** | Het schema op basis waarvan de dataset in Adobe Experience Platform is gemaakt. |
   | **[!UICONTROL Dataset]** | De naam van de gegevensset. |
   | **[!UICONTROL Preview: *naam gegevensset *]** | Hiermee geeft u een voorvertoning weer van de gegevensset met datum, mijn id en de kolommen Id. |
   | **[!UICONTROL Remove]** | U kunt de dataset schrappen of verwijderen en identiteitskaart van de Persoon veranderen zonder de volledige verbinding te schrappen. Het schrappen of het verwijderen vermindert de kosten betrokken bij gegevensopname en het lastige proces om de volledige verbinding en bijbehorende gegevensmeningen opnieuw te creëren. |

   {style="table-layout:auto"}

## Verbindingsvoorbeeld {#preview}

Selecteer **[!UICONTROL Connection preview]** in het dialoogvenster Verbindingsinstellingen.

![Voorvertoning van verbinding](assets/create-conn4.png)

Dit voorbeeld bevat enkele kolommen met informatie over de verbindingsconfiguratie. Welke kolomtypen worden weergegeven, hangt af van uw individuele gegevenssets.

## Typen gegevenssets {#dataset-types}

Voor elke gegevensset die u aan deze verbinding toevoegt, [!UICONTROL Customer Journey Analytics] wordt het type gegevensset automatisch ingesteld op basis van de binnenkomende gegevens.

>[!IMPORTANT]
>
>Voeg ten minste één gebeurtenisgegevensset toe als onderdeel van een verbinding.

Er zijn drie verschillende typen gegevenssets: [!UICONTROL Event] gegevens, [!UICONTROL Profile] gegevens en [!UICONTROL Lookup] gegevens.

| Type gegevensset | Beschrijving | Tijdstempel | Schema | Persoon-id |
|---|---|---|---|---|
| **[!UICONTROL Event]** | Gegevens die gebeurtenissen in de tijd vertegenwoordigen (bijvoorbeeld webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, impressiedata, enzovoort). Deze gegevens kunnen bijvoorbeeld standaardgegevens van een klikstream zijn, met een klant-id of een cookie-id en een tijdstempel. Bij Gebeurtenisgegevens hebt u enige flexibiliteit met betrekking tot de id die wordt gebruikt als de Person-id. | Automatisch instellen op het standaardtijdstempelveld vanuit op gebeurtenissen gebaseerde schema&#39;s in [!UICONTROL Experience Platform]. | Een ingebouwd of aangepast schema dat is gebaseerd op een XDM-klasse met het gedrag &quot;Tijdreeks&quot;. Voorbeelden zijn &quot;XDM Experience Event&quot; of &quot;XDM Decision Event&quot;. | U kunt kiezen welke persoon-id u wilt opnemen. Voor elk datasetschema dat in het Experience Platform is gedefinieerd, kan een eigen set met een of meer identiteiten worden gedefinieerd en aan een naamruimte zijn gekoppeld. Al deze identiteiten kunnen worden gebruikt als de persoon-id. Voorbeelden zijn Koekjescode-id, Stitched ID, Gebruikers-ID, Trackingcode enzovoort. |
| **[!UICONTROL Lookup]** | U kunt nu gegevenssets toevoegen als zoekopdrachten van velden binnen alle typen gegevenssets: Profiel, Opzoeken en Gebeurtenisgegevenssets (deze laatste werden altijd ondersteund). Deze extra capaciteit breidt de capaciteit van CJA uit om complexe gegevensmodellen, met inbegrip van B2B CDP te steunen. Deze gegevens worden gebruikt om waarden of sleutels op te zoeken die in uw Gebeurtenis, Profiel, of de gegevens van de Opzoeken worden gevonden. U kunt maximaal twee niveaus opzoeken. (Let op: [Afgeleide velden](/help/data-views/derived-fields/derived-fields.md) kan niet worden gebruikt als overeenkomende sleutels voor zoekopdrachten binnen verbindingen.) U kunt bijvoorbeeld opzoekgegevens uploaden waarmee u numerieke id&#39;s in uw gebeurtenisgegevens toewijst aan productnamen. Zie [B2B-gebruiksgeval](/help/use-cases/b2b/b2b.md) bijvoorbeeld. | N.v.t. | Een ingebouwd of aangepast schema dat is gebaseerd op een XDM-klasse met het gedrag &quot;Record&quot;, behalve de klasse &quot;XDM Individual Profile&quot;. | N.v.t. |
| **[!UICONTROL Profile]** | Gegevens die worden toegepast op uw personen, gebruikers of klanten in de [!UICONTROL Event] gegevens. Staat u bijvoorbeeld toe om CRM-gegevens over uw klanten te uploaden. | N.v.t. | Een ingebouwd of aangepast schema dat is gebaseerd op de klasse &quot;XDM Individual Profile&quot;. | U kunt kiezen welke persoon-id u wilt opnemen. Elke gegevensset die is gedefinieerd in het dialoogvenster [!DNL Experience Platform] heeft een eigen set van een of meer personen-id&#39;s gedefinieerd, bijvoorbeeld cookie-id, id met titel, gebruikers-id, code bijhouden enzovoort.<br>![Persoon-id ](assets/person-id.png)**Opmerking**: Als u een verbinding maakt die gegevenssets met verschillende id&#39;s bevat, geeft de rapportage dat aan. Als u gegevenssets wilt samenvoegen, moet u dezelfde persoon-id gebruiken. |

{style="table-layout:auto"}

## Numerieke velden gebruiken als opzoektoetsen en opzoekwaarden {#numeric}

Deze opzoekfunctionaliteit is handig als u een numeriek veld, zoals een kostenpost of marge, wilt toevoegen aan een sleutelveld op basis van een tekenreeks. Hiermee kunnen numerieke waarden als sleutels of als waarden in zoekopdrachten worden opgenomen. In uw raadplegingsschema, zou u numerieke waarden kunnen hebben verbonden aan, bijvoorbeeld, uw productnamen, COGS, de kosten van de campagne marketing, of marges. Hier volgt een voorbeeld van een opzoekschema in Adobe Experience Platform:

![Schema opzoeken](assets/schema.png)

U steunt nu het introduceren van deze waarden als metriek of dimensies in Customer Journey Analytics rapportering. Wanneer u opstelling uw verbinding en trekkracht in raadplegingsdatasets, kunt u de datasets uitgeven om te selecteren [!UICONTROL Key] en [!UICONTROL Matching Key]:

![Edit-dataset](assets/lookup-dataset.png)

Wanneer u een gegevensweergave instelt op basis van deze verbinding, voegt u de numerieke waarden als componenten toe aan de gegevensweergave. Elk project dat is gebaseerd op deze gegevensweergave, kan vervolgens over deze numerieke waarden rapporteren.

## Identiteitskaart gebruiken als persoon-id {#id-map}

De Customer Journey Analytics steunt de capaciteit om de Kaart van de Identiteit voor zijn identiteitskaart van de Persoon te gebruiken. Identiteitskaart is een structuur van kaartgegevens die u toestaat om sleutel -> waardeparen te uploaden. De sleutels zijn identiteitsnaamruimten en de waarde is een structuur die de identiteitswaarde bevat. De identiteitskaart bestaat op elke rij/gebeurtenis die wordt geüpload en wordt voor elke rij overeenkomstig gevuld.

De Kaart van de Identiteit is beschikbaar voor om het even welke dataset die een schema gebruikt dat op [ExperienceEvent XDM](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home) klasse. Wanneer u een dergelijke dataset selecteert die in een Verbinding van de Customer Journey Analytics moet worden omvat, hebt u de optie om of een gebied als primaire identiteitskaart of de Kaart van de Identiteit te selecteren:

![](assets/idmap1.png)

Als u Identiteitskaart selecteert, krijgt u twee extra configuratieopties:

| Optie | Beschrijving |
|---|---|
| **[!UICONTROL Use Primary ID Namespace]** | Met deze optie krijgt de Customer Journey Analytics de opdracht om per rij de identiteit te zoeken in het identiteitsoverzicht dat is gemarkeerd met een `primary=true` en gebruik die identiteit als Persoon identiteitskaart voor die rij. Deze identiteit is de primaire sleutel die in Experience Platform voor het verdelen wordt gebruikt. En deze identiteit is ook de eerste kandidaat voor gebruik als identiteitskaart van de Persoon van de Customer Journey Analytics (afhankelijk van hoe de dataset in een Verbinding van de Customer Journey Analytics wordt gevormd). |
| **[!UICONTROL Namespace]** | (Deze optie is alleen beschikbaar als u de primaire-id-naamruimte niet gebruikt.) Identiteitsnaamruimten zijn een component van de component [Experience Platform Identity Service](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces) die dienen als indicatoren van de context waarop een identiteit betrekking heeft. Als u een naamruimte opgeeft, zoekt de Customer Journey Analytics in elke rij naar Identiteitskaart voor deze naamruimtesleutel en gebruikt de identiteit onder die naamruimte als Persoon-id voor die rij. Aangezien de Customer Journey Analytics geen volledige datasetaftasten van alle rijen kan doen om te bepalen welke namespaces aanwezig zijn, worden alle mogelijke namespaces getoond in de drop-down lijst. Weet welke naamruimten in de gegevens zijn opgegeven; deze naamruimten worden niet automatisch gedetecteerd. |

{style="table-layout:auto"}

### Kwalen met de rand van Identity Map {#id-map-edge}

Deze lijst toont de twee configuratieopties wanneer de randgevallen aanwezig zijn en hoe zij worden behandeld:

| Optie | Er zijn geen id&#39;s aanwezig op de identiteitskaart | Meerdere id&#39;s, geen gemarkeerd als primair | Meerdere id&#39;s zijn gemarkeerd als primaire id | Eén id, al dan niet gemarkeerd als primair | Ongeldige naamruimte met een ID gemarkeerd als primair |
|---|---|---|---|---|---|
| **[!UICONTROL Use Primary ID Namespace]geruit** | Met Customer Journey Analytics wordt de rij gezet. | Bij Customer Journey Analytics wordt de rij weggezet, omdat er geen primaire id is opgegeven. | Alle id&#39;s die als primair zijn gemarkeerd in alle naamruimten, worden geëxtraheerd in een lijst. Ze worden dan alfabetisch gesorteerd; met de nieuwe sortering wordt de eerste naamruimte met de eerste id gebruikt als persoons-id. | De enkele id wordt gebruikt als persoons-id. | Hoewel de naamruimte ongeldig kan zijn (niet aanwezig in Adobe Experience Platform), gebruikt Customer Journey Analytics de primaire ID onder die naamruimte als de Persoon-id. |
| **[!UICONTROL Specific Identity Map namespace]uitverkoren** | Met Customer Journey Analytics wordt de rij gezet. | Alle id&#39;s onder de geselecteerde naamruimte worden geëxtraheerd naar een lijst en de eerste id wordt gebruikt als de persoon-id. | Alle id&#39;s onder de geselecteerde naamruimte worden geëxtraheerd naar een lijst en de eerste id wordt gebruikt als de persoon-id. | Alle id&#39;s onder de geselecteerde naamruimte worden geëxtraheerd naar een lijst en de eerste id wordt gebruikt als de Person-id. | Alle id&#39;s onder de geselecteerde naamruimte worden geëxtraheerd naar een lijst en de eerste id wordt gebruikt als de Person-id. (Alleen een geldige naamruimte kan tijdens het maken van de verbinding worden geselecteerd, zodat een ongeldige naamruimte/id niet kan worden gebruikt als Person-id.) |

{style="table-layout:auto"}

## Het gemiddelde aantal dagelijkse gebeurtenissen berekenen {#average-number}

Deze berekening wordt uitgevoerd voor elke dataset in de verbinding.

1. Ga naar [Adobe Experience Platform Query Services](https://experienceleague.adobe.com/en/docs/experience-platform/query/home) en maak een query.

   De query ziet er als volgt uit:

   ```
   Select AVG(A.total_events) from (Select DISTINCT COUNT (*) as total_events, date(TIMESTAMP) from analytics_demo_data GROUP BY 2 Having total_events>0) A;
   ```

   In dit voorbeeld is &quot;analytics_demo_data&quot; de naam van de dataset.

2. Om alle datasets te tonen die in Adobe Experience Platform bestaan, voer uit `Show Tables` query.


## Algorithmic pruning of large lookup datasets

Wanneer u een verbinding maakt, kunt u grote gegevenssets toevoegen voor zoekdoeleinden. Bijvoorbeeld, kan een dataset die een productcatalogus zo beschrijvende productinformatie vertegenwoordigt worden opgezocht wanneer het bouwen van rapporten en visualisaties. Een dergelijke grote opzoekgegevensset kan het maximum van 10 miljoen unieke opzoekingen overschrijden die momenteel zijn geïmplementeerd als een begeleidend document, waardoor extra gegevens worden overgeslagen.

U kunt een verzoek indienen om een algoritmische snoepbewerking uit een grote opzoekgegevensset uit te voeren. Deze algoritmische het snoeien houdt slechts gegevens in de raadplegingsdataset die de sleutels in uw gebeurtenisdataset aanpast. Op deze manier hoeft u niet de gehele onafgebroken opzoekgegevensset te laden. Oude of minder vaak gebruikte items worden verwijderd, wat een lichte invloed kan hebben op rapporten, maar aanzienlijke voordelen met zich meebrengt. Het algoritme kijkt terug 90 dagen en werkt wekelijks bij.

Neem contact op met het ondersteuningsteam voor Adoben voor meer informatie en om deze functie in te schakelen.
