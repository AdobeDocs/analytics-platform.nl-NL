---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste CJA-release
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 64a774d9151c40ea9eadb1fb80c07db168ac8667
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 6%

---

# Opmerkingen bij de huidige release van Customer Journey Analytics (CJA) (april 2023)

**Laatste update**: 12 april 2023

Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Belangrijke functies en updates

| Functie | Beschrijving | [Begin van rollout](/help/release-notes/releases.md) | [Algemene beschikbaarheid](/help/release-notes/releases.md) |
| ----------- | ---------- | ----- | --- |
| **Rij-/kolomfiltering voor streaming van Analyse Source Connector** | Met de Bronverbinding Analytics in Adobe Experience Platform kunt u nu analysegegevens filteren die worden gebruikt om profielen te vullen in [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en). Filteren op rijniveau helpt het aantal gebeurtenissen dat aan profielen is gekoppeld, te verminderen. Filteren op kolomniveau helpt de rijkheid van de gebeurtenissen zelf te verminderen, zodat u het gebruik van profielrechten kunt optimaliseren. Deze filtering is alleen van toepassing op gegevens die naar het realtime-klantprofiel worden verzonden en [Identiteitsservice](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=en). **Filteren heeft geen invloed op de gegevens die naar het Data Lake worden verzonden voor gebruik in toepassingen zoals Customer Journey Analytics**. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en#filtering-for-profile) | N.v.t. | 29 maart 2023 |
| **Gegevenswoordenboek in Analysis Workspace** | Met het gegevenswoordenboek kunnen gebruikers en beheerders de componenten (afmetingen, meetgegevens) in hun CJA-omgeving bijhouden en beter begrijpen. [Meer informatie](/help/components/data-dictionary/data-dictionary-overview.md) | 8 maart 2023 | 29 maart 2023 |
| **Het delen van verbindingen voor projecten (geen vereiste login)** | <p>U kunt nu alleen-lezen koppelingen naar Analysis Workspace-projecten delen met mensen die geen toegang hebben tot Adobe Analytics. Dit omvat het delen met mensen buiten uw organisatie, of die binnen uw organisatie die niet provisioned voor CJA zijn. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/share-projects.html?lang=en#share-public-link)</p> <p>Deze functionaliteit is standaard ingeschakeld en kan door de systeembeheerder worden uitgeschakeld. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/user-preferences.html?lang=en#company-preferences)</p> | 26 april 2023 (alleen voor toegang tot bèta uit de particuliere sector) | Juni 2023 |
| **Adobe Product Analytics - Alleen persoonlijke bètatoegang** | Op 21 maart 2023 kondigde Adobe Product Analytics van Adobe aan, een nieuwe manier om met kanaalgegevens en inzichten in Customer Journey Analytics te communiceren. Dankzij deze nieuwe mogelijkheden kunnen productteams gegevens en inzichten over hun productervaring zelf bedienen via geleide &#x200B; voor analyses. Teams kunnen:<ul><li>Begrijp patronen in gebruikersbetrokkenheid in tijd &#x200B;</li><li>De groei van &#x200B; analyseren</li><li>Wrijvingsgebieden in een reeks stappen identificeren &#x200B;</li><li>De impact van &#x200B; meten</li><li>Ontdek zinvolle segmenten om gedurende hun hele levenslange reis met het product &#x200B; te gaan en te voeden</li><li>Open in Analysis Workspace voor een diepgaande analyse en samenwerking met analisten en nog veel meer! &#x200B;</li></ul>Neem contact op met het accountteam van Adobe als u een CJA-klant bent en u wilt deelnemen aan de persoonlijke bètaversie. [Meer informatie](https://business.adobe.com/products/product-analytics/adobe-product-analytics.html) | N.v.t. | 17 juli 2023 |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-313118; AN-313390; AN-314135; AN-316381; AN-316811

## Belangrijke kennisgevingen voor CJA-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | N.v.t. | N.v.t. |

{style="table-layout:auto"}

## Gerelateerde bronnen

* [Opmerkingen bij de vorige CJA-release voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
