---
title: Begrijp uw Adobe Analytics-implementatie en hoe deze van invloed is op uw upgrade naar Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: b9cff809-6df7-4d75-9bc1-0cc12074d355
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '939'
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
>id="cja-upgrade-appmeasurement-third-party"
>title="AppMeasurement met een tagbeheerprogramma van derden"
>abstract="Een implementatie die gebruikmaakt van een hulpprogramma voor tagbeheer van derden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-unknown"
>title="Onbekende implementatie"
>abstract="Als u niet de persoon bent die uw implementatie beheert, kunt u deze optie tijdelijk selecteren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-determine-implementation"
>title="Het bestaande implementatietype bepalen"
>abstract="Werk intern binnen uw organisatie om te bepalen welk type implementatie u momenteel gebruikt om gegevens naar Adobe Analytics te verzenden. Terwijl u aan Customer Journey Analytics bevordert, partner met het individu of het team dat deze informatie kent.<br><br> nadat u het type van implementatie bepaalt dat uw organisatie gebruikt, wijzig uw antwoord in de Gids van de Verbetering van Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

Adobe Analytics kan op verschillende manieren worden geïmplementeerd. Wanneer u een upgrade uitvoert naar Customer Journey Analytics, zijn niet alle upgradepaden beschikbaar voor alle Adobe Analytics-implementaties. Het aanbevolen upgradepad is echter altijd beschikbaar, ongeacht de manier waarop Adobe Analytics in uw organisatie is geïmplementeerd.

Gebruik de onderstaande informatie voor meer informatie over uw huidige Adobe Analytics-implementatie en over de upgradepaden die beschikbaar zijn voor uw organisatie.

Neem contact op met uw Adobe-vertegenwoordiger als u meer specifiek advies, advies of ondersteuning nodig hebt.

| Bestaande Adobe Analytics-implementatie | Beschrijving | Beschikbare upgradepaden |
|---------|----------|----------|
| AppMeasurement | AppMeasurement for JavaScript is historisch gezien een gangbare methode geweest om Adobe Analytics te implementeren.<p>Voor meer informatie over dit implementatietype, zie [&#x200B; Adobe Analytics met AppMeasurement voor JavaScript &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/js/overview) uitvoeren.</p> | <ul><li>[&#x200B; (Aanbevolen) Nieuwe implementatie van het Web SDK van Experience Platform voor aan de gang zijnde gegevensinzameling; de bron van Analytics schakelaar voor historische gegevens &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[&#x200B; Nieuwe implementatie van het Web SDK van Experience Platform &#x200B;](/help/data-ingestion/aepwebsdk.md) </li><li>[&#x200B; Migreer Adobe Analytics aan het Web SDK &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-alternative-appmeasurement.md)</li><li>[&#x200B; Bron van Analytics schakelaar &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-alternative-source-connector.md)</li></ul> |
| Adobe Analytics-extensie (tags) | <p>Tags in Adobe Experience Platform zijn een oplossing voor tagbeheer waarmee u naast andere coderingsvereisten ook analytische code kunt implementeren. Adobe biedt integratie met andere oplossingen en producten, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.</p><p>Voor meer informatie over dit implementatietype, zie [&#x200B; Adobe Analytics uitvoeren gebruikend de uitbreiding van Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/launch/overview).</p> | <ul><li>[&#x200B; (Aanbevolen) Nieuwe implementatie van het Web SDK van Experience Platform voor aan de gang zijnde gegevensinzameling; de bron van Analytics schakelaar voor historische gegevens &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[&#x200B; Nieuwe implementatie van het Web SDK van Experience Platform &#x200B;](/help/data-ingestion/aepwebsdk.md) </li><li>[&#x200B; Migreer Adobe Analytics aan het Web SDK &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-alternative-appmeasurement.md)</li><li>[&#x200B; Bron van Analytics schakelaar &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-alternative-source-connector.md)</li></ul> |
| Experience Platform Web SDK (alloy.js) | De Experience Platform Web SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. <p>Voor meer informatie over dit implementatietype, zie [&#x200B; Adobe Analytics met Adobe Experience Platform Edge Network &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/aep-edge/overview) uitvoeren.</p> | <ul><li>[&#x200B; (Aanbevolen) Nieuwe implementatie van het Web SDK van Experience Platform voor aan de gang zijnde gegevensinzameling; de bron van Analytics schakelaar voor historische gegevens &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[&#x200B; Nieuwe implementatie van het Web SDK van Experience Platform &#x200B;](/help/data-ingestion/aepwebsdk.md) </li><li>[&#x200B; vorm de implementatie van SDK van het Web van Adobe Analytics om gegevens naar Platform &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-existing-adobe-analytics-websdk.md) te verzenden</li></ul> |
| Experience Platform Web SDK-extensie (tags) | Experience Platform Web SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics for web data. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. <p>Voor meer informatie over dit implementatietype, zie [&#x200B; Adobe Analytics uitvoeren gebruikend SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/aep-edge/web-sdk/overview)</p> | <ul><li>[&#x200B; (Aanbevolen) Nieuwe implementatie van het Web SDK van Experience Platform voor aan de gang zijnde gegevensinzameling; de bron van Analytics schakelaar voor historische gegevens &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[&#x200B; Nieuwe implementatie van het Web SDK van Experience Platform &#x200B;](/help/data-ingestion/aepwebsdk.md)</li><li>[&#x200B; vorm de implementatie van SDK van het Web van Adobe Analytics om gegevens naar Platform &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-existing-adobe-analytics-websdk.md) te verzenden</li></ul> |
| Experience Platform Mobile SDK | Experience Platform Mobile SDK is de momenteel aanbevolen methode voor het implementeren van Adobe Analytics for mobile-gegevens. Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden.<p>De Adobe Experience Platform Mobile SDK helpt Adobe Experience Cloud-oplossingen en -services aan te zwengelen in uw mobiele apps. </p><p>Voor meer informatie over dit implementatietype, zie [&#x200B; Adobe Analytics uitvoeren gebruikend Adobe Experience Platform Mobile SDK &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/aep-edge/mobile-sdk/overview)</p> | <ul><li>[&#x200B; (Aanbevolen) Nieuwe implementatie van het Web SDK van Experience Platform voor aan de gang zijnde gegevensinzameling; de bron van Analytics schakelaar voor historische gegevens &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[&#x200B; Nieuwe implementatie van het Web SDK van Experience Platform &#x200B;](/help/data-ingestion/aepwebsdk.md) </li><li>[&#x200B; vorm de implementatie van SDK van het Web van Adobe Analytics om gegevens naar Platform &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-existing-adobe-analytics-websdk.md) te verzenden</li></ul> |
| API voor data-invoer in bulk | De BDIA (Bulk Data Insertion API) is een Adobe Analytics-functie waarmee u gegevens van serveroproepen in batches bestanden kunt uploaden in plaats van bibliotheken op de client, zoals AppMeasurement. </p><p>Voor meer informatie over dit implementatietype, zie [&#x200B; Bulk API van de Invoeging van Gegevens &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/).</p> | <ul><li>[&#x200B; (Aanbevolen) Nieuwe implementatie van het Web SDK van Experience Platform voor aan de gang zijnde gegevensinzameling; de bron van Analytics schakelaar voor historische gegevens &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</li><li>[&#x200B; Nieuwe implementatie van het Web SDK van Experience Platform &#x200B;](/help/data-ingestion/aepwebsdk.md)</li><li>[&#x200B; Adobe Experience Platform Edge Network Server API en Edge Network &#x200B;](/help/data-ingestion/serverapi.md)</li></ul> |

{style="table-layout:auto"}


