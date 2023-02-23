---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste CJA-release
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 4e41bda273f0f7e93941bb00b55bffc6b357ac1f
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 6%

---

# Opmerkingen bij de release Current Customer Journey Analytics (CJA) (februari 2023)

**Laatste update**: 23 februari 2023

Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Belangrijke functies en updates

| Functie | Beschrijving | [Begin van rollout](/help/release-notes/releases.md) | [Algemene beschikbaarheid](/help/release-notes/releases.md) |
| ----------- | ---------- | ----- | --- |
| **Bijwerken naar publiek CJA** | Nadat u een publiek hebt gecreeerd, leidt Adobe tot een Experience Platform het stromen segment voor elk nieuw publiek CJA. Er wordt alleen een streaming segment gemaakt als uw organisatie is ingesteld op streamingsegmentatie. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/audiences/publish.html#after-audience-created) | N.v.t. | 3 februari 2023 |
| **Vergelijk datumbereiken in Mobile Scorecards verbergen** | Met Mobile Scorecards kunt u nu vergelijkingsdatumbereiken verbergen. | N.v.t. | 8 februari 2023 |
| **Agenda-updates in werkruimte** | <ul><li>Datums deelvenster Anker: U kunt de componenten van het datumbereik relatief maken ten opzichte van de deelvensterkalender. [Meer informatie](/help/components/date-ranges/calendar.md)</li><li>Updates voor kalenderstijlen: De kalenderstijlen door UI zijn bevorderd om een consistentere en gebruiksvriendelijker werkschema voor te stellen.</li><li>Updates van de kalenderformule: Als u relatieve datums gebruikt, wordt in alle kalenderformules het begin van het datumbereik van het deelvenster weergegeven. [Meer informatie](/help/components/date-ranges/calendar.md)</li></ul> | N.v.t. | 8 februari 2023 |
| **Updates voor het datumbereik van deelvensters** | In Workspace zijn de volgende verbeteringen aangebracht:<ul><li>Vanaf de release van februari worden voorvertoningen van componenten en gegevens gebaseerd op het datumbereik van het deelvenster en niet op de laatste 90 dagen. </li><li>Alle componenten die in de linkerspoorstaaf worden vermeld zullen beschikbaar zijn gebaseerd op de waaier van de paneeldatum.</li><li>Alle datumvoorvertoningen in het segment en de berekende metrische builders worden gebaseerd op het bereik van de deelvensterdatum (tenzij ze worden benaderd door de componentmanagers, die geen bijbehorend deelvenster hebben, zijn ze nog steeds gebaseerd op de laatste 90 dagen).</li><li>In alle voorvertoningen van gegevens worden gegevens of componenten weergegeven op basis van het datumbereik van het deelvenster.</li></ul> | N.v.t. | 8 februari 2023 |
| **Rij-/kolomfiltering voor streaming Adobe Analytics Source Connector** | Met de Bronverbinding Analytics in Adobe Experience Platform kunt u nu analysegegevens filteren die worden gebruikt om profielen te vullen in [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en).<p>Filteren op rijniveau helpt het aantal gebeurtenissen dat aan profielen is gekoppeld, te verminderen. Filteren op kolomniveau helpt de rijkheid van de gebeurtenissen zelf te verminderen, zodat u het gebruik van profielrechten kunt optimaliseren. Deze filtering is alleen van toepassing op gegevens die naar het realtime-klantprofiel worden verzonden en [Identiteitsservice](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=en).<p>**Filteren heeft geen invloed op de gegevens die naar het Data Lake worden verzonden voor gebruik in toepassingen zoals Customer Journey Analytics**. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en#filtering-for-profile) | N.v.t. | Gewijzigd tot 29 maart 2023 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Customer Journey Analytics

AN-309106

## Belangrijke kennisgevingen voor CJA-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| Geen huidige aankondigingen | N.v.t. | N.v.t. |

{style=&quot;table-layout:auto&quot;}

## Gerelateerde bronnen

* [Opmerkingen bij de vorige CJA-release voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
