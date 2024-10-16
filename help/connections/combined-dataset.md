---
title: Gecombineerde gegevenssets voor gebeurtenissen
description: Leer hoe de Customer Journey Analytics tot een verbinding leidt door datasets te combineren.
exl-id: 9f678225-a9f3-4134-be38-924b8de8d57f
solution: Customer Journey Analytics
feature: Connections
role: Admin
source-git-commit: 8241bcc4a2653da456c1577eb95d5504ca118cd9
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 3%

---


# Gecombineerde gegevenssets voor gebeurtenissen

Wanneer u een verbinding creeert, combineert de Customer Journey Analytics alle gebeurtenisdatasets in één enkele dataset. Deze gecombineerde gebeurtenisdataset is wat de Customer Journey Analytics voor het melden (samen met profiel en raadplegingsdatasets) gebruikt. Wanneer u veelvoudige gebeurtenisdatasets in een verbinding omvat:

* De gegevens voor gebieden in datasets die op de **zelfde schemapad** worden gebaseerd worden samengevoegd in één enkele kolom in de gecombineerde dataset.
* De kolom van identiteitskaart van de Persoon, die voor elke dataset wordt gespecificeerd, wordt samengevoegd in één enkele kolom in de gecombineerde dataset, **ongeacht hun naam**. Deze kolom vormt de basis voor het identificeren van unieke personen in Customer Journey Analytics.
* Rijen worden verwerkt op basis van een tijdstempel.
* Gebeurtenissen worden tot op het millisecondenniveau opgelost.

## Voorbeeld

Kijk eens naar het volgende voorbeeld. U hebt twee gebeurtenisdatasets, elk met verschillende gebieden die verschillende gegevens bevatten.

>[!NOTE]
>
>Adobe Experience Platform slaat doorgaans een tijdstempel op in UNIX® milliseconden. Voor leesbaarheid in dit voorbeeld worden datum en tijd gebruikt.

| example_id | tijdstempel | string_color | string_animal | metrisch_a |
| --- | --- | --- | --- | ---: |
| user_310 | 01 jan. 7:02 | Rood | Fox | |
| user_310 | 01 jan. 7:04 | | | 2 |
| user_310 | 01 jan. 7:08 | Blauw | | 3 |
| user_847 | 12:31 | | Turf | 4 |
| user_847 | 12:44 | | | 2 |

| different_id | tijdstempel | string_color | string_shape | metrisch_b |
| --- | --- | --- | --- | ---: |
| user_847 | 2 jan. 12:26 | Geel | Cirkel | 8,5 |
| user_847 | 2 jan. 13:01 | Rood | | |
| alternateid_656 | 2 jan. 8:58 | Rood | Vierkant | 4,2 |
| alternateid_656 | 2 jan. 9:03 | | Driehoek | 3,1 |

Wanneer u een verbinding gebruikend deze twee gebeurtenisdatasets creeert en hebt geïdentificeerd

* `example_id` als Persoon-id voor de eerste gegevensset, en
* `different_id` als Persoon-id voor de tweede dataset,

de volgende gecombineerde gegevensset wordt gebruikt voor de rapportage.

| id | tijdstempel | string_color | string_animal | string_shape | metrisch_a | metrisch_b |
| --- | --- | --- | --- | --- | ---: | ---: |
| user_310 | 01 jan. 7:02 | Rood | Fox | | | |
| user_310 | 01 jan. 7:04 | | | | 2 | |
| user_310 | 01 jan. 7:08 | Blauw | | | 3 | |
| user_847 | 2 jan. 12:26 | Geel | | Cirkel | | 8,5 |
| user_847 | 12:31 | | Turf | | 4 | |
| user_847 | 12:44 | | | | 2 | |
| user_847 | 2 jan. 13:01 | Rood | | | | |
| alternateid_656 | 2 jan. 8:58 | Rood | | Vierkant | | 4,2 |
| alternateid_656 | 2 jan. 9:03 | | | Driehoek | | 3,1 |

Om het belang van schemawegen te illustreren, overweeg dit scenario. In de eerste dataset, is `string_color` gebaseerd op schemapad `_experience.whatever.string_color` en in de tweede dataset op schemapad `_experience.somethingelse.string_color`. In dit scenario, wordt het gegeven **niet** samengevoegd in één kolom in de resulterende gecombineerde dataset. In plaats daarvan is het resultaat twee `string_color` kolommen in de gecombineerde dataset:

