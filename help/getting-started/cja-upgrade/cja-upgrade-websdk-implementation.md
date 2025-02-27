---
title: Begrijp de implementatieopties van SDK van het Web wanneer het bevorderen aan Customer Journey Analytics
description: Meer informatie over de implementatieopties van de Web SDK bij de upgrade naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 1ae4be09a07bd4991342daa43cc23fb966b68aaf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Begrijp de implementatieopties van SDK van het Web wanneer het bevorderen aan Customer Journey Analytics {#web-sdk-implementation-options}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-websdk-js"
>title="Web SDK JavaScript-bibliotheek (alloy.js)"
>abstract="Neem de Web SDK-bibliotheek (alloy.js) op elke pagina van uw site op."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-websdk-tags"
>title="Web SDK-tagextensie"
>abstract="(Aanbevolen) Als u nog geen tags gebruikt, installeert u de tagloader op uw site. Als u al tags gebruikt, kunt u de extensie Web SDK toevoegen aan de eigenschap tag. Deze optie omvat implementaties die tags gebruiken in Adobe Experience Platform Data Collection en systemen voor tagbeheer van derden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-websdk-api"
>title="NPM-pakket"
>abstract="Gebruik de API voor gegevensverzameling om gegevens rechtstreeks naar een gegevensstroom te verzenden. Zowel niet-geverifieerde (client-naar-server) als geverifieerde (server-naar-server) typen worden ondersteund."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

Het aanbevolen proces om van Adobe Analytics naar Customer Journey Analytics te upgraden is een nieuwe implementatie van de Experience Platform Web SDK, de voorkeursmethode voor gegevensverzameling voor Customer Journey Analytics.

Er zijn drie ondersteunde manieren om Adobe Experience Platform Web SDK te gebruiken:

* [ de markeringsuitbreiding van SDK van het Web ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/install/extension): Adobe adviseert gebruikend deze methode. Installeer een tagloader op uw site en gebruik vervolgens de gebruikersinterface van de Adobe Experience Platform-gegevensverzameling om uw implementatie te configureren.

* [ de bibliotheek van JavaScript van SDK van het Web ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/install/library): Verwijzing een CDN-ontvangen bibliotheekdossier, of gastheer het bibliotheekdossier gebruikend uw eigen infrastructuur. Aanroepen vanuit de code op uw site naar de bibliotheek uitvoeren.

* [ NPM ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/install/npm): Installeer het Web SDK op uw plaats gebruikend NPM pakketmanager.

Voor meer informatie, zie [ het installatieoverzicht van SDK van het Web ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/install/overview) in de Gids van SDK van het Web van Experience Platform.



