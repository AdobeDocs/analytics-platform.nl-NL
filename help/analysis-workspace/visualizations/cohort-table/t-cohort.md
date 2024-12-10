---
description: Maak een cohorttabel en voer een cohortanalyse uit in Analysis Workspace.
keywords: Analysis Workspace
title: Een Cohortingtabel configureren
feature: Visualizations
exl-id: c3fd9fbf-b2c8-4703-92de-e6fdc141ebc6
role: User
source-git-commit: c16ad9f490abed1e15e1012a5a9347e2628b7642
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---

# Een Cohortingtabel configureren

Een [!UICONTROL Cohort table] maken en configureren:

1. Voeg a ![ TextNumbered ](/help/assets/icons/TextNumbered.svg) **[!UICONTROL Cohort table]** visualisatie toe. Zie [ een visualisatie aan een paneel ](../freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.

1. Definieer de waarden **[!UICONTROL Inclusion Criteria]** , **[!UICONTROL Return Criteria]** , **[!UICONTROL Cohort Type]** en **[!UICONTROL Settings]** zoals gedefinieerd in de onderstaande tabel.

   ![ vorm een cohortelijst ](assets/cohort-configure.png)

   | Element | Beschrijving |
   |--- |--- |
   | **[!UICONTROL Inclusion criteria]** | U kunt tot 10 integratiefilters en tot 3 integratiemetriek toepassen. Metrisch specificeert wat tot welke cohort een gebruiker behoort. Bijvoorbeeld, als inclusiemetrisch Orden is, slechts worden de gebruikers die een orde tijdens de tijdwaaier van de cohortanalyse plaatsten inbegrepen in de aanvankelijke cohort.<br> de standaardexploitant tussen metriek is EN, maar u kunt het in OF veranderen. Bovendien kunt u numerieke filters toevoegen aan deze cijfers. Bijvoorbeeld: `Sessions >= 1`.</br> |
   | **[!UICONTROL Return criteria]** | U kunt maximaal 10 retourfilters en maximaal 3 retourcijfers toepassen. Metrisch wijst erop of de gebruiker (behoud) of niet (klusje) is behouden. Als de retourwaarde bijvoorbeeld Video-weergaven is, worden alleen gebruikers die video&#39;s tijdens volgende tijdsperioden (na de periode waarin ze aan een cohort zijn toegevoegd) weergegeven als behouden. Een andere metrische waarde die het behoud kwantificeert, zijn sessies. |
   | **[!UICONTROL Granularity]** | De tijdsgranulariteit van Dag, Week, Maand, Kwart, of Jaar. |
   | **[!UICONTROL Type]** | **[!UICONTROL Retention]** (standaardwaarde): een **[!UICONTROL Retention]** -cohort meet hoe goed uw persoonlijke cohorten in de loop der tijd naar uw eigenschap terugkeren. Een retentiecohort is de standaardcohort en geeft het gedrag van de gebruiker voor retourneren en herhalen aan. Een groene kleur geeft een [!UICONTROL Retention] -kleur in de tabel aan.<br>**[!UICONTROL Churn]**: een **[!UICONTROL Churn]**-cohort (ook wel attrition of fallout genoemd) meet de manier waarop de cohorten van uw persoon uit uw eigenschap in de loop der tijd vallen. Churn is het tegenovergestelde van retentie: `Churn = 1 - Retention` . [!UICONTROL Churn] is een goede maatstaf voor kleverigheid en kansen door u te laten zien hoe vaak klanten niet terugkomen. U kunt churn gebruiken om aandachtsgebieden te analyseren en te identificeren: welke cohortfilters kunnen enige aandacht gebruiken? Een rode kleur geeft een [!UICONTROL Churn] -cohort in de tabel aan (vergelijkbaar met een fallout in de **[!UICONTROL Flow]**visualisatie). </br> |
   | **[!UICONTROL Settings]** | **[!UICONTROL Rolling calculation]**: berekent het behoud of de kolom op basis van de vorige kolom in plaats van de kolom Opgenomen (standaard). [!UICONTROL Rolling Calculation] wijzigt de berekeningsmethode voor de &#39;return&#39;-periodes. De normale berekening vindt gebruikers die aan de rendementscriteria voldoen en deel uitmaakten van de opnemingsperiode. Ongeacht of zij al dan niet in het cohort waren voor de voorgaande periode. In plaats daarvan zoekt [!UICONTROL Rolling Calculation] gebruikers die voldoen aan de &quot;return&quot;-criteria en die deel uitmaakten van de vorige periode. Daarom filtert [!UICONTROL Rolling Calculation] de gebruikers die voortdurend aan de periode van de &quot;terugkeer&quot;criteria voldoen. [!UICONTROL Return] -criteria worden toegepast op elk van de perioden die tot de geselecteerde periode leiden. </br><br>**[!UICONTROL Latency Table]**: Een [!UICONTROL Latency table] meet de tijd die is verstreken voor en na de insluitingsgebeurtenis. [!UICONTROL Latency table] is ideaal voor pre-/postanalyse. U hebt bijvoorbeeld een product of campagne die binnenkort wordt opgestart en u wilt het gedrag voor en na de introductie bijhouden. In [!UICONTROL Latency table] wordt het gedrag vóór en na het schrijven naast elkaar weergegeven om de directe invloed te zien. De cellen die vooraf in de opname zijn opgenomen in de [!UICONTROL Latency table] berekenen gebruikers die voldoen aan de [!UICONTROL Inclusion] -criteria voor de opnemingsperiode en vervolgens voldoen aan de [!UICONTROL Return] -criteria in de perioden vóór de opnemingsperiode. [!UICONTROL Latency table] en [!UICONTROL Custom dimension cohort] kunnen niet samen worden gebruikt.</br><br>**[!UICONTROL Custom dimension cohort]**: Maak cohorten op basis van de geselecteerde dimensie in plaats van op tijd gebaseerde cohorts (standaard). Vele klanten willen hun cohorten met iets anders dan tijd analyseren en de nieuwe eigenschap van de Cohort van het Dimension van de Douane biedt u de flexibiliteit om cohorten te bouwen die op afmetingen van hun kiezen worden gebaseerd. De afmetingen van het gebruik, zoals marketing kanaal, campagne, product, pagina, gebied, of een andere afmeting tonen hoe het behoud verandert die op de verschillende waarden van deze dimensies wordt gebaseerd. Bij de definitie van het filter [!UICONTROL Custom Dimension] Cohort wordt het item Dimensie alleen toegepast als onderdeel van de opnemingsperiode, niet als onderdeel van de retourdefinitie.</br><br> na het kiezen van de [!UICONTROL Custom dimension cohort] optie, kunt u slepen en neerzetten welke afmeting u in de dalingsstreek wilt. Door dimensies toe te voegen, kunt u vergelijkbare dimensie-items in dezelfde tijdsperiode vergelijken. U kunt bijvoorbeeld de prestaties van steden naast elkaar, producten, campagnes, enzovoort vergelijken. De tabel Cohort retourneert de bovenste 14 dimensieitems. Nochtans, kunt u filter van de Filter van de a ![ gebruiken ](/help/assets/icons/Filter.svg) om slechts gewenste afmetingspunten te tonen. Een [!UICONTROL Custom dimension cohort] kan niet worden gebruikt met de functie [!UICONTROL Latency table] . </br> |

1. Klik op **[!UICONTROL Build]**.
1. Om [!UICONTROL Cohort table] aan te passen, uitgezocht ![ geef ](/help/assets/icons/Edit.svg) uit.

1. (Optioneel) Maak een filter of publiek op basis van een selectie.

   Selecteer cellen (aangrenzend of niet aangrenzend) en klik vervolgens met de rechtermuisknop > **[!UICONTROL Create Filter From Selection]** .

   ![ creeer filter of publiek ](assets/retention-createfilter.png)

1. In de [ bouwer van de Filter ](/help/components/filters/filter-builder.md), geef verder de filter uit, dan klik **[!UICONTROL Save]**.

   Het opgeslagen filter is beschikbaar voor gebruik in het deelvenster [!UICONTROL Filter] in [!UICONTROL Analysis Workspace] .

## Instellingen

U kunt specifieke instellingen definiëren voor een [!UICONTROL Cohort table] .

1. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) om de [!UICONTROL Cohort table] montages aan te passen.

   | Instelling | Beschrijving |
   |---|---|
   | **toont slechts percenten** | Hiermee verwijdert u de getalwaarde en geeft u alleen het percentage weer. |
   | **Rond percenten aan dichtstbijzijnde geheel** | Rondt de percentagewaarde aan het meest dichtbijgelegen geheel in plaats van het tonen van de decimale waarde. |
   | **toon Gemiddelde Percentarij** | Hiermee voegt u een nieuwe rij boven aan de tabel in en voegt u vervolgens het gemiddelde voor de waarden binnen elke kolom toe. |


>[!MORELIKETHIS]
>
>[ voeg een visualisatie aan een paneel toe ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Visualisatie-instellingen ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Contextmenu Visualisatie ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>

