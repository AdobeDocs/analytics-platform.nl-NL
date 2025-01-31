---
title: Historische gegevens van Googles Analytics samenvoegen
description: Verklaart hoe te om Adobe Customer Journey Analytics te gebruiken om uw gegevens van Googles Analytics in Adobe Experience Platform in te voeren.
exl-id: 314378c5-b1d7-4c74-a241-786198fa0218
solution: Customer Journey Analytics
feature: Use Cases
role: Admin
source-git-commit: 4bf8c616965718426efe880865acb0e5054b6a31
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---


# Historische gegevens van Googles Analytics samenvoegen

Deze pagina concentreert zich op hoe te om uw Googles Analytics historische gegevens in Adobe Experience Platform als dataset in te voeren, toestaand u om die dataset in een Mening van Gegevens in Customer Journey Analytics van verwijzingen te voorzien. U kunt de stappen op deze pagina combineren met [ Vormend een levende implementatie van Googles Analytics ](streaming.md), die een terugkomende dataset produceert. Combineer deze historische dataset met de dataset van uw huidige implementatie om een naadloze mening van gegevens in Customer Journey Analytics met zowel huidige als backfill gegevens te krijgen.

## Vereisten

Voor het uitvoeren van deze taken hebt u de volgende toegang en machtigingen nodig:

* Toegang tot Adobe Experience Platform
* Toegang tot Googles Analytics (GA-standaard of GA 360)
* [ Toegang Admin ](/help/technotes/access-control.md) aan Customer Journey Analytics

## Een BigQuery-export instellen

De gegevensstructuur in Universal Analytics-eigenschappen verschilt van de gegevensstructuur in Googles Analytics 4-eigenschappen. Opstelling een Uitvoer BigQuery die op het bezitstype wordt gebaseerd dat u gegevens van wilt uitvoeren:

* [ Opstelling de Uitvoer van een BigQuery voor een Universeel bezit van Analytics ](https://support.google.com/analytics/answer/3416092)
* [ Opstelling de Uitvoer van BigQuery voor Googles Analytics 4 bezit ](https://support.google.com/analytics/answer/9823238)

### Aanvullende eisen voor eigenschappen van Universal Analytics

>[!NOTE]
>
>Deze sectie is alleen van toepassing op eigenschappen van Universal Analytics. Als u van een bezit GA4 uitvoert, kunt u aan [ gegevens van de Uitvoer aan het Platform van de Wolk van Google ](#export-gcp) te werk gaan.

Met de Universal Analytics-eigenschappen wordt elke record in de gegevens opgeslagen als een gebruikerssessie in plaats van als afzonderlijke gebeurtenissen. Er is een SQL-query vereist om de Universal Analytics-gegevens om te zetten in een indeling die compatibel is met Adobe Experience Platform. Pas de functie `UNNEST` toe op het `hits` -veld in het GA-schema en sla deze op als een BigQuery-tabel.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ van Googles Analytics aan Customer Journey Analytics - BigQuery ](https://video.tv.adobe.com/v/332634?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


```sql
SELECT
   *,
   timestamp_seconds(`visitStartTime` + hit.time) AS `timestamp` 
FROM
   (
      SELECT
         fullVisitorId,
         visitNumber,
         visitId,
         visitStartTime,
         trafficSource,
         socialEngagementType,
         channelGrouping,
         device,
         geoNetwork,
         hit 
      FROM
         `example_bq_table_*`,
         UNNEST(hits) AS hit 
   )
```

## Gegevens exporteren naar Google Cloud Platform {#export-gcp}

In het Platform van de Wolk van Google, navigeer aan **Uitvoer > de Uitvoer aan GCS**. Zodra de gegevens in Google Cloud Storage staan, kunnen ze naar Adobe Experience Platform worden gehaald.

## Gegevens importeren van Google Cloud Storage naar Experience Platform

1. Selecteer in Adobe Experience Platform **[!UICONTROL Sources]** aan de linkerkant.
1. Zoek in de catalogus de optie **[!UICONTROL Google Cloud Storage]** . Klik op **[!UICONTROL Add data]**.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ gegevens van de Googles Analytics van de Invoer in Adobe Experience Platform ](https://video.tv.adobe.com/v/332676?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


>[!TIP]
>
>Als u van plan bent om zowel historische als levende het stromen Googles Analytics gegevens in te voeren, zorg ervoor dat u het zelfde schema voor beide datasets gebruikt. U kunt de datasets in een Customer Journey Analytics samenvoegen gebruikend a [ Gecombineerde dataset ](/help/connections/combined-dataset.md).

U kunt de GA gebeurtenisgegevens in een bestaande dataset in kaart brengen die u eerder creeerde, of een dataset tot stand brengen, gebruikend welk schema XDM u kiest. Zodra u het schema hebt geselecteerd, past het Experience Platform machine het leren toe om automatisch elk van de gebieden in de gegevens van Googles Analytics aan uw [ XDM schema ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html#ui) pre-in kaart te brengen.

![ kaart van het Schema die de GA gegevensgebieden en de het schemaafbeeldingen van het Doel benadrukt ](../assets/schema-map.png)

Als u klaar bent met het toewijzen van de velden aan uw XDM-schema, kunt u deze import op terugkerende basis plannen en tijdens het innameproces foutvalidatie toepassen. Deze bevestiging zorgt ervoor dat er geen kwesties met de gegevens zijn u hebt ingevoerd.

## Vereiste XDM-velden

Bepaalde XDM-velden in Platform hebben de juiste indeling nodig om de gegevens correct te kunnen verwerken.

* **`timestamp`**: Maak een speciaal berekend veld in de gebruikersinterface van het schema van het Experience Platform. Klik op **[!UICONTROL Add calculated field]** en laat de `timestamp` string in een `date` functie omlopen:

  `date(timestamp, "yyyy-MM-dd HH:mm:ssZ")`

  Sla het berekende veld op in de gegevensstructuur van het tijdstempel in het schema:

  ![ Tijdstempel ](../assets/timestamp.png)

* **`_id`**: In dit veld moet een waarde staan. De Customer Journey Analytics geeft niet wat de waarde is. U kunt een &quot;1&quot; aan het veld toevoegen:

  ![ identiteitskaart ](../assets/_id.png)

## Volgende stappen

* Als u huidige gegevens hebt die u in Adobe Experience Platform wilt stromen, zie [ Opstelling die voor Googles Analytics gegevens ](streaming.md) stroomt.
* Als u wilt beginnen rapporterend over achtergevulde gegevens, zie [ een verbinding ](/help/connections/create-connection.md) creëren.
