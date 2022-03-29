---
title: Een gegevensweergave maken of bewerken
description: Alle instellingen die u kunt aanpassen om een gegevensweergave te maken of te bewerken.
exl-id: 02494ef6-cc32-43e8-84a4-6149e50b9d78,35cbf69c-e1e5-4cf0-9bb4-6105d3e4c78e
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: 48cc438032fb1df043b7caf085aadf3f2c2f1ecf
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---

# Een gegevensweergave maken of bewerken

Het creëren van een gegevensmening impliceert of het creëren van metriek en dimensies van schemaelementen of het gebruiken van standaardcomponenten. De meeste schemaelementen kunnen of een afmeting of metrisch afhankelijk van de vereisten van uw zaken zijn. Zodra u een schemaelement in een gegevensmening sleept, verschijnen de opties op het recht waar u kunt aanpassen hoe de afmeting of metrisch in CJA werkt.

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/35110/?quality=12&learn=on)

## Een gegevensweergave configureren {#configure}

1. Aanmelden bij [Customer Journey Analytics](https://analytics.adobe.com) en ga naar de **[!UICONTROL Data Views]** tab.
2. Klikken **[!UICONTROL Add]** om een gegevensweergave te maken of klik op een bestaande gegevensweergave om deze te bewerken.

![Nieuwe gegevensweergave](assets/new-data-view.png)

### Instellingen voor gegevensweergave {#settings}

Verstrekt overkoepelende montages voor de gegevensmening.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Connection] | Dit gebied verbindt de gegevensmening met de verbinding die u vroeger vestigde, die één of meerdere datasets van Adobe Experience Platform bevat. |
| [!UICONTROL Name] | Vereist. De naam van de gegevensweergave. Deze waarde wordt weergegeven in het rechtsboven weergegeven vervolgkeuzemenu in Analysis Workspace. |
| [!UICONTROL Description] | Optioneel. Adobe raadt een gedetailleerde beschrijving aan, zodat gebruikers begrijpen waarom de gegevensweergave bestaat en voor wie deze is ontworpen. |

### Containers {#containers}

Hiermee geeft u de naam van containers voor de gegevensweergave aan. Containernamen worden vaak gebruikt in [filters](/help/components/filters/filters-overview.md#Filter-containers).

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Person container name] | [!UICONTROL Person] (standaard). De [!UICONTROL Person] container bevat elke sessie en gebeurtenis voor bezoekers binnen de opgegeven tijdsperiode. Als uw organisatie een andere term gebruikt (bijvoorbeeld &quot;Bezoeker&quot; of &quot;Gebruiker&quot;), kunt u de naam van de container hier wijzigen. |
| [!UICONTROL Session container name] | [!UICONTROL Session] (standaard). De [!UICONTROL Session] Met container kunt u paginainteracties, campagnes of conversies voor een specifieke sessie identificeren. U kunt de naam van deze container wijzigen in &#39;Visit&#39; of in een andere term die uw organisatie verkiest. |
| [!UICONTROL Event container name] | [!UICONTROL Event] (standaard). De [!UICONTROL Event] de container bepaalt individuele gebeurtenissen in een dataset. Als uw organisatie een andere term gebruikt (bijvoorbeeld &quot;Hits&quot; of &quot;Paginaweergaven&quot;), kunt u de naam van de container hier wijzigen. |

### Kalender {#calendar}

