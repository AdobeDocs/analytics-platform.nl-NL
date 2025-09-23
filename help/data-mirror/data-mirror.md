---
title: Data Mirror - Overzicht
description: Begrijp hoe te om gegevens tussen datapakhuis inheemse oplossingen en Customer Journey Analytics te synchroniseren
solution: Customer Journey Analytics
feature: Basics
role: Admin
hide: true
hidefromtoc: true
badgePremium: label="Beta"
source-git-commit: 9bd124ad651274b48052edc56bfb72358aa2d79a
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 1%

---

# Experience Platform Data Mirror - overzicht

{{release-limited-testing}}

Data Mirror is een vermogen van Experience Platform dat rij-vlakke veranderingsopname van externe gegevensbestanden in het gegevenshoek gebruikend model-gebaseerde schema&#39;s toelaat. Het bewaart gegevensverhoudingen, dwingt uniciteit af, en steunt versioning zonder upstream extractie, transformatie, lading (ETL) processen te vereisen.

Met Data Mirror kunt u invoegtoepassingen, updates en verwijderingen (muteerbare gegevens) vanuit externe gegevensopslagsystemen rechtstreeks synchroniseren met native oplossingen zoals [!DNL Snowflake] , [!DNL Azure Databricks] of [!DNL Google BigQuery] in Experience Platform. Met Data Mirror kunt u de bestaande structuur en gegevensintegriteit van het databasemodel behouden wanneer u gegevens naar Experience Platform overbrengt.


## Capaciteiten en voordelen

Data Mirror biedt de volgende essentiële mogelijkheden voor databasesynchronisatie:

* **Primaire zeer belangrijke handhaving**. Zorgt voor eenduidigheid binnen gegevenssets en voorkomt dubbele records tijdens inname.
* **row-vlakke veranderingsopname**. Ondersteunt wijzigingen in korrelige gegevens, waaronder upserts en delete met precisiecontrole.
* **verhoudingen van het Schema**. Laat buitenlandse en primaire zeer belangrijke verhoudingen tussen datasets door beschrijvers toe.
* **uit-van-orde gebeurtenis behandeling**. Verwerkt gebeurtenissen met versie- en tijdstempelbeschrijvingen, zelfs als deze uit de juiste volgorde komen.
* **Directe pakhuis integratie**. Verbindt met gesteunde douane van de wolkengegevens voor veranderingssynchronisatie in real time.

Gebruik Data Mirror om wijzigingen rechtstreeks van uw bronsystemen in te voeren, de schemacontegriteit af te dwingen en de gegevens beschikbaar te stellen voor analyses, reisorchestratie en compatibiliteitsworkflows. Data Mirror elimineert complexe stroomopwaartse processen ETL en versnelt implementatie door direct het weerspiegelen van bestaande gegevensbestandmodellen toe te laten. Deze verwijdering kan het gegevensbeheer verbeteren door een nauwkeurige controle op schrappingen en gegevenshygiënische activiteiten.

<!-- Add link when AEP docs are ready... -->

Zie ook de Experience Platform documentatie op Data Mirror.


## Data Mirror voor Customer Journey Analytics

>[!NOTE]
>
>Het vermogen van Experience Platform Data Mirror voor Customer Journey Analytics is beschikbaar in a **openbare bèta** tot 25 Maart, 2026. Tijdens de bètaperiode zijn CDC-updates (change data capture) beperkt tot 0,5% van de maandelijkse rijen met gegevens van uw organisatie. De maandelijkse rijen met gegevens zijn gebaseerd op uw jaarmachtigingen voor rijen met gegevens gedeeld door 12. Adobe behoudt zich het recht voor om de toegang tot de bètaversie van Experience Platform Data Mirror for Customer Journey Analytics te beëindigen als uw organisatie deze limiet overschrijdt.
>

De Experience Platform Data Mirror for Customer Journey Analytics-mogelijkheid is beschikbaar voor geselecteerde native oplossingen voor gegevensopslagruimten ([!DNL Azure Databricks], [!DNL Google BigQuery] en [!DNL Snowflake]). De Customer Journey Analytics-versie van de Data Mirror-functionaliteit vereist een correcte installatie en configuratie van verschillende onderdelen:

* [Eigen oplossing voor gegevenspakhuis](datawarehouse.md)
* [Experience Platform](aep.md)
* [Customer Journey Analytics](cja.md)


>[!MORELIKETHIS]
>
>[ Data Mirror snelle startgids: Spiegel en gebruik op model-gebaseerde gegevens ](data-mirror.md)
>