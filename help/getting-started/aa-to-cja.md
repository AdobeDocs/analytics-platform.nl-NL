---
title: Evolutie uit Adobe Analytics
description: Stappen om Adobe Analytics-gegevens om te zetten in Customer Journey Analytics-gegevens
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 5e3f0aa0-ba24-48c8-948c-ebb5c270f34d
source-git-commit: 38be838fccf896a12da3fbadac50e578081312ba
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 0%

---

# Evolutie uit Adobe Analytics

## Bestaande gegevens voorbereiden

Het voorbereiden van uw Adobe Analytics-gegevens voor een naadloze overgang naar Customer Journey Analytics is van essentieel belang voor de gegevensintegriteit en de consistentie van de rapportage.

### Identiteiten verzamelen

Misschien de meest kritieke component van het begrip van een klantenreis is het weten van wie de klant bij elke stap is. Voor Customer Journey Analytics kunt u met een id die al uw kanalen en de bijbehorende gegevens bevat, meerdere bronnen samenvoegen in Customer Journey Analytics.
Voorbeelden van identiteiten kunnen een klant-id, account-id of e-mailadres zijn. Ongeacht de identiteit (en er kunnen meerdere zijn), moet u rekening houden met het volgende voor elke id:

* Id bestaat of kan worden toegevoegd aan alle gegevensbronnen die u naar Customer Journey Analytics wilt verzenden
* ID is gevuld op elke rij gegevens
* ID bevat geen PII. Pas hashing op om het even wat toe die gevoelig zou kunnen zijn.
* ID gebruikt dezelfde indeling voor alle bronnen (dezelfde lengte, dezelfde hash-methode, enz.)

