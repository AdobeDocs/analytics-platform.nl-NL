---
description: Ontdek hoe AEP-Attribution AI kunnen worden geïntegreerd met Workspace in CJA.
title: Attribution AI integreren met CJA
role: Admin
solution: Customer Journey Analytics
exl-id: 5ab563b9-d4f6-4210-8789-e16e5c93d968
mini-toc-levels: 3
source-git-commit: c87d7428a2ddca35297225314e97171fe8b129fb
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 1%

---

# Attribution AI integreren met CJA

[Attribution AI](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/attribution-ai/overview.html?lang=en), als onderdeel van Adobe Experience Platform Intelligent Services, is een multi-channel, algoritmische attributiedienst die de invloed en de incrementele impact van klanteninteractie tegen gespecificeerde resultaten berekent. Met Attribution AI kunnen marketers marketing- en advertentiekosten meten en optimaliseren door de impact van elke individuele interactie van de klant in elke fase van de klantentransmissie te begrijpen.

Attribution AI integreert met Customer Journey Analytics (CJA) voor zover de Attribution AI modellen tegen de marketing touchpoints van klanten en omzettingsdatasources in werking stelt. CJA importeert dan de uitvoer van die modellen als een gegevensset, of het kan worden geïntegreerd met de rest van uw CJA-gegevenssets. Attribution AI-Toegelaten datasets kunnen dan in gegevensmeningen en rapportering in CJA worden gebruikt.

Attribution AI steunt 3 schema&#39;s van het Experience Platform: Experience Event, Adobe Analytics en Consumer Experience Event.

Attribution AI ondersteunt twee scores: algoritmisch en op regel gebaseerd.

## Algoritmische scores

Algoritmische scores omvatten incrementele en beïnvloede scores.

* **[!UICONTROL Influenced]scores** 100 % van het conversiekrediet wordt verdeeld over de afzetkanalen .
* **[!UICONTROL Incremental]scores** in de eerste plaats rekening houden met een basislijn voor omzetting die u zelfs zonder marketing zou hebben bereikt. Deze basislijn hangt van AI observaties van patronen, seizoensgebondenheid, etc., toe te schrijven aan bestaande merkerkenning, loyaliteit, en woord van mond. De resterende kredieten worden verdeeld over de afzetkanalen.

## Op regels gebaseerde scores

Op regels gebaseerde scores omvatten

* **[!UICONTROL First touch]** geeft 100% krediet aan het aanraakpunt dat voor het eerst in het terugkijkvenster van de attributie wordt gezien.
* **[!UICONTROL Last touch]** geeft 100% krediet aan het aanraakpunt dat zich het laatst vóór de conversie voordeed.
* **[!UICONTROL Linear]** geeft hetzelfde krediet aan elk aanraakpunt dat wordt weergegeven voor een conversie.
* **[!UICONTROL U-shaped]** geeft 40% krediet aan de eerste interactie, 40% krediet aan de laatste interactie, en deelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt aan beide een krediet van 50% toegekend.
* **[!UICONTROL Time-Decay]** volgt een exponentieel verval met een aangepaste parameter voor de halfwaardetijd, waarbij de standaardwaarde 7 dagen is. Het gewicht van elk kanaal is afhankelijk van de hoeveelheid tijd die is verstreken tussen het starten van het aanraakpunt en de uiteindelijke conversie. De formule die wordt gebruikt om het krediet te bepalen is `2^(-t/halflife)`, waarbij `t` is de hoeveelheid tijd tussen een aanraakpunt en een conversie. Alle aanraakpunten worden vervolgens genormaliseerd tot 100%.

## Workflow

Sommige stappen worden uitgevoerd in Adobe Experience Platform voordat wordt gewerkt met de uitvoer in CJA. De uitvoer bestaat uit een gegevensset met een toegepast Attribution AI-model.

### Stap 1: Een Attribution AI-instantie maken

Maak in Experience Platform een Attribution AI-instantie door gegevens te selecteren en toe te wijzen, gebeurtenissen te definiëren en uw gegevens op te leiden, zoals beschreven [hier](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/attribution-ai/user-guide.html).

![AAI-instantie](assets/aai-instance.png)

### Stap 2: Een CJA-verbinding met gegevenssets van Attribution AI instellen

In CJA kunt u nu [een of meer verbindingen maken](/help/connections/create-connection.md) op gegevenssets van Experience Platforms die van instrumenten zijn voorzien voor Attribution AI. Deze datasets verschijnen met het prefix &quot;van Scores van de Attribution AI&quot;, zoals hier getoond:

