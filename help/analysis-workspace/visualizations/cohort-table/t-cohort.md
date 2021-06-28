---
description: Maak een cohort en voer een rapport voor cohortanalyse uit in Analysis Workspace.
keywords: Analysis Workspace
title: Een rapport voor cohortanalyse configureren
uuid: 5574230f-8f35-43ea-88d6-cb4960ff0bf4
exl-id: c3fd9fbf-b2c8-4703-92de-e6fdc141ebc6
source-git-commit: 8cee89a8ed656ad6376e64c8327aa7c94a937ce9
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 1%

---

# Een [!UICONTROL Cohort Analysis]-rapport configureren

Maak een cohort en voer een [!UICONTROL Cohort Analysis]-rapport uit in Analysis Workspace.

1. Klik in Analysis Workspace op het pictogram **[!UICONTROL Visualizations]** in de linkerrails en sleep een **[!UICONTROL Cohort Table]** naar het canvas.

   ![](assets/cohort-table.png)

1. Definieer **[!UICONTROL Inclusion Criteria]**, **[!UICONTROL Return Criteria]**, **[!UICONTROL Cohort Type]** en **[!UICONTROL Settings]** zoals gedefinieerd in de onderstaande tabel.

| Element | Beschrijving |
|--- |--- |
| **[!UICONTROL Inclusion Criteria]** | U kunt tot 10 integratiefilters en tot 3 integratiemetriek toepassen. Met de metrische waarde wordt opgegeven wat een gebruiker in een cohort plaatst. Bijvoorbeeld, als inclusiemetrisch Orden is, slechts zullen de gebruikers die een orde tijdens de tijdwaaier van de cohortanalyse plaatsten in de aanvankelijke cohort worden omvat.<br>De standaardoperator tussen metriek is AND, maar u kunt deze wijzigen in OR. Bovendien kunt u numerieke filters toevoegen aan deze cijfers. Bijvoorbeeld: &quot;Visit >= 1&quot;.</br> |
| **[!UICONTROL Return Criteria]** | U kunt maximaal 10 retourfilters en maximaal 3 retourcijfers toepassen. Metrisch wijst erop of de gebruiker (behoud) of niet (klusje) is behouden. Als de retourwaarde bijvoorbeeld Video-weergaven is, worden alleen gebruikers die video&#39;s tijdens volgende tijdsperioden (na de periode waarin ze aan een cohort zijn toegevoegd) weergegeven als behouden. Een andere maatstaf die retentie kwantificeert, zijn Bezoekingen. |
| **[!UICONTROL Granularity]** | De tijdsgranulariteit van Dag, Week, Maand, Kwart, of Jaar. |
| **[!UICONTROL Type]** | **[!UICONTROL Retention]**(standaard): Met een retentiecohort wordt gemeten hoe goed de bezoekerscohorten in de loop der tijd naar uw eigenschap terugkeren. Dit is het standaardcohort dat we altijd hebben gehad en dat het gedrag van gebruikers weergeeft en herhaalt. Een [!UICONTROL Retention] Cohort wordt aangegeven door de kleur groen in de tabel.<br>**[!UICONTROL Churn]**: Een churn (ook wel &#39;kenmerk&#39; of &#39;fallout&#39; genoemd) cohort meet hoe uw bezoekerscohorten in de loop der tijd uit uw eigendom vallen. Churn = 1 - Behoud. [!UICONTROL Churn] Dit is een goede maatstaf voor zelfgenoegzaamheid en mogelijkheden door u te laten zien hoe vaak klanten niet terugkomen. U kunt churn gebruiken om aandachtsgebieden te analyseren en te identificeren: Welke cohortfilters kunnen enige aandacht krijgen. Een [!UICONTROL Churn] Cohort wordt aangegeven door de kleur rood in de tabel (vergelijkbaar met fallout in onze **[!UICONTROL Flow]**visualisatie).</br> |
| **[!UICONTROL Settings]** | **[!UICONTROL Rolling Calculation]**: Bereken het behoud of de kromme op de vorige kolom, eerder dan de Included kolom (gebrek) wordt gebaseerd. [!UICONTROL Rolling Calculation] Hiermee wijzigt u de berekeningsmethode voor uw &quot;return&quot;-periodes. Bij de normale berekening zijn onafhankelijke gebruikers betrokken die aan de &quot;return&quot;-criteria voldoen en deel uitmaakten van de opnemingsperiode, ongeacht of zij al dan niet in het cohort voor de voorgaande periode waren opgenomen. [!UICONTROL Rolling Calculation] zoekt in plaats daarvan gebruikers die aan de &quot;terugkeercriteria&quot;voldoen en deel van de vorige periode uitmaakten. Daarom filtreert en treert [!UICONTROL Rolling Calculation] de gebruikers die voortdurend aan de periode van de &quot;terugkeer&quot;criteria voldoen. [!UICONTROL Return] criteria worden toegepast op elk van de perioden die tot de geselecteerde periode leiden. </br><br>**[!UICONTROL Latency Table]**: Een  [!UICONTROL Latency] tabel meet de tijd die is verstreken vóór en na de opnemingsgebeurtenis. [!UICONTROL Latency] is erg handig voor pre-/postanalyse. Als u bijvoorbeeld een product of campagne wilt starten en u wilt het gedrag vóór bijhouden en zien hoe het na de introductie functioneert, wordt het gedrag vóór en na de introductie naast elkaar weergegeven om de directe impact te zien. [!UICONTROL Latency] De cellen vóór opname in de tabel [!UICONTROL Latency] worden berekend door gebruikers die voldoen aan de [!UICONTROL Inclusion] criteria voor de opnemingsperiode en vervolgens voldoen aan de [!UICONTROL Return] criteria in de perioden vóór de opnemingsperiode. [!UICONTROL Latency] tabellen en [!UICONTROL Custom Dimension] cohort kunnen niet samen worden gebruikt.</br><br>**[!UICONTROL Custom Dimension Cohort]**: Maak cohorten op basis van de geselecteerde dimensie in plaats van op tijd gebaseerde cohorts (standaard). Veel klanten willen hun cohorten met iets anders dan tijd analyseren en de nieuwe functie van de Cohort van de Dimension van de Douane biedt u de flexibiliteit om cohorten te bouwen die op afmetingen van hun kiezen worden gebaseerd. Met afmetingen zoals marketingkanaal, campagne, product, pagina, regio of een andere dimensie in Customer Journey Analytics kunt u zien hoe de retentie verandert op basis van de verschillende waarden van deze dimensies. Bij de definitie van het filter [!UICONTROL Custom Dimension] Cohort wordt het item Dimensie alleen toegepast als onderdeel van de opnemingsperiode, niet als onderdeel van de retourdefinitie.</br><br>Nadat u de optie  [!UICONTROL Custom Dimension] Cohort hebt gekozen, kunt u de gewenste dimensie naar de neerzetzone slepen. Dit staat u toe om gelijkaardige afmetingspunten over de zelfde tijdspanne te vergelijken. U kunt bijvoorbeeld de prestaties van steden naast elkaar vergelijken, producten, campagnes, enzovoort. Het zal uw hoogste 14 afmetingspunten terugkeren. U kunt echter een filter gebruiken (dit filter openen door de muis boven de dimensie te houden die is aangesleept) om alleen gewenste dimensie-items weer te geven. Een [!UICONTROL Custom Dimension] Cohort kan niet worden gebruikt met de [!UICONTROL Latency] eigenschap van de Lijst.</br> |

1. Pas **[!UICONTROL Cohort Table Settings]** door het tandwielpictogram te klikken aan.

| Instelling | Beschrijving |
| Alleen percentage weergeven | Hiermee verwijdert u de getalwaarde en geeft u alleen het percentage weer. |
| Percentage afgerond op het dichtstbijzijnde gehele getal | Rondt de percentagewaarde aan het meest dichtbijgelegen geheel in plaats van het tonen van de decimale waarde. |
| Gemiddelde procentuele rij tonen | Hiermee voegt u een nieuwe rij boven aan de tabel in en voegt u vervolgens het gemiddelde voor de waarden binnen elke kolom toe. |

## Het [!UICONTROL Cohort Analysis]-rapport samenstellen

1. Klik op **[!UICONTROL Build]**.

   ![Stap Resultaat](assets/cohort-report.png)

   In het rapport worden bezoekers weergegeven die een bestelling hebben geplaatst ( *`Included`* kolom) en die bij volgende bezoeken zijn teruggekeerd naar uw site. De vermindering van bezoeken in tijd laat u toe om problemen te ontdekken en actie te ondernemen.
1. (Optioneel) Maak een filter van een selectie.

   Selecteer cellen (aangrenzend of niet aangrenzend) en klik vervolgens met de rechtermuisknop > **[!UICONTROL Create Filter From Selection]**.

1. Bewerk in [Filter Builder](/help/components/filters/manage-filters.md) het filter verder en klik vervolgens op **[!UICONTROL Save]**.

   Het opgeslagen filter is beschikbaar voor gebruik in het [!UICONTROL Filter] paneel in [!UICONTROL Analysis Workspace].
1. Geef uw cohortproject een naam en sla het op.
1. (Optioneel) [Curate en share](/help/analysis-workspace/curate-share/curate.md) de projectcomponenten.

   >[!NOTE]
   >
   >U moet uw project bewaren alvorens de kromming beschikbaar is.
