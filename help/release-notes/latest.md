---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste release Customer Journey Analytics
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: daf41a2aefeebe6339b4f86cc04c071b57887ce3
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 4%

---

# Opmerkingen bij de huidige Adobe Customer Journey Analytics-release (juli 2023)

**Laatste update**: 10 juli 2023

Adobe Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Adobe Product Analytics** | Adobe Product Analytics is een nieuwe manier om te communiceren met kanaalgegevens en inzichten in Customer Journey Analytics. Dankzij deze nieuwe mogelijkheden kunnen productteams gegevens en inzichten over hun productervaring zelf bedienen via geleide &#x200B; voor analyses. Teams kunnen:<ul><li>Begrijp patronen in gebruikersbetrokkenheid in tijd &#x200B;</li><li>De groei en het behoud van de &#x200B; van de gebruiker bijhouden</li><li>Wrijvingsgebieden in het product identificeren</li><li>De impact van &#x200B; en eerste gebruik van functies meten</li><li>Ontdek betekenisvolle segmenten van gebruikers om zich gedurende hun hele levenslange reis met het product te engageren en te voeden &#x200B;</li><li>Verbinding maken met Analysis Workspace voor uitgebreidere analyse en samenwerking met analisten</li></ul>Adobe Product Analytics is een betaalde aanvulling op Customer Journey Analytics. Neem contact op met het accountteam van uw Adobe als uw organisatie deze functie wil gebruiken. [Meer informatie](/help/guided-analysis/overview.md) | N.v.t. | 17 juli 2023 |
| **Afgeleide velden** | Dit vertegenwoordigt de aanvankelijke versie van Afgeleide gebieden. Een afgeleid gebied staat u toe om (vaak complexe) gegevensmanipulaties op de vlucht, door een klantgerichte regelbouwer te bepalen. U kunt het afgeleide veld verder definiëren als een component (metrisch of dimensionaal) in gegevensweergaven en het afgeleide veld vervolgens gebruiken als een component in Workspace.<p>Deze release ondersteunt een sjabloon voor marketingkanalen en de volgende functies:</p><ul><li>Samenvoegen</li><li>Hoofdletters/kleine letters</li><li>Zoeken en vervangen</li><li>Opzoeken</li><li>URL-parsering</li></ul> <p>[Meer informatie](/help/data-views/derived-fields/derived-fields.md)</p> | 10 mei 2023 | 2 augustus 2023 |
| **Uitgebreide opzoekondersteuning voor profiel- en opzoekgegevens** | Verstrekt de capaciteit om datasets als raadplegingen van gebieden binnen de datasets van het Profiel of van de Opzoekopdracht toe te voegen. Eerder werden alleen gegevenssets voor gebeurtenissen ondersteund. [Meer informatie] | 21 juni 2023 | 12 juli 2023 |
| **Report Builder-verbeteringen** | <ul><li>Filter van cel voor meerdere gegevensblokken. U kunt de filters op meerdere gegevensblokken in een cel wijzigen. Gebruik een vooraf gedefinieerde cel, wijs deze toe aan meerdere gegevensblokken en werk de gegevens bij op basis van de filters die in de cel zijn gedefinieerd. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-reportbuilder/select-data-view.html?lang=en)</li><li>Rij- en kolomkoppen tonen en verbergen. U kunt gegevensbloktabelkoppen of rij- en kolomkoppen weergeven of verbergen om de tabel opnieuw op te maken en gegevensblokken in een rapport uit te lijnen. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-reportbuilder/create-a-data-block.html?lang=en#build-the-data-block)</li></ul> | N.v.t. | 19 juli 2023 |
| **Ervaar Edge-geo-zoekopdrachten** | Adobe Experience Edge voegt een geografische opzoekservice toe die alle Experience Edge-gebruikers (Adobe Analytics, Customer Journey Analytics, Adobe Target, Adobe Media Analytics, Adobe Experience Platform, enz.) uniforme geografische gegevens biedt. | N.v.t. | 26 juli 2023 |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-317971; AN-319234; AN-320439; AN-320519; AN-321740; AN-322444; AN-323116

## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Wijzigingen in de manier waarop Customer Journey Analytics gegevens verwerkt** | 22 juni 2023 | We hebben onlangs veranderd hoe we gegevens verwerken in Customer Journey Analytics.<ul><li>Alle gebeurtenisgegevens met een tijdstempel van minder dan 24 uur oud worden gestreamd.</li><li>Alle gebeurtenisgegevens met een tijdstempel van meer dan 24 uur oud (zelfs als deze zich in dezelfde batch bevinden als nieuwere gegevens) worden beschouwd als backfill en worden bij een lagere prioriteit opgenomen.</li></ul> |

{style="table-layout:auto"}

## Aankondigingen einde levensduur (EOL)

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar AdobeIO OAuth Server-to-Server-referenties** | 11 mei 2023 | Adobe Analytics API-, Customer Journey Analytics API- en Livestream-klanten die AdobeIO JWT-gebruikersgegevens gebruiken, moeten naar AdobeIO OAuth Server-to-Server-referenties migreren door **1 januari 2025**. AdobeIO staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Het gebruiken van de nieuwe geloofsbrieven van Server-aan-Server OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release van Customer Journey Analytics voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
