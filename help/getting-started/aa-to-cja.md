---
title: Migreren van Adobe Analytics naar Customer Journey Analytics
description: Stappen voor migratie van Adobe Analytics naar Customer Journey Analytics
solution: Customer Journey Analytics
feature: CJA Basics
exl-id: 5e3f0aa0-ba24-48c8-948c-ebb5c270f34d
source-git-commit: 2f38b38328816a523427d73f812041904e294bc7
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# Migratie van Adobe Analytics naar Customer Journey Analytics voorbereiden

Voordat u uw gegevens van Adobe Analytics naar Customer Journey Analytics migreert, verkent u deze overwegingen om uw gegevens voor te bereiden en om u bewust te maken van de kritieke verschillen tussen de twee technologieën.

## Uw gegevens voorbereiden

Het voorbereiden van uw Adobe Analytics-gegevens voor een naadloze overgang naar Customer Journey Analytics is van essentieel belang voor de gegevensintegriteit en de consistentie van rapporten.

### 1. Identiteiten verzamelen

Misschien de meest kritieke component van het begrip van een klantenreis is het weten van wie de klant bij elke stap is. Voor Customer Journey Analytics, staat het hebben van een herkenningsteken dat over al uw kanalen en de overeenkomstige gegevens bestaat voor het verbinden van veelvoudige bronnen binnen CJA toe.
Voorbeelden van identiteiten kunnen een klant-id, account-id of e-mailadres zijn. Ongeacht de identiteit (en er kunnen meerdere zijn), moet u rekening houden met het volgende voor elke id:

* Id bestaat of kan worden toegevoegd aan alle gegevensbronnen die u in CJA wilt plaatsen
* ID is gevuld op elke rij gegevens
* ID bevat geen PII. Pas hashing op om het even wat toe die gevoelig zou kunnen zijn.
* ID gebruikt dezelfde indeling voor alle bronnen (dezelfde lengte, dezelfde hash-methode, enz.)

In datasets zoals Adobe Analytics, kan een identiteit niet op elke rij van gegevens bestaan, maar een secundaire identiteit. In dit geval, kan de Analytics van het Kanaal (vroeger genoemd &quot;Op gebied-gebaseerde Stitching&quot;) worden gebruikt om de hiaat tussen rijen te overbruggen wanneer een klant slechts door hun ECID wordt geïdentificeerd en wanneer een identiteit wordt verzameld (bijvoorbeeld, wanneer een klant voor authentiek verklaart). [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/cca/overview.html?lang=en)

### 2. Variabelen uitlijnen

De meest eenvoudige migratie van Adobe Analytics-gegevens naar Customer Journey Analytics is het opnemen van een [algemene rapportsuite](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html?lang=en) in Experience Platform met de [Adobe Analytics Source Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en). Deze schakelaar brengt uw variabelen van Adobe Analytics rechtstreeks aan een schema XDM en dataset in AEP in kaart, die beurtelings gemakkelijk met CJA kunnen worden verbonden.

Een volledige algemene rapportenreeks is mogelijk niet altijd uitvoerbaar voor een implementatie. Als u veelvoudige rapportreeksen in Customer Journey Analytics wilt brengen, moet u vooruit plannen om variabelen over die rapportreeksen te brengen.

eVar 1 in rapportsuite 1 verwijst bijvoorbeeld naar [!UICONTROL Page]. In rapportsuite 2 kan eVar1 verwijzen naar [!UICONTROL Internal Campaign]. Wanneer deze variabelen in CJA worden opgenomen, zullen ze zich in één enkele eVar1-dimensie mengen, wat kan leiden tot verwarring en onjuiste rapportage.

Als u niet naar een algemene rapportsuite bent gegaan vanwege problemen met [!UICONTROL Uniques Exceeded] of [!UICONTROL Low Traffic], weet dat CJA geen [kardinaliteitsbeperkingen voor een dimensie](/help/components/dimensions/high-cardinality.md). Hiermee kan elke unieke waarde worden weergegeven en geteld.

### 3. (Opnieuw)Uw marketingkanalen configureren

De traditionele Adobe Analytics Marketing Channel-instellingen voeren niet hetzelfde uit in CJA. Dit is om twee redenen:

* het verwerkingsniveau op de Adobe Analytics-gegevens die in Adobe Experience Platform worden ingevoerd, en

* De rapporttijd van Customer Journey Analytics

Adobe heeft gepubliceerd [bijgewerkte best practices voor implementatie van marketingkanalen](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/mchannel-best-practices.html?lang=en). Met deze bijgewerkte aanbevelingen kunt u optimaal gebruikmaken van de mogelijkheden die Adobe Analytics al met Attribution IQ heeft. Ze zullen u ook instellen voor succes bij het overschakelen naar Customer Journey Analytics.

### 4. Beslissen over het gebruik van de gegevensbronaansluiting versus Experience Platform-SDK&#39;s

Als [Beleef de rand](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en) de gegevensinzameling evolueert, zult u waarschijnlijk aan of migreren [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/web-sdk.html?lang=en) of [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/mobile.html?lang=en) met het Adobe Experience Platform Edge Network. Terwijl een typische implementatie van SDKs gegevens naar Adobe Analytics zal verzenden, biedt een nieuwe kans voor het verzenden van gegevens rechtstreeks naar Adobe Experience Platform. Het kan dan in Customer Journey Analytics worden opgenomen, terwijl ook het handhaven van gegevens die naar Adobe Analytics worden verzonden.

