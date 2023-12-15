---
title: Componentinstellingen opmaken
description: Vorm hoe metrisch wordt geformatteerd.
exl-id: 5ce13fe9-29fa-474c-bae3-65f275153a59
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: cf9e8c90eec78658e470d3a7a56cb2e3414591d4
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 1%

---

# Componentinstellingen opmaken

Het formaat laat u bepalen hoe bepaalde metrisch wanneer gebruikt in rapporten wordt getoond.

## Vorm formaatmontages voor metrisch

U kunt bepalen hoe een bepaalde metrische waarde wordt getoond door zijn formaatmontages aan te passen.

1. Selecteer in Customer Journey Analytics de optie [!UICONTROL **Gegevensweergaven**] tab.

1. Selecteer de gegevensmening die de component bevat waarvan formaat dat u wilt vormen plaatst.

1. Selecteer de [!UICONTROL **Componenten**] tab.

1. Selecteer de component die u wilt vormen, dan breid uit [!UICONTROL **Indeling**] aan de rechterkant van de pagina.

   ![Indelingsinstellingen](../assets/format-settings.png)

1. Geef de volgende informatie op:

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Format]** | Hier kunt u de opmaak van een metrische waarde opgeven als Decimaal, Tijd, Percentage of Valuta. |
   | **[!UICONTROL Decimal]** | Niet zichtbaar op de gegevenstypen van het schema van het Geheel. Hier kunt u het aantal decimalen opgeven dat metrisch wordt weergegeven. |
   | **[!UICONTROL Date]** | Hiermee kunt u bepalen hoe het datum-tijdveld moet worden weergegeven wanneer dit als een dimensie in de rapportage wordt gebruikt. [Meer informatie](../../use-cases/data-views/data-views-usecases.md#date-and-date-time-use-cases) |
   | **[!UICONTROL Date-Time]** | Hiermee kunt u bepalen hoe het datum-tijdveld moet worden weergegeven wanneer dit als een dimensie in de rapportage wordt gebruikt. [Meer informatie](../../use-cases/data-views/data-views-usecases.md#date-and-date-time-use-cases) |
   | **[!UICONTROL Currency]** | Hiermee kunt u bepalen in welke valuta de metrische waarde moet worden weergegeven. <p>Als u globale gegevens analyseert waar transacties in verschillende valuta&#39;s plaatsvinden, zie  [Valuta-conversie gebruiken](#use-currency-conversion).</p> |
   | **[!UICONTROL Show upward trend as]** | Hier kunt u opgeven of een opwaartse trend in deze metrische waarde goed (groen) of slecht (rood) is. |
   | **[!UICONTROL True value]** en **[!UICONTROL False value]** | Alleen zichtbaar op gegevenstypen van een Booleaans schema. Hiermee kunt u het label van het dimensie-item aanpassen voor `true` en `false` waarden. |

   {style="table-layout:auto"}

## Valuta-conversie gebruiken

Valutaconversie in Customer Journey Analytics kan van zeer groot belang zijn voor bedrijven die internationaal actief zijn. Door de complexiteit van handmatige valutaomrekening weg te nemen, zorgt valutaomrekening in Customer Journey Analytics voor uniformiteit en duidelijkheid in de financiële gegevens. Bij de omrekening van valuta worden de dagelijkse historische wisselkoersen bijgehouden en deze dagkoersen gedurende een periode van vier jaar gehandhaafd.

Als bijvoorbeeld een e-commercebedrijf actief is in de VS, het Verenigd Koninkrijk en de EU, kunnen verkoopgegevens automatisch worden omgezet in USD, waardoor een gemakkelijke vergelijking en een holistisch begrip van de prestaties worden gewaarborgd.

>[!NOTE]
>
>Overweeg het volgende voordat u een metrische waarde voor valutaomzetting gaat configureren:
>
>* De metrische waarde die u selecteert voor valutaomzetting, moet een numeriek type hebben (Dubbel, Lang, Geheel getal, Kort, Byte).
>* Opstelling uw verbinding van de Customer Journey Analytics om minstens één gebeurtenisdataset te bevatten die een dimensie van de muntcode voor elke gebeurtenis bevat die een valuta metrisch bevat. Voor deze dimensie van de valutacode wordt een alfabetische valutacode gebruikt die voldoet aan de [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html) standaard voor de weergave van valuta&#39;s. Deze waarden moeten in hoofdletters worden ingevoerd, zoals USD voor $, EUR voor €, GBP voor £.

Om te bepalen hoe de valuta&#39;s voor bepaalde metrisch worden getoond en omgezet:

1. Beginnen metrisch te vormen waarvoor u munt als formaat, zoals hierboven beschreven, wilt gebruiken in [Vorm formaatmontages voor metrisch](#configure-format-settings-for-a-metric).

1. Selecteer de metrische waarde en maak de volgende selecties in het dialoogvenster [!UICONTROL **Indeling**] aan de rechterkant van de pagina:

   * In de [!UICONTROL **Indeling**] veld, selecteren [!UICONTROL **Valuta**].

   * In de [!UICONTROL **Decimale plaatsen**] het aantal decimalen dat de metrische weergave bevat.

     Deze optie is alleen beschikbaar als de metrische waarde een numeriek type &#39;Double&#39; heeft.

   * Selecteer de [!UICONTROL **Valuta converteren**] -optie.

   * In de [!UICONTROL **Dimensie valutacode selecteren**] , selecteert u de dimensie die de valuta vertegenwoordigt die u wilt converteren (de valuta waarop uw gegevens zijn gebaseerd). Selecteer bijvoorbeeld een dimensie die [!UICONTROL **Valutacode**].

     Als u geen dimensie hebt in uw huidige gegevensschema dat een gebied van de muntcode bevat, kunt u een nieuw gebied van de muntcode tot stand brengen gebruikend [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html), [Data Distiller](https://experienceleague.adobe.com/docs/experience-platform/query/data-distiller/overview.html), of [Afgeleide velden](/help/data-views/derived-fields/derived-fields.md). Data Prep is alleen geschikt voor nieuwe implementaties omdat het alleen op doorlopende basis gebeurt. Afhankelijk van de opstelling van een organisatie, kunnen de Gegevens Distiller en Afgeleide Gebieden worden gebruikt om tot de waarden van de valutacode historisch toegang te hebben.

   * In de [!UICONTROL **Valuta converteren en weergeven in**] , kiest u de valuta waarin u de gegevens wilt converteren.

1. Herhaal deze stappen als u valutaconversie wilt toepassen op extra metriek.



### Veelgestelde vragen

+++ Hoe wordt valutaomrekening uitgevoerd?

Op rapporttijd, wordt de waarde van de metrische en originele muntcode omgezet in USD en dan omgezet in de valuta die voor vertoning wordt gevormd. Voor deze omrekening worden de dagelijkse wisselkoersen gebruikt die op het tijdstip van de gebeurtenis van toepassing zijn.

+++