Hiermee geeft u de kalender-indeling aan die moet worden gevolgd door de gegevensweergave. U kunt meerdere gegevensweergaven hebben op basis van hetzelfde [Verbinding](/help/connections/create-connection.md) en geef deze verschillende kalendertypen of tijdzones. Deze gegevensmeningen kunnen teams toestaan die verschillende kalendertypes gebruiken om hun respectieve behoeften met de zelfde onderliggende gegevens aan te passen.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Time zone] | Kies in welke tijdzone de gegevens moeten worden weergegeven. Als u een tijdzone kiest die op de Tijd van de Besparing van het Daglicht werkt, worden de gegevens automatisch aangepast om dat te weerspiegelen. In de lente wanneer de klokken één uur vooruit aanpassen, is een gat van één uur aanwezig. In de val wanneer de klokken één uur achter aanpassen, wordt één uur herhaald tijdens de verschuiving van DST. |
| [!UICONTROL Calendar Type] | Bepaal hoe weken van de maand worden gegroepeerd.<br>**Gregoriaans:** Standaardkalenderindeling. Kwarten worden gegroepeerd op maand.<br>**4-5-4 Detailhandel:** Een gestandaardiseerde 4-5-4 retailkalender. De eerste en laatste maanden van het kwartaal bevatten vier weken, terwijl de tweede maand van het kwartaal uit vijf weken bestaat.<br>**Aangepast (4-5-4):** Gelijkaardig aan 4-5-4 kalender behalve kunt u kiezen de eerste dag van het jaar en welk jaar dat de &quot;extra&quot;week voorkomt.<br>**Aangepast (4-4-5):** De eerste en tweede maand van elk kwartaal bevatten vier weken, terwijl de laatste week van elk kwartaal bestaat uit vijf weken.<br>**Aangepast (5-4-4):** De eerste maand van elk kwartaal bestaat uit vijf weken, terwijl de tweede en derde maand van elk kwartaal uit vier weken bestaan. |
| [!UICONTROL First month of the year] en [!UICONTROL First day of week] | Zichtbaar voor het Gregoriaanse kalendertype. Geef op op welke maand het kalenderjaar moet beginnen en op welke dag elke week moet beginnen. |
| [!UICONTROL First day of current year] | Zichtbaar voor aangepaste kalendertypen. Geef op welke dag van het jaar het huidige jaar moet beginnen. Op basis van deze waarde wordt de eerste dag van elke week automatisch opgemaakt in de kalender. |
| [!UICONTROL Year in which the "extra" week occurs] | Met de meeste kalenders van 364 dagen (52 weken van elk 7 dagen), accumuleert elk jaar leftoverdagen tot zij een extra week vormen. Deze extra week wordt dan toegevoegd aan de laatste maand van dat jaar. Geef op aan welk jaar u de extra week wilt toevoegen. |

## De componenten van een gegevensweergave instellen {#set-components}

Vervolgens kunt u metriek en dimensies maken op basis van schema-elementen. U kunt ook Standaardcomponenten gebruiken.

