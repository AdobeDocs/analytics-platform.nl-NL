---
title: Historische gegevens van Googles Analytics opnemen in Adobe Experience Platform
description: Verklaart hoe te om Adobe Customer Journey Analytics te gebruiken om uw gegevens van Googles Analytics in Adobe Experience Platform in te voeren.
exl-id: 314378c5-b1d7-4c74-a241-786198fa0218
solution: Customer Journey Analytics
feature: Use Cases
source-git-commit: c343a729de4cb13473a7acc04e837b5e5f69809b
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---


# Historische gegevens van Googles Analytics opnemen in Adobe Experience Platform

Deze pagina concentreert zich op hoe te om uw Googles Analytics historische gegevens in Adobe Experience Platform als dataset in te voeren, toestaand u om die dataset in een Mening van Gegevens in Customer Journey Analytics van verwijzingen te voorzien. U kunt de stappen op deze pagina combineren met [Implementatie van live Googles Analytics configureren](streaming.md), die een terugkerende dataset produceert. Combineer deze historische dataset met de dataset van uw huidige implementatie om een naadloze mening van gegevens in Customer Journey Analytics met zowel huidige als backfill gegevens te krijgen.

## Vereisten

Voor het uitvoeren van deze taken hebt u de volgende toegang en machtigingen nodig:

* Toegang tot Adobe Experience Platform
* Toegang tot Googles Analytics (GA-standaard of GA 360)
* [Beheerderstoegang](/help/admin/cja-access-control.md) naar Customer Journey Analytics

## Een BigQuery-export instellen

De gegevensstructuur in Universal Analytics-eigenschappen verschilt van de gegevensstructuur in Googles Analytics 4-eigenschappen. Opstelling een Uitvoer BigQuery die op het bezitstype wordt gebaseerd dat u gegevens van wilt uitvoeren:

* [Een BigQuery-export instellen voor een Universal Analytics-eigenschap](https://support.google.com/analytics/answer/3416092)
* [Opstelling een Uitvoer van BigQuery voor een Google Analytics 4 bezit](https://support.google.com/analytics/answer/9823238)

### Aanvullende eisen voor eigenschappen van Universal Analytics

>[!NOTE]
>
>Deze sectie is alleen van toepassing op eigenschappen van Universal Analytics. Als u exporteert vanuit een GA4-eigenschap, kunt u doorgaan naar [Gegevens exporteren naar Google Cloud Platform](#export-gcp).

Met de Universal Analytics-eigenschappen wordt elke record in de gegevens opgeslagen als een gebruikerssessie in plaats van als afzonderlijke gebeurtenissen. Er is een SQL-query vereist om de Universal Analytics-gegevens om te zetten in een indeling die compatibel is met Adobe Experience Platform. Pas de `UNNEST` aan de `hits` in het GA-schema en sla het op als een BigQuery-tabel.

>[!VIDEO](https://video.tv.adobe.com/v/332634)

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

Navigeer in Google Cloud Platform naar **Exporteren > Exporteren naar GCS**. Zodra de gegevens in Google Cloud Storage staan, kunnen ze naar Adobe Experience Platform worden gehaald.

## Gegevens importeren van Google Cloud Storage naar Experience Platform

1. Selecteer in Adobe Experience Platform **[!UICONTROL Sources]** links.
1. Ga onder de catalogus naar **[!UICONTROL Google Cloud Storage]** -optie. Klik op **[!UICONTROL Add data]**.

>[!VIDEO](https://video.tv.adobe.com/v/332676)

>[!TIP]
>
>Als u van plan bent om zowel historische als levende het stromen Googles Analytics gegevens in te voeren, zorg ervoor dat u het zelfde schema voor beide datasets gebruikt. U kunt de datasets in een Customer Journey Analytics samenvoegen gebruikend een [Gecombineerde gegevensset](/help/connections/combined-dataset.md).

U kunt de GA gebeurtenisgegevens in een bestaande dataset in kaart brengen die u eerder creeerde, of een dataset tot stand brengen, gebruikend welk schema XDM u kiest. Nadat u het schema hebt geselecteerd, wordt automatisch leren toegepast op het Experience Platform om automatisch elk van de velden in de gegevens van de Googles Analytics vooraf toe te wijzen aan uw [XDM-schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html#ui).

![Schemaoverzicht waarin de GA-gegevensvelden en de schematoewijzingen voor het doel worden gemarkeerd](../assets/schema-map.png)

Als u klaar bent met het toewijzen van de velden aan uw XDM-schema, kunt u deze import op terugkerende basis plannen en tijdens het innameproces foutvalidatie toepassen. Deze bevestiging zorgt ervoor dat er geen kwesties met de gegevens zijn u hebt ingevoerd.

## Vereiste XDM-velden

Bepaalde XDM-velden in Platform hebben de juiste indeling nodig om de gegevens correct te kunnen verwerken.

* **`timestamp`**: Maak een speciaal berekend veld in de interface van het schema Experience Platform. Klikken **[!UICONTROL Add calculated field]** en de `timestamp` tekenreeks in een `date` functie:

  `date(timestamp, "yyyy-MM-dd HH:mm:ssZ")`

  Sla het berekende veld op in de gegevensstructuur van het tijdstempel in het schema:

  ![Tijdstempel](../assets/timestamp.png)

* **`_id`**: Dit veld moet een waarde bevatten. De Customer Journey Analytics kan er niet om geven wat de waarde is. U kunt een &quot;1&quot; aan het veld toevoegen:

  ![ID](../assets/_id.png)

## Volgende stappen

* Als u de huidige gegevens hebt die u naar Adobe Experience Platform wilt streamen, raadpleegt u [Streaming instellen voor gegevens van Googles Analytics](streaming.md).
* Als u wilt beginnen met het rapporteren van gegevens met een back-up, raadpleegt u [Verbinding maken](/help/connections/create-connection.md).