| id | tijdstempel | _experience.<br/> alles.<br/> string_color | _experience.<br/> iets anders.<br/> string_color | string_animal | string_shape | metrisch_a | metrisch_b |
| --- | --- | --- | --- | --- | --- | ---: | ---:|
| user_310 | 01 jan. 7:02 | Rood | | Fox | | | |
| user_310 | 01 jan. 7:04 | | | | | 2 | |
| user_310 | 01 jan. 7:08 | Blauw | | | | 3 | |
| user_847 | 2 jan. 12:26 | | Geel | | Cirkel | | 8,5 |
| user_847 | 12:31 | | | Turf |  | 4 | |
| user_847 | 12:44 | | | | | 2 | |
| user_847 | 2 jan. 13:01 | | Rood | | | | |
| alternateid_656 | 2 jan. 8:58 | | Rood | | Vierkant | | 4,2 |
| alternateid_656 | 2 jan. 9:03 | | | | Driehoek | | 3,1 |

Deze gecombineerde gebeurtenisdataset is wat in het melden wordt gebruikt. Het maakt niet uit van welke dataset een rij afkomstig is. Customer Journey Analytics behandelt alle gegevens alsof het in de zelfde dataset is. Als een overeenkomende persoon-id in beide gegevenssets wordt weergegeven, worden deze als dezelfde unieke persoon beschouwd. Als een overeenkomende persoon-id binnen 30 minuten in beide gegevenssets wordt weergegeven met een tijdstempel, wordt deze beschouwd als onderdeel van dezelfde sessie. Velden met identieke schemapaden worden samengevoegd.

Dit concept is ook van toepassing op attributie. Het maakt niet uit van welke dataset een rij afkomstig is; de attributie werkt precies alsof alle gebeurtenissen uit één dataset kwamen. De bovenstaande tabellen als voorbeeld gebruiken:

Als uw verbinding alleen de eerste tabel bevatte en niet de tweede, zou het trekken van een rapport aan de hand van de `string_color` -dimensie en `metric_a` -meting met de laatste aanraakkenmerk het volgende laten zien:

| string_color | metrisch_a |
| --- | ---: |
| Niet opgegeven | 6 |
| Blauw | 3 |
| Rood | 2 |

Als u echter beide tabellen hebt opgenomen in uw verbinding, verandert de toewijzing omdat `user_847` zich in beide gegevenssets bevindt. Een rij van de tweede dataset attributen `metric_a` aan &quot;Geel&quot;waar zij eerder niet specificeerden:

| string_color | metrisch_a |
| --- | ---: |
| Geel | 6 |
| Blauw | 3 |
| Rood | 2 |

>[!NOTE]
>
>Als een samengevoegd gebied een raadplegingssleutel voor één gebeurtenisdataset in de verbinding is, zal de bijbehorende raadplegingsdataset **alle** waarden van dat gebied verrijken. Het maakt niet uit van welke gebeurtenisdataset een rij afkomstig is, aangezien de raadplegingsverhouding met de gedeelde schemapad wordt geassocieerd.

## Kanaaloverschrijdende analyse

Het volgende niveau van het combineren van datasets is kanaalanalyse, waar datasets van verschillende kanalen worden gecombineerd, die op een gemeenschappelijke herkenningsteken (identiteitskaart van de Persoon) wordt gebaseerd. De analyse over kanalen kan van het stitching functionaliteit profiteren, die u toestaat om identiteitskaart van de Persoon van een dataset opnieuw te bepalen zodat wordt de dataset behoorlijk bijgewerkt om een naadloze combinatie veelvoudige datasets toe te laten. Bij het zoeken naar gebruikersgegevens van zowel geverifieerde als niet-geverifieerde sessies wordt een aangesloten id gegenereerd.

Met de kanaalanalyse kunt u vragen beantwoorden zoals:

* Hoeveel mensen beginnen met hun ervaring in één kanaal, en eindigen het in een andere?
* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt de campagne klikdoorhalingen die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn begrip van campagnedoeltreffendheid als ik apparatuurreizen bekijk? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?


Raadpleeg het specifieke geval van gebruik voor meer informatie over kanaalanalyse:

* [Kanaaloverschrijdende analyse](../use-cases/cross-channel/cross-channel.md)

Ga voor een diepgaandere bespreking van de stitching-functionaliteit naar:

* [Overzicht van tekenreeksen](/help/stitching/overview.md)
* [Veelgestelde vragen](/help/stitching/faq.md)

