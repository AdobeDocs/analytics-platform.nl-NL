---
title: CJA-ondersteuning voor Adobe Experience Platform Data Governance
description: Leer hoe de gegevensetiketten en het beleid die in AEP worden bepaald rapportering in CJA beïnvloeden.
mini-toc-levels: 3
source-git-commit: 82060862c64aae10ea6dd375a8cd65d67ee21704
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 0%

---


# CJA-ondersteuning voor Adobe Experience Platform Data Governance

>[!NOTE]
>
>Deze functionaliteit is momenteel in [beperkte tests](/help/release-notes/releases.md).

De integratie tussen CJA en [Adobe Experience Platform Data Governance](https://experienceleague.adobe.com/docs/experience-platform/data-governance/home.html?lang=en) maakt etikettering van gevoelige CJA-gegevens en handhaving van privacybeleid mogelijk.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in het werkschema van CJA- gegevensmeningen worden rond gekomen. Deze labels stoppen of waarschuwen gebruikers die metriek en/of afmetingen van gevoelige velden maken.

Wanneer gegevens vanuit CJA worden geëxporteerd (via rapportage, export, API, enz.), worden bovendien waarschuwingen of labels toegevoegd om gebruikers te laten weten dat een rapport gevoelige informatie bevat die op een specifieke manier moet worden behandeld.

Dankzij deze integratie kunt u de compatibiliteit eenvoudiger beheren. Gegevensstewards in uw organisatie kunnen beleid plaatsen om gebruik te beperken. Dientengevolge, kunnen uw gebruikers CJA gegevens betrouwbaarder gebruiken, wetend dat het aan beleid voldoet dat door gegevens eerder wordt bepaald.

## Etikettering en beleid in Adobe Experience Platform

Wanneer u een dataset in Experience Platform creeert, kunt u tot stand brengen [gegevensgebruikslabels](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=en) voor sommige of alle elementen in de gegevensset. Tot nu toe zijn deze labels niet beschikbaar gesteld in CJA. Met deze release kunt u deze labels weergeven in CJA. Voor CJA zijn de volgende labels van bijzonder belang:

* De `C8` label - **[!UICONTROL No measurement]**. Dit label geeft aan dat gegevens niet kunnen worden gebruikt voor analyses op de websites of apps van uw organisatie.

* De `C12` label - **[!UICONTROL No General Data Export]**. Schemavelden met het label this way kunnen niet worden geëxporteerd of gedownload van CJA (via rapportage, export, API, enzovoort)

De etikettering op zich betekent niet dat deze etiketten van het gegevensgebruik worden afgedwongen. Daar wordt beleid voor gebruikt. U kunt uw beleid maken via de [Beleidsservice-API](https://experienceleague.adobe.com/docs/experience-platform/data-governance/api/overview.html?lang=en) in Experience Platform.

Het beleid bestaat uit twee onderdelen: het gegevensetiket en een marketingactie die consumenten kunnen ondernemen in het kader van een beleid inzake beperkt gegevensgebruik. In de context van CJA, twee Adobe-bepaald [marketingacties](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=en#appendix) zijn belangrijk:

* Analyse - gegevens gebruiken voor analytische doeleinden, zoals het meten, analyseren en rapporteren van het consumentengebruik van de sites of apps van uw organisatie.

* Gegevens exporteren naar een derde partij, dat wil zeggen uit de Adobe-omgeving.

U koppelt labels en marketingacties aan een beleid en schakelt het beleid vervolgens in. Het beleid neemt het etiket en de marketing actie en zegt: deze beperking handhaven. In CJA worden twee door Adobe gedefinieerde beleidsregels weergegeven die van invloed zijn op rapportage en downloaden/delen:

* Beleid voor analyse afdwingen
* Downloadbeleid afdwingen


### Gegevenslabels weergeven in CJA-gegevensweergaven

De etiketten van gegevens die in Experience Platform werden gecreeerd worden getoond in drie plaatsen in het gebruikersinterface van gegevensmeningen:

| Locatie | Beschrijving |
| --- | --- |
| De knop Info op een schemaveld | Klik op deze knop om aan te geven welke labels voor gegevensgebruik momenteel van toepassing zijn op een veld:<p>![](assets/data-label-left.png) |
| Rechterspoor onder [Componentinstellingen](/help/data-views/component-settings/overview.md) | Alle labels voor gegevensgebruik worden hier weergegeven:<p>![](assets/data-label-right.png) |
| Gegevenslabels toevoegen als kolom | U kunt de Etiketten van Gegevens als kolom aan de Opgenomen kolommen van Componenten in gegevensmeningen toevoegen. Klik enkel het pictogram van de kolomselecteur en selecteer de Etiketten van het Gebruik van Gegevens:<p>![](assets/data-label-column.png) |

### Filter op labels voor gegevensbeheer in gegevensweergaven

Klik in de editor voor gegevensweergaven op het pictogram Filter in het linkerspoor en filter de componenten van de gegevensweergaven op het label of de labels voor gegevensbeheer:

![](assets/filter-labels.png)

Klikken **[!UICONTROL Apply]** om te zien welke componenten etiketten hebben in bijlage aan hen.

### Filter op beleid voor gegevensbeheer in gegevensweergaven

U kunt controleren om te zien of wordt een beleid aangezet dat het gebruik van bepaalde elementen van de CJA- gegevensmening voor analytische of uitvoerdoel blokkeert.

Klik nogmaals op het pictogram Filter in de linkertrack en klik onder Gegevensbeheer op Beleid:

![](assets/filter-policies.png)

Klikken **[!UICONTROL Apply]** om te zien welk beleid wordt toegelaten _voor deze gegevensweergave?_

### Hoe [!UICONTROL Enforce Analytics] beleid beïnvloedt Werkruimteprojecten

Als dit beleid wordt aangezet, die schemagebieden die bepaalde gegevensetiketten (zoals C8) verbonden aan hen hebben niet voor analysedoeleinden binnen de Werkruimte CJA kunnen worden gebruikt.

Voor rapportage betekent dit dat

* U kunt deze velden niet toevoegen aan gegevensweergaven en ze worden grijs weergegeven in de linkertrack [!UICONTROL Schema fields] lijst.
* U kunt geen gegevensweergave opslaan waarin velden zijn geblokkeerd.

Als u probeert een Workspace-analyse uit te voeren op gegevensweergaven die items bevatten die niet zijn toegestaan voor analyses, krijgt u een bericht zoals dit:

![](assets/policy-enforce.png)

Op individuele componenten zou het bericht gelijkaardig aan dit zijn:

![](assets/policy-enforce2.png)

### Hoe [!UICONTROL Enforce Download] beleid beïnvloedt Werkruimteprojecten

Als dit beleid wordt aangezet, zal om het even welke download (zoals het e-mailen of het delen van pdfs) van de projecten van de Werkruimte de gevoelige gebieden hakken. U kunt deze velden nog steeds analyseren in Workspace, maar als u een project probeert te e-mailen of anderszins te delen, worden de geblokkeerde velden weergegeven als gehashte items in het .pdf-bestand.

Voeg hier een schermafbeelding toe.

### Labels weergeven in Report Builder

Zie _deze sectie_ voor meer informatie . (link naar Christine&#39;s doc)
