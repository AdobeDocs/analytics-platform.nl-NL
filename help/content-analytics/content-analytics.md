---
title: Overzicht van Content Analytics
description: Een overzicht van Content Analytics
solution: Customer Journey Analytics
feature: Data Views
role: Admin
hide: true
hidefromtoc: true
exl-id: 0d3be50d-c635-459b-8b01-61d6d4ef0cdf
source-git-commit: 164d67748f8af066b603dcabeecf6d7cfca0f947
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Overzicht van Content Analytics

<!-- 
This is a placeholder article for upcoming Content Analytics documentation. Currently used to set up contextual help entries for developer working on onboarding UI and workspace UI 
-->

>[!WARNING]
>
>Dit artikel is een voorlopige niet-officiële ontwerpversie van een toekomstige definitieve versie en maakt deel uit van de documentatie van Content Analytics. Alle inhoud kan worden gewijzigd en er kunnen geen wettelijke verplichtingen uit de huidige versie van dit artikel worden afgeleid.
>

{#release-limited-testing}

Content Analytics helpt marketers te begrijpen hoe inhoud van invloed is op de belangrijkste prestatie-indicatoren die een bedrijf heeft gedefinieerd. Naast de traditionele, op microniveau gebaseerde functies voor het testen van inhoud (bijvoorbeeld A/B-tests), biedt Content Analytics inzicht in de manier waarop inhoud invloed heeft op macroniveau. Bijvoorbeeld, antwoorden de klanten beter aan een specifieke toon van stem, een specifieke kleurenpallet, of specifieke thema&#39;s?

De Analytics van de inhoud gebruikt AI en machine het leren baseerde **featurization dienst** om inhoud in componenten en attributen neer te breken. Door een gestructureerd metagegevensprofiel voor al uw inhoud te maken, kunt u analyseren welke inhoud en welke kenmerken van die inhoud de bedrijfsresultaten beïnvloeden.

Naast de verwezenlijking van dit gestructureerde meta-gegevensprofiel, verleent de Analyse van de Inhoud een **identiteitsdienst** die activa en ervaringen gebruikend één enkel herkenningsteken identificeert. De identiteitsdienst begrijpt of een middel, bijvoorbeeld, resized, bijgesneden, of opgeslagen aan een verschillend dossierformaat is. De service wijst alle variaties van dat element toe aan dezelfde id. Dientengevolge, staat de identiteitsdienst u toe om de prestaties van activa te groeperen die op zijn diverse vormen en plaatsingen worden gebaseerd.

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

Content Analytics maakt gebruik van webafbeeldingsweergavegegevens die zijn verzameld in gebeurtenisdatasets in Experience Platform. Deze gegevens kunnen worden verzameld via de verschillende beschikbare methoden: Experience Platform Edge Network (Web SDK, Server API) of Analytics-bronconnector.

![ Analytics van de Inhoud - hoe het ](assets/how-it-works.png) werkt


1. Het detectiedeel van de service featurization wordt geactiveerd bij elke nieuwe momentopname van gegevens die aankomen bij een voor Content Analytics ingeschakelde gebeurtenisdataset.
1. De service voor detectie van functies bepaalt welke gegevens in die momentopname relevant zijn voor inhoudsanalyses en herziet de ervaring en elementen van deze weergaven van webafbeeldingen.
1. Op de revisit, worden de specifieke gegevens van de inhoudanalyse verzameld door een juiste configuratie van de Edge Network van het Web SDK van het Experience Platform en van het Experience Platform. En dan worden de gegevens verzonden naar een specifieke dataset van de inhoudsanalyse en relevante raadplegingsdatasets.
1. De service voor het samenstellen van functies en de identiteitsservice verwerken de herziene gegevens.
1. De resultaten van deze diensten (componenten, kenmerken en identiteiten) worden gebruikt om de relevante specifieke gegevenssets voor inhoudsanalyses in Experience Platform bij te werken.
1. De gegevens van de inhoudsanalyse, samen met gedragsgegevens en andere raadplegingsdatasets, kunnen dan in een configuratie van de Customer Journey Analytics (Verbinding, de mening van Gegevens en Workspace) worden gebruikt. Die configuratie vormt de basis voor de unieke macroniveauinzichten van uw inhoud.

>[!MORELIKETHIS]
>
>[ Analytics van de Inhoud van het Gebruik (t.b.d.) ](#value)
>[Inhoud analyseren configureren ](config/configuration.md)
