---
title: Componentinstellingen opmaken
description: Vorm hoe metrisch wordt geformatteerd.
exl-id: 5ce13fe9-29fa-474c-bae3-65f275153a59
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: 387c787dba4caa9db82d46071e23a2131043c8c6
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 2%

---

# Componentinstellingen opmaken

Met de indeling kunt u bepalen hoe een bepaalde metrische waarde wordt weergegeven.

![Indelingsinstellingen](../assets/format-settings.png)

| Instelling | Beschrijving |
| --- | --- |
| **[!UICONTROL Format]** | Hier kunt u de opmaak van een metrische waarde opgeven als Decimaal, Tijd, Percentage of Valuta. |
| **[!UICONTROL Decimal Places]** | Niet zichtbaar op de gegevenstypen van het schema van het Geheel. Hier kunt u het aantal decimalen opgeven dat metrisch wordt weergegeven. |
| **[!UICONTROL Date]** | Hiermee kunt u bepalen hoe het datum-tijdveld moet worden weergegeven wanneer dit als een dimensie in de rapportage wordt gebruikt. [Meer informatie](../../use-cases/data-views/data-views-usecases.md#date-and-date-time-use-cases) |
| **[!UICONTROL Date-Time]** | Hiermee kunt u bepalen hoe het datum-tijdveld moet worden weergegeven wanneer dit als een dimensie in de rapportage wordt gebruikt. [Meer informatie](../../use-cases/data-views/data-views-usecases.md#date-and-date-time-use-cases) |
| **[!UICONTROL Currency]** | Hiermee kunt u bepalen in welke valuta de metrische waarde moet worden weergegeven. Zie [Valuta](#currency) voor meer informatie . |
| **[!UICONTROL Show upward trend as]** | Hier kunt u opgeven of een opwaartse trend in deze metrische waarde goed (groen) of slecht (rood) is. |
| **[!UICONTROL True value]** en **[!UICONTROL False value]** | Alleen zichtbaar op gegevenstypen van een Booleaans schema. Hiermee kunt u het label van het dimensie-item aanpassen voor `true` en `false` waarden. |

{style="table-layout:auto"}

## Valuta

Wanneer u **[!UICONTROL Currency]** als de [!UICONTROL Format] voor metrisch, kunt u bepalen hoe te om valuta&#39;s te tonen en om te zetten.

### Valuta weergeven

Een valuta voor een metrisch object weergeven:

1. Voer het aantal van **[!UICONTROL Decimal places]**.

1. Selecteer een valuta in het menu **[!UICONTROL Display currency in]** lijst.


### Valuta converteren en weergeven

De conversie van een valuta voor een of meer meetwaarden mogelijk maken:

- Opstelling uw verbinding van de Customer Journey Analytics om minstens één gebeurtenisdataset te bevatten die een dimensie van de muntcode voor elke gebeurtenis bevat die een valuta metrisch bevat. Voor deze dimensie van de valutacode wordt een alfabetische valutacode gebruikt die voldoet aan de [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html) standaard voor de weergave van valuta&#39;s. Deze waarden zouden in volledige hoofdletters moeten zijn zoals USD voor $, EUR voor €, GBP voor £.

   1. Selecteer de dimensie in een van uw gegevenssets die de valutacodes bevat. Bijvoorbeeld, [!UICONTROL Currency code].

   1. Selecteren **[!UICONTROL Currency Code]** in de lijst met afmetingen.

- Herhaal deze stappen als u meer dimensies met valutacodes hebt die u wilt gebruiken voor valutaconversie.

>[!NOTE]
>
>De metrische waarde die u selecteert voor valutaomzetting, moet een numeriek type hebben (Dubbel, Lang, Geheel getal, Kort, Byte).


U definieert als volgt hoe een valuta voor een metrische waarde moet worden omgezet en weergegeven:

1. Voer het aantal van **[!UICONTROL Decimal places]**.

1. Selecteren **[!UICONTROL Convert Concurrency]**.

1. Selecteer de juiste dimensie in de lijst met afmetingen die het veld voor de valutacode bevat.

1. Selecteer een valuta in het menu **[!UICONTROL Convert and display currency in]** lijst.

### Veelgestelde vragen

+++ Hoe wordt valutaomrekening uitgevoerd?

Op rapporttijd, wordt de waarde van de metrische en originele muntcode omgezet in USD en dan omgezet in de valuta die voor vertoning wordt gevormd. Voor deze omrekening worden de dagelijkse wisselkoersen gebruikt die op het tijdstip van de gebeurtenis van toepassing zijn.

+++


+++ Hoe ver zijn de dagelijkse omrekeningskoersen achtergebleven?

De dagelijkse omrekeningskoersen worden gedurende de laatste vier jaar gehandhaafd.

+++


+++ Wat als ik geen gebied van de muntcode als deel van mijn huidig gegevensschema heb?

Er zijn verschillende opties voor het maken van een nieuw valutacodeveld, waaronder Data Prep, Data Distiller en Derived Fields. Data Prep zou ideaal zijn voor nieuwe implementaties, aangezien het alleen op een vooruitstrevende basis zou zijn. Afhankelijk van de opstelling van een organisatie, kunnen de Gegevens Distiller en Afgeleide Gebieden worden gebruikt om tot de waarden van de valutacode historisch toegang te hebben.

+++

