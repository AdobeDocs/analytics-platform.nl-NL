---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste release Customer Journey Analytics
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 2dab438b956513eaff3f05d2ff8de2fff43d9977
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 5%

---

# Huidige Adobe Customer Journey Analytics-releaseopmerkingen (augustus 2023)

**Laatste update**: 9 augustus 2023

Deze releaseopmerkingen hebben betrekking op de releaseperiode van 9 augustus tot 13 september 2023. Adobe Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Report Builder-verbeteringen** | <ul><li>Download geplande taken vanaf het tabblad Historie, waar u de geschiedenis van geplande taken kunt weergeven. Download het werkboek van die taak. </li><li>Begindatum als dimensie: stelt gebruikers in staat de begindatum van het gegevensblok als een dimensie in de uitvoer van het gegevensblok aan te geven. </li></ul> | N.v.t. | 17 augustus 2023 |
| **Valutaconversie** | Klantreis voegt de mogelijkheid toe om meerdere valuta&#39;s te ondersteunen. U kunt een valuta converteren naar een andere valuta in de weergave-instellingen voor gegevens. [Meer informatie](/help/data-views/component-settings/format.md) | N.v.t. | 31 augustus 2023 |
| **Steun voor classificaties A4T in de Bron van Analytics Schakelaar** | We voegen een correlatie-id toe voor het eenvoudig samenvoegen van classificatiegegevens voor Adobe Target-activiteiten en ervaringsgebeurtenissen. | N.v.t. | 31 augustus 2023 |
| **Activity Manager rapporteren** | Biedt beheerders gedetailleerde zichtbaarheid bij het rapporteren van verbruik voor elke verbinding, zodat beheerders eenvoudig capaciteitsproblemen tijdens piekrapportagetijden kunnen vaststellen en verhelpen. | N.v.t. | 6 september 2023 |
| **PowerBI en Tableau toegang tot Customer Journey Analytics-gegevensweergaven** | Met de Adobe Customer Journey Analytics SQL-connector krijgt SQL toegang tot gegevensweergaven die u in Customer Journey Analytics hebt gedefinieerd. De ingenieurs en de analisten van gegevens vertrouwd met Power BI, Tableau, of andere bedrijfsintelligentie en visualisatiehulpmiddelen kunnen nu rapporten en dashboards tot stand brengen die op de zelfde gegevensmeningen worden gebaseerd die de gebruikers van Customer Journey Analytics voor hun projecten van Analysis Workspace gebruiken. [Meer informatie](/help/data-views/sql-connector.md) | N.v.t. | 13 september 2023 |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-309141; AN-319198; AN-324576; AN-324939; AN-325138; AN-325554

## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Wijzigingen in de manier waarop Customer Journey Analytics gegevens verwerkt** | 22 juni 2023 | We hebben onlangs veranderd hoe we gegevens verwerken in Customer Journey Analytics.<ul><li>Alle gebeurtenisgegevens met een tijdstempel van minder dan 24 uur oud worden gestreamd.</li><li>Alle gebeurtenisgegevens met een tijdstempel van meer dan 24 uur oud (zelfs als deze zich in dezelfde batch bevinden als nieuwere gegevens) worden beschouwd als backfill en worden bij een lagere prioriteit opgenomen.</li></ul> |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL)

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API-, Customer Journey Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar de gebruikersgegevens van Adobe I/O OAuth Server-to-Server migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release van Customer Journey Analytics voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
