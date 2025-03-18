---
title: Overzicht van Content Analytics
description: Een overzicht van Content Analytics
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin, User
hide: true
hidefromtoc: true
exl-id: 0d3be50d-c635-459b-8b01-61d6d4ef0cdf
source-git-commit: 62491fcbf37961d33be92d209e5710bf9696c223
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Overzicht van Content Analytics

>[!WARNING]
>
>Dit artikel is een voorlopige niet-officiële ontwerpversie van een toekomstige definitieve versie en maakt deel uit van de documentatie van Content Analytics. Alle inhoud kan worden gewijzigd en er kunnen geen wettelijke verplichtingen uit de huidige versie van dit artikel worden afgeleid.
>

{{release-limited-testing}}

Content Analytics helpt marketers te begrijpen hoe inhoud van invloed is op de belangrijkste prestatie-indicatoren die een bedrijf heeft gedefinieerd. Naast de gedragsgegevens verzamelt Content Analytics gegevens over hoe inhoud wordt verbruikt en hoe inhoud invloed heeft. Bijvoorbeeld, antwoorden de klanten beter aan een specifieke toon van stem, een specifieke kleurenpallet, of specifieke thema&#39;s? Deze informatie, samen met specifiek ontworpen rapportwerkschema&#39;s en malplaatjes, kan u helpen om nog betere analyse uit te voeren en diepgaandere inzichten van klantenreisgegevens in Customer Journey Analytics te bereiken.

De Analytics van de inhoud gebruikt AI en machine het leren baseerde **featurization dienst** om inhoud in componenten en attributen neer te breken. Door een gestructureerd metagegevensprofiel voor al uw inhoud te maken, kunt u analyseren welke inhoud en welke kenmerken van die inhoud de bedrijfsresultaten beïnvloeden.

Naast de verwezenlijking van dit gestructureerde meta-gegevensprofiel, verstrekt Content Analytics de **identiteitsdienst** die activa en ervaringen gebruikend één enkel herkenningsteken identificeert. De identiteitsservice kan herkennen wanneer hetzelfde element op meerdere plaatsen wordt weergegeven. Wanneer dat gebeurt, worden de twee exemplaren van activa als zelfde behandeld, die voor een holistischer beeld van inhoudsgebruik en consumptie toestaan.

## Waarde

Content Analytics biedt wel een hogere waarde:

1. Het gebruik van de inhoud ****: Met de Analytics van de Inhoud krijgt u inzicht op welke activa beelden ontvangen en waar de activa impressies ontvangen. Deze inzichten helpen u om te zien of worden de activa ondergebruikt of op uw Web-eigenschappen overgebruikt.
1. Inhoud **overeenkomsten**: De Analytics van de inhoud kan betrokkenheidsinzichten zoals het gemiddelde klikken door tarief voor activa met bepaalde attributen verstrekken. Deze inzichten helpen u om te bepalen of specifieke soorten ervaringen nog efficiënt zijn.
1. Inhoud **reizen**: Voorts wanneer gecombineerd met alle andere gegevens beschikbaar in Experience Platform, kunt u extra inzichten op uw inhoudstrajecten verkrijgen. Of specifieke inhoud bijvoorbeeld leidt tot conversies, bovenop de betrokkenheid. En met die kennis kunt u ROI op types van inhoud bepalen.
1. De inhoud **verpersoonlijking**: De Analytics van de Inhoud staat u toe om op uw inzichten te handelen en deze inzichten te gebruiken om te bepalen hoe te om geld aan inhoud uit te geven. Moet ik bijvoorbeeld specifieke typen inhoud naar specifieke doelgroepen sturen? Welke inhoud biedt me mogelijkheden tot high-personalization?

## Terminologie

Voor Content Analytics worden de volgende sleuteltermen gebruikt:

![ Assets en ervaringen ](/help/content-analytics/assets//content-analytics-experience-asset.png)

* **Ervaring**: Een ervaring is al tekst op een Web-pagina die reproduceerbaar gebruikend URL is die door de aanvankelijke gebruiker wordt gebruikt die die die Web-pagina bezoekt. Elke ervaring krijgt een unieke id.
* **Activa**: Een activa is een individueel en uniek stuk van inhoud, zoals een beeld. Elk element krijgt ook een unieke id.
* **Attribuut**: Een attribuut is een beschrijvend meta-gegevenselement verbonden aan een ervaring of activa. Voorbeelden van een kenmerk zijn: stijl van fotografie, leesbaarheid, overredingsstrategie, objectkleur en achtergrondkleur.

## Hoe werkt het

Content Analytics maakt gebruik van webafbeeldingsweergavegegevens die zijn verzameld in gebeurtenisgegevenssets in Experience Platform. Deze gegevens kunnen worden verzameld via de verschillende beschikbare methoden: Experience Platform Edge Network (Web SDK, Server API) of de bronaansluiting Analytics.

![ Analytics van de Inhoud - hoe het ](assets/aca-overview.gif) werkt


1. Wanneer een gebruiker een plaats bezoekt, die voor Content Analytics wordt gevormd, registreert het Web SDK van Experience Platform interactie met inhoud.
1. De service voor het samenstellen van functies en de identiteitsservice verwerken de herziene gegevens. Dat proces bestaat uit een kruipper die de publiek-gerichte versies van gevormde URLs terugkeert en de diensten AI/ML toepast.
1. De resultaten van deze services (componenten, kenmerken en identiteiten) worden gebruikt om de relevante specifieke gegevenssets voor inhoudsanalyses in Experience Platform bij te werken.
1. De gegevens van de inhoudsanalyse, samen met gedragsgegevens en andere raadplegingsdatasets, gebruikt u in de opstelling van Customer Journey Analytics (combinatie Verbinding, de mening van Gegevens en Workspace). Die opstelling verstrekt de stichting aan de unieke macrovlakke inzichten op uw inhoud.

>[!NOTE]
>
>Content Analytics maakt gebruik van AI/ML-services die tot onjuiste of misleidende resultaten kunnen leiden. Dientengevolge, gelieve uw oordeel te gebruiken om AI/ML geproduceerde output te herzien en te bevestigen.
>
>U kunt het **[!UICONTROL Feedback]** lusje, beschikbaar van ![ InfoOutline ](/help/assets/icons/InfoOutline.svg) op de belangrijkste interface gebruiken, om te verstrekken terugkoppelt op de AI/ML geproduceerde output.
>

>[!NOTE]
>
>Als u een licentie hebt verleend voor de &#39;Privacy and Security Shield add-on&#39;, dient u er rekening mee te houden dat (alle gegevens die zijn gegenereerd op basis van) ervaringen en bedrijfsmiddelen, afhankelijk van Content Analytics, niet worden gedekt door DULE-labels of door Klant beheerde sleutels.
>


>[!MORELIKETHIS]
>
>[ Analytics die van de Inhoud ](report/report.md) melden
>[Inhoud analyseren configureren ](config/configuration.md)
>