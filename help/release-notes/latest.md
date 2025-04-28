---
title: Opmerkingen bij de release van Customer Journey Analytics
description: Aanvullende informatie voor de nieuwste versie van Customer Journey Analytics weergeven
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 4e65e2fd1720b63b9dec341d4a67f7356df77fcb
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 3%

---

# Huidige Adobe Customer Journey Analytics-releaseopmerkingen (april 2025)

**Laatste update**: 28 april 2025

Deze opmerkingen hebben betrekking op de releaseperiode van 27 maart tot 15 mei 2025. De versies van Adobe Customer Journey Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Updates aan de lijnpunt van de &quot;Geen Waarde&quot;op numerieke afmetingen** | Voor numerieke afmetingen kunt u met deze update<ul><li>Gebruik de dimensie-item Geen waarde in een segment.</li><li>Voer een uitsplitsing uit in een rapport over de post &quot;Geen waarde&quot;.</li></ul> [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/no-value-options#numeric) | vrijdag 27 maart 2025 |
| **Adobe Content Analytics** | Met Adobe Content Analytics kunt u snel en eenvoudig grote hoeveelheden inhoudsgegevens onderzoeken om trends, anomalieën in steunkleuren, vermoeidheid van inhoud en inzicht in de blootstelling aan inhoud te ontdekken.<p>U kunt tijd besparen met vooraf gebouwde rapportagesjablonen en nieuwe functies, zoals Asset Inspector. Met deze functie kunt u het middel niet alleen visualiseren in overeenstemming met uw gegevens, maar ook elk middel openen voor samengevatte details, zoals prestaties, plaatsingen, kenmerken en meer.<p>U kunt deze nieuwe reeks inhoudsgegevens binnen de context van de volledige klantenreis onderzoeken om belangrijke bedrijfsvragen te beantwoorden, inhoudsprestaties te beoordelen, segmentatie te verbeteren, optimalisatiemogelijkheden te identificeren, en nieuw publiek voor activering te bepalen.<p>Content Analytics is een add-on bij Customer Journey Analytics. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/content-analytics) |  | vrijdag 27 maart 2025 |
| **de Inzameling van Media: De Verbindingsupdates van Adobe Source voor nieuwe Media die XDM** melden | De Analytics Source Connector wijst streaming mediagegevens in Adobe Analytics automatisch toe aan dezelfde velden die door de Web SDK worden gebruikt. Eerder werden gegevens zowel aan de oude als aan de nieuwe locatie toegewezen, maar in de toekomst wordt alleen de nieuwe locatie gebruikt. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/xdm-var-mapping) |  | dinsdag 31 maart 2025 |
| **Bijgewerkte gebieden XDM voor het verzamelen van het stromen gegevens van Media in Adobe Experience Platform** | Wanneer het verzamelen van de Gegevens van Media van de Streaming in Adobe Experience Platform, zouden de XDM gebiedspaden onder de rubriek van &quot;Pad van het Gebied XDM&quot;van de Streaming de parameterdocumentatie van Media niet meer moeten worden gebruikt. Deze gebiedspaden worden gevonden op de volgende pagina&#39;s en als &quot;Vervangen&quot;duidelijk: [ Audio en videoparameters ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters), [ Advertentieparameters ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/ad-parameters), [ de parameters van het Hoofdstuk ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/chapter-parameters), [ de staatsparameters van de Speler ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/player-state-parameters), en [ de parameters van de Kwaliteit ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/quality-parameters). <p>In plaats daarvan moeten klanten migreren naar de `mediaReporting` -veldpaden, zoals wordt weergegeven onder de kop &quot;XDM Field Path&quot; (XDM-veldpad rapporteren) van de documentatie voor Streaming Media waarnaar hierboven wordt verwezen.<p>Tijdens een overgangsperiode van drie maanden, zal gegevensinname op de afgekeurde XDM gebiedspaden voortzetten. Eind juli 2025 worden afgekeurde veldpaden echter volledig verwijderd en niet meer zichtbaar in de gebruikersinterface van het Adobe Experience Platform-schema. De gegevens worden alleen verzonden met behulp van de `mediaReporting` -veldpaden.<p>Klanten die vóór 22 april 2025 de gegevensbronaansluiting voor Analytics hebben geïmplementeerd om streaming Media-gegevens te verzamelen in Platform, moeten hun bestaande configuraties migreren om de nieuwe veldpaden te gebruiken. Deze migratie moet eind juli 2025 zijn voltooid. Neem contact op met uw Adobe Consulting Services of accountteam voor ondersteuning van migratie. Er is geen actie vereist voor klanten die de bronconnector voor Analytics na 22 april 2025 implementeren.</p> |  | woensdag 22 april 2025 |
| **de verandering van de Terminologie: &quot;Filters&quot;in &quot;Segmenten&quot;** | Eerder verwees Adobe Customer Journey Analytics naar segmenten als &quot;filters&quot;. Deze terminologie is nu in overeenstemming gebracht met Adobe Analytics. &quot;Filters&quot; worden nu &quot;segmenten&quot; genoemd. (Doorzoekfilters worden natuurlijk nog steeds &#39;filters&#39; genoemd.) De interface en documentatie zijn bijgewerkt. | | donderdag 16 april 2025 |
| **Stitching: Haal blijvende en voorbijgaande IDs van XDM IdentityMap** op | Deze functie biedt ondersteuning voor het gebruik van identiteiten die zijn opgeslagen in de XDM identityMap in het koppelingsproces. De identityMap kan worden gebruikt voor de permanente of tijdelijke id voor op het veld gebaseerde stitching en kan worden gebruikt voor de permanente id voor op grafiek gebaseerde stitching.  U kunt een specifieke naamruimte of een primaire identiteit uit de identityMap gebruiken. Leer meer [ hier ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/stitching/fbs#identitymap) en [ ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/stitching/gbs#identitymap) |  | dinsdag 28 april 2025 |
| **Gedeelde metriek en dimensies over gegevensmeningen** | Hiermee kunt u dimensie- en metrische instellingen toepassen op meerdere gegevensweergaven. Wijzigingen in een gedeelde dimensie of metrische waarde zijn van toepassing op alle instanties van die dimensie of metrisch in alle toepasselijke gegevensweergaven. Met deze interface kunnen Customer Journey Analytics-beheerders componenten gemakkelijker beheren wanneer er veel gegevensweergaven worden gebruikt. [Meer informatie](/help/data-views/shared-metrics-dimensions/smd-overview.md) |  | donderdag 30 april 2025 |


## Oplossingen in Customer Journey Analytics

**Admin Console**: AN-370228
**Analysis Workspace**: AN-371933; AN-371933; AN-371979
**Soorten publiek**: AN-373032
**montages van de Component**: AN-367400
**Voortgekomen gebieden**: AN-370614; AN-370959
**de plaatsen van de Uitvoer**: AN-371670
**Volledige lijstuitvoer**: AN-360492; AN-369204; AN-370755;AN-372294; AN-372363; AN-372754; 373040; AN-373081; AN-373168
**Canvas van de Reis**: AN-373294
**Mobiele app**: AN-363169; AN-368496; AN-371766
**het gebruik van het Product**: AN-369501
**het Melden**: AN-369085; AN-371094; AN-372580


## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | | |

## Gerelateerde bronnen

* [Opmerkingen bij de vorige Customer Journey Analytics-release voor 2025](/help/release-notes/2025.md)
* [ de versienota&#39;s van Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [ de versienota&#39;s van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
