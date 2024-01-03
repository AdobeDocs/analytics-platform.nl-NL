---
title: De Regels van de verwerking, VISTA, en classificaties vs. de Prep van Gegevens voor de bron van Analytics schakelaar
description: Meer informatie over gegevenstransformatie met verwerkingsregels en VISTA versus Data Prep
exl-id: 049ad97e-0b4f-4163-a022-32661e48bf13
feature: Basics
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Verwerkingsregels, VISTA, en classificaties versus Prep van Gegevens

Adobe Analytics [verwerkingsvoorschriften en VISTA-regels](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/processing-rule-order.html?lang=en) een middel bieden om gegevens die in Adobe Analytics worden doorgegeven, om te zetten en te manipuleren [gegevensverzameling](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/reporting-interface/overview-data-collection.html?lang=en). Deze transformaties maken deel uit van de gegevensverwerking van de Adobe voordat de gegevens voor rapportage- en analysedoeleinden in Adobe Analytics worden opgeslagen.

[Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html?lang=en) is een gereedschap waarmee u op rijen gebaseerde toewijzingen en transformaties kunt toepassen op gegevens die u in [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=en). Vervolgens worden de gegevens ter beschikking gesteld van toepassingen in de Experience Platform, waaronder Customer Journey Analytics en andere. Data prep is geïntegreerd met veel van het platform [bronconnectors](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=en), alsmede met de [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en). Deze aansluiting biedt een manier om gegevens uit de rapportsuite van Adobe Analytics in Platform in te voeren.

## Verdere transformatie met Data Prep {#data-prep}

Gegevens die door Adobe Analytics worden verzameld en in worden opgeslagen, kunnen worden getransformeerd aan de hand van verwerkingsregels, VISTA-regels of beide. Maar de rapportsuites die dan aan Platform via de Analytics bronschakelaar worden doorgestuurd kunnen nog een tijd worden omgezet gebruikend Prep van Gegevens. Dit kan voor een aantal doeleinden wenselijk zijn:

* **Schema-verschillen oplossen tussen rapportsuites voor gebruik in Customer Journey Analytics en/of RTCDP**. Stel bijvoorbeeld dat rapportsuite A definieert `eVar1` als &quot;Zoekterm&quot; en rapportsuite B `eVar2` als &quot;Zoekterm&quot;. U kunt data prep gebruiken om de twee verschillende eVars in een gemeenschappelijk gebied in kaart te brengen dat gegevens van beide eVars bevat. Hierdoor is het mogelijk [rapportsuites combineren met verschillende schema&#39;s](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/combine-report-suites.html?lang=en) in een [Verbinding met Customer Journey Analytics](/help/connections/overview.md) of voor gebruik in [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=en).
* **Toewijzing `eVars` velden naar semantische betekenisvolle namen**. `eVars` en `props` die door de bronschakelaar van de Analyse komen wordt in kaart gebracht aan gebieden zoals _\_experience.analytics.customDimensions.eVars.eVar1_. Gegevensvoorbeeld kan worden gebruikt om `eVar` en `prop` velden naar nieuwe velden met betekenisvollere namen voor uw gebruikers of met dezelfde namen die afkomstig zijn uit andere gegevensbronnen. (Dit kan ook op andere manieren worden gedaan, bijvoorbeeld door de namen van de velden in een [Gegevens Customer Journey Analytics, weergave](/help/data-views/create-dataview.md).)
* **Gegevens doorgaans transformeren**. Data prep heeft honderden toewijzingsfuncties die kunnen worden gebruikt om nieuwe gebieden te berekenen en te berekenen die op de gegevens worden gebaseerd die door de de bronschakelaar van de Analyse komen. U kunt gescheiden velden splitsen in afzonderlijke velden. U kunt velden combineren. U kunt tekenreeksen manipuleren. U kunt informatie uit een veld extraheren op basis van reguliere expressies en nog veel meer.

## Gegevensprep en classificatie {#classifications}

Data Prep heeft cross-over met [classificaties](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=en) in sommige situaties.

In een veld met scheidingstekens kunt u bijvoorbeeld Data Prep gebruiken om dat veld in meerdere afzonderlijke velden te splitsen zonder classificaties te gebruiken. Over het algemeen zijn classificaties een manier om metagegevens aan een veld toe te voegen door een opzoekbestand te uploaden dat buiten de stroom van inkomende gebeurtenissen Analytics wordt geleverd.

U kunt bijvoorbeeld een classificatiebestand uploaden waarin SKU&#39;s worden gegroepeerd in &#39;grootte&#39;, &#39;merk&#39;, &#39;kleur&#39; enzovoort. Een ander verschil tussen classificaties en Data Prep is dat classificaties van toepassing zijn op gegevens _zowel historisch als in de toekomst_. Aan de andere kant worden gegevenprep-toewijzingen toegepast _doorsturen_ aan gegevens vanaf het moment dat de toewijzing wordt gemaakt.
