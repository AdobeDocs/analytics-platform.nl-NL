---
title: De opmerkingen bij de huidige release van de Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste release Customer Journey Analytics
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: abaa747934ff2cdd0a3dab867165afb46fbc71db
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 2%

---

# Huidige Adobe Customer Journey Analytics-releaseopmerkingen (april 2024)

**Laatste update**: 17 april 2024

Deze opmerkingen hebben betrekking op de releaseperiode van 10 april 2024 tot en met mei 2024. Adobe Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Streaming media: Roku-gegevens verzenden naar Adobe Experience Platform Edge** | Wanneer [Media Analytics installeren met Experience Platform Edge](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge)kunt u de Adobe Experience Platform Roku SDK gebruiken om streaming Media-gegevens naar Adobe Experience Platform te verzenden. |  | zaterdag 12 april 2024 |
| **Gemaakte maandelijkse rapporten in de Manager van de Activiteit van de Rapportering** | Wanneer het bekijken van rapporteringsactiviteit voor alle verbindingen in de Manager van de Activiteit van de Rapportering, is een grafiek nu beschikbaar die toont [maandelijkse rapporten/verzoeken](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity#view-all-report-suites) die werden uitgevoerd op IMS Org-niveau, voor zowel de huidige als de vorige maand.<p>**Opmerking:** De gegevens zijn beschikbaar vanaf begin tot en met de maand maart 2024. | | dinsdag 15 april 2024 |
| **Intelligente bijschriften in mobiele scorecards** | [Intelligente bijschriften](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dashboards/manage-scorecard#captions) kunnen niet-analisten helpen hun gegevens beter te begrijpen zonder de hulp van analisten. Ze zijn nu beschikbaar in Customer Journey Analytics scorecards. |  | donderdag 17 april 2024 |
| **Verbetering van machtigingen voor alleen project [!UICONTROL Workspace] componenten** | Eerder, als één gebruiker (Gebruiker A) een project met een andere gebruiker (Gebruiker B) deelde, en Gebruiker B gaf geeft geeft geeft toegang tot het project uit, zou Gebruiker B het project kunnen uitgeven. Gebruiker B kan echter geen bewerkingen uitvoeren [!UICONTROL Quick Segments] ingesloten in het project. Deze beperking is nu verwijderd. Gebruiker B kan deze bewerken [!UICONTROL Quick Segments] en andere projectgebonden componenten die in het gedeelde project zijn ingesloten. |  | donderdag 17 april 2024 |
| **Beheerders kunnen alle locaties in hun organisatie beheren** | Een nieuwe optie op de knop [Locatiepagina](https://experienceleague.adobe.com/en/docs/analytics/components/locations/locations-manager) Hiermee kunnen beheerders alle locaties in de organisatie weergeven en beheren. Eerder konden beheerders alleen de door hen gemaakte locaties weergeven en beheren. |  | donderdag 17 april 2024 |
| **Adobe Product Analytics: matrix met functies** | Beslissingen over brandstofinvesteringen door te begrijpen wat uw kern, macht, eenmalig en twijfelachtige eigenschappen zijn. [!UICONTROL Feature matrix] meet gebeurtenissen naar gebruiksfrequentie vs % actieve gebruikers en vergelijkt het mediaan gebruik. | donderdag 17 april 2024 | woensdag 30 april 2024 |
| **Adobe Product Analytics: Verbeterde inzichten in de trechter** | In de [Wrijving](https://experienceleague.adobe.com/en/docs/analytics-platform/using/guided-analysis/funnel/friction) de schriftelijke inzichten zijn uitgebreid tot categorieën , delta &#39; s en beschrijvingen om de grafiek en de tabel beter te begrijpen . | donderdag 17 april 2024 | zaterdag 26 april 2024 |
| **Adobe Product Analytics: verbeterde weergave voor behoud** | Er zijn verschillende mogelijkheden toegevoegd aan de [Bewaren](https://experienceleague.adobe.com/en/docs/analytics-platform/using/guided-analysis/retention/retention-rates) de mening van tarieven om diepere &amp; klantgerichte behoudsinzichten te drijven:<ul><li>Start- en retourgebeurtenissen ontkoppelen</li><li>Meerdere retourgebeurtenissen vergelijken in één weergave</li><li>Pas het retentiemodel aan dat met de instellingen aan of na (zonder begrenzing) is toegepast, op elke (met begrenzing) en tussen haakjes geplaatste instelling</li><li>Afzonderlijke cohortrijen in het diagram tonen en verbergen</li></ul> | donderdag 24 april 2024 | donderdag 8 mei 2024 |
| **Adobe Product Analytics: vergelijk gebeurtenissen binnen één enkele stap van de Trechter** | U kunt nu gebeurtenissen vergelijken in één trede in de [Wrijving](https://experienceleague.adobe.com/en/docs/analytics-platform/using/guided-analysis/funnel/friction) weergeven. Dit is met name handig wanneer uw reis stapopties heeft of een stap waarbij een A/B-experiment wordt uitgevoerd. | woensdag 23 april 2024 | zaterdag 3 mei 2024 |
| **B2B-schematransformatie voor rekening van persoon** | Laat u datasets omzetten om op persoon-gebaseerde raadplegingen in Customer Journey Analytics B2B beter te steunen rapporteringsscenario&#39;s. Dit vermogen is beschikbaar voor datasets voor B2B- schema&#39;s die op de volgende klassen worden gebaseerd:<ul><li>XDM Zakelijke account Person Relatie</li><li>XDM Business Opportunity Person Relatie</li><li>Leden van XDM Business Marketing List</li><li>XDM Business Campaign-leden</li></ul> | | donderdag 1 mei 2024 |
| **Ervaar de detectie van Edge-bot** | [Bodemdetectie](https://experienceleague.adobe.com/docs/experience-platform/datastreams/bot-detection.html) staat u toe om gebeurtenissen te identificeren die door Web SDK, Mobiele SDK en Server API worden geproduceerd zoals die door bekende spinnen en bots worden geproduceerd. | | donderdag 1 mei 2024 |
| **Afgeleide velden: functie Volgende of Vorige** | Met deze nieuwe functies kunt u een veld als invoer gebruiken en vervolgens de waarde n-previous of n-next identificeren om een beter beeld te krijgen van de reis van de gebruiker. Deze functionaliteit kan ook worden gecombineerd met andere functies in [!UICONTROL Derived Fields], zoals [!UICONTROL Concatenate]om nieuwe afmetingen te maken. |  | donderdag 1 mei 2024 |
| **Soorten publiek wordt gepubliceerd naar een nieuwe sectie &quot;Soorten publiek&quot; in Experience Platform** | Soorten publiek die vanuit de Customer Journey Analytics worden gepubliceerd, zijn nu beschikbaar in de nieuwe sectie &quot;Soorten publiek&quot; in Adobe Experience Platform.<p>Eerder waren publiek dat vanuit Customer Journey Analytics werd gepubliceerd, beschikbaar in Experience Platform onder de sectie &quot;Segmenten&quot;.</p><p>Deze verbetering biedt de volgende voordelen:</p><ul><li>Het publiek heeft niet langer een vertraging van 1 uur voordat het in het Experience Platform wordt weergegeven; het zijn pas seconden nadat het is gepubliceerd.</li><li>De soorten publiek kunnen in Experience Platform worden gesorteerd door de kolom &quot;Oorsprong&quot;te gebruiken, die de toepassing toont waarvan het publiek oorspronkelijk werd gepubliceerd.</li><li>Met de filter- en sorteeropties in het Experience Platform kunt u sneller het desbetreffende publiek vinden.</li></ul> |  | Mei 2024 |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-319662; AN-337894; AN-338469; AN-340147; AN-340200; AN-340443; AN-341594; AN 342442; AN-342976; AN-343020; AN-343469; AN-343703; AN-343938; AN-344614; AN-3 44677

## Belangrijke kennisgevingen voor beheerders van Customers Journey Analytics

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Bijgewerkte verbindingen in de meningen van Gegevens en Verbindingen UIs** | Februari 15 | Begin maart, is de Adobe van plan om de volgende verbindingen in de het productgebruikersinterface van de Customer Journey Analytics bij te werken. Werk uw bladwijzers dienovereenkomstig bij.<ul><li>**Pagina met gegevensweergaven, Data views Manager**: [Bestaande koppeling](https://experience.adobe.com/#/@aresstagevalidationco/platform/analytics/#/dataViewsCJA/manager) > [Nieuwe koppeling](https://experience.adobe.com/#/@org/platform/analytics/#/apps/data-management/data-views)</li><li>**Nieuwe gegevensweergave maken**: [Bestaande koppeling](https://experience.adobe.com/#/@aresstagevalidationco/platform/analytics/#/dataViewsCJA/new) > [Nieuwe koppeling](https://experience.adobe.com/#/@org/platform/analytics/#/apps/data-management/data-views/new)</li><li>**Gegevensweergave bewerken**: [Bestaande koppeling](https://experience.adobe.com/#/@aresstagevalidationco/platform/analytics/#/dataViewsCJA/edit/dv_65b9f6eba2c6554743236e88) > [Nieuwe koppeling](https://experience.adobe.com/#/@aresemeavalidationco/platform/analytics/#/apps/data-management/data-views/dv_62fde2e158324f2803c9e5d6/edit)</li><li>**Verbindingsbeheer**: [Bestaande koppeling](https://experience.adobe.com/#/@aresstagevalidationco/platform/analytics/#/connections2/manager) > [Nieuwe koppeling](https://experience.adobe.com/#/@org/platform/analytics/#/apps/data-management/connections)</li><li>**Informatie over verbindingen**: [Bestaande koppeling](https://experience.adobe.com/#/@aresstagevalidationco/platform/analytics/#/connections2/view/dg_66749c92-784b-45bb-b114-e9e8377a2fc1) > [Nieuwe koppeling](https://experience.adobe.com/#/@org/platform/analytics/#/apps/data-management/connections/dg_a2b297a6-9220-440d-a403-ee8fbf627cd8)</li><li>**Verbinding bewerken**: [Bestaande koppeling](https://experience.adobe.com/#/@aresstagevalidationco/platform/analytics/#/connections2/edit/dg_66749c92-784b-45bb-b114-e9e8377a2fc1) > [Nieuwe koppeling](https://experience.adobe.com/#/@org/platform/analytics/#/apps/data-management/connections/dg_a2b297a6-9220-440d-a403-ee8fbf627cd8/edit)</li><li>**Nieuwe verbinding maken**: [Bestaande koppeling](https://experience.adobe.com/#/@aresstagevalidationco/platform/analytics/#/connections2/new) > [Nieuwe koppeling](https://experience.adobe.com/#/@org/platform/analytics/#/apps/data-management/connections/new/edit)</li></ul> |

{style="table-layout:auto"}

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release van Customer Journey Analytics voor 2024](/help/release-notes/2024.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Opmerkingen bij de release van Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)
* [Documentatieupdates Customer Journey Analytics](/help/release-notes/doc-changes.md)
