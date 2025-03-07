---
title: Streaming Google Analytics-gegevens configureren
description: Leer hoe u uw implementatie instelt voor het verzenden van een Google-gegevenslaag naar Adobe Experience Platform
exl-id: 58854f4b-ae28-424e-a2cf-0e76219cb802
feature: Use Cases
role: Admin
source-git-commit: 8262539078c57e32bc3195ef669325fa4889bea0
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Streaming Google Analytics-gegevens configureren

Deze pagina concentreert zich op hoe te om uw levende gegevens van Google Analytics in Adobe Experience Platform in te voeren, toestaand u om die dataset in een Mening van Gegevens in Customer Journey Analytics van verwijzingen te voorzien. U kunt de stappen op deze pagina met [ combineren de historische gegevens van Google Analytics in Adobe Experience Platform ](backfill.md), die een dataset produceert die historische gegevens bevat. Combineer een het stromen dataset met een backfill dataset om een naadloze mening van verleden en heden gegevens in Customer Journey Analytics te krijgen.

Het vormen van gegevensinzameling impliceert de volgende stappen:

1. Voer [ Markeringen voor Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html) uit. Zie de [ gids van de QuickStart ](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) om een basisimplementatie in werking te stellen en te krijgen.
1. Installeer de [ uitbreiding van de Laag van Gegevens van Google ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/google-data-layer/overview.html). Deze extensie fungeert als alternatief voor het installeren van de extensie Web SDK, die specifiek is gericht op een Google-gegevenslaag.
1. [ creeer een DataStream ](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html) in de Inzameling van Gegevens van Adobe Experience Platform. Configureer de DataStream om gegevens naar Adobe Experience Platform te verzenden. U moet momenteel elk Google-gegevenslaagobject hier toewijzen aan een toepasselijk XDM-veld. Adobe is van plan deze toewijzingsworkflow in de toekomst te vereenvoudigen.

Zodra u uitvoert en de gewenste markeringen op uw plaats publiceert, kunt u dan te werk gaan [ een verbinding ](/help/connections/create-connection.md) creëren, dan [ creeer een gegevensmening ](/help/data-views/create-dataview.md).
