---
title: Componentinstellingen opmaken
description: Vorm hoe metrisch wordt geformatteerd.
exl-id: 5ce13fe9-29fa-474c-bae3-65f275153a59
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: d65171873f68835de0628b95158f01713eaacb6b
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 1%

---

# Componentinstellingen opmaken {#format-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_metric_format"
>title="Indeling"
>abstract="Bepaal hoe een component wordt getoond wanneer gebruikt in rapporten."

<!-- markdownlint-enable MD034 -->


Het formaat laat u bepalen hoe bepaalde metrisch wanneer gebruikt in rapporten wordt getoond.

## Vorm formaatmontages voor metrisch

U kunt bepalen hoe een bepaalde metrische waarde wordt getoond door zijn formaatmontages aan te passen.

1. In Customer Journey Analytics, selecteer de [!UICONTROL **meningen van Gegevens**] tabel.

1. Selecteer de gegevensmening die de component bevat waarvan formaat dat u wilt vormen plaatst.

1. Selecteer de [!UICONTROL **Componenten**] tabel.

1. Selecteer de component die u wilt vormen, breid dan de [!UICONTROL **sectie van het Formaat**] op de rechterkant van de pagina uit.

   ![ montages van het Formaat ](../assets/format-settings.png)

1. Geef de volgende informatie op:

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Format]** | Hier kunt u de opmaak van een metrische waarde opgeven als Decimaal, Tijd, Percentage of Valuta. |
   | **[!UICONTROL Decimal]** | Niet zichtbaar op de gegevenstypen van het schema van het Geheel. Hier kunt u het aantal decimalen opgeven dat metrisch wordt weergegeven. |
   | **[!UICONTROL Date]** | Hiermee kunt u bepalen hoe het datum-tijdveld moet worden weergegeven wanneer dit als een dimensie in de rapportage wordt gebruikt. [Meer informatie](../../use-cases/data-views/data-views-usecases.md#date-and-date-time-use-cases) |
   | **[!UICONTROL Date-Time]** | Hiermee kunt u bepalen hoe het datum-tijdveld moet worden weergegeven wanneer dit als een dimensie in de rapportage wordt gebruikt. [Meer informatie](../../use-cases/data-views/data-views-usecases.md#date-and-date-time-use-cases) |
   | **[!UICONTROL Currency]** | Hiermee kunt u bepalen in welke valuta de metrische waarde moet worden weergegeven. <p>Als u globale gegevens analyseert waar de transacties in verschillende valuta voorkomen, zie [ de muntomzetting van het Gebruik ](#use-currency-conversion).</p> |
   | **[!UICONTROL Show upward trend as]** | Hier kunt u opgeven of een opwaartse trend in deze metrische waarde goed (groen) of slecht (rood) is. |
   | **[!UICONTROL True value]** en **[!UICONTROL False value]** | Alleen zichtbaar op gegevenstypen van een Booleaans schema. Hiermee kunt u het label van het dimensie-item aanpassen voor waarden `true` en `false` . |

   {style="table-layout:auto"}

## Valuta-conversie gebruiken {#use-currency-conversion}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_metric_format_currencyconversion"
>title="Omrekening in valuta"
>abstract="Selecteer een valutacodedimensie om valuta in een geselecteerd valutatype te configureren en weer te geven."

<!-- markdownlint-enable MD034 -->

Valutaconversie in Customer Journey Analytics kan van zeer groot belang zijn voor bedrijven die internationaal actief zijn. Door de complexiteit van handmatige valutaomrekening weg te nemen, zorgt valutaomrekening in Customer Journey Analytics voor uniformiteit en duidelijkheid in de financiële gegevens. Bij de omrekening van valuta worden de dagelijkse historische wisselkoersen bijgehouden en deze dagkoersen gedurende een periode van vier jaar gehandhaafd.

Als bijvoorbeeld een e-commercebedrijf actief is in de VS, het Verenigd Koninkrijk en de EU, kunnen verkoopgegevens automatisch worden omgezet in USD, waardoor een gemakkelijke vergelijking en een holistisch begrip van de prestaties worden gewaarborgd.

>[!NOTE]
>
>Overweeg het volgende voordat u een metrische waarde voor valutaomzetting gaat configureren:
>
>* De metrische waarde die u selecteert voor valutaomzetting, moet een numeriek type hebben (Dubbel, Lang, Geheel getal, Kort, Byte).
>* Opstelling uw verbinding van de Customer Journey Analytics om minstens één gebeurtenisdataset te bevatten die een dimensie van de muntcode voor elke gebeurtenis bevat die een valuta metrisch bevat. Die dimensie van de muntcode gebruikt een alfabetische muntcode die aan [ ISO 4217 ](https://www.iso.org/iso-4217-currency-codes.html) norm in overeenstemming is voor het vertegenwoordigen van valuta&#39;s. Deze waarden moeten in hoofdletters worden ingevoerd, zoals USD voor $, EUR voor €, GBP voor £.

Om te bepalen hoe de valuta&#39;s voor bepaalde metrisch worden getoond en omgezet:

1. Begin vormend metrisch waarvoor u munt als formaat wilt gebruiken, zoals hierboven beschreven, in [ vorm formaatmontages voor metrisch ](#configure-format-settings-for-a-metric).

1. Met metrisch geselecteerd, maak de volgende selecties in de [!UICONTROL **sectie van het Formaat**] op de rechterkant van de pagina:

   * Op het [!UICONTROL **gebied van het Formaat**], uitgezochte [!UICONTROL **Valuta**].

   * Op het [!UICONTROL **Decimale plaatsen**] gebied, kies het aantal decimalen de metrische vertoningen.

     Deze optie is alleen beschikbaar als de metrische waarde een numeriek type &#39;Double&#39; heeft.

   * Selecteer de [!UICONTROL **optie van de Valuta van de Bekeerling**].

   * In het [!UICONTROL **Uitgezochte de afmeting van de muntcode**] gebied, selecteer de afmeting die de munt vertegenwoordigt u van (de munt die uw gegevens gebaseerd is) omzet. Bijvoorbeeld, selecteer een dimensie genoemd [!UICONTROL **code van de Valuta**].

     Als u geen afmeting in uw huidig gegevensschema hebt dat een gebied van de muntcode bevat, kunt u een nieuw gebied van de muntcode tot stand brengen gebruikend ](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) de Prep van Gegevens 0}, [ Gegevens Distiller ](https://experienceleague.adobe.com/docs/experience-platform/query/data-distiller/overview.html), of [ Voortgekomen Gebieden ](/help/data-views/derived-fields/derived-fields.md). [ Data Prep is alleen geschikt voor nieuwe implementaties omdat het alleen op doorlopende basis gebeurt. Afhankelijk van de opstelling van een organisatie, kunnen de Gegevens Distiller en Afgeleide Gebieden worden gebruikt om tot de waarden van de valutacode historisch toegang te hebben.

   * In het [!UICONTROL **Bekeerling en vertoningsmunt in**] gebied, kies de munt waarin u gegevens wilt worden omgezet.

1. Herhaal deze stappen als u valutaconversie wilt toepassen op extra metriek.



### Veelgestelde vragen

+++ Hoe wordt valutaomrekening uitgevoerd?

Op rapporttijd, wordt de waarde van de metrische en originele muntcode omgezet in USD en dan omgezet in de valuta die voor vertoning wordt gevormd. Voor deze omrekening worden de dagelijkse wisselkoersen gebruikt die op het tijdstip van de gebeurtenis van toepassing zijn.

+++

