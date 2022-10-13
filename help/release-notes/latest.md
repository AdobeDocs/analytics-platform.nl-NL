---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste CJA-release
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: ed5b1a233dc0e4cbfe223fe71e6e1960efba0592
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opmerkingen bij de release Customer Journey Analytics (CJA) (oktober 2022)

**Laatste update**: 13 oktober 2022

Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Gerelateerde bronnen

* [Opmerkingen bij de vorige CJA-release voor 2022](/help/release-notes/2022.md)

* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)

* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)

* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)

## Belangrijke functies en updates

| Functie | Beschrijving | [Doeldatum](/help/release-notes/releases.md) |
| ----------- | ---------- | ----- |
| **Deelvenster Experimentatie** | Met dit nieuwe deelvenster Werkruimte kunnen CJA-gebruikers de lift en het vertrouwen evalueren van een A/B-experiment vanuit elke bron - online, offline, vanuit Adobe-oplossingen, Adobe Journey Optimizer en zelfs BYO-gegevens. [Meer informatie](/help/analysis-workspace/c-panels/experimentation.md) | 5 oktober 2022 |
| **[!UICONTROL Key metric summary]visualisatie** | De [!UICONTROL Key metric summary] Met visualisatie kunt u zien hoe een belangrijke metriek binnen één tijdsperiode trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. Meer informatie | Geleidelijke uitrol vanaf 5 oktober 2022 |
| **Datumveldondersteuning in CJA** | Staat CJA toe om op datum en datum-tijd gebieden te melden. [Meer informatie](/help/data-views/data-views-usecases.md#date) | 5 oktober 2022 |
| **Mobiele app: Aangepaste detailweergaven** | Met de gedetailleerde weergaven van Aangepast kunt u zich nog meer richten op de informatie die u deelt met uw publiek, doordat u deze kunt richten op wat het belangrijkst is. U kunt de lay-out van de detailmening veranderen verbonden aan elke scorecardtegel en u kunt tekst toevoegen om beter te verklaren wat de eindgebruiker in de gegevens kan zien. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dashboards/create-scorecard.html?lang=en) | 5 oktober 2022 |
| **Niet-hoofdlettergevoelige meerwaardevariabelen** | Voor niet-hoofdlettergevoelige meerwaardevariabelen worden de waarden opgeslagen in `mvvar1` - `mvvar3` wordt niet meer automatisch verlaagd. In plaats daarvan, zullen de gegevens die door de Verbinding van de Bron van Analytics aan Adobe Experience Platform en CJA worden overgegaan op het originele geval wijzen dat van de pagina werd overgegaan. | 24 oktober 2022 |

{style=&quot;table-layout:auto&quot;}

## Belangrijke kennisgevingen voor CJA-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Standaardlandingspagina** | 29 september 2023 | De [nieuwe bestemmingspagina](/help/getting-started/landing.md) die eerder dit jaar is geïntroduceerd, wordt de standaardeigenschap voor alle gebruikers in de **Januari 2023**. De huidige pagina wordt afgekeurd en iedereen moet de nieuwe ervaring gebruiken. |
| **Verbeterde IP-naar-geolocatietoewijzing** | 29 september 2022 | Digitaal verkoper voor IP raadplegingen, Element, bevordert aan een nieuwe betere dataset (de Pulse van de NetAcuity) voor IP-aan-geolocatietoewijzing. Adobe Analytics heeft de goedkeuring van deze nieuwe gegevensset uitgesteld tot **Januari 2023**. De nieuwe database is nauwkeuriger dan vorige versies. Sommige IP-aan-geo afbeeldingen zullen veranderen/verbeteren wanneer het nieuwe gegevensbestand wordt goedgekeurd.<p> CJA-gegevens verstrekt via [!UICONTROL Analytics Source Connector] zal ook automatisch voordeel van de nieuwe afbeeldingen halen. |
| **[!UICONTROL Anomaly detection]automatisch afloopcondities** | 29 september 2022 | Vandaag, [!UICONTROL Anomaly detection] auto-looppas op alle kolommen van tijd-reeksen vrije lijsten. Om ervoor te zorgen dat gegevens beschikbaar zijn voor analyse en projecten sneller worden geladen, wijzigt Adobe hoe [!UICONTROL Anomaly detection] automatisch uitgevoerd. Starten **26 oktober 2022** Anomaly-detectie wordt alleen automatisch uitgevoerd voor de eerste metrische kolom in een tabel. U kunt kolominstellingen configureren om uit te voeren [!UICONTROL Anomaly detection] op andere kolommen, indien nodig. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>[Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
