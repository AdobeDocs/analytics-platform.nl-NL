---
title: Upgrade van een externe analyseoplossing naar Customer Journey Analytics
description: Leer hoe u van een externe analyseoplossing naar Customer Journey Analytics kunt upgraden
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: bc79ba1a-1153-4fe8-b265-9703a323c977
source-git-commit: 87df2fb92f238ce051ac5f6cc90e218737279471
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 1%

---

# Upgrade van een externe analyseoplossing naar Customer Journey Analytics {#upgrade-from-third-party}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-third-party"
>title="Een product voor externe analyse"
>abstract="Een implementatie die gegevens verzamelt voor een ander analyseproduct, zoals Google Analytics. Als u deze optie selecteert, worden verschillende opties in de vragenlijst uitgeschakeld die niet van toepassing zijn bij de upgrade naar Customer Journey Analytics van een ander analyseproduct."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in [ Customer Journey Analytics verbeteringschecklist ](https://gigazelle.github.io/cja-ttv/).

Het aanbevolen proces om van een oplossing van de derdeanalyse aan Customer Journey Analytics te bevorderen is een nieuwe implementatie van het Web SDK van Experience Platform, dat de aangewezen methode van de gegevensinzameling voor Customer Journey Analytics is. In combinatie met de Web SDK raadt Adobe ook aan historische gegevens van de oplossing voor analyse van derden in Adobe Experience Platform in te voeren.

<!-- After you have enough historical data using the Experience Platform Web SDK and you have fully transitioned to Customer Journey Analytics, the Analytics source connector can be turned off and the Web SDK can be used exclusively. -->

Gebruik het volgende proces wanneer u van een externe analyseoplossing, zoals Google Analytics, naar Customer Journey Analytics gaat:

1. ...


Neem contact op met uw Adobe-vertegenwoordiger als u meer specifiek advies, advies of ondersteuning nodig hebt.

| Bestaande analyseoplossing | Beschrijving | Beschikbare upgradepaden |
|---------|----------|----------|
| AppMeasurement | AppMeasurement for JavaScript is historisch gezien een gangbare methode geweest om Adobe Analytics te implementeren.<p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics met AppMeasurement voor JavaScript ](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) uitvoeren.</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md) </li><li>Adobe Analytics migreren naar Web SDK</li><li>[ de Schakelaar van Source van Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-exclusively.md)</li></ul> |
| Adobe Analytics-extensie (tags) | <p>Tags in Adobe Experience Platform zijn een oplossing voor tagbeheer waarmee u naast andere coderingsvereisten ook analytische code kunt implementeren. Adobe biedt integratie met andere oplossingen en producten, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.</p><p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend de uitbreiding van Analytics ](https://experienceleague.adobe.com/en/docs/analytics/implementation/launch/overview).</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md) </li><li>Adobe Analytics migreren naar Web SDK</li><li>[ de Schakelaar van Source van Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-exclusively.md)</li></ul> |
| Experience Platform Web SDK (alloy.js) | De Experience Platform Web SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. <p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics met Adobe Experience Platform Edge Network ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/overview) uitvoeren.</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md) </li><li>Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden</li></ul> |
| Experience Platform Web SDK-extensie (tags) | Experience Platform Web SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics for web data. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. <p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/overview)</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md)</li><li>Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden</li></ul> |
| Experience Platform Mobile SDK | Experience Platform Mobile SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics for mobile-gegevens. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden.<p>De Adobe Experience Platform Mobile SDK helpt Adobe Experience Cloud-oplossingen en -services aan te zwengelen in uw mobiele apps. </p><p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend Adobe Experience Platform Mobile SDK ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/mobile-sdk/overview)</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md) </li><li>Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden</li></ul> |
| API voor data-invoer in bulk | De BDIA (Bulk Data Insertion API) is een Adobe Analytics-functie waarmee u gegevens van serveroproepen in batches bestanden kunt uploaden in plaats van bibliotheken op de client, zoals AppMeasurement. </p><p>Voor meer informatie over dit implementatietype, zie [ Bulk API van de Invoeging van Gegevens ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/).</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md)</li><li>[ Adobe Experience Platform Edge Network Server API en Edge Network ](/help/data-ingestion/serverapi.md)</li></ul> |

{style="table-layout:auto"}
