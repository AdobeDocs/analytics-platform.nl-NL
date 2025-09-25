---
title: Experience Platform configureren
description: Begrijp hoe te om schema's en datasets voor Experience Platform Data Mirror voor Customer Journey Analytics te vormen
solution: Customer Journey Analytics
feature: Basics
role: Admin
badgePremium: label="Beta"
exl-id: 87593d7d-9456-48f8-8d39-5c3d95fe51ec
source-git-commit: edf7bdac87d9bed48244ad80521bbbf83c48f7b6
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Experience Platform configureren

{{release-limited-testing}}

Experience Platform Data Mirror for Customer Journey Analytics vereist de juiste configuratie van verschillende Experience Platform-componenten:

* schema
* gegevensset
* bronaansluiting

Zoek onder details die u zou moeten overwegen wanneer het vormen van elk van deze componenten.

## Schema

U moet a [ model-gebaseerd schema ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/model-based){target="_blank"} tot stand brengen dat modellen de gegevens pakhuis inheemse lijst u wilt spiegelen. Wanneer u het model-gebaseerde schema construeert, zorg ervoor dat aan de volgende vereisten wordt voldaan:

* Wanneer ertoe aangezet voor het type van op model-gebaseerd schema, zorg ervoor u de handoptie selecteert.
* Selecteer het juiste schema voor het type gegevens. Experience Platform Data Mirror wordt vooral gebruikt voor tijdreeksgegevens (bijvoorbeeld gebeurtenisgegevens).

* De velden in uw schema en de bijbehorende kenmerken definiëren
* Configureer de vereiste kenmerken voor velden in een op een model gebaseerd schema:

   * primaire sleutel
   * versie-id
   * tijdstempel-id (voor tijdreeksgegevens).

## Gegevensset

U kunt opstelling vooraf een dataset voor uw schema, of een dataset tot stand brengen wanneer u opstelling uw bronschakelaar.
Wanneer u een dataset vooraf creeert of een dataset selecteert, verzeker u het gegevensgebruik een op model-gebaseerd [ schema ](#schema) u vroeger creeerde.


## Source-connector

Aan opstelling gebruikt de bronschakelaar aan de gesteunde inheemse oplossingen van het gegevenspakhuis, u het bronwerkschema dat u door de opstelling begeleidt. Die workflow bestaat uit de volgende stappen:

### Verificatie

Voor authentificatie tegen de gesteunde gegevens pakhuis inheemse oplossing, zie de relevante documentatie van Experience Platform:

* [ Azure Databricks ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/databases/databricks)
* [ Google BigQuery ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/databases/bigquery)
* [ Snowflake ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/databases/snowflake)


### Gegevens selecteren

Zodra met succes verbonden met uw met gegevens pakhuis inheemse oplossing, selecteer de lijst van de inheemse oplossing van het gegevenspakhuis u voor gegevenspiegel wilt gebruiken. Wanneer deze optie is geselecteerd, wordt een voorvertoning van de inhoud van de gegevens weergegeven.


### Gegevens

Zorg ervoor dat u het vastleggen van wijzigingsgegevens inschakelt. Er wordt een informatievenster weergegeven waarin de vereisten voor het vastleggen van wijzigingsgegevens worden uitgelegd.

Geef een nieuwe of bestaande gegevensset op die is gebaseerd op het model-gebaseerde schema dat u eerder hebt gemaakt. Specificeer en selecteer andere opties in de Dataflow detailinterface.


### Toewijzing

Wijs de gebieden van de lijst in de inheemse oplossing van het gegevenspakhuis aan de gebieden toe die u voor het op model-gebaseerde schema hebt gespecificeerd.


### Planning

Bepaal een programma om de gegevens van de lijst in de inheemse oplossing van het gegevenspakhuis aan de dataset in Experience Platform te weerspiegelen.


### Controleren

Herzie de montages voor de bronschakelaar aan de inheemse oplossing van het gegevenspakhuis die gegevenspiegel en veranderingsgegevens vangt steunt.


Zodra u de opstelling van de bronschakelaar beëindigde, wordt een dataflow gecreeerd. Vanaf dat ogenblik op gegevensveranderingen (tussenvoegsels, updates, schrappingen) in het gegevenspakhuis wordt de inheemse oplossing weerspiegeld aan de gespecificeerde dataset.


>[!MORELIKETHIS]
>
>[ Data Mirror snelle startgids: Spiegel en gebruik op model-gebaseerde gegevens ](model-based.md)
>&#x200B;>[Data Mirror (de documentatie van Experience Platform) ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/data-mirror/overview)
>&#x200B;>[Model-gebaseerde schema&#39;s (de documentatie van Experience Platform) ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/model-based)
