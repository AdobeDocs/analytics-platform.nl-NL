---
title: Gegevens van Google Analytics opnemen in Adobe Experience Platform
description: 'Verklaart hoe te hefboomwerking Customer Journey Analytics (CJA) om uw gegevens van Google Analytics in Adobe Experience Platform in te voeren. '
exl-id: 314378c5-b1d7-4c74-a241-786198fa0218
translation-type: tm+mt
source-git-commit: a4e95424ee304869e76a0532b7240290a3f13418
workflow-type: tm+mt
source-wordcount: '1208'
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
* Toegang tot Customer Journey Analytics en zijn [Admin toestemmingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en#admin-access-permissions).

Hoe u gegevens van Google Analytics in Adobe Experience Platform brengt hangt van welke versie van Google Analytics af u gebruikt:

| Als u... | U hebt deze licentie ook nodig... | En doe dit... |
| --- | --- | --- |
| **Universal Analytics** | Google Analytics 360 | Voer stap 1-3 van de onderstaande instructies uit |
| **Google Analytics 4** | Gratis GA-versie of Google Analytics 360 | Voer stap 1 en 3 van de onderstaande instructies uit. Geen behoefte aan stap 2. |

## Samenvatting historische gegevens (backfill)

### 1. Verbind uw gegevens van Google Analytics met BigQuery

Raadpleeg [deze instructies](https://support.google.com/analytics/answer/3416092?hl=en) voor meer informatie. Deze instructies zijn gebaseerd op Universal Google Analytics.

### 2. Google Analytics-sessies transformeren naar gebeurtenissen in BigQuery en exporteren naar Google Cloud Storage

>[!IMPORTANT]
>
>Deze stap is alleen van toepassing op klanten van Universal Analytics

GA-gegevens slaan elke record in de gegevens op als een gebruikerssessie in plaats van als afzonderlijke gebeurtenissen. U moet een SQL vraag tot stand brengen om de Universele gegevens van Analytics in een ervaring-Platform-volgzaam formaat om te zetten. U past de functie &quot;Unest&quot; toe op het veld &quot;hits&quot; in het GA-schema. Hier volgt het SQL-voorbeeld dat u kunt gebruiken:

`SELECT
*,
timestamp_seconds(`` + hit.time) AS `` 
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
`visitStartTimetimestampyour_bq_table_2021_04_*`,
UNNEST(hits) AS hit 
)`

Zodra de vraag voltooit, sparen de volledige resultaten in een lijst BigQuery.

Zie [deze instructies](https://support.google.com/analytics/answer/7029846?hl=en&amp;ref_topic=9359001#zippy=%2Cold-export-schema%2Cuse-this-script-to-migrate-existing-bigquery-datasets-from-the-old-export-schema-to-the-new-one%2Cscript-migration-scriptsql), die instructies op de SQL vraag omvatten.

In de volgende video wordt ook de volgende stap uitgelegd, namelijk het exporteren van de Google Analytics-gebeurtenissen naar Google Cloud Storage in JSON-indeling. Klik **Exporteren > Exporteren naar GCS**. Als er eenmaal gegevens beschikbaar zijn, kunnen ze naar Adobe Experience Platform worden gehaald.

>[!VIDEO](https://video.tv.adobe.com/v/332634)

### 3. Gegevens van Google Cloud Storage importeren in Experience Platform en toewijzen aan XDM-schema

Selecteer **[!UICONTROL Sources]** in Experience Platform en zoek de optie **[!UICONTROL Google Cloud Storage]**. Van daar, moet u enkel de dataset vinden u van BigQuery had bewaard.

Houd dit in gedachten:

* Selecteer de JSON-indeling.
* U kunt een bestaande dataset selecteren, of een nieuwe dataset (geadviseerd) creëren.
* Zorg ervoor om het zelfde schema voor historische gegevens van Google Analytics en levende het stromen Google Analytics te selecteren, zelfs als zij in afzonderlijke datasets zijn. U kunt de datasets in een [verbinding CJA ](/help/connections/combined-dataset.md) later samenvoegen.

Bekijk deze video voor instructies:

>[!VIDEO](https://video.tv.adobe.com/v/332676)

U kunt de GA gebeurtenisgegevens in een bestaande dataset in kaart brengen die u eerder creeerde, of een nieuwe dataset tot stand brengen, gebruikend welk schema XDM u kiest. Zodra u het schema hebt geselecteerd, past het Experience Platform machine het leren toe om elk van de gebieden in de gegevens van Google Analytics aan uw [XDM schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en#ui) automatisch pre-in kaart te brengen.

![](assets/schema-map.png)

Toewijzingen zijn zeer gemakkelijk te veranderen en u kunt zelfs afgeleide of berekende gebieden van de gegevens van Google Analytics tot stand brengen. Nadat u de velden hebt toegewezen aan uw XDM-schema, kunt u deze import op terugkerende basis plannen en tijdens het innameproces foutvalidatie toepassen. Op die manier weet u zeker dat er geen problemen zijn met de gegevens die u hebt geïmporteerd.

**Berekend veld &#39;Tijdstempel&#39;**

Voor het `timestamp` schemagebied in Google Analytics gegevens, moet u een speciaal berekend gebied in het schema UI van het Experience Platform tot stand brengen. Klik **[!UICONTROL Add calculated field]** en verpakt de `timestamp` koord in een `date` functie, als dit:

`date(timestamp, "yyyy-MM-dd HH:mm:ssZ")`

Vervolgens moet u dit berekende veld opslaan in de gegevensstructuur van het tijdstempel in het schema:

![](assets/timestamp.png)

**Berekend veld &#39;_id&#39;**

Het schemaveld `_id` moet een waarde erin hebben - CJA geeft niet wat de waarde is. U kunt gewoon een &quot;1&quot; aan het veld toevoegen:

![](assets/_id.png)

## Live streaming Google Analytics-gegevens verwerken

U kunt ook livestreaminggebeurtenissen vastleggen van Google Tag Manager rechtstreeks naar Adobe Experience Platform.

### 1. Aangepaste variabelen toevoegen

Nadat u zich hebt aangemeld bij het Google Tag Manager-account, moet u enkele aangepaste constante variabelen toevoegen die betrekking hebben op Adobe. U hebt waarschijnlijk al variabelen in Google Tag Manager die naar Google Analytic worden verzonden, zoals het e-mailadres van de klant, de naam van de klant, de taal en de aanmeldingsstatus van de klant. U moet vijf nieuwe aangepaste variabelen definiëren:

* Adobe Experience Cloud org ID
* DCS Streaming-eindpunt
* ID gegevensset Experience Platform
* Schema
* Tijdstempel pagina

Het krijgen van deze waarden zorgt ervoor dat alle gegevens van Google Analytics naar de correcte dataset worden verzonden en het juiste schema hebben. Als u de Experience Cloud Org of een van de andere variabelen die we zojuist hebben genoemd niet kent, kan uw accountmanager van Adobe u helpen deze op te sporen.

Nadat u deze aangepaste variabelen hebt gedefinieerd, kunnen we een trigger instellen om alle gegevens die u al verzendt, ook naar de Google Analytics van het Experience Platform te verzenden.

### 2. Een trigger instellen in Google Tag Manager

In dit voorbeeld is de trigger Account Creation gedefinieerd, waarbij `pageUrl equals account-creation` is gedefinieerd. Door enige informatie aan deze trigger toe te voegen, kunt u ervoor zorgen dat gegevens naar zowel Google Analytics als AEP worden verzonden wanneer de gebruiker met succes verifieert en de pagina voor het maken van een account wordt geladen.

U kunt ook naar [Gegevensverwerking en Google Tag Manager](https://experienceleague.adobe.com/docs/platform-learn/comprehensive-technical-tutorial/module9/data-ingestion-using-google-tag-manager-and-google-analytics.html?lang=en#module9) verwijzen.

Bekijk deze video voor instructies:

>[!VIDEO](https://video.tv.adobe.com/v/332668)

## Creeer een Verbinding in CJA aan de dataset van Google Analytics

Zodra Adobe Experience Platform is begonnen de levende gegevens van Google Analytics te ontvangen, en u hebt de historische gegevens van Google Analytics van BigQuery teruggevuld, bent u klaar om in CJA te springen en [uw eerste verbinding te creëren](/help/connections/create-connection.md). Met deze verbinding worden de GA-gegevens gekoppeld aan al uw andere klantgegevens met behulp van een gemeenschappelijke &quot;Customer ID&quot;.

## Volgende stappen

* Een gegevensweergave maken op basis van Google Analytics-gegevens
Daarna, creeert u [een gegevensmening](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#cja-dataviews) in CJA, die op de verbinding wordt gebaseerd die de gegevens van Google Analytics bevat.

* Voer een verbluffende analyse uit in [Workspace](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/home.html?lang=en#cja-workspace). Kom later terug voor bepaalde gevallen van rapportgebruik.