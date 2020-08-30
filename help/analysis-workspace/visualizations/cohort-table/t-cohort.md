---
description: Creeer een cohort en stel een rapport van de cohortanalyse in de Werkruimte van de Analyse in werking.
keywords: Analysis Workspace
title: Een cohortanalyserapport uitvoeren
topic: Reports and analytics
uuid: 5574230f-8f35-43ea-88d6-cb4960ff0bf4
translation-type: tm+mt
source-git-commit: 7862233892e56d1faafed6c14bd527db89ff1a3b
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---


# Vorm een [!UICONTROL Cohort Analysis] verslag

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Een cohort maken en een [!UICONTROL Cohort Analysis] rapport in de Werkruimte van de Analyse.

1. In de Werkruimte van de Analyse, klik **[!UICONTROL Visualizations]** pictogram in de linkerspoorstaaf en sleep een **[!UICONTROL Cohort Table]** naar het canvas.

   ![](assets/cohort-table.png)

1. Bepaal het **[!UICONTROL Inclusion Criteria]**, **[!UICONTROL Return Criteria]**, **[!UICONTROL Cohort Type]** en **[!UICONTROL Settings]** zoals gedefinieerd in onderstaande tabel.

| Element | Beschrijving |
| --- | --- |
| **[!UICONTROL Inclusion Criteria]** | U kunt tot 10 integratiesegmenten en tot 3 integratiemetriek toepassen. Metrisch specificeert welke plaatsen een gebruiker in een cohort. Bijvoorbeeld, als metrisch de opneming Orden is, slechts zullen de gebruikers die een orde tijdens de tijdwaaier van de cohortanalyse plaatsten in de aanvankelijke cohort worden omvat. <br> De standaardexploitant tussen metriek is EN, maar u kunt het in OF veranderen. Bovendien kunt u het numerieke filtreren aan deze metriek toevoegen. Bijvoorbeeld: &quot;Bezoeken >= 1&quot;. |
| **[!UICONTROL Return Criteria]** | U kunt tot 10 terugkeersegmenten en tot 3 terugkeermetriek toepassen. Metrisch wijst erop of de gebruiker (behoud) of niet (kurn) is behouden. Bijvoorbeeld, als de terugkeer metrisch VideoMeningen is, slechts zullen de gebruikers die video&#39;s tijdens verdere tijdsperioden (na de periode waarin zij aan een cohort) werden toegevoegd bekeken worden vertegenwoordigd zoals behouden. Een andere metrisch die behoud kwantificeert is Bezoeken. |
| **[!UICONTROL Granularity]** | De tijdsgranulariteit van Dag, Week, Maand, Kwartaal, of Jaar. |
| **[!UICONTROL Type]** | **[!UICONTROL Retention]** (standaard): Een retentiecohort meet hoe goed uw bezoekerscohorten na verloop van tijd terugkeren naar uw eigendom. Dit is het standaardcohort dat wij altijd hebben gehad en wijst op terugkeer en herhalend gebruikersgedrag. A [!UICONTROL Retention] Cohort wordt aangegeven door de kleur groen in de tabel. <br> **[!UICONTROL Churn]**: Een churn (ook wel &#39;attrition&#39; of &#39;fallout&#39; genoemd) cohort meet hoe je bezoekercohorten in de loop der tijd uit je bezit vallen. Churn = 1 - Bewaring. [!UICONTROL Churn] is een goede maatstaf voor kleverigheid en kansen door u te laten zien hoe vaak klanten niet terugkomen. U kunt kurn gebruiken om gebieden van nadruk te analyseren en te identificeren: welke cohortsegmenten kunnen enige aandacht krijgen . A [!UICONTROL Churn] Cohort wordt aangegeven door de kleur rood in de tabel (vergelijkbaar met de uitval in onze tabel) **[!UICONTROL Flow]** visualisatie). |
| **[!UICONTROL Settings]** | **[!UICONTROL Rolling Calculation]**: Bereken het behoud of de kurn op de vorige kolom, eerder dan de Included kolom (gebrek) wordt gebaseerd die. [!UICONTROL Rolling Calculation] verandert de berekeningsmethode voor uw &quot;terugkeer&quot;periodes. Bij de normale berekening worden gebruikers die aan de &quot;return&quot;-criteria voldoen en deel uitmaakten van de opnemingsperiode onafhankelijk van de vraag of zij al dan niet in de cohort voor de vorige periode waren opgenomen. In plaats daarvan, [!UICONTROL Rolling Calculation] vindt gebruikers die voldoen aan de &quot; return &quot; - criteria en deel uitmaakten van de vorige periode . Daarom [!UICONTROL Rolling Calculation] filters en treinen de gebruikers die voortdurend voldoen aan de &quot;return&quot; criteria over een periode. [!UICONTROL Return] criteria worden toegepast voor elk van de perioden die tot de geselecteerde periode leiden. <br> **[!UICONTROL Latency Table]**: A [!UICONTROL Latency] de lijst meet de tijd die vóór en na de opnemingsgebeurtenis is verstreken. [!UICONTROL Latency] is goed te gebruiken voor pre-/postanalyse. Bijvoorbeeld, als u een aanstaande product of een campagnemening hebt en u gedrag wilt volgen alvorens evenals zien hoe het na, uitvoert [!UICONTROL Latency] de tabel zal het gedrag vóór en na elkaar weergeven om de directe impact te zien . De pre-inclusiecellen in de [!UICONTROL Latency] De lijst wordt berekend door gebruikers die aan de [!UICONTROL Inclusion] criteria voor de opnemingsperiode en vervolgens aan de [!UICONTROL Return] criteria in de perioden vóór de opnemingsperiode. Merk op dat [!UICONTROL Latency] tabellen en [!UICONTROL Custom Dimension] Cohort kan niet samen worden gebruikt. <br> **[!UICONTROL Custom Dimension Cohort]**: Creeer cohorts die op de geselecteerde afmeting, eerder dan op tijd-gebaseerde cohorts (gebrek) worden gebaseerd. Vele klanten willen hun cohorten door iets buiten tijd analyseren en de nieuwe eigenschap van de Cohort van de Dimensie van de Douane voorziet u van de flexibiliteit om cohorts te bouwen die op afmetingen van hun het kiezen worden gebaseerd. De afmetingen van het gebruik zoals marketing kanaal, campagne, product, pagina, gebied, of een andere afmeting in de Analyse van Adobe om te tonen hoe de retentieveranderingen op de verschillende waarden van deze afmetingen worden gebaseerd. De [!UICONTROL Custom Dimension] De definitie van het cohortensegment past de dimensie-item alleen toe als onderdeel van de opnemingsperiode, niet als onderdeel van de terugkeerdefinitie. <br> Na het kiezen van [!UICONTROL Custom Dimension] De optie van de cohort, kunt u slepen en laten vallen welke afmeting u in de dalingsstreek wilt. Dit staat u toe om gelijkaardige afmetingspunten over de zelfde tijdspanne te vergelijken. Bijvoorbeeld, kunt u prestaties van steden naast elkaar, producten, campagnes, enz. vergelijken. Het zal uw hoogste 14 afmetingspunten terugkeren. Nochtans, kunt u een filter gebruiken (heb toegang tot het door op het recht van de afmeting te hangen die werd gesleept) om slechts gewenste afmetingspunten te tonen. A [!UICONTROL Custom Dimension] Cohort kan niet worden gebruikt met de [!UICONTROL Latency] Tabelfunctie. |

1. Pas de **[!UICONTROL Cohort Table Settings]** door op het pictogram voor het vistuig te klikken.

| Instelling | Beschrijving | | Alleen percentage weergeven | Verwijdert de aantalwaarde en toont slechts het percentage. | | Percentage afgerond tot op het dichtstbijzijnde gehele getal | Hiermee wordt de procentuele waarde afgerond op het dichtstbijzijnde gehele getal in plaats van de decimale waarde. | | Gemiddelde procentuele rij tonen | Neemt een nieuwe rij bij de bovenkant van de lijst op en voegt dan het gemiddelde voor de waarden binnen elke kolom toe. |

## De [!UICONTROL Cohort Analysis] verslag

1. Klik op **[!UICONTROL Build]**.

   ![Stap Resultaat](assets/cohort-report.png)

   Het rapport toont bezoekers die een orde plaatsten ( *`Included`* kolom), en wie bij volgende bezoeken op uw plaats terugkeerde. De vermindering van bezoeken in tijd laat u toe om problemen te ontdekken en actie te ondernemen.
1. (Facultatief) creeer een segment van een selectie.

   Selecteer cellen (aangrenzend of niet aangrenzend) en klik vervolgens met de rechtermuisknop > **[!UICONTROL Create Segment From Selection]**.

1. In de [Filter ontwerper](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html), geef het segment verder uit, dan klik **[!UICONTROL Save]**.

   Het opgeslagen segment is beschikbaar voor gebruik in [!UICONTROL Segment] paneel in [!UICONTROL Analysis Workspace].
1. De naam en bewaart uw cohortproject.
1. (facultatief) [Cursus en aandeel](/help/analysis-workspace/curate-share/curate.md) de projectcomponenten.

   >[!NOTE]
   >
   >U moet uw project bewaren alvorens de kromming beschikbaar is.

