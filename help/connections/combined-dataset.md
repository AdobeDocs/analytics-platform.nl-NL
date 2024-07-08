---
title: Gecombineerde gegevenssets voor gebeurtenissen
description: Leer hoe de Customer Journey Analytics tot een verbinding leidt door datasets te combineren.
exl-id: 9f678225-a9f3-4134-be38-924b8de8d57f
solution: Customer Journey Analytics
feature: Connections
role: Admin
source-git-commit: 3389c141105ff71ed26abe4384fe3bb930448d43
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 1%

---


# Gecombineerde gegevenssets voor gebeurtenissen

Wanneer u een verbinding creeert, combineert de Customer Journey Analytics alle gebeurtenisdatasets in één enkele dataset. Deze gecombineerde gebeurtenisdataset is wat de Customer Journey Analytics voor het melden (samen met profiel en raadplegingsdatasets) gebruikt. Wanneer u meerdere gebeurtenisgegevenssets in een verbinding opneemt:

* De gegevens voor velden in gegevensreeksen op basis van de **hetzelfde schema-pad** worden samengevoegd tot één kolom in de gecombineerde gegevensset.
* De kolom Person ID, die voor elke dataset wordt gespecificeerd, wordt samengevoegd in één kolom in de gecombineerde dataset, **ongeacht hun naam**. Deze kolom vormt de basis voor het identificeren van unieke personen in Customer Journey Analytics.
* Rijen worden verwerkt op basis van een tijdstempel.
* Gebeurtenissen worden tot op het millisecondenniveau opgelost.

## Voorbeeld

Kijk eens naar het volgende voorbeeld. U hebt twee gebeurtenisdatasets, elk met verschillende gebieden die verschillende gegevens bevatten.

>[!NOTE]
>
>Adobe Experience Platform slaat doorgaans een tijdstempel op in UNIX® milliseconden. Voor leesbaarheid in dit voorbeeld worden datum en tijd gebruikt.

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

Wanneer u een verbinding gebruikend deze twee gebeurtenisdatasets creeert en hebt geïdentificeerd

* `example_id` als Persoon-id voor de eerste gegevensset, en
* `different_id` persoons-id voor de tweede gegevensset;

de volgende gecombineerde gegevensset wordt gebruikt voor rapportage.

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

Bekijk dit scenario ter illustratie van het belang van schemapaden. In de eerste gegevensset `string_color` is dit gebaseerd op het schemapad `_experience.whatever.string_color` en in de tweede gegevensset op schemapad  `_experience.somethingelse.string_color`. In dit scenario worden **de gegevens niet** samengevoegd in één kolom van de resulterende gecombineerde gegevensset. In plaats daarvan bestaat het resultaat uit twee `string_color` kolommen in de gecombineerde gegevensset.

Deze gecombineerde gebeurtenisdataset is wat in het melden wordt gebruikt. Het maakt niet uit van welke dataset een rij komt. Customer Journey Analytics behandelt alle gegevens alsof het in de zelfde dataset is. Als een overeenkomende persoon-id in beide gegevenssets wordt weergegeven, worden deze als dezelfde unieke persoon beschouwd. Als een overeenkomende persoon-id binnen 30 minuten in beide gegevenssets wordt weergegeven met een tijdstempel, wordt deze beschouwd als onderdeel van dezelfde sessie. Velden met identieke schemapaden worden samengevoegd.

Dit concept is ook van toepassing op attributie. Het maakt niet uit van welke dataset een rij komt; attributie werkt precies alsof alle gebeurtenissen afkomstig zijn uit één gegevensset. Met de bovenstaande tabellen als voorbeeld:

Als uw verbinding alleen de eerste tabel bevatte en niet de tweede, toont u het volgende als u een rapport ophaalt met de afmetingen en `metric_a` de `string_color` metriek via de laatste aanraking:

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

>[!NOTE]
>
>Als een samengevoegd gebied een raadplegingssleutel voor één gebeurtenisdataset in de verbinding is, zal de bijbehorende raadplegingsdataset verrijken *alles* waarden van dat veld. Het maakt niet uit van welke gebeurtenisset een rij komt, omdat de zoekrelatie is gekoppeld aan het pad van het gedeelde schema.

## Cross-channel analyse

Het volgende niveau bij het combineren van gegevenssets is cross-channel analyse, waarbij gegevenssets van verschillende kanalen worden gecombineerd op basis van een gemeenschappelijke id (Persoon-ID). Cross-channel-analyse kan profiteren van stitching-functionaliteit, waardoor u de Persoonlijke ID van een gegevensset opnieuw kunt toetsen, zodat de gegevensset correct wordt bijgewerkt voor een naadloze combinatie van meerdere gegevenssets. Stitching kijkt naar gebruikersgegevens van zowel geverifieerde als niet-geverifieerde sessies om een samengevoegde id te genereren.

Met de kanaalanalyse kunt u vragen beantwoorden zoals:

* Hoeveel mensen beginnen met hun ervaring in één kanaal, en eindigen het in een andere?
* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt de campagne klikdoorhalingen die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn begrip van de effectiviteit van een campagne als ik reizen met verschillende apparaten overweeg? Hoe verandert mijn trechteranalyse?
* Wat zijn de meest gangbare paden die gebruikers van het ene apparaat naar het andere nemen? Waar vallen ze af? Waar slagen ze in?
* Waarin verschilt het gedrag van gebruikers met meerdere apparaten van die van gebruikers met één apparaat?


Raadpleeg de specifieke situatie voor meer informatie over cross-channel-analyse:

* [Kanaaloverschrijdende analyse](../use-cases/cross-channel/cross-channel.md)

Ga voor een diepgaandere bespreking van de stitching-functionaliteit naar:

* [Overzicht van tekenreeksen](/help/stitching/overview.md)
* [Veelgestelde vragen](/help/stitching/faq.md)

