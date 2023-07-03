---
title: Filteroperatoren
description: Bepaal hoe een component met een waarde binnen een filter interactie aangaat.
exl-id: 744c7450-d6e9-4f78-a306-fe725ea0fa18
feature: Filters
source-git-commit: edbad9c9d3dc0b48db5334828a18ef652d4a38aa
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%

---

# Filteroperatoren

Met de filterbuilder kunt u waarden vergelijken en beperken met behulp van geselecteerde operatoren. Er zijn twee categorieën operatoren: [!UICONTROL Standard] en [!UICONTROL Distinct Count].

## Standaardoperatoren

| Operator | Beschrijving |
| --- | --- |
| equals | Retourneert items die exact overeenkomen voor een numerieke waarde of tekenreekswaarde. Als u jokertekens gebruikt, gebruikt u de operator &quot;overeenkomsten&quot;. |
| is niet gelijk aan | Retourneert alle items die niet exact overeenkomen met de ingevoerde waarde.  Als u jokertekens gebruikt, gebruikt u de operator &quot;komt niet overeen&quot;. |
| is gelijk aan een van de | Retourneert items die overeenkomen met de ingevoerde subtekenreekswaarden, gescheiden door een komma. |
| contains | Retourneert items die de subtekenreeksen van de ingevoerde waarden vergelijken. Als de regel voor een tekenreeksdimensie bijvoorbeeld `"Search"`, komt deze overeen met elke pagina die de subtekenreeks heeft `"Search"` in het `"Search Results"`, `"Search"`, en `"Searching"`. Deze operator is hoofdlettergevoelig. |
| bevat niet | Alle items die overeenkomen met de ingevoerde waarde worden niet in de resultaten opgenomen. Als de regel voor een tekenreeksdimensie bijvoorbeeld geen `"Search"`, worden pagina&#39;s met de subtekenreeks uitgesloten `"Search"` in het `"Search Results"`, `"Search"`, en `"Searching"`. |
| bevat alle | Retourneert items die alle subtekenreeksen (gescheiden door een spatie) in een willekeurige volgorde bevatten. Als u bijvoorbeeld `"Search Results"` met deze operator zou overeenkomen `"Search Results"` en `"Results of Search"`, maar niet `"Search"` of `"Results"` onafhankelijk. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| bevat niet alle | Alle items die overeenkomen met elke ingevoerde waarde worden niet in de resultaten opgenomen. Als u bijvoorbeeld `"Search Results"` met deze operator `"Search Results"` en `"Results of Search"`, maar niet `"Search"` of `"Results"`. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| bevat een van de | Retourneert items die een van de opgegeven subtekenreeksen bevatten. Als u bijvoorbeeld `"Search Results"` met deze operator zou overeenkomen `"Search Results"`, `"Results of Search"`, `"Search"`, en `"Results"`. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| bevat geen van de | Alle items die overeenkomen met een subtekenreeks worden uitgesloten van de resultaten. Als u bijvoorbeeld `"Search Results"` zou uitsluiten `"Search Results"`, `"Results of Search"`, `"Search"`, en `"Results"`. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| begint met | Retourneert items die beginnen met het teken of de tekenreeksen van de ingevoerde waarde. |
| start niet met | Retourneert alle items die niet beginnen met de tekens of tekenreeksen van de ingevoerde waarden. |
| eindigt met | Retourneert items die eindigen met het teken of de tekenreeksen van de ingevoerde waarde. |
| eindigt niet met | Retourneert alle items die niet eindigen met de tekens of tekenreeksen van de ingevoerde waarde. |
| matches | Retourneert items die exact overeenkomen op basis van een opgegeven numerieke waarde of tekenreekswaarde. Ondersteunt jokertekens die een sterretje gebruiken (`*`). Deze operator is hoofdlettergevoelig. Bijvoorbeeld:<ul><li>`a*e` overeenkomsten `ae`, `abcde`, `adobe`, en `a whole sentence`.</li><li>`adob*` overeenkomsten `adobe`, `adobe analytics`, en `adobo recipe`</li><li>`*dobe` overeenkomsten `dobe`, `adobe`, en `cute little dobe`.</li></ul> |
| komt niet overeen | Alle items die overeenkomen met de tekenreeks worden uitgesloten. Ondersteunt jokertekens die een sterretje gebruiken (`*`). |
| exists | Retourneert items als de waarde niet null is. |
| bestaat niet | Retourneert items als de waarde null is. |

## Operatoren voor onderscheiden aantallen

U kunt filteren op een aantal verschillende items binnen een dimensie. U kunt bijvoorbeeld filters maken voor personen die meer dan vijf verschillende producten hebben bekeken of bezoeken waarbij meer dan vijf afzonderlijke pagina&#39;s zijn weergegeven.

| Operator | Beschrijving |
| --- | --- |
| equals | Retourneert dimensieitems waarvan het unieke aantal gelijk is aan de ingevoerde waarde. |
| is niet gelijk aan | Retourneert dimensieitems waarvan het unieke aantal niet gelijk is aan de ingevoerde waarde. |
| is groter dan | Retourneert dimensieitems waarvan het unieke aantal groter is dan de ingevoerde waarde. |
| is kleiner dan | Retourneert dimensieitems waarvan het unieke aantal kleiner is dan de ingevoerde waarde. |
| is groter dan of gelijk aan | Retourneert dimensieitems waarvan het unieke aantal groter dan of gelijk is aan de ingevoerde waarde. |
| is kleiner dan of gelijk aan | Retourneert dimensieitems waarvan het unieke aantal kleiner dan of gelijk is aan de ingevoerde waarde. |
