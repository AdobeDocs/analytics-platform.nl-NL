---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste CJA-release
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: fbfc7113aef8857e11ccfba5e5e557eed16c2465
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 3%

---

# Opmerkingen bij de release Customer Journey Analytics (CJA) (oktober/november 2022)

**Laatste update**: 25 oktober 2022

Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Belangrijke functies en updates

| Functie | Beschrijving | [Begin van rollout](/help/release-notes/releases.md) | [Algemene beschikbaarheid](/help/release-notes/releases.md) |
| ----------- | ---------- | ----- | --- |
| **[!UICONTROL Key metric summary]visualisatie** | De [!UICONTROL Key metric summary] Met visualisatie kunt u zien hoe een belangrijke metriek binnen één tijdsperiode trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. [Meer informatie](/help/analysis-workspace/visualizations/key-metric.md) | 5 oktober 2022 | 19 oktober 2022 |
| **Niet-hoofdlettergevoelige meerwaardevariabelen** | Voor niet-hoofdlettergevoelige meerwaardevariabelen worden de waarden opgeslagen in `mvvar1` - `mvvar3` wordt niet meer automatisch verlaagd. In plaats daarvan, zullen de gegevens die door de Verbinding van de Bron van Analytics aan Adobe Experience Platform en CJA worden overgegaan op het originele geval wijzen dat van de pagina werd overgegaan. ASC/CJA-kolommen `_experience.analytics.customDimensions.lists.list1.list[]` - `_experience.analytics.customDimensions.lists.list3.list[]` door deze wijziging worden beïnvloed. | N.v.t. | 24 oktober 2022 |
| **CJA-auditlogboek** | Met Customer Journey Analytics (CJA) kunt u gebruikersactiviteiten voor verschillende services en mogelijkheden controleren in de vorm van &quot;auditlogs&quot;. Deze logboeken vormen een auditspoor dat kan helpen met het oplossen van problemenkwesties, en uw zaken kunnen effectief voldoen aan het beleid en de regelgevende vereisten van het collectieve gegevensbeheer, zoals de Wet van de Portabiliteit en van de Verantwoording van de Ziekteverzekering (HIPAA). Deze logbestanden waren voorheen alleen beschikbaar via de API voor controlelogbestanden. [Meer informatie](/help/privacy/audit-log.md) | N.v.t. | 26 oktober 2022 |
| **Gereedheid van HIPAA** | Adobe ondersteunt nu het ontvangen, gebruiken, onderhouden of doorgeven van beveiligde gezondheidsinformatie in Customer Journey Analytics en andere op Experience Platform gebaseerde toepassingen alleen voor de klant van het gezondheidsschild. Gezondheidsschild is alleen voor klanten in de gezondheidszorg die ofwel een onder de dekking vallende entiteit zijn, ofwel een Business Associate in de VS. [Meer informatie](https://www.adobe.com/trust/compliance/hipaa-ready.html) | N.v.t. | 7 november 2022 |
| **Wachtwoordbeveiliging voor geplande projecten** | Deze functie maakt deel uit van HIPAA-gereedheid en is alleen van toepassing op klanten van het gezondheidszorgschild. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/t-schedule-report.html#password) | N.v.t. | 7 november 2022. |

{style=&quot;table-layout:auto&quot;}

## Oplossingen

* Probleem verholpen waarbij recente MacOS-versies onjuist werden aangeduid als &quot;Macintosh&quot;. Met deze correctie begint de dimensie van het besturingssysteem met het gebruik van &quot;MacOS&quot;-versienummering, te beginnen met MacOS 11. (AN-301834)

### Overige correcties

AN-302367; AN-302562; AN-304036

## Belangrijke kennisgevingen voor CJA-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Standaardlandingspagina** | 29 september 2023 | De [nieuwe bestemmingspagina](/help/getting-started/landing.md) die eerder dit jaar is geïntroduceerd, wordt de standaardeigenschap voor alle gebruikers in de **Januari 2023**. De huidige pagina wordt afgekeurd en iedereen moet de nieuwe ervaring gebruiken. |
| **Verbeterde IP-naar-geolocatietoewijzing** | 29 september 2022 | Digitaal verkoper voor IP raadplegingen, Element, bevordert aan een nieuwe betere dataset (de Pulse van de NetAcuity) voor IP-aan-geolocatietoewijzing. Adobe Analytics heeft de goedkeuring van deze nieuwe gegevensset uitgesteld tot **Januari 2023**. De nieuwe database is nauwkeuriger dan vorige versies. Sommige IP-aan-geo afbeeldingen zullen veranderen/verbeteren wanneer het nieuwe gegevensbestand wordt goedgekeurd.<p> CJA-gegevens verstrekt via [!UICONTROL Analytics Source Connector] zal ook automatisch voordeel van de nieuwe afbeeldingen halen. |
| **[!UICONTROL Anomaly detection]automatisch afloopcondities** | 29 september 2022 | Vandaag, [!UICONTROL Anomaly detection] auto-looppas op alle kolommen van tijd-reeksen vrije lijsten. Om ervoor te zorgen dat gegevens beschikbaar zijn voor analyse en projecten sneller worden geladen, wijzigt Adobe hoe [!UICONTROL Anomaly detection] automatisch uitgevoerd. Starten **26 oktober 2022** Anomaly-detectie wordt alleen automatisch uitgevoerd voor de eerste metrische kolom in een tabel. U kunt kolominstellingen configureren om uit te voeren [!UICONTROL Anomaly detection] op andere kolommen, indien nodig. |

{style=&quot;table-layout:auto&quot;}


## Gerelateerde bronnen

* [Opmerkingen bij de vorige CJA-release voor 2022](/help/release-notes/2022.md)

* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)

* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)

* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)

* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
