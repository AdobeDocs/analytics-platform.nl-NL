---
title: Componentinstellingen voor geen waardeopties
description: Bepaal hoe een dimensie moet worden verwerkt als deze leeg is.
source-git-commit: af357167e65f4a577880832818221f6edbfc8b0a
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Componentinstellingen voor Geen waardopties

Geen waardeopties laten u bepalen hoe Analysis Workspace situaties behandelt waar een gebeurtenis in een dataset metrisch bevat maar de afmeting geen waarde bevatte. U kunt de naam van dit dimensie-item kiezen, het geheel verbergen of het zelfs als een werkelijke waarde behandelen.

![Geen waardeopties](../assets/no-value-options.png)

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL If shown, call "No value"] | Een tekstveld waarin u de naam van het **[!UICONTROL No value]**-dimensie-item kunt wijzigen in iets anders. |
| [!UICONTROL Don't show No value by default] | Deze waarde wordt niet weergegeven in de rapportage. Metrische voorvallen die niet aan deze dimensie zijn gekoppeld, zijn niet zichtbaar in het rapport. |
| [!UICONTROL Show No value by default] | Deze waarde wordt in de rapportage weergegeven. |
| [!UICONTROL Treat No value as a value] | Hiermee vervangt u lege waarden in de gegevens door de tekst die u onder [!UICONTROL If shown, call "No value"] hebt opgegeven. Als u bijvoorbeeld mobiele apparaattypen als de dimensie had, kunt u de naam van het **[!UICONTROL No value]**-item wijzigen in &quot;Computer&quot;. Wanneer u dit veld wijzigt in een aangepaste waarde, wordt de aangepaste waarde beschouwd als een geldige tekenreekswaarde. Als u de waarde &quot;Rood&quot; in dit veld invoert, worden alle instanties van de tekenreeks &quot;Rood&quot; die in de gegevens zelf worden weergegeven, daarom onder hetzelfde lijstitem als u hebt opgegeven. |
