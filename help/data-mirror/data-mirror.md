---
title: Data Mirror - Overzicht
description: Begrijp hoe te om gegevens tussen datapakhuis inheemse oplossingen en Customer Journey Analytics te synchroniseren
solution: Customer Journey Analytics
feature: Basics
role: Admin
badgePremium: label="Beta"
exl-id: f40e1263-1f4a-416c-a045-15fbe68ce509
source-git-commit: c9d7a4596a842ab7d949364e3469747d20ca15b4
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 1%

---

# Experience Platform Data Mirror - overzicht

{{release-limited-testing}}

Data Mirror is een capaciteit van Experience Platform die rij-vlakke veranderingsopname van externe gegevensbestanden in het gegevensmeer gebruikend relationele schema&#39;s toelaat. Het bewaart gegevensverhoudingen, dwingt uniciteit af, en steunt versioning zonder upstream extractie, transformatie, en ladings (ETL) processen te vereisen.

Met Experience Platform Data Mirror kunt u invoegtoepassingen, updates en verwijderingen (muteerbare gegevens) rechtstreeks met gegevens in Experience Platform synchroniseren vanuit externe native oplossingen voor gegevenspakken ([!DNL Snowflake], [!DNL Azure Databricks] of [!DNL Google BigQuery] ). Met Data Mirror kunt u de bestaande structuur en gegevensintegriteit van het databasemodel behouden wanneer u gegevens naar Experience Platform overbrengt.

## Capaciteiten en voordelen

Data Mirror biedt de volgende essentiële mogelijkheden voor databasesynchronisatie:

* **Primaire zeer belangrijke handhaving.** Zorgt voor unieke gegevenssets en voorkomt dubbele records tijdens inname.
* **de verandering van het rij-niveau opname.** Ondersteunt wijzigingen in korrelgegevens, waaronder upserts en delete met precisiecontrole.
* **relaties van het Schema.** Hiermee schakelt u externe en primaire-sleutelrelaties tussen gegevenssets in via beschrijvingen.
* **uit-van-orde gebeurtenis behandeling.** Verwerkt veranderingsgebeurtenissen gebruikend versie en timestamp beschrijvers, zelfs wanneer zij uit opeenvolging aankomen.
* **Directe pakhuis integratie.** Verbindt met gesteunde de pakhuizen van wolkengegevens voor veranderingssynchronisatie in real time.

Gebruik Data Mirror om wijzigingen rechtstreeks van uw bronsystemen in te voeren, de schemacontegriteit af te dwingen en de gegevens beschikbaar te stellen voor analyses, reisorchestratie en compatibiliteitsworkflows. Data Mirror elimineert complexe stroomopwaartse processen ETL en versnelt implementatie door direct het weerspiegelen van bestaande gegevensbestandmodellen toe te laten. Deze verwijdering kan het gegevensbeheer verbeteren door een nauwkeurige controle op schrappingen en gegevenshygiënische activiteiten.

Zie ook de [&#x200B; documentatie van Experience Platform op Data Mirror &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/data-mirror/overview){target="_blank"}.

## Data Mirror voor Customer Journey Analytics

>[!NOTE]
>
>Het vermogen van Experience Platform Data Mirror voor Customer Journey Analytics is beschikbaar in a **openbare bèta** tot 25 Maart, 2026. Klanten kunnen per dag maximaal 2 miljoen rijen wijzigen in het Adobe Experience Platform Data Lake via bronconnectors. Adobe behoudt zich het recht voor om bètatoegang tot de functionaliteit van Experience Platform Data Mirror te beëindigen als uw organisatie deze limiet overschrijdt. <br/> om toegang tot dit vermogen te verzoeken, gelieve uw Adobe accountteam te contacteren.
>

Experience Platform Data Mirror for Customer Journey Analytics is beschikbaar voor geselecteerde native oplossingen voor gegevensopslagruimten ([!DNL Azure Databricks], [!DNL Google BigQuery] en [!DNL Snowflake]). De Customer Journey Analytics-versie van Experience Platform Data Mirror vereist een correcte configuratie van de volgende toepassingen of onderdelen:

* [Native oplossingen voor gegevenspakhuis](datawarehouse.md)
* [Experience Platform](aep.md)
* [Customer Journey Analytics](cja.md)

>[!MORELIKETHIS]
>
>[&#x200B; Data Mirror snelle startgids: Spiegel en gebruik relationele gegevens &#x200B;](relational.md)
>[Data Mirror (de documentatie van Experience Platform) &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/data-mirror/overview)
>[Relationele schema&#39;s (documentatie van Experience Platform) &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/relational)
