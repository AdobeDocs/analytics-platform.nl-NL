---
title: Filteroperatoren
description: Bepaal hoe een component met een waarde binnen een filter interactie aangaat.
source-git-commit: 1334e1edb36583ba978936fecbff2657e63a94bf
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# Filteroperatoren

Met de filterbuilder kunt u waarden vergelijken en beperken met behulp van geselecteerde operatoren. Er zijn twee categorieën operatoren: [!UICONTROL Standard] en [!UICONTROL Distinct Count].

## Standaardoperatoren

| Exploitant | Beschrijving |
| Gelijken | Retourneert items die exact overeenkomen voor een numerieke waarde of tekenreekswaarde. Als u jokertekens gebruikt, gebruikt u de operator &quot;overeenkomsten&quot;. |
| niet gelijk aan | Retourneert alle items die niet exact overeenkomen met de ingevoerde waarde.  Als u jokertekens gebruikt, gebruikt u de operator &quot;komt niet overeen&quot;. |
| bevat | Retourneert items die vergeleken worden met de subtekenreeksen van de ingevoerde waarden. Als de regel voor een tekenreeksdimensie bijvoorbeeld `"Search"` bevat, komt deze overeen met elke pagina die de subtekenreeks `"Search"` erin bevat, inclusief `"Search Results"`, `"Search"` en `"Searching"`. Deze operator is hoofdlettergevoelig. |
| bevat niet | Alle items die overeenkomen met de ingevoerde waarde worden niet in de resultaten opgenomen. Als de regel voor een tekenreeksdimensie bijvoorbeeld `"Search"` niet bevat, sluit deze elke pagina uit die de subtekenreeks `"Search"` erin bevat, inclusief `"Search Results"`, `"Search"` en `"Searching"`. |
| bevat alle | Retourneert items die alle subtekenreeksen (gescheiden door een spatie) in een willekeurige volgorde bevatten. Als u bijvoorbeeld `"Search Results"` met deze operator invoert, komen `"Search Results"` en `"Results of Search"` overeen, maar niet `"Search"` of `"Results"` onafhankelijk. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| bevat niet alle | Alle items die overeenkomen met elke ingevoerde waarde worden niet in de resultaten opgenomen. Als u bijvoorbeeld `"Search Results"` met deze operator invoert, worden `"Search Results"` en `"Results of Search"` niet opgenomen, maar `"Search"` of `"Results"` niet. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| bevat één van de volgende | Retourneert items die een van de opgegeven subtekenreeksen bevatten. Als u bijvoorbeeld `"Search Results"` met deze operator invoert, komen `"Search Results"`, `"Results of Search"`, `"Search"` en `"Results"` overeen. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| bevat geen van de | Alle items die overeenkomen met een subtekenreeks, worden uitgesloten van de resultaten. Als u bijvoorbeeld `"Search Results"` invoert, worden `"Search Results"`, `"Results of Search"`, `"Search"` en `"Results"` niet opgenomen. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| begint met | Retourneert items die beginnen met het teken of de tekenreeksen van de ingevoerde waarde. |
| start niet met | Retourneert alle items die niet beginnen met de tekens of tekenreeksen van de ingevoerde waarden. |
| Eindigt met | Retourneert items die eindigen met het teken of de tekenreeksen van de ingevoerde waarde. |
| eindigt niet met | Retourneert alle items die niet eindigen met de tekens of tekenreeksen van de ingevoerde waarde. |
| overeenkomsten | Retourneert items die exact overeenkomen op basis van een opgegeven numerieke waarde of tekenreekswaarde. Ondersteunt jokertekens die een asterisk (`*`) gebruiken. Deze operator is hoofdlettergevoelig. Bijvoorbeeld:<ul><li>`a*e` komt overeen  `ae`,  `abcde`,  `adobe`en  `a whole sentence`.</li><li>`adob*` overeenkomsten  `adobe`,  `adobe analytics`en  `adobo recipe`</li><li>`*dobe` overeenkomsten  `dobe`,  `adobe`en  `cute little dobe`.</li></ul>|
| komt niet overeen | Alle items die overeenkomen met de tekenreeks worden uitgesloten. Ondersteunt jokertekens die een asterisk (`*`) gebruiken. |
| bestaat | Retourneert items als de waarde niet null is. |
| bestaat niet | Retourneert items als de waarde null is. |

## Operatoren voor onderscheiden aantallen

U kunt op een duidelijke telling van punten binnen een afmeting segmenteren. U kunt bijvoorbeeld filters maken voor bezoekers die meer dan vijf verschillende producten hebben bekeken of bezoeken waarbij meer dan vijf afzonderlijke pagina&#39;s werden weergegeven.

| Operator | Beschrijving |
| --- | --- |
| equals | Retourneert dimensieitems waarvan het unieke aantal gelijk is aan de ingevoerde waarde. |
| is niet gelijk aan | Retourneert dimensieitems waarvan het unieke aantal niet gelijk is aan de ingevoerde waarde. |
| is groter dan | Retourneert dimensieitems waarvan het unieke aantal groter is dan de ingevoerde waarde. |
| is kleiner dan | Retourneert dimensieitems waarvan het unieke aantal kleiner is dan de ingevoerde waarde. |
| is groter dan of gelijk aan | Retourneert dimensieitems waarvan het unieke aantal groter dan of gelijk is aan de ingevoerde waarde. |
| is kleiner dan of gelijk aan | Retourneert dimensieitems waarvan het unieke aantal kleiner dan of gelijk is aan de ingevoerde waarde. |
