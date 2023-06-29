---
title: Hoe stikken werkt
description: Begrijp het concept stitching
solution: Customer Journey Analytics
feature: Stitching
source-git-commit: 34566535589c84c96a8d7a47988cd155b743674e
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 10%

---

# Hoe stikken werkt

Met Stitching worden minimaal twee gegevenscontroles in een bepaalde gegevensset uitgevoerd:

* **Actief stiteren**: pogingen om elke hit vast te zetten terwijl hij binnenkomt. De netto nieuwe apparaten aan de dataset die nooit het programma hebben geopend worden typisch niet vastgemaakt op dit niveau. Apparaten die al zijn herkend, worden direct vastgezet.

* **Replay stitching**: Hiermee worden gegevens opnieuw afgespeeld op basis van unieke id&#39;s die het heeft geleerd. In dit stadium worden nieuwe apparaten aan de verbinding vastgezet. Adobe biedt twee herhalingsintervallen:
   * **Dagelijks**: Gegevens worden elke dag opnieuw afgespeeld met een terugzoekvenster van 24 uur. Deze optie biedt een voordeel dat het aantal keren wordt afgespeeld, maar niet-geregistreerde bezoekers moeten zich op dezelfde dag verifiëren dat ze uw site bezoeken.
   * **Wekelijks**: De gegevens worden eenmaal per week opnieuw afgespeeld met een terugkijkvenster van 7 dagen. Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Gegevens van minder dan een week oud worden echter niet vastgezet.

* **Privacy (optioneel)**: Wanneer verzoeken met betrekking tot privacy worden ontvangen, moet, naast het verwijderen van de gevraagde identiteit, elke koppeling van die identiteit tussen niet-geverifieerde gebeurtenissen ongedaan worden gemaakt.

Gegevens buiten het terugzoekvenster worden niet opnieuw afgespeeld. Een bezoeker moet binnen een bepaald terugkijkvenster voor een ongeautoriseerd bezoek en voor authentiek verklaard bezoek voor authentiek verklaren om samen worden geïdentificeerd. Als een apparaat eenmaal is herkend, wordt het vanaf dat punt live vastgezet. De verzoeken van de privacy worden verwerkt over stitched gegevens ongeacht tijd.

## Stap 1: Actief stiteren

Live stilzetten probeert elke gebeurtenis na verzameling aan te sluiten op bekende apparaten en kanalen. Overweeg het volgende voorbeeld, waar het Loodje verschillende gebeurtenissen als deel van een gebeurtenisdataset registreert.

*Gegevens zoals deze worden weergegeven op de dag waarop ze worden verzameld:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Transient ID (aanmeldings-id) | Id met titel (na liveslot) |
|---|---|---|---|---|
| 1 | 2023-05-12 12:01 | 246 ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **246** |
| 2 | 2023-05-12 12:02 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob |
| 3 | 2023-05-12 12:03 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 4 | 2023-05-12 12:04 | 246 | - | **Bob** |
| 5 | 2023-05-12 12:05 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 6 | 2023-05-12 12:06 | 246 | - | **Bob** | |
| 7 | 2023-05-12 12:07 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob |
| 8 | 2023-05-12 12:03 | 3579 ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **3579** |
| 9 | 2023-05-12 12:09 | 3579 ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **3579** |
| 10 | 2023-05-12 12:02 | 81911 ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **81911** |
| 11 | 2023-05-12 12:05 | 81911 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 12 | 2023-05-12 12:12 | 81911 | - | **Bob** |
| | | **3 apparaten** | | **4 personen**:<br/>246, Bob, 3579, 81911 |

{style="table-layout:auto"}

