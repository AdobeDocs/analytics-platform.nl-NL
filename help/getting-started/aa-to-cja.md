---
title: Evolutie uit Adobe Analytics
description: Stappen om Adobe Analytics-gegevens om te zetten in Customer Journey Analytics-gegevens
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 5e3f0aa0-ba24-48c8-948c-ebb5c270f34d
source-git-commit: 46d799ad2621d83906908a3f60a59a1027c6518c
workflow-type: tm+mt
source-wordcount: '1431'
ht-degree: 0%

---

# Evolutie uit Adobe Analytics

Naarmate uw organisatie evolueert naar het gebruik van Customer Journey Analytics, verkent u deze stappen om uw gegevens voor te bereiden en bewust te worden van de kritieke verschillen tussen de twee technologieën. Dit artikel is gericht op een beheerdersgroep.

## Uw gegevens voorbereiden

Het voorbereiden van uw Adobe Analytics-gegevens voor een naadloze overgang naar de Customer Journey Analytics is van essentieel belang voor de gegevensintegriteit en de consistentie van de rapportage.

### 1. Identiteiten verzamelen {#identities}

Misschien de meest kritieke component van het begrip van een klantenreis is het weten van wie de klant bij elke stap is. Voor Customer Journey Analytics, staat het hebben van een herkenningsteken dat over al uw kanalen en de overeenkomstige gegevens bestaat voor het verbinden van veelvoudige bronnen samen binnen Customer Journey Analytics toe.
Voorbeelden van identiteiten kunnen een klant-id, account-id of e-mailadres zijn. Ongeacht de identiteit (en er kunnen meerdere zijn), moet u rekening houden met het volgende voor elke id:

* ID bestaat of kan aan alle gegevensbronnen worden toegevoegd u in Customer Journey Analytics wilt brengen
* ID is gevuld op elke rij gegevens
* ID bevat geen PII. Pas hashing op om het even wat toe die gevoelig zou kunnen zijn.
* ID gebruikt dezelfde indeling voor alle bronnen (dezelfde lengte, dezelfde hash-methode, enz.)

In datasets zoals Adobe Analytics, kan een identiteit niet op elke rij van gegevens bestaan, maar een secundaire identiteit. In dit geval, kan de Analyse van het Kanaal (die ook als &quot;Stitching&quot;wordt bekend) worden gebruikt om het hiaat tussen rijen te overbruggen wanneer een klant slechts door hun ECID wordt geïdentificeerd en wanneer een identiteit wordt verzameld (bijvoorbeeld, wanneer een klant voor authentiek verklaart). [Meer informatie](../stitching/overview.md).

### 2. Lijn de variabelen uit {#variables}

De eenvoudigste manier om Adobe Analytics-gegevens om te zetten in Customer Journey Analytics-gegevens is om een [algemene rapportsuite](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html) in Experience Platform met de [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html). Deze schakelaar brengt uw variabelen van Adobe Analytics rechtstreeks aan een schema XDM en dataset in Experience Platform in kaart, die beurtelings gemakkelijk met Customer Journey Analytics kunnen worden verbonden.

Een volledige algemene rapportenreeks is mogelijk niet altijd uitvoerbaar voor een implementatie. Als u van plan bent om veelvoudige rapportsuites in Customer Journey Analytics te brengen, hebt u twee opties:

* Plan vooruit om variabelen over die rapportreeksen in overeenstemming te brengen. EVar1 in rapportsuite 1 verwijst bijvoorbeeld naar [!UICONTROL Page]. In rapportsuite 2 kan eVar1 verwijzen naar [!UICONTROL Internal Campaign]. Wanneer deze variabelen in de Customer Journey Analytics worden gebracht, zullen ze zich in één enkele dimensie eVar1 mengen, wat tot potentieel verwarrende en onnauwkeurige rapportering zal leiden.

