---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 22d3e7b8-4a4d-48a8-a98d-5172a9876286
source-git-commit: bb87226ee4b9acc433031f41997d403d49f48db3
workflow-type: tm+mt
source-wordcount: '1589'
ht-degree: 0%

---

# Verbinding maken en configureren voor gebruik met Customer Journey Analytics {#upgrade-create-connection}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-connection"
>title="Verbinding maken in Customer Journey Analytics"
>abstract="Met een verbinding kunt u gegevens van Adobe Experience Platform omzetten in een indeling die is geoptimaliseerd voor het rapporteren van Customers Journey Analytics. Het maken van een verbinding in de Customer Journey Analytics is eenvoudig, het duurt slechts een paar minuten om te voltooien."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/connections/create-connection.md -->

De volgende informatie verklaart hoe te om een verbinding tot stand te brengen en te vormen, evenals hoe te om Experience Platform datasets aan de verbinding toe te voegen u creeert. Voor extra informatie over het creëren van en het vormen van een verbinding, zie [ een verbinding ](/help/connections/create-connection.md) creëren of uitgeven.

## Verbinding maken en configureren {#create-connection}

1. Selecteer in Customer Journey Analytics de tab **[!UICONTROL Connections]** .
1. Selecteer **[!UICONTROL Create new connection]** .

   ![ Naamloze verbindingsmontages ](assets/create-conn1.png)

