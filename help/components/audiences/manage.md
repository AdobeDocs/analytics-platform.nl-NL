---
title: Leer hoe u het publiek dat in de Customer Journey Analytics is gemaakt, kunt beheren
description: Leer hoe u het publiek in de Customer Journey Analytics beheert
exl-id: 0cc50f64-40b5-4245-a9bb-a60fc90f507a
feature: Audiences
role: User
source-git-commit: 8676497c9341e3ff74d1b82ca79bc1e73caf514f
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 1%

---

# Soorten publiek beheren

Soorten publiek kan in Customer Journey Analytics worden beheerd met **[!UICONTROL Components]** > **[!UICONTROL Audiences]** .

Door eerder gemaakte soorten publiek te beheren, kunt u:

* **Programma of de-planning** automatisch publiek verfrist zich/werkt bij. De maximale vervaldatum in de planning is 1 jaar.
* **vernieuw een publiek verfrist programma** wanneer het op het punt staat te verlopen. Het uitbreiden van het publiek wordt op dezelfde manier behandeld als het verlopen van geplande rapporten - admin krijgt een e-mail een maand alvorens het programma verloopt.
* Bekijk **verfris interval** en de **laatste tijd dat een publiek** werd bijgewerkt
* Het inzicht van de winst in de **hoeveelheid tijd het nam om een publiek** van Customer Journey Analytics te produceren. En de hoeveelheid tijd die nodig was om het publiek in real-time klantplatform te laten verschijnen voor activeringsdoeleinden.
* Zie of het publiek in Customer Journey Analytics **actief door het Platform van de Klant in real time** wordt gebruikt. Of (ideaal) om het even welke Experience Platform toepassingen die het publiek verbruiken dat door Customer Journey Analytics wordt gecreeerd.

