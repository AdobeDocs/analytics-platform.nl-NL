---
title: Migreren van Adobe Analytics naar Customer Journey Analytics
description: Stappen voor migratie van Adobe Analytics naar Customer Journey Analytics
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 868cd819148b29436fbd92cf220c8bc4cb9e0725
workflow-type: tm+mt
source-wordcount: '1038'
ht-degree: 0%

---


# Migratie van Adobe Analytics naar Customer Journey Analytics voorbereiden

Voordat u uw gegevens van Adobe Analytics naar Customer Journey Analytics migreert, verkent u deze overwegingen om uw gegevens voor te bereiden en om u bewust te maken van de kritieke verschillen tussen de twee technologieën.

## Uw gegevens voorbereiden

Het voorbereiden van uw Adobe Analytics-gegevens voor een naadloze overgang naar Customer Journey Analytics is van essentieel belang voor de gegevensintegriteit en de consistentie van rapporten.

### 1. Identiteiten verzamelen

Misschien de meest kritieke component van het begrip van een klantenreis is het weten van wie de klant bij elke stap is. Voor Customer Journey Analytics, staat het hebben van een herkenningsteken dat over al uw kanalen en de overeenkomstige gegevens bestaat voor het verbinden van veelvoudige bronnen binnen CJA toe.
Voorbeelden van identiteiten kunnen een klant-id, account-id of e-mailadres zijn. Ongeacht de identiteit (en er kunnen meerdere zijn), moet u rekening houden met het volgende voor elke id:

* Bestaat of kan aan op alle gegevensbronnen worden toegevoegd u in CJA wilt brengen
* Wordt gevuld op elke rij gegevens
* Bevat geen PII. Pas hashing op om het even wat toe die gevoelig zou kunnen zijn.
* Gebruikt dezelfde indeling voor alle bronnen (dezelfde lengte, dezelfde hash-methode, enz.)

In datasets zoals Adobe Analytics, kan een identiteit niet op elke rij van gegevens bestaan, maar een secundaire identiteit. In dit geval, kan de Analytics van het Kanaal (vroeger genoemd &quot;Op gebied-gebaseerde Stitching&quot;) worden gebruikt om de hiaat tussen rijen te overbruggen wanneer een klant slechts door hun ECID wordt geïdentificeerd en wanneer een identiteit wordt verzameld (bijvoorbeeld, wanneer een klant voor authentiek verklaart). [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/cca/overview.html?lang=en)

### 2. Variabelen uitlijnen

De meest eenvoudige migratie van Adobe Analytics-gegevens naar Customer Journey Analytics is het opnemen van een algemene rapportsuite in Experience Platform met behulp van de [Adobe Analytics Source Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en). Deze schakelaar brengt uw variabelen van Adobe Analytics rechtstreeks aan een schema XDM en dataset in AEP in kaart, die beurtelings gemakkelijk met CJA kunnen worden verbonden.

Een volledige algemene rapportenreeks is mogelijk niet altijd uitvoerbaar voor een implementatie. Als u veelvoudige rapportreeksen in Customer Journey Analytics wilt brengen, moet u vooruit plannen om variabelen over die rapportreeksen te brengen.

eVar 1 in rapportsuite 1 verwijst bijvoorbeeld naar [!UICONTROL Page]. In rapportsuite 2 kan eVar1 verwijzen naar [!UICONTROL Internal Campaign]. Wanneer deze variabelen in CJA worden opgenomen, zullen ze zich in één enkele eVar1-dimensie mengen, wat kan leiden tot verwarring en onjuiste rapportage.

Als u niet naar een algemene rapportsuite bent gegaan vanwege problemen met [!UICONTROL Uniques Exceeded] of [!UICONTROL Low Traffic], weet dat CJA geen [kardinaliteitsbeperkingen voor een dimensie](/help/components/dimensions/high-cardinality.md). Hiermee kan elke unieke waarde worden weergegeven en geteld.

### 3. (Opnieuw)Uw marketingkanalen configureren

De traditionele Adobe Analytics Marketing Channel-instellingen voeren niet hetzelfde uit in CJA. Dit is om twee redenen:

* het verwerkingsniveau op de Adobe Analytics-gegevens die in Adobe Experience Platform worden ingevoerd, en

* De rapporttijd van Customer Journey Analytics

Adobe heeft gepubliceerd [bijgewerkte best practices voor implementatie van marketingkanalen](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/mchannel-best-practices.html?lang=en). Met deze bijgewerkte aanbevelingen kunt u optimaal gebruikmaken van de mogelijkheden die Adobe Analytics al met Attribution IQ heeft. Ze zullen u ook instellen voor succes bij het overschakelen naar Customer Journey Analytics.

