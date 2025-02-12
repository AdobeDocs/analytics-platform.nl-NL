---
title: Begrijp uw Adobe Analytics-implementatie en hoe deze van invloed is op uw upgrade naar Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: b9cff809-6df7-4d75-9bc1-0cc12074d355
source-git-commit: a462bdbff59e8d83d6948ef882e66690624c4847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 1%

---

# Begrijp uw Adobe Analytics-implementatie en hoe deze van invloed is op uw upgrade naar Customer Journey Analytics {#implementation-affects-upgrade}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-appmeasurement"
>title="AppMeasurement (handmatig JS-bestand)"
>abstract="Een JavaScript-implementatie die AppMeasurement.js op een pagina laadt en gegevens naar Adobe verzendt met het s-object (bijvoorbeeld s.eVar1)."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-analyticsextension"
>title="Adobe Analytics-extensie (tags)"
>abstract="A tags implementation that load Adobe Experience Platform Data Collection (voorheen Launch genoemd). De extensie Adobe Analytics is geïnstalleerd op de tag."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-websdk"
>title="Web SDK (alloy.js)"
>abstract="Een JavaScript-implementatie die de Web SDK-bibliotheek (alloy.js) op een pagina laadt en gegevens naar Adobe verzendt met een JSON-payload."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-websdkextension"
>title="Web SDK-extensie (tags)"
>abstract="A tags implementation that load Adobe Experience Platform Data Collection (voorheen Launch genoemd). Voor de tag is de extensie Web SDK geïnstalleerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-api"
>title="API voor data-invoer"
>abstract="Een implementatie die de API voor het invoegen van gegevens of de API voor het invoegen van bulkgegevens gebruikt."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-mobilesdk"
>title="Mobile SDK"
>abstract="Een implementatie die gebruikmaakt van de Adobe Experience Platform Mobile SDK."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-unknown"
>title="Onbekende implementatie"
>abstract="Als u niet de persoon bent die uw implementatie beheert, kunt u deze optie tijdelijk selecteren."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in [ Customer Journey Analytics verbeteringschecklist ](https://gigazelle.github.io/cja-ttv/).

Adobe Analytics kan op verschillende manieren worden geïmplementeerd. Wanneer u een upgrade uitvoert naar Customer Journey Analytics, zijn niet alle upgradepaden beschikbaar voor alle Adobe Analytics-implementaties. Het aanbevolen upgradepad is echter altijd beschikbaar, ongeacht de manier waarop Adobe Analytics in uw organisatie is geïmplementeerd.

Gebruik de onderstaande informatie voor meer informatie over uw huidige Adobe Analytics-implementatie en over de upgradepaden die beschikbaar zijn voor uw organisatie.

Neem contact op met uw Adobe-vertegenwoordiger als u meer specifiek advies, advies of ondersteuning nodig hebt.

| Bestaande Adobe Analytics-implementatie | Beschrijving | Beschikbare upgradepaden |
|---------|----------|----------|
| AppMeasurement | AppMeasurement for JavaScript is historisch gezien een gangbare methode geweest om Adobe Analytics te implementeren.<p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics met AppMeasurement voor JavaScript ](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) uitvoeren.</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md) </li><li>Adobe Analytics migreren naar Web SDK</li><li>[ de Schakelaar van Source van Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-exclusively.md)</li></ul> |
| Adobe Analytics-extensie (tags) | <p>Tags in Adobe Experience Platform zijn een oplossing voor tagbeheer waarmee u naast andere coderingsvereisten ook analytische code kunt implementeren. Adobe biedt integratie met andere oplossingen en producten, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.</p><p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend de uitbreiding van Analytics ](https://experienceleague.adobe.com/en/docs/analytics/implementation/launch/overview).</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md) </li><li>Adobe Analytics migreren naar Web SDK</li><li>[ de Schakelaar van Source van Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-exclusively.md)</li></ul> |
| Experience Platform Web SDK (alloy.js) | De Experience Platform Web SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. <p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics met Adobe Experience Platform Edge Network ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/overview) uitvoeren.</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md) </li><li>Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden</li></ul> |
| Experience Platform Web SDK-extensie (tags) | Experience Platform Web SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics for web data. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. <p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/overview)</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md)</li><li>Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden</li></ul> |
| Experience Platform Mobile SDK | Experience Platform Mobile SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics for mobile-gegevens. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden.<p>De Adobe Experience Platform Mobile SDK helpt Adobe Experience Cloud-oplossingen en -services aan te zwengelen in uw mobiele apps. </p><p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend Adobe Experience Platform Mobile SDK ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/mobile-sdk/overview)</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md) </li><li>Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden</li></ul> |
| API voor data-invoer in bulk | De BDIA (Bulk Data Insertion API) is een Adobe Analytics-functie waarmee u gegevens van serveroproepen in batches bestanden kunt uploaden in plaats van bibliotheken op de client, zoals AppMeasurement. </p><p>Voor meer informatie over dit implementatietype, zie [ Bulk API van de Invoeging van Gegevens ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/).</p> | <ul><li>[ (Aanbevolen) Nieuwe implementatie van Experience Platform Web SDK voor aan de gang zijnde gegevensinzameling; de Schakelaar van Analytics Source voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[ Nieuwe implementatie van het Web SDK van Experience Platform ](/help/data-ingestion/aepwebsdk.md)</li><li>[ Adobe Experience Platform Edge Network Server API en Edge Network ](/help/data-ingestion/serverapi.md)</li></ul> |

{style="table-layout:auto"}
