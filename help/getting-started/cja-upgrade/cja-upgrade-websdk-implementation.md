---
title: Begrijp de implementatieopties van SDK van het Web wanneer het bevorderen aan Customer Journey Analytics
description: Meer informatie over de implementatieopties van de Web SDK bij de upgrade naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 94a2bf2f-ad84-4f35-af8f-b8a5d9e5c607
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '350'
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

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-websdk-no-selection"
>title="Voer SDK van het Web voor uw bepaalde bezit uit"
>abstract="Selecteer het gewenste implementatietype in de upgradehandleiding voor meer gedetailleerde instructies."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-websdk-third-party"
>title="De Web SDK-bibliotheek toevoegen aan uw externe tagbeheersysteem"
>abstract="Werk met de beheerder via het tagbeheersysteem om de Web SDK-bibliotheek aan uw site toe te voegen.<br><br> Voltooiingstijd voor deze taak hangt sterk van de ontvankelijkheid van het individu verantwoordelijk voor uw systeem van het markeringsbeheer af. Het toevoegen van de bibliotheek van SDK van het Web zou met bijbehorende implementatielogica kunnen worden gebundeld, en tijdens de standaardversiecycli van uw organisatie worden opgesteld."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

Het aanbevolen proces om van Adobe Analytics naar Customer Journey Analytics te upgraden is een nieuwe implementatie van de Experience Platform Web SDK, de voorkeursmethode voor gegevensverzameling voor Customer Journey Analytics.

Er zijn drie ondersteunde manieren om Adobe Experience Platform Web SDK te gebruiken:

* [&#x200B; de markeringsuitbreiding van SDK van het Web &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/install/extension): Adobe adviseert gebruikend deze methode. Installeer een tagloader op uw site en gebruik vervolgens de gebruikersinterface van de Adobe Experience Platform-gegevensverzameling om uw implementatie te configureren.

* [&#x200B; de bibliotheek van JavaScript van SDK van het Web &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/install/library): Verwijzing een CDN-ontvangen bibliotheekdossier, of gastheer het bibliotheekdossier gebruikend uw eigen infrastructuur. Aanroepen vanuit de code op uw site naar de bibliotheek uitvoeren.

* [&#x200B; NPM &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/install/npm): Installeer het Web SDK op uw plaats gebruikend NPM pakketmanager.

Voor meer informatie, zie [&#x200B; het installatieoverzicht van SDK van het Web &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/install/overview) in de Gids van SDK van het Web van Experience Platform.