* Gebruik de [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) functie voor het toewijzen van variabelen. Terwijl het het gemakkelijker maakt als alle rapportsuites het zelfde gemeenschappelijke veranderlijke ontwerp gebruiken, is het niet vereist als u het nieuwe Experience Platform gebruikt [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html#mapping) gebruiken. Hiermee kunt u naar een variabele verwijzen op basis van de toegewezen waarde, die zich op het niveau van de gegevensstroom (of eigenschap) bevindt.

Als u niet naar een algemene rapportsuite bent gegaan vanwege problemen met [!UICONTROL Uniques Exceeded] of [!UICONTROL Low Traffic], weet dat Customer Journey Analytics geen [kardinaliteitsbeperkingen voor een dimensie](/help/components/dimensions/high-cardinality.md). Hiermee kan elke unieke waarde worden weergegeven en geteld.

Hier is een gebruiksgeval ingeschakeld [het combineren van rapportsuites met verschillende schema&#39;s](/help/use-cases/aa-data/combine-report-suites.md).

### 3. (Opnieuw)Uw marketingkanalen configureren {#marketing-channels}

De traditionele Adobe Analytics Marketing Channel-instellingen voeren niet hetzelfde uit in de Customer Journey Analytics. Dit is om twee redenen:

* het verwerkingsniveau op de Adobe Analytics-gegevens die in Adobe Experience Platform worden ingevoerd, en

* De aard van de Customer Journey Analytics tijdens de verslagperiode

Adobe is gepubliceerd [bijgewerkte best practices voor implementatie van marketingkanalen](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/mchannel-best-practices.html). Met deze bijgewerkte aanbevelingen kunt u optimaal gebruikmaken van de mogelijkheden die Adobe Analytics al met Attribution IQ heeft. Zij zullen u ook voor succes bij overgang aan Customer Journey Analytics oprichten.

Met de invoering van [Afgeleide velden](../data-views/derived-fields/derived-fields.md) als deel van de meningen van de Gegevens van de Customer Journey Analytics, worden de Kanalen van de Marketing ook gesteund op een niet-destructieve en retro-actieve manier gebruikend [Sjabloon voor marketingkanaalfunctie](../data-views/derived-fields/derived-fields.md#function-templates).

### 4. Beslissen over het gebruik van de bronconnector van Analytics versus SDK&#39;s van Experience Platforms {#connector-vs-sdk}

Adobe Analytics-klanten kunnen hun rapportsuites eenvoudig benutten in de Adobe Experience Platform en de Customer Journey Analytics met behulp van de Analytics-bronconnector. Voor informatie bij het gebruiken van de de bronschakelaar van de Analyse, zie de snelle startgids over hoe te [Gegevens uit Adobe Analytics innemen en gebruiken in Customer Journey Analytics](../data-ingestion/analytics.md). Zie ook [Een Adobe Analytics-bronverbinding maken in de gebruikersinterface](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) voor meer informatie .

Adobe biedt ook de mogelijkheid om gegevensverzameling te implementeren met behulp van de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/web-sdk.html) of [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/mobile.html). Met deze methoden worden de mogelijkheden voor gegevensverzameling aanzienlijk vergroot. Er geldt niet langer een beperking op het aantal velden of de noodzaak om gegevenselementen toe te wijzen aan props, eVars en gebeurtenissen zoals in Analytics. U kunt onbeperkte schemaelementen van verschillende types gebruiken en hen vertegenwoordigen op veelvoudige manieren gebruikend Customer Journey Analytics [Gegevens weergeven](/help/data-views/data-views.md). De beschikbaarheid van gegevens neemt toe wanneer deze rechtstreeks naar Adobe Experience Platform worden verzonden, omdat de tijd voor gegevensverwerking via Adobe Analytics wordt verwijderd.

**Voordelen van het gebruik van Experience Platform-SDK&#39;s:**

* Flexibel schema voor het definiëren van velden die u nodig hebt
* Niet afhankelijk van Adobe Analytics-nomenclatuur (profiel, eVar, gebeurtenis, enz.)
* Geen tekenlimiet (100 tekens voor props)
* Snellere beschikbaarheid van gegevens in Adobe Experience Platform [Gebruiksgevallen voor realtime personalisatie](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)
* [Apparaat-id&#39;s van eerste partij](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/first-party-device-ids.html) voor een grotere nauwkeurigheid van de identificatie van de bezoeker

**Drawbacks aan het gebruiken van Experience Platform SDKs**

De volgende Adobe Analytics-functies of -componenten worden niet ondersteund:

* Bot filteren
* Metingen voor streamingmedia
* Livestream- of Livestream-triggers

### 5. Kaart projecten en onderdelen van Adobe Analytics aan Customer Journey Analytics

Adobe Analytics-beheerders kunnen Adobe Analytics-projecten en de bijbehorende onderdelen migreren naar Customer Journey Analytics.

Het migratieproces omvat:

* Adobe Analytics-projecten opnieuw maken in Customer Journey Analytics.

* De dimensies en metriek van de afbeelding van Adobe Analytics melden reeksen aan dimensies en metriek in de mening van de gegevens van de Customer Journey Analytics.

Voordat u met de migratie begint, moet u eerst [Migratie van onderdelen en projecten van Adobe Analytics naar Customer Journey Analytics voorbereiden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration.html).

Nadat u alle benodigde voorbereidingen hebt getroffen, kunt u [Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/component-migration.html).

## Voorbereiden op kritieke verschillen

### Geniet van gemak met rapportverwerking {#report-time}

De rapportage in Adobe Analytics is afhankelijk van een aanzienlijke hoeveelheid gegevens die vooraf wordt verwerkt om resultaten te genereren zoals de persistentie die u in [!UICONTROL eVars]. Customer Journey Analytics voert deze berekeningen daarentegen uit tijdens de uitvoering van het rapport.

[!UICONTROL Report time processing] Hiermee opent u de mogelijkheid om instellingen met terugwerkende kracht toe te passen en meerdere versies van variabele persistentie te maken zonder dat u hoeft te wijzigen hoe de onderliggende gegevens worden verzameld.

Deze verschuiving resulteert in enkele verschillen in de manier waarop gegevens worden gerapporteerd, met name voor variabelen die een lang verloopvenster kunnen hebben. U kunt beginnen door te evalueren hoe de rapport-tijd verwerking uw rapportering kan beïnvloeden gebruikend [virtuele rapportsuite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html).

### Identificeer kritieke Segmenten en Berekende Metriek {#segments-calcmetrics}

Adobe Analytics-segmenten (opgeroepen [!UICONTROL filters] in Customer Journey Analytics) en berekende meetwaarden zijn niet compatibel met Customer Journey Analytics. In veel gevallen, kunnen deze componenten in Customer Journey Analytics worden herbouwd gebruikend de nieuwe schema&#39;s en beschikbare gegevens.

Als u de overgang zo soepel mogelijk wilt laten verlopen voor gebruikers die een overgang maken tussen de systemen, kunt u

1. De meest kritieke onderdelen van deze componenten identificeren.

2. hun definities te documenteren, en

3. Bepalen welke velden in de gegevens moeten worden opgenomen om deze in Customer Journey Analytics te repliceren als [Filters](/help/components/filters/filters-overview.md) en [Berekende cijfers](/help/components/calc-metrics/calc-metr-overview.md).

Hieronder volgen enkele video&#39;s die u moeten begeleiden:

* [Adobe Analytics-segmenten naar Customer Journey Analytics verplaatsen](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/moving-adobe-analytics-segments-to-customer-journey-analytics.html)

* [Je berekende cijfers van Adobe Analytics naar Customer Journey Analytics verplaatsen](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/components/calc-metrics/moving-your-calculated-metrics-from-adobe-analytics-to-customer-journey-analytics.html)

### Andere overwegingen

* Gebruikend de macht van de gegevensmeningen van de Customer Journey Analytics, hebt u veel meer flexibiliteit in de definitie van metriek en dimensies binnen Customer Journey Analytics. U kunt bijvoorbeeld de waarde van een dimensie gebruiken om een metrische definitie te worden. [Meer informatie](/help/use-cases/data-views/data-views-usecases.md)

* Als u een aangepaste kalender hebt gedefinieerd in Adobe Analytics, hebt u een vergelijkbare kalender [aangepaste kalendermogelijkheden](/help/components/date-ranges/custom-date-ranges.md) binnen de Customer Journey Analytics. U moet ervoor zorgen dat uw kalender correct wordt bepaald.

* In Customer Journey Analytics, kunt u een douanebezoek/zittingsonderbreking bepalen evenals metrisch bepalen die een nieuwe zitting zal beginnen. U kunt gegevensweergaven maken met verschillende sessiedefinities om meer inzicht te krijgen dan in Adobe Analytics mogelijk was. Dit vermogen kan bijzonder gunstig zijn voor mobiele datasets.

* U kunt overwegen een gegevenswoordenboek voor uw gebruikers op te geven - of de SDR uit te breiden met de veldnaam van het Experience Platform voor schema-elementen.

## Volgende stappen

Als u na de overgang naar de Customer Journey Analytics enige gegevensdiscrepantie opmerkt, kunt u de oorspronkelijke Adobe Analytics-gegevens vergelijken met de Adobe Analytics-gegevens die nu in Customer Journey Analytics zijn. [Meer informatie](/help/troubleshooting/compare.md)