<!--
| Timestamp | Web dataset Persistent ID | Web dataset Transient ID | Stitched ID after live stitch | Call enter Person ID | Explanation of hit | People metric (cumulative) |
| --- | --- | --- | --- | --- | --- | --- |
| `1` | `246` | - | - | `246` | Bob visits your site on a desktop, unauthenticated | `1` (246) |
| `2` | `246` | `Bob` | - | `Bob` | Bob logs in on desktop | `2` (246 and Bob) |
| `3` | - | - | `Bob` | `Bob` | Bob calls customer service | `2` (246 and Bob) |
| `4` | `3579` | - | - | `3579` | Bob accesses your site on a mobile device, unauthenticated | `3` (246, Bob, and 3579) |
| `5` | `3579` | `Bob` | - | `Bob` | Bob logs in via mobile | `3` (246, Bob, and 3579) |
| `6` | - | - | `Bob` | `Bob` | Bob calls customer service again | `3` (246, Bob, and 3579) |
| `7` | `246` | - | - | `Bob` | Bob visits your site on a desktop again, unauthenticated | `3` (246, Bob, and 3579) |
-->

Zowel niet-geverifieerde als geverifieerde gebeurtenissen op nieuwe apparaten worden als afzonderlijke personen geteld (tijdelijk). Niet-geverifieerde gebeurtenissen op herkende apparaten worden live stilgezet.

Attributie werkt wanneer de identificerende douanevariabele aan een apparaat bindt. In het bovenstaande voorbeeld worden alle gebeurtenissen behalve de gebeurtenissen 1, 8, 9 en 10 live vernaakt (ze gebruiken allemaal de `Bob` id). Als u de stitching live uitvoert, wordt de geroteerde id voor gebeurtenis 4, 6 en 12 opgelost.

## Stap 2: Replay stitching

Met regelmatige intervallen (eenmaal per week of eenmaal per dag, afhankelijk van het gekozen terugkijkvenster) worden historische gegevens opnieuw berekend op basis van de apparaten die het nu herkent. Als een apparaat aanvankelijk gegevens verzendt terwijl niet voor authentiek verklaard en dan login, replay stitching bindt die niet voor authentiek verklaarde gebeurtenissen aan de correcte persoon. In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar worden verschillende getallen weergegeven op basis van het opnieuw afspelen van de gegevens.

*Dezelfde gegevens na afspelen:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Transient ID (aanmeldings-id) | Id met titel (na liveslot) | Id met titel (na opnieuw afspelen) |
|---|---|---|---|---|---|
| 1 | 2023-05-12 12:01 | 246 | - | 246 | **Bob** |
| 2 | 2023-05-12 12:02 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob | Bob ![Pijl-omhoog](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) |
| 3 | 2023-05-12 12:03 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | Bob |
| 4 | 2023-05-12 12:04 | 246 | - | **Bob** | Bob |
| 5 | 2023-05-12 12:05 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | Bob |
| 6 | 2023-05-12 12:06 | 246 | - | **Bob** | Bob |
| 7 | 2023-05-12 12:07 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob | Bob |
| 8 | 2023-05-12 12:03 | 3579 ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **3579** | **3579** |
| 9 | 2023-05-12 12:09 | 3579 ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **3579** | **3579** |
| 10 | 2023-05-12 12:02 | 81911 | - | 81911 | **Bob** |
| 11 | 2023-05-12 12:05 | 81911 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | Bob ![Pijl-omhoog](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) |
| 12 | 2023-05-12 12:12 | 81911 | - | **Bob** | Bob |
| | | **3 apparaten** | | **4 personen**:<br/>246, Bob, 3579, 81911 | **2 personen**:<br/>Bob, 3579 |

{style="table-layout:auto"}

Attributie werkt wanneer de identificerende douanevariabele aan een apparaat bindt. In het bovenstaande voorbeeld worden gebeurtenis 1 en 10 vastgezet als resultaat van het opnieuw afspelen, waarbij alleen gebeurtenis 8 en 9 niet worden vastgezet. En het aantal mensen (cumulatief) verminderen tot 2.

## Stap 3: Privacy-aanvraag

