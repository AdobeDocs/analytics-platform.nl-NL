---
description: Leer hoe u geplande projecten beheert.
title: Geplande projecten
feature: Components
exl-id: fa7c5a0f-4983-40ee-b9c1-3e10aab3fc28
role: User
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---

# Geplande projecten

Geplande Analysis Workspace-projecten kunnen in Customer Journey Analytics worden beheerd met **[!UICONTROL Components]** > **[!UICONTROL Scheduled projects]** .

In **[!UICONTROL Scheduled Projects]** kunt u terugkerende projectschema&#39;s bewerken en verwijderen.  De [&#x200B; Geplande projectlijst &#x200B;](#scheduled-project-list) toont de punten die een specifieke gebruiker heeft gecreeerd. Als de gebruikersaccount in de toepassing is uitgeschakeld, worden alle geplande leveringen gestopt.

![&#x200B; Geplande projecteninterface &#x200B;](assets/scheduled-projects.png)

## Geplande projectlijst

In de lijst Geplande projecten ➊ worden kolommen weergegeven voor:

| Kolom | Beschrijving |
| --- | --- |
| ![&#x200B; SelectBox &#x200B;](/help/assets/icons/SelectBox.svg) | Wanneer één of meerdere geplande projecten worden geselecteerd, verschijnt een blauwe actiebar bij de bodem van de Geplande interface van Projecten. Zie [&#x200B; Acties &#x200B;](#actions) voor meer details. |
| ![&#x200B; Ster &#x200B;](/help/assets/icons/Star.svg) | Selecteer om ![&#x200B; Ster &#x200B;](/help/assets/icons/Star.svg) of niet-gunst ![&#x200B; StarOutline &#x200B;](/help/assets/icons/StarOutline.svg) een gepland project te begunstigen. |
| **[!UICONTROL Schedule ID]** | Een id die vooral wordt gebruikt voor foutopsporingsdoeleinden. |
| **[!UICONTROL Name]** | Naam van dit project.<br/> Uitgezochte ![&#x200B; InfoOutline &#x200B;](/help/assets/icons/InfoOutline.svg) om meer details voor het geplande project te zien.<br/> Uitgezochte ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) om een contextmenu te openen. Vanuit dit menu kunt u:<ul><li>![&#x200B; Schrap &#x200B;](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** een gepland project.</li><li>![&#x200B; Etiketten &#x200B;](/help/assets/icons/Labels.svg) **[!UICONTROL Tag]** een gepland project.</li><li>![&#x200B; CheckmarkCircle &#x200B;](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Approve]** een gepland project.</li><li>![&#x200B; FileCSV &#x200B;](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export CSV]**: Exporteer een gepland project naar een CSV-bestand.</li></ul> |
| **[!UICONTROL Owner]** | De persoon die het project heeft gemaakt en bezit. |
| **[!UICONTROL Tags]** | (facultatief) het etiketteren is een goede manier om projecten te organiseren. Alle gebruikers kunnen labels maken en een of meer tags toepassen op een project. U kunt echter alleen labels zien voor de projecten die u hebt of die met u zijn gedeeld. |
| **[!UICONTROL Delivered to]** | De ontvangers van dit geplande project. |
| **[!UICONTROL Expiration date]** | U kunt de vervaldatum instellen op maximaal één jaar, ongeacht de frequentie van de planning. |
| **[!UICONTROL Frequency]** | Hoe vaak wilt u dit planningsproject hebben dat naar één of meerdere ontvangers wordt verzonden. |
| **[!UICONTROL Execution Time]** | Op welk tijdstip van de dag dit geplande project wordt verzonden. |
| **[!UICONTROL Number of Queries]** | Het aantal vragen tegen dit project. |
| **[!UICONTROL Longest Date Range]** | Het langste datumbereik dat is gedefinieerd voor het geplande project. Deze waarde kan relevant zijn om prestatieproblemen te onderzoeken. Zie [&#x200B; het Melden van de Manager van de Activiteit &#x200B;](/help/reporting-activity-manager/reporting-activity-overview.md) voor meer informatie. |
| **[!UICONTROL Number of queries]** | Het aantal vragen die voor het geplande project worden uitgevoerd. Deze waarde kan relevant zijn om prestatieproblemen te onderzoeken. Zie [&#x200B; het Melden van de Manager van de Activiteit &#x200B;](/help/reporting-activity-manager/reporting-activity-overview.md) voor meer informatie. |


U kunt ![&#x200B; gebruiken ColumnSetting &#x200B;](/help/assets/icons/ColumnSetting.svg) om te vormen welke kolommen aan vertoning.

Onderzoek naar een gepland project gebruikend ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg). U kunt ook zien of er filters zijn toegepast vanuit het deelvenster Filters. Om een filter te verwijderen, selecteer ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg) voor een filter. Selecteer **[!UICONTROL Clear all]** als u alle filters wilt verwijderen.

Als u een gepland project wilt bewerken, selecteert u de titel van het geplande project. Gebruik het dialoogvenster **[!UICONTROL Edit scheduled project]** om de planningsdetails bij te werken. Zie [&#x200B; dossiers naar andere &#x200B;](../analysis-workspace/export/t-schedule-report.md) voor meer details verzenden.

![&#x200B; geef gepland project &#x200B;](assets/edit-scheduled-project.png) uit

Selecteer **[!UICONTROL Update]** om het schema bij te werken.




## Handelingen

Het volgende is gemeenschappelijke acties in de Geplande Manager van Projecten. U kunt acties selecteren in het contextmenu of op de blauwe actiebalk wanneer u een of meer geplande projecten selecteert.

| Pictogram | Handeling | Beschrijving |
|:---:|---|---|
| ![&#x200B; dicht &#x200B;](/help/assets/icons/Close.svg) | **[!UICONTROL *x *geselecteerd]** | Selecteer deze optie om de selectie van uw geselecteerde geplande projecten op te heffen. |
| ![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder de geselecteerde geplande projecten voor het project. De projecten worden niet verwijderd.  <p>Voor informatie over het schrappen van een project, zie [&#x200B; Overzicht van Projecten &#x200B;](/help/analysis-workspace/build-workspace-project/freeform-overview.md).</p> |
| ![&#x200B; Etiketten &#x200B;](/help/assets/icons/Labels.svg) | **[!UICONTROL Tag]** | Geef labels aan de geselecteerde geplande projecten. Selecteer in **[!UICONTROL Tag Scheduled projects]** tags en selecteer **[!UICONTROL Save]** om op te slaan. |
| ![&#x200B; CheckmarkCircle &#x200B;](/help/assets/icons/CheckmarkCircle.svg) | **[!UICONTROL Approve]** | Goedkeuren van de geselecteerde geplande projecten. |
| ![&#x200B; FileCSV &#x200B;](/help/assets/icons/FileCSV.svg) | **[!UICONTROL Export to CSV]** | Exporteer de geselecteerde geplande projecten naar het bestand `Export Scheduled Projects List.csv` . |


## Filter

U kunt de geplande projecten [&#x200B; Geplande lijst van het Project &#x200B;](#scheduled-project-list) filtreren gebruikend het filterpaneel ➌. Om het gebruik van het filterpaneel te tonen of te verbergen ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg).

Het filterdeelvenster bestaat uit de volgende secties.

### Tags

| Tags | Beschrijving |
|---|---|
| ![&#x200B; Markeringen &#x200B;](/help/components/assets/scheduledprojects-filter-tags.png){width="300"} | In de sectie **[!UICONTROL Tags]** kunt u filteren op tags. <ul><li>U gebruikt ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) **[!UICONTROL Search Tags]** om naar markeringen te zoeken u wilt gebruiken om te filtreren.</li><li>U kunt meerdere tags selecteren. Welke labels beschikbaar zijn, is afhankelijk van de selecties die in andere secties in het filterdeelvenster zijn gemaakt.</li><li>De getallen geven aan:<ul><li>7︎⃣: Het aantal geplande projecten dat aan de specifieke tag is gekoppeld.</li></ul></li></ul> |


### Eigenaars

| Eigenaar | Beschrijving |
|---|---|
| ![&#x200B; Eigenaars &#x200B;](/help/components/assets/scheduledprojects-filter-owners.png){width="300"} | In de sectie **[!UICONTROL Owner]** kunt u filteren op eigenaars. <ul><li>U gebruikt ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) *eigenaars van het Onderzoek* aan onderzoek naar eigenaars u wilt gebruiken om te filtreren.</li><li>U kunt meerdere eigenaars selecteren. Welke eigenaars beschikbaar zijn, is afhankelijk van de selecties die in andere secties in het filterdeelvenster zijn gemaakt.</li><li>De getallen geven aan:<ul><li>4︎⃣: Het aantal geplande projecten dat aan de specifieke eigenaar is gekoppeld.</li></ul></li></ul> |


### Overige filters

| Overige filters | Beschrijving |
|---|---|
| ![&#x200B; Andere filters &#x200B;](/help/components/assets/scheduledprojects-filter-otherfilters.png){width="300"} | Met de sectie **[!UICONTROL Other filters]** kunt u filteren op een ander vooraf gedefinieerd filter.<ul><li>U kunt een of meer van de volgende opties selecteren:<ul><li> **[!UICONTROL Expired]**: filter op verlopen geplande projecten.</li><li>**[!UICONTROL Failed]**: filter op geplande projecten waarvoor de planning is mislukt.</li></ul>Wat u kunt selecteren hangt van uw rol en toestemmingen af.</li><li>U kunt meerdere filters selecteren. Welke andere filters beschikbaar zijn, is afhankelijk van de selecties die in andere secties van het filterdeelvenster zijn gemaakt.</li><li>De getallen geven aan:<ul><li>4︎⃣: Het aantal geplande projecten dat is gekoppeld aan het specifieke andere filter.</li></ul></li></ul> |
