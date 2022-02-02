---
title: Gegevens van Google Analytics opnemen in Adobe Experience Platform
description: 'Verklaart hoe te hefboomwerking Customer Journey Analytics (CJA) om uw gegevens van Google Analytics in Adobe Experience Platform in te voeren. '
exl-id: 314378c5-b1d7-4c74-a241-786198fa0218
solution: Customer Journey Analytics
feature: Use Cases
source-git-commit: c36dddb31261a3a5e37be9c4566f5e7ec212f53c
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---


# Gegevens van Google Analytics opnemen in Adobe Experience Platform

Dit gebruiksgeval concentreert zich op hoe te om uw gegevens van Google Analytics als dataset in Adobe Experience Platform in te nemen. We leggen uit hoe we zowel historische als live gegevens kunnen opnemen. Zodra gedaan, kunt u beide datasets in Customer Journey Analytics combineren om een dwars-apparatenmening van de reis van uw gebruiker te bereiken.

Datasets in het Experience Platform bestaan uit twee dingen: een schema en de daadwerkelijke verslagen in de dataset. Het schema (wij roepen dit het Model van Gegevens van de Ervaring of XDM voor kort) is als de kolommen van de dataset en is als blauwdruk of de regels die de gegevens zelf beschrijven. Binnen het Platform, verstrekt Adobe 2 types van schema&#39;s:

* Buiten-de-doosschema&#39;s dat u uw gegevens van Google Analytics aan automatisch kunt in kaart brengen (genoemd het schema van de Gebeurtenis van de Ervaring)
* Aangepaste schema&#39;s die u kunt maken en waarmee u de Google Analytics-gegevens eenvoudig kunt toewijzen

Één van de krachtigste aspecten van het gegevensmodel van Adobe is dat het u toestaat om al uw gegevens van de klanteninteractie in één gemeenschappelijk schema te standaardiseren - dit maakt het veel gemakkelijker om de gegevens samen in CJA te binden.

## Vereisten

Voor het uitvoeren van deze taken hebt u de volgende toegang en machtigingen nodig:

