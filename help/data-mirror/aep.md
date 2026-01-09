---
title: Experience Platform configureren
description: Begrijp hoe te om schema's en datasets voor Experience Platform Data Mirror voor Customer Journey Analytics te vormen
solution: Customer Journey Analytics
feature: Basics
role: Admin
badgePremium: label="Beta"
exl-id: 87593d7d-9456-48f8-8d39-5c3d95fe51ec
source-git-commit: cd3baec708f1811a7cbc37dfe0a9c3af75eb97c3
workflow-type: tm+mt
source-wordcount: '550'
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

U moet a [&#x200B; relationeel schema &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/relational){target="_blank"} tot stand brengen dat de inheemse lijst van het gegevenspakhuis is u wilt spiegelen. Wanneer u het relationele schema construeert, zorg ervoor dat aan de volgende vereisten wordt voldaan:

* Wanneer ertoe aangezet voor het type van relationeel schema, zorg ervoor u de handoptie selecteert.
* Selecteer het juiste schema voor het type gegevens. Experience Platform Data Mirror wordt vooral gebruikt voor tijdreeksgegevens (bijvoorbeeld gebeurtenisgegevens), maar kan ook worden gebruikt voor op records gebaseerde gegevens (opzoeken en profiel).

* De velden in uw schema en de bijbehorende kenmerken definiëren
* Configureer de vereiste kenmerken voor velden in een relationeel schema:

   * **Primaire sleutel**.
   * **beschrijver van de Versie**, die als opeenvolgend aantal (het gebiedstype van het Geheel Geheel) of als Datumtime gebiedstype moet worden gevormd. Wanneer u een DateTime-veldtype gebruikt, definieert de versiedescriptor het tijdstempel van een wijziging van de gegevens, bijvoorbeeld om een laatst gewijzigde tijdstempel te bevatten.
   * **de beschrijver van de Chronologie** (voor tijdreeksgegevens), die onveranderlijke timestamp op het ogenblik bepaalt dat een gebeurtenis wordt gevangen. De tijdstempeldescriptor is niet vereist voor een op records gebaseerd relationeel schema.



## Gegevensset

U kunt opstelling vooraf een dataset voor uw schema, of een dataset tot stand brengen wanneer u opstelling uw bronschakelaar.
Wanneer u een dataset vooraf creeert of een dataset selecteert, verzeker u het gegevensgebruik een relationeel [&#x200B; schema &#x200B;](#schema) u vroeger creeerde.


## Source-connector

Aan opstelling gebruikt de bronschakelaar aan de gesteunde inheemse oplossingen van het gegevenspakhuis, u het bronwerkschema dat u door de opstelling begeleidt. Die workflow bestaat uit de volgende stappen:

### Verificatie

Voor authentificatie tegen de gesteunde gegevens pakhuis inheemse oplossing, zie de relevante documentatie van Experience Platform:

* [&#x200B; Azure Databricks &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/databases/databricks)
* [&#x200B; Google BigQuery &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/databases/bigquery)
* [&#x200B; Snowflake &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/databases/snowflake)


### Gegevens selecteren

Zodra met succes verbonden met uw met gegevens pakhuis inheemse oplossing, selecteer de lijst van de inheemse oplossing van het gegevenspakhuis u voor gegevenspiegel wilt gebruiken. Wanneer deze optie is geselecteerd, wordt een voorvertoning van de inhoud van de gegevens weergegeven.


### Gegevens

Zorg ervoor dat u het vastleggen van wijzigingsgegevens inschakelt. Er wordt een informatievenster weergegeven waarin de vereisten voor het vastleggen van wijzigingsgegevens worden uitgelegd.

Geef een nieuwe of bestaande gegevensset op die is gebaseerd op het relationele schema dat u eerder hebt gemaakt. Specificeer en selecteer andere opties in de Dataflow detailinterface.


### Toewijzing

Wijs de gebieden van de lijst in de inheemse oplossing van het gegevenspakhuis aan de gebieden toe die u voor het relationele schema hebt gespecificeerd.


### Planning

Bepaal een programma om de gegevens van de lijst in de inheemse oplossing van het gegevenspakhuis aan de dataset in Experience Platform te weerspiegelen.


### Controleren

Herzie de montages voor de bronschakelaar aan de inheemse oplossing van het gegevenspakhuis die gegevenspiegel en veranderingsgegevens vangt steunt.


Zodra u de opstelling van de bronschakelaar beëindigde, wordt een dataflow gecreeerd. Vanaf dat ogenblik op gegevensveranderingen (tussenvoegsels, updates, schrappingen) in het gegevenspakhuis wordt de inheemse oplossing weerspiegeld aan de gespecificeerde dataset.


>[!MORELIKETHIS]
>
>[&#x200B; Data Mirror snelle startgids: Spiegel en gebruik relationele gegevens &#x200B;](relational.md)
>[Data Mirror (de documentatie van Experience Platform) &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/data-mirror/overview)
>[Relationele schema&#39;s (documentatie van Experience Platform) &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/relational)
