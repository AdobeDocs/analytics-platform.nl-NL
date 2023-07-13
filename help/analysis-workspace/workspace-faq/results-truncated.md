---
title: Resultaten afgekapt dimensie-item
description: Verklaart de afmetingspost "Afgekort Resultaten"en waarom het in rapportering verschijnt.
feature: FAQ
exl-id: 262a219a-315a-4c9b-a400-48cff119d45d
source-git-commit: cf3c451cbefa7d6f9d5ea326c69fc2e5944881ff
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Resultaten afgekapt dimensie-item

Wanneer het gebruiken van een afmeting die vele unieke waarden bevat, kan een rapport een afmetingspunt etiketteren terugkeren **[!UICONTROL Results Truncated]**. Dit dimensiepunt betekent dat het gevraagde rapport te veel unieke waarden bevat om efficiënt te kunnen verwerken. Hierdoor worden de minst belangrijke items verwijderd.

## Customer Journey Analytics-verwerkingsarchitectuur en unieke waarden

Customer Journey Analytics verwerkt rapporten in de tijd dat zij in werking worden gesteld, die de gecombineerde dataset aan verscheidene servers verdelen. De gegevens per verwerkingsserver worden gegroepeerd door identiteitskaart van de Persoon, betekenend dat één enkele verwerkingsserver alle gegevens voor een bepaalde persoon bevat. Zodra de server klaar is met de verwerking, worden de verwerkte gegevens naar een aggregatorserver verzonden. Alle subsets van verwerkte gegevens worden gecombineerd en geretourneerd in de vorm van een Workspace-rapport.

Als een afzonderlijke server een resultaatset samenvoegt die groter is dan een formaatdrempel, worden de resultaten afgebroken voordat ze worden teruggestuurd. Deze optimalisering houdt het netwerkverkeer en de samenvoeging binnen grenzen om voor snelle rapportering toe te staan. Aangezien elke verwerkingsserver resultaten afkapt met alleen de weergave van zijn eigen gegevens, is het mogelijk dat de items die in Analysis Workspace worden weergegeven, metrische waarden hebben die iets weg zijn.

De server kiest welke afmetingspunten te verwerpen die op metrisch worden gebaseerd die voor het sorteren wordt gebruikt. Als het sorteren metrisch berekende metrisch is, gebruikt de server metriek binnen berekende metrisch om te bepalen welke afmetingspunten om te beknotten. Aangezien berekende metriek verschillende metriek van verschillend belang kan bevatten, kunnen de resultaten minder nauwkeurig zijn. Bij de berekening van &quot;Ontvangsten per persoon&quot; worden bijvoorbeeld het totale bedrag aan inkomsten en het totale aantal personen geretourneerd en geaggregeerd voordat de splitsing wordt uitgevoerd. Dientengevolge, kiest elke knoop welke punten te verwijderen zonder het weten hoe hun resultaten algemene sortering beïnvloeden.

## Verschillen tussen &#39;Results Truncated&#39; en &#39;Low-Traffic&#39;

In eerdere versies van Adobe Analytics werd een andere verwerkingsarchitectuur gebruikt. De gegevens werden verwerkt op het moment dat ze werden verzameld. De punten van Dimension werden geplaatst onder &quot;Laag-Verkeer&quot;nadat een afmeting 500.000 unieke waarden bereikte, en toepasten agressievere het filtreren bij één miljoen unieke waarden. Het aantal &quot;Unieke waarden&quot; is opnieuw ingesteld aan het begin van elke kalendermaand. de verwerkte gegevens permanent waren; Er was geen manier om bestaande gegevens uit &quot;Laag-Verkeer&quot; te halen.

In Customer Journey Analytics, zijn de afmetingspunten slechts afgekapt als de resultaten van een rapport te groot zijn. De verwerkte gegevens zijn niet permanent, wat betekent dat u de beknotting kunt verminderen of elimineren door uw rapport te wijzigen.

## Het afmetingsitem &#39;Results Truncated&#39; verkleinen

Als u het aantal gebeurtenissen in het afmetingsitem &#39;Results Truncated&#39; wilt verminderen, raadt Adobe aan een van de volgende handelingen uit te voeren:

* Een [Filter](/help/components/filters/create-filters.md). Filters worden toegepast op het moment dat elke server een subset gegevens verwerkt. Door het aantal unieke waarden dat ze retourneren te beperken, wordt het dimensiemenu &#39;Results Truncated&#39; kleiner.
* Gebruik een zoekopdracht. Als een zoekopdracht wordt gebruikt, worden de items die niet overeenkomen met de zoekopdracht uit de rapportresultaten verwijderd, waardoor de kans groter is dat u de gewenste items ziet.
* Gebruik een dimensie van de raadplegingsdataset. De dimensies van de dataset van de opzoekopdracht combineren de dimensies van de gebeurtenisdataset, die het aantal unieke teruggekeerde waarden beperken.
