---
title: Gecombineerde gegevenssets
description: Leer hoe CJA tot een verbinding leidt door datasets te combineren.
translation-type: tm+mt
source-git-commit: 2dab33dca173fcc0eab657b810e85e4740e5d7e0

---


# Gecombineerde gegevenssets

Wanneer u een verbinding creeert, combineert CJA alle schema&#39;s en datasets in één enkele dataset. Deze &quot;gecombineerde dataset&quot; is wat CJA gebruikt voor rapportage. Wanneer u veelvoudige schema&#39;s of datasets in een verbinding omvat:

* Schema&#39;s worden gecombineerd. Dubbele schemavelden worden samengevoegd.
* De kolom &#39;Person ID&#39; van elke dataset wordt samengevoegd in één kolom, ongeacht de naam ervan. Deze kolom vormt de basis voor het identificeren van unieke bezoekers in CJA.
* Rijen worden verwerkt op basis van een tijdstempel.

## Voorbeeld

Neem het volgende voorbeeld. U hebt twee datasets, elk met verschillende gebieden die verschillende gegevens bevatten.

>[!NOTE] In Adobe Experience Platform wordt de tijdstempel meestal opgeslagen in Unix milliseconden. Voor leesbaarheid in dit voorbeeld worden datum en tijd gebruikt.

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

Wanneer u een verbinding gebruikend deze twee datasets creeert, wordt de volgende lijst gebruikt voor het melden.

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

Deze gecombineerde dataset is wat in rapportering wordt gebruikt. Het maakt niet uit van welke gegevensset een rij afkomstig is; CJA behandelt alle gegevens alsof het in de zelfde dataset is. Als een overeenkomende persoon-id in beide gegevenssets wordt weergegeven, worden deze beschouwd als dezelfde unieke bezoeker. Als een overeenkomende persoon-id binnen 30 minuten in beide gegevenssets wordt weergegeven met een tijdstempel, wordt deze beschouwd als onderdeel van dezelfde sessie.

Dit concept is ook van toepassing op attributie. Het maakt niet uit van welke gegevensset een rij afkomstig is; attributie werkt precies alsof alle gebeurtenissen uit één dataset kwamen. De bovenstaande tabellen als voorbeeld gebruiken:

Als de verbinding alleen de eerste tabel en niet de tweede bevat, ziet u het volgende als u een rapport met de `string_color` afmetingen en de `metric_a` metrische waarde trekt met de laatste aanraakkenmerk:

| string_color | metrisch_a |
| --- | --- |
| Blauw | 5 |
| Niet opgegeven | 6 |
| Rood | 2 |

Nochtans, als u beide lijsten in uw verbinding omvatte, verandert de attributie aangezien in beide datasets `user_847` is. Een rij van de tweede dataset kenmerken `metric_a` aan &quot;Geel&quot;waar zij vroeger niet specificeerden:

| string_color | metrisch_a |
| --- | --- |
| Geel | 6 |
| Rood | 2 |
| Blauw | 3 |
