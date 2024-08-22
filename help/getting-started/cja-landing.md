---
title: Handleiding voor Customer Journey Analytics
description: Customer Journey Analytics landingspagina.
solution: Customer Journey Analytics
feature: Basics
exl-id: 7f67c497-386b-4442-a502-6b492f35c6e6
source-git-commit: a9dd06a7b9d7c1ee6d5be5b944564e971cfe5192
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 2%

---

# Handleiding voor Customer Journey Analytics

Deze handleiding voor technische documentatie biedt zelfhulp voor Customer Journey Analytics. Met Customer Journey Analytics kunt u uw klantgegevens vanuit elk kanaal dat u kiest (zowel online als offline) naar Adobe Experience Platform overbrengen. Analyseer deze gegevens op dezelfde manier als je bestaande digitale gegevens met Analysis Workspace vandaag.

Met Customer Journey Analytics kunt u bepalen hoe u online en offline gegevens in Analysis Workspace verbindt met een gemeenschappelijke klant-id, zodat u kenmerken, filters, stroom, fallout enz. kunt uitvoeren. van uw klantgegevens.

## Wat is nieuw?

Bekijk een glimp van de nieuwste verbeteringen in het product en de documentatie van de Customer Journey Analytics! Voor een uitvoerige lijst van eigenschappen, verbeteringen, en moeilijke situaties, controleer de gedetailleerde [ Nota&#39;s van de Versie ](../release-notes/latest.md). Bezoek de [ pagina van documentatieupdates ](../release-notes/doc-changes.md) om met de recentste veranderingen bijgewerkt te blijven.

>[!BEGINTABS]

>[!TAB  AI Medewerker ]

De Medewerker van AI is een conversatie ervaring die artsen toestaat om taken in een snel tempo uit te voeren - of zijn begrip concepten, het oplossen van problemenproblemen, of het zoeken door informatie. Het stelt ook niet-deskundigen in staat om deskundig taken uit te voeren en verhoogt de algemene kwaliteit van het werk.

[![afbeelding](assets/learn-more-button.svg)](/help/ai-assistant.md)

>[!TAB  Summiere gegevens ]

Staat u toe om tijdreeksgegevens in te brengen die geen persoon identiteitskaart hebben Deze tijdreeksgegevens kunnen worden gebruikt om verschillende gebruiksgevallen te ondersteunen, zoals

- Prestatie-indicatoren op hoog niveau presenteren als onderdeel van of naast gegevens op gebeurtenisniveau.
- Uploaden van doelen of doelen op een uur- of dagbasis, en vervolgens positioneren van deze doelen of doelen op basis van metriek op gebeurtenisniveau.

[![afbeelding](assets/learn-more-button.svg)](/help/data-views/summary-data.md)

>[!TAB  Grafiek-based stitching* ]

Door op grafiek-gebaseerde het stitching, kunt u de identiteitsgrafiek van de Dienst van de Identiteit van het Experience Platform gebruiken om een betere mening van de klantenreis te krijgen door: <ul><li>Gegevenssets samenvoegen met verschillende id&#39;s zonder dat er aanvullende gegevens moeten worden opgehaald, getransformeerd en geladen om één id te weerspiegelen.</li> <li>Verbetering van de dekking van de preferente of gouden identiteit voor één gegevensset door identiteiten over gegevensreeksen te delen;</li><li>Profielen die in Real-time Customer Data Platform en Journey Optimizer zijn gemaakt, worden uitgelijnd op personen in Customer Journey Analytics.</li></ul>

[![afbeelding](assets/learn-more-button.svg)](/help/stitching/overview.md#graph-based-stitching)

*_u moet het Eerste pakket voor op grafiek-gebaseerd het stitching hebben._*

>[!TAB  B2B raadplegingen ]

Als deel van het vormen van een verbinding, kunt u datasets voor specifieke B2B raadplegingsschema&#39;s omzetten om op persoon-gebaseerde raadplegingen op B2B- gegevens beter te steunen.

[![afbeelding](assets/learn-more-button.svg)](/help/connections/transform-datasets-b2b-lookups.md)

>[!TAB  Voortgekomen gebieden ]

Nieuwe afgeleide veldfuncties (Math, Next of Previous, Summarize, Deduplicate) en extra functiesjablonen (zoals Stuiterwaarden, Friendly Dataset Name, Holiday Season, Monthly Goals, Simple Bot Detection, enzovoort) zijn nu beschikbaar.

[![afbeelding](assets/learn-more-button.svg)](/help/data-views/derived-fields/derived-fields.md)

>[!TAB  BI uitbreiding* ]

De uitbreiding van BI laat SQL toegang tot de gegevensmeningen toe die u in Customer Journey Analytics hebt bepaald. U kunt uw favoriete hulpmiddel van BI nu gebruiken om rapportering en dashboards tot stand te brengen die op de zelfde gegevensmeningen die de gebruikers van de Customer Journey Analytics met hun projecten van Analysis Workspace gebruiken.

[![afbeelding](assets/learn-more-button.svg)](/help/data-views/bi-extension.md)

*_u moet het Uitgezochte pakket of hoger hebben om de uitbreiding van BI te gebruiken._*


<!--
>[!TAB Improved Audience Publising] 

Audiences that are published from Customer Journey Analytics are now available in the new **Audiences** section in Adobe Experience Platform. Audiences are now available in Experience Platform seconds after they are published from Customer Journey Analytics. Improved sorting and filter options in Experience Platform for Customer Journey Analytics audiences. 

[![image](assets/learn-more-button.svg)](/help/components/audiences/publish.md)

-->

>[!TAB  Voorspelling ]

Prognosering is een Analysis Workspace-functie voor het voorspellen van een standaard of berekende metrische waarde met een ondersteunde tijdgranulariteit (uur, dag, week, maand en jaar). Prognosering is alleen beschikbaar voor aan tijdreeksen gerelateerde gegevens.

[![afbeelding](assets/learn-more-button.svg)](/help/analysis-workspace/c-forecast/forecasting.md)

>[!TAB  Nieuwe documentatie ]

De nieuwe documentatiesecties zijn nu beschikbaar op:<ul><li>Samenvattingscase voor gegevensgebruik en B2B-voorbeeldgebruik.</li><li>Een upgrade uitvoeren van Adobe Analytics naar Customer Journey Analytics.</li><li>Gebruiksscenario&#39;s voor gegevensuitvoer en de vereiste Experience Platform- en klantenreisfuncties. </li></ul>Selecteer **[!UICONTROL Learn more]** voor deze en andere documentatie-updates.

[![afbeelding](assets/learn-more-button.svg)](/help/release-notes/doc-changes.md)

>[!ENDTABS]

## Beginnen met de basisbeginselen

Begin met het lezen van het materiaal in de koppelingen hieronder om uzelf vertrouwd te maken met de mogelijkheden en functies van de Customer Journey Analytics.

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="/help/getting-started/aa-vs-cja/overview.md"><img src="./assets/aa-vs-cja.png"></a>
    <div><strong> voorbij online gegevens </strong><br/> leren hoe de Customer Journey Analytics met Adobe Analytics vergelijkt, welke eigenschappen worden gedeeld en hoe u uw gegevens van Analytics kunt gebruiken.</div>
    </td>
    <td>
    <a href="/help/data-ingestion/data-ingestion.md"><img src="./assets/data-ingestion.png"></a>
    <div><strong> Samenvatting en gebruik gegevens </strong><br/> leren over de opties die u gegevens in Experience Platform moet opnemen en het voor analyse en het melden in Customer Journey Analytics gebruiken.</div>
    </td>
    <td>
    <a href="/help/guided-analysis/overview.md"><img src="./assets/product-analytics.png"></a>
    <div><strong> Geleide Analyse </strong><br/> Leer hoe te om werkschema's te gebruiken om gegevens en inzichten over de het productervaring van uw klant te bereiken. Product Analytics door middel van geleide analyse...
    </div>
    </td>
    <td>
    <a href="/help/analysis-workspace/home.md"><img src="./assets/workspace.png"></a>
    <div><strong> Analysis Workspace </strong><br/> het Gebruik Analysis Workspace om basis en geavanceerde analyse, zoals attributie, stroom en reservediagrammen, afmetingsonderverdelingen uit te voeren.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="/help/getting-started/aa-vs-cja/overview.md"><img src="./assets/learn-more-button.svg"></a></td>
    <td align="center"><a href="/help/data-ingestion/data-ingestion.md"><img src="./assets/learn-more-button.svg"></a></td>
    <td align="center"><a href="/help/guided-analysis/overview.md"><img src="./assets/learn-more-button.svg"></a></td>
    <td align="center"><a href="/help/analysis-workspace/home.md"><img src="./assets/learn-more-button.svg"></a></td>
    </tr>
</table>


## Documentatie verkennen

Begrijp hoe de Customer Journey Analytics met Adobe Analytics vergelijkt. En hoe u uw gegevens in de oplossing kunt krijgen en deze gegevens en de daaruit voortvloeiende analyse en rapporten kunt voorbereiden, bekijken, analyseren en democratiseren.

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
      <img src="./assets/analytics.svg" width="35px"><br/>
      <strong> Vergelijk met Adobe Analytics </strong><br/> <a href="/help/getting-started/aa-vs-cja/overview.md"> Overzicht </a> - <a href="/help/getting-started/aa-to-cja.md"> Evolutie </a> - <a href="/help/getting-started/aa-vs-cja/aa-data-in-cja.md"> de gegevens van Adobe Analytics van het Gebruik </a> - <a href="/help/getting-started/aa-vs-cja/cja-aa.md"> de steun van de Eigenschap </a> - <a href="/help/getting-started/aa-vs-cja/terminology.md"> Terminologie </a> - <a href="/help/getting-started/aa-vs-cja/data-processing-comparisons.md"> de verwerking van Gegevens </a>
    </td>
    <td>
      <img src="./assets/connections.svg" width="35px"><br/>
      <strong> Verbindingen </strong><br/> <a href="/help/connections/overview.md"> Overzicht </a> - <a href="/help/connections/create-connection.md"> creeer </a> - <a href="/help/connections/manage-connections.md"> beheer </a> - <a href="/help/stitching/overview.md"> Stitch </a> - <a href="/help/connections/combined-dataset.md"> Gecombineerde gebeurtenisdatasets </a> - <a href="/help/connections/standard-lookups.md"> StandaardLookups </a>
    </td>
     <td>
      <img src="./assets/dataviews.svg" width="35px"><br/>
      <strong> de meningen van Gegevens </strong><br/> <a href="/help/data-views/data-views.md"> Overzicht </a> - <a href="/help/data-views/create-dataview.md"> creeer of geef uit </a> - <a href="/help/data-views/session-settings.md"> montages van de Zitting </a> - <a href="/help/data-views/derived-fields/derived-fields.md"> Voortgekomen gebieden </a> - <a href="/help/data-views/summary-data.md"> Summiere gegevens </a> - <a href="/help/data-views/component-reference.md"> Verwijzing van de Component </a>
    </td>

</tr>
  <tr style="border: 0;">
    <td>
      <img src="./assets/workspace.svg" width="35px"><br/>
      <strong> de Projecten van Workspace </strong><br/> <a href="/help/analysis-workspace/home.md"> Analysis Workspace </a> - <a href="/help/analysis-workspace/perform-basic-analysis.md"> Basis </a> &amp; <a href="/help/analysis-workspace/perform-adv-analysis.md"> Geavanceerde analyse </a> - <a href="/help/analysis-workspace/build-workspace-project/freeform-overview.md"> Projecten </a> - <a href="/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md"> Visualisaties </a> - <a href="/help/analysis-workspace/c-panels/freeform-panel.md"> Punten </a>
    </td>
    <td>
      <img src="./assets/guided-analysis.svg" width="35px"><br/>
      <strong> Geleide Analyse </strong><br/> <a href="/help/guided-analysis/overview.md"> Overzicht </a> - <a href="/help/guided-analysis/types/active.md"> de Groei van de Gebruiker </a> - <a href="/help/guided-analysis/types/usage.md"> Trends </a> - <a href="/help/guided-analysis/types/friction.md"> Trechter </a> - <a href="/help/guided-analysis/types/release.md"> Effect </a> - <a href="/help/guided-analysis/industry-use-cases.md"> het gebruikscase van de Industrie </a>
    </td>
    <td>
      <img src="./assets/share.svg" width="35px"><br/>
      <strong> Aandeel, de uitvoer, integreert </strong><br/> <a href="/help/analysis-workspace/curate-share/share-projects.md"> Projecten </a> - <a href="/help/mobile-app/home.md"> de Dashboards van Analytics </a> - <a href="/help/report-builder/report-buider-overview.md"> Report Builder </a> - <a href="/help/components/exports/manage-exports.md"> de uitvoer van de Wolk </a> - <a href="/help/integrations/overview.md"> Integraties </a>
    </td>
  </tr>
</table>

## Aanvullende bronnen

<table style="table-layout:fixed"><tr style="border: 0;">
<td><strong> Customer Journey Analytics </strong><br/>
<a href="https://experienceleague.adobe.com/en/docs/customer-journey-analytics-learn/tutorials/overview" target="_blank"> Tutorials </a> - <a href="https://helpx.adobe.com/legal/product-descriptions/customer-journey-analytics.html" target="_blank"> het productbeschrijving van de Customer Journey Analytics </a> - <a href="https://helpx.adobe.com/legal/product-descriptions/adobe-analytics-addon-customer-journey-analytics.html" target="_blank"> Adobe Analytics (Customer Journey Analytics toe:voegen-op) productbeschrijving </a> - <a href="https://developer.adobe.com/cja-apis/docs/" target="_blank"> Customer Journey Analytics APIs </a> - <a href="/help/ai-assistant.md"> AI Medewerker </a>
</td>
<td><strong> Ingestie van Gegevens </strong><br/> <a href="/help/data-ingestion/data-ingestion.md"> Overzicht </a> - <a href="/help/data-ingestion/analytics.md"> Analytics </a> - <a href="/help/data-ingestion/aepwebsdk.md"> SDK van het Web </a> - <a href="/help/data-ingestion/aepmobilesdk.md"> Mobiele SDK </a> - <a href="/help/data-ingestion/batch.md"> Partij </a> - <a href="/help/data-ingestion/streaming.md"> Streaming </a> - <a href="/help/data-ingestion/sources.md"> Bronnen </a> - <a href="/help/data-ingestion/serverapi.md"> Server API </a>
</td>
</tr>
</table>


<table style="table-layout:auto" class="tablelayout-is-fixed"><tbody><tr style="border: 0;"><td><img src="./assets/newsletter.png"></td><td>
<b> blijf op de hoogte, draag aan de gemeenschap bij, en verhoog uw ervaring van de Customer Journey Analytics!</b><br> Bezoek de gemeenschap van Adobe Analytics om de functionaliteit met medepraktiseraars te bespreken. <a href="https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community"> sluit zich vandaag aan bij de gemeenschap!</a></td></tr></tbody></table>
