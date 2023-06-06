---
title: Componentinstellingen voor geen waardeopties
description: Bepaal hoe een dimensie moet worden verwerkt als deze leeg is.
exl-id: c7f226c5-0058-4151-9c9a-652b37266beb
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: 0bd632d9e748b567c7b946f4c7d1437f0a776ca2
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---

# Componentinstellingen voor Geen waardopties

Geen waardeopties laten u bepalen hoe Analysis Workspace situaties behandelt waar een gebeurtenis in een dataset metrisch bevat maar de afmeting geen waarde bevatte. U kunt de naam van dit dimensie-item kiezen, het geheel verbergen of het zelfs als een werkelijke waarde behandelen.

![Geen waardeopties](../assets/no-value-options.png)

## Instellingen {#settings}

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL If shown, call "No value"] | Een tekstveld waarin u de naam van de **[!UICONTROL No value]** dimensie-item naar iets anders. |
| [!UICONTROL Don't show No value by default] | Deze waarde wordt niet weergegeven in de rapportage. Metrische voorvallen die niet aan deze dimensie zijn gekoppeld, zijn niet zichtbaar in het rapport. |
| [!UICONTROL Show No value by default] | Deze waarde wordt in de rapportage weergegeven. |
| [!UICONTROL Treat No value as a value] | Hiermee vervangt u lege waarden in de gegevens door de tekst die u onder [!UICONTROL If shown, call "No value"]. Als u bijvoorbeeld Mobiel apparaattypen als de dimensie had, kunt u de naam van de component **[!UICONTROL No value]** item naar &quot;Computer&quot;. Wanneer u dit veld wijzigt in een aangepaste waarde, wordt de aangepaste waarde beschouwd als een geldige tekenreekswaarde. Als u de waarde &quot;Rood&quot; in dit veld invoert, worden alle instanties van de tekenreeks &quot;Rood&quot; die in de gegevens zelf worden weergegeven, daarom onder hetzelfde lijstitem als u hebt opgegeven. |

{style="table-layout:auto"}

## Blogbericht

Hier is een gerelateerd blogbericht over [verwerken van &quot;geen waarde&quot; in CJA](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/handling-quot-no-value-quot-in-customer-journey-analytics/ba-p/597339).
