---
title: Afmetingen van hoge kardinaliteit
description: Verklaart hoe Customer Journey Analytics dimensies met vele unieke waarden behandelt.
feature: Dimensions
solution: Customer Journey Analytics
exl-id: 17b275a5-c2c2-48ee-b663-e7fe76f79456
role: User
source-git-commit: f350fd99187f6ce35042ad9d97d9d02b5f8d1721
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# Afmetingen van hoge kardinaliteit

Wanneer het gebruiken van een afmeting die vele unieke waarden bevat, kan het resulterende rapport teveel unieke afmetingspunten bevatten om te tonen of te berekenen. Resultaten worden afgekapt door dimensiepunten te verwijderen die als minst belangrijk worden beschouwd. Deze optimalisaties worden uitgevoerd om de project- en productprestaties te behouden.

Wanneer u om een rapport vraagt dat een dimensie met teveel unieke waarden bevat, toont Analysis Workspace een indicator in de afmetingskopbal die verklaart dat niet alle afmetingspunten inbegrepen zijn. Bijvoorbeeld **[!UICONTROL Rows: 1-50 of more than 22,343,156]** . Het trefwoord **[!UICONTROL more than]** geeft aan dat er enige optimalisatie is toegepast op het rapport om de belangrijkste dimensie-items te retourneren.

![&#x200B; de lijst van de Vrije vorm in Workspace die het &quot;meer dan&quot;sleutelwoord toont om 1-50 van meer dan 22.343.156 &#x200B;](assets/high-cardinality.png) te tonen

## Bepalen welke dimensie-items moeten worden weergegeven

Customer Journey Analytics verwerkt rapporten op het tijdstip dat zij in werking worden gesteld, die de gecombineerde dataset aan verscheidene servers verdelen. De grootte van het gegevensverzoek en de hoeveelheid beschikbare hardware van Adobe zijn twee van vele factoren die helpen het aantal servers bepalen die worden toegewezen om een rapport te verwerken. Aangezien de servers dynamisch worden toegewezen en niet zichtbaar in de interface, is er geen manier om het aantal servers te zien of te controleren die een rapport verwerken.

Gegevens per verwerkingsserver worden gegroepeerd op persoon-id, wat betekent dat één verwerkingsserver alle gegevens voor een bepaalde persoon bevat. Zodra een server klaar is met de verwerking, stuurt deze de subset verwerkte gegevens door naar een aggregatorserver. Alle subsets van verwerkte gegevens worden gecombineerd en geretourneerd in de vorm van een Workspace-rapport.

Als om het even welke individuele server gegevens verwerkt die een unieke drempel overschrijden, beknotten het de resultaten alvorens de verwerkte ondergroep van gegevens terug te keren. Afgeknot dimensieitems worden bepaald op basis van de metrische waarde die wordt gebruikt voor sorteren.

Als het sorteren metrisch berekende metrisch is, gebruikt de server de metriek binnen berekende metrisch om te bepalen welke afmetingspunten om te beknotten. Aangezien berekende metriek verschillende metriek van verschillend belang kan bevatten, kunnen de resultaten minder nauwkeurig zijn. Bij de berekening van &quot;Ontvangsten per persoon&quot; worden bijvoorbeeld het totale bedrag aan inkomsten en het totale aantal personen geretourneerd en geaggregeerd voordat de splitsing wordt uitgevoerd. Dientengevolge, kiest elke individuele verwerkingsserver welke punten om te verwijderen zonder het weten hoe hun resultaten het algemene sorteren beïnvloeden.

Hoewel sommige individuele afmetingspunten in hoge kardinaliteitsrapporten zouden kunnen ontbreken, zijn de kolomtotalen nauwkeurig en niet gebaseerd op afgekapte gegevens. De [[!UICONTROL Approximate Count Distinct]](/help/components/calc-metrics/cm-adv-functions.md#approximate-count-distinct) berekende metrische functie wordt ook niet beïnvloed door afgekapte afmetingspunten.

## Aanbevolen werkwijzen voor afmetingen met een hoge cardinaliteit

De beste manier om hoge kardinaliteitsdimensies aan te passen is het aantal afmetingspunten te beperken dat een rapport verwerkt. Aangezien alle rapporten op het tijdstip worden verwerkt dat zij worden gevraagd, kunt u rapportparameters voor directe resultaten aanpassen. Adobe raadt een van de volgende optimalisaties aan voor afmetingen met een hoge cardinaliteit:

* Gebruik a [&#x200B; segment &#x200B;](/help/components/segments/seg-create.md). Segmenten worden toegepast op het moment dat elke server een subset van gegevens verwerkt.
* Gebruik een zoekopdracht. Dimension-items die zijn uitgesloten van de zoekterm worden verwijderd uit de rapportresultaten, waardoor de kans groter is dat u de gewenste dimensie-items ziet.
* Gebruik een dimensie van de raadplegingsdataset. De dimensies van de dataset van de opzoekopdracht combineren de dimensies van de gebeurtenisdataset, die het aantal unieke teruggekeerde waarden beperken.
* Gebruik [&#x200B; omvatten/uitsluiten &#x200B;](/help/data-views/component-settings/include-exclude-values.md) component die in de manager van de gegevensmening plaatst.
* Verkort het datumbereik van de aanvraag. Als er zich in de loop der tijd veel unieke waarden ophopen, kan het verkorten van het datumbereik van het Workspace-rapport het aantal unieke waarden voor servers dat moet worden verwerkt, beperken.
* Overweeg het gebruiken van [&#x200B; Volledige Uitvoer van de Lijst &#x200B;](/help/analysis-workspace/export/export-cloud.md) om alle rijen van de lijst terug te keren.
* Wanneer het aantal unieke waarden de primaire focus is, gebruikt u de berekende metrische functie [[!UICONTROL Approximate Count Distinct]](/help/components/calc-metrics/cm-adv-functions.md#approximate-count-distinct) .
