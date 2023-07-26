---
title: Een gegevensweergave maken of bewerken
description: Alle instellingen die u kunt aanpassen om een gegevensweergave te maken of te bewerken.
exl-id: 02494ef6-cc32-43e8-84a4-6149e50b9d78
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: 92511d2bedf322097b4d70ccede5ac6e0df7b0c6
workflow-type: tm+mt
source-wordcount: '1272'
ht-degree: 0%

---

# Een gegevensweergave maken of bewerken

Het creëren van een gegevensmening impliceert of het creëren van metriek en dimensies van schemaelementen of het gebruiken van standaardcomponenten. De meeste schemaelementen kunnen of een afmeting of metrisch afhankelijk van de vereisten van uw zaken zijn. Nadat u een schema-element naar een gegevensweergave hebt gesleept, worden aan de rechterkant opties weergegeven waarmee u de werking van de dimensie of metrische waarde in Customer Journey Analytics kunt aanpassen.

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/35110/?quality=12&learn=on)

Een gegevensweergave maken of bewerken:

1. Aanmelden bij [Customer Journey Analytics](https://analytics.adobe.com) en ga naar de **[!UICONTROL Data views]** tab.
1. Selecteer **[!UICONTROL Create new data view]**. U kunt ook een bestaande gegevensweergave selecteren in de lijst met gegevensweergaven om deze te bewerken.


## Configureren

Een nieuwe of bestaande gegevensweergave configureren:

1. Selecteer de **[!UICONTROL Configure]** tab (als deze nog niet actief is).

   ![Gegevensweergave configureren](assets/dataview-configure.png)
1. Opgeven [!UICONTROL Settings], [!UICONTROL Container], en [!UICONTROL Calendar] nadere gegevens (zie hieronder).
1. Selecteren **[!UICONTROL Save and continue]** om uw nieuwe of bestaande gegevensmening te blijven vormen. Selecteren **[!UICONTROL Save]** om de configuratie voor uw bestaande gegevensmening te bewaren.


### Instellingen

Verstrekt overkoepelende montages voor de gegevensmening.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Connection] | Dit gebied verbindt de gegevensmening met de verbinding die u vroeger vestigde, die één of meerdere datasets van Adobe Experience Platform bevat. |
| [!UICONTROL Name] | Vereist. De naam van de gegevensweergave. Deze waarde wordt weergegeven in de vervolgkeuzelijst rechtsboven in Analysis Workspace. |
| [!UICONTROL Description] | Optioneel. Adobe raadt een gedetailleerde beschrijving aan, zodat gebruikers begrijpen waarom de gegevensweergave bestaat en voor wie deze is ontworpen. |

{style="table-layout:auto"}

### Containers

Hiermee geeft u de naam van containers voor de gegevensweergave aan. Containernamen worden vaak gebruikt in [filters](/help/components/filters/filters-overview.md#Filter-containers).

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Person container name] | [!UICONTROL Person] (standaard). De [!UICONTROL Person] container omvat elke zitting en gebeurtenis voor personen binnen het gespecificeerde tijdkader. Als uw organisatie een andere term gebruikt (bijvoorbeeld &quot;Bezoeker&quot; of &quot;Gebruiker&quot;), kunt u de naam van de container hier wijzigen. |
| [!UICONTROL Session container name] | [!UICONTROL Session] (standaard). De [!UICONTROL Session] Met container kunt u paginainteracties, campagnes of conversies voor een specifieke sessie identificeren. U kunt de naam van deze container wijzigen in &#39;Visit&#39; of in een andere term die uw organisatie verkiest. |
| [!UICONTROL Event container name] | [!UICONTROL Event] (standaard). De [!UICONTROL Event] de container bepaalt individuele gebeurtenissen in een dataset. Als uw organisatie een andere term gebruikt (bijvoorbeeld &quot;Hits&quot; of &quot;Paginaweergaven&quot;), kunt u de naam van de container hier wijzigen. |

{style="table-layout:auto"}

### Kalender

