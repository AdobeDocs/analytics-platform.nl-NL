---
title: Een gegevensblok maken in Report Builder
description: Leer hoe u een gegevensblok maakt.
role: User
feature: Report Builder
type: Documentation
exl-id: 46382621-d5e1-41d6-865c-782ec28a21fa
solution: Customer Journey Analytics
source-git-commit: 31d3b40ad7a081aefa4297d7f4a3b986711ead03
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# Een gegevensblok maken

A *gegevensblok* is de lijst van gegevens die door één enkel gegevensverzoek worden gecreeerd. Een werkboek van Report Builder kan veelvoudige gegevensblokken bevatten. Wanneer u een gegevensblok creeert, vorm eerst het gegevensblok en bouwt dan het gegevensblok.

## Het gegevensblok configureren

Vorm de aanvankelijke parameters van het gegevensblok voor de het blokplaats van Gegevens, de meningen van Gegevens, en een waaier van de Datum.

1. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**.

   ![&#x200B; Schermafbeelding die de Create optie van het gegevensblok toont &#x200B;](./assets/create-data-block.png){zoomable="yes"}


1. Stel de **[!UICONTROL Data block location]** in.

   Met de optie voor gegevensbloklocatie definieert u de werkbladlocatie waar Report Builder de gegevens aan het werkblad toevoegt.

   Als u de locatie van het gegevensblok wilt opgeven, selecteert u één cel in het werkblad of voert u een celadres in, bijvoorbeeld `a3` , `\\\$a3` , `a\\\$3` of `sheet1!a2` . De opgegeven cel wordt de linkerbovenhoek van het gegevensblok wanneer de gegevens worden opgehaald.

   Het gebruik ![&#x200B; DataBlockSelector &#x200B;](/help/assets/icons/DataBlockSelector.svg) om een plaats van het gegevensblok van de huidige geselecteerde cel in het blad te kiezen.

1. Kies de **[!UICONTROL Data views]** .

   Met de optie Gegevens kunt u een gegevensweergave kiezen in een vervolgkeuzelijst of naar een gegevensweergave verwijzen vanuit een cellocatie.

   Selecteer ![&#x200B; DataViewSelector &#x200B;](/help/assets/icons/DataViewSelector.svg) om een gegevensmening van een cel tot stand te brengen.

1. Stel de **[!UICONTROL Date range]** in.

   Met de optie **[!UICONTROL Date range]** kunt u een datumbereik kiezen. Datumbereiken kunnen vast zijn of doorlopen.

   Selecteer **[!UICONTROL Calendar]** om een gegevenswaaier te plukken gebruikend ![&#x200B; Kalender &#x200B;](/help/assets/icons/Calendar.svg) of een datumwaaier manueel in te gaan. Naar keuze, kunt u vooraf ingesteld van het **[!UICONTROL _Onderzoek kiezen stelt_]** drop-down menu vooraf in.

   Selecteer **[!UICONTROL From cell]** om een begin- en eindgegevens te definiëren op basis van een cel in het huidige blad.

   Voor informatie over de opties van de datumwaaier, zie [&#x200B; Selecteer een datumwaaier &#x200B;](select-date-range.md).

1. Selecteer **[!UICONTROL Next]**.

   ![&#x200B; Schermafbeelding die de optie van de datumwaaier en de actieve Volgende knoop tonen.](./assets/choose_date_data_view3.png)

   Nadat u het gegevensblok vormt, kunt u afmetingen, metriek, en segmenten selecteren om uw gegevensblok te bouwen. De tabbladen **[!UICONTROL Dimensions]** , **[!UICONTROL Metrics]** en **[!UICONTROL Segments]** worden boven het deelvenster **[!UICONTROL Table]** weergegeven.

## Het gegevensblok samenstellen

Om het gegevensblok te bouwen, selecteer rapportcomponenten, en pas dan de lay-out aan.

1. Voeg **[!UICONTROL Dimensions]** -, **[!UICONTROL Metrics]** - en **[!UICONTROL Segments]** -componenten toe.

   Schuif de componentenlijsten of gebruik het ![&#x200B; &#x200B;](/help/assets/icons/Search.svg) gebied van het Onderzoek van componenten **[!UICONTROL _om van componenten de plaats te bepalen._]** Sleep componenten naar het deelvenster [!UICONTROL Table] of selecteer een componentnaam in de lijst om de component aan het deelvenster [!UICONTROL Table] toe te voegen.

   Selecteer een component tweemaal om de component aan een standaardsectie van de lijst toe te voegen.

   - De componenten van Dimension worden toegevoegd aan ![&#x200B; TableSelectRow &#x200B;](/help/assets/icons/TableSelectRow.svg) **[!UICONTROL Row]** sectie of aan ![&#x200B; TableSelectColumn &#x200B;](/help/assets/icons/TableSelectColumn.svg) **[!UICONTROL Column]** sectie als u een afmeting reeds in de kolommen hebt.
   - De componenten van de datum worden toegevoegd aan de ![&#x200B; &#x200B;](/help/assets/icons/TableSelectColumn.svg) **[!UICONTROL Column]** sectie TableSelectColumn.
   - De componenten van het segment worden toegevoegd aan de ![&#x200B; sectie van de Segmentatie &#x200B;](/help/assets/icons/Segmentation.svg) **[!UICONTROL Segments]**.
   - De componenten van metriek worden toegevoegd aan de ![&#x200B; sectie van de Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **[!UICONTROL Values]**.

1. Rangschik de punten in de ruit van de Lijst om de lay-out van uw gegevensblok aan te passen.

   De belemmering en dalingscomponenten binnen elke lijst in de ruit van de Lijst om componenten opnieuw te ordenen of ![&#x200B; MeerSmall &#x200B;](/help/assets/icons/MoreSmall.svg) te selecteren en ![&#x200B; te selecteren ArrowUp &#x200B;](/help/assets/icons/ArrowUp.svg) Beweging omhoog, ![&#x200B; ArrowDown &#x200B;](/help/assets/icons/ArrowDown.svg) Beweging neer, en meer om componenten binnen een lijst te bewegen.

   Wanneer u componenten aan de lijst toevoegt, wordt een voorproef van het gegevensblok getoond bij de het blokplaats van Gegevens in het aantekenvel. De lay-out van de voorvertoning van gegevensblokken wordt automatisch bijgewerkt wanneer u items in de tabel toevoegt, verplaatst of verwijdert.

   ![&#x200B; Schermafbeelding die de toegevoegde componenten en het bijgewerkte werkblad tonen.](./assets/image10.png)


1. Stel desgewenst de **[!UICONTROL Start date]** in als een dimensie om de begindatum van uw gegevensblok te identificeren. Het toevoegen van de begingegevens als dimensie is nuttig als u een regelmatig gepland rapport hebt dat een het rollen datumwaaier heeft. Of als u een onconventioneel datumbereik hebt en u moet expliciet zijn over de begindatum.

   ![&#x200B; het Schermafbeelding die de datum van het Begin in de lijst van dimensies toont.](./assets/start-date-dimension.png)

1. U kunt ook rij- en kolomkoppen weergeven of verbergen. Daartoe:

   1. Selecteer het **[!UICONTROL Table]** ![&#x200B; Plaatsende &#x200B;](/help/assets/icons/Setting.svg) montagespictogram.

      ![&#x200B; Schermafbeelding die de de montagesoptie van de Lijst toont.](./assets/table-settings.png)

   1. Schakel de optie voor **[!UICONTROL Display row and column headers]** in of uit. De kopteksten worden standaard weergegeven.

1. U kunt desgewenst ook dimensielabels en metrische koppen verbergen of weergeven. Daartoe:

   1. Selecteer ![&#x200B; MoreSmall &#x200B;](/help/assets/icons/MoreSmall.svg) op het afmetingsetiket of de kolomkopbal om het contextmenu te tonen.

      ![&#x200B; het weglatingspictogram in de sectie van de Rij.](./assets/row-heading.png)

   1. Selecteer ![&#x200B; VisibilityOff &#x200B;](/help/assets/icons/VisibilityOff.svg) **[!UICONTROL Hide]** of ![&#x200B; Zichtbaarheid &#x200B;](/help/assets/icons/Visibility.svg) **[!UICONTROL Show]** om de afmetingsetiket of kolomkopbal van een knevel te voorzien. Alle labels worden standaard weergegeven.

1. Selecteer **[!UICONTROL Finish]** om de configuratie van uw gegevensblok te voltooien.

1. Er wordt een verwerkingsbericht **[!UICONTROL #BUSY]** weergegeven terwijl de analysegegevens worden opgehaald.

   ![&#x200B; Het verwerkingsbericht.](./assets/image11.png)

1. Report Builder haalt de gegevens op en geeft het voltooide gegevensblok weer in het werkblad.

   ![&#x200B; het voltooide gegevensblok.](./assets/image12.png)


>[!MORELIKETHIS]
>
>[&#x200B; selecteer een gegevensmening &#x200B;](select-data-view.md)
>[Selecteer een datumbereik &#x200B;](select-date-range.md)
>[Filterafmetingen &#x200B;](filter-dimensions.md)
>[Werken met segmenten &#x200B;](work-with-filters.md)
>
