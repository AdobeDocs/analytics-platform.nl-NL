---
title: Datumbereiken maken
description: Maak een datumbereik voor rapportage.
feature: Calendar
exl-id: 3e4fa3cc-c14b-45e5-afbb-518ecfa0033e
role: User
source-git-commit: df0fd0af8a22c84705c3dea11065132359dd80ff
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Datumbereiken maken


Iedereen kan een aangepast datumbereik maken. U kunt op de volgende manieren een datumbereik maken:

![ creeer een aantekening ](assets/create-date-range.png)

* ?? Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer **[!UICONTROL Date range]** . Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) [!UICONTROL **[!UICONTROL Add]**] van de [[!UICONTROL Date range] manager ](/help/components/date-ranges/manage.md).
* ?? Selecteer **[!UICONTROL Custom date range to this date range]** in een Workspace-project in het contextmenu in een visualisatie.
* ?? Selecteer in een Workspace-project **[!UICONTROL Components]** in het menu en selecteer **[!UICONTROL Create date range]**
* ?? In een Workspace-project gebruikt u de sneltoets **[!UICONTROL ctrl+shift+d]** (Windows) of **[!UICONTROL shift+command+d]** (macOS).
* ?? In een project van Workspace, van het linkerpaneel van Componenten, voegt de uitgezochte ![ ](/help/assets/icons/Add.svg) bij ![ de waaiers van de Kalender ](/help/assets/icons/Calendar.svg) **Datum** toe.

Als u de annotatie wilt definiëren, gebruikt u de instructie [[!UICONTROL Date range builder]](#annotation-builder) :

<!-- Should we really mention API here. If so, we can do it all over the place in the docs...
| **Use the [Customer Journey Analytics Annotations API](https://developer.adobe.com/cja-apis/docs/endpoints/annotations/)** | The Customer Journey Analytics Annotations APIs allow you to create, update, or retrieve annotations programmatically through Adobe Developer. These APIs use the same data and methods that Adobe uses inside the product UI. |
-->


## Bouwer van datumbereik {#date-range-builder}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_dateranges_endtime"
>title="Eindtijd"
>abstract="Eindtijden omvatten altijd 59 seconden."

<!-- markdownlint-enable MD034 -->




Het dialoogvenster **[!UICONTROL New date range]** of **[!UICONTROL Edit date range]** wordt gebruikt om nieuwe datumbereiken te maken of bestaande datumbereiken te bewerken.

![ het venster van de details van de Annotatie die gebieden en opties tonen in de volgende sectie worden beschreven.](assets/edit-date-range.png)


1. Geef een **[!UICONTROL Title]** voor het datumbereik op. Bijvoorbeeld **[!UICONTROL Quarterly]** .
1. Geef desgewenst een **[!UICONTROL Description]** op.
1. Organiseer het filter door een of meer **[!UICONTROL Tags]** te maken of toe te passen. Begin te typen om naar bestaande tags te zoeken die u kunt selecteren. Of druk op **[!UICONTROL ENTER]** om een nieuwe tag toe te voegen. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om een markering te verwijderen. |
1. Selecteer een **[!UICONTROL Date Range]** door eerst de begindatum en vervolgens de einddatum te selecteren.
Alternatief, kunt u a **[!UICONTROL Preset]** van [!UICONTROL *selecteren selecteert vooraf ingesteld*] dropdown menu.

1. Selecteer indien nodig **[!UICONTROL Show advanced settings]** tot en met:

   * Geef **[!UICONTROL Start time]** en **[!UICONTROL End time]** anders op dan de standaardinstellingen `12:00 AM` (`0:00`) en `11:59 PM` (`23:59`). Eindtijden omvatten altijd 59 seconden. Voor een datumbereik dat vele dagen omvat, geldt de begintijd voor de eerste dag van het datumbereik en de eindtijd voor de laatste dag in het datumbereik. Met **[!UICONTROL (Reset time values)]** kunt u de standaardinstellingen van de begin- en eindtijd herstellen.
   * **[!UICONTROL Use rolling dates]**. Indien ingeschakeld, worden vooraf ingestelde datumbereiken zoals **[!UICONTROL Last 7 full days]** dynamisch bijgewerkt als de huidige datum- en tijdvoortgang. Als deze optie is uitgeschakeld, worden deze voorinstellingen niet bijgewerkt nadat ze zijn toegepast.

     U kunt de tekst tussen haakjes selecteren (bijvoorbeeld **[!UICONTROL fixed start - rolling quarterly]** ) om het deelvenster uit te breiden en details voor **[!UICONTROL Start]** en **[!UICONTROL End]** op te geven.

     ![ de datums van het Rollinf ](assets/rolliing-dates.png)

      1. Selecteer **[!UICONTROL Start of]**, **[!UICONTROL End of]** of **[!UICONTROL Fixed day]** .
      1. Wanneer u **[!UICONTROL Start of]** of **[!UICONTROL End of]** hebt geselecteerd, kunt u een volledige expressie maken. Bijvoorbeeld: **[!UICONTROL End of]** **[!UICONTROL current quarter]** **[!UICONTROL minus]** `20` **[!UICONTROL days]** . Kies de juiste waarde voor elk afzonderlijk deel van de expressie.
         * Selecteer een waarde voor de huidige. Bijvoorbeeld **[!UICONTROL current quarter]** .
         * Selecteer een waarde voor extra berekening. Bijvoorbeeld **[!UICONTROL minus]** .
         * Geef een waarde op wanneer u een extra berekening hebt opgegeven. Bijvoorbeeld `20` .
         * Wanneer u een extra berekening hebt opgegeven, selecteert u de periode die u voor de berekening wilt gebruiken. Bijvoorbeeld **[!UICONTROL days]** .

     Selecteer **[!UICONTROL Hide details]** om de details voor het rollen datumberekening te verbergen.

1. Selecteren:
   * **[!UICONTROL Save]** om het datumbereik op te slaan.
   * **[!UICONTROL Save As]** om een kopie van het datumbereik op te slaan.
   * **[!UICONTROL Cancel]** om eventuele wijzigingen in het datumbereik te annuleren of om het maken van een nieuw datumbereik te annuleren.


<!--


You can create a date range using either of the following two methods:

* Directly in a workspace project by clicking the '`+`' button next to the list of date range components on the left
* Within the date range manager

To create a date range in the date range manager:

1. Log in to [analytics.adobe.com](https://analytics.adobe.com) using your AdobeID credentials.
1. Navigate to [!UICONTROL Components] > [!UICONTROL Date Ranges].
1. Click the [!UICONTROL Add] button to open the modal window that creates a date range.

## Create a date range modal window

The modal window has four fields you can edit:

* **Date range**: The date range you want for this component.
* **Title**: The name you want for this component. The title is used in workspace projects.
* **Description**: The description you want for this component. The description is seen when clicking the ![i](../assets/i.png) icon.
* **Tags**: Use tags to organize your date ranges. A date range can belong to multiple tags.

## Selecting a date range

When clicking the date range in the modal window, you have several options:

* **Calendar**: Select the start and end date.
* **Use rolling dates**: Check this box if you want the date range to change as time goes on. Do not check this box if you want your date range to remain static.
* **Select preset**: Use this drop-down selection if you want a custom date range based on a range that Adobe offers by default. When you select a preset, you can further customize the date range to suit your needs. It does not affect the preset that Adobe offers.

## Rolling date ranges

If you want a rolling date range, you can customize when it rolls. You can control when the start and end dates roll independently of each other.

* **When the date starts**: Choose if the date starts at the beginning of a time period, at the end of a time period, or use a fixed day.
* **The time period to use**: Choose how often the date range rolls. You can have it roll every day, every week, every month, every quarter, or every year.
* **Offset**: Choose the offset of the date range. You can add or subtract days, weeks, months, quarters, or years.

## Rolling date examples

Some date ranges can be useful in certain reports.

Year-to-date:

```text
Start: Start of current year
End: End of current day
```

Last Thursday to this Thursday:

```text
Start: Start of current week minus 3 days
End: Start of current week plus 4 days
```

Fiscal year (for example, if a fiscal year starts in December)

```text
Start: Start of current year minus 1 month
End: End of current year minus 1 month
```


-->