In datasets zoals Adobe Analytics, kan een identiteit niet op elke rij van gegevens bestaan, maar een secundaire identiteit. In dit geval, {de Analyse van het Kanaal 0} (die ook als &quot;Stitching&quot;wordt bekend) [&#128279;](/help/stitching/overview.md) kan worden gebruikt om het hiaat tussen rijen te overbruggen wanneer een klant slechts door hun ECID wordt geïdentificeerd en wanneer een identiteit wordt verzameld (bijvoorbeeld, wanneer een klant voor authentiek verklaart).

### Variabelen uitlijnen

De meest ongecompliceerde methode om de gegevens van Adobe Analytics in Customer Journey Analytics om te zetten is a [ globale rapportreeks ](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html?lang=nl-NL) in Experience Platform in te voeren gebruikend de [ Schakelaar van Source van de Analytics ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=nl-NL). Deze schakelaar brengt uw variabelen van Adobe Analytics rechtstreeks aan een XDM schema en dataset in Experience Platform in kaart, die beurtelings gemakkelijk met Customer Journey Analytics kunnen worden verbonden.

Een volledige algemene rapportenreeks is mogelijk niet altijd uitvoerbaar voor een implementatie. Als u meerdere rapportsuites wilt overbrengen naar Customer Journey Analytics, hebt u twee opties:

* Plan vooruit om variabelen over die rapportreeksen in overeenstemming te brengen. EVar1 in rapportsuite 1 verwijst bijvoorbeeld mogelijk naar [!UICONTROL Page] . In rapportsuite 2 verwijst eVar1 mogelijk naar [!UICONTROL Internal Campaign] . Als deze variabelen in Customer Journey Analytics worden opgenomen, zullen ze zich in één eVar1-dimensie mengen, wat kan leiden tot verwarrende en onjuiste rapportage.

* Gebruik de [ Prep van Gegevens ](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html?lang=nl-NL) eigenschap aan kaartvariabelen. Terwijl het het gemakkelijker maakt als alle rapportsuites het zelfde gemeenschappelijke veranderlijke ontwerp gebruiken, is het niet vereist als u de nieuwe eigenschap van de Prep van de Gegevens van Experience Platform [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=nl-NL#mapping) gebruikt. Hiermee kunt u naar een variabele verwijzen op basis van de toegewezen waarde, die zich op het niveau van de gegevensstroom (of eigenschap) bevindt.

Als u zich aan een globale rapportreeks wegens kwesties met [!UICONTROL Uniques Exceeded] of [!UICONTROL Low Traffic] hebt vermeden, weet dat Customer Journey Analytics geen [ kardinaliteitsgrenzen op een dimensie ](/help/components/dimensions/high-cardinality.md) heeft. Hiermee kan elke unieke waarde worden weergegeven en geteld.

Hier is een gebruiksgeval op [ combinerend rapportreeksen met verschillende schema&#39;s ](/help/use-cases/aa-data/combine-report-suites.md).

### (Opnieuw)Uw marketingkanalen configureren

De traditionele Adobe Analytics Marketing Channel-instellingen werken niet op dezelfde manier in Customer Journey Analytics. Dit is om twee redenen:

* het verwerkingsniveau op de Adobe Analytics-gegevens die in Adobe Experience Platform worden ingevoerd, en

* De rapporttijd van Customer Journey Analytics

Adobe heeft [ bijgewerkte beste praktijken voor de implementatie van het Kanaal van de Marketing ](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/mchannel-best-practices.html?lang=nl-NL) gepubliceerd. Deze bijgewerkte aanbevelingen helpen u de mogelijkheden die Adobe Analytics al met Attribution IQ heeft, optimaal te benutten. Ze zullen u ook instellen voor succes bij de overgang naar Customer Journey Analytics.

Met de introductie van [ Voortgekomen gebieden ](../data-views/derived-fields/derived-fields.md) als deel van de meningen van Gegevens van Customer Journey Analytics, worden de Marketing Kanalen ook gesteund op een niet-destructieve en retro-actieve manier gebruikend het [ de functiesjabloon van het Kanaal van de Marketing ](../data-views/derived-fields/derived-fields.md#function-templates).

## Voorbereiden op belangrijke verschillen bij het migreren naar Customer Journey Analytics

Naarmate uw organisatie zich ontwikkelt om Customer Journey Analytics te gebruiken, verkent u deze stappen om uw gegevens voor te bereiden en om inzicht te krijgen in de kritieke verschillen tussen de twee technologieën. Dit artikel is gericht op een beheerdersgroep.

### Geniet van gemak met rapportverwerking {#report-time}

De rapportage in Adobe Analytics is afhankelijk van een aanzienlijke hoeveelheid gegevens die vooraf wordt verwerkt om resultaten te genereren zoals de persistentie die u in [!UICONTROL eVars] ziet. Customer Journey Analytics voert deze berekeningen daarentegen uit tijdens de uitvoering van het rapport.

[!UICONTROL Report time processing] opent de mogelijkheid om instellingen toe te passen die retroactief zijn en om meerdere versies van variabele persistentie te maken zonder dat het nodig is om te wijzigen hoe de onderliggende gegevens worden verzameld.

Deze verschuiving resulteert in enkele verschillen in de manier waarop gegevens worden gerapporteerd, met name voor variabelen die een lang verloopvenster kunnen hebben. U kunt beginnen door te evalueren hoe rapport-tijd verwerking uw het melden kan beïnvloeden gebruikend a [ virtuele rapportreeks ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=nl-NL).

### Identificeer kritieke Segmenten en Berekende Metriek {#segments-calcmetrics}

Adobe Analytics-segmenten en berekende maatstaven zijn niet compatibel met Customer Journey Analytics. In veel gevallen kunnen deze componenten opnieuw worden samengesteld in Customer Journey Analytics met behulp van de nieuwe schema&#39;s en beschikbare gegevens.

Als u de overgang zo soepel mogelijk wilt laten verlopen voor gebruikers die een overgang maken tussen de systemen, kunt u

1. De meest kritieke onderdelen van deze componenten identificeren.

2. hun definities te documenteren, en

3. Identificerend welke gebieden in de gegevens zullen worden vereist om hen in Customer Journey Analytics als [ Segmenten ](/help/components/segments/seg-overview.md) en [ Berekende Metriek ](/help/components/calc-metrics/calc-metr-overview.md) te herhalen.

Hieronder volgen enkele video&#39;s die u moeten begeleiden:

* [ de segmenten van Adobe Analytics van de beweging aan Customer Journey Analytics ](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/moving-adobe-analytics-segments-to-customer-journey-analytics.html?lang=nl-NL)

* [ Beweeg uw Berekende Metriek van Adobe Analytics aan Customer Journey Analytics ](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/components/calc-metrics/moving-your-calculated-metrics-from-adobe-analytics-to-customer-journey-analytics.html?lang=nl-NL)

### Andere overwegingen

* Met de kracht van Customer Journey Analytics-gegevensweergaven beschikt u over veel meer flexibiliteit bij het definiëren van maateenheden en dimensies in Customer Journey Analytics. U kunt bijvoorbeeld de waarde van een dimensie gebruiken om een metrische definitie te worden. [Meer informatie](/help/use-cases/data-views/data-views-usecases.md)

* Als u een douanekalender in Adobe Analytics hebt bepaald, zult u gelijkaardige [ mogelijkheden van de douanekalender ](/help/components/date-ranges/overview.md) binnen Customer Journey Analytics hebben. U moet ervoor zorgen dat uw kalender correct wordt bepaald.

* In Customer Journey Analytics kunt u een aangepaste time-out voor een bezoek/sessie definiëren en een metrische waarde definiëren waarmee een nieuwe sessie wordt gestart. U kunt gegevensweergaven maken met verschillende sessiedefinities om meer inzicht te krijgen dan in Adobe Analytics mogelijk was. Dit vermogen kan bijzonder gunstig zijn voor mobiele datasets.

* U kunt overwegen een gegevenswoordenboek voor uw gebruikers op te geven of de SDR uit te breiden met de Experience Platform-veldnaam voor schema-elementen.

### Volgende stappen

Nadat u naar Customer Journey Analytics bent gegaan, kunt u uw oorspronkelijke Adobe Analytics-gegevens vergelijken met de Adobe Analytics-gegevens die zich nu in Customer Journey Analytics bevinden. [Meer informatie](/help/troubleshooting/compare.md)
