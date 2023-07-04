---
title: Reisanalyse Kanaal
description: Analyseer en extraheer inzichten van klanteninteractie over de klantenreis.
exl-id: 285532b1-eb37-4984-9559-054a18515ddf
solution: Customer Journey Analytics
feature: Use Cases, Cross-Channel Analysis
source-git-commit: 73496ea3c8341d9db7e879a4f5ae4f35893c605d
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Kanaaloverschrijdende analyse

De analyse tussen kanalen laat één enkele geconsolideerde mening van klantengedrag over diverse kanalen door gegevens van diverse Web, mobiele, en off-line eigenschappen te verenigen toe. U kunt deze geconsolideerde weergave bijvoorbeeld gebruiken om de interactie van klanten op verschillende desktops en mobiele apparaten te analyseren, zodat u het gedrag van klanten begrijpt en inzichten kunt ophalen om de beleving van digitale klanten te optimaliseren. U kunt klanteninteractie over kanalen, met inbegrip van digitale en off-line kanalen zoals steuninteractie en in-store aankopen ook analyseren om de klantenreis beter te begrijpen en te optimaliseren.

## Workflow

![Kanaalarchitectuur](../assets/cca-architecture.png)

## Implementatiestappen

1. [Schema&#39;s maken](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) voor gegevens die moeten worden ingevoerd.
1. [Gegevenssets maken](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/create-datasets-and-ingest-data.html) voor gegevens die moeten worden ingevoerd.
1. [Gegevens in Experience Platform opnemen](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/understanding-data-ingestion.html):
   1. Op gebeurtenissen gebaseerde gegevens ![event](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg) van website of mobiele toepassing via de Edge Network of Analytics Data Connector.
   2. Profielgegevens ![profiel](https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg) (bijvoorbeeld van een systeem van CRM, vraag centrumtoepassing, loyaliteitstoepassing).
   3. Gegevens opzoeken ![opzoeken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) (bijvoorbeeld productnaam, categorie van een productinformatiesysteem).

1. Gebruik een gemeenschappelijke namespaceidentiteitskaart over datasets. Gebruiken [Stiksel](../../stitching/overview.md) om om het even welke op gebeurtenis-gebaseerde dataset op te heffen ![gegevens vernieuwen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataRefresh_18_N.svg) voor het verstrekken van de gemeenschappelijke id op elke rij. Merk op dat Customer Journey Analytics momenteel niet de diensten van het Profiel van het Experience Platform of van de Identiteit voor het stitching gebruikt.
1. Voer om het even welke voorbereiding van douanegegevens uit om een gemeenschappelijke sleutel over tijdreeksdatasets te verzekeren die in Customer Journey Analytics moeten worden opgenomen.
1. Opzoekgegevens een primaire id geven die kan worden gekoppeld aan een veld in de gebeurtenisgegevens. Telt als rijen in licentie.
1. Stel dezelfde primaire id voor profielgegevens in als de primaire id van de gebeurtenisgegevens.
1. [Verbinding maken](../../connections/overview.md) om de desbetreffende gegevensreeksen van Experience Platform aan Customer Journey Analytics in te voeren.
1. [Een gegevensweergave maken](/help/data-views/create-dataview.md) op de verbinding om de specifieke afmetingen en metriek te selecteren die in de mening moeten worden omvat. Attributie- en toewijzingsinstellingen worden ook geconfigureerd in de gegevensweergave. Deze instellingen worden tijdens het rapport berekend.
1. [Een project maken](/help/analysis-workspace/home.md) om dashboards en rapporten binnen Analysis Workspace te vormen.

## Overwegingen

Zorg ervoor dat u bij het instellen van deze workflow rekening houdt met de volgende punten.

* Voor het analyseren van gegevens tussen kanalen is dezelfde id-naamruimte vereist voor elke record.
* Het verenigingsproces van het verenigen van verschillende datasets vereist een gemeenschappelijke primaire persoon/entiteitsleutel over de datasets.
* Secundaire op sleutels gebaseerde unies worden momenteel niet ondersteund.
* Het stitching proces staat voor het opnieuw teweegbrengen van identiteiten in rijen toe die op voorbijgaande identiteitskaart (zoals een authentificatie ID) informatie van verslagen worden gebaseerd die zelfde blijvende identiteitskaart delen.Dit staat voor het oplossen van ongelijksoortige verslagen aan één enkele gestikte identiteitskaart voor analyse op het persoonniveau, eerder dan op het apparaat of koekjesniveau toe.
* Objecten en kenmerken van hetzelfde XDM-veld worden samengevoegd in één dimensie in Customer Journey Analytics. Om veelvoudige attributen van diverse datasets in de zelfde dimensie van Customer Journey Analytics samen te voegen, zouden de datasets het zelfde XDM gebied of schema moeten van verwijzingen voorzien.

