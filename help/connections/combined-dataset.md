---
title: Gecombineerde gegevenssets voor gebeurtenissen
description: Leer hoe CJA tot een verbinding leidt door datasets te combineren.
translation-type: tm+mt
source-git-commit: ef05a948cb2036db24c8e308695e3615613d98d8
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# Gecombineerde gegevenssets voor gebeurtenissen

Wanneer u een verbinding creeert, combineert CJA alle schema&#39;s en datasets in één enkele dataset. Dit &quot;gecombineerde gebeurtenisdataset&quot;is wat CJA voor rapportering gebruikt. Wanneer u veelvoudige schema&#39;s of datasets in een verbinding omvat:

* Schema&#39;s worden gecombineerd. Dubbele schemavelden worden samengevoegd.
* De kolom &#39;Person ID&#39; van elke dataset wordt samengevoegd in één kolom, ongeacht de naam ervan. Deze kolom vormt de basis voor het identificeren van unieke bezoekers in CJA.
* Rijen worden verwerkt op basis van een tijdstempel.

## Voorbeeld

Neem het volgende voorbeeld. U hebt twee gebeurtenisdatasets, elk met verschillende gebieden die verschillende gegevens bevatten.

>[!NOTE]
>
>Adobe Experience Platform slaat de tijdstempel doorgaans op in Unix milliseconden. Voor leesbaarheid in dit voorbeeld worden datum en tijd gebruikt.

| `example_id` | `timestamp` | `string_color` | `string_animal` | `metric_a` |
| --- | --- | --- | --- | --- |
| `user_310` | `1 Jan 7:02 AM` | `Red` | `Fox` |  |
| `user_310` | `1 Jan 7:04 AM` |  |  | `2` |
| `user_310` | `1 Jan 7:08 AM` | `Blue` |  | `3` |
| `user_847` | `2 Jan 12:31 PM` |  | `Turtle` | `4` |
| `user_847` | `2 Jan 12:44 PM` |  |  | `2` |

| `different_id` | `timestamp` | `string_color` | `string_shape` | `metric_b` |
| --- | --- | --- | --- | --- |
| `user_847` | `2 Jan 12:26 PM` | `Yellow` | `Circle` | `8.5` |
| `user_847` | `2 Jan 1:01 PM` | `Red` |  |  |
| `alternateid_656` | `2 Jan 8:58 PM` | `Red` | `Square` | `4.2` |
| `alternateid_656` | `2 Jan 9:03 PM` |  | `Triangle` | `3.1` |

Wanneer u een verbinding gebruikend deze twee gebeurtenisdatasets creeert, wordt de volgende lijst gebruikt voor het melden.

| `id` | `timestamp` | `string_color` | `string_animal` | `string_shape` | `metric_a` | `metric_b` |
| --- | --- | --- | --- | --- | --- | --- |
| `user_310` | `1 Jan 7:02 AM` | `Red` | `Fox` |  |  |  |
| `user_310` | `1 Jan 7:04 AM` |  |  |  | `2` |  |
| `user_310` | `1 Jan 7:08 AM` | `Blue` |  |  | `3` |  |
| `user_847` | `2 Jan 12:26 PM` | `Yellow` |  | `Circle` |  | `8.5` |
| `user_847` | `2 Jan 12:31 PM` |  | `Turtle` |  | `4` |  |
| `user_847` | `2 Jan 12:44 PM` |  |  |  | `2` |  |
| `user_847` | `2 Jan 1:01 PM` | `Red` |  |  |  |  |
| `alternateid_656` | `2 Jan 8:58 PM` | `Red` |  | `Square` |  | `4.2` |
| `alternateid_656` | `2 Jan 9:03 PM` |  |  | `Triangle` |  | `3.1` |

Deze gecombineerde gebeurtenisdataset is wat in het melden wordt gebruikt. Het maakt niet uit van welke gegevensset een rij afkomstig is; CJA behandelt alle gegevens alsof het in de zelfde dataset is. Als een overeenkomende persoon-id in beide gegevenssets wordt weergegeven, worden deze beschouwd als dezelfde unieke bezoeker. Als een overeenkomende persoon-id binnen 30 minuten in beide gegevenssets wordt weergegeven met een tijdstempel, wordt deze beschouwd als onderdeel van dezelfde sessie.

Dit concept is ook van toepassing op attributie. Het maakt niet uit van welke gegevensset een rij afkomstig is; attributie werkt precies alsof alle gebeurtenissen uit één dataset kwamen. De bovenstaande tabellen als voorbeeld gebruiken:

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
