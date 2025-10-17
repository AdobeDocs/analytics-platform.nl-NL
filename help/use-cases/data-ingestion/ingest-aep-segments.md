---
title: Experience Platform-publiek voorstellen en gebruiken
description: Verklaart hoe te om Experience Platform publiek in Customer Journey Analytics voor verdere analyse op te nemen en te gebruiken.
solution: Customer Journey Analytics
feature: Use Cases
exl-id: cb5a4f98-9869-4410-8df2-b2f2c1ee8c57
role: Admin
source-git-commit: a30b4286207eb72f7674bb4f6ba4cf0a1aecd280
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---

# Experience Platform-publiek voorstellen en gebruiken

In deze gebruikszaak wordt gezocht naar een voorlopige oplossing om Experience Platform-publiek in Customer Journey Analytics te krijgen. Dit publiek zou in de Bouwer van het Segment van Experience Platform, of Adobe Audience Manager, of andere hulpmiddelen kunnen gecreeerd zijn, en in het Profiel van de Klant in real time opgeslagen. Het publiek bestaat uit een set profiel-id&#39;s, samen met eventuele toepasselijke kenmerken, gebeurtenissen en meer. Je wilt die publieksgegevens naar Customer Journey Analytics brengen voor verdere analyse.

## Vereisten