1. Aanmelden bij [Customer Journey Analytics](https://analytics.adobe.com) en ga naar de **[!UICONTROL Data Views]** tab.
1. Klikken **[!UICONTROL Add]** om een gegevensweergave te maken of klik op een bestaande gegevensweergave om deze te bewerken.
1. Klik op de knop **[!UICONTROL Components]** tab.

   ![Tabblad Componenten](assets/components-tab.png)

   U kunt de [!UICONTROL Connection] aan de linkerbovenhoek, die de datasets en zijn bevat [!UICONTROL Schema fields] hieronder. Merk op dat de reeds inbegrepen componenten standaard vereiste componenten (systeem geproduceerd) voor alle gegevensmeningen zijn. Adobe past ook het filter toe **[!UICONTROL Contains data]** door gebrek, zodat slechts de gebieden van het Schema die gegevens bevatten verschijnen. Als u een veld wilt hebben dat geen gegevens bevat, verwijdert u dit filter.

1. Sleep een schemaveld, zoals `pageTitle`van de linkerspoorstaaf naar het gedeelte Metriek of Dimension.

   U kunt het zelfde schemagebied in de dimensies of metrieksecties veelvoudige tijden slepen en de zelfde afmeting of metrisch op verschillende manieren vormen. Bijvoorbeeld vanuit de `pageTitle` in het veld kunt u een dimensie met de naam &quot;Productpagina&#39;s&quot; en een andere dimensie met de naam &quot;Foutpagina&#39;s&quot; maken door een andere dimensie te gebruiken [Componentinstellingen](component-settings/overview.md) rechts.

   ![Tab 3](assets/components-tab-3.png)

   Als u een schemagebiedomslag van het linkerspoor sleept, worden zij automatisch gesorteerd in typische secties. Tekenreeksvelden eindigen in het dialoogvenster [!UICONTROL Dimensions] sectie- en numerieke schematypen eindigen in de [!UICONTROL Metrics] sectie. U kunt ook op **[!UICONTROL Add all]** en alle schemavelden worden toegevoegd aan hun respectieve locaties.

1. Nadat u de component hebt geselecteerd, wordt rechts een aantal instellingen weergegeven. De component configureren met [Componentinstellingen](component-settings/overview.md). Welke componentinstellingen beschikbaar zijn, hangt af van het feit of de component een dimensie/metrische component is en van het gegevenstype schema. Voorbeelden van instellingen:

   * [[!UICONTROL Attribution]](component-settings/attribution.md)
   * [[!UICONTROL Behavior]](component-settings/behavior.md)
   * [[!UICONTROL Format]](component-settings/format.md)
   * [[!UICONTROL Include exclude values]](component-settings/include-exclude-values.md)
   * [[!UICONTROL Metric deduplication]](component-settings/metric-deduplication.md)
   * [[!UICONTROL No value options]](component-settings/no-value-options.md)
   * [[!UICONTROL Persistence]](component-settings/persistence.md)
   * [[!UICONTROL Value bucketing]](component-settings/value-bucketing.md)

## Maten of afmetingen dupliceren {#duplicate}

Het dupliceren van metriek of afmetingen en het vervolgens wijzigen van specifieke montages is een gemakkelijke manier om veelvoudige metriek of afmetingen van één enkel schemagebied tot stand te brengen. Selecteer [!UICONTROL Duplicate] het plaatsen onder de metrische metrische naam of dimensies bij het hoogste recht. Wijzig de nieuwe dimensie of metrische waarde en sla deze onder een beschrijvende naam op.

![Dupliceren](assets/duplicate.png)

## Filterschemavelden of -gegevenssets {#filter}

U kunt schemagebieden in het linkerspoor door de volgende gegevenstypes filtreren:

![Filtervelden](assets/filter-fields.png)

U kunt ook filteren op gegevenssets en op het feit of een schemaveld gegevens bevat of dat het een identiteit is. Standaard past Adobe eerst de **[!UICONTROL Contains data]** naar alle gegevensweergaven te filteren.

![Andere filters](assets/filter-other.png)

## Het tabblad Instellingen {#settings-tab}

1. Aanmelden bij [Customer Journey Analytics](https://analytics.adobe.com) en ga naar de **[!UICONTROL Data Views]** tab.
1. Klikken **[!UICONTROL Add]** om een gegevensweergave te maken of klik op een bestaande gegevensweergave om deze te bewerken.
1. Klik op de knop **[!UICONTROL Settings]** tab.

### Globaal, filter {#global-filter}

U kunt filters toevoegen die op een volledige gegevensmening van toepassing zijn. Dit filter wordt toegepast op elk rapport dat u uitvoert in Workspace. Sleep een filter van de lijst in de linkerspoorstaaf aan [!UICONTROL Add filters] veld.

### Sessieinstellingen {#sessions}

Bepaal de periode van inactiviteit tussen gebeurtenissen alvorens een zitting verloopt en nieuwe wordt begonnen. Een tijdsperiode is vereist. U kunt desgewenst ook een nieuwe sessie forceren om te starten wanneer een gebeurtenis een bepaalde metrische waarde bevat.

Als alle gewenste instellingen zijn opgegeven, klikt u op **[!UICONTROL Save and finish]**.
