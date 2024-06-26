---
title: De opmerkingen bij de huidige release van de Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste release Customer Journey Analytics
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 1534b628841a5b4588379b944822073f3288d710
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 2%

---

# Opmerkingen bij de huidige Adobe Customer Journey Analytics-release (juni 2024)

**Laatste update**: 18 juni 2024

Deze opmerkingen hebben betrekking op de releaseperiode van 6 juni 2024 tot en met juli 2024. Adobe Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **AI Assistant voor Customer Journey Analytics** | Staat u toe om natuurlijk-taalvragen in de UI van de Customer Journey Analytics te stellen en antwoorden te krijgen die op de documentatie van de Customer Journey Analytics worden gebaseerd. [Meer informatie](/help/ai-assistant.md) | | vrijdag 6 juni 2024 |
| **Op grafiek gebaseerde stitching** | Door op grafiek-gebaseerde het stitching, kunt u de identiteitsgrafiek van de Dienst van de Identiteit van het Experience Platform gebruiken om een betere mening van de klantenreis te krijgen door:<ul><li>Gegevenssets samenvoegen met verschillende id&#39;s zonder dat er aanvullende gegevens moeten worden opgehaald, getransformeerd en geladen om één id te weerspiegelen.</li><li>Het verbeteren van dekking van aangewezen of gouden identiteit voor één enkele dataset door identiteiten over datasets te delen.</li><li>Profielen die in Real-time Customer Data Platform en Journey Optimizer zijn gemaakt, worden uitgelijnd op personen in Customer Journey Analytics.</li></ul>[Meer informatie](/help/stitching/overview.md) |  | zaterdag 28 juni 2024 |
| **B2B-schematransformatie voor rekening van persoon** | Om op persoon-gebaseerde raadplegingen op B2B- gegevens (met inbegrip van rekeningen, kansen, marketing lijsten en campagnes) te steunen, kunt u B2B raadplegingsdatasets omzetten. Deze transformatie is beschikbaar slechts voor datasets met gegevens voor B2B raadplegingsschema&#39;s, die op de volgende klassen worden gebaseerd:<ul><li>XDM Zakelijke account Person Relatie</li><li>XDM Business Opportunity Person Relatie</li><li>Leden van XDM Business Marketing List</li><li>XDM Business Campaign-leden</li></ul>[Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/transform-datasets-b2b-lookups) |  | donderdag 5 juni 2024 |
| **Afgeleide velden - wiskundige functie** | Hiermee kunt u eenvoudige wiskundige operatoren uitvoeren in gegevensweergaven om vragen over uw gebruikers te beantwoorden. U kunt bijvoorbeeld producten, garanties en verzendkosten combineren. [Meer informatie](/help/data-views/derived-fields/derived-fields.md#math)</p> | | donderdag 5 juni 2024 |
| **Afgeleide velden - volgende of vorige functie** | Hiermee kunt u bekijken wat de volgende of vorige waarde is. Bijvoorbeeld, wat waren de vorige marketing kanalen iemand met voorafgaand aan het geselecteerde marketing kanaal in wisselwerking stond? Of, wat hadden de paginagebruikers met vóór of na de geselecteerde pagina interactie? Wat is de populairste kanaalgebruikers met alvorens in-store te gaan in wisselwerking? [Meer informatie](/help/data-views/derived-fields/derived-fields.md#next-or-previous)</p> | | donderdag 12 juni 2024 |
| **Afgeleide velden - functie Samenvatten** | Verstrekt de capaciteit om samenvoeging-type functies op metriek of dimensies op gebeurtenis, zitting, en gebruikersniveaus toe te passen. [Meer informatie](/help/data-views/derived-fields/derived-fields.md#summarize) | | donderdag 26 juni 2024 |
| **Afgeleide velden - deduplicatiefunctie** | Hiermee voorkomt u dat een waarde herhaaldelijk wordt geteld. Kan worden toegepast op gebruiker- of sessieniveau of op basis van de unieke waarde van een dimensie. (Koppeling naar documentatie) |  | donderdag 10 juli 2024 |
| **Ingestieprioritisering en latentie** | U kunt uw gebeurtenisgegevens nu binnen 90 minuten in Customer Journey Analytics opnemen, ongeacht of de gegevens 24 uur, 48 uur of 7 dagen oud zijn. Merk op dat dit vermogen op het SKU-pakket verschilt uw bedrijf kocht:<ul><li>CJA Priority Ingestie Basic: 24-uurs oude gegevens binnen SLT-verwerking van 90 minuten (beschikbaar voor CJA Foundation en CJA Select)</li><li>CJA Priority Ingestie Intermediate: gegevens van 72 uur oud binnen de SLT-verwerking van 90 minuten (beschikbaar voor CJA Premium)</li><li>Geavanceerde CJA Priority Ingestie: 1 week oude gegevens binnen SLT-verwerking van 90 minuten (beschikbaar voor CJA Ultimate)</li></ul> |  | donderdag 12 juni 2024 |
| **Accounts en locaties delen die worden gebruikt voor exporteren en importeren** | Gebruikers kunnen de accounts en locaties die ze maken nu beschikbaar maken voor alle gebruikers in hun organisatie. Alleen account- en locatie-eigenaars en systeembeheerders kunnen accounts en locaties bewerken en verwijderen. Eerder konden accounts en locaties alleen worden gebruikt door de gebruiker die ze heeft gemaakt. Deze instellingen zijn beschikbaar wanneer gebruikers [cloud-exportaccounts configureren](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/exports/cloud-export-accounts) en [cloudexportlocaties configureren](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/exports/cloud-export-locations). | donderdag 12 juni 2024 | Medio juli 2024 |
| **Meerdere velden in een vervolgkeuzemenu selecteren** | Wanneer meerdere velden zijn toegevoegd aan een vervolgkeuzefilter, kunnen gebruikers nu meerdere velden tegelijk selecteren. Het deelvenster wordt gefilterd en bevat een van de geselecteerde velden. <p>Eerder konden gebruikers slechts één veld tegelijk selecteren in een vervolgkeuzemenu.</p><p>De optie om een selectie in een drop-down filter te vereisen is verplaatst naar het menu wanneer het met de rechtermuisknop klikken van een drop-down filter.</p><p>Eerder konden gebruikers op de knop (x) naast de optie Geen filter in de vervolgkeuzelijst klikken.</p><p>Zie voor meer informatie [Statische vervolgkeuzefilters](/help/analysis-workspace/c-panels/panels.md#static-drop-down-filters) in [Overzicht van deelvensters](/help/analysis-workspace/c-panels/panels.md).</p><p>[Een videodemonstratie van deze functie weergeven](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/navigating-workspace-projects/use-multi-select-drop-down-filters).</p> |  | donderdag 19 juni 2024 |
| **Inhoudsopgave voor Workspace-projecten** | Er is nu een nieuwe inhoudsopgave beschikbaar voor projecten. De inhoudsopgave bevat koppelingen waarmee gebruikers snel tussen deelvensters en visualisaties in het project kunnen navigeren. <p>De inhoudsopgave is in alle projecten beschikbaar in de linkerspoorlijn.</p><p>Zie voor meer informatie [Inhoudsopgave van project](/help/analysis-workspace/build-workspace-project/project-table-of-contents.md).</p><p>[Een videodemonstratie van deze functie weergeven](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/navigating-workspace-projects/create-a-toc-in-analysis-workspace).</p> |  | donderdag 19 juni 2024 |
| **Hyperlinks maken voor dimensie-items in een vrije-vormtabel** | U kunt hyperlinks maken voor een of meer dimensie-items, zodat hierop kan worden geklikt in een vrije-vormtabel in Analysis Workspace. <p>U kunt hyperlinks maken voor dimensie-items die URL-waarden hebben, of u kunt aangepaste URL&#39;s maken voor dimensie-items die geen URL-waarden hebben.</p><p>U kunt dynamische aangepaste URL&#39;s maken voor meerdere dimensie-items met behulp van variabelen. Variabelen kunnen verwijzen naar de waarde van een dimensie-item of naar de uitsplitsingsdimensie.</p><p>Zie voor meer informatie [Hyperlinks maken voor afmetingen in een vrije-vormtabel](/help/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md).</p><p>[Een videodemonstratie van deze functie weergeven](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/tips-and-tricks/create-hyperlinks-in-freeform-tables).</p> |  | donderdag 19 juni 2024 |
| **De gegevensweergave van uw Customer Journey Analytics gebruiken met Adobe Journey Optimizer** | Een nieuwe configuratieoptie in Customer Journey Analytics staat u toe om een de gegevensmening van de Customer Journey Analytics aan gebruik met Adobe Journey Optimizer, zonder de behoefte aan handconfiguratie aan te wijzen. <p>Voor informatie over hoe te om deze configuratieoptie toe te laten, zie [Compatibiliteit](/help/data-views/create-dataview.md#compatibility) sectie in [Een gegevensweergave maken of bewerken](/help/data-views/create-dataview.md).</p><p>Eerder moest u een verbinding en gegevensmeningen manueel vormen wanneer het bekijken van de gegevens van Journey Optimizer in Customer Journey Analytics.</p> |  | donderdag 19 juni 2024 |
| **Soorten publiek wordt gepubliceerd naar een nieuwe sectie &quot;Soorten publiek&quot; in Experience Platform** | Soorten publiek die vanuit de Customer Journey Analytics worden gepubliceerd, zijn nu beschikbaar in de nieuwe sectie &quot;Soorten publiek&quot; in Adobe Experience Platform.<p>Eerder waren publiek dat vanuit Customer Journey Analytics werd gepubliceerd, beschikbaar in Experience Platform onder de sectie &quot;Segmenten&quot;.</p><p>Deze verbetering biedt de volgende voordelen:</p><ul><li>Het publiek heeft niet langer een vertraging van 1 uur voordat het in het Experience Platform wordt weergegeven; het zijn pas seconden nadat het is gepubliceerd.</li><li>De soorten publiek kunnen in Experience Platform worden gesorteerd door de kolom &quot;Oorsprong&quot;te gebruiken, die de toepassing toont waarvan het publiek oorspronkelijk werd gepubliceerd.</li><li>Met de filter- en sorteeropties in het Experience Platform kunt u sneller het desbetreffende publiek vinden.</li></ul> <p>(Koppeling naar documentatie)</p> |  | maandag 14 juli 2024 |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-345454; AN-349816; AN-349905; AN-350617

## Belangrijke kennisgevingen voor beheerders van Customers Journey Analytics

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | | |

{style="table-layout:auto"}

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release van Customer Journey Analytics voor 2024](/help/release-notes/2024.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
* [Opmerkingen bij de release voor het ophalen van streaming media](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Opmerkingen bij de release van Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)
* [Documentatieupdates Customer Journey Analytics](/help/release-notes/doc-changes.md)
