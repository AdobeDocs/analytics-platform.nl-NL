---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste CJA-release
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 0fdf95906e17b9e90fa6ba652aa8e53f695279a4
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 6%

---

# Opmerkingen bij de huidige release van Customer Journey Analytics (CJA) (mei 2023)

**Laatste update**: 31 mei 2023

Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Belangrijke functies en updates

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Adobe Journey Optimizer-gegevensweergaven** | CJA Admins heeft toegang tot sommige extra gegevensmeningen in CJA, getiteld &quot;de mening van Gegevens AJO (zandbak-naam)&quot;. Deze gegevensweergaven worden gebruikt om de rapporten in Adobe Journey Optimizer (AJO) aan te sturen. Zij kunnen ook worden gebruikt voor een diepgaande analyse van AJO-activiteiten in CJA. [Meer informatie](https://experienceleague.adobe.com/docs/journey-optimizer/using/campaigns/content-experiment/reporting-configuration.html). |  | 25 mei 2023 |
| **Backfill voor niet-productiesandboxen** | Wanneer u een gegevensstroom van de Analytics Source Connector maakt in een niet-productiesandbox, wordt de back-up van niet-productiesandboxen beperkt tot 3 maanden. Het zal 13 maanden blijven voor productie zandbakken. | N.v.t. | 26 april 2023 |
| **Het delen van verbindingen voor projecten (geen vereiste login)** | U kunt nu alleen-lezen koppelingen naar Analysis Workspace-projecten delen met mensen die geen toegang hebben tot Adobe Analytics. Dit omvat het delen met mensen buiten uw organisatie of met mensen binnen uw organisatie die niet zijn ingericht voor Adobe Analytics. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/share-projects.html?lang=en#share-public-link) <p>Deze functionaliteit is standaard ingeschakeld en kan door de systeembeheerder worden uitgeschakeld. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/user-preferences.html?lang=en#ims-organization-preferences)</p> | 3 mei 2023 | 5 juni 2023 |
| **Bijgewerkt startscherm voor de app Analytics-dashboards (Mobile App)** | Het nieuwe bijgewerkte scherm van het Huis staat u toe om elk van uw scorecards in één geconsolideerde scorecard lijst te bekijken.  Als u toegang tot meer dan één organisatie onder één login hebt, zullen alle scorecards van uw organisaties in één enkele lijst beschikbaar zijn. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dashboards/executive.html#use-dashboards) | N.v.t. | 10 mei 2023 |
| **Afgeleide velden** | Dit vertegenwoordigt de aanvankelijke versie van Afgeleide gebieden. Een afgeleid gebied staat u toe om (vaak complexe) gegevensmanipulaties op de vlucht, door een klantgerichte regelbouwer te bepalen. U kunt het afgeleide veld verder definiëren als een component (metrisch of dimensionaal) in de gegevensweergave en het afgeleide veld vervolgens gebruiken als een component in Workspace.<p>Deze release ondersteunt een sjabloon voor marketingkanalen en de volgende functies:</p><ul><li>Samenvoegen</li><li>Hoofdletters/kleine letters</li><li>Zoeken en vervangen</li><li>Opzoeken</li><li>URL-parsering</li></ul> <p>[Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/derived-fields.html)</p> | 10 mei 2023 | 2 augustus 2023 |
| **Report Builder voor CJA - Gegevensweergave selecteren uit cel** | Met deze functie kunnen gebruikers de gegevensweergave selecteren voor een gegevensblok in een cel. Dit is nuttig als u een werkboek creeert en u veelvoudige gegevensmeningen hebt die de gelijkaardige gegevensbouw hebben en u een werkboek wilt kunnen veelvoudige tijden, met verschillende gegevensmeningen opnieuw gebruiken. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-reportbuilder/select-data-view.html) | N.v.t. | 24 mei 2023 |
| **Componenten sorteren in Analysis Workspace** | <p>Er is nu een nieuwe sorteeroptie beschikbaar wanneer u componenten in de linkertrack of in het gegevenswoordenboek in Analysis Workspace bekijkt. U kunt componenten sorteren op Aanbevolen (de meest gebruikte), Alfabetisch of Categorisch (type).</p><p>Eerder kon u alleen componenten zoeken of filteren. [Meer informatie](/help/components/overview.md)</p> | N.v.t. | TBD |
| **Rijen met dynamische afmetingen uit een tabel voor vrije vorm verwijderen** | In een Freeform-tabel in Analysis Workspace kunt u nu snel specifieke rijen met dynamische afmetingen verwijderen met het x-pictogram. Hierbij wordt automatisch de filterregel &#39;Items altijd uitsluiten&#39; toegepast.<p>Eerder, de enige manier om rijen te schrappen die dynamische afmetingen bevatten was manueel een regel in de dialoog van de Filter te creëren. [Meer informatie](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md)</p> | N.v.t. | 17 mei 2023 |
| **Nieuwe knop om een visualisatie in een deelvenster toe te voegen** | Er is nu een nieuwe knop beschikbaar onder aan elk deelvenster in Analysis Workspace, zodat u snel een visualisatie kunt toevoegen. <p>Eerder, de enige methodes om een visualisatie aan een paneel toe te voegen waren een visualisatie van de linkerspoorstaaf te slepen, een bestaande visualisatie te dupliceren of te kopiëren, of een leeg paneel tot stand te brengen. [Meer informatie](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md)</p> | N.v.t. | 17 mei 2023 |
| **Diepe koppeling (mobiele toepassing)** | Hiermee kunnen gebruikers koppelingen naar scorecards verzenden die rechtstreeks naar het scorecard-project in de app leiden. Hierdoor wordt het nog eenvoudiger om projecten te delen en de betrokkenheid van minder technische gebruikers te verhogen. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dashboards/create-scorecard.html#share-scorecards-using-a-shareable-link) | N.v.t. | 17 mei 2023 |
| **Intelligente bijschriften** | Verrijk het vertellen van verhalen voor gebruikers met natuurlijke taalsamenvattingen van a [!UICONTROL Line] visualisatie. [Meer informatie](/help/analysis-workspace/visualizations/intelligent-captions.md) | 17 mei 2023 | 1 juni 2023 |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-316412; AN-317105; AN-318122; AN-317353

## Belangrijke kennisgevingen voor CJA-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | N.v.t. | N.v.t. |

## Aankondigingen einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar AdobeIO OAuth Server-to-Server-referenties** | 11 mei 2023 | Adobe Analytics API-, CJA API- en Livestream-klanten die AdobeIO JWT-gebruikersgegevens gebruiken, moeten naar AdobeIO OAuth Server-to-Server-referenties migreren door **1 januari 2025**. AdobeIO staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Het gebruiken van de nieuwe geloofsbrieven van Server-aan-Server OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul>![](assets/jwt.png) |

{style="table-layout:auto"}

## Gerelateerde bronnen

* [Opmerkingen bij de vorige CJA-release voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