Hiermee geeft u de kalender-indeling aan die moet worden gevolgd door de gegevensweergave. U kunt meerdere gegevensweergaven hebben op basis van hetzelfde [Verbinding](/help/connections/create-connection.md) en geef deze verschillende kalendertypen of tijdzones. Deze gegevensmeningen kunnen teams toestaan die verschillende kalendertypes gebruiken om hun respectieve behoeften met de zelfde onderliggende gegevens aan te passen.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Time zone] | Kies in welke tijdzone de gegevens moeten worden weergegeven. Als u een tijdzone kiest die op de Tijd van de Besparing van het Daglicht werkt, worden de gegevens automatisch aangepast om dat te weerspiegelen. In de lente wanneer de klokken één uur vooruit aanpassen, is een gat van één uur aanwezig. In de val wanneer de klokken één uur achter aanpassen, wordt één uur herhaald tijdens de verschuiving van DST. |
| [!UICONTROL Calendar Type] | Bepaal hoe weken van de maand worden gegroepeerd.<br>**Gregoriaans:** Standaardkalenderindeling. Kwarten worden gegroepeerd op maand.<br>**4-5-4 Detailhandel:** Een gestandaardiseerde 4-5-4 retailkalender. De eerste en laatste maanden van het kwartaal bevatten vier weken, terwijl de tweede maand van het kwartaal uit vijf weken bestaat.<br>**Aangepast (4-5-4):** Gelijkaardig aan 4-5-4 kalender behalve kunt u kiezen de eerste dag van het jaar en welk jaar dat de &quot;extra&quot;week voorkomt.<br>**Aangepast (4-4-5):** De eerste en tweede maand van elk kwartaal bevatten vier weken, terwijl de laatste week van elk kwartaal vijf weken omvat.<br>**Aangepast (5-4-4):** De eerste maand van elk kwartaal bestaat uit vijf weken, terwijl de tweede en derde maand van elk kwartaal uit vier weken bestaan. |
| [!UICONTROL First month of the year] en [!UICONTROL First day of week] | Zichtbaar voor het Gregoriaanse kalendertype. Geef op op welke maand het kalenderjaar moet beginnen en op welke dag elke week moet beginnen. |
| [!UICONTROL First day of current year] | Zichtbaar voor aangepaste kalendertypen. Geef op welke dag van het jaar het huidige jaar moet beginnen. Op basis van deze waarde wordt de eerste dag van elke week automatisch opgemaakt in de kalender. |
| [!UICONTROL Year in which the "extra" week occurs] | Met de meeste kalenders van 364 dagen (52 weken van elk 7 dagen), accumuleert elk jaar leftoverdagen tot zij aan een extra week toevoegen. Deze extra week wordt dan toegevoegd aan de laatste maand van dat jaar. Geef op aan welk jaar u de extra week wilt toevoegen. |

{style="table-layout:auto"}

## Onderdelen

Vervolgens kunt u de componenten van een gegevensweergave instellen. Dit betekent dat u metriek en afmetingen kunt maken op basis van schema-elementen. U kunt ook standaardcomponenten gebruiken.

1. Selecteer de **[!UICONTROL Components]** tab.

   ![Tabblad Componenten](assets/dataview-components.png)

   U kunt de [!UICONTROL Connection] aan de linkerbovenhoek, die de datasets en zijn bevat [!UICONTROL Schema fields] hieronder.  De reeds inbegrepen componenten zijn standaardcomponenten (systeem geproduceerd) die voor alle gegevensmeningen (zoals Gebeurtenissen, Mensen, de metriek van zittingen, en Minuut, Kwart, Week afmetingen) worden vereist. Adobe past ook het filter toe **[!UICONTROL Contains data]** en **[!UICONTROL is not deprecated]** door gebrek, zodat slechts de gebieden van het Schema die gegevens bevatten en die niet verouderd zijn verschijnen.

1. Een schemaveld zoeken met ![Zoekpictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) **[!UICONTROL Search schema fields]** of vind een gebied door zich in om het even welke datasetinzamelingen te bewegen, als ![Mappictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Folder_18_N.svg) **[!UICONTROL Event datasets]**.<br/>U kunt ook een afgeleid veld maken met ![Gegevenspictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) **Afafgeleid veld maken** . Zie [Afgeleide velden](./derived-fields/derived-fields.md) voor meer informatie .

