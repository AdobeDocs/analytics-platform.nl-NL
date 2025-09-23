---
title: Systeemeigen oplossingen voor gegevenspakhuis configureren
description: Begrijp hoe te om gegevenspakhuis inheemse oplossingen voor Experience Platform Data Mirror voor Customer Journey Analytics te vormen
solution: Customer Journey Analytics
feature: Basics
role: Admin
hide: true
hidefromtoc: true
badgePremium: label="Beta"
exl-id: 92cffcc5-d7a7-47f5-869d-1fc665594bf4
source-git-commit: b585187f112c2081a8e51bd84d9f95e75ceebdc3
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Systeemeigen oplossingen voor gegevenspakhuis configureren

{{release-limited-testing}}

Om Experience Platform Data Mirror for Customer Journey Analytics te ondersteunen, moeten de gegevens die u wilt gebruiken van de drie ondersteunde native oplossingen voor gegevensopslagruimten ([[!DNL Azure Databricks]](#azure-databricks), [[!DNL Google BigQuery]](#google-bigquery), [[!DNL Snowflake]](#snowflake) ) zijn ingeschakeld voor het vastleggen van wijzigingsgegevens.


## [!DNL Azure Databricks]

Laat **invoer van veranderingsgegevens** in uw [!DNL Azure Databricks] lijsten toe om veranderingsgegevens te gebruiken vangen in uw bronverbinding.

Gebruik de volgende opdrachten om de invoer van wijzigingsgegevens in uw tabellen in te schakelen:

**Nieuwe lijst**

Als u de gewijzigde gegevensinvoer wilt toepassen op een nieuwe tabel, moet u de tabeleigenschap `delta.enableChangeDataFeed` instellen op `TRUE` in de opdracht `CREATE TABLE` .

```sql
CREATE TABLE student (id INT, name STRING, age INT) TBLPROPERTIES (delta.enableChangeDataFeed = true)
```

**Bestaande lijst**

Als u een gewijzigde gegevensfeed wilt toepassen op een bestaande tabel, moet u de tabeleigenschap `delta.enableChangeDataFeed` instellen op `TRUE` in de opdracht `ALTER TABLE` .

```sql
ALTER TABLE myDeltaTable SET TBLPROPERTIES (delta.enableChangeDataFeed = true)
```

**Alle nieuwe lijsten**

Als u de gegevensfeed change wilt toepassen op alle nieuwe tabellen, moet u de standaardeigenschappen instellen op `TRUE` .

```sql
set spark.databricks.delta.properties.defaults.enableChangeDataFeed = true;
```

Voor meer informatie, lees de [[!DNL Azure Databricks]  gids bij het toelaten van de voer van veranderingsgegevens ](https://docs.databricks.com/aws/en/delta/delta-change-data-feed#enable-change-data-feed).

Lees de volgende documentatie voor stappen over het inschakelen van het vastleggen van wijzigingsgegevens voor uw [!DNL Azure Databricks] bronverbinding:

* [ creeer a [!DNL Azure Databricks]  basisverbinding ](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/api-tutorials/create/databases/databricks).
* [ creeer een bronverbinding voor een gegevensbestand ](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/api-tutorials/collect/database-nosql#create-a-source-connection).

## [!DNL Google BigQuery]

Als u het vastleggen van wijzigingsgegevens wilt gebruiken in de [!DNL Google BigQuery] -bronverbinding, navigeert u naar de [!DNL Google BigQuery] -pagina in de [!DNL Google Cloud] -console en stelt u `enable_change_history` in op `TRUE` . Met deze eigenschap wordt de wijzigingshistorie voor uw gegevenstabel ingeschakeld.

Voor meer informatie, lees de gids over [ de taalverklaringen van de gegevensdefinitie in  [!DNL GoogleSQL] ](https://cloud.google.com/bigquery/docs/reference/standard-sql/data-definition-language#table_option_list).

Lees de volgende documentatie voor stappen over het inschakelen van het vastleggen van wijzigingsgegevens voor uw [!DNL Google BigQuery] bronverbinding:

* [ creeer a [!DNL Google BigQuery]  basisverbinding ](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/api-tutorials/create/databases/bigquery).
* [ creeer een bronverbinding voor een gegevensbestand ](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/api-tutorials/collect/database-nosql#create-a-source-connection).

## [!DNL Snowflake]

Laat **verandering het volgen** in uw [!DNL Snowflake] lijsten toe om veranderingsgegevens te gebruiken vangen in uw bronverbindingen.

Schakel in [!DNL Snowflake] de optie Wijzigingen bijhouden in met de waarden `ALTER TABLE` en `CHANGE_TRACKING` op `TRUE` .

```sql
ALTER TABLE mytable SET CHANGE_TRACKING = TRUE
```

Voor meer informatie, lees de [[!DNL Snowflake]  gids bij het gebruiken van de veranderingsclausule ](https://docs.snowflake.com/en/sql-reference/constructs/changes#usage-notes).

Lees de volgende documentatie voor stappen over het inschakelen van het vastleggen van wijzigingsgegevens voor uw [!DNL Snowflake] bronverbinding:

* [ creeer a [!DNL Snowflake]  basisverbinding ](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/api-tutorials/create/databases/snowflake).
* [ creeer een bronverbinding voor een gegevensbestand ](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/api-tutorials/collect/database-nosql#create-a-source-connection).


>[!MORELIKETHIS]
>
>[ Data Mirror snelle startgids: Spiegel en gebruik op model-gebaseerde gegevens ](model-based.md)
>
