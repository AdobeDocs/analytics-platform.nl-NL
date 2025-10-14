---
title: Een gegevensweergave selecteren in Report Builder
description: Beschrijft hoe te om gegevensmeningen in Adobe Report Builder te selecteren
role: User
feature: Report Builder
type: Documentation
solution: Customer Journey Analytics
exl-id: bf765144-34f8-465b-b06d-53e4ca91014a
source-git-commit: f03c82375a907821c8e3f40b32b4d4200a47323f
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Een gegevensweergave selecteren

U kunt een gegevensweergave selecteren in het keuzemenu of een gegevensweergave selecteren in een cel en uw gegevensblok automatisch bijwerken met een nieuwe gegevensweergave.

## Gegevens uit een cel selecteren

Als u een gegevensweergave in een cel selecteert, kunt u gegevensblokken eenvoudig vernieuwen met verschillende gegevensweergaven. In plaats van volledig nieuwe rapporten met afzonderlijke gegevensblokken te creëren, kunt u gegevensblokken met een gegevensmening verfrissen die van een cel wordt geselecteerd.

Het selecteren van een gegevensweergave in een cel is handig als u:

* Meerdere gegevensweergaven die op elkaar lijken of identiek zijn in structuur.
* Gecompliceerde gegevensblokindelingen die aangepaste componenten en lay-outs bevatten.

Als u een gegevensweergave in een cel wilt selecteren, maakt u eerst een gegevensblok en wijst u meerdere gegevensweergaven toe aan een cel buiten het gegevensblok. Gebruik vervolgens het deelvenster **[!UICONTROL Data view from cell]** om uw gegevensblokken van verschillende gegevensweergaven te vernieuwen.

1. Maak een gegevensblok. Voor informatie over het creëren van een gegevensblok, zie [&#x200B; een gegevensblok &#x200B;](/help/report-builder/create-a-data-block.md) creëren.

1. Selecteer ![&#x200B; DataViewSelector &#x200B;](/help/assets/icons/DataViewSelector.svg) in **[!UICONTROL Data views]**.

1. Selecteer een cel gebruikend ![&#x200B; DataBlockSelector &#x200B;](/help/assets/icons/DataBlockSelector.svg) buiten het gegevensblok.

1. Voeg een of meer gegevensweergaven van de **[!UICONTROL Select data views to add to data view from cell]** toe met slepen en neerzetten. U kunt ook een gegevensweergave selecteren om de gegevensweergave aan de lijst van **[!UICONTROL Data views included]** toe te voegen.

   * U kunt ![&#128279;](/help/assets/icons/Search.svg) **[!UICONTROL _Uitgezochte gegevensmeningen van het 0&rbrace; Onderzoek_]** gebruiken om naar gegevensmeningen te zoeken.
   * Gebruik ![&#x200B; MoreSmall &#x200B;](/help/assets/icons/MoreSmall.svg) om een contextmenu te openen zodat kunt u gegevensmeningen omhoog of onderaan in de **[!UICONTROL Data views included]** lijst bewegen.
   * Gebruik ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg) om een gegevensmening van de **[!UICONTROL Data views included]** lijst te schrappen.

   ![&#x200B; Uitgezochte gegevensmening van een cel &#x200B;](assets/dataviews-from-a-cell.png){zoomable="yes"}

1. Selecteer **[!UICONTROL Apply]** om de geselecteerde gegevensweergaven toe te passen op de geselecteerde cel.


## De gegevensweergave vanuit een cel wijzigen

1. Selecteer de locatie van de gegevensweergavecel in het vel.
1. Selecteer in de Report Builder-hub de koppeling **[!UICONTROL Data views from cell]** in **[!UICONTROL Quick edit]** .
1. Selecteer een gegevensweergave in het vervolgkeuzemenu **[!UICONTROL Data view]** .

   ![&#x200B; de gegevensmening van de Verandering van een cel &#x200B;](assets/change-data-view-from-cell.png){zoomable="yes"}
1. Selecteer **[!UICONTROL Refresh data block(s) upon change]** Optioneel.

1. Selecteer **[!UICONTROL Apply]** . Report Builder vernieuwt het gegevensblok op basis van de geselecteerde gegevensweergave.
