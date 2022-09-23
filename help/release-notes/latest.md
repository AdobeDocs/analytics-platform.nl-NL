---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste CJA-release
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: d2aec8976d7d81c28a6b9b76c58fec0fc2c3b360
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 4%

---

# Opmerkingen bij de release Current Customer Journey Analytics (CJA) (september 2022)

**Laatste update**: 14 september 2022

Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Gerelateerde bronnen

* [Opmerkingen bij de vorige CJA-release voor 2022](/help/release-notes/2022.md)

* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)

* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)

* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)

## Belangrijkste kenmerken

| Functie | Beschrijving | [Doeldatum](/help/release-notes/releases.md) |
| ----------- | ---------- | ----- |
| **Ondersteuning voor verschillende regio&#39;s voor de analytische bronconnector** | U kunt nu rapportsuites uit om het even welke regio (Verenigde Staten, Verenigd Koninkrijk, of Singapore) opnemen. Deze rapportsuites moeten echter worden toegewezen aan dezelfde organisatie als de Sandbox-instantie van het Experience Platform waarin de bronverbinding wordt gemaakt. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) | 24 augustus 2022 |
| **Eerste sessiemelding** | Ontdek of een bepaalde zitting de eerste-ooit zitting van een gebruiker was. [Meer informatie](/help/data-views/data-views-usecases.md) | 24 augustus 2022 |
| **Deelvenster Experimentatie voor CJA** | Met dit nieuwe deelvenster Werkruimte kunnen CJA-gebruikers de lift en het vertrouwen evalueren van een A/B-experiment vanuit een willekeurige bron - online, offline, vanuit Adobe-oplossingen, Adobe Journey Optimizer en zelfs BYO-gegevens (uw eigen gegevens leveren). [Meer informatie](/help/analysis-workspace/c-panels/experimentation.md) | [Beperkte release](/help/release-notes/releases.md) 14 september 2022 |
| **Visualisatie van combinatieteksten in werkruimte** | Met combinatiekaarten kunt u metrische gegevens in Workspace gemakkelijker en intuïtiever vergelijken. [Meer informatie](/help/analysis-workspace/visualizations/combo-charts.md) | 14 september 2022 |
| **CJA-ondersteuning voor labels en beleid voor gegevensbeheer** | Automatiseert de integratie tussen CJA en Adobe Experience Platform privacy labels en beleid. De etiketten van gegevens die op datasets worden gecreeerd die door Platform worden verbruikt worden bedekt in CJA- gegevensmeningen om gebruikers tegen te houden of te waarschuwen die metriek en/of dimensies van gevoelige gebieden tot stand brengen. Daarnaast geldt dat wanneer gegevens worden geëxporteerd vanuit CJA (via Workspace of Report Builder-rapportage, export, API, enzovoort) extra waarschuwingen of etiketten zullen worden toegevoegd om gebruikers mee te delen dat een rapport gevoelige informatie bevat die op een specifieke manier moet worden behandeld. [Meer informatie](/help/data-views/data-governance.md) | 14 september 2022 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen

AN-298412

## Belangrijke kennisgevingen voor CJA-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Verbeterde IP-naar-geolocatietoewijzing** | 9 september 2022 | Digitaal verkoper voor IP raadplegingen, Element, bevordert aan een nieuwe betere dataset (de Pulse van de NetAcuity) voor IP-aan-geolocatietoewijzing. Adobe Analytics zal dit nieuwe gegevensbestand goedkeuren op **5 oktober 2022**. De nieuwe database is nauwkeuriger dan vorige versies. Sommige IP-aan-geo afbeeldingen zullen veranderen/verbeteren wanneer het nieuwe gegevensbestand wordt goedgekeurd.<p> De gegevens CJA die door de Bronschakelaar van de Analyse worden verstrekt zullen automatisch uit de nieuwe afbeeldingen voordeel halen. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>[Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
