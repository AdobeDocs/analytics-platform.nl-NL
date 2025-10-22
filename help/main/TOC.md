---
git-repo: https://github.com/AdobeDocs/analytics-platform.nl-NL
cloud: Experience Cloud
product: adobe analytics
sub-product: customer journey
solution: Customer Journey Analytics
type: Documentation
index: true
user-guide-title: Handleiding voor Customer Journey Analytics
user-guide-description: Meer informatie over Adobe Customer Journey Analytics en hoe u Analysis Workspace kunt gebruiken met gegevens van Experience Platform.
breadcrumb-title: Handleiding voor Customer Journey Analytics
source-git-commit: 9c584bb7c66e9e6b2ef2fc49802fb6839db1d70a
workflow-type: tm+mt
source-wordcount: '1310'
ht-degree: 11%

---

# Adobe Customer Journey Analytics Guide {#using}

+ [Adobe Customer Journey Analytics Guide](../getting-started/cja-landing.md)

+ Aanvullende informatie {#releases}
   + [Meest recente release](../release-notes/latest.md)
   + [Opmerkingen voorafgaand aan de release](../release-notes/pre-release-notes.md)
   + [2025 releases](../release-notes/2025.md)
   + [2024 releases](../release-notes/2024.md)
   + [2023 releases](../release-notes/2023.md)
   + [2022 introducties](../release-notes/2022.md)
   + [Release 2021](../release-notes/2021.md)
   + [2020 introducties](../release-notes/2020.md)
   + [Strategie voor release van functies](../release-notes/releases.md)
   + [Documentatie-updates](../release-notes/doc-changes.md)

+ Aan de slag {#cja-overview}
   + Customer Journey Analytics {#cja-b2c-overview}
      + [Overzicht](../getting-started/cja-overview.md)
      + [Handleiding voor snel starten](../getting-started/cja-getting-started.md)
      + [Openingspagina](../getting-started/landing.md)
      + [Veelgestelde vragen](../getting-started/cja-faq.md)
      + [Vergelijk met BI-oplossingen](../getting-started/cja-vs-bi.md)
      + [AI-assistent](../ai-assistant.md)
      + [Data Insights Agent](../data-analysis-ai.md)
   + Customer Journey Analytics B2B edition {#cja-b2b}
      + [Overzicht](/help/getting-started/cja-b2b-edition.md)
      + [B2B-concepten en -functies](/help/getting-started/cja-b2b-concepts-features.md)
      + [Handleiding voor snel starten](/help/getting-started/cja-b2b-quick-start-guide.md)
      + [Overgangsgeleider](/help/getting-started/cja-b2b-transition.md)

+ Upgrade en vergelijk {#compare-aa-cja}
   + Upgrade naar Customer Journey Analytics {#upgrade-to-cja}
      + [Aan de slag](/help/getting-started/cja-upgrade/cja-upgrade-getstarted.md)
      + [Upgradepad kiezen](/help/getting-started/cja-upgrade/cja-upgrade-path.md)
      + [Gegevens verzenden naar platform](/help/getting-started/cja-upgrade/cja-upgrade-send-to-platform.md)
      + [Historische gegevens behouden](/help/getting-started/cja-upgrade/cja-upgrade-historical-data.md)
      + [Aanbevolen upgradeproces](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)
      + [Uw organisatie voorbereiden](/help/getting-started/cja-upgrade/cja-upgrade-org-readiness.md)
      + Architect en maak een schema {#schema}
         + [Uw schema archiveren](/help/getting-started/cja-upgrade/cja-upgrade-schema-architect.md)
         + [Uw schema maken](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md)
         + [Het bestaande schema gebruiken](/help/getting-started/cja-upgrade/cja-upgrade-schema-existing.md)
      + Een gegevensstroom maken {#create-datastream}
         + [Een gegevensstroom maken](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md)
         + [Platform toevoegen als service](/help/getting-started/cja-upgrade/cja-upgrade-datastream-addplatform.md)
      + Gegevenssets maken {#create-datasets}
         + [Een gegevensset maken](/help/getting-started/cja-upgrade/cja-upgrade-dataset.md)
         + [Opzoekgegevenssets maken voor classificaties](/help/getting-started/cja-upgrade/cja-upgrade-dataset-lookup.md)
         + [Inname van gegevensset controleren](/help/getting-started/cja-upgrade/cja-upgrade-dataset-ingestion.md)
      + De Web SDK implementeren met tags {#create-tags}
         + [Een tag voor uw eigenschap maken](/help/getting-started/cja-upgrade/cja-upgrade-tag-property.md)
         + [De extensie Web SDK toevoegen aan uw tag](/help/getting-started/cja-upgrade/cja-upgrade-tag-extension.md)
         + [De ladertag voor de Web SDK-extensie implementeren](/help/getting-started/cja-upgrade/cja-upgrade-tag-loader.md)
         + [XDM-logica voor gegevensverzameling toevoegen aan uw tag](/help/getting-started/cja-upgrade/cja-upgrade-tag-xdm.md)
      + [Handmatig de Web SDK implementeren](/help/getting-started/cja-upgrade/cja-upgrade-manual.md)
      + [Implementeer de Web SDK met de API](/help/getting-started/cja-upgrade/cja-upgrade-api.md)
      + [Verbinding maken](/help/getting-started/cja-upgrade/cja-upgrade-connection.md)
      + [Een gegevensweergave maken](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md)
      + [Een afgeleid veld voor een marketingkanaal maken](/help/getting-started/cja-upgrade/cja-upgrade-marketing-channel.md)
      + [Gegevensstroom valideren](/help/getting-started/cja-upgrade/cja-upgrade-validate.md)
      + [Streaming media-verzameling instellen](/help/getting-started/cja-upgrade/cja-upgrade-streaming-media.md)
      + Historische gegevens behouden met de bronaansluiting Analytics {#historical-data-source-connector}
         + [Maak een XDM-schema voor de bronconnector van Analytics](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md)
         + [De bronaansluiting voor Analytics en kaartvelden maken](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md)
         + [Voeg de gegevensset van de bron van de Analyse aan de verbinding toe](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md)
      + [Bepalen wanneer Adobe Analytics moet worden uitgeschakeld](/help/getting-started/cja-upgrade/cja-upgrade-fully-move.md)
      + [Adobe Analytics uitschakelen](/help/getting-started/cja-upgrade/cja-upgrade-disable-appmeasurement.md)
      + Alternatieve upgrademethoden {#alternative-upgrade-methods}
         + [AppMeasurement-gegevensverzameling gebruiken](/help/getting-started/cja-upgrade/cja-upgrade-alternative-appmeasurement.md)
         + [Gegevenslaag verzenden](/help/getting-started/cja-upgrade/cja-upgrade-alternative-data-layer.md)
         + [Bronconnector voor analyse](/help/getting-started/cja-upgrade/cja-upgrade-alternative-source-connector.md)
      + Andere upgradescenario&#39;s {#other-upgrade-scenarios}
         + [Van de bron Analytics schakelaar aan het Web SDK](/help/getting-started/cja-upgrade/cja-upgrade-from-source-connector.md)
         + [Upgrade van een niet-Adobe Analytics-oplossing](/help/getting-started/cja-upgrade/cja-upgrade-third-party-solution.md)
      + Aanvullende informatie {#additional-information}
         + [De implementatie van Analytics begrijpen](/help/getting-started/cja-upgrade/cja-upgrade-analytics-implementation.md)
         + [Adobe Analytics-functieondersteuning bij upgrades](/help/getting-started/cja-upgrade/cja-upgrade-adobe-analytics-features.md)
         + [Customer Journey Analytics-functies](/help/getting-started/cja-upgrade/cja-upgrade-customer-journey-analytics-features.md)
         + [Implementatieopties voor Web SDK](/help/getting-started/cja-upgrade/cja-upgrade-websdk-implementation.md)
         + [Adobe Analytics Web SDK for Platform configureren](/help/getting-started/cja-upgrade/cja-upgrade-existing-adobe-analytics-websdk.md)
         + [Verpersoonlijking gebruiken met Adobe Journey Optimizer](/help/getting-started/cja-upgrade/cja-upgrade-personalization-journeyoptimizer.md)
   + Vergelijken met Adobe Analytics {#cja-aa-comparison}
      + [Overzicht](../getting-started/aa-vs-cja/overview.md)
      + [Adobe Analytics-gegevens gebruiken](../getting-started/aa-vs-cja/aa-data-in-cja.md)
      + [Functieondersteuning](../getting-started/aa-vs-cja/cja-aa.md)
      + [Terminologie vergelijken](../getting-started/aa-vs-cja/terminology.md)
      + [Gegevensverwerking vergelijken](../getting-started/aa-vs-cja/data-processing-comparisons.md)
      + [Omgevingen](../getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md)
      + [Analyseverwerking versus Data Prep](../getting-started/aa-vs-cja/pr-vista-dataprep.md)
      + [Analytische identiteiten](../getting-started/aa-vs-cja/aaid-ecid-adc.md)
   + [Evolutie uit Adobe Analytics](../getting-started/aa-to-cja.md)
   + [Gebruikershandleiding voor Adobe Analytics-gebruikers](../getting-started/aa-to-cja-user.md)

+ Gegevensinvoer {#cja-data-ingestion}
   + [Overzicht](../data-ingestion/data-ingestion.md)
   + Hulplijnen voor snel starten samenstellen en gebruiken{#ingest-use-guides}
      + [Adobe Analytics](../data-ingestion/analytics.md)
      + Experience Platform Edge Network {#edge-network}
         + [Web SDK](../data-ingestion/aepwebsdk.md)
         + [Mobile SDK](../data-ingestion/aepmobilesdk.md)
         + [Server-API](../data-ingestion/serverapi.md)
      + [Batchgegevens](../data-ingestion/batch.md)
      + [Streaming gegevens](../data-ingestion/streaming.md)
      + [Source-connectors](../data-ingestion/sources.md)
      + [Ad-hocgegevens](/help/data-ingestion/adhoc.md)

+ Gegevensspiegel {#cja-data-mirror}
   + [Overzicht](/help/data-mirror/data-mirror.md)
   + Configureren {#configure}
      + [Native oplossingen voor gegevenspakhuis](/help/data-mirror/datawarehouse.md)
      + [Experience Platform](/help/data-mirror/aep.md)
      + [Customer Journey Analytics](/help/data-mirror/cja.md)
   + [Data Mirror-handleiding voor snel starten](/help/data-mirror/model-based.md)

+ Verbindingen {#cja-connections}
   + [Overzicht van verbindingen](../connections/overview.md)
   + [Verbinding maken of bewerken](../connections/create-connection.md)
   + [Verbindingen beheren](../connections/manage-connections.md)
   + [Gecombineerde gegevenssets voor gebeurtenissen](../connections/combined-dataset.md)
   + [Standaardzoekopdrachten](../connections/standard-lookups.md)
   + [B2B-zoekopdrachten](../connections/transform-datasets-b2b-lookups.md)

+ Gegevens weergeven {#cja-dataviews}
   + [Overzicht van gegevensweergaven](../data-views/data-views.md)
   + [Een gegevensweergave maken of bewerken](../data-views/create-dataview.md)
   + [Sessieinstellingen](../data-views/session-settings.md)
   + Componentinstellingen {#component-settings}
      + [Overzicht van componentinstellingen](../data-views/component-settings/overview.md)
      + [Attributie](../data-views/component-settings/attribution.md)
      + [Gedrag](../data-views/component-settings/behavior.md)
      + [Indeling](../data-views/component-settings/format.md)
      + [Waarden uitsluiten opnemen](../data-views/component-settings/include-exclude-values.md)
      + [Metrische deduplicatie](../data-views/component-settings/metric-deduplication.md)
      + [Geen waardeopties](../data-views/component-settings/no-value-options.md)
      + [Persistentie](../data-views/component-settings/persistence.md)
      + [Subtekenreeks](../data-views/component-settings/substring.md)
      + [Samenvattingsgegevensgroep](../data-views/component-settings/summary-data-group.md)
      + [Waardebeperking](../data-views/component-settings/value-bucketing.md)
   + [Standaardcomponentverwijzing](../data-views/component-reference.md)
   + [BI-extensie](../data-views/bi-extension.md)
   + [Afgeleide velden](../data-views/derived-fields/derived-fields.md)
   + [Samenvattingsgegevens](../data-views/summary-data.md)
   + [Labels en beleid](../data-views/data-governance.md)
   + Gedeelde metriek en dimensies{#shared-metrics-dimensions}
      + [Overzicht](/help/data-views/shared-metrics-dimensions/smd-overview.md)
      + [Editor](/help/data-views/shared-metrics-dimensions/shared-component-editor.md)

+ Gereedschappen {#tools}
   + Asset Transfer {#asset-transfer}
      + [&#x200B; activa van de Overdracht &#x200B;](../tools/asset-transfer/transfer-assets.md)
   + Productgebruik {#product-usage}
      + [Overzicht](../tools/product-usage/usage-overview.md)
      + [Gegevensinstellingen](../tools/product-usage/data-settings.md)
      + [Instellingen voor Uitschakelen](../tools/product-usage/opt-out-settings.md)

+ Workspace-projecten {#cja-workspace}
   + [Overzicht van Analysis Workspace](../analysis-workspace/home.md)
   + [Basisanalyse uitvoeren](../analysis-workspace/perform-basic-analysis.md)
   + [Geavanceerde analyse uitvoeren](../analysis-workspace/perform-adv-analysis.md)
   + Projecten {#build-workspace-project}
      + [Overzicht](../analysis-workspace/build-workspace-project/freeform-overview.md)
      + [Snel projecten starten](/help/analysis-workspace/build-workspace-project/starter-projects.md)
      + [Projecten maken](/help/analysis-workspace/build-workspace-project/create-projects.md)
      + [Projecten openen](/help/analysis-workspace/build-workspace-project/open-projects.md)
      + [Opmerkingen over projecten](/help/analysis-workspace/build-workspace-project/comment-projects.md)
      + [Projecten opslaan](../analysis-workspace/build-workspace-project/save-projects.md)
      + [Inhoudsopgave](../analysis-workspace/build-workspace-project/project-table-of-contents.md)
      + Mappen in Workspace {#workspace-folders}
         + [Overzicht](../analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)
         + [Mappen maken](../analysis-workspace/build-workspace-project/workspace-folders/create-folders.md)
         + [Mappen beheren](../analysis-workspace/build-workspace-project/workspace-folders/manage-folders.md)
         + [Projecten toevoegen of verplaatsen](../analysis-workspace/build-workspace-project/workspace-folders/add-projects.md)
      + [Hotkeys](../analysis-workspace/build-workspace-project/fa-shortcut-keys.md)
      + [Kleurenpaletten](../analysis-workspace/build-workspace-project/color-palettes.md)
      + [Weergavedichtheid](../analysis-workspace/build-workspace-project/view-density.md)
      + [Debugger](../analysis-workspace/build-workspace-project/debugger.md)
   + Sjablonen {#templates}
      + [Sjablonen gebruiken](../analysis-workspace/templates/use-templates.md)
      + [Sjablonen maken en beheren](../analysis-workspace/templates/create-templates.md)
   + Visualisaties {#visualizations}
      + [Overzicht](../analysis-workspace/visualizations/freeform-analysis-visualizations.md)
      + [Gegevensbronnen beheren](../analysis-workspace/visualizations/t-sync-visualization.md)
      + [Intelligente bijschriften](../analysis-workspace/visualizations/intelligent-captions.md)
      + Vrije-vormtabel {#freeform-table}
         + [Overzicht](../analysis-workspace/visualizations/freeform-table/freeform-table.md)
         + [Hyperlinks maken](/help/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md)
         + [Getraalde gegevens weergeven](/help/analysis-workspace/visualizations/freeform-table/freeform-table-trended-data.md)
         + [Filteren en sorteren](../analysis-workspace/visualizations/freeform-table/filter-and-sort.md)
         + [Totalen](../analysis-workspace/visualizations/freeform-table/workspace-totals.md)
         + Instellingen voor kolommen en rijen {#column-row-settings}
            + [Kolominstellingen](../analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)
            + [Rijinstellingen](../analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)
            + [Dynamische en statische items](../analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md)
      + Cohortingtabel {#cohort-table}
         + [Overzicht](../analysis-workspace/visualizations/cohort-table/cohort-analysis.md)
         + [Configureren](../analysis-workspace/visualizations/cohort-table/t-cohort.md)
         + [Gebruik hoofdletters](../analysis-workspace/visualizations/cohort-table/cohort-use-cases.md)
      + Fallout {#fallout}
         + [Overzicht](../analysis-workspace/visualizations/fallout/fallout-flow.md)
         + [Configureren](../analysis-workspace/visualizations/fallout/configuring-fallout.md)
         + [Interdimensionale uitval](../analysis-workspace/visualizations/fallout/configuring-interdimensional-fallout.md)
         + [Segmenten toepassen](../analysis-workspace/visualizations/fallout/compare-segments-fallout.md)
      + Stroom {#flow}
         + [Overzicht](../analysis-workspace/visualizations/c-flow/flow.md)
         + [Configureren](../analysis-workspace/visualizations/c-flow/create-flow.md)
         + [Interdimensionale stromen](../analysis-workspace/visualizations/c-flow/multi-dimensional-flow.md)
      + Reiscanvas {#journey-canvas}
         + [Overzicht](../analysis-workspace/visualizations/journey-canvas/journey-canvas.md)
         + [Configureren](../analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md)
         + [Problemen oplossen](../analysis-workspace/visualizations/journey-canvas/journey-canvas-troubleshooting.md)
      + [Gebied (gestapeld)](../analysis-workspace/visualizations/area.md)
      + [Staaf (gestapeld)](../analysis-workspace/visualizations/bar.md)
      + [Opsommingsteken](../analysis-workspace/visualizations/bullet-graph.md)
      + [Combo](../analysis-workspace/visualizations/combo-charts.md)
      + [Donut](../analysis-workspace/visualizations/donut.md)
      + [Histogram](../analysis-workspace/visualizations/histogram.md)
      + [Horizontale balk (gestapeld)](../analysis-workspace/visualizations/horizontal-bar.md)
      + [Samenvatting van metrische sleutel](../analysis-workspace/visualizations/key-metric.md)
      + [Lijn](../analysis-workspace/visualizations/line.md)
      + [Kaart](/help/analysis-workspace/visualizations/map.md)
      + [Spreiding](../analysis-workspace/visualizations/scatterplot.md)
      + [Sectiekop](/help/analysis-workspace/visualizations/section-header.md)
      + [Samenvattingsnummer en wijziging](../analysis-workspace/visualizations/summary-number-change.md)
      + [Tekst](../analysis-workspace/visualizations/text.md)
      + [Treemap](../analysis-workspace/visualizations/treemap.md)
      + [Venn](../analysis-workspace/visualizations/venn.md)
   + Deelvensters {#panels}
      + [Overzicht](../analysis-workspace/c-panels/panels.md)
      + [Leeg deelvenster](../analysis-workspace/c-panels/blank-panel.md)
      + [Attributie](../analysis-workspace/c-panels/attribution.md)
      + [Experimentatie](../analysis-workspace/c-panels/experimentation.md)
      + [Vrije vorm](../analysis-workspace/c-panels/freeform-panel.md)
      + [Gemiddeld aantal minuten voor medium](/help/analysis-workspace/c-panels/average-minute-audience-panel.md)
      + [Gelijktijdige viewers voor media](../analysis-workspace/c-panels/media-concurrent-viewers.md)
      + [De afspeeltijd van media is verstreken](../analysis-workspace/c-panels/media-playback-time-spent.md)
      + [Volgende of vorige item](../analysis-workspace/c-panels/next-previous.md)
      + [Snelle inzichten](../analysis-workspace/c-panels/quickinsight.md)
   + Curven en delen {#curate-share}
      + [Overzicht](../analysis-workspace/curate-share/send-schedule-files.md)
      + [Cursieve projecten](../analysis-workspace/curate-share/curate.md)
      + [Projecten delen](../analysis-workspace/curate-share/share-projects.md)
      + [Deelbare koppelingen maken](../analysis-workspace/curate-share/shareable-links.md)
      + [Alleen-lezen projecten](../analysis-workspace/curate-share/view-only-projects.md)
      + [Presentaties genereren](/help/analysis-workspace/curate-share/generate-slides.md)
   + Exporteren {#export}
      + [Overzicht](../analysis-workspace/export/export-project-overview.md)
      + [Downloaden](../analysis-workspace/export/download-send.md)
      + [Verzenden en plannen](../analysis-workspace/export/t-schedule-report.md)
      + [Naar de cloud exporteren](../analysis-workspace/export/export-cloud.md)
   + Attributie {#attribution}
      + [Overzicht van kenmerken](../analysis-workspace/attribution/overview.md)
      + [Venster Model, container en lookback](../analysis-workspace/attribution/models.md)
      + [Algorithmic, toewijzing](../analysis-workspace/attribution/algorithmic.md)
      + [Best practices](../analysis-workspace/attribution/best-practices.md)
      + [Veelgestelde vragen](../analysis-workspace/attribution/faq.md)
   + Anomaliedetectie {#anomaly-detection}
      + [Overzicht](../analysis-workspace/c-anomaly-detection/anomaly-detection.md)
      + [anomalieën weergeven](../analysis-workspace/c-anomaly-detection/view-anomalies.md)
      + [Statistische technieken](../analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)
   + Voorspelling {#forecasting}
      + [Overzicht](../analysis-workspace/c-forecast/forecasting.md)
      + [Prognoses weergeven](../analysis-workspace/c-forecast/view-forecasts.md)
      + [Statistische technieken](../analysis-workspace/c-forecast/statistics-forecasting.md)
   + [Gebruikersvoorkeuren](../analysis-workspace/user-preferences.md)
   + Veelgestelde vragen over Workspace en meer {#workspace-faq}
      + [Veelgestelde vragen](../analysis-workspace/workspace-faq/faq.md)
      + [Prestaties optimaliseren](../analysis-workspace/workspace-faq/optimizing-performance.md)
      + [Fout en problemen oplossen](../analysis-workspace/workspace-faq/error-messages.md)
      + [Beperkingen](../analysis-workspace/workspace-faq/aw-limitations.md)
      + [Vereisten](../analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md)
      + [Toegankelijkheid](../analysis-workspace/workspace-faq/aw-accessibility.md)

+ Content Analytics {#content-analytics}
   + [Overzicht](/help/content-analytics/content-analytics.md)
   + Rapport {#report}
      + [Overzicht](/help/content-analytics/report/report.md)
      + [Onderdelen](/help/content-analytics/report/components.md)
   + Configuratie {#configuration}
      + [Overzicht](/help/content-analytics/config/configuration.md)
      + [Configuratie met instructies](/help/content-analytics/config/guided.md)
      + [Handmatige configuratie](/help/content-analytics/config/manual.md)
      + [Dataverzameling](/help/content-analytics/config/datacollection.md)

+ Analysedashboards {#cja-dashboards}
   + [Overzicht](../mobile-app/home.md)
   + [Curatortaken](../mobile-app/curator.md)
   + [Mobiele scorecards maken](../mobile-app/create-scorecard.md)
   + [Mobiele scorecards beheren](../mobile-app/manage-scorecard.md)
   + [Stel managers in voor het gebruik van dashboards](../mobile-app/set-up-execs.md)
   + [Snelle handleiding voor gebruikers](../mobile-app/executive.md)

+ Analyse met instructies {#guided-analysis}
   + [Overzicht](../guided-analysis/overview.md)
   + [Actieve groei](../guided-analysis/types/active-growth.md)
   + [Conversietrends](../guided-analysis/types/conversion-trends.md)
   + [Betrokkenheid](../guided-analysis/types/engagement.md)
   + [Effect voor eerste gebruik](../guided-analysis/types/first-use-impact.md)
   + [Frequentie](../guided-analysis/types/frequency.md)
   + [Trechter](../guided-analysis/types/funnel.md)
   + [Netto groei](../guided-analysis/types/net-growth.md)
   + [Geen effect](../guided-analysis/types/release-impact.md)
   + [Bewaren](../guided-analysis/types/retention.md)
   + [Tijdlijn](../guided-analysis/types/timeline.md)
   + [Trends](../guided-analysis/types/trends.md)
   + [Industriële gebruiksgevallen](../guided-analysis/industry-use-cases.md)
   + [Veelgestelde vragen](../guided-analysis/faq.md)

+ Onderdelen {#cja-components}
   + [Overzicht](../components/overview.md)
   + [Componenten gebruiken](../components/use-components-in-workspace.md)
   + [Componentbeschrijvingen toevoegen](../components/add-component-descriptions.md)
   + Annotaties {#annotations}
      + [Overzicht](../components/annotations/overview.md)
      + [Annotaties maken](../components/annotations/create-annotations.md)
      + [Annotaties beheren](../components/annotations/manage-annotations.md)
      + [Annotaties weergeven](../components/annotations/view-annotations.md)
      + [Mobiele scorecardannotaties](../components/annotations/mobile-annotations.md)
   + Soorten publiek {#audiences}
      + [Overzicht publiek](../components/audiences/audiences-overview.md)
      + [Soorten publiek maken en publiceren](../components/audiences/publish.md)
      + [Soorten publiek beheren](../components/audiences/manage.md)
   + Dimensies {#dimensions}
      + [Overzicht](../components/dimensions/overview.md)
      + [Voorvertoningsafmetingen](../components/dimensions/view-dimensions.md)
      + [Afmetingen onderverdelingen](../components/dimensions/t-breakdown-fa.md)
      + [Afmetingen van tijd tot tijd](../components/dimensions/time-parting-dimensions.md)
      + [Afmetingen van hoge kardinaliteit](../components/dimensions/high-cardinality.md)
   + [Metrics](../components/apply-create-metrics.md)
   + Segmenten {#segments}
      + [Overzicht](/help/components/segments/seg-overview.md)
      + [Segmenten maken](/help/components/segments/seg-create.md)
      + [Segmenten maken](/help/components/segments/seg-builder.md)
      + [Snelle segmenten](/help/components/segments/seg-quick.md)
      + [Sequentiële segmenten](/help/components/segments/seg-sequential-build.md)
      + [Segmenten delen](/help/components/segments/seg-share.md)
      + [Tagsegmenten](/help/components/segments/seg-tag.md)
      + [De lijst met segmenten filteren](/help/components/segments/seg-filter.md)
      + [Segmenten markeren als favoriet](/help/components/segments/seg-favorite.md)
      + [Segmenten goedkeuren](/help/components/segments/seg-approve.md)
      + [Segmenten kopiëren](/help/components/segments/seg-copy.md)
      + [Segmenten beheren](/help/components/segments/seg-manage.md)
      + [Operatoren](/help/components/segments/seg-operators.md)
      + [Segmenten gebruiken](/help/components/segments/seg-use.md)
   + Berekende cijfers {#cja-calcmetrics}
      + [Overzicht](../components/calc-metrics/calc-metr-overview.md)
      + Workflow {#cm-workflow}
         + [Berekende waarden maken](../components/calc-metrics/cm-workflow/cm-workflow.md)
         + [Metrische gegevens zoeken](../components/calc-metrics/cm-workflow/cm-finding.md)
         + [Berekende maatstaven samenstellen](../components/calc-metrics/cm-workflow/cm-build-metrics.md)
         + [Een eenvoudig voorbeeld](../components/calc-metrics/cm-workflow/cm-pvv.md)
         + [Een complexer voorbeeld](../components/calc-metrics/cm-workflow/cm-orders-participation.md)
         + [Type en attributie metrisch](../components/calc-metrics/cm-workflow/m-metric-type-alloc.md)
         + [Metrische gegevens voor deelname](../components/calc-metrics/cm-workflow/participation-metric.md)
         + [Gesegmenteerde metriek](../components/calc-metrics/cm-workflow/metrics-with-segments.md)
         + [Segmenten stapelen en vervangen](../components/calc-metrics/cm-workflow/cm-stack-seg.md)
         + [Berekende maateenheden filteren](../components/calc-metrics/cm-workflow/cm-filter.md)
         + [Berekende metriek markeren als favoriet](../components/calc-metrics/cm-workflow/cm-favorite.md)
         + [Berekende cijfers kopiëren](../components/calc-metrics/cm-workflow/cm-copy.md)
         + [Functies gebruiken](../components/calc-metrics/cm-workflow/cm-using-functions.md)
         + [Berekende maatstaven voor tags](../components/calc-metrics/cm-workflow/cm-tagging.md)
         + [Berekende waarden goedkeuren](../components/calc-metrics/cm-workflow/cm-approving.md)
         + [Berekende maatstaven delen](../components/calc-metrics/cm-workflow/cm-sharing.md)
         + [Berekende waarden beheren](../components/calc-metrics/cm-workflow/cm-manager.md)
         + [Voorbeelden](../components/calc-metrics/cm-workflow/cm-weighted-metric.md)
      + [Sjablonen voor berekende metriek](../components/calc-metrics/default-calcmetrics.md)
      + [Basisfuncties](../components/calc-metrics/cm-functions.md)
      + [Geavanceerde functies](../components/calc-metrics/cm-adv-functions.md)
   + Datumbereiken {#cja-date-ranges}
      + [Overzicht](../components/date-ranges/overview.md)
      + [Datumbereiken maken](../components/date-ranges/create.md)
      + [Datumbereiken beheren](../components/date-ranges/manage.md)
      + [Datumvergelijking](../components/date-ranges/time-comparison.md)
      + [Voorbeelden](../components/date-ranges/custom-date-ranges.md)
   + Waarschuwingen {#alerts}
      + [Overzicht](/help/components/c-intelligent-alerts/intelligent-alerts.md)
      + [Waarschuwingen maken](/help/components/c-intelligent-alerts/alert-builder.md)
      + [Waarschuwingen beheren](/help/components/c-intelligent-alerts/alert-manager.md)
      + [Functievergelijking](/help/components/c-intelligent-alerts/alerts-feature-comparison.md)
      + [Gebruik hoofdletters](/help/components/c-intelligent-alerts/alerts-use-cases.md)
   + Uitvoer {#exports}
      + [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md)
      + [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md)
      + [Cloud-exportlocaties beheren](/help/components/exports/manage-export-locations.md)
      + [Exporteren beheren](/help/components/exports/manage-exports.md)
      + [Exportlogboeken beheren](/help/components/exports/manage-export-logs.md)
      + [Problemen met exporteren oplossen](/help/components/exports/troubleshoot-exports.md)
   + Gegevenswoordenboek {#data-dictionary}
      + [Overzicht](../components/data-dictionary/data-dictionary-overview.md)
      + [Componentinformatie weergeven in gegevenswoordenboek](../components/data-dictionary/view-data-dictionary.md)
      + [Onderdeelitems bewerken in het gegevenswoordenboek](../components/data-dictionary/edit-entries-data-dictionary.md)
      + [Gezondheid gegevenswoordenboek controleren](../components/data-dictionary/monitor-data-dictionary-health.md)
   + Real-time rapportage {#real-time-reporting}
      + [Overzicht](/help/components/real-time/real-time.md)
      + [Real-time rapportage gebruiken](/help/components/real-time/use-real-time.md)
   + [Geplande projecten](../components/scheduled-projects-manager.md)
+ Report Builder {#cja-reportbuilder}
   + [Overzicht](../report-builder/rb-overview.md)
   + [Report Builder instellen](../report-builder/report-builder-setup.md)
   + [Een gegevensblok maken](../report-builder/create-a-data-block.md)
   + [Report Builder hub](../report-builder/report-builder-hub.md)
   + [Een gegevensweergave selecteren](../report-builder/select-data-view.md)
   + [Een datumbereik selecteren](../report-builder/select-date-range.md)
   + [Werken met segmenten](../report-builder/work-with-filters.md)
   + [Filterafmetingen](../report-builder/filter-dimensions.md)
   + [Gegevensblokken beheren](../report-builder/manage-reportbuilder.md)
   + [Werkboeken plannen voor e-mail](../report-builder/schedule-reportbuilder.md)
   + [Workbooks plannen voor het exporteren van cloud](../report-builder/report-builder-export.md)
   + [Workflowschema&#39;s beheren](/help/report-builder/manage-schedules-reportbuilder.md)
   + [Beperkte labels](../report-builder/restricted-labels.md)
   + [Report Builder-instellingen](../report-builder/report-builder-settings.md)


+ Activity Manager rapporteren {#reporting-activity-manager}
   + [Overzicht](../reporting-activity-manager/reporting-activity-overview.md)
   + [Rapportactiviteiten weergeven](../reporting-activity-manager/reporting-activity.md)
   + [Rapportageverzoeken annuleren](../reporting-activity-manager/reporting-activity-cancel-requests.md)

+ Stiksel {#stitching}
   + [Overzicht](/help/stitching/overview.md)
   + [Veldgebaseerde stitatie](/help/stitching/fbs.md)
   + [Op grafiek gebaseerde stitching](/help/stitching/gbs.md)
   + [Sstitching gebruiken](/help/stitching/use-stitching.md)
   + [Sstitching gebruiken](/help/stitching/use-stitching-ui.md)
   + [Verstikte gegevenssets maken en beheren](/help/stitching/stitching-ui.md)
   + [Stikken valideren](/help/stitching/validate.md)
   + [Veelgestelde vragen](/help/stitching/faq.md)

+ Adobe-integratie {#integrations}
   + [Overzicht](/help/integrations/overview.md)
   + [Adobe Analytics integreren](/help/integrations/aa.md)
   + [Doel integreren](/help/integrations/at.md)
   + [Journey Optimizer-gegevens integreren](/help/integrations/ajo.md)
   + [Beslissingsbeheergegevens integreren](/help/integrations/ajo-od.md)
   + [AI van klant integreren](/help/integrations/customer-ai.md)
   + [Adobe Advertising integreren](/help/integrations/advertising.md)

+ Datagovernance {#cja-privacy}
   + [Datagovernance](../privacy/privacy-overview.md)
   + [Controlelogboek](../privacy/audit-log.md)
   + [Door de klant beheerde toetsen](../privacy/cmk.md)

+ Gebruik hoofdletters {#cja-usecases}
   + [Customer Journey Analytics-gebruikskwesties](../use-cases/cja-usecases.md)
   + Adobe Analytics-gegevens {#aa-data}
      + [Afmetingen marketingkanaal gebruiken](../use-cases/aa-data/marketing-channels.md)
      + [Rapportsuites combineren met verschillende schema&#39;s](../use-cases/aa-data/combine-report-suites.md)
   + B2B {#b2b}
      + [Een voorbeeld van een op persoon gebaseerd B2B-project](../use-cases/b2b/example.md)
      + B2B edition {#b2b-edition}
         + [Overzicht van gevallen gebruiken](/help/use-cases/b2b/b2b-edition/use-cases-overview.md)
         + [Instellen](/help/use-cases/b2b/b2b-edition/setup.md)
         + [Accountmarketing optimaliseren](/help/use-cases/b2b/b2b-edition/optimize-account-marketing.md)
         + [Sleutelaccounts vergroten](/help/use-cases/b2b/b2b-edition/grow-key-accounts.md)
         + [Productwaarde opbouwen](/help/use-cases/b2b/b2b-edition/build-product-value.md)
   + Complexe gegevens {#complex-data}
      + [Arrays van objecten gebruiken](../use-cases/object-arrays.md)
   + Kanaalgegevens {#cross-channel}
      + [Gegevens via kanalen analyseren](../use-cases/cross-channel/cross-channel.md)
      + [Telefooncentrum en webgegevens importeren](../use-cases/cross-channel/call-center.md)
   + Gegevens exporteren {#data-export}
      + [Overzicht](../use-cases/data-export/overview.md)
      + [BI-extensie](../use-cases/data-export/bi-extension.md)
      + [Gegevensbestanden exporteren](../use-cases/data-export/export-datasets.md)
      + [Volledige tabel exporteren](../use-cases/data-export/export-full-table.md)
      + [De Dienst van de vraag en de datasets van de Uitvoer](../use-cases/data-export/queryservice-export-datasets.md)
   + Gegevensinvoer {#data-ingestion}
      + [Marketo Engage-gegevens invoegen en gebruiken](../use-cases/data-ingestion/marketo.md)
      + [Experience Platform-publiek voorstellen en gebruiken](../use-cases/data-ingestion/ingest-aep-segments.md)
   + Gegevensweergaven {#data-views}
      + [Gebruiksscenario&#39;s voor gegevensweergaven](/help/use-cases/data-views/data-views-usecases.md)
      + [Afmetingen en metriek van binding gebruiken](/help/use-cases/data-views/binding-dimensions-metrics.md)
      + [Samenvattingsgegevens gebruiken](/help/use-cases/data-views/summary-data.md)
      + [Gebruikskwesties voor extensie BI](/help/use-cases/data-views/bi-extension-usecases.md)
   + Afgeleide velden {#derived-fields}
      + [Verslag over het door LLM en AI gegenereerde verkeer](/help/use-cases/ai-traffic.md)
      + [Verslag over doelstellingen](../use-cases/goals-using-derived-fields.md)
   + Productanalyse {#product-analysis}
      + [Productanalyse](/help/use-cases/product-analysis.md)
   + Stiksel {#stitching}
      + [Gedeelde apparaten](/help/use-cases/stitching/shared-devices.md)
   + Gegevens van derden {#third-party}
      + [Overzicht](/help/use-cases/third-party/overview.md)
      + Google Analytics {#ga}
         + [Gegevens migreren uit Google Analytics](/help/use-cases/third-party/ga/overview.md)
         + [Historische gegevens van Google Analytics weergeven](/help/use-cases/third-party/ga/backfill.md)
         + [Streaming Google Analytics-gegevens configureren](/help/use-cases/third-party/ga/streaming.md)
         + [Rapport over Google Analytics-gegevens](/help/use-cases/third-party/ga/report.md)
      + Quantum Metric {#qm}
         + [Overzicht](/help/use-cases/third-party/quantum-metric/qm-overview.md)
         + [Herhaalde sessies beëindigen](/help/use-cases/third-party/quantum-metric/tie-session-replays.md)
         + [Hatmaps gebruiken](/help/use-cases/third-party/quantum-metric/heatmap.md)
         + [Wrijvingsgebeurtenissen toevoegen](/help/use-cases/third-party/quantum-metric/friction-events.md)
         + [Source-connector](/help/use-cases/third-party/quantum-metric/source-connector.md)

+ Labs {#labs}
   + [Gebruikershandleiding voor labels](../labs/labs.md)

+ Problemen oplossen {#troubleshooting}
   + [Gegevens Source Connector vergelijken](../troubleshooting/compare.md)
   + [Consistentie van metriek en publiek](../troubleshooting/consistency-rcdp-cja.md)
   + [Gebrek aan machtigingen](../troubleshooting/lack-of-permissions.md)

+ Technische notities {#technotes}
   + [Toegangsbeheer](../technotes/access-control.md)
   + [Gegevenscentra](../technotes/data-centers.md)
   + [Gevolgen van verwijdering](../technotes/deletion.md)
   + [Domeinen](../technotes/domains.md)
   + [Woordenlijst](../technotes/glossary.md)
   + [Guardrails](../technotes/guardrails.md)
   + [IP-adressen](../technotes/ip-addresses.md)
   + [Prestaties optimaliseren](../technotes/optimizing-performance.md)
   + [Gebruik beheren](../technotes/estimate-usage.md)

+ [&#x200B; Customer Journey Analytics API &#x200B;](https://developer.adobe.com/cja-apis/docs/)
