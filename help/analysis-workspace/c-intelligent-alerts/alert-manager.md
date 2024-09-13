---
description: Waarschuwingen maken, bewerken of verwijderen.
title: Waarschuwingsbeheer (Analysis Workspace)
feature: Workspace Basics
role: User, Admin
source-git-commit: 1613b3fc7e9cce1fb74b86bb7435612b2d469eb1
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Waarschuwingen beheren

U kunt bestaande waarschuwingen beheren in het venster Waarschuwingen. U kunt verschillende beheertaken uitvoeren voor waarschuwingen, zoals labelen, hernoemen, verwijderen en meer.

De manager van het Alarm is zeer gestructureerd zoals de [ manager van de Filter ](/help/components/filters/manage-filters.md) en [ Berekende Metrische Manager ](/help/components/calc-metrics/cm-workflow/cm-manager.md).

## Waarschuwingen maken

Waarschuwingen maken via het Alarmbeheer:

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Alerts]** om het Waarschuwingenbeheer in Customer Journey Analytics te openen.

   ![](assets/alert-manager.png)

1. Selecteer [!UICONTROL **toevoegen**] (of [!UICONTROL **creëren nieuw alarm**] als u geen bestaand alarm hebt).

1. Ga met [ voort creeer alarm ](/help/analysis-workspace/c-intelligent-alerts/alert-builder.md) voor meer details over het creëren van alarm.

## Bestaande waarschuwingen beheren

Bestaande waarschuwingen beheren in het Waarschuwingenbeheer:

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Alerts]** om het Waarschuwingenbeheer in Customer Journey Analytics te openen.

   ![](assets/alert-manager.png)

1. Selecteer een of meer waarschuwingen die u wilt beheren.

   ![](assets/alert-manager-tasks.png)

1. Selecteer een van de volgende opties op de actiebalk:

   | Handeling | Functie |
   |---------|----------|
   | [!UICONTROL **Markering**] | Pas een tag toe op een waarschuwing. Hierdoor kunt u waarschuwingen ordenen voor gebruiksgemak. |
   | [!UICONTROL **Schrapping**] | Hiermee verwijdert u de waarschuwing. |
   | [!UICONTROL **anders noemen**] | Wijzigt de naam van de waarschuwing. |
   | [!UICONTROL **goedkeuren**] | Markeer de waarschuwing als Goedgekeurd. |
   | [!UICONTROL **Exemplaar**] | Hiermee maakt u een kopie (kopie) van de waarschuwing. |
   | [!UICONTROL **onbruikbaar maken**] | Hiermee wordt een waarschuwing uitgeschakeld die momenteel is ingeschakeld. |
   | [!UICONTROL **laat toe**] | Hiermee wordt een waarschuwing ingeschakeld die momenteel is uitgeschakeld. |
   | [!UICONTROL **Vernieuwen**] | Hiermee wordt de vervaldatum van de waarschuwing vernieuwd. Hiermee wordt de vervaldatum verlengd tot 1 jaar vanaf de dag waarop u deze optie hebt geselecteerd, ongeacht de oorspronkelijke vervaldatum. |
   | [!UICONTROL **Uitvoer aan CSV**] | Exporteert de waarschuwing naar een CSV-bestand. |

## Een waarschuwing bewerken

Een bestaande waarschuwing bewerken:

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Alerts]** om Alerts Manager in Adobe Analytics te openen.

   ![](assets/alert-manager.png)

1. Selecteer de waakzame naam in de [!UICONTROL **Titel en beschrijvings**] kolom.

1. Bewerk de waarschuwing naar wens.

   Hier volgen enkele voorbeelden van wat u kunt doen wanneer u een waarschuwing bewerkt:

   * Waarschuwingen toevoegen aan andere rapportsuites
   * De eigenaar wijzigen
   * Filters bijwerken
   * De vervaldatum bijwerken

1. Bewerk het alarm, dan uitgezocht [!UICONTROL **sparen**].

## Kolommen configureren

U kunt de informatie vormen die voor elke alarm in de manager van het Alarm wordt getoond door de kolommen te vormen die worden getoond.

De zichtbare kolommen configureren in het Alarmbeheer:

1. Selecteer in Adobe Analytics de tab **[!UICONTROL Components]** en selecteer vervolgens **[!UICONTROL Alerts]** .

1. In de Waakzame manager, selecteer **kolommen** pictogram ![ aanpassen kolommen pictogram ](assets/customize-columns-icon.png), dan selecteer de kolommen die u in de manager van het Alarm wilt worden getoond.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Titel en beschrijving | Deze waarden worden opgegeven in de Alert Builder. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de waarschuwingsconstructor te openen. |
   | Favorieten | Hiermee geeft u sterpictogrammen weer naast elke waarschuwing, zodat u waarschuwingen als favorieten kunt markeren. <!-- For more information, see [Mark calculated metrics as favorites](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). --> |
   | Type | Toont of het alarm een de gegevensalarm van de Analyse of een alarm van het de vraaggebruik van de Server is. |
   | Ingeschakeld | Hiermee wordt getoond of de waarschuwing is ingeschakeld of uitgeschakeld. |
   | Rapportsuite | Geeft aan in welke rapportsuite de waarschuwing het laatst is opgeslagen. |
   | Eigenaar | Hiermee wordt aangegeven wie de eigenaar van de waarschuwing is. Als niet-beheerder, kunt u slechts alarm zien u bezit of die met u werden gedeeld. |
   | Tags | Hier ziet u tags die zijn toegepast op de waarschuwing, door u of door personen die de waarschuwing met u hebben gedeeld. |
   | Vervaldatum | Geeft de datum en tijd weer waarop de waarschuwing is ingesteld op verlopen. |
   | Datum gewijzigd | Geeft de datum aan waarop de waarschuwing voor het laatst is gewijzigd. |

   {style="table-layout:auto"}

   <!-- When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> -->

## Een waarschuwing oplossen

Wanneer u een probleem met een waarschuwing oplost, geeft u het JID-nummer (Job Instance ID) op aan de ondersteuning van Adoben. Het JID-nummer bevindt zich onder aan het e-mailbericht dat u hebt ontvangen.

![ Alert e-mail ](assets/alerts-email.PNG)