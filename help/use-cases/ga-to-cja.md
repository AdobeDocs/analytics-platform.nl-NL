---
title: Google Analytics in Adobe Experience Platform krijgen voor analyse in Customer Journey Analytics (CJA)
description: 'Verklaart hoe te hefboomwerking Customer Journey Analytics (CJA) om uw Google Analytics en firebase gegevens in Adobe Experience Platform in te voeren. '
exl-id: 314378c5-b1d7-4c74-a241-786198fa0218
translation-type: tm+mt
source-git-commit: 793b2ce4ec8a487f6c4290fe2eff00879fcca13d
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---


# Gegevens van Google Analytics opnemen in Adobe Experience Platform

Dit gebruiksgeval concentreert zich op hoe te om uw gegevens van Google Analytics als dataset in Adobe Experience Platform in te nemen. (Dit geldt zowel voor historische als voor live gegevens.) Zodra gedaan, kunt u beide datasets combineren om een dwars-apparatenmening van de reis van uw gebruiker te bereiken.

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
| **Universele Google Analytics** | Google Analytics 360 | Voer stap 1 - 5 van de onderstaande instructies uit |
| **Google Analytics 4** | Gratis GA-versie of Google Analytics 360 | Voer stap 1 en 3-5 van de onderstaande instructies uit. Geen behoefte aan stap 2. |

## 1. Verbind uw gegevens van Google Analytics met BigQuery

De volgende instructies zijn gebaseerd op Universal Google Analytics.

Zie [deze instructies](https://support.google.com/analytics/answer/3416092?hl=en).

## 2. Google Analytics-sessies transformeren naar gebeurtenissen in BigQuery

>[!IMPORTANT]
>
>Deze stap is alleen van toepassing op klanten van Universal Analytics

GA-gegevens slaan elke record in de gegevens op als een gebruikerssessie in plaats van als afzonderlijke gebeurtenissen. Door de gegevens te transformeren, zijn de gegevens compatibel met Adobe Experience Platform.

Zie [deze instructies](https://support.google.com/analytics/answer/3437618?hl=en).

U moet een SQL vraag tot stand brengen om de Universele gegevens van Analytics in een ervaring-Platform-volgzaam formaat om te zetten. Bekijk deze video voor instructies:

>[!VIDEO](https://video.tv.adobe.com/v/332634)

## 3. Exporteer Google Analytics-gebeurtenissen in JSON-indeling naar Google Cloud Storage en sla deze op in een emmertje

Zie [deze instructies](https://support.google.com/analytics/answer/3437719?hl=en&amp;ref_topic=3416089).

## 4. De gegevens van Google Cloud Storage in Experience Platform brengen

Bekijk deze video voor instructies:

>[!VIDEO](https://video.tv.adobe.com/v/332641)

## 5. GCS-gebeurtenissen importeren naar Adobe Experience Platform en toewijzen aan XDM-schema

Exportschema voor BigQuery (https://support.google.com/analytics/answer/3437719?hl=en&amp;ref_topic=3416089)
