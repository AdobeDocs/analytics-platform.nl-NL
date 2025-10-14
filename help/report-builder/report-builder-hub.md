---
title: Wat is de Report Builder Hub in Customer Journey Analytics
description: Beschrijft de componenten van de Hub van Report Builder
role: User
feature: Report Builder
type: Documentation
exl-id: 119bd0b5-0d07-407f-b6e9-ef43352bad31
solution: Customer Journey Analytics
source-git-commit: 065cf61d80ceb3c921ea666ba299e56fb044335b
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Report Builder hub

De hub van Report Builder is de juiste ruit die binnen uw werkboek van Excel wordt getoond wanneer u ![&#x200B; AdobeLogoRedonWhite &#x200B;](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** van de bar van het lint van Excel selecteert.

Met de Report Builder-hub kunt u gegevensblokken maken, bijwerken, verwijderen en beheren.

De hub van Report Builder bevat ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**, ![&#x200B; TableManage &#x200B;](/help/assets/icons/TableManage.svg) **[!UICONTROL Manage]** en ![&#x200B; Kalender &#x200B;](/help/assets/icons/Calendar.svg) **[!UICONTROL Schedule]** knopen, het **[!UICONTROL Commands]** paneel, en het **[!UICONTROL Quick edit]** paneel.

![&#x200B; hub van Report Builder &#x200B;](assets/hub51.png){zoomable="yes"}


Selecteren

* ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]** [&#x200B; creeert nieuwe gegevensblokken &#x200B;](create-a-data-block.md).
* ![&#x200B; TableManage &#x200B;](/help/assets/icons/TableManage.svg) **[!UICONTROL Manage]** aan [&#x200B; beheer bestaande gegevensblokken &#x200B;](manage-reportbuilder.md).
* ![&#x200B; Kalender &#x200B;](/help/assets/icons/Calendar.svg) **[!UICONTROL Schedule]** aan [&#x200B; beheert programma&#39;s om uw werkboek door e-mail &#x200B;](schedule-reportbuilder.md) te verzenden.

## Opdrachten, deelvenster

Gebruik het deelvenster **[!UICONTROL Commands]** voor toegang tot opdrachten die compatibel zijn met de geselecteerde cellen of een vorige handeling.

| Opdrachten | Beschikbaar als... | Doel |
|------|------------------|--------|
| ![&#x200B; geef &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit data block]** uit | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Wordt gebruikt om een gegevensblok te bewerken. |
| ![&#x200B; verfrissen zich &#x200B;](/help/assets/icons/Refresh.svg) **[!UICONTROL Refresh data block]** | De selectie bevat ten minste één gegevensblok. Met deze opdracht vernieuwt u alleen de gegevensblokken in de selectie. | Vernieuw een of meer gegevensblokken. |
| ![&#x200B; DocumentRefresh &#x200B;](/help/assets/icons/DocumentRefresh.svg) **[!UICONTROL Refresh all data blocks]** | Het werkboek bevat één of meerdere gegevensblokken. | Gebruik om alle gegevensblokken in het werkboek te verfrissen |
| ![&#x200B; verzend &#x200B;](/help/assets/icons/Send.svg) **[!UICONTROL Send workbook]** | Het werkboek bevat één of meerdere gegevensblokken. | Gebruik om het werkboek als dossier door e-mail te verzenden. |
| ![&#x200B; Exemplaar &#x200B;](/help/assets/icons/Copy.svg) **[!UICONTROL Copy data block]** | De geselecteerde cel of het geselecteerde celbereik maakt deel uit van een of meer gegevensblokken. | Wordt gebruikt om een gegevensblok te kopiëren. |
| ![&#x200B; Besnoeiing &#x200B;](/help/assets/icons/Cut.svg) **[!UICONTROL Cut data block]** | De geselecteerde cel of het geselecteerde celbereik maakt deel uit van een of meer gegevensblokken. | Zie om een gegevensblok te knippen. |
| ![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) **[!UICONTROL Delete data block]** | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Gebruiken om een gegevensblok te verwijderen |

## Deelvenster Snel bewerken

Wanneer u een of meer gegevensblokken in een spreadsheet selecteert, geeft Report Builder het deelvenster **[!UICONTROL Quick edit]** weer. U kunt het deelvenster **[!UICONTROL Quick edit]** gebruiken om parameters in een of meer gegevensblokken tegelijk te wijzigen.

De wijzigingen die u aanbrengt wanneer u de secties **[!UICONTROL Quick Edit]** gebruikt, zijn van toepassing op alle geselecteerde gegevensblokken.

### Gegevensweergaven

Gegevensblokken trekken gegevens uit een geselecteerde gegevensweergave. Als de veelvoudige gegevensblokken in een aantekenvel worden geselecteerd en zij trekken geen gegevens van de zelfde gegevensmening, de **verbindingsvertoningen van de meningen van Gegevens**&#x200B;[!UICONTROL _ Veelvoud _]&#x200B;**.**

Wanneer u de gegevensweergave wijzigt, nemen alle gegevensblokken in de selectie de nieuwe gegevensweergave over. Componenten in het gegevensblok worden op basis van ID aangepast aan de nieuwe gegevensweergave. Als een component niet in een gegevensblok wordt gevonden, wordt de component verwijderd en met **[!UICONTROL Invalid value]** vervangen of ![&#x200B; AlertRed &#x200B;](/help/assets/icons/AlertRed.svg) wordt getoond voor de specifieke component.

Als u de gegevensweergave wilt wijzigen, selecteert u een nieuwe gegevensweergave in de vervolgkeuzelijst **[!UICONTROL Data view]** .


### Datumbereik

**waaier van de Datum** toont de datumwaaier voor de geselecteerde gegevensblokken. Als de veelvoudige gegevensblokken met veelvoudige datumwaaiers worden geselecteerd, **[!UICONTROL Date range]** verbindingsvertoningen **[!UICONTROL _Veelvoud_]**.

### Segmenten

De **verbinding van Segmenten** toont een summiere lijst van de segmenten die door de geselecteerde gegevensblokken worden gebruikt. Als de veelvoudige gegevensblokken met veelvoudige toegepaste segmenten worden geselecteerd, de **verbindingsvertoningen van segmenten**&#x200B;[!UICONTROL _ Veelvoudig _]&#x200B;**.**

>[!MORELIKETHIS]
>
>[&#x200B; selecteer een gegevensmeningen &#x200B;](select-data-view.md)
>[Selecteer een datumbereik &#x200B;](select-date-range.md)
>[Werken met filters &#x200B;](work-with-filters.md)
>
