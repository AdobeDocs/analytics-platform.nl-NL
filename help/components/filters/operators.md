---
title: Operatoren
description: Bepaal hoe een component met een waarde binnen een filter interactie aangaat.
exl-id: 744c7450-d6e9-4f78-a306-fe725ea0fa18
feature: Filters
role: User
source-git-commit: 5b441472a21db99728d012c19f12d98f984086f5
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# Operatoren

Met de filterbuilder kunt u waarden voor componenten vergelijken en beperken met behulp van geselecteerde operatoren. Er zijn twee categorieën operatoren: [[!UICONTROL Standard]](#standard-operators) en [[!UICONTROL Distinct Count]](#distinct-count-operators) .

## Standaardoperatoren

| Operator | Beschrijving |
| --- | --- |
| **[!UICONTROL equals]** | Retourneert items die exact overeenkomen voor een numerieke waarde of tekenreekswaarde. Als het gebruiken van vervangingskarakters, gebruik de gelijkenexploitant. |
| **[!UICONTROL does not equal]** | Retourneert alle items die niet exact overeenkomen met de ingevoerde waarde.  Als u jokertekens gebruikt, gebruikt u de operator &#39;komt niet overeen&#39;. |
| **[!UICONTROL equals any of]** | Retourneert items die overeenkomen met de ingevoerde subtekenreekswaarden, gescheiden door een komma. |
| **[!UICONTROL contains]** | Retourneert items die de subtekenreeksen van de ingevoerde waarden vergelijken. Als de waarde voor een paginanaam-dimensie bijvoorbeeld `Search` bevat, komt deze operator overeen met elke pagina die de subtekenreeks `Search` in zijn naam bevat, inclusief `Search Results` , `Search` en `Searching` . Deze operator is hoofdlettergevoelig. |
| **[!UICONTROL does not contain]** | Alle items die overeenkomen met de ingevoerde waarde worden niet in de resultaten opgenomen. Als de waarde voor een paginanaam-afmeting bijvoorbeeld niet `Search` bevat, sluit deze operator elke pagina uit die de subtekenreeks `Search` in de naam heeft, inclusief `Search Results` , `Search` en `Searching` . |
| **[!UICONTROL contains all of]** | Retourneert items die alle subtekenreeksen (gescheiden door een spatie) in een willekeurige volgorde bevatten. Als u bijvoorbeeld `Search Results` opgeeft als waarde voor deze operator, komt dit overeen met `Search Results` en `Results of Search` , maar niet `Search` of `Results` afzonderlijk. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| **[!UICONTROL does not contain all of]** | Alle items die overeenkomen met elke ingevoerde waarde worden niet in de resultaten opgenomen. Als u bijvoorbeeld `Search Results` opgeeft als waarde voor deze operator, worden `Search Results` en `Results of Search` niet opgenomen, maar niet `Search` of `Results` . Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| **[!UICONTROL contains any of]** | Retourneert items die een van de opgegeven subtekenreeksen bevatten. Als u bijvoorbeeld `Search Results` opgeeft als de waarde voor deze operator, komt dit overeen met `Search Results` , `Results of Search` , `Search` en `Results` . Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| **[!UICONTROL does not contain any of]** | Alle items die overeenkomen met een subtekenreeks worden niet in de resultaten opgenomen. Als u bijvoorbeeld `Search Results` opgeeft als waarde voor deze operator, worden `Search Results` , `Results of Search` , `Search` en `Results` uitgesloten. Deze operator ondersteunt maximaal 100 woorden gescheiden door spaties. |
| **[!UICONTROL starts with]** | Retourneert items die beginnen met het teken of de tekenreeksen van de opgegeven waarde. |
| **[!UICONTROL does not start with]** | Retourneert alle items die niet beginnen met de tekens of tekenreeksen van de opgegeven waarde. |
| **[!UICONTROL ends with]** | Retourneert items die eindigen met het teken of de tekenreeksen van de opgegeven waarde. |
| **[!UICONTROL does not end with]** | Retourneert alle items die niet eindigen met de tekens of tekenreeksen van de opgegeven waarde. |
| **[!UICONTROL matches]** | Retourneert items die overeenkomen met items die exact zijn gebaseerd op een bepaalde numerieke waarde of tekenreekswaarde. Steunt vervangingen gebruikend een asterisk (`*`). Deze operator is hoofdlettergevoelig. Bijvoorbeeld:<ul><li>`a*e` komt overeen met `ae` , `abcde` , `adobe` en `a whole sentence` .</li><li>`adob*` komt overeen met `adobe` , `adobe analytics` en `adobo recipe`</li><li>`*dobe` komt overeen met `dobe` , `adobe` en `cute little dobe` .</li></ul> |
| **[!UICONTROL does not match]** | Alle items die overeenkomen met de tekenreeks worden uitgesloten. Steunt vervangingen gebruikend een asterisk (`*`). |
| **[!UICONTROL exists]** | Retourneert items als de waarde niet null is. |
| **[!UICONTROL does not exist]** | Retourneert items als de waarde null is. |

## Operatoren voor onderscheiden tellen

U kunt filteren op een aantal verschillende items binnen een dimensie. U kunt bijvoorbeeld filters maken voor personen die meer dan vijf verschillende producten hebben bekeken of bezoeken waarbij meer dan vijf afzonderlijke pagina&#39;s zijn weergegeven.

| Operator | Beschrijving |
| --- | --- |
| **[!UICONTROL equals]** | Retourneert dimensieitems waarvan het unieke aantal gelijk is aan de ingevoerde waarde. |
| **[!UICONTROL does not equal]** | Retourneert dimensieitems waarvan het unieke aantal niet gelijk is aan de ingevoerde waarde. |
| **[!UICONTROL is greater than]** | Retourneert dimensieitems waarvan het unieke aantal groter is dan de ingevoerde waarde. |
| **[!UICONTROL is less than]** | Retourneert dimensieitems waarvan het unieke aantal kleiner is dan de ingevoerde waarde. |
| **[!UICONTROL is greater than or equal to]** | Retourneert dimensieitems waarvan het unieke aantal groter dan of gelijk is aan de ingevoerde waarde. |
| **[!UICONTROL is less than or equal to]** | Retourneert dimensieitems waarvan het unieke aantal kleiner dan of gelijk is aan de ingevoerde waarde. |
