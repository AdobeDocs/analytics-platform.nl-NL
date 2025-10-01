---
title: Opmerkingen bij de release van Customer Journey Analytics
description: Aanvullende informatie voor de nieuwste versie van Customer Journey Analytics weergeven
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 8359e9da7e4bdbd450e23dacb7eee03328412aeb
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 2%

---

# Huidige Customer Journey Analytics-releaseopmerkingen (september 2025)

**Laatste update**: 23 september 2025


Deze releaseopmerkingen betreffen de releaseperiode van september tot begin oktober 2025. De versies van Adobe Customer Journey Analytics werken op a [&#x200B; ononderbroken leveringsmodel &#x200B;](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [&#x200B; Het begin van de Uitvoer &#x200B;](releases.md) | [&#x200B; Algemene Beschikbaarheid &#x200B;](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Updates aan de interface van het Gebruik** | De [&#x200B; interface van het Gebruik &#x200B;](/help/connections/manage-connections.md#usage) voegt nu informatie over kerngegevensvolume en gemiddelde rijgrootte toe.<p>Voor meer informatie, zie [&#x200B; verbindingen &#x200B;](/help/connections/manage-connections.md#usage) beheren.</p> | | vrijdag 4 september 2025 |
| **Verbeteringen wanneer het migreren van projecten en componenten aan Customer Journey Analytics** | De volgende verbeteringen zijn nu beschikbaar bij het migreren van projecten en onderdelen van Adobe Analytics naar Customer Journey Analytics:<ul><li>Migreer meerdere projecten tegelijk.<br/> u kunt tot 20 projecten tegelijkertijd migreren.<br/> eerder, kon u slechts één project tegelijkertijd migreren.</li><li>Update-toewijzingen voor dimensies en metriek die al zijn toegewezen aan een vorige projectmigratie.<br/> u kunt deze afbeeldingen nu bijwerken telkens als u een project migreert, zelfs als de zelfde afmetingen en metriek eerder met een vroegere migratie in kaart werden gebracht.<br/> eerder, waren om het even welke afbeeldingen u koos permanent voor alle toekomstige projectmigraties.</li><li>Verbeterde prestaties voor organisaties met een groot aantal projecten.</li></ul><p>Deze functie is beschikbaar via de Adobe Analytics-interface. Voor meer informatie, zie [&#x200B; componenten en projecten van Adobe Analytics aan Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/component-migration/component-migration) migreren.</p> | dinsdag 15 september 2025 | vrijdag 18 september 2025 |
| **de toetsengrens van de Raadpleging steeg tot 1 miljard** | Het maximumaantal unieke sleutels voor een raadplegingsdataset is nu tot 1 miljard, afhankelijk van uw Customer Journey Analytics recht. <p>Eerder was het maximumaantal 10 miljoen voor alle toeslagrechten.<p>Voor meer informatie, zie [&#x200B; Guardrails &#x200B;](/help/technotes/guardrails.md).</p> | | vrijdag 25 september 2025 |
| **Steun voor ad hoc en op model-gebaseerde schema&#39;s** | [&#x200B; Ad hoc &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/tutorials/ad-hoc) en op model-gebaseerde schema&#39;s worden gebruikt in gegeven en gegevens weerspiegelen werkschema&#39;s voor Experience Platform. |  | 23 september 2025 (oorspronkelijk gepland voor vrijgave op 28 augustus 2025) |
| **Echt - tijd rapporterend** | Real-time rapportage in Customer Journey Analytics geeft gegevens en visualisaties in een of meer deelvensters in Analysis Workspace in real-time weer en werkt deze bij.<br/><br/> (Koppeling met documentatie voor opvolgen.) | 18 september 2025 (oorspronkelijk gepland voor vrijgave op 15 augustus 2025) | donderdag 8 oktober 2025 |
| **Steun voor gegevensspiegel** | Met steun voor model-gebaseerde schema&#39;s en de functionaliteit van de vangst van veranderingsgegevens (CDC) voor specifieke bronschakelaars in Experience Platform, zal Customer Journey Analytics de functionaliteit van de gegevenspiegel van oplossingen zoals [!DNL Snowflake], [!DNL Azure Databrick] kunnen steunen, en [!DNL Google BigQuery].<p>Neem contact op met uw Adobe-accountteam voor toegang tot de bètaversie.</p><p>(Koppeling met documentatie die moet worden gevolgd.)</p> | Beta release, vanaf 24 september 2025 | TBD |
| **Streaming Media: Bijgewerkte gebieden XDM voor het verzamelen van het stromen gegevens van Media in Adobe Experience Platform** | Wanneer het verzamelen van de Gegevens van Media van de Streaming in Adobe Experience Platform, zouden de XDM gebiedspaden onder de rubriek van &quot;Pad van het Gebied XDM&quot;van de Streaming de parameterdocumentatie van Media niet meer moeten worden gebruikt. In plaats daarvan, moeten de klanten die de analytische bronschakelaar uitvoerden om het stromen gegevens van Media in Platform vóór 9 Mei te verzamelen, 2025 hun bestaande configuraties aan mediaReporting gebiedspaden, zoals aangetoond onder de rubriek &quot;het Weg van het Gebied van XDM&quot;van de documentatie van de parameters van Media het Streamen.<p> Deze gebiedspaden worden gevonden op de volgende pagina&#39;s en als &quot;Vervangen&quot;duidelijk: [&#x200B; Audio en videoparameters &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/audio-video-parameters), [&#x200B; Advertentieparameters &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/ad-parameters), [&#x200B; de parameters van het Hoofdstuk &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/chapter-parameters), [&#x200B; de staatsparameters van de Speler &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/player-state-parameters), en [&#x200B; de parameters van de Kwaliteit &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/quality-parameters). (Geen actie wordt vereist voor klanten die de bron van Analytics schakelaar na 9 Mei, 2025 uitvoeren, en reeds mediaReporting XDM wegen gebruiken.)</p><p>Gegevensinvoer op de afgekeurde XDM-veldpaden gaat door tot eind oktober 2025. Na die tijd, zullen de afgekeurde gebiedspaden volledig worden verwijderd en niet meer zichtbaar in het Schema UI van Adobe Experience Platform, en de gegevens zullen worden verzonden slechts gebruikend mediaReporting gebiedspaden.</p><p>Voor meer informatie, zie [&#x200B; migreren een implementatie van de Verbinding van Analytics Source aan bijgewerkte XDM Streaming Media &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/media-use-cases/xdm-updates/updated-xdm-fields).</p><p>Neem contact op met uw Adobe Consulting Services of accountteam voor ondersteuning van migratie. </p> |  | Oktober 2025 |
| **Stitching in verbindingen** | Vereenvoudigt het stitching van Customer Journey Analytics. In plaats van een dataset te dupliceren en het verbinden op de gedupliceerde dataset toe te passen, wordt nu het stitching gedaan op de opname van gegevens in Customer Journey Analytics, die het vereiste van gedupliceerde datasets en schema&#39;s schrapt. <p>Bovendien in plaats van het moeten het stitching door klantensteun vragen, kunt u het stitching nu van een bijgewerkte UI van Verbindingen in werking stellen.</p><p> *de eerder meegedeelde versiedata worden geduwd toe te schrijven aan extra vereiste inspanningen. De nieuwe releasedata overlappen zich met het vakantieseizoen, dat extra vrijgavebeperkingen introduceert. Een gefaseerde uitrol wordt nu gepland om stabiliteit te verzekeren en verstoring tijdens de vakantieperiode te minimaliseren.*</p> <p>(Koppeling met documentatie die moet worden gevolgd.)</p> | Eind oktober 2025 | Eind januari 2026 |

## Oplossingen in Customer Journey Analytics

**Analysis Workspace**: AN-391719, AN-380838, AN-389402, AN-389373, AN-390851, AN-391593, AN-391 404 AN-393064 AN-379337
**Componenten**: AN-393810
**Content Analytics**:
**Geleide Analyse**:
**Platform**:
**Report Builder**: AN-387741, AN-386777, AN-388720, AN-389343
**het Melden**: AN-391439, AN-391228, AN-393620, AN-393640, AN-391334, AN-39304
**Segmentatie**:
**Geplande rapporten**: AN-391150, AN-390474
**Gedeelde metriek en dimensies**:
**Andere**: AN-387858


## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | | |

## Gerelateerde bronnen

* [Opmerkingen bij de vorige Customer Journey Analytics-release voor 2025](/help/release-notes/2025.md)
* [&#x200B; de versienota&#39;s van Adobe Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=nl-NL)
* [&#x200B; het stromen de versienota&#39;s van de Inzameling van Media &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=nl-NL)
* [&#x200B; de versienota&#39;s van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