### 4. Beslissen over het gebruik van gegevensconnector Analytics vs. SDK&#39;s van Experience Platforms

Als [Beleef de rand](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en) De gegevensinzameling evolueert, zult u waarschijnlijk aan of het Web SDK van Adobe Experience Platform of de Mobiele SDK van Adobe Experience Platform met het Netwerk van de Rand van Adobe Experience Platform migreren. Terwijl een typische implementatie van SDKs gegevens naar Adobe Analytics zal verzenden, biedt een nieuwe kans voor het verzenden van gegevens rechtstreeks naar Adobe Experience Platform. Het kan dan in Customer Journey Analytics worden opgenomen, terwijl ook het handhaven van gegevens die naar Adobe Analytics worden verzonden.

Met deze methode worden de mogelijkheden voor gegevensverzameling aanzienlijk uitgebreid: Er geldt niet langer een beperking op het aantal velden of de noodzaak om gegevenselementen toe te wijzen aan props, eVars en gebeurtenissen zoals in Analytics. U kunt onbeperkte schemaelementen van verschillende types gebruiken en hen vertegenwoordigen op veelvoudige manieren gebruikend CJA [Gegevens](/help/data-views/data-views.md). De beschikbaarheid van gegevens neemt toe wanneer deze rechtstreeks naar Adobe Experience Platform worden verzonden, omdat de tijd voor gegevensverwerking via Adobe Analytics wordt verwijderd.

**Voordelen van het gebruiken van Experience Platform SDKs**

* Flexibel schema voor het definiëren van velden die u nodig hebt
* Niet afhankelijk van Adobe Analytics-nomenclatuur (profiel, eVar, gebeurtenis, enz.)
* Geen tekenlimiet (100 tekens voor props)
* Snellere gegevensbeschikbaarheid in Adobe Experience Platform

**Drawbacks aan het gebruiken van Experience Platform SDKs**

De volgende Adobe Analytics-componenten worden niet ondersteund:

* Marketingkanalen
* Bot filteren
* Geo, Domain, Device Lookups
* Analyses voor doel (A4T)

## Voorbereiden op kritieke verschillen

### Geniet van gemak met de verwerking van de rapporttijd

De rapportage in Adobe Analytics is afhankelijk van een aanzienlijke hoeveelheid gegevens die vooraf wordt verwerkt om resultaten te genereren zoals de persistentie die je in eVars ziet. Customer Journey Analytics voert die berekeningen in rapportruntime uit.

De tijdverwerking van het rapport opent de capaciteit om montages toe te passen die retroactief zijn en veelvoudige versies van veranderlijke persistentie tot stand brengen zonder het moeten veranderen hoe de onderliggende gegevens worden verzameld.

Deze verschuiving resulteert in enkele verschillen in de manier waarop gegevens worden gerapporteerd, met name voor variabelen die een lang verloopvenster kunnen hebben. U kunt beginnen door te evalueren hoe de rapport-tijd verwerking uw rapportering kan beïnvloeden gebruikend [virtuele rapportsuite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html).

### Identificeer kritieke Segmenten en Berekende Metriek

Adobe Analytics-segmenten (filters in CJA genoemd) en berekende meetwaarden zijn niet compatibel met Customer Journey Analytics. In veel gevallen, kunnen deze componenten in CJA worden herbouwd gebruikend de nieuwe schema&#39;s en beschikbare gegevens.

Als u de overgang zo soepel mogelijk wilt laten verlopen voor gebruikers die een overgang maken tussen de systemen, kunt u

1. De meest kritieke onderdelen van deze componenten identificeren.

1. hun definities te documenteren, en

1. Identificeren welke velden in de gegevens vereist zijn om deze in CJA te repliceren als [Filters](/help/components/filters/filters-overview.md) en [Berekende cijfers](/help/components/calc-metrics/calc-metr-overview.md).

Hieronder volgen enkele video&#39;s die u moeten begeleiden:

* [Adobe Analytics-segmenten verplaatsen naar Customer Journey Analytics](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/moving-adobe-analytics-segments-to-customer-journey-analytics.html?lang=en)

* [Je berekende cijfers van Adobe Analytics naar Customer Journey Analytics verplaatsen](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/moving-your-calculated-metrics-from-adobe-analytics-to-customer-journey-analytics.html?lang=en)
