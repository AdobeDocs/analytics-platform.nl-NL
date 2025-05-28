---
title: Opmerkingen bij de release van Customer Journey Analytics
description: Aanvullende informatie voor de nieuwste versie van Customer Journey Analytics weergeven
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: df8a10c674ed64d0341209fbe0a700a5c94b3b75
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 4%

---

# Huidige Adobe Customer Journey Analytics-releaseopmerkingen (mei 2025)

**Laatste update**: 22 mei 2025


Deze opmerkingen hebben betrekking op de releaseperiode van 22 april tot 18 juni 2025. De versies van Adobe Customer Journey Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Bijgewerkte gebieden XDM voor het verzamelen van het stromen gegevens van Media in Adobe Experience Platform** | Wanneer het verzamelen van de Gegevens van Media van de Streaming in Adobe Experience Platform, zouden de XDM gebiedspaden onder de rubriek van &quot;Pad van het Gebied XDM&quot;van de Streaming de parameterdocumentatie van Media niet meer moeten worden gebruikt. Deze gebiedspaden worden gevonden op de volgende pagina&#39;s en als &quot;Vervangen&quot;duidelijk: [ Audio en videoparameters ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters), [ Advertentieparameters ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/ad-parameters), [ de parameters van het Hoofdstuk ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/chapter-parameters), [ de staatsparameters van de Speler ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/player-state-parameters), en [ de parameters van de Kwaliteit ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/quality-parameters). <p>In plaats daarvan moeten klanten migreren naar de `mediaReporting` -veldpaden, zoals wordt weergegeven onder de kop &quot;XDM Field Path&quot; (XDM-veldpad rapporteren) van de documentatie voor Streaming Media waarnaar hierboven wordt verwezen.<p>Tijdens een overgangsperiode van drie maanden, zal gegevensinname op de afgekeurde XDM gebiedspaden voortzetten. Eind juli 2025 worden afgekeurde veldpaden echter volledig verwijderd en niet meer zichtbaar in de gebruikersinterface van het Adobe Experience Platform-schema. De gegevens worden alleen verzonden met behulp van de `mediaReporting` -veldpaden.<p>Klanten die vóór 22 april 2025 de gegevensbronaansluiting voor Analytics hebben geïmplementeerd om streaming Media-gegevens te verzamelen in Platform, moeten hun bestaande configuraties migreren om de nieuwe veldpaden te gebruiken. Deze migratie moet eind juli 2025 zijn voltooid. Neem contact op met uw Adobe Consulting Services of accountteam voor ondersteuning van migratie. Er is geen actie vereist voor klanten die de bronconnector voor Analytics na 22 april 2025 implementeren.</p> |  | woensdag 22 april 2025 |
| **Stitching: Haal blijvende en voorbijgaande IDs van XDM IdentityMap** op | Deze functie biedt ondersteuning voor het gebruik van identiteiten die zijn opgeslagen in de XDM identityMap in het koppelingsproces. De identityMap kan worden gebruikt voor de permanente of tijdelijke id voor op het veld gebaseerde stitching en kan worden gebruikt voor de permanente id voor op grafiek gebaseerde stitching.  U kunt een specifieke naamruimte of een primaire identiteit uit de identityMap gebruiken. Leer meer [ hier ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/stitching/fbs#identitymap) en [ ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/stitching/gbs#identitymap) |  | dinsdag 28 april 2025 |
| **Gedeelde metriek en dimensies over gegevensmeningen** | Hiermee kunt u dimensie- en metrische instellingen toepassen op meerdere gegevensweergaven. Wijzigingen in een gedeelde dimensie of metrische waarde zijn van toepassing op alle instanties van die dimensie of metrisch in alle toepasselijke gegevensweergaven. Met deze interface kunnen Customer Journey Analytics-beheerders componenten gemakkelijker beheren wanneer er veel gegevensweergaven worden gebruikt. [Meer informatie](/help/data-views/shared-metrics-dimensions/smd-overview.md) |  | donderdag 30 april 2025 |
| **Verhoging in volledige lijst de uitvoergrenzen van de lijst** | Adobe verhoogde het aantal kolommen u met [ volledige lijstuitvoer ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/export/export-cloud#comparison-of-full-table-export-in-customer-journey-analytics-to-data-warehouse-in-adobe-analytics) van 5 dimensies en 5 metriek aan 10 dimensies en 10 metriek kunt gebruiken. Dit geldt voor alle Customer Journey Analytics-lagen. De rechten voor het aantal rijen dat kan worden geëxporteerd, worden niet gewijzigd. |  | donderdag 30 april 2025 |
| **dimensie van de Diepte van de Gebeurtenis** | Een nieuwe [ dimensie van de Diepte van de Gebeurtenis ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-reference#required-standard-components) werd toegevoegd aan de lijst van vereiste standaardcomponenten voor een gegevensmening. |  | vrijdag 8 mei 2025 |
| **maak het manifestdossier onbruikbaar wanneer het uitvoeren van volledige lijsten** | Hiermee kunt u het manifestbestand uitschakelen dat standaard wordt opgenomen wanneer u volledige tabellen exporteert vanuit Analysis Workspace. [Meer informatie](/help/analysis-workspace/export/export-cloud.md) |  | woensdag 20 mei 2025 |
| **Agent van Gegevens Inzichten** | De Agent van Gegevens, deel van de Medewerker AI in Customer Journey Analytics, is een generatieve AI gespreksagent. Componenten uit uw gegevensweergave en uw feitelijke gegevens worden gebruikt om gegevensgerichte vragen snel en efficiënt te beantwoorden door relevante visualisaties te maken in Analysis Workspace. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) |  | donderdag 28 mei 2025 |
| **Dimension formaatgebreken aan 2 voor het Dubbele type afmetingen** | Voor schema&#39;s met Dubbele gegevenstypen, blijft het formaat van de afmeting nu aan 2 decimalen in gebreke. U kunt dit getal wijzigen in 0 tot en met 5 decimalen.<p>Eerder werd de notatie standaard ingesteld op 0 decimalen.</p><p>Dit betekent dat als u afmetingen van twee typen gebruikt in uw Analysis Workspace-rapporten, er standaard geen decimalen worden weergegeven. Dezelfde rapporten bevatten nu twee decimalen.</p><p>Voor meer informatie over hoe te om het aantal decimalen bij te werken die voor dubbel-type dimensies worden getoond, zie {de componentenmontages van 0} Formaat ](/help/data-views/component-settings/format.md).[</p> | | vrijdag 29 mei 2025 |
| **verlaten paneel van Analysis Workspace opent niet meer en sluit op aanwijzen** | Het linkerdeelvenster in Analysis Workspace wordt gebruikt om onderdelen, deelvensters en visualisaties aan uw project toe te voegen. De optie om het linkerdeelvenster tijdelijk te openen door de muisaanwijzer op een van de pictogrammen aan de linkerkant te plaatsen, is niet meer beschikbaar. Klik in plaats daarvan gewoon op een van deze pictogrammen om het deelvenster open te houden en klik vervolgens op hetzelfde pictogram om het te sluiten. |  | dinsdag 2 juni 2025 <p>(Oorspronkelijk gepland voor vrijgave op 29 mei 2025)</p> |
| **Customer Journey Analytics B2B edition** | Customer Journey Analytics B2B edition helpt B2B-bedrijven hun marketing-, verkoop- en productteams op elkaar af te stemmen door inzichten van actioneerbare accounts te bieden die de inkomstengroei stimuleren. Met de rekening die bij het centrum van het gegevensmodel wordt geplaatst, richt alle analyse zich op de rekeningsreis. Als u een nieuwe laag entiteiten (accounts, mogelijkheden en inkoopgroepen) toevoegt boven op gebeurtenissen op basis van tijd en persoonlijke gebeurtenissen, krijgt u een volledig beeld van de B2B-marketing- en inkomstenlevenscyclus. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition) |  | donderdag 18 juni 2025 |
| **voeg en meningscommentaren in de projecten van Analysis Workspace toe** | Een nieuwe [ het becommentariëren eigenschap ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/comment-projects) in Analysis Workspace staat u toe om inzichten te delen en vragen binnen de context van een project van Analysis Workspace te stellen. Hierdoor kunnen discussies over de gegevens worden gestroomlijnd, waarbij gesprekken worden gevoerd binnen de context van de gegevens die worden besproken. U kunt <ul><li>Opmerkingen maken over elk Analysis Workspace-project waartoe u toegang hebt</li><li>Opmerkingen maken over een specifiek punt in een visualisatie of algemene opmerkingen maken over een project</li><li>Andere gebruikers een label geven voor hun opmerkingen</li><li>Bestaande opmerkingen beheren (bewerken, vastzetten, oplossen, enzovoort)</li></ul>De beheerders van Customer Journey Analytics kunnen [ commentaren op het organisatieniveau ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/user-preferences#ims-organization-preferences) onbruikbaar maken. De eigenaars van het project kunnen [ commentaren op het projectniveau ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) onbruikbaar maken. |  | donderdag 25 juni 2025 <p>(Oorspronkelijk gepland voor vrijgave op 29 mei 2025)</p> |

## Oplossingen in Customer Journey Analytics

**Analysis Workspace**: AN-361874; AN-371360; AN-373079; AN-374382; AN-37447; AN-375277; AN-375 680
**Soorten publiek**: AN-372343
**Logboek van de Controle**: AN-378168
**Verbindingen**: AN-373121; AN-372996
**schrapping van Gegevens**: AN-375450
**Afgeleide gebieden**: AN-373689; AN-377852
**de plaatsen van de Uitvoer**: AN-374167
**Canvas van de Reis**: AN-373319
**Report Builder**: AN-369786
**het Melden**: AN-377326; AN-378051
**die activiteitenmanager** melden: AN-377148


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
