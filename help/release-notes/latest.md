---
title: De opmerkingen bij de huidige release van de Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste release Customer Journey Analytics
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 2b8712506d68d89d41668fac32bb669055d94e91
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 3%

---

# Opmerkingen bij de huidige Adobe Customer Journey Analytics-release (oktober 2023)

**Laatste update**: 4 oktober 2023

Deze opmerkingen hebben betrekking op de releaseperiode van 4 oktober 2023 tot en met 24 oktober 2023. Adobe Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Volledige tabellen exporteren naar de cloud** | Met de Customer Journey Analytics Full Table Export kunt u miljoenen rijen in de werkruimte exporteren naar cloudinstellingen. Het uitvoeren van volledige lijsten biedt eenmalige of geplande levering van gegevenslijsten die binnen Werkruimte met steun voor maximaal vijf onderbrekingen, vijf metriek, filters, en berekende metriek, allen in een samengevoegde lijst worden ontworpen. Het is de evolutie van de rapporten van de Data Warehouse in Adobe Analytics, met vele nieuwe, vaak gevraagde eigenschappen die niet beschikbaar in de Data Warehouse vandaag zijn. Exportopties voor cloud omvatten:<ul><li>Adobe Experience Platform Data Landing Zone</li><li>Amazon S3 Role ARN</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li><li>Snowflake</li></ul>Zie voor meer informatie [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/export/export-cloud.html). | 4 oktober 2023 | 19 oktober 2023 |
| **Nieuwe kolommen beschikbaar bij het beheren van componenten** | De volgende nieuwe kolommen zijn nu beschikbaar in de [Het berekende manager van metriek](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-manager.html) en de [Filterbeheer](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/cja-filters/manage-filters.html) bij het beheren van componenten:<ul><li>Gebruikt in</li><li>Laatst gebruikt</li></ul>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd. U kunt het gegevenswoordenboek samen met deze informatie gebruiken om u te helpen bij het volgen van en beter begrijpen hoe de componenten in uw organisatie worden gebruikt. | 23 september 2023 | 4 oktober 2023 |
| **Adobe Analytics-projecten en alle inbegrepen onderdelen migreren naar Customer Journey Analytics** | U kunt nu uw Adobe Analytics-projecten migreren naar Customer Journey Analytics. Dit proces vereenvoudigt de overgang van Adobe Analytics naar Customer Journey Analytics. Wanneer u projecten naar Customer Journey Analytics migreert, worden de activa in kaart gebracht van een het rapportreeks van Adobe Analytics aan een de gegevensmening van de Customer Journey Analytics. **U migreert projecten aan Customer Journey Analytics van de interface van Adobe Analytics.** [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration.html) | N.v.t. | 4 oktober 2023 |
| **Adobe Product Analytics: Reeks tonen/verbergen** | Klik op de diagramlegenda of tabelrijen om de zichtbaarheid van reeksen in uw visualisaties te bepalen.  Meer informatie (binnenkort beschikbaar) | N.v.t. | 4 oktober 2023 |
| **Annotaties in Adobe Product Analytics** | De geleide analyseprojecten steunen nu de capaciteit om annotaties te bekijken. Verwijs naar elk meningstype in [Analyse met instructies](/help/guided-analysis/overview.md) voor meer informatie over de interactie met annotaties. Meer informatie (binnenkort beschikbaar) | N.v.t. | 4 oktober 2023 |
| **Activity Manager rapporteren** | De manager van de Activiteit van de Rapportering laat u de rapporteringscapaciteit voor elke verbinding in uw organisatie zien. Het biedt beheerders gedetailleerde zichtbaarheid bij het melden van het verbruik om capaciteitsproblemen tijdens piekrapportagetijden eenvoudig te kunnen vaststellen en verhelpen. De belangrijkste kenmerken van de manager van de activiteit van de Rapportering omvatten:<ul><li>Huidige rapportageverzoeken annuleren (inclusief verzoeken van geleide analyses en volledige tabelexport)</li><li>Verdere verzoeken voor een bepaalde periode beperken</li></ul>Naast het annuleren van huidige verzoeken, kunnen de beheerders verzoeken voor een bepaalde tijdspanne nu beperken. De beheerders kunnen verzoeken door verzoek, project, of gebruiker beperken.  Meer informatie (binnenkort beschikbaar) | 17 oktober 2023 | 23 oktober 2023 |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-325940; AN-326468; AN-328301; AN-328640; AN-329370

## Belangrijke kennisgevingen voor beheerders van Customers Journey Analytics

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | N.v.t. | N.v.t. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL)

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API, Customer Journey Analytics API, en LiveStream klanten die de geloofsbrieven van JWT van Adobe I/O gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door migreren **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release van Customer Journey Analytics voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl)
* [Documentatieupdates Customer Journey Analytics](/help/release-notes/doc-changes.md)
