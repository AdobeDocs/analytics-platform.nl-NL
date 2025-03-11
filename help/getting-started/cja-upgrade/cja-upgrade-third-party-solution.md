---
title: Upgrade van een externe analyseoplossing naar Customer Journey Analytics
description: Leer hoe u van een externe analyseoplossing naar Customer Journey Analytics kunt upgraden
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: bc79ba1a-1153-4fe8-b265-9703a323c977
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Upgrade van een externe analyseoplossing naar Customer Journey Analytics {#upgrade-from-third-party}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-third-party"
>title="Een niet-Adobe Analytics-product"
>abstract="Een implementatie die gegevens verzamelt voor een ander product dan Adobe Analytics, zoals Google Analytics. Als u deze optie selecteert, worden verschillende opties in de upgradehandleiding uitgeschakeld die niet van toepassing zijn bij het upgraden naar Customer Journey Analytics vanuit een niet-Adobe Analytics-product."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

Het aanbevolen proces om van een andere analytische oplossing dan Adobe Analytics naar Customer Journey Analytics te upgraden is een nieuwe implementatie van de Experience Platform Web SDK, de voorkeursmethode voor gegevensverzameling voor Customer Journey Analytics. In combinatie met de Web SDK raadt Adobe ook aan historische gegevens van de oplossing voor analyse van derden in Adobe Experience Platform in te voeren.

<!-- After you have enough historical data using the Experience Platform Web SDK and you have fully transitioned to Customer Journey Analytics, the Analytics source connector can be turned off and the Web SDK can be used exclusively. -->

Gebruik het volgende proces wanneer u van een externe analyseoplossing, zoals Google Analytics, naar Customer Journey Analytics gaat:

1. Volg de [ Gedetailleerde geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#detailed-recommended-upgrade-steps).

   Deze stappen zijn bedoeld voor organisaties die een upgrade uitvoeren vanuit Adobe Analytics. Houd rekening met het volgende wanneer u deze stappen uitvoert:

   * U moet een gegevensstroom tot stand brengen.

   * U kunt geen projecten en componenten van een niet-Adobe Analytics oplossing migreren.

   * Afhankelijk van uw analyseoplossing, zou een bronschakelaar voor het opnemen van historische gegevens beschikbaar kunnen zijn. Voor meer informatie zie [ Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home#analytics) in [ Source connectors overzicht ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home) in de documentatie van Experience Platform.


Neem contact op met uw Adobe-vertegenwoordiger als u meer specifiek advies, advies of ondersteuning nodig hebt.

