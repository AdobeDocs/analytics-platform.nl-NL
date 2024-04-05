---
title: Afmetingen van hoge kardinaliteit
description: Verklaart hoe de Customer Journey Analytics dimensies met vele unieke waarden behandelt
feature: Dimensions
solution: Customer Journey Analytics
exl-id: 17b275a5-c2c2-48ee-b663-e7fe76f79456
role: User
source-git-commit: aaab21ef817e3acf67ca83cb6f9258b812625c8e
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Afmetingen van hoge kardinaliteit

Wanneer het gebruiken van een afmeting die vele unieke waarden bevat, kan het resulterende rapport teveel unieke afmetingspunten bevatten om te tonen of te berekenen. Resultaten worden afgekapt door dimensiepunten te verwijderen die als minst belangrijk worden beschouwd. Deze optimalisaties worden uitgevoerd om de project- en productprestaties te behouden.

Wanneer u om een rapport met teveel unieke waarden verzoekt, toont Analysis Workspace een indicator in de afmetingskopbal die verklaart dat niet alle afmetingspunten inbegrepen zijn. Bijvoorbeeld &quot;Rijen: 1-50 van meer dan 22.343.156&quot;. Het &quot;meer dan&quot;sleutelwoord wijst erop dat één of andere optimalisering werd toegepast op het rapport om de belangrijkste afmetingspunten terug te keren.

![Vrije-vormtabel in Workspace met het trefwoord &quot;Meer dan&quot; om 1-50 van meer dan 22.343.156 weer te geven](assets/high-cardinality.png)

## Bepalen welke dimensie-items moeten worden weergegeven

De processen van de Customer Journey Analytics rapporten in de tijd dat zij in werking worden gesteld, die de gecombineerde dataset aan verscheidene servers verdelen. Gegevens per verwerkingsserver worden gegroepeerd op persoon-id, wat betekent dat één verwerkingsserver alle gegevens voor een bepaalde persoon bevat. Zodra een server klaar is met de verwerking, stuurt deze de subset verwerkte gegevens door naar een aggregatorserver. Alle subsets van verwerkte gegevens worden gecombineerd en geretourneerd in de vorm van een Workspace-rapport.

Als om het even welke individuele server gegevens verwerkt die een unieke drempel overschrijden, beknotten het de resultaten alvorens de verwerkte ondergroep van gegevens terug te keren. Afgeknot dimensieitems worden bepaald op basis van de metrische waarde die wordt gebruikt voor sorteren.

Als het sorteren metrisch berekende metrisch is, gebruikt de server de metriek binnen berekende metrisch om te bepalen welke afmetingspunten om te beknotten. Aangezien berekende metriek verschillende metriek van verschillend belang kan bevatten, kunnen de resultaten minder nauwkeurig zijn. Bij de berekening van &quot;Ontvangsten per persoon&quot; worden bijvoorbeeld het totale bedrag aan inkomsten en het totale aantal personen geretourneerd en geaggregeerd voordat de splitsing wordt uitgevoerd. Dientengevolge, kiest elke individuele verwerkingsserver welke punten om te verwijderen zonder het weten hoe hun resultaten het algemene sorteren beïnvloeden.

Hoewel sommige individuele afmetingspunten in hoge kardinaliteitsrapporten zouden kunnen ontbreken, zijn de kolomtotalen nauwkeurig en niet gebaseerd op afgekapte gegevens. De functie &#39;Afzonderlijk tellen&#39; in berekende metriek wordt ook niet beïnvloed door afgekapte dimensie-items.

## Aanbevolen werkwijzen voor afmetingen met een hoge cardinaliteit

De beste manier om hoge kardinaliteitsdimensies aan te passen is het aantal afmetingspunten te beperken dat een rapport verwerkt. Aangezien alle rapporten op het tijdstip worden verwerkt dat zij worden gevraagd, kunt u rapportparameters voor directe resultaten aanpassen. Adobe raadt een van de volgende optimalisaties aan voor afmetingen met een hoge cardinaliteit:

* Een [Filter](/help/components/filters/create-filters.md). Filters worden toegepast op het moment dat elke server een subset van gegevens verwerkt.
* Gebruik een zoekopdracht. De punten van het Dimension die van de onderzoekstermijn worden uitgesloten worden verwijderd uit de rapportresultaten, die het waarschijnlijker maken dat u de gewenste afmetingspunten ziet.
* Gebruik een dimensie van de raadplegingsdataset. De dimensies van de dataset van de opzoekopdracht combineren de dimensies van de gebeurtenisdataset, die het aantal unieke teruggekeerde waarden beperken.
* Gebruik de [Opnemen/uitsluiten](/help/data-views/component-settings/include-exclude-values.md) in het gegevensweergavebeheer.
* Verkort het datumbereik van de aanvraag. Als er zich na verloop van tijd veel unieke waarden ophopen, kan het verkorten van het datumbereik van het Workspace-rapport het aantal unieke waarden voor servers dat moet worden verwerkt, beperken.
* Gebruik [Volledige tabelexport](/help/analysis-workspace/export/export-cloud.md) om alle rijen van de tabel te retourneren.