Als u ](/help/technotes/access-control.md#user-level-access) toegang hebt van de Mening van het publiek [ {, kunt u publiek bekijken. Als u [ publiek hebt leidt tot ](/help/technotes/access-control.md#user-level-access) toegang, kunt u publiek uitgeven en schrappen. De [ lijst van Soorten publiek ](#audiences-list) toont het publiek.

## Publiek

In de lijst Soorten publiek ➊ worden kolommen weergegeven voor:

| Kolom | Beschrijving |
| --- | --- |
| ![ SelectBox ](/help/assets/icons/SelectBox.svg) | Wanneer een of meer soorten publiek zijn geselecteerd, wordt een blauwe actiebalk onder aan de interface Soorten publiek weergegeven. Zie [ Acties ](#actions) voor meer details. |
| **[!UICONTROL Title & Description]** | De titel en beschrijving die u hebt ingevoerd toen u het publiek hebt gemaakt. |
| **[!UICONTROL Data view]** | De gegevensweergave waarin dit publiek is gemaakt. |
| **[!UICONTROL Audience size]** | Het totale aantal mensen in dit publiek. |
| **[!UICONTROL Owner]** | De eigenaar van het publiek - de persoon die het publiek creëerde. |
| **[!UICONTROL Refresh frequency]** | Het vernieuwde interval dat werd gevormd toen het publiek werd gecreeerd. |
| **[!UICONTROL Tags]** | Alle tags die op dit publiek zijn toegepast. |
| **[!UICONTROL Publishing status]** | Kan ![ StatusGreen ](/help/assets/icons/StatusGreen.svg) tonen **[!UICONTROL Ready]**, ![ StatusGray ](/help/assets/icons/StatusGray.svg) **[!UICONTROL In progress]**, of ![ StatusRed ](/help/assets/icons/StatusRed.svg) **[!UICONTROL Error]**. |
| **[!UICONTROL Last refreshed]** | Tijdstempel wanneer het publiek voor het laatst is vernieuwd. |
| **[!UICONTROL Last modified]** | Tijdstempel wanneer het publiek voor het laatst is bewerkt of gewijzigd. |

U kunt ![ gebruiken ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te vormen welke kolommen aan vertoning. Onderzoek naar een publiek gebruikend ![ Onderzoek ](/help/assets/icons/Search.svg).

Een publiek bewerken:

1. Selecteer de titel van het publiek. Gebruik het dialoogvenster **[!UICONTROL Edit audience project]** om het publiek bij te werken. Zie [ Bouwer van de Publiek ](publish.md#audience-builder) voor meer details.

1. Selecteer **[!UICONTROL Republish]** om het publiek opnieuw te publiceren.


## Handelingen

Het volgende is gemeenschappelijke acties in de Geplande Manager van Projecten. U kunt handelingen selecteren in het contextmenu:

| Pictogram | Handeling | Beschrijving |
|:---:|---|---|
| ![ Etiketten ](/help/assets/icons/Labels.svg) | **[!UICONTROL Tag]** | Label het geselecteerde publiek. In de **[!UICONTROL Update tags: *dialoog van de publieksnaam *]**, uitgezochte markeringen van het dropdown menu of type één of meerdere nieuwe markeringen. Selecteer **[!UICONTROL Save]**voor opslaan. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder het geselecteerde publiek. |
| ![ geeft ](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Rename]** | Wijzig de naam van het geselecteerde publiek. Gebruik de **[!UICONTROL Rename: *dialoog van de publieksnaam *]**om het publiek anders te noemen en **[!UICONTROL Save]**te selecteren om te bewaren. |

De volgende acties zijn beschikbaar op de blauwe actiebalk wanneer u een of meer geplande projecten selecteert.

| Pictogram | Handeling | Beschrijving |
|:---:|---|---|
| ![ dicht ](/help/assets/icons/Close.svg) | **[!UICONTROL *x *geselecteerd]** | Selecteer deze optie om de selectie van het geselecteerde publiek op te heffen. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder het geselecteerde publiek. |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) | **[!UICONTROL Export to CSV]** | Exporteer het geselecteerde publiek naar het bestand `audiences.csv` . |

## Filter

U kunt de [ lijst van Soorten van publiek ](#audiences-list) filtreren gebruikend de ➋ van het filterpaneel. Om het gebruik van het filterpaneel te tonen of te verbergen ![ Filter ](/help/assets/icons/Filter.svg).

Het filterdeelvenster bestaat uit de volgende secties.

### Gegevens, weergave

| Gegevens, weergave | Beschrijving |
|---|---|
| ![ Eigenaars ](/help/components/audiences/assets/audiences-filter-dataviews.png){width="300"} | In de sectie **[!UICONTROL Data view]** kunt u filteren op gegevensweergaven. <ul><li>U gebruikt ![ Onderzoek ](/help/assets/icons/Search.svg) om naar gegevensmeningen te zoeken u aan filter wilt gebruiken.</li><li>U kunt meerdere gegevensweergaven selecteren.</li></ul> |

### Eigenaars

| Eigenaar | Beschrijving |
|---|---|
| ![ Eigenaars ](/help/components/audiences/assets/audiences-filter-owner.png){width="300"} | In de sectie **[!UICONTROL Owner]** kunt u filteren op eigenaars. <ul><li>U gebruikt ![ Onderzoek ](/help/assets/icons/Search.svg) aan onderzoek naar eigenaars u wilt gebruiken om te filtreren.</li><li>U kunt meerdere eigenaars selecteren. </li></ul> |

## Frequentie vernieuwen

| Frequentie vernieuwen | Beschrijving |
|---|---|
| ![ verfrist frequentie ](/help/components/audiences/assets/audiences-filter-refreshfrequency.png){width="300"} | In de sectie **[!UICONTROL Refresh frequency]** kunt u filteren op vernieuwingsfrequentie. <ul><li>U gebruikt ![ Onderzoek ](/help/assets/icons/Search.svg) om naar te zoeken verfrist frequentie u wilt gebruiken om te filtreren.</li><li>Slechts verfrist de frequenties voor het publiek <br/> worden bepaald in de [ lijst van Soorten van publiek ](#audiences-list) worden getoond als beschikbare opties.</li></ul> |


### Tags

| Tags | Beschrijving |
|---|---|
| ![ Markeringen ](/help/components/audiences/assets/audiences-filter-tags.png){width="300"} | In de sectie **[!UICONTROL Tags]** kunt u filteren op tags. <ul><li>U gebruikt ![ Onderzoek ](/help/assets/icons/Search.svg) om naar markeringen te zoeken u wilt gebruiken om te filtreren. |
