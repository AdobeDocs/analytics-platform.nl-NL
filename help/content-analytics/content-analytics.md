---
title: Content Analytics-overzicht
description: Een overzicht van Content Analytics
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin, User
exl-id: 0d3be50d-c635-459b-8b01-61d6d4ef0cdf
source-git-commit: dd4adc5acd05aecf0a67072df6688a344e1ce5c9
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Content Analytics-overzicht

Content Analytics helpt marketers te begrijpen hoe inhoud van invloed is op de belangrijkste prestatie-indicatoren die een bedrijf heeft gedefinieerd. Naast de gedragsgegevens verzamelt Content Analytics gegevens over hoe inhoud wordt verbruikt en hoe inhoud invloed heeft. Bijvoorbeeld, antwoorden de klanten beter aan een specifieke toon van stem, een specifiek kleurenpalet, of specifieke thema&#39;s? Deze informatie, samen met specifiek ontworpen rapportwerkschema&#39;s en malplaatjes, kan u helpen om nog betere analyse uit te voeren en diepgaandere inzichten van klantenreisgegevens in Customer Journey Analytics te bereiken.

Content Analytics gebruikt AI en machine het leren de gebaseerde **featurization dienst** om inhoud in componenten en attributen neer te breken. Door een gestructureerd metagegevensprofiel voor al uw inhoud te maken, kunt u analyseren welke inhoud en welke kenmerken van die inhoud de bedrijfsresultaten beïnvloeden.

Naast de verwezenlijking van dit gestructureerde meta-gegevensprofiel, verstrekt Content Analytics de **identiteitsdienst** die activa en ervaringen gebruikend één enkel herkenningsteken identificeert. De identiteitsservice kan herkennen wanneer exact hetzelfde element op meerdere plaatsen wordt weergegeven. Wanneer dat gebeurt, worden de instanties van dit actief als hetzelfde actief behandeld, waardoor een meer holistische kijk op het gebruik en de consumptie van inhoud mogelijk wordt.

## Waarde

Content Analytics biedt wel een hogere waarde:

1. Het gebruik van de inhoud ****: Met Content Analytics krijgt u inzicht op welke activa beelden ontvangen en waar de activa impressies ontvangen. Deze inzichten helpen u om te zien of worden de activa ondergebruikt of op uw Web-eigenschappen overgebruikt.
1. Inhoud **overeenkomsten**: Content Analytics kan betrokkenheidsinzichten zoals het gemiddelde klikken door tarief voor activa met bepaalde attributen verstrekken. Deze inzichten helpen u om te bepalen of specifieke soorten ervaringen nog efficiënt zijn.
1. Inhoud **reizen**: Voorts wanneer gecombineerd met alle andere gegevens beschikbaar in Experience Platform, kunt u extra inzichten op uw inhoudstrajecten verkrijgen. Of specifieke inhoud bijvoorbeeld leidt tot conversies, bovenop de betrokkenheid. En met die kennis kunt u ROI op types van inhoud bepalen.
1. De inhoud **verpersoonlijking**: De Analytics van de Inhoud staat u toe om op uw inzichten te handelen en deze inzichten te gebruiken om te bepalen hoe te om geld aan inhoud uit te geven. Moet ik bijvoorbeeld specifieke typen inhoud naar specifieke doelgroepen sturen? Welke inhoud biedt me mogelijkheden tot high-personalization?

## Terminologie

Voor Content Analytics worden de volgende sleuteltermen gebruikt:

![ Assets en ervaringen ](/help/content-analytics/assets/content-analytics-experience-asset.png)

