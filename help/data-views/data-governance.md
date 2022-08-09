---
title: CJA-ondersteuning voor Adobe Experience Platform Data Governance
description: null
source-git-commit: 40b87cd748717124a355b030b17b1e3b6f94a99e
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---


# CJA-ondersteuning voor Adobe Experience Platform Data Governance

De integratie tussen CJA en [Adobe Experience Platform Data Governance](https://experienceleague.adobe.com/docs/experience-platform/data-governance/home.html?lang=en) maakt etikettering van gevoelige CJA-gegevens en handhaving van privacybeleid mogelijk.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in het werkschema van CJA- gegevensmeningen worden rond gekomen. Deze labels stoppen of waarschuwen gebruikers die metriek en/of afmetingen van gevoelige velden maken.

Wanneer gegevens vanuit CJA worden geëxporteerd (via rapportage, export, API, enz.), worden bovendien waarschuwingen of labels toegevoegd om gebruikers te laten weten dat een rapport gevoelige informatie bevat die op een specifieke manier moet worden behandeld.

Dankzij deze integratie kunt u de compatibiliteit eenvoudiger beheren. Gegevensstewards in uw organisatie kunnen beleid plaatsen om gebruik te beperken. Dientengevolge, kunnen uw gebruikers CJA gegevens betrouwbaarder gebruiken, wetend dat het aan beleid voldoet dat door gegevens eerder wordt bepaald.

## Etikettering en beleid in Adobe Experience Platform

Wanneer u een dataset in Experience Platform creeert, kunt u tot stand brengen [gegevensgebruikslabels](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=en) voor sommige of alle elementen in de gegevensset. Tot nu toe zijn deze labels niet beschikbaar gesteld in CJA. Met deze release kunt u deze labels weergeven in CJA. CJA heeft met name belang bij het label C8, waarin staat: &quot;Gegevens kunnen niet worden gebruikt voor het meten van de websites of apps van uw organisatie&quot;.

De etikettering op zich betekent niet dat deze etiketten van het gegevensgebruik worden afgedwongen. Daar wordt beleid voor gebruikt. U kunt uw beleid maken via de [Beleidsservice-API](https://experienceleague.adobe.com/docs/experience-platform/data-governance/api/overview.html?lang=en) in Experience Platform.

Het beleid bestaat uit twee onderdelen: het gegevensetiket en een marketingactie die consumenten kunnen ondernemen in het kader van een beleid inzake beperkt gegevensgebruik. In de context van CJA, twee Adobe-bepaald [marketingacties](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=en#appendix) zijn belangrijk:

* Analyse - gegevens gebruiken voor analytische doeleinden, zoals het meten, analyseren en rapporteren van het consumentengebruik van de sites of apps van uw organisatie.

* Deze gegevens exporteren uit de Adobe-omgeving, zoals gegevens exporteren naar een derde.

U koppelt labels en marketingacties aan een beleid en schakelt het beleid vervolgens in. Het beleid neemt het etiket en de marketing actie en zegt: deze beperking handhaven. In CJA worden twee door Adobe gedefinieerde beleidsregels opgehaald:

* Analysebeleid
* Beleid voor downloaden

## Gegevenslabels weergeven in CJA-gegevensweergaven

De etiketten van gegevens die in Experience Platform werden gecreeerd tonen in drie plaatsen in het gebruikersinterface van gegevensmeningen:

| Locatie | Beschrijving |
| --- | --- |
| De knop Info op een schemaveld | Klik op deze knop om aan te geven welke labels voor gegevensgebruik momenteel van toepassing zijn op een veld:<p>![](assets/data-label-left.png) |
| Rechterspoor onder [Componentinstellingen](/help/data-views/component-settings/overview.md) | Alle labels voor gegevensgebruik worden hier weergegeven:<p>![](assets/data-label-right.png) |
| Gegevenslabels toevoegen als kolom | U kunt de Etiketten van Gegevens als kolom aan de Opgenomen kolommen van Componenten in gegevensmeningen toevoegen. Klik enkel het pictogram van de kolomselecteur en selecteer de Etiketten van het Gebruik van Gegevens:<p>![](assets/data-label-column.png) |

### Filter op labels voor gegevensbeheer in CJA

Klik in de editor voor gegevensweergaven op het pictogram Filter in het linkerspoor en filter de componenten van de gegevensweergaven op de labels voor gegevensbeheer:

![](assets/filter-labels.png)

### Filter op beleid voor gegevensbeheer in CJA

U kunt controleren om te zien of wordt een beleid aangezet dat het gebruik van bepaalde elementen van de CJA- gegevensmening voor analytische of uitvoerdoel blokkeert.

Klik nogmaals op het pictogram Filter in de linkertrack en klik onder Gegevensbeheer op Beleid:

![](assets/filter-policies.png)

Als het beleid wordt aangezet, die schemagebieden die bepaalde gegevensetiketten (zoals C8) verbonden aan hen hebben, kunnen niet voor analytische of downloaddoeleinden (zoals het e-mailen of het delen van pdfs) binnen de Werkruimte van CJA worden gebruikt.

Let op:

* U mag deze niet toevoegen aan gegevensweergaven. Deze velden worden grijs weergegeven in de lijst met velden van het linkerspoorwegschema.
* U kunt geen gegevensweergave opslaan waarin velden zijn geblokkeerd.