1. Configureer de verbindingsinstellingen.

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Connection name]** | Voer een unieke naam in voor de verbinding. |
   | **[!UICONTROL Connection description]** | Beschrijf het doel van deze verbinding. |
   | **[!UICONTROL Sandbox]** | Kies een sandbox in het Experience Platform die de gegevensset of gegevenssets bevat waarnaar u een verbinding wilt maken.<p>Adobe Experience Platform verstrekt [ zandbakken ](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) die één enkele instantie van het Platform in afzonderlijke virtuele milieu&#39;s verdelen helpen digitale ervaringstoepassingen ontwikkelen en evolueren. U kunt sandboxen zien als &#39;gegevenssilo&#39;s&#39; die gegevenssets bevatten. Sandboxen worden gebruikt om toegang tot datasets te controleren.<p>Als u de sandbox hebt geselecteerd, geeft de linkerrail alle gegevenssets in die sandbox weer waaruit u kunt trekken. |
   | **[!UICONTROL Enable rolling data window]** | Als u dit selectievakje inschakelt, kunt u de gegevensbewaring van de Customer Journey Analytics definiëren als een schuivend venster in maanden (1 maand, 3 maanden, 6 maanden enzovoort) op verbindingsniveau.<p>Het bewaren van gegevens is gebaseerd op de tijdstempels van de gebeurtenisdataset en is slechts op gebeurtenisdatasets van toepassing. Er bestaat geen instelling voor het schuivende gegevensvenster voor profiel- of opzoekgegevenssets, omdat er geen relevante tijdstempels zijn. Nochtans, als uw verbinding om het even welk profiel of raadplegingsdatasets (naast één of meerdere gebeurtenisdatasets) omvat, worden die gegevens bewaard voor de zelfde tijdspanne.<p> Het belangrijkste voordeel is dat u alleen gegevens opslaat of rapporteert die van toepassing zijn en nuttig zijn, en oudere gegevens verwijdert die niet meer nuttig zijn. Het helpt u onder uw contractgrenzen te blijven en vermindert het risico van overleeftijdskosten.<p>Als u de standaardinstelling (uitgeschakeld) verlaat, vervangt de bewaarinstelling voor Adobe Experience Platform-gegevens de bewaarperiode. Als je 25 maanden aan gegevens in Experience Platform hebt, krijgt Customer Journey Analytics 25 maanden aan gegevens door backfill. Als u 10 van die maanden in Platform schrapte, zou de Customer Journey Analytics de resterende 15 maanden behouden. |
   | **[!UICONTROL Add datasets]** (zie hieronder) | Voeg datasets toe als geen datasets in uw datasetlijst verschijnen. |
   | **[!UICONTROL Dataset name]** | Selecteer een of meer gegevenssets die u in de Customer Journey Analytics wilt opnemen en selecteer **[!UICONTROL Add]** .<p>(Als u veel datasets hebt waaruit u kunt kiezen, kunt u naar de juiste zoeken met behulp van de zoekbalk met zoekgegevens boven de lijst met gegevenssets.) |
   | **[!UICONTROL Last updated]** | Alleen voor gebeurtenisgegevenssets wordt deze instelling automatisch ingesteld op het standaardtijdstempelveld van op gebeurtenissen gebaseerde schema&#39;s in Experience Platform. &quot;N.v.t.&quot; betekent dat deze gegevensset geen gegevens bevat. |
   | **[!UICONTROL Number of records]** | The total records in the previous month for the dataset in Experience Platform. |
   | **[!UICONTROL Schema]** | Het [ die schema ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition) wordt gebaseerd waarop de dataset in Adobe Experience Platform werd gecreeerd. |
   | **[!UICONTROL Dataset type]** | Voor elke dataset die u aan deze verbinding toevoegde, plaatst de Customer Journey Analytics automatisch het datasettype dat op de gegevens wordt gebaseerd die binnen komen. Er zijn drie verschillende gegevenstypen: gebeurtenisgegevens, profielgegevens en opzoekgegevens. Zie de tabel hieronder voor een uitleg van de typen gegevenssets. |
   | **[!UICONTROL Granularity]** | De granulariteit van de gegevens in de gegevensset; alleen van toepassing voor samenvattende gegevenssets. |
   | **[!UICONTROL Data source type]** | Het gegevensbrontype van de dataset. Niet van toepassing voor samenvattende gegevensreeksen. |
   | **[!UICONTROL Person ID]** | Selecteer een persoon-id in de vervolgkeuzelijst met beschikbare identiteiten. Deze identiteiten werden bepaald in het datasetschema in het Experience Platform. Zie hieronder voor informatie over het gebruik van Identiteitskaart als Persoon identiteitskaart<p>BELANGRIJK: Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer personen-id&#39;s niet zijn gedefinieerd in het schema. Bekijk [ deze video ](https://www.youtube.com/watch?v=G_ttmGl_LRU) op hoe te om een identiteit in Experience Platform te bepalen. |
   | **[!UICONTROL Key]** | Alleen voor opzoekgegevenssets (zoals _id). |
   | **[!UICONTROL Matching Key]** | Alleen voor opzoekgegevenssets (zoals _id). |
   | **[!UICONTROL Import new data]** | Instellen op Aan of Uit. |
   | **[!UICONTROL Backfill data]** | U kunt verzoeken om de gegevens in een dataset terug te vullen. U kunt bijvoorbeeld een verzoek indienen om een back-up te maken van de gegevens van de laatste 7 dagen. Vorm correct de dataset en test uw verbinding. Als alles er goed uitziet, kunt u eenvoudig back-ups maken van alle resterende gegevens.<p>Bovendien kunt u de invoer van nieuwe gegevens door dataset toelaten. |
   | **[!UICONTROL Backfill status]** | Deze status geeft aan of er backfill-gegevens worden verwerkt. |

   {style="table-layout:auto"}

## Gegevenssets toevoegen en configureren {#add-dataset}

U kunt een gegevensset van het Experience Platform toevoegen wanneer u een verbinding creeert.

1. Selecteer **[!UICONTROL Add datasets]** in het dialoogvenster Verbindingsinstellingen.

