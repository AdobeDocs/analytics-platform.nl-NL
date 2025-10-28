---
title: De Regels van de verwerking, VISTA, en classificaties vs. de Prep van Gegevens voor de bron van Analytics schakelaar
description: Meer informatie over gegevenstransformatie met verwerkingsregels en VISTA versus Data Prep
exl-id: 049ad97e-0b4f-4163-a022-32661e48bf13
feature: Basics
role: User
source-git-commit: 359fe2a718ccef816377083aceb2652b4a905072
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Verwerkingsregels, VISTA, en classificaties versus Prep van Gegevens

Adobe Analytics [&#x200B; verwerkingsregels en de regels van VISTA &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/processing-rule-order.html?lang=nl-NL) verstrekken een middel om gegevens om te zetten en te manipuleren die in Adobe Analytics [&#x200B; gegevensinzameling &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/reporting-interface/overview-data-collection.html?lang=nl-NL) worden overgegaan. Deze transformaties vinden plaats als onderdeel van de Adobe-gegevensverwerking voordat de gegevens voor rapportage- en analysedoeleinden in Adobe Analytics worden opgeslagen.

[&#x200B; Prep van Gegevens &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html?lang=nl-NL) is een hulpmiddel dat u op rij-gebaseerde afbeeldingen en transformaties op gegevens laat toepassen die in [&#x200B; Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform.html?lang=nl-NL) worden opgenomen. Vervolgens worden de gegevens beschikbaar gesteld aan Experience Platform-toepassingen, waaronder Customer Journey Analytics en andere. De gegevens prep is geïntegreerd met veel van de 2&rbrace; bron van het Platform [&#x200B; schakelaars &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=nl-NL), evenals met de [&#x200B; Analyse bronschakelaar &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=nl-NL). Deze aansluiting biedt een manier om gegevens uit de rapportsuite van Adobe Analytics in Platform in te voeren.

## Verdere transformatie met Data Prep {#data-prep}

Gegevens die door Adobe Analytics worden verzameld en in worden opgeslagen, kunnen worden getransformeerd aan de hand van verwerkingsregels, VISTA-regels of beide. Maar de rapportsuites die dan aan Platform via de Analytics bronschakelaar worden doorgestuurd kunnen nog een tijd worden omgezet gebruikend Prep van Gegevens. Dit kan voor een aantal doeleinden wenselijk zijn:

* **het oplossen van schemaverschillen tussen rapportreeksen voor gebruik in Customer Journey Analytics en/of RTCDP**. Een rapportsuite A definieert `eVar1` bijvoorbeeld als &#39;Zoekterm&#39; en rapportsuite B definieert `eVar2` als &#39;Zoekterm&#39;. U kunt data prep gebruiken om de twee verschillende eVars in een gemeenschappelijk gebied in kaart te brengen dat gegevens van beide eVars bevat. Dit maakt het mogelijk om [&#x200B; rapportreeksen met verschillende schema&#39;s &#x200B;](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/combine-report-suites.html?lang=nl-NL) in a [&#x200B; verbinding van Customer Journey Analytics &#x200B;](/help/connections/overview.md) of voor gebruik in [&#x200B; Real-time het Platform van Gegevens van de Klant &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=nl-NL) te combineren.
* **gebieden van 0&rbrace; het in kaart brengen &lbrace;aan semantisch betekenisvolle namen `eVars`.** `eVars` en `props` die door de bronschakelaar van de Analyse komen worden in kaart gebracht aan gebieden zoals _\_experience.analytics.customDimensions.eVars.eVar1_. Gegevensvoorbeeld kan worden gebruikt om `eVar` - en `prop` -velden toe te wijzen aan nieuwe velden die betekenisvollere namen voor uw gebruikers hebben, of die dezelfde namen hebben als andere gegevensbronnen. (Dit kan ook via andere middelen worden verwezenlijkt, zoals het anders noemen van de gebieden in a [&#x200B; de gegevensmening van Customer Journey Analytics &#x200B;](/help/data-views/create-dataview.md).)
* **over het algemeen transformerend gegevens**. Data prep heeft honderden toewijzingsfuncties die kunnen worden gebruikt om nieuwe gebieden te berekenen en te berekenen die op de gegevens worden gebaseerd die door de de bronschakelaar van de Analyse komen. U kunt gescheiden velden splitsen in afzonderlijke velden. U kunt velden combineren. U kunt tekenreeksen manipuleren. U kunt informatie uit een veld extraheren op basis van reguliere expressies en nog veel meer.

## Gegevensprep en classificatie {#classifications}

Prep van gegevens heeft oversteekplaats met [&#x200B; classificaties &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=nl-NL) in sommige situaties.

In een veld met scheidingstekens kunt u bijvoorbeeld Data Prep gebruiken om dat veld in meerdere afzonderlijke velden te splitsen zonder classificaties te gebruiken. Over het algemeen zijn classificaties een manier om metagegevens aan een veld toe te voegen door een opzoekbestand te uploaden dat buiten de stroom van inkomende gebeurtenissen Analytics wordt geleverd.

U kunt bijvoorbeeld een classificatiebestand uploaden waarin SKU&#39;s worden gegroepeerd in &#39;grootte&#39;, &#39;merk&#39;, &#39;kleur&#39; enzovoort. Een ander verschil tussen classificaties en Prep van Gegevens is dat classificaties op gegevens _zowel historisch als vooruitgaand_ van toepassing zijn. De afbeeldingen van de Prep van gegevens, anderzijds, worden toegepast _voorwaarts_ aan gegevens van de tijd de afbeelding wordt gecreeerd.
