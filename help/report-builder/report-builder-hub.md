---
title: Wat is de Hub van de Report Builder in Customer Journey Analytics
description: Beschrijft de componenten van de Hub van Report Builder
role: Data Engineer, Data Architect, Admin, User
feature: Report Builder
type: Documentation
exl-id: 119bd0b5-0d07-407f-b6e9-ef43352bad31
solution: Customer Journey Analytics
source-git-commit: abdf9dc510ebf929be2ca6be02ea60a83785a6f7
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Report Builder Hub

Gebruik de hub van Report Builder om gegevensblokken tot stand te brengen, bij te werken, te schrappen en te beheren.

De Report Builder-hub bevat de knoppen Maken en Beheren, de lijst OPDRACHTEN en de deelvensters SNEL BEWERKEN.

<img src="./assets/hub51.png" width="50%"/>


## Knoppen maken en beheren

Met de knoppen Maken of Beheren kunt u nieuwe gegevensblokken maken of bestaande gegevensblokken beheren.

## Deelvenster OPDRACHTEN

Gebruik het deelvenster OPDRACHTEN voor toegang tot opdrachten die compatibel zijn met de geselecteerde cellen of een vorige handeling.

![](./assets/hub1.png)

### Opdrachten

| Weergegeven opdrachten | Beschikbaar als... | Doel |
|------|------------------|--------|
| Gegevensblok maken | Één of meerdere cellen wordt geselecteerd in het werkboek. | Wordt gebruikt om een gegevensblok te maken |
| Gegevensblok bewerken | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Used to edit a data block |
| Gegevensblok vernieuwen | De selectie bevat ten minste één gegevensblok. De opdracht vernieuwt alleen de gegevensblokken in de selectie. | Used to refresh one or more data blocks |
| Alle gegevensblokken vernieuwen | Het werkboek bevat één of meerdere gegevensblokken. | Gebruikt om ALLE gegevensblokken in het werkboek te verfrissen |
| Gegevensblok kopiëren | De geselecteerde cel of het geselecteerde celbereik maakt deel uit van een of meer gegevensblokken. | Wordt gebruikt om een gegevensblok te kopiëren |
| Gegevensblok verwijderen | The selected cell or cells range is part of one data block only. | Wordt gebruikt om een gegevensblok te verwijderen |

## Deelvenster SNEL BEWERKEN

Wanneer u een of meer gegevensblokken in een spreadsheet selecteert, geeft Report Builder het deelvenster SNEL BEWERKEN weer. U kunt het deelvenster SNEL BEWERKEN gebruiken om parameters in één gegevensblok te wijzigen of om parameters in meerdere gegevensblokken tegelijk te wijzigen.

![](./assets/hub2.png)

De wijzigingen die u hebt aangebracht met de secties Snel bewerken zijn van toepassing op alle geselecteerde gegevensblokken.

### Gegevensweergaven

Gegevensblokken trekken gegevens uit een geselecteerde gegevensweergave. Als er meerdere gegevensblokken zijn geselecteerd in een werkblad en deze geen gegevens ophalen uit dezelfde gegevensweergave, worden de **Gegevensweergaven** koppelingsweergaven *Meerdere*.

Wanneer u de gegevensweergave wijzigt, nemen alle gegevensblokken in de selectie de nieuwe gegevensweergave over. Componenten in het gegevensblok komen overeen met de nieuwe gegevensweergave op basis van bijvoorbeeld id ```evars```). If a component isn&#39;t found in a data block, a warning message is displayed and the component is removed from the data block.

To change the data view, select a new data view from the drop-down menu.

![](./assets/image16.png)

### Datumbereik

**Datumbereik** Hiermee geeft u het datumbereik voor de geselecteerde gegevensblokken weer. If multiple data blocks are selected with multiple date ranges, the **Datumbereik** koppelingsweergaven *Meerdere*.

### Filters

De **Filters** de verbinding toont een summiere lijst van de filters die door de geselecteerde gegevensblokken worden gebruikt. Als er meerdere gegevensblokken zijn geselecteerd met meerdere filters toegepast, wordt **Filters** koppelingsweergaven *Meerdere*.
