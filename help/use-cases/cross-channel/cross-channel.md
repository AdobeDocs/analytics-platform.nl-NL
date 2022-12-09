---
title: Reisanalyse Kanaal
description: Analyseer en extraheer inzichten van klanteninteractie over de klantenreis.
exl-id: 285532b1-eb37-4984-9559-054a18515ddf
solution: Customer Journey Analytics
feature: Use Cases
source-git-commit: dbb7edae43fdc970cacf5863ecd13df75deaefad
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Reisanalyse Kanaal

Eén geconsolideerde weergave van het gedrag van klanten op verschillende kanalen hebben door gegevens van verschillende web-, mobiele en offline eigenschappen te verenigen. U kunt deze geconsolideerde weergave bijvoorbeeld gebruiken om de interactie van klanten op verschillende desktops en mobiele apparaten te analyseren, zodat u het gedrag van klanten begrijpt en inzichten kunt ophalen om de beleving van digitale klanten te optimaliseren. U kunt klanteninteractie over kanalen, met inbegrip van digitale en off-line kanalen zoals steuninteractie en in-store aankopen ook analyseren om de klantenreis beter te begrijpen en te optimaliseren.

## Architectuur

![Kanaalarchitectuur](../assets/cross-channel-architecture.svg)

## Implementatiestappen

1. [Schema&#39;s maken](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) voor gegevens die moeten worden ingevoerd.
1. [Gegevenssets maken](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/create-datasets-and-ingest-data.html) voor gegevens die moeten worden ingevoerd.
1. [Gegevens in Experience Platform opnemen](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/understanding-data-ingestion.html).
1. Een gemeenschappelijke naamruimte-id gebruiken in verschillende gegevenssets of gebruiken [Kanaaloverschrijdende analyse](/help/connections/cca/overview.md) om mensen aan elkaar te koppelen. Merk op dat Customer Journey Analytics momenteel niet de diensten van het Profiel van het Experience Platform of van de Identiteit voor het stitching gebruikt.
1. Voer om het even welke voorbereiding van douanegegevens uit om een gemeenschappelijke sleutel over tijdreeksdatasets te verzekeren die in Customer Journey Analytics moeten worden opgenomen.
1. Opzoekgegevens een primaire id geven die kan worden gekoppeld aan een veld in de gebeurtenisgegevens. Telt als rijen in licentie.
1. Stel dezelfde primaire id voor profielgegevens in als de primaire id van de gebeurtenisgegevens.
1. Configureer een gegevensverbinding om gegevens van Experience Platform tot Customer Journey Analytics in te voeren.
1. [Een gegevensweergave maken](/help/data-views/create-dataview.md) op de verbinding om de specifieke afmetingen en metriek te selecteren die in de mening moeten worden omvat. Attributie- en toewijzingsinstellingen worden ook geconfigureerd in de gegevensweergave. Deze instellingen worden tijdens het rapport berekend.
1. Creeer een project om dashboards en rapporten binnen Analysis Workspace te vormen.

## Overwegingen

Zorg ervoor dat u bij het instellen van deze workflow rekening houdt met de volgende punten.

* Voor het analyseren van gegevens tussen kanalen is dezelfde id-naamruimte vereist voor elke record.
* Het verenigingsproces van het verenigen van verschillende datasets vereist een gemeenschappelijke primaire persoon/entiteitsleutel over de datasets.
* Secundaire op sleutels gebaseerde unies worden momenteel niet ondersteund.
* Het op gebied-gebaseerde identiteitsstitching proces staat voor het opnieuw teweegbrengen van identiteiten in rijen toe die op verdere voorbijgaande verslagen van identiteitskaart, zoals een authentificatieidentiteitskaart worden gebaseerd. Hierdoor kunnen afwijkende records op één id worden omgezet voor analyse op het niveau van de persoon in plaats van op het apparaat of cookie.
* Objecten en kenmerken van hetzelfde XDM-veld worden samengevoegd in één dimensie in Customer Journey Analytics. Om veelvoudige attributen van diverse datasets in de zelfde dimensie van Customer Journey Analytics samen te voegen, zouden de datasets het zelfde XDM gebied of schema moeten van verwijzingen voorzien.
