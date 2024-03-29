---
title: Hoe herspeelt u?
description: Begrijp het concept "replay"in Kanaalanalyse
exl-id: 1100043a-4e4f-4dbc-9cfc-9dcba5db5f67
solution: Customer Journey Analytics
hide: true
hidefromtoc: true
source-git-commit: 4c6e968272b554188243b772bd159fe8174b3c3b
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# Hoe herspeelt u?

Met Kanaalanalyse kunt u gegevens op een bepaalde verbinding in twee stappen doorgeven:

* **Levend stitching**: CCA probeert elke gebeurtenis te verbinden aangezien het binnen komt. De netto nieuwe apparaten aan de dataset die nooit het programma hebben geopend worden typisch niet vastgemaakt op dit niveau. Apparaten die al zijn herkend, worden direct vastgezet.
* **Opnieuw afspelen**: CCA &quot;replay&quot;gegevens die op unieke herkenningstekens worden gebaseerd het heeft geleerd. In dit stadium worden nieuwe apparaten aan de verbinding vastgezet. Adobe biedt twee herhalingsintervallen:
   * Dagelijks: gegevens worden elke dag opnieuw afgespeeld met een terugkijkvenster van 24 uur. Deze optie biedt een voordeel dat replay veel frequenter is, maar niet-geregistreerde personen moeten zich op dezelfde dag verifiëren als zij uw site bezoeken.
   * Wekelijks: gegevens worden eenmaal per week opnieuw afgespeeld met een terugkijkvenster van 7 dagen. Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Gegevens van minder dan een week oud worden echter niet vastgezet.

Gegevens buiten het terugzoekvenster worden niet opnieuw afgespeeld. Een persoon moet binnen een bepaald raadplegingsvenster voor een ongeautoriseerd bezoek en voor authentiek verklaard bezoek voor authentiek verklaren om samen te worden geïdentificeerd. Als een apparaat eenmaal is herkend, wordt het vanaf dat punt voorwaarts vastgezet.

## Stap 1: live-stitching

CCA probeert om elke gebeurtenis op inzameling aan bekende apparaten en kanalen te verbinden. Overweeg het volgende voorbeeld, waar het Loodje twee verschillende kanalen gebruikt.

*Gegevens zoals deze worden weergegeven op de dag waarop ze worden verzameld:*

| Tijdstempel | Persistente ID van webgegevensset | Tijdelijke id voor webgegevensset | Identiteitskaart van het centrum van de vraag | Gebruikte persoon-id | Verklaring van de gebeurtenis | Metrische personen (cumulatief) |
| --- | --- | --- | --- | --- | --- | --- |
| `1` | `246` | - | - | `246` | Bob bezoekt uw site op zijn bureaublad, niet geverifieerd | `1` (246) |
| `2` | `246` | `Bob` | - | `Bob` | Bob meldt zich aan op desktop | `2` (246 en Bob) |
| `3` | - | - | `Bob` | `Bob` | Bob roept de klantenservice aan | `2` (246 en Bob) |
| `4` | `3579` | - | - | `3579` | Bob benadert uw site op zijn mobiele apparaat, niet geverifieerd | `3` (246, Bob en 3579) |
| `5` | `3579` | `Bob` | - | `Bob` | Bob meldt zich aan via mobile | `3` (246, Bob en 3579) |
| `6` | - | - | `Bob` | `Bob` | Bob roept de klantenservice opnieuw aan | `3` (246, Bob en 3579) |
| `7` | `246` | - | - | `Bob` | Bob bezoekt opnieuw uw site op zijn bureaublad, zonder verificatie | `3` (246, Bob en 3579) |

Zowel niet-geverifieerde als geverifieerde gebeurtenissen op nieuwe apparaten worden als afzonderlijke personen geteld (tijdelijk). Niet-geverifieerde gebeurtenissen op herkende apparaten worden live-gezet.

Attributie werkt zodra de identificerende douanevariabele aan een apparaat bindt. In het bovenstaande voorbeeld zijn alle gebeurtenissen behalve de gebeurtenissen 1 en 4 live-gezet (ze gebruiken allemaal de `Bob` id). Attributie werkt bij gebeurtenissen 1 en 4 na het opnieuw afspelen van stitching.

## Stap 2: Spatiëring opnieuw afspelen

Met regelmatige intervallen (eens per week of eens per dag afhankelijk van het gekozen terugkijkvenster), herberekent CCA historische gegevens die op apparaten worden gebaseerd het nu herkent. Als een apparaat aanvankelijk gegevens verzendt terwijl niet voor authentiek verklaard en dan login, bindt CCA die niet voor authentiek verklaarde gebeurtenissen aan de correcte persoon. In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar worden verschillende getallen weergegeven op basis van het opnieuw afspelen van de gegevens.

*Dezelfde gegevens na afspelen:*

| Tijdstempel | Persistente ID van webgegevensset | Tijdelijke id voor webgegevensset | Identiteitskaart van het centrum van de vraag | Gebruikte persoon-id | Verklaring van de gebeurtenis | Metrische personen (cumulatief) |
| --- | --- | --- | --- | --- | --- | --- |
| `1` | `246` | - | - | `Bob` | Bob bezoekt uw site op zijn bureaublad, niet geverifieerd | `1` (Bob) |
| `2` | `246` | `Bob` | - | `Bob` | Bob meldt zich aan op desktop | `1` (Bob) |
| `3` | - | - | `Bob` | `Bob` | Bob roept de klantenservice aan | `1` (Bob) |
| `4` | `3579` | - | - | `Bob` | Bob benadert uw site op zijn mobiele apparaat, niet geverifieerd | `1` (Bob) |
| `5` | `3579` | `Bob` | - | `Bob` | Bob meldt zich aan via mobile | `1` (Bob) |
| `6` | - | - | `Bob` | `Bob` | Bob roept de klantenservice opnieuw aan | `1` (Bob) |
| `7` | `246` | - | - | `Bob` | Bob bezoekt opnieuw uw site op zijn bureaublad, zonder verificatie | `1` (Bob) |

>[!NOTE]
>
>Gegevens worden alleen voor de websitegegevensset afgespeeld. De dataset van het vraagcentrum blijft onveranderd, maar past op wanneer correcte persoon identiteitskaart wordt gebruikt.

## Opnieuw

* CCA hecht onmiddellijk bekende apparaten aan, maar sluit niet onmiddellijk nieuwe of niet-herkende apparaten aan.
* De gegevens worden met regelmatige intervallen opnieuw afgespeeld, en verandert historische gegevens in de verbinding die op apparaten wordt gebaseerd het heeft geleerd om zich te identificeren.
