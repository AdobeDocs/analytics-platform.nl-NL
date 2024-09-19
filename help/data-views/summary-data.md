---
title: Samenvattingsgegevens
description: Details en informatie over het gebruiken en vormen van summiere gegevens in een gegevensmening.
solution: Customer Journey Analytics
feature: Data Views
role: Admin
exl-id: 417443ae-a1ab-483b-a8fd-cff5ee8b6263
source-git-commit: e6f57b03689bd9aaaec12c13fc95da5b079b901e
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 2%

---

# Samenvattingsgegevens

Samenvattingsgegevens zijn tijdreeksgegevens die niet aan een individuele persoon-id zijn gekoppeld. De summiere gegevens vertegenwoordigen samengevoegde gegevens op een verschillend niveau van samenvoeging, bijvoorbeeld campagnes. U kunt deze gegevens in Customer Journey Analytics gebruiken om verschillende gebruiksgevallen te ondersteunen. Bijvoorbeeld gegevens die een datum en een enkele metrische waarde bevatten, of gegevens die meerdere afmetingen en metriek bevatten.

Deze beknopte gegevens kunnen vervolgens worden gebruikt om prestatie-indicatoren op hoog niveau te presenteren of om analyses uit te voeren. Voorbeelden van samenvattingsgegevens zijn onder andere advertenties, e-mails openen, reclameuitgaven, kosten van goed verkocht, S&amp;P-indices en meer. U kunt samenvattingsgegevens ook gebruiken om doelen of doelen per uur of per dag te uploaden.

>[!NOTE]
>
>De summiere gegevens zijn tijdreeksgegevens van een summiere dataset. Die summiere dataset is gebaseerd op een schema dat de klasse van Metriek XDM Summiere als zijn basisklasse gebruikt.
>Alleen tijdreeksgegevens die zijn gebaseerd op uren of dagen worden ondersteund.

>[!TIP]
>
>U kunt een verbinding, een gegevensmening vormen en daarna op **slechts** summiere gegevens rapporteren. Het is niet vereist om extra gebeurtenis, profiel of raadplegingsgegevens als deel van uw configuratie te hebben.


## Voorbeeld

Een voorbeeld van het gebruiken van summiere gegevens is het combineren van samengevatte reclamecampagnegegevens met online klikstroomgegevens voor het melden.

### Samenvattingsgegevens

Uw samenvattingsgegevens bevatten de volgende gegevens voor de advertentiecampagne.

| Campagnecode | Impressies | Kosten |
|---|---:|---:|
| abc123 | 1.250 | USD 1.500 |
| def456 | 775 | $ 650 |
| ghi789 | 500 | $ 500 |


### Gebeurtenisgegevens

Uw klikstreamgegevens op de site bevatten de volgende gebeurtenissen.

| Trackingcode | Doorklikken | Ontvangsten |
|---|---:|---:|
| abc123 | 1.250 | USD 7.200 |
| def456 | 775 | USD 1.250 |
| ghi789 | 500 | $ 750 |

### Gecombineerde gegevens

Zoals verklaard in [ Gecombineerde gebeurtenisdataset ](/help/connections/combined-dataset.md), wanneer het bepalen van een verbinding, leidt de Customer Journey Analytics tot een algemene gecombineerde gebeurtenisdataset. Wanneer u uw gegevensmening voor afmetingen uit een summiere dataset vormt, zijn de opties beschikbaar om afmetingen te groeperen en te verbergen als voorbereiding voor het melden in Workspace. Specifiek voor summiere gegevens, wordt het summiere gegeven gecombineerd met gebeurtenisgegevens, die op de [ worden gebaseerd samenvattingscomponent van de gegevensgroep ](component-settings/summary-data-group.md) configuratie.

| Trackingcode | Campagnecode | Impressies | Kosten | Doorklikken | Ontvangsten |
|---|---|--:|--:|--:|--:|
| abc123 | abc123 | 1.250 | USD 1.500 | 1.250 | USD 7.200 |
| def456 | def123 | 775 | $ 650 | 775 | USD 1.250 |
| ghi789 | ghi789 | 500 | $ 500 | 500 | $ 750 |



### Rapportage

Door de samengevatte gebeurtenisgegevens te combineren met on-site clickstream-gegevens, kunt u in Workspace rapporteren op return on ad exps (ROAS).

| Trackingcode | Impressies | Kosten | Doorklikken | Ontvangsten | ROAS |
|---|--:|--:|--:|--:|:--|
| abc123 | 1.250 | USD 1.500 | 1.250 | USD 7.200 | 4,80 |
| def456 | 775 | $ 650 | 775 | USD 1.250 | 1,92 |
| ghi789 | 500 | $ 500 | 500 | $ 750 | 1,50 |


### Gegevens opzoeken

Als u het gebruiken van een afmeting wilt melden die in een extra raadplegingsdataset (bijvoorbeeld, campagnenaam wordt bepaald), moet u deze extra stappen volgen:

1. Creeer een nieuw afgeleid gebied dat de [ ](/help/data-views/derived-fields/derived-fields.md#lookup) functie van de Raadpleging gebruikt om de campagnenaam van de raadplegingsdataset te zoeken. In de definitie van de [ ](/help/data-views/derived-fields/derived-fields.md#lookup) functie van de Opzoeken gebruikt u de gelijke tussen campagnecode en het volgen code om de campagnenaam te zoeken.
1. Voeg het nieuwe afgeleide gebied als afmetingscomponent aan uw gegevensmening toe.
1. Vorm de de afmetingscomponent van de campagnenaam (van de raadplegingsdataset) om een summiere gegevens te hebben groeperen met het pas gecreëerde afgeleide gebied.

Zie [ Samenvatten en rapport over summiere gegevens ](/help/use-cases/data-views/summary-data.md) gebruiksgeval voor een gedetailleerd artikel over hoe te om gebruik van te maken van, te rapporteren over, en samenvattingsgegevens in Customer Journey Analytics te analyseren.


## Vereisten

Om summiere gegevens in uw rapporten en analyse behoorlijk te gebruiken, zijn een aantal eerste vereisten van toepassing. In de volgende secties worden deze voorwaarden nader beschreven.

### Korreligheid en tijdzone

Wanneer het vormen van de dataset die de summiere gegevens in Customer Journey Analytics bevatten, merkt u op dat granularity automatisch uit de gegevens wordt afgeleid. De selecties voor **[!UICONTROL Timestamp]** en **[!UICONTROL Timezone]** dropdown zijn uitgeschakeld omdat beide uit de schemadefinitie zijn afgeleid.

#### Granulariteit

U kunt niet het uur en de dagelijkse granulariteit van uw summiere gegevens in één dataset (of met verschillende datasets) mengen en aanpassen, gebruikend één samenvattingsgegevensschema. Als u bijvoorbeeld dagelijkse en uurkorrelige samenvattingsgegevens voor reclamecampagne hebt, hebt u twee schema&#39;s nodig: één voor de dagelijkse en één voor de uursamenvattingsgegevens. En upload dan de relevante korrelige gegevens in datasets verbonden aan het juiste schema (bijvoorbeeld, upload uurgegevens in een dataset verbonden aan het schema van het uursamenvatting van gegevens).

#### Tijdzone

De tijdzone van uw summiere gegevens wordt bepaald op het summiere schemaniveau in Experience Platform. De tijdzone is alleen van toepassing op korrelgegevens per uur.

- Voor de dagelijkse granulariteit, veronderstelt Experience Platform UTC, tenzij een timezone compensatie in timestamp wordt omvat. Wanneer het toevoegen van de summiere dataset die de dagelijkse summiere gegevens bevat, negeert de Customer Journey Analytics de tijdzonedefinitie die op het schema wordt geplaatst en de dag verbonden aan timestamp van de gegevens in de dataset respecteert.
- Voor korreligheid per uur, respecteert de Customer Journey Analytics de tijdzone die op het summiere gegevensschema in Experience Platform wordt gevormd wanneer het interpreteren van timestamp. In de onderstaande tabel staan enkele voorbeelden van deze interpretatie.

  | Tijdstempel <br/> brongegevens | Tijdzone <br/> schema | Tijdstempel <br/> Platform van de Ervaring 1}<br/> | Tijdzone <br/> gegevens <br/> mening | De Analyse van de Stem van de Stem <br/> van de Klant <br><br/> |
  |---|---|---|:---|---|
  | 2024-07-29T01 :00: 00 | *gebrek GMT* | 2024-07-29T01 :00: 00 | GMT | 2024-07-29T01 :00: 00 |
  | 2024-07-29T01 :00: 00 | *gebrek GMT* | 2024-07-29T01 :00: 00 | PST | 2024-07-28T18 :00: 00 |
  | 2024-07-30T01 :00: 00-05:00 | *gebrek GMT* | 2024-07-30T06 :00: 00 | GMT | 2024-07-30T06 :00: 00 |
  | 2024-07-30T01 :00: 00-05:00 | *gebrek GMT* | 2024-07-30T06 :00: 00 | PST | 2024-07-29T23 :00: 00 |
  | 2024-08-02 | *gebrek GMT* | 2024-08-02T00 :00: 00 | IST | 2024-08-02T05 :00: 00 |
  | 2024-07-29T01 :00: 00 | `America/`<br/>`Los_Angeles` | 2024-07-28T18 :00: 00 | PST | 2024-07-28T18 :00: 00 |
  | 2024-07-30T01 :00: 00-05:00 | `Australia/`<br/>`Sydney` | 2024-07-30T17 :00: 00 | CET | 2024-07-30T08 :00: 00 |

  Voor tijdzones met een verschuiving van 30 minuten (bijvoorbeeld IST, India Standard Time), wordt de verschuiving van 30 minuten verwijderd bij het rapporteren van beknopte gegevens. 12:30 wordt bijvoorbeeld gerapporteerd als 12:00.


