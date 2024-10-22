---
title: Inclusief instellingen van waardecomponent
description: Omvat of sluit voorwaardelijk een afmetingspunt afhankelijk van zijn waarde uit.
exl-id: 1a3f8ab5-bd82-415a-989a-f93e6714df4b
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: 555dbd5c84fbec7c71b328229da5196fe2e64b76
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Inclusief instellingen van waardecomponent {#include-exclude-values-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_metric_includeexcludevalues"
>title="Waarden uitsluiten opnemen"
>abstract="Filter een metrische waarde om alleen waarden te tellen die aan specifieke criteria voldoen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_dimension_includeexcludevalues"
>title="Waarden uitsluiten opnemen"
>abstract="Verfijn een dimensie om alleen waarden op te nemen die aan specifieke criteria voldoen. Opnamen en uitsluitingen vinden plaats vóór de toewijzing en filters in rapporten.<br/><br/>**Gevoelige Geval van Parameters **<br/>****: Bepaal als de filterlogica hieronder case-sensitive is."

<!-- markdownlint-enable MD034 -->

Met Waarden voor uitsluiten kunt u regels maken die afhankelijk zijn van de waarde van een dimensie-item. Waarden die niet voldoen aan de criteria die u instelt, worden in Analysis Workspace behandeld alsof ze nooit bestaan, hoewel de gegevens nog steeds bestaan in de onderliggende dataset.

![ de meningsvenster van Gegevens die omvatten sluit waarden ](../assets/include-exclude.png) uit

| Instelling | Omschrijving/gebruik |
| --- | --- |
| [!UICONTROL Set include/exclude values] | Een selectievakje waarmee u voorwaarden kunt inschakelen waarin gegevens worden opgenomen in een gegevensweergave. |
| [!UICONTROL Case sensitive] | Zichtbaar op de gegevenstypen van het schema van het Koord. Standaard ingeschakeld. Deze instelling is alleen van toepassing op de [!UICONTROL Include/Exclude Values] -logica, niet op de resulterende waarde. Het staat u toe om te specificeren als de regel gevoelig geval is. |
| [!UICONTROL Match] | Hier kunt u opgeven welke waarden u wilt gebruiken voor de rapportage voorafgaand aan de toewijzing en filters (bijvoorbeeld alleen waarden gebruiken die de uitdrukking &quot;fout&quot; bevatten). U kunt **[!UICONTROL If all criteria are met]** of **[!UICONTROL If any criteria are met]** opgeven. Scheid elke waarde met een spatie. |
| [!UICONTROL Criteria] | Hier geeft u de logica op die moet worden toegepast op een bepaalde filterregel.<ul><li>**Koord**: [!UICONTROL Contains the phrase], [!UICONTROL Contains any term], [!UICONTROL Contains all terms], [!UICONTROL Does not contain any term], [!UICONTROL Does not contain the phrase], [!UICONTROL Equals], [!UICONTROL Does not equal], [!UICONTROL Starts with], [!UICONTROL Ends with]</li><li>**dubbel/Geheel**: [!UICONTROL Equals], [!UICONTROL Does not equal], [!UICONTROL Is greater than], [!UICONTROL Is less than], [!UICONTROL Is greater than or equal to], [!UICONTROL Is less than or equal to]</li><li>**Datum**: [!UICONTROL Equals], [!UICONTROL Does not equal], [!UICONTROL Is later than], [!UICONTROL Is before], [!UICONTROL Occurs within]</li></ul> |
| [!UICONTROL Match operand] | Hier geeft u de overeenkomende operand op waarop de overeenkomende operator moet worden toegepast.<ul><li>**Koord**: Het gebied van de Tekst</li><li>**dubbel/Geheel Geheel**: Het Gebied van de tekst met omhoog/onderaan pijlen voor numerieke waarden</li><li>**Datum**: De selecteur van de granulariteit van de dag (kalender)</li><li>**Tijd van de Datum**: De selecteur van de datum en van de tijdgranulariteit</li></ul> |
| [!UICONTROL Add rule] | Hier kunt u een extra match-operator en -operand opgeven. |

{style="table-layout:auto"}