* **Ervaring**: Een ervaring is al tekst op een Web-pagina die reproduceerbaar gebruikend URL is die door de aanvankelijke gebruiker wordt gebruikt die de Web-pagina bezocht. Elke ervaring krijgt een unieke id. Wijzigingen in de pagina die leiden tot wijzigingen in de HTML van de pagina, leiden tot een nieuwe ervaring.
* **Activa**: Een activa is een individueel en uniek stuk van inhoud, zoals een beeld. Elk element krijgt ook een unieke id en een perceptuele id. Een perceptuele id is een id die wordt gedeeld met elementen die visueel identiek zijn. Met perceptuele id&#39;s kunt u elementen dedupliceren die een andere element-URL en dus een andere element-id hebben, maar die wel exact hetzelfde zijn.
* **Attribuut**: Een attribuut is een beschrijvend meta-gegevenselement verbonden aan een ervaring of activa. Voorbeelden van een kenmerk zijn: stijl van fotografie, leesbaarheid, overredingsstrategie, objectkleur en achtergrondkleur.

## Hoe werkt het

Content Analytics gebruikt de gegevens van de de meningsmening van het Webbeeld in gebeurtenisdatasets in Experience Platform om [ gegevens van de inhoudsgebeurtenis ](config/datacollection.md) te verzamelen. En combineert die inhoudsgegevensverzameling met de (bestaande) implementatie van gegevensverzameling van gedragsgegevens.

![ Analytics van de Inhoud - hoe het ](assets/aca-overview.gif) werkt

1. Wanneer een gebruiker een plaats bezoekt, [ voor Content Analytics ](config/configuration.md) wordt gevormd, registreert het Web SDK van Experience Platform indrukkingen en interactie met inhoud.
1. De identiteit en de featuriseringsdienst verwerken deze interactie. Dat proces bestaat uit een herwinningsdienst die de openbaar-onder ogen ziet versies van gevormde URLs herziet die de interactie bepalen. Voor al deze opgehaalde URL&#39;s identificeert de identiteitsservice de ervaringen en elementen op unieke wijze. En de featurization dienst past de diensten van AI/van ML toe om ervaringen en activa meta-gegevens en attributen te ontdekken.
1. De resultaten van deze diensten ([ componenten, attributen, en identiteiten ](/help/content-analytics/report/components.md)) worden gebruikt om de relevante specifieke datasets van inhoudsanalyses in Experience Platform bij te werken.
1. De gegevens van de inhoudsanalyse, samen met gedragsgegevens en andere raadplegingsgegevens, kunt u in een opstelling van Customer Journey Analytics gebruiken ([ Verbinding ](/help/connections/overview.md), [ mening van Gegevens ](/help/data-views/data-views.md) en [ Workspace ](/help/analysis-workspace/home.md)). Die opstelling verstrekt de stichting aan de unieke macrovlakke inzichten op uw inhoud. <br/> u kunt sprongen uw rapporten en analyse van Content Analytics gebruikend het [ malplaatje van Content Analytics ](/help/content-analytics/report/report.md#template).


>[!NOTE]
>
>Content Analytics maakt gebruik van AI/ML-services die tot onjuiste of misleidende resultaten kunnen leiden. Dientengevolge, gelieve uw oordeel te gebruiken om AI/ML geproduceerde output te herzien en te bevestigen.
>
>U kunt het **[!UICONTROL Feedback]** lusje, beschikbaar van ![ InfoOutline ](/help/assets/icons/InfoOutline.svg) op de belangrijkste interface gebruiken, om te verstrekken terugkoppelt op de AI/ML geproduceerde output.
>

>[!NOTE]
>
>Als u een licentie hebt verleend voor de &#39;Privacy and Security Shield add-on&#39;, dient u er rekening mee te houden dat (alle gegevens die zijn gegenereerd op basis van) ervaringen en bedrijfsmiddelen, afhankelijk van Content Analytics, niet worden gedekt door DULE-labels of door Klant beheerde sleutels. Bovendien is Content Analytics geen HIPAA-Klaar dienst.
>


>[!MORELIKETHIS]
>
>[ Content Analytics die ](report/report.md) meldt
>[Content Analytics configureren ](config/configuration.md)
>[Het berekenen van stuitingen en het stuiteren tarief in Customer Journey Analytics ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/calculating-bounces-amp-bounce-rate-in-adobe-customer-journey/ba-p/706446#M454)
>

