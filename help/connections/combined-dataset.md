---
title: Gecombineerde gegevenssets voor gebeurtenissen
description: Leer hoe de Customer Journey Analytics tot een verbinding leidt door datasets te combineren.
exl-id: 9f678225-a9f3-4134-be38-924b8de8d57f
solution: Customer Journey Analytics
feature: Connections
role: Admin
source-git-commit: 80d5a864e063911b46ff248f2ea89c1ed0d14e32
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 1%

---


# Gecombineerde gegevenssets voor gebeurtenissen

Wanneer u een verbinding creeert, combineert de Customer Journey Analytics alle schema&#39;s en datasets in één enkele dataset. Deze &#39;gecombineerde gebeurtenissendataset&#39; is wat de Customer Journey Analytics gebruikt voor rapportage. Wanneer u veelvoudige schema&#39;s of datasets in een verbinding omvat:

* Schema&#39;s worden gecombineerd. Dubbele schemavelden worden samengevoegd.
* De kolom &#39;Person ID&#39; van elke dataset wordt samengevoegd in één kolom, ongeacht de naam ervan. Deze kolom vormt de basis voor het identificeren van unieke personen in Customer Journey Analytics.
* Rijen worden verwerkt op basis van een tijdstempel.
* Gebeurtenissen worden tot op het millisecondenniveau opgelost.

## Voorbeeld

Kijk eens naar het volgende voorbeeld. U hebt twee gebeurtenisdatasets, elk met verschillende gebieden die verschillende gegevens bevatten.

>[!NOTE]
>
>Adobe Experience Platform slaat de tijdstempel doorgaans op in Unix milliseconden. Voor leesbaarheid in dit voorbeeld worden datum en tijd gebruikt.

| `example_id` | `timestamp` | `string_color` | `string_animal` | `metric_a` |
| --- | --- | --- | --- | --- |
| `user_310` | `1 Jan 7:02 AM` | `Red` | `Fox` | |
| `user_310` | `1 Jan 7:04 AM` | | | `2` |
| `user_310` | `1 Jan 7:08 AM` | `Blue` | | `3` |
| `user_847` | `2 Jan 12:31 PM` | | `Turtle` | `4` |
| `user_847` | `2 Jan 12:44 PM` | | | `2` |

| `different_id` | `timestamp` | `string_color` | `string_shape` | `metric_b` |
| --- | --- | --- | --- | --- |
| `user_847` | `2 Jan 12:26 PM` | `Yellow` | `Circle` | `8.5` |
| `user_847` | `2 Jan 1:01 PM` | `Red` | | |
| `alternateid_656` | `2 Jan 8:58 PM` | `Red` | `Square` | `4.2` |
| `alternateid_656` | `2 Jan 9:03 PM` | | `Triangle` | `3.1` |

Wanneer u een verbinding gebruikend deze twee gebeurtenisdatasets creeert, wordt de volgende lijst gebruikt voor het melden.

| `id` | `timestamp` | `string_color` | `string_animal` | `string_shape` | `metric_a` | `metric_b` |
| --- | --- | --- | --- | --- | --- | --- |
| `user_310` | `1 Jan 7:02 AM` | `Red` | `Fox` | | | |
| `user_310` | `1 Jan 7:04 AM` | | | | `2` | |
| `user_310` | `1 Jan 7:08 AM` | `Blue` | | | `3` | |
| `user_847` | `2 Jan 12:26 PM` | `Yellow` | | `Circle` | | `8.5` |
| `user_847` | `2 Jan 12:31 PM` | | `Turtle` | | `4` | |
| `user_847` | `2 Jan 12:44 PM` | | | | `2` | |
| `user_847` | `2 Jan 1:01 PM` | `Red` | | | | |
| `alternateid_656` | `2 Jan 8:58 PM` | `Red` | | `Square` | | `4.2` |
| `alternateid_656` | `2 Jan 9:03 PM` | | | `Triangle` | | `3.1` |

Deze gecombineerde gebeurtenisdataset is wat in het melden wordt gebruikt. Het maakt niet uit van welke dataset een rij afkomstig is; de Customer Journey Analytics behandelt alle gegevens alsof het in de zelfde dataset is. Als een overeenkomende persoon-id in beide gegevenssets wordt weergegeven, worden deze als dezelfde unieke persoon beschouwd. Als een overeenkomende persoon-id binnen 30 minuten in beide gegevenssets wordt weergegeven met een tijdstempel, wordt deze beschouwd als onderdeel van dezelfde sessie.

Dit concept is ook van toepassing op attributie. Het maakt niet uit van welke dataset een rij afkomstig is; de attributie werkt precies alsof alle gebeurtenissen uit één dataset kwamen. De bovenstaande tabellen als voorbeeld gebruiken:

Als uw verbinding slechts de eerste lijst en niet de tweede omvatte, trekkend een rapport gebruikend `string_color` dimensie en `metric_a` Metrisch met laatste aanraakkenmerk geeft het volgende weer:

| string_color | metrisch_a |
| --- | --- |
| Niet opgegeven | 6 |
| Blauw | 3 |
| Rood | 2 |

Als u echter beide tabellen hebt opgenomen in uw verbinding, verandert de toewijzing sinds `user_847` bevindt zich in beide gegevenssets. Een rij van de tweede dataset attributen `metric_a` op &#39;Geel&#39; waar ze voorheen niet waren gespecificeerd:

| string_color | metrisch_a |
| --- | --- |
| Geel | 6 |
| Blauw | 3 |
| Rood | 2 |

## Kanaaloverschrijdende analyse

Het volgende niveau van het combineren van datasets is kanaalanalyse, waar datasets van verschillende kanalen worden gecombineerd, die op een gemeenschappelijke herkenningsteken (persoon ID) wordt gebaseerd. De analyse over kanalen kan van het stitching functionaliteit profiteren, die u toestaat om de de persoonsidentiteitskaart van een dataset opnieuw te bepalen zodat wordt de dataset behoorlijk bijgewerkt om een naadloze combinatie veelvoudige datasets toe te laten. Bij het zoeken naar gebruikersgegevens van zowel geverifieerde als niet-geverifieerde sessies wordt een aangesloten id gegenereerd.

Met de kanaalanalyse kunt u vragen beantwoorden zoals:

* Hoeveel mensen beginnen met hun ervaring in één kanaal, en eindigen het in een andere?
* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt de campagne klikdoorhalingen die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn begrip van campagnedoeltreffendheid als ik apparatuurreizen bekijk? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?


Raadpleeg het specifieke geval van gebruik voor meer informatie over kanaalanalyse:

* [Kanaaloverschrijdende analyse](../use-cases/cross-channel/cross-channel.md)

Ga voor een diepgaandere discussie over stitching-functionaliteit naar:

* [Overzicht van tekenreeksen](/help/stitching/overview.md)
* [Veelgestelde vragen](/help/stitching/faq.md)