* Toegang tot Adobe Experience Platform
* Toegang tot Universal Google Analytics (versie Google Analytics 360) of Google Analytics 4 (versie met gratis versie of versie Google Analytics 360)
* Toegang tot Customer Journey Analytics en [Beheerdersmachtigingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en#admin-access-permissions).

Hoe u gegevens van Google Analytics in Adobe Experience Platform brengt hangt van welke versie van Google Analytics af u gebruikt:

| Als u... | U hebt deze licentie ook nodig... | En doe dit... |
| --- | --- | --- |
| **Universal Analytics** | Google Analytics 360 | Voer stap 1-3 van de onderstaande instructies uit |
| **Google Analytics 4** | Gratis GA-versie of Google Analytics 360 | Voer stap 1 en 3 van de onderstaande instructies uit. Geen behoefte aan stap 2. |

## Samenvatting historische gegevens (backfill)

### 1. Verbind uw gegevens van Google Analytics met BigQuery

Raadpleeg voor meer informatie [deze instructies](https://support.google.com/analytics/answer/3416092?hl=en). Deze instructies zijn gebaseerd op Universal Google Analytics.

### 2. Google Analytics-sessies transformeren naar gebeurtenissen in BigQuery en exporteren naar Google Cloud Storage

>[!IMPORTANT]
>
>Deze stap is alleen van toepassing op klanten van Universal Analytics

GA-gegevens slaan elke record in de gegevens op als een gebruikerssessie in plaats van als afzonderlijke gebeurtenissen. U moet een SQL vraag tot stand brengen om de Universele gegevens van Analytics in een ervaring-Platform-volgzaam formaat om te zetten. U past de functie &quot;Unest&quot; toe op het veld &quot;hits&quot; in het GA-schema. Hier volgt het SQL-voorbeeld dat u kunt gebruiken:

```
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
         `your_bq_table_2021_04_*`,
         UNNEST(hits) AS hit 
   )
```

Zodra de vraag voltooit, sparen de volledige resultaten in een lijst BigQuery.

Zie [deze instructies](https://support.google.com/analytics/answer/7029846?hl=en&amp;ref_topic=9359001#zippy=%2Cold-export-schema%2Cuse-this-script-to-migrate-existing-bigquery-datasets-from-the-old-export-schema-to-the-new-one%2Cscript-migration-scriptsql), die instructies bevatten over de SQL-query.

In de volgende video wordt ook de volgende stap uitgelegd, namelijk het exporteren van de Google Analytics-gebeurtenissen naar Google Cloud Storage in JSON-indeling. Alleen klikken **Exporteren > Exporteren naar GCS**. Als er eenmaal gegevens beschikbaar zijn, kunnen ze naar Adobe Experience Platform worden gehaald.

>[!VIDEO](https://video.tv.adobe.com/v/332634)

### 3. Gegevens van Google Cloud Storage importeren in Experience Platform en toewijzen aan XDM-schema

Selecteer in Experience Platform de optie **[!UICONTROL Sources]** en de **[!UICONTROL Google Cloud Storage]** optie. Van daar, moet u enkel de dataset vinden u van BigQuery had bewaard.

Houd dit in gedachten:

* Selecteer de JSON-indeling.
* U kunt een bestaande dataset selecteren, of een nieuwe dataset (geadviseerd) creëren.
* Zorg ervoor om het zelfde schema voor historische gegevens van Google Analytics en levende het stromen Google Analytics te selecteren, zelfs als zij in afzonderlijke datasets zijn. U kunt de gegevenssets vervolgens samenvoegen in een [CJA-verbinding](/help/connections/combined-dataset.md).

Bekijk deze video voor instructies:

>[!VIDEO](https://video.tv.adobe.com/v/332676)

U kunt de GA gebeurtenisgegevens in een bestaande dataset in kaart brengen die u eerder creeerde, of een nieuwe dataset tot stand brengen, gebruikend welk schema XDM u kiest. Nadat u het schema hebt geselecteerd, wordt automatisch leren toegepast op het Experience Platform om automatisch elk van de velden in de Google Analytics-gegevens vooraf toe te wijzen aan uw [XDM-schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en#ui).

![](assets/schema-map.png)

Toewijzingen zijn zeer gemakkelijk te veranderen en u kunt zelfs afgeleide of berekende gebieden van de gegevens van Google Analytics tot stand brengen. Nadat u de velden hebt toegewezen aan uw XDM-schema, kunt u deze import op terugkerende basis plannen en tijdens het innameproces foutvalidatie toepassen. Op die manier weet u zeker dat er geen problemen zijn met de gegevens die u hebt geïmporteerd.

**Berekend veld &#39;Tijdstempel&#39;**

Voor de `timestamp` schemagebied in Google Analytics gegevens, moet u een speciaal berekend gebied in het schema UI van het Experience Platform tot stand brengen. Klikken **[!UICONTROL Add calculated field]** en de `timestamp` tekenreeks in een `date` functie, als volgt:

`date(timestamp, "yyyy-MM-dd HH:mm:ssZ")`

Vervolgens moet u dit berekende veld opslaan in de gegevensstructuur van het tijdstempel in het schema:

![](assets/timestamp.png)

**Berekend veld &#39;_id&#39;**

De `_id` schemaveld moet er een waarde in hebben - CJA geeft niet wat de waarde is. U kunt gewoon een &quot;1&quot; aan het veld toevoegen:

![](assets/_id.png)

## Live streaming Google Analytics-gegevens verwerken

U kunt livestreaminggebeurtenissen ook rechtstreeks vastleggen vanuit Google Tag Manager naar Adobe Experience Platform.

### 1. Aangepaste variabelen toevoegen

Nadat u zich hebt aangemeld bij het Google Tag Manager-account, moet u enkele aangepaste constante variabelen toevoegen die betrekking hebben op Adobe. U hebt waarschijnlijk al variabelen in Google Tag Manager die naar Google Analytics worden verzonden, zoals de klant-e-mail, de naam van de klant, de taal en de aanmeldingsstatus van de klant. U moet vijf nieuwe aangepaste variabelen definiëren:

* Adobe Experience Cloud org ID
* DCS Streaming-eindpunt
* ID gegevensset Experience Platform
* Schema
* Tijdstempel pagina

Het krijgen van deze waarden zorgt ervoor dat alle gegevens van Google Analytics naar de correcte dataset worden verzonden en het juiste schema hebben. Als u de Experience Cloud Org of een van de andere variabelen die we zojuist hebben genoemd niet kent, kan uw accountmanager van Adobe u helpen deze op te sporen.

Nadat u deze aangepaste variabelen hebt gedefinieerd, kunnen we een trigger instellen om alle gegevens die u al verzendt, ook naar de Google Analytics van het Experience Platform te verzenden.

### 2. Een trigger instellen in Google-tagbeheer

In dit voorbeeld is de trigger &quot;Account Creation&quot; gedefinieerd, waarbij de `pageUrl equals account-creation`. Door enige informatie aan deze trigger toe te voegen, kunt u ervoor zorgen dat gegevens naar zowel Google Analytics als AEP worden verzonden wanneer de gebruiker met succes verifieert en de pagina voor het maken van een account wordt geladen.

U kunt ook verwijzen naar [Gegevensverwerking en Google-tagbeheer](https://experienceleague.adobe.com/docs/platform-learn/comprehensive-technical-tutorial/module9/data-ingestion-using-google-tag-manager-and-google-analytics.html?lang=en#module9).

Bekijk deze video voor instructies:

>[!VIDEO](https://video.tv.adobe.com/v/332668)

## Creeer een Verbinding in CJA aan de dataset van Google Analytics

Als de Adobe Experience Platform de live Google Analytics-gegevens heeft ontvangen en u een back-up hebt gemaakt van de historische Google Analytics-gegevens van BigQuery, kunt u naar CJA springen en [uw eerste verbinding maken](/help/connections/create-connection.md). Met deze verbinding worden de GA-gegevens gekoppeld aan al uw andere klantgegevens met behulp van een gemeenschappelijke &quot;klant-id&quot;.

## Volgende stappen

* Een [gegevensweergave](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#cja-dataviews) op basis van de verbinding die Google Analytics-gegevens bevat.

* Wat verbazingwekkend [analyse in Workspace](/help/use-cases/ga-to-cja-reporting.md).