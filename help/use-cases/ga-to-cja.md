---
title: Google Analytics instellen die rapporteren in Customer Journey Analytics
description: null
translation-type: tm+mt
source-git-commit: 1324ad5768a7ab215431b9447d9519367dfe17a0
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# Google Analytics instellen die rapporteren in Customer Journey Analytics



## Vereisten

* Toegang tot Adobe Experience Platform
* Toegang tot Universal Google Analytics (versie Google Analytics 360) of Google Analytics 4 (versie met gratis versie of versie Google Analytics 360)
* Toegang tot Customer Journey Analytics

## 1. Gegevens van Google Analytics verbinden met Adobe Experience Platform

Hoe u gegevens van Google Analytics in Adobe Experience Platform brengt hangt van welke versie van Google Analytics af u gebruikt:

| Als u... | U hebt deze licentie ook nodig... | En doe dit... |
| --- | --- | --- |
| **Universele Google Analytics** | Google Analytics 360 | Voer stap 1 - x van de onderstaande instructies uit |
| **Google Analytics 4** | Gratis GA-versie of Google Analytics 360 | Geen noodzaak voor stap x in de onderstaande instructies. |

De volgende instructies zijn gebaseerd op Universal Google Analytics.

1. Verbind uw gegevens van Google Analytics met BigQuery en
Zie [deze instructies](https://support.google.com/analytics/answer/3416092?hl=en).

1. (Alleen voor Universal Analytics-klanten) Transformeer Google Analytics-sessies naar gebeurtenissen in BigQuery.
Hierdoor zijn de gegevens compatibel met Adobe Experience Platform. Zie [deze instructies](https://support.google.com/analytics/answer/3437618?hl=en).

   Details: In BigQuery worden uw GA-gegevens weergegeven als een tabel:

   ![](assets/ga-bigquery.png)
U moet een SQL vraag tot stand brengen om de Universele gegevens van Analytics in een ervaring-Platform-volgzaam formaat om te zetten. Bekijk deze video voor instructies:

   >[!VIDEO](https://video.tv.adobe.com/v/332634)

1. Exporteer Google Analytics-gebeurtenissen in JSON-indeling naar Google Cloud Storage en sla deze op in een emmertje.
Zie [deze instructies](https://support.google.com/analytics/answer/3437719?hl=en&amp;ref_topic=3416089).

1. Breng de gegevens van Google Cloud Storage in Experience Platform.
Bekijk deze video voor instructies:

   >[!VIDEO](https://video.tv.adobe.com/v/332641)

1. GCS-gebeurtenissen importeren naar Adobe Experience Platform en toewijzen aan XDM-schema

Exportschema voor BigQuery (https://support.google.com/analytics/answer/3437719?hl=en&amp;ref_topic=3416089)

