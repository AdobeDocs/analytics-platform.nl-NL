---
title: De opmerkingen bij de huidige release van de Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste release Customer Journey Analytics
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 6ae081aecf0143dd78c3feb4e397bb4f7ba32c68
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 2%

---

# Huidige Adobe Customer Journey Analytics-releaseopmerkingen (mei 2024)

**Laatste update**: 6 juni 2024

Deze opmerkingen hebben betrekking op de releaseperiode van 15 mei 2024 tot en met juni 2024. Adobe Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **AI Assistant voor Customer Journey Analytics** | Staat u toe om natuurlijk-taalvragen in de UI van de Customer Journey Analytics te stellen en antwoorden te krijgen die op de documentatie van de Customer Journey Analytics worden gebaseerd. [Meer informatie](/help/ai-assistant.md) | | vrijdag 6 juni 2024 |
| **Transformatie van B2B-opzoekgegevenssets** | U kunt nu [B2B-opzoekgegevenssets transformeren](/help/connections/transform-datasets-b2b-lookups.md) bij het definiëren van een verbinding. Deze transformatie staat toe om op persoon-gebaseerde raadplegingen op B2B gegevens te steunen. | | vrijdag 6 juni 2024 |
| **BI Extension** | De uitbreiding van BI laat SQL toegang tot de gegevensmeningen toe die u in Customer Journey Analytics hebt bepaald. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/bi-extension) | | donderdag 15 mei 2024 |
| **Soorten publiek wordt gepubliceerd naar een nieuwe sectie &quot;Soorten publiek&quot; in Experience Platform** | Soorten publiek die vanuit de Customer Journey Analytics worden gepubliceerd, zijn nu beschikbaar in de nieuwe sectie &quot;Soorten publiek&quot; in Adobe Experience Platform.<p>Eerder waren publiek dat vanuit Customer Journey Analytics werd gepubliceerd, beschikbaar in Experience Platform onder de sectie &quot;Segmenten&quot;.</p><p>Deze verbetering biedt de volgende voordelen:</p><ul><li>Het publiek heeft niet langer een vertraging van 1 uur voordat het in het Experience Platform wordt weergegeven; het zijn pas seconden nadat het is gepubliceerd.</li><li>De soorten publiek kunnen in Experience Platform worden gesorteerd door de kolom &quot;Oorsprong&quot;te gebruiken, die de toepassing toont waarvan het publiek oorspronkelijk werd gepubliceerd.</li><li>Met de filter- en sorteeropties in het Experience Platform kunt u sneller het desbetreffende publiek vinden.</li></ul> <p>(Bijgewerkte documentatiekoppeling die moet worden gevolgd)</p> |  | Eind mei tot begin juni 2024 |
| **Streaming media: Webgegevens naar Adobe Experience Platform Edge Network verzenden met de Web SDK** | U kunt de SDK van het Web van Adobe Experience Platform nu gebruiken om het stromen de Webgegevens van Media naar de Edge Network van Adobe Experience Platform te verzenden, die u toestaat om meer gepersonaliseerde campagnes te bouwen en meer gepersonaliseerde inhoud te verstrekken, resulterend in meer het volgen gegevens om over te melden.<p>Deze verbetering verstrekt een verenigde inzamelingsmethode voor Webimplementaties over alle oplossingen van het Platform, zoals Customer Journey Analytics, rt-CDP, AJO, en Gebeurtenis door:sturen. Eerder was de enige manier om webgegevens van Streaming media naar Edge Network te verzenden met de Media Edge API. <p>[Meer informatie](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/edge-web-sdk)</p> | | donderdag 29 mei 2024 |
| **Afgeleide Gebieden - Nieuwe Functies en de Malplaatjes van de Functie** | Aanvullende afgeleide veldfuncties ([Math](/help/data-views/derived-fields/derived-fields.md#math), [Volgende of Vorige](/help/data-views/derived-fields/derived-fields.md#next-or-previous)) en [functiesjablonen](/help/data-views/derived-fields/derived-fields.md#function-templates). | | donderdag 5 juni 2024 |
| **Accounts en locaties delen die worden gebruikt voor exporteren en importeren** | Gebruikers kunnen de accounts en locaties die ze maken nu beschikbaar maken voor alle gebruikers in hun organisatie. Alleen account- en locatie-eigenaars en systeembeheerders kunnen accounts en locaties bewerken en verwijderen.<p>Eerder konden accounts en locaties alleen worden gebruikt door de gebruiker die ze heeft gemaakt.</p><p>Deze instellingen zijn beschikbaar wanneer gebruikers cloudexportaccounts configureren en exportlocaties voor de cloud configureren.</p> <p>Zie voor meer informatie [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md) en [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md).</p> | donderdag 12 juni 2024 | maandag 30 juni 2024 |
| **Nieuwe documentatie voor upgrade van Adobe Analytics naar Customer Journey Analytics** | Voor organisaties die van Adobe Analytics aan Customer Journey Analytics bevorderen, zijn er veelvoudige verbeteringsopties en vele overwegingen om in mening te houden gebaseerd op de huidige implementatie van Adobe Analytics van een organisatie en langetermijndoelstellingen. De nieuwe documentatiebronnen zijn nu beschikbaar om u te helpen beter begrijpen:<ul><li>De verschillende upgradepaden die bestaan</li><li>Welke verbeteringspaden beschikbaar zijn op basis van de huidige Adobe Analytics-implementatie van een organisatie</li><li>De voor- en nadelen van elk upgradepad</li><li>Stapsgewijze begeleiding voor elk verbeteringspad</li><li>Overwegingen bij de verwerking van historische gegevens</li></ul>[Aan de slag met de upgrade naar Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-getstarted) | | Nu beschikbaar |
| **Nieuwe documentatie over gevallen waarin gegevens worden geëxporteerd** | In deze nieuwe sectie wordt een overzicht gegeven [Gebruiksscenario&#39;s voor exporteren van gegevens](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-usecases/data-export/overview) zoals<ul><li>Gegevensback-up</li><li>Gegevensvalidatie</li><li>Data Lake, Data Warehouse of BI Tools</li><li>Gereedheid voor AI/ML</li></ul> en hoe deze te implementeren met behulp van Experience Platform- en Customer Journey Analytics-functies. | | Nu beschikbaar |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-342309; AN-342312; AN-345267; AN-345909; AN-346016; AN-346049; AN-346052; AN 346287; AN-346624; AN-347919

## Belangrijke kennisgevingen voor beheerders van Customers Journey Analytics

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | | |

{style="table-layout:auto"}

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release van Customer Journey Analytics voor 2024](/help/release-notes/2024.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Opmerkingen bij de release van Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)
* [Documentatieupdates Customer Journey Analytics](/help/release-notes/doc-changes.md)