1. Wanneer u een specifiek schemaveld hebt gevonden of uw afgeleide veld hebt gedefinieerd, sleept u dat veld, bijvoorbeeld ![Handgreeppictogram](https://spectrum.adobe.com/static/icons/workflow_22/Smock_DragHandle_22_N.svg) **[!UICONTROL Page Name]**van de linkerspoorstaaf naar het gedeelte Metriek of Dimension.
U kunt het zelfde schemagebied in de dimensies of metrieksecties veelvoudige tijden slepen en de zelfde afmeting of metrisch op verschillende manieren vormen. U kunt bijvoorbeeld in het veld pageName een dimensie met de naam &quot;Productpagina&#39;s&quot; maken en een andere dimensie met de naam &quot;Foutpagina&#39;s&quot;, door verschillende [Componentinstellingen](component-settings/overview.md) rechts.
Als u een schemagebiedomslag van het linkerspoor sleept, worden zij automatisch gesorteerd in typische secties. Tekenreeksvelden eindigen in het dialoogvenster [!UICONTROL Dimensions] sectie- en numerieke schematypen eindigen in de [!UICONTROL Metrics] sectie. U kunt ook op **[!UICONTROL Add all]** en alle schemavelden worden toegevoegd aan hun respectieve locaties.

1. Zodra u een component selecteert, verschijnen de montages op het recht.

   ![Geselecteerde component DataView](assets/dataview-component-pagename.png)

   De component configureren met [Componentinstellingen](component-settings/overview.md). Welke componentinstellingen beschikbaar zijn, hangt af van het feit of de component een dimensie/metrische component is en van het gegevenstype schema. Voorbeelden van instellingen:

   * [[!UICONTROL Attribution]](component-settings/attribution.md)
   * [[!UICONTROL Behavior]](component-settings/behavior.md)
   * [[!UICONTROL Format]](component-settings/format.md)
   * [[!UICONTROL Include exclude values]](component-settings/include-exclude-values.md)
   * [[!UICONTROL Metric deduplication]](component-settings/metric-deduplication.md)
   * [[!UICONTROL No value options]](component-settings/no-value-options.md)
   * [[!UICONTROL Persistence]](component-settings/persistence.md)
   * [[!UICONTROL Value bucketing]](component-settings/value-bucketing.md)

1. Selecteren **[!UICONTROL Save and continue]** om uw nieuwe of bestaande gegevensmening te blijven vormen. Selecteren **[!UICONTROL Save]** om de configuratie voor uw bestaande gegevensmening te bewaren.

**Maten of afmetingen dupliceren**

Het dupliceren van metriek of afmetingen en het vervolgens wijzigen van specifieke montages is een gemakkelijke manier om veelvoudige metriek of afmetingen van één enkel schemagebied tot stand te brengen. Selecteer de [!UICONTROL Duplicate] onder de naam van de metrische waarde of de afmetingen in de rechterbovenhoek instellen. Wijzig de nieuwe dimensie of metrische waarde en sla deze onder een beschrijvende naam op.

**Filterschemavelden of -gegevenssets**

U kunt ![Filterpictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg) schema-velden in linkerspoor per [!UICONTROL data type], [!UICONTROL datasets], [!UICONTROL data governance], en [!UICONTROL other] criteria ([!UICONTROL contains data], [!UICONTROL is identity], en [!UICONTROL is not deprecated]):

![Filtervelden](assets/dataview-components-filter.png)


## Instellingen

1. Selecteer de **[!UICONTROL Settings]** tab.
1. Configureer filters om toe te passen op de volledige gegevensweergave. Zie [Instellingen (filters)](#settings-filters) hieronder.
1. Configureer de sessietime-out en metriek. Zie [Sessieinstellingen](#session-settings) hieronder.
1. Selecteren **[!UICONTROL Save and continue]** om uw nieuwe of bestaande gegevensmening te blijven vormen. Selecteren **[!UICONTROL Save]** om de configuratie voor uw bestaande gegevensmening te bewaren.

### Instellingen (filters)

U kunt filters toevoegen die op een volledige gegevensmening van toepassing zijn. Dit filter wordt toegepast op elk rapport dat u uitvoert in Workspace. Sleep een filter van de lijst in de linkerspoorstaaf aan [!UICONTROL Add filters] veld.

### Sessieinstellingen

Bepaal de periode van inactiviteit tussen gebeurtenissen alvorens een zitting verloopt en nieuwe wordt begonnen. Er is een tijdsperiode vereist. U kunt desgewenst ook een nieuwe sessie forceren om te starten wanneer een gebeurtenis een bepaalde metrische waarde bevat. Zie [Contextbewuste sessies](context-aware-sessions.md) voor meer informatie .

Klik op **[!UICONTROL Save and finish]**.
