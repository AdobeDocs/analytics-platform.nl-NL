---
description: Het synchroniseren van visualisaties laat u controleren welke gegevenslijst of gegevensbron aan een visualisatie beantwoordt.
keywords: Analysis Workspace;Synchronize visualization with data source
title: Databronnen beheren
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 4%

---


# Databronnen beheren

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Het synchroniseren van visualisaties laat u controleren welke gegevenslijst of gegevensbron aan een visualisatie beantwoordt.

**Tip:** U kunt zien welke visualisaties gerelateerd zijn aan de kleur van de stip naast de titel. De gelijke kleuren betekenen dat de visualisaties op de zelfde gegevensbron gebaseerd zijn.

Het leiden van een gegevensbron laat u de gegevensbron tonen of de selectie sluiten. Deze montages bepalen hoe de visualisatie verandert (of niet verandert) wanneer de nieuwe gegevens binnen komen.

1. [Een project maken](/help/analysis-workspace/home.md) met een datatabel en een [visualisatie](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md).
1. In de gegevenslijst, selecteer de cellen (gegevensbron) u met de visualisatie wilt associëren.
1. In de visualisatie, klik de punt naast de titel om omhoog te brengen **[!UICONTROL Data Source]** dialoog. Selecteer **[!UICONTROL Show Data Source]** of **[!UICONTROL Lock Selection]**.

   ![](assets/manage-data-source.png)

   Het synchroniseren van een visualisatie aan een lijstcel leidt tot een nieuwe (verborgen) lijst en kleur-codes de gesynchroniseerde visualisatie met die lijst.

| Element | Beschrijving |
|--- |--- |
| Gekoppelde visualisaties | Als er visualisaties zijn die met een freeform of cohortlijst worden verbonden, opent de hoogste linkerpunt om van de verbonden visualisaties een lijst te maken en heeft een &quot;show&quot;checkbox optie om de lijst te tonen/te verbergen.  Het verbergen benadrukt de verbonden visualisatie, en het klikken van het neemt u aan het. |
| Gegevensbron weergeven | Laat u (door checkbox toe te laten) of verbergen (door onbruikbaar te maken) de gegevenslijst tonen die aan de visualisatie beantwoordt. |
| Selectie vergrendelen | Laat dit het plaatsen toe om de visualisatie aan de gegevens te sluiten die momenteel in de overeenkomstige gegevenslijst worden geselecteerd. Zodra toegelaten, kies tussen:  <ul><li>**Geselecteerde posities**: Kies deze optie als u de visualisatie gesloten op de posities wilt blijven die in de overeenkomstige gegevenslijst worden geselecteerd. Deze posities zullen zichtbaar blijven, zelfs als de specifieke posten in deze posities veranderen. Bijvoorbeeld, kies deze optie als u de hoogste vijf campagnenamen in deze visualisatie wilt altijd tonen, geen kwestie die campagnenamen in hoogste vijf verschijnen.</li> <li>**Geselecteerde items**: Kies deze optie als u wilt dat de visualisatie vergrendeld blijft op de specifieke items die momenteel zijn geselecteerd in de corresponderende datatabel. Deze items blijven zichtbaar, zelfs als ze hun rangschikking tussen de items in de tabel wijzigen. Bijvoorbeeld, kies deze optie als u de zelfde vijf specifieke campagnemenamen in deze visualisatie wilt altijd tonen, geen kwestie waar die campagnenamen rangschikken.</li></ul> |

Deze architectuur verschilt van vorige in dat de Werkruimte van de Analyse niet meer tot een dubbele verborgen lijst leidt die de gesloten selectie voor u opslaat. Nu, richt de gegevensbron aan de lijst dat u de visualisatie van creeerde.

**Voorbeelden:**

* U kunt een summiere visualisatie tot stand brengen en het sluiten aan een cel in de lijst u het van creeerde. Wanneer u &quot;toont Gegevensbron&quot;toelaat, toont het u precies waar deze informatie uit in de lijst komt. De brongegevens worden grijs weergegeven:

   ![](assets/data-source2.png)>
* U kunt veel visualisaties toevoegen en hen uit verschillende cellen in de zelfde lijst, zoals hier getoond bron. De lijst is het zelfde als in het voorbeeld hierboven, maar de bronced cel (en metrisch) is verschillend:

   ![](assets/data-source3.png)>
* U kunt zien of er visualisaties zijn die met een freeform of cohortlijst worden verbonden door de hoogste linkerpunt (de Montages van de Gegevensbron) te klikken. Als u de muis hierboven houdt, wordt de gekoppelde visualisatie weergegeven. En als u erop klikt, gaat u direct naar de gekoppelde visualisatie.

   ![](assets/linked-visualizations.png)>
