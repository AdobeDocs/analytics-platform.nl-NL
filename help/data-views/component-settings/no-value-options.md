---
title: Componentinstellingen voor geen waardeopties
description: Bepaal hoe een dimensie moet worden verwerkt als deze leeg is.
exl-id: c7f226c5-0058-4151-9c9a-652b37266beb
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: c526531206887acf7c750c8759d4eec5dd24935f
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Componentinstellingen voor Geen waardopties {#no-value-options-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_dimension_novalueoptions"
>title="Geen waardeopties"
>abstract="Vorm het standaardgedrag voor wanneer geen waarde in een afmeting aanwezig is."

<!-- markdownlint-enable MD034 -->


[!UICONTROL No value options] laat u bepalen hoe Analysis Workspace situaties behandelt waar een gebeurtenis in een dataset metrisch bevat maar de afmeting geen waarde bevatte. U kunt de naam van dit dimensie-item kiezen, het geheel verbergen of het zelfs als een werkelijke waarde behandelen.

![&#x200B; Geen waardeopties &#x200B;](../assets/no-value-options.png)

## Instellingen {#settings}

| Instelling | Beschrijving |
| --- | --- |
| **[!UICONTROL If shown, call "No value"]** | Een tekstveld waarin u de naam van het dimensie-item **[!UICONTROL No value]** kunt wijzigen in iets anders. |
| **[!UICONTROL Don't show "No value" by default]** | Deze waarde wordt niet weergegeven in de rapportage. Metrische voorvallen die niet aan deze dimensie zijn gekoppeld, zijn niet zichtbaar in het rapport. |
| **[!UICONTROL Show "No value" by default]** | Deze waarde wordt in de rapportage weergegeven. |
| **[!UICONTROL Treat "No value" as a value]** | (Niet ondersteund voor numerieke afmetingen) Hiermee vervangt u lege waarden in de gegevens door de tekst die u onder [!UICONTROL If shown, call "No value"] hebt opgegeven. Als u bijvoorbeeld mobiele apparaattypen als afmetingen hebt, kunt u de naam van het item **[!UICONTROL No value]** wijzigen in &quot;Computer&quot;. Wanneer u dit veld wijzigt in een aangepaste waarde, wordt de aangepaste waarde beschouwd als een geldige tekenreekswaarde. Als u de waarde &quot;Rood&quot; in dit veld invoert, worden alle instanties van de tekenreeks &quot;Rood&quot; die in de gegevens zelf worden weergegeven, daarom onder hetzelfde lijstitem als u hebt opgegeven. |

## Ondersteuning voor Geen waarde voor numerieke afmetingen {#numeric}

Wanneer u een numerieke waarde als een afmeting gebruikt, kunt u

* Configureer de optie Geen waarde in een gegevensweergave. Alle hierboven weergegeven configuratie-instellingen worden ondersteund, behalve **[!UICONTROL Treat "No value" as a value]** .
* Gebruik **[!UICONTROL Include "No value"]** voor numerieke afmetingen in een tabel voor vrije vorm in Workspace.
* Gebruik in de Segment Builder de operatoren **[!UICONTROL exists]** of **[!UICONTROL does not exist]** met numerieke afmetingen.


>[!MORELIKETHIS]
>
>[&#x200B; Volledige playbook voor behandeling &quot;Geen waarde&quot;in Adobe Customer Journey Analytics &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/the-complete-playbook-for-handling-no-value-in-adobe-cja/ba-p/756696#M598).