Om ervoor te zorgen, wordt juiste timezone gebruikt voor uw per uur korrelige summiere gegevens, moet u het schema verzekeren dat voor summiere gegevens wordt gebruikt juiste gevormde timezone heeft.

Om granularity en timezone voor uw summiere gegevensschema te vormen, moet u de volgende API vraag gebruiken aangezien er geen gelijkwaardige beschikbare gebruikersinterface is.

```shell
curl -X POST \
https://platform.adobe.io/data/foundation/schemaregistry/tenant/descriptors \
 -H "Authorization: Bearer {$ACCESS_TOKEN}" \
 -H 'Content-Type: application/json' \
 -H 'x-api-key: {$API_KEY}' \
 -H 'x-gw-ims-org-id: {$ORG_ID}' \
 -H 'x-sandbox-name: {$SANDBOX_NAME}' \
 -d '{  
    "@type": "xdm:descriptorTimeSeriesGranularity",
    "xdm:sourceSchema": "{$SCHEMA_ID}",
    "xdm:sourceVersion": 1,
    "xdm:granularity": "{$GRANULARITY}",
    "xdm:ianaTimezone": "{$TIMEZONE}" 
 }'
```

| Variabele | Waarde |
|---|---|
| `$ACCESS_TOKEN`<br/>`$API_KEY`<br/>`$ORG_ID`<br/>`$SANDBOX_NAME` | Zie [ voor authentiek verklaren en toegang Experience Platform APIs ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication) voor meer informatie over hoe te om waarden voor deze variabelen te specificeren. |
| `$SCHEMA_ID` | U kunt identiteitskaart van uw schema in Experience Platform UI vinden. Selecteer het overzichtsschema in de lijst met schema&#39;s en zoek **[!UICONTROL API Usage]** > **[!UICONTROL Schema ID]** in het rechterdeelvenster. Gebruik die id als waarde. |
| `$GRANULARITY` | Geef `hour` of `day` op als waarde. |
| `$TIMEZONE` | Specificeer de juiste waarde van het tijdzoneherkenningsteken van de TZ herkenningstekenkolom in de [ Lijst van de tijdstreken van het karaktergegevensbestand ](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). Bijvoorbeeld: `America/Los_Angeles` . |

## Componentinstellingen

Controleer of de componentinstellingen voor een overzichtsgegevensgroep gelijk zijn. Zie [ Samenvattende de componentenmontages van de gegevensgroep ](component-settings/summary-data-group.md#same-component-settings) voor meer details.

>[!MORELIKETHIS]
>
>Zie [ Samenvatten en gebruik summiere gegevens ](/help/use-cases/data-views/summary-data.md) artikel voor een gedetailleerd gebruiksgevalvoorbeeld op hoe te en rapport over summiere gegevens te gebruiken.