Met deze methode worden de mogelijkheden voor gegevensverzameling aanzienlijk uitgebreid: Er geldt niet langer een beperking op het aantal velden of de noodzaak om gegevenselementen toe te wijzen aan props, eVars en gebeurtenissen zoals in Analytics. U kunt onbeperkte schemaelementen van verschillende types gebruiken en hen vertegenwoordigen op veelvoudige manieren gebruikend CJA [Gegevens](/help/data-views/data-views.md). De beschikbaarheid van gegevens neemt toe wanneer deze rechtstreeks naar Adobe Experience Platform worden verzonden, omdat de tijd voor gegevensverwerking via Adobe Analytics wordt verwijderd.

**Voordelen van het gebruiken van Experience Platform SDKs**

* Flexibel schema voor het definiëren van velden die u nodig hebt
* Niet afhankelijk van Adobe Analytics-nomenclatuur (profiel, eVar, gebeurtenis, enz.)
* Geen tekenlimiet (100 tekens voor props)
* Snellere gegevensbeschikbaarheid in Adobe Experience Platform

**Drawbacks aan het gebruiken van Experience Platform SDKs**

De volgende Adobe Analytics-functies of -componenten worden niet ondersteund:

* Marketingkanalen
* Bot filteren
* Geo, Domain, Device Lookups
* Analyses voor doel (A4T)

## Voorbereiden op kritieke verschillen

### Geniet van gemak met de verwerking van de rapporttijd

De rapportage in Adobe Analytics is afhankelijk van een aanzienlijke hoeveelheid gegevens die vooraf wordt verwerkt om resultaten te genereren zoals de persistentie die u in [!UICONTROL eVars]. Customer Journey Analytics voert deze berekeningen daarentegen uit tijdens de uitvoering van het rapport.

[!UICONTROL Report time processing] Hiermee opent u de mogelijkheid om instellingen met terugwerkende kracht toe te passen en meerdere versies van variabele persistentie te maken zonder dat u hoeft te wijzigen hoe de onderliggende gegevens worden verzameld.

Deze verschuiving resulteert in enkele verschillen in de manier waarop gegevens worden gerapporteerd, met name voor variabelen die een lang verloopvenster kunnen hebben. U kunt beginnen door te evalueren hoe de rapport-tijd verwerking uw rapportering kan beïnvloeden gebruikend [virtuele rapportsuite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html).

### Identificeer kritieke Segmenten en Berekende Metriek

Adobe Analytics-segmenten (opgeroepen [!UICONTROL filters] in CJA) en berekende meetwaarden zijn niet compatibel met Customer Journey Analytics. In veel gevallen, kunnen deze componenten in CJA worden herbouwd gebruikend de nieuwe schema&#39;s en beschikbare gegevens.

Als u de overgang zo soepel mogelijk wilt laten verlopen voor gebruikers die een overgang maken tussen de systemen, kunt u

1. De meest kritieke onderdelen van deze componenten identificeren.

1. hun definities te documenteren, en

1. Identificeren welke velden in de gegevens vereist zijn om deze in CJA te repliceren als [Filters](/help/components/filters/filters-overview.md) en [Berekende cijfers](/help/components/calc-metrics/calc-metr-overview.md).

Hieronder volgen enkele video&#39;s die u moeten begeleiden:

* [Adobe Analytics-segmenten verplaatsen naar Customer Journey Analytics](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/moving-adobe-analytics-segments-to-customer-journey-analytics.html?lang=en)

* [Je berekende cijfers van Adobe Analytics naar Customer Journey Analytics verplaatsen](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/moving-your-calculated-metrics-from-adobe-analytics-to-customer-journey-analytics.html?lang=en)

### Andere overwegingen

* Gebruikend de macht van CJA- gegevensmeningen, hebt u veel meer flexibiliteit in de definitie van metriek en dimensies binnen Customer Journey Analytics. U kunt bijvoorbeeld de waarde van een dimensie gebruiken om een metrische definitie te worden. [Meer informatie](/help/data-views/data-views-usecases.md)

* Als u een aangepaste kalender hebt gedefinieerd in Adobe Analytics, hebt u vergelijkbare kalendermogelijkheden binnen CJA. U moet ervoor zorgen dat uw kalender correct wordt bepaald.

* In Customer Journey Analytics, kunt u een douanebezoek/zittingsonderbreking bepalen evenals metrisch bepalen die een nieuwe zitting zal beginnen. U kunt gegevensweergaven maken met verschillende sessiedefinities om meer inzicht te krijgen dan in Adobe Analytics mogelijk was. Dit vermogen kan bijzonder gunstig zijn voor mobiele datasets.

## Volgende stappen

Nadat u naar CJA bent gegaan, kunt u, als u gegevensdiscrepanties opmerkt, uw oorspronkelijke Adobe Analytics-gegevens vergelijken met de Adobe Analytics-gegevens die nu in Customer Journey Analytics staan. [Meer informatie](/help/troubleshooting/compare.md)