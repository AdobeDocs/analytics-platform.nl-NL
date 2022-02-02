---
title: Inclusief instellingen van waardecomponent
description: Omvat of sluit voorwaardelijk een afmetingspunt afhankelijk van zijn waarde uit.
exl-id: 1a3f8ab5-bd82-415a-989a-f93e6714df4b
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: c36dddb31261a3a5e37be9c4566f5e7ec212f53c
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Inclusief instellingen van waardecomponent

Met Waarden voor uitsluiten kunt u regels maken die afhankelijk zijn van de waarde van een dimensie-item. Waarden die niet voldoen aan de criteria die u instelt, worden in Analysis Workspace behandeld alsof ze nooit bestaan, hoewel de gegevens nog steeds bestaan in de onderliggende dataset.

![Inclusief uitsluiten](../assets/include-exclude.png)

| Instelling | Beschrijving/Hoofdletters gebruiken |
| --- | --- |
| [!UICONTROL Set include/exclude values] | Een selectievakje waarmee u voorwaarden kunt inschakelen waarin gegevens worden opgenomen in een gegevensweergave. |
| [!UICONTROL Case sensitive] | Zichtbaar op de gegevenstypen van het schema van het Koord. Standaard ingeschakeld. Deze instelling is alleen van toepassing op de [!UICONTROL Include/Exclude Values] niet naar de resulterende waarde. Het staat u toe om te specificeren als de regel gevoelig geval is. |
| [!UICONTROL Match] | Hier kunt u opgeven welke waarden u wilt gebruiken voor de rapportage voorafgaand aan de toewijzing en filters (bijvoorbeeld alleen waarden gebruiken die de uitdrukking &quot;fout&quot; bevatten). U kunt **[!UICONTROL If all criteria are met]** of **[!UICONTROL If any criteria are met]**. |
| [!UICONTROL Criteria] | Hier geeft u de logica op die moet worden toegepast op een bepaalde filterregel.<ul><li>**String**: Bevat de uitdrukking, Bevat om het even welke termijn, Bevat alle termijnen, bevat geen termijn, bevat niet de uitdrukking, Gelijk, is niet gelijk, Begint met, Eind met</li><li>**Dubbel/geheel getal**: gelijk aan, niet gelijk aan, groter dan, kleiner dan, groter dan of gelijk aan, kleiner dan of gelijk aan</li><li>**Datum**: is gelijk aan, niet gelijk aan, is later dan, is eerder, komt voor binnen</li></ul> |
| [!UICONTROL Match operand] | Hier geeft u de overeenkomende operand op waarop de overeenkomende operator moet worden toegepast.<ul><li>**String**: Tekstveld</li><li>**Dubbel/geheel getal**: Tekstveld met pijl-omhoog/pijl-omlaag voor numerieke waarden</li><li>**Datum**: Selector voor daggranulariteit (kalender)</li><li>**Datum en tijd**: Selector voor granulariteit voor datum en tijd</li></ul> |
| [!UICONTROL Add rule] | Hier kunt u een extra match-operator en -operand opgeven. |