1. In de stap [!UICONTROL Select datasets] ziet u een lijst met de gegevenssets voor Experience Platforms.

   ![ Uitgezochte datasets ](assets/select-datasets.png)

   Voor elke dataset, toont de lijst:

   | Kolom | Beschrijving |
   |---|---|
   | Gegevensset | Naam van de gegevensset. Selecteer de naam om u naar de dataset in Experience Platform te leiden. Selecteer ![ Info ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) om popup met meer details voor de dataset te tonen. U kunt **[!UICONTROL Edit in Platform]** selecteren om de dataset direct in Experience Platform uit te geven. |
   | Het type DataSet | Het type gegevensset: Event, Profile, Lookup of Summary. |
   | Aantal records | The total records in the previous month for the dataset in Experience Platform. |
   | Schema | Het schema voor de dataset. Selecteer de naam om u naar het schema in Experience Platform te leiden. |
   | Laatste batch | De status van de laatste batch die in het Experience Platform is opgenomen. Zie [ de staten van de Partij ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/batch/troubleshooting#batch-states) meer informatie. |
   | Dataset-id | De id van de gegevensset. |
   | Laatst bijgewerkt | De laatst bijgewerkte tijdstempel van de gegevensset. |


1. Selecteer een of meer gegevenssets en selecteer **[!UICONTROL Next]** . Minstens één gebeurtenisdataset moet deel van de verbinding uitmaken.
   * Om de kolommen te veranderen die voor de lijst van datasets worden getoond, selecteer ![ montages van de Kolom ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg) en selecteer de kolommen die in de [!UICONTROL Customize table] dialoog moeten worden getoond.
   * Om naar een specifieke dataset te zoeken, gebruik het ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) onderzoeksgebied van het 1} Onderzoek ![.
   * Om tussen het tonen of het verbergen van de geselecteerde datasets van een knevel te voorzien, selecteer ![ Uitgezochte ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SelectBoxAll_18_N.svg) **[!UICONTROL Hide selected]** of **[!UICONTROL Show selected]**.
   * Om een dataset uit de lijst van geselecteerde datasets te verwijderen, gebruik ![ dicht ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Close_18_N.svg). Als u alle geselecteerde gegevenssets wilt verwijderen, selecteert u **[!UICONTROL Clear all]** .




1. Nu, vorm de datasets één voor één.

   ![ vorm datasets ](assets/add-dataset.png)

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Person ID]** | Alleen beschikbaar voor gebeurtenis- en profielgegevenssets. Selecteer een persoon-id in de vervolgkeuzelijst met beschikbare identiteiten. Deze identiteiten werden bepaald in het datasetschema in het Experience Platform. Zie hieronder voor informatie over het gebruik van Identiteitskaart als Persoon identiteitskaart<p>Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer personen-id&#39;s niet zijn gedefinieerd in het schema. Zie [ identiteitsgebieden in UI ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie bepalen. <p>De waarde voor de geselecteerde persoon-id wordt als hoofdlettergevoelig beschouwd. `abc123` en `ABC123` zijn bijvoorbeeld twee verschillende waarden. |
   | **[!UICONTROL Timestamp]** | Alleen voor gebeurtenis- en samenvattingsgegevenssets wordt deze instelling automatisch ingesteld op het standaardtijdstempelveld van op gebeurtenissen gebaseerde schema&#39;s in Experience Platform. |
   | **[!UICONTROL Key]** | Alleen beschikbaar voor opzoekgegevenssets. De sleutel aan gebruik voor een dataset van de Opzoeken. |
   | **[!UICONTROL Matching key]** | Alleen beschikbaar voor opzoekgegevenssets. De passende sleutel om zich aan te sluiten in één van de gebeurtenisdatasets. Als deze lijst leeg is, hebt u waarschijnlijk geen gebeurtenisdataset toegevoegd of gevormd. |
   | **[!UICONTROL Timezone]** | Alleen beschikbaar voor samenvattingsgegevens. Selecteer de aangewezen tijdzone voor de tijdreekssummiere gegevens. |
   | **[!UICONTROL Data source type]** | Selecteer een type gegevensbron. <br/> de Types van gegevensbronnen omvatten: <ul><li>[!UICONTROL Web data]</li><li>[!UICONTROL Mobile App data]</li><li>[!UICONTROL POS data]</li><li>[!UICONTROL CRM data]</li><li>[!UICONTROL Survey data]</li><li>[!UICONTROL Call Center data]</li><li>[!UICONTROL Product data]</li><li> [!UICONTROL Accounts data]</li><li> [!UICONTROL Transaction data]</li><li>[!UICONTROL Customer Feedback data]</li><li> [!UICONTROL Other]</li></ul>Dit veld wordt gebruikt om de typen gebruikte gegevensbronnen te controleren. |
   | **[!UICONTROL Import new data]** | Schakel deze optie in als u een continue verbinding wilt maken. Met een lopende verbinding zijn de nieuwe gegevensbatches die aan de datasets worden toegevoegd automatisch beschikbaar in Workspace. |
   | **[!UICONTROL Dataset backfill]** | Schakel **[!UICONTROL Backfill all existing data]** in om ervoor te zorgen dat een back-up wordt gemaakt van alle bestaande gegevens.<br/><br/> selecteer **[!UICONTROL Request backfill]** om historische gegevens voor een specifieke periode terug te vullen. U kunt tot 10 periodes van de datasetbackfill bepalen.<ol><li>Bepaal de periode door begin en eindgegevens in te gaan of data te selecteren gebruikend ![ Kalender ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg).</li><li>Selecteer **[!UICONTROL Queue backfill]** om de backfill aan de lijst toe te voegen, of **[!UICONTROL Cancel]** om te annuleren.</li></ol>Voor elke ingang, uitgezocht ![ geef ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) uit om de periode uit te geven, of selecteer ![ Schrapping ](https://spectrum.adobe.com/static/icons/ui_18/CrossSize500.svg) om de ingang te schrappen.<br/><br/> op backfills:<ul><li>U kunt elke dataset afzonderlijk terugvullen.</li><li>U geeft voorrang aan nieuwe gegevens die aan een dataset in de verbinding worden toegevoegd, zodat heeft dit nieuwe gegeven de laagste latentie.</li><li>Alle backfill (historische) gegevens worden langzamer geïmporteerd. De hoeveelheid historische gegevens beïnvloedt de latentie.</li><li>De bronschakelaar van de Analyse voert tot 13 maanden van gegevens (ongeacht grootte) voor productiesandboxen in. De back-up van niet-productiesandboxen is beperkt tot 3 maanden.</li></ul> |
   | **[!UICONTROL Transform dataset]** | Voor specifieke B2B raadplegingsdatasets, kunt u de transformatie van een dataset voor juiste B2B op persoon-gebaseerde rapporteringsscenario&#39;s toelaten. |
   | **[!UICONTROL Backfill status]** | Mogelijke statusindicatoren zijn:<ul><li>Succes</li><li>X backfill(s) verwerken</li><li>Uit</li></ul> |
   | **[!UICONTROL Dataset ID]** | Deze id wordt automatisch gegenereerd. |
   | **[!UICONTROL Description]** | De beschrijving die aan deze dataset werd gegeven toen het werd gecreeerd. |
   | **[!UICONTROL Dataset size]** | De grootte van de gegevensset. |
   | **[!UICONTROL Schema]** | Het schema op basis waarvan de dataset in Adobe Experience Platform is gemaakt. |
   | **[!UICONTROL Dataset]** | De naam van de gegevensset. |
   | **[!UICONTROL Preview: *naam van de dataset *]** | Hiermee geeft u een voorvertoning weer van de gegevensset met datum, mijn id en de kolommen Id. |
   | **[!UICONTROL Remove]** | U kunt de dataset schrappen of verwijderen en identiteitskaart van de Persoon veranderen zonder de volledige verbinding te schrappen. Het schrappen of het verwijderen vermindert de kosten betrokken bij gegevensopname en het lastige proces om de volledige verbinding en bijbehorende gegevensmeningen opnieuw te creëren. |

   {style="table-layout:auto"}

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