![AAI-scores](assets/aai-scores.png)

![Verbinding maken](assets/aai-create-connection.png)

### Stap 3: Gegevensweergaven maken op basis van deze verbindingen

In CJA: [een of meer gegevensweergaven maken](/help/data-views/create-dataview.md) die de Attribution AI XDM-velden bevatten.

Hier volgen de XDM-schemavelden voor aanraakpunten:

![XDM-velden met aanraakpunten](assets/touchpoint-fields.png)

En hier zijn de XDM schemagebieden voor omzetting:

![XDM-velden converteren](assets/conversion-fields.png)

### Stap 4: AAI-gegevens rapporteren in CJA Workspace

In een project van de Werkruimte van CJA, kunt u metriek zoals &quot;Orders van AAI&quot;trekken, en dimensies zoals &quot;Naam van de Campagne AAI&quot; of &quot;Kanaal van de Marketing van AAI&quot;, bijvoorbeeld.

![AAI-afmetingen](assets/aai-dims.png)

De onbewerkte score in AAI heeft een genest schema, waarbij het pad naar velden lang genoeg kan zijn om de meeste spaties in tabellen of visualisaties op te nemen. Ter beknoptheid: [!UICONTROL Display Name] wordt automatisch gegenereerd en gebruikt in CJA volgens de onderstaande regels:

* Alle velden hebben een voorvoegsel &quot;AAI&quot;
* Voor aanraakpuntvelden:
   * Voor gebieden die deel van de score XDM uitmaken, verschijnen zij in CJA zoals `AAI T {field name}`
   * Voor velden die zijn opgenomen als passThrough-kolom, worden ze in CJA weergegeven als `AAI T PT {field name}`
* Voor conversievelden:
   * Voor gebieden die deel van de score XDM uitmaken, zullen zij in CJA verschijnen zoals `AAI C {field name}`
   * Voor velden die zijn opgenomen als passThrough-kolom, worden ze in CJA weergegeven als `AAI C PT {field name}`

**Orders met beïnvloede en incrementele scores**

Hier zien we een Workspace-project met AAI-gegevens die orders met beïnvloede en incrementele scores weergeven. Bouw neer aan om het even welke afmeting om attributie te begrijpen door: campagne, productgroep, gebruikerssegment, geografie, enzovoort.

![AAI-project](assets/aai-project.png)

![AAI-project](assets/aai-project2.png)

**Marketingprestaties**

Toonpuntattributie vergelijken en contrasten tussen verschillende attributiemodellen:

![Vergelijken](assets/compare.png)

**Kanaalinteractie**

Begrijp kanaalinteractie om te zien welk kanaal het meest effectief met andere kanalen kan worden gebruikt, gebruikend een diagram van de Plaats:

![Overlappen van marketingkanaal](assets/mc-overlap.png)

**Bovenste paden naar conversie**

In deze tabel worden de belangrijkste paden naar conversie (gededupliceerd) weergegeven die u helpen bij het ontwerpen en optimaliseren van aanraakpunten:

![Bovenste kanalen](assets/top-channels.png)

**Tijd leiden naar conversie**

Hier zien we de aanlooptijd naar conversie wanneer een aanraakpunt in de mix zit. Het helpt bij het optimaliseren van doorlooptijd:

![Leadtijd](assets/lead-time.png)

## Verschillen tussen Attribution AI en Attribution IQ

Wanneer moet u dus Attribution AI-gegevens gebruiken in plaats van [Attribution IQ](/help/analysis-workspace/attribution/overview.md), een native CJA-mogelijkheid? In deze tabel worden enkele verschillen in functionaliteit weergegeven:

| Functionaliteit | Attribution AI | Attribution IQ |
| --- | --- | --- |
| Bepaalt incrementele toewijzing | Ja | Nee |
| Hiermee kunnen gebruikers het model aanpassen | Ja | Ja |
| Kenmerken via kanalen (Opmerking: AAI gebruikt niet de gegevens die in CJA zijn opgeslagen.) | Ja | Ja |
| Inclusief beïnvloede scores | Ja | Ja |
| Werken met ML | Ja | Ja |
| Op regio&#39;s gebaseerde attributiemodellen | Ja | Ja |
| Kan marketingaanraakpunten in model configureren | Ja | Nee |

{style=&quot;table-layout:auto&quot;}
