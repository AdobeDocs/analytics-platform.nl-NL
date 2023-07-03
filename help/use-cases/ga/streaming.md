---
title: Gegevens voor streaming Google Analytics configureren in Adobe Experience Platform
description: Leer hoe u uw implementatie instelt voor het verzenden van een Google-gegevenslaag naar Adobe Experience Platform
exl-id: 58854f4b-ae28-424e-a2cf-0e76219cb802
feature: Use Cases
source-git-commit: edbad9c9d3dc0b48db5334828a18ef652d4a38aa
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Gegevens voor streaming Google Analytics configureren in Adobe Experience Platform

Deze pagina concentreert zich op hoe te om uw levende Google Analytics gegevens in Adobe Experience Platform in te voeren, toestaand u om die dataset in een Mening van Gegevens binnen Customer Journey Analytics van verwijzingen te voorzien. U kunt de stappen op deze pagina combineren met [Historische gegevens van Google Analytics opnemen in Adobe Experience Platform](backfill.md), die een gegevensset met historische gegevens genereert. Combineer een het stromen dataset met een backfill dataset om een naadloze mening van verleden en heden gegevens in Customer Journey Analytics te krijgen.

Het vormen van gegevensinzameling impliceert de volgende stappen:

1. Implementeren [Tags voor Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html). Zie de [Snelstartgids](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) om een basisimplementatie op gang te brengen.
1. Installeer de [Google Data Layer-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/google-data-layer/overview.html). Deze extensie fungeert als alternatief voor het installeren van de Web SDK-extensie, die specifiek is gericht op een Google-gegevenslaag.
1. [Een DataStream maken](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html) in Adobe Experience Platform Data Collection. Configureer de DataStream om gegevens naar Adobe Experience Platform te verzenden. U moet momenteel elk Google-gegevenslaagobject hier toewijzen aan een toepasselijk XDM-veld. Adobe is van plan deze toewijzingsworkflow in de toekomst te vereenvoudigen.

Nadat u de gewenste tags op uw site hebt geïmplementeerd en gepubliceerd, kunt u doorgaan naar [Verbinding maken](/help/connections/create-connection.md)vervolgens [Een gegevensweergave maken](/help/data-views/create-dataview.md).