Wanneer u een privacyverzoek ontvangt, wordt de rij met de originele gebruikersinformatie verwijderd, samen met alle aangesloten id&#39;s die dezelfde persoongegevens bevatten. De volgende lijst vertegenwoordigt de zelfde gegevens zoals hierboven, maar toont het effect dat een privacyverzoek voor Loodje op de gegevens na verwerking het heeft. De rijen waar Bob voor authentiek is verklaard worden verwijderd (2, 3, 5, 7, en 11) samen met het verwijderen van Bob als voorbijgaande identiteitskaart voor andere rijen.

*Dezelfde gegevens na een privacyverzoek voor Bob:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Transient ID (aanmeldings-id) | Id met titel (na liveslot) | Id met titel (na opnieuw afspelen) | Transient ID (aanmeldings-id) | Id met titel (na privacyverzoek) |
|---|---|---|---|---|---|---|---|
| 1 | 2023-05-12 12:01 | 246 | - | 246 | **Bob** | - | 246 |
| 2 | 2023-05-12 12:02 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob | Bob ![Pijl-omhoog](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | 246 |
| 3 | 2023-05-12 12:03 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | Bob | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | 246 |
| 4 | 2023-05-12 12:04 | 246 | - | **Bob** | Bob | - | 246 |
| 5 | 2023-05-12 12:05 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | Bob | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | 246 |
| 6 | 2023-05-12 12:06 | 246 | - | **Bob** | Bob | - | 246 |
| 7 | 2023-05-12 12:07 | 246 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob | Bob | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | 246 |
| 8 | 2023-05-12 12:03 | 3579 ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **3579** | **3579** | - | 3579 |
| 9 | 2023-05-12 12:09 | 3579 ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **3579** | **3579** | - | 3579 |
| 10 | 2023-05-12 12:02 | 81911 | - | 81911 | **Bob** | - | 81911 |
| 11 | 2023-05-12 12:05 | 81911 | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | Bob ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | Bob ![Pijl-omhoog](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | 81911 |
| 12 | 2023-05-12 12:12 | 81911 | - | **Bob** | Bob | - | 81911 |
| | | **3 apparaten** | | **4 personen**:<br/>246, Bob, 3579, 81911 | **2 personen**:<br/>Bob, 3579 |  | **3 personen**:<br/>246 3579 819 |


<!--
| Timestamp | Web dataset Persistent ID | Web dataset Transient ID | Call center person ID | Person ID used (stitched ID) | Explanation of hit | People metric (cumulative) |
| --- | --- | --- | --- | --- | --- | --- |
| `1` | `246` | - | - | `Bob` | Bob visits your site on a desktop, unauthenticated | `1` (Bob) |
| `2` | `246` | `Bob` | - | `Bob` | Bob logs in on desktop | `1` (Bob) |
| `3` | - | - | `Bob` | `Bob` | Bob calls customer service | `1` (Bob) |
| `4` | `3579` | - | - | `Bob` | Bob accesses your site on a mobile device, unauthenticated | `1` (Bob) |
| `5` | `3579` | `Bob` | - | `Bob` | Bob logs in via mobile | `1` (Bob) |
| `6` | - | - | `Bob` | `Bob` | Bob calls customer service again | `1` (Bob) |
| `7` | `246` | - | - | `Bob` | Bob visits your site on a desktop again, unauthenticated | `1` (Bob) |
-->

## Samenvatting

* Bij het plaatsen worden bekende apparaten meteen vastgezet, maar worden nieuwe of niet-herkende apparaten niet onmiddellijk vastgezet.
* De gegevens worden met regelmatige intervallen opnieuw afgespeeld, en verandert historische gegevens in de verbinding die op apparaten wordt gebaseerd het heeft geleerd om zich te identificeren.
* Op één gegevensset worden actieve stitching en replay stitching uitgevoerd. Het resultaat is een nieuwe opgeheven dataset die geschikter is om te worden gebruikt wanneer gecombineerd met andere datasets (bijvoorbeeld, vraag-centrum gegevens) om kanaalanalyse uit te voeren.
* De verzoeken van de privacy verwijderen identiteiten die aan unauthenticated rijen werden verspreid.
