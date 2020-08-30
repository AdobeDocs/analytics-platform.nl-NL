---
title: Gecombineerde datasets
description: Leer hoe CJA tot een verbinding door datasets te combineren leidt.
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# Gecombineerde datasets

Wanneer u een verbinding creeert, combineert CJA alle schema&#39;s en datasets in één enkele dataset. Deze &quot;gecombineerde dataset&quot; is wat CJA gebruikt voor rapportage. Wanneer u veelvoudige schema&#39;s of datasets in een verbinding omvat:

* Schema&#39;s zijn gecombineerd. De dubbele schemagebieden worden samengevoegd.
* De kolom &quot;identiteitskaart van de Persoon&quot;van elke dataset wordt samengevoegd in één enkele kolom, ongeacht hun naam. Deze kolom is de stichting van het identificeren van unieke bezoekers in CJA.
* De rijen worden verwerkt gebaseerd op timestamp.

## Voorbeeld

Overweeg het volgende voorbeeld. U hebt twee datasets, elk met verschillende gebieden die verschillende gegevens bevatten.

>[!NOTE]
>
>Het Platform van de Ervaring van Adobe slaat typisch timestamp in de milliseconden van Unix op. Voor leesbaarheid in dit voorbeeld, worden de datum en de tijd gebruikt.

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

Deze gecombineerde dataset is wat in rapportering wordt gebruikt. Het maakt niet uit van welke dataset een rij afkomstig is; CJA behandelt alle gegevens alsof het in de zelfde dataset is. Als een passende identiteitskaart van de Persoon in beide datasets verschijnt, worden zij beschouwd als de zelfde unieke bezoeker. Als een passende identiteitskaart van de Persoon in beide datasets met timestamp binnen 30 minuten verschijnt, worden zij beschouwd als deel van de zelfde zitting.

Dit begrip geldt ook voor de toerekening. Het maakt niet uit van welke dataset een rij afkomstig is; de attributie werkt precies alsof alle gebeurtenissen uit één enkele dataset kwamen. Het gebruik van de bovenstaande tabellen als voorbeeld:

Als uw verbinding slechts de eerste lijst en niet de tweede omvatte, trekkend een rapport gebruikend `string_color` dimensie en `metric_a` De metrisch gebruikend laatste aanraking attributen zou tonen:

| string_color | metrisch_a |
| --- | --- |
| Niet gespecificeerd | 6 |
| Blauw | 3 |
| Rood | 2 |

Nochtans, als u beide lijsten in uw verbinding omvatte, verandert de attributie sinds `user_847` is in beide datasets. Een rij van de tweede datasetattributen `metric_a` &quot;Geel&quot;, indien zij voorheen niet waren gespecificeerd:

| string_color | metrisch_a |
| --- | --- |
| Geel | 6 |
| Blauw | 1 |
| Rood | 2 |