* Toegang tot [&#x200B; Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home), specifiek in real time het Profiel van de Klant.
* De toegang om de schema&#39;s van Experience Platform [&#x200B; &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home) en [&#x200B; datasets &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview) tot stand te brengen en te beheren.
* Toegang tot [&#x200B; de Dienst van de Vraag van Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/home) (en de capaciteit om SQL te schrijven).
* Toegang tot een hulpmiddel dat sommige transformaties van gegevens kan uitvoeren.
* Toegang tot Customer Journey Analytics. U moet a [&#x200B; het productadmin van Customer Journey Analytics &#x200B;](/help/technotes/access-control.md) zijn om de verbindingen en de gegevensmeningen van Customer Journey Analytics tot stand te brengen en te wijzigen.
* [&#x200B; verifieer en toegang tot Experience Platform APIs (de Dienst API van de Catalogus en de Dienst API van de Segmentatie) &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication). U moet een project in de console van de Ontwikkelaar van de organisatie en de zandbak tot stand brengen en u verzekeren u de informatie hebt die wordt vereist om API vraag met succes voor te leggen.

## Stappen

De tussenoplossing omvat de volgende stappen:

1. [&#x200B; Uitgezochte publiek (UI van Experience Platform) &#x200B;](#select-audiences).
1. [&#x200B; creeer een profiel-toegelaten dataset (Experience Platform API) &#x200B;](#create-a-profile-enabled-dataset).
1. [&#x200B; het publiek van de Uitvoer (Experience Platform API) &#x200B;](#export-audiences).
1. [&#x200B; zet de output (UI van Experience Platform en meer) om &#x200B;](#transform-the-output).
1. [&#x200B; creeer een schema en dataset (Experience Platform UI) &#x200B;](#create-a-schema-and-dataset).
1. [&#x200B; voeg of geef een verbinding (Customer Journey Analytics UI) toe uit &#x200B;](#add-or-edit-a-connection).
1. [&#x200B; vorm een gegevensmening (Customer Journey Analytics UI) &#x200B;](#configure-a-data-view).
1. [&#x200B; Rapport en analyseer (Customer Journey Analytics UI) &#x200B;](#report-and-analyze).


### Soorten publiek selecteren

De oplossing begint met de identificatie van het publiek dat u in Customer Journey Analytics wilt innemen.

+++ Soorten publiek identificeren

In de gebruikersinterface van Experience Platform:

1. Selecteer **[!UICONTROL Customer]** > ![&#x200B; SegmentAudience &#x200B;](/help/assets/icons2/SegmentAudience.svg) **[!UICONTROL Audiences]**.
1. Selecteer **[!UICONTROL Browse]** en zoek naar het publiek dat u in Customer Journey Analytics wilt opnemen en gebruiken. Noteer **[!UICONTROL Audience Id]** voor elk publiek voor later gebruik.

   ![&#x200B; Soorten publiek &#x200B;](assets/audiences.png)

+++

### Een voor profielen geschikte dataset maken

U moet een dataset tot stand brengen die op het op kern-gebaseerde **[!UICONTROL XDM Individual Profile]** schema wordt gebaseerd. U kunt niet dat kern gebaseerd Individueel Profiel XDM als schema selecteren wanneer u een dataset in Experience Platform UI creeert. In plaats daarvan, gebruik de [&#x200B; Dienst API van de Catalogus om een dataset &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create#create-a-dataset) tot stand te brengen die op het `_xdm.context.profile__union` schema wordt gebaseerd.

+++ Gegevenssetaanvraag maken

#### Verzoek

```shell
curl -X POST \
  'https://platform.adobe.io/data/foundation/catalog/dataSets?requestDataSource=true' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {ORG_ID}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
   "name": "{DATASET_NAME}",
   "schemaRef": {
      "id": "_xdm.context.profile__union",
      "contentType": "application/vnd.adobe.xed+json;version=1"
   },
   "fileDescription": {
      "persistet": true,
      "containerFormat": "parquet",
      "format": "parquet"
   }
}'
```

Waarbij:

* `DATASET_NAME` is de vriendelijke naam van de dataset. Bijvoorbeeld `Segment Export Job Dataset for CJA` .

#### Antwoord

```json
["@/dataSets/{DATASET_ID}"]
```

Waarbij:

* `DATASET_ID` is de id van de gegevensset voor de gemaakte gegevensset.

+++

### Soorten publiek exporteren

Exporteer het geselecteerde publiek naar de gegevensset die u net hebt gemaakt. Gebruik de [&#x200B; Dienst API van de Segmentatie om een uitvoerbaan &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/export-jobs#create) tot stand te brengen die het publiek in de dataset verzendt.

+++ Aanvraag voor exporttaak

```shell
curl -X POST https://platform.adobe.io/data/core/ups/export/jobs \
 -H 'Authorization: Bearer {ACCESS_TOKEN}' \
 -H 'Content-Type: application/json' \
 -H 'x-gw-ims-org-id: {ORG_ID}' \
 -H 'x-api-key: {API_KEY}' \
 -H 'x-sandbox-name: {SANDBOX_NAME}' \
 -d '{
    "fields": "{COMMA_SEPARATED_LIST_OF_FULLY_QUALIFIED_FIELD_NAMES}",
    "filter": {
        "segments": [
            {
                "segmentId": "{AUDIENCE_ID_1}",
                "segmentNs": "ups",
                "status": [
                    "realized"
                ],
                "segmentId": "{AUDIENCE_ID_2}",
                "segmentNs": "ups",
                "status": [
                    "realized"
                ],
                "segmentId": "{AUDIENCE_ID_3}",
                "segmentNs": "ups",
                "status": [
                    "realized"
                ]             
             }
        ]
    },
    "destination":{
        "datasetId": "{DATASET_ID}",
        "segmentPerBatch": false
    },
    "schema":{
        "name": "_xdm.context.profile"
    }
}'
```

Wanneer

* `COMMA_SEPARATED_LIST_OF_FULLY_QUALIFIED_FIELD_NAMES` zou iets als `_demoemea.identification.core.ecid, _demoemea.identification.core.email, _demoemea.identification.core.phoneNumber, person.gender, person.name.firstName, person.name.lastName` kunnen zijn. Zorg ervoor dat u ten minste de relevante velden opneemt (zoals de persoon-id (e-mail)) die u wilt gebruiken in uw analyse van de reis van de klant.
* `AUDIENCE_ID_x` zijn de publiek-id&#39;s van het publiek dat u wilt exporteren.
* `DATASET_ID` is de dataset die u creeerde.


### Antwoord

```json
{
  "..."
  "id": "{EXPORT_JOB_ID}",
  "..."
}
```

Wanneer

* `EXPORT_JOB_ID` is de id van de exporttaak.


+++

Gebruik de [&#x200B; Dienst API van de Segmentatie om het statuut van de uitvoerbaan &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/export-jobs#get) te controleren.

+++ Een specifieke aanvraag voor een exporttaak ophalen

#### Verzoek

```shell
curl -X GET https://platform.adobe.io/data/core/ups/export/jobs/{EXPORT_JOB_ID} \
 -H 'Authorization: Bearer {ACCESS_TOKEN}' \
 -H 'x-gw-ims-org-id: {ORG_ID}' \
 -H 'x-api-key: {API_KEY}' \
 -H 'x-sandbox-name: {SANDBOX_NAME}'
```

#### Antwoord

```json
{
  "..."
  "id": "{EXPORT_JOB_ID}",
  "..."
  "status": "SUCCEEDED",
  "..."
}
```

+++

Nadat de uitvoerbaan is geslaagd, verifieer of de dataset met succes ingebedde partijen bevat.

+++ Invoerstatus controleren

In de gebruikersinterface van Experience Platform:

1. Selecteer **[!UICONTROL Data Management]** > ![&#x200B; Gegevens &#x200B;](/help/assets/icons2/Data.svg) **[!UICONTROL Datasets]**.
1. Selecteer de gegevensset die u hebt gemaakt, bijvoorbeeld: **[!UICONTROL Segment Export Job Dataset for CJA]** .

   ![&#x200B; de activiteit van de Dataset &#x200B;](assets/dataset-activity.png)

1. Verifieer de opgenomen partijen. Als de dataset ontbroken partijen bevat, gebruik **[!UICONTROL Data Management]** > ![&#x200B; Controle &#x200B;](/help/assets/icons2/Monitoring.svg) **[!UICONTROL Monitoring]** om te zien wat de reden is. U hebt bijvoorbeeld een veldnaam gebruikt die niet in het schema voorkomt.
1. Kopieer **[!UICONTROL Table name]** van de dataset. Bijvoorbeeld: **[!UICONTROL segment_export_job_dataset_for_cja]** .  U gebruikt die naam in de volgende stap.

+++


### De uitvoer transformeren

De gegevens in de gegevensset hebben niet de juiste indeling voor Customer Journey Analytics. Als u de gegevens wilt transformeren, gebruikt u de Experience Platform Query Service om de gegevens op te halen.

+++ SQL om geëxporteerde publieksgegevens op te halen

Gebruik een PSQL-client die verbinding maakt met de Experience Platform Query Service.

In de gebruikersinterface van Experience Platform:

1. Selecteer **[!UICONTROL Data Management]** > ![&#x200B; DataSearch &#x200B;](/help/assets/icons2/DataSearch.svg) **[!UICONTROL Queries]**.
1. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Credentials]**.

Gebruik de referenties om uw PSQL-client te configureren voor verbinding met de Customer Journey Analytics Query Service.

#### Query

Voer deze vraag uit om de publieksgegevens van de dataset terug te winnen:

```sql
SELECT ROW_NUMBER() OVER (ORDER BY key)::text as _id, personID, key as audienceMembershipId
FROM (
   SELECT {IDENTITY_TO_USE_AS_PERSON_ID} AS personID, explode(segmentMembership.ups)
   FROM {DATASET_TABLE_NAME}
)
WHERE value.status = 'realized' AND (key = '{AUDIENCE_ID_1}' OR key = 'AUDIENCE_ID_2' OR key = 'AUDIENCE_ID_3')
```

Waarbij:

* `IDENTITY_TO_USE_AS_PERSON_ID` is een van de velden die u hebt gedefinieerd als onderdeel van de exporttaak. Bijvoorbeeld: `_demoemea.identification.core.email` .
* `DATASET_TABLE_NAME` is de tabelnaam van de gegevensset.
* `AUDIENCE_ID_x` is het publiek dat u hebt gedefinieerd als onderdeel van de exporttaak. U moet deze doelgroepen opnieuw opgeven omdat de specificatie in de exporttaak een filter op rijniveau is. Die rij-vlakke filter keert profielen voor de gespecificeerde segmenten met alle segmentlidmaatschap voor elk van de profielen terug.


#### Resultaten

Het resultaat van de query, in JSON-indeling, moet er als volgt uitzien:

```json
[
   {
      "_id": "1",
      "personID": "{PERSON_ID_x}",
      "audienceMembershipId": "{AUDIENCE_ID_x}"
   },
   {
      "_id": "2",
      "personID": "PERSON_ID_y",
      "audienceMembershipId": "{AUDIENCE_ID_x}"
   }

]
```

Waarbij:

* `PERSON_ID_x` zijn de id-waarden voor de id die u als de persoon-id wilt gebruiken. `john.doe@gmail.com` bijvoorbeeld wanneer u e-mail gebruikt.
* `AUDIENCE_ID_x` zijn de publiek-id&#39;s.

+++

U moet deze JSON- gegevens omzetten om de huurdersnaam van het milieu toe te voegen en een gebruikersvriendelijkere naam voor het publiek te verstrekken.

+++ Transform JSON

De uiteindelijke JSON zou er als volgt moeten uitzien:

```json
[
   {
      "_id": "1",
      "personID": "{PERSON_ID_x}",
      "{TENANT_NAME}": {
         "audienceMembershipId": "{AUDIENCE_ID_x}",
         "audienceMembershipName": "{AUDIENCE_FRIENDLY_NAME_x}"
      }
  },
  {
      "_id": "2",
      "personID": "{PERSON_ID_y}",
      "{TENANT_NAME}": {
         "audienceMembershipId": "{AUDIENCE_ID_y}",
         "audienceMembershipName": "{AUDIENCE_FRIENDLY_NAME_y}"
      }
    }
  }

]
```

Waarbij:

* `TENANT_NAME` is de naam van de huurder. Bijvoorbeeld: `_demoemea` .
* `PERSON_ID_x` zijn de id-waarden voor de id die u als de persoon-id wilt gebruiken. `john.doe@gmail.com` bijvoorbeeld wanneer u e-mail gebruikt.
* `AUDIENCE_ID_x` zijn de publiek-id&#39;s.
* `AUDIENCE_FRIENDLY_NAME_x` zijn vriendelijke publieksnamen voor de doelgroepen. Bijvoorbeeld: `Luma - Blue+ Members` .

Gebruik uw favoriete gereedschap om de originele JSON om te zetten in deze indeling.

+++


### Een schema en gegevensset maken

Als u de getransformeerde JSON wilt gebruiken als geëxporteerde publieksgegevens in Customer Journey Analytics, moet u een speciaal schema maken.

+++ Schema maken

Het schema maken:

In de gebruikersinterface van Experience Platform:

1. Selecteer **[!UICONTROL Data Management]** > ![&#x200B; Schema &#x200B;](/help/assets/icons2/Schema.svg) **[!UICONTROL Schemas]**.
1. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create schema]**. Selecteer **[!UICONTROL Standard]** in de vervolgkeuzelijst.
1. Selecteer **[!UICONTROL Manual]** in het dialoogvenster **[!UICONTROL Create a schema]** en gebruik **[!UICONTROL Select]** om door te gaan.
1. In de wizard **[!UICONTROL Create schema]** voert u in de stap **[!UICONTROL Select a class]** de volgende handelingen uit:
   1. Selecteer **[!UICONTROL Individual Profile]**.
   1. Selecteer **[!UICONTROL Next]**.
1. In de wizard **[!UICONTROL Create schema]** voert u in de stap **[!UICONTROL Name and review]** de volgende handelingen uit:
   1. Voer een **[!UICONTROL Schema display name]** in. Bijvoorbeeld: `Audience Export for CJA Schema` .
   1. (optioneel) Voer een **[!UICONTROL Description]** in.
   1. Selecteer **[!UICONTROL Finish]**.
1. Stel uw schema zo in dat het een aangepaste veldgroep bevat (bijvoorbeeld **[!UICONTROL Audience Membership]** ) die twee velden met de naam **[!UICONTROL audienceMembershipId]** en **[!UICONTROL audienceMembershipName]** bevat.
1. Zorg ervoor dat het veld **[!UICONTROL personID]** een **[!UICONTROL Identity]** , **[!UICONTROL Primary Identity]** is en **[!UICONTROL Email]** heeft als de I **&#x200B; [!UICONTROL dentity namespace]**.

   ![&#x200B; Segment voor de uitvoer &#x200B;](assets/segment-for-export.png)

1. **[!UICONTROL Apply]** alle wijzigingen. Selecteer **[!UICONTROL Save]** om het schema op te slaan.

+++

Maak een dataset en gebruik die dataset om de getransformeerde JSON-gegevens in te voeren.

+++ Gegevensset maken en gegevens opnemen

In de gebruikersinterface van Experience Platform:

1. Selecteer **[!UICONTROL Data Management]** > ![&#x200B; Gegevens &#x200B;](/help/assets/icons2/Data.svg) **[!UICONTROL Datasets]**.
1. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create dataset]**.
1. Selecteer **[!UICONTROL Create dataset from schema]**.
1. In de wizard **[!UICONTROL Create dataset from schema]** voert u in de stap **[!UICONTROL Select schema]** de volgende handelingen uit:
   1. Selecteer het schema dat u zojuist hebt gemaakt. Bijvoorbeeld: **[!UICONTROL Audience Export for CJA Schema]** .
   1. Selecteer **[!UICONTROL Next]**.
1. In de wizard **[!UICONTROL Create dataset from schema]** voert u in de stap **[!UICONTROL Configure dataset]** de volgende handelingen uit:
   1. Voer een **[!UICONTROL Name]** in voor de gegevensset.
   1. (optioneel) Voer een **[!UICONTROL Description]** in voor de gegevensset.
   1. Selecteer **[!UICONTROL Finish]**.
1. In **[!UICONTROL Datasets]** > **[!UICONTROL _naam van de dataset_]**, sleep het getransformeerde JSON- gegevensdossier en laat vallen het dossier op **[!UICONTROL Drag and drop files]**. Met deze handeling wordt de opname van de geëxporteerde JSON-gegevens in de gegevensset gestart.
1. Verifieer de opgenomen partijen. Als de dataset ontbroken partijen bevat, gebruik **[!UICONTROL Data Management]** > ![&#x200B; Controle &#x200B;](/help/assets/icons2/Monitoring.svg) **[!UICONTROL Monitoring]** om te zien wat de reden is. U hebt bijvoorbeeld een veldnaam in de JSON gedefinieerd die niet in het schema bestaat.


+++

### Een verbinding toevoegen of bewerken

Zodra de getransformeerde JSON-gegevens met de publieksgegevens van Experience Platform zijn opgenomen, kunt u de gegevensset toevoegen aan een nieuwe of bestaande verbinding in Customer Journey Analytics.

+++ Gegevensset toevoegen aan verbinding

In de gebruikersinterface van Customer Journey Analytics:

1. Selecteer **[!UICONTROL Data Management]** > **[!UICONTROL Connections]** .
1. Maak een nieuwe verbinding/ Define **[!UICONTROL Connection settings]** en **[!UICONTROL Data settings]** . Of selecteer een bestaande verbinding en gebruik ![&#x200B; geeft &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit Connection]** uit om de verbinding uit te geven.
1. Selecteer ![&#x200B; DataAdd &#x200B;](/help/assets/icons/DataAdd.svg) **[!UICONTROL Add datasets]**.
1. Selecteer de dataset die u creeerde en waarin u de getransformeerde JSON gegevens opnam.
1. Vorm de dataset. Bijvoorbeeld:

   ![&#x200B; Verbinding - Dataset met uitgevoerde publieksgegevens &#x200B;](assets/connection-add-dataset.png)

1. **[!UICONTROL Save]** de verbinding.

+++

### Een gegevensweergave configureren

Configureer een gegevensweergave voor de verbinding die u net hebt gemaakt of bewerkt.

+++ publiekscomponenten definiëren

1. Selecteer **[!UICONTROL Data Management]** > **[!UICONTROL Data views]** .
1. Bewerk een bestaande gegevensweergave of maak een nieuwe gegevensweergave.
1. Controleer in het tabblad **[!UICONTROL Components]** van de gegevensweergave of **[!UICONTROL Audience Membership Id]** en **[!UICONTROL Audience Membership Name]** zijn toegevoegd als dimensie-componenten.

   ![&#x200B; de meningscomponenten van Gegevens &#x200B;](assets/dataview-components.png)

1. Selecteer **[!UICONTROL Save and Continue]** om de gegevensweergave op te slaan.

+++

### Rapport en analyse

Tot slot gebruikt u Analysis Workspace om gegevens over Experience Platform-doelgroepen te rapporteren in een of meer deelvensters waarin de gegevensweergave wordt gebruikt voor de lidmaatschapscomponenten voor het publiek, zoals `audienceMembershipId` , `audienceMembershipIdName` en `personID` .



<!--

## Step 1: Select audiences in Real-time Customer Profile {#audience}

Experience Platform [Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html) lets you see a holistic view of each individual customer by combining data from multiple channels, including online, offline, CRM, and third party. 

You likely already have audiences in RTCP that may have come from various sources. Select one or more audiences to ingest into Customer Journey Analytics. For example, WKND Fly Platinum and Gold Fly Club Members.




## Step 2: Create a Profile Union dataset for the export

In order to export the audience to a dataset that you can ingest in Customer Journey Analytics as profiles, create a dataset whose schema is a Profile [Union schema](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html#understanding-union-schemas).

Union schemas are composed of multiple schemas that share the same class and have been enabled for Profile. The union schema enables you to see an amalgamation of all of the fields contained within schemas sharing the same class. Real-time Customer Profile uses the union schema to create a holistic view of each individual customer.

## Step 3: Export an audience to the Profile Union dataset via API call {#export}

Before you can bring an audience into Customer Journey Analytics, you need to export it to an Adobe Experience Platform dataset. This can only be done using the Segmentation API, and specifically the [Export Jobs API Endpoint](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html). 

You can create an export job using the audience ID of your choice, and put the results in the Profile Union Adobe Experience Platform dataset you created in Step 2. Although you can export various attributes/events for the audience, you only need to export the specific profile ID field that matches the person ID field used in the Customer Journey Analytics connection you will be leveraging (see below in Step 5).

## Step 4: Edit the export output 

The results of the export job need to be transformed into a separate Profile dataset in order to be ingested into Customer Journey Analytics.  This transformation can be done with [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html), or another transformation tool of your choice. We only need the Profile ID (that will match the Person ID in Customer Journey Analytics) and one or more audience ID(s) to do the reporting in Customer Journey Analytics.

The standard export job, however, contains more data and so we need to edit this output to remove extraneous data, as well as move some things around.  Also, you need to create a schema/dataset first before you add the transformed data to it.

Here is an example of the export output in the Profile union dataset, **before** any editing:

![Unedited output](../assets/export-unedited.png)

Note the following:

* The audience ID is contained under `segmentmembership.ups.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.status`.
* The status has to be "realized", or "entered", but not "exited".

This is the format of the Profile dataset that you can send into Customer Journey Analytics.

![Edited output](../assets/export-edited.png)

Here are the data elements that need to be present:

* `_aresprodvalidation` string field: Refers to your Organization ID. Yours will be different.
* `personID` string field: This is the standard XDM schema field on Profile datasets to identity the person. Use the Profile ID from the export.
* `audienceMembershipId` string field: The audience ID from the export.  NOTE: This field can be named whatever you want (from your own schema).
* Add a friendly name for the audience (`audienceMembershipIdName`), such as

   ![Friendly audience name](../assets/audience-name.png)
   
* Add other audience metadata if you desire.

## Step 5: Add this Profile dataset to an existing connection in Customer Journey Analytics

You could [create a new connection](/help/connections/create-connection.md), but most customers will want to add the Profile dataset to an existing connection. The audience IDs "enrich" the existing data in Customer Journey Analytics.

## Step 6: Modify existing (or create new) Customer Journey Analytics data view

Add `audienceMembershipId`, `audienceMembershipIdName` and `personID` to the data view.

## Step 7: Report in Workspace

You can now report on `audienceMembershipId`, `audienceMembershipIdName` and `personID` in Workspace.

-->


## Aanvullende opmerkingen

* U moet dit proces uitvoeren op een reguliere cadence, zodat de publieksgegevens in Customer Journey Analytics voortdurend worden vernieuwd.
* U kunt meerdere soorten publiek importeren binnen één Customer Journey Analytics-verbinding. Dit vergroot de complexiteit van het proces, maar het is mogelijk. Dit werkt alleen als u enkele wijzigingen aanbrengt in het bovenstaande proces:
   1. Voer dit proces voor elk gewenst publiek in uw publieksinzameling binnen RTCP uit.
   1. Customer Journey Analytics ondersteunt arrays/objectarrays in profielgegevenssets. Het gebruiken van een [&#x200B; serie van voorwerpen &#x200B;](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/complex-data/object-arrays.html) voor `audienceMembershipId` of `audienceMembershipIdName` is de beste optie.
   1. Maak in uw gegevensweergave een nieuwe dimensie met behulp van de subtekenreekstransformatie in het veld `audienceMembershipId` om de tekenreeks met door komma&#39;s gescheiden waarden om te zetten in een array. NOTA: er is momenteel een grens van 10 waarden in de serie.
   1. U kunt nu over deze nieuwe dimensie `audienceMembershipIds` rapporteren in Customer Journey Analytics Workspace.
