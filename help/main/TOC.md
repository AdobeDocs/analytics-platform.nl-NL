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
source-git-commit: ee463e2d2394505621c92ef827eb5788dc543304
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 12%

---

# Adobe Customer Journey Analytics Guide {#using}

+ [Adobe Customer Journey Analytics Guide](../getting-started/cja-landing.md)

+ [AI Assistant voor Adobe Customer Journey Analytics](../ai-assistant.md)

+ Opmerkingen bij de release {#releases}
   + [Meest recente release](../release-notes/latest.md)
   + [2024 releases](../release-notes/2024.md)
   + [2023 releases](../release-notes/2023.md)
   + [2022 introducties](../release-notes/2022.md)
   + [Release 2021](../release-notes/2021.md)
   + [2020 introducties](../release-notes/2020.md)
   + [Strategie voor release van functies](../release-notes/releases.md)
   + [Documentatie-updates](../release-notes/doc-changes.md)

+ Aan de slag {#cja-overview}
   + [Overzicht van Customer Journey Analytics](../getting-started/cja-overview.md)
   + [Handleiding voor snel starten](../getting-started/cja-getting-started.md)
   + [Openingspagina](../getting-started/landing.md)
   + [Openingspagina (oud)](../getting-started/cja-landing-old.md)
   + [Veelgestelde vragen](../getting-started/cja-faq.md)
   + [Vergelijk Customer Journey Analytics met de oplossingen van BI](../getting-started/cja-vs-bi.md)

+ Customer Journey Analytics en Adobe Analytics {#compare-aa-cja}
   + Upgrade naar Customer Journey Analytics {#upgrade-to-cja}
      + [Aan de slag](/help/getting-started/cja-upgrade/cja-upgrade-getstarted.md)
      + [Upgradepad kiezen](/help/getting-started/cja-upgrade/cja-upgrade-path.md)
      + [Gegevens verzenden naar platform](/help/getting-started/cja-upgrade/cja-upgrade-send-to-platform.md)
      + [Historische gegevens behouden](/help/getting-started/cja-upgrade/cja-upgrade-historical-data.md)
   + Vergelijking met Adobe Analytics {#cja-aa-comparison}
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

+ Gegevensinname {#cja-data-ingestion}
   + [Overzicht van gegevensinvoer](../data-ingestion/data-ingestion.md)
   + Hulplijnen voor snel starten samenstellen en gebruiken {#ingest-use-guides}
      + [Adobe Analytics](../data-ingestion/analytics.md)
      + Edge Network Experience Platform {#edge-network}
         + [Web SDK](../data-ingestion/aepwebsdk.md)
         + [Mobile SDK](../data-ingestion/aepmobilesdk.md)
         + [Server-API](../data-ingestion/serverapi.md)
      + [Batchgegevens](../data-ingestion/batch.md)
      + [Streaming gegevens](../data-ingestion/streaming.md)
      + [Source-connectors](../data-ingestion/sources.md)

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

+ Gereedschappen {#tools}
   + Asset Transfer {#asset-transfer}
      + [ activa van de Overdracht ](../tools/asset-transfer/transfer-assets.md)
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
      + [Projecten maken](/help/analysis-workspace/build-workspace-project/create-projects.md)
      + [Projecten openen](/help/analysis-workspace/build-workspace-project/open-projects.md)
      + [Projecten opslaan](../analysis-workspace/build-workspace-project/save-projects.md)
      + Mappen in Workspace {#workspace-folders}
         + [Mappen](../analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)
         + [Mappen en submappen maken](../analysis-workspace/build-workspace-project/workspace-folders/create-folders.md)
         + [Mappen beheren](../analysis-workspace/build-workspace-project/workspace-folders/manage-folders.md)
         + [Projecten toevoegen aan of verplaatsen naar mappen](../analysis-workspace/build-workspace-project/workspace-folders/add-projects.md)
      + [Hotkeys (sneltoetsen)](../analysis-workspace/build-workspace-project/fa-shortcut-keys.md)
      + [Kleurenpaletten](../analysis-workspace/build-workspace-project/color-palettes.md)
      + [Weergavedichtheid](../analysis-workspace/build-workspace-project/view-density.md)
   + Visualisaties {#visualizations}
      + [Overzicht](../analysis-workspace/visualizations/freeform-analysis-visualizations.md)
      + [Gegevensbronnen beheren](../analysis-workspace/visualizations/t-sync-visualization.md)
      + [Intelligente bijschriften](../analysis-workspace/visualizations/intelligent-captions.md)
      + Vrije-vormentabel {#freeform-table}
         + [Overzicht](../analysis-workspace/visualizations/freeform-table/freeform-table.md)
         + [Hyperlinks maken](/help/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md)
         + Instellingen voor kolommen en rijen {#column-row-settings}
            + [Kolominstellingen](../analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)
            + [Rijinstellingen](../analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)
            + [Dynamische en statische items](../analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md)
         + [Tabellen filteren en sorteren](../analysis-workspace/visualizations/freeform-table/filter-and-sort.md)
         + [Totaal Workspace](../analysis-workspace/visualizations/freeform-table/workspace-totals.md)
      + Cohorttabel {#cohort-table}
         + [Overzicht](../analysis-workspace/visualizations/cohort-table/cohort-analysis.md)
         + [Configureren](../analysis-workspace/visualizations/cohort-table/t-cohort.md)
         + [Gebruik hoofdletters](../analysis-workspace/visualizations/cohort-table/cohort-use-cases.md)
      + Uitval {#fallout}
         + [Overzicht](../analysis-workspace/visualizations/fallout/fallout-flow.md)
         + [Configureren](../analysis-workspace/visualizations/fallout/configuring-fallout.md)
         + [Interdimensionale uitval](../analysis-workspace/visualizations/fallout/configuring-interdimensional-fallout.md)
         + [Filters toepassen](../analysis-workspace/visualizations/fallout/compare-segments-fallout.md)
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
      + [Spreiding](../analysis-workspace/visualizations/scatterplot.md)
      + [Samenvattingsnummer en wijziging](../analysis-workspace/visualizations/summary-number-change.md)
      + [Sectiekop](/help/analysis-workspace/visualizations/section-header.md)
      + [Tekst](../analysis-workspace/visualizations/text.md)
      + [Boomstructuur](../analysis-workspace/visualizations/treemap.md)
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
   + Projecten cureren, delen en plannen {#curate-share}
      + [Overzicht](../analysis-workspace/curate-share/send-schedule-files.md)
      + [Cursieve projecten](../analysis-workspace/curate-share/curate.md)
      + [Projecten delen](../analysis-workspace/curate-share/share-projects.md)
      + [Deelbare koppelingen maken](../analysis-workspace/curate-share/shareable-links.md)
      + [Alleen-weergeven projecten](../analysis-workspace/curate-share/view-only-projects.md)
   + Exporteren {#export}
      + [Overzicht](../analysis-workspace/export/export-project-overview.md)
      + [Downloaden](../analysis-workspace/export/download-send.md)
      + [Verzenden naar anderen](../analysis-workspace/export/t-schedule-report.md)
      + [Naar de cloud exporteren](../analysis-workspace/export/export-cloud.md)
   + Anomaliedetectie {#anomaly-detection}
      + [Overzicht](../analysis-workspace/c-anomaly-detection/anomaly-detection.md)
      + [anomalieën weergeven](../analysis-workspace/c-anomaly-detection/view-anomalies.md)
      + [Statistische technieken](../analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)
   + Voorspelling {#forecasting}
      + [Overzicht](../analysis-workspace/c-forecast/forecasting.md)
      + [Prognoses weergeven](../analysis-workspace/c-forecast/view-forecasts.md)
      + [Statistische technieken](../analysis-workspace/c-forecast/statistics-forecasting.md)
   + [Inhoudsopgave](../analysis-workspace/build-workspace-project/project-table-of-contents.md)
   + [Gebruikersvoorkeuren](../analysis-workspace/user-preferences.md)
   + Workspace - Veelgestelde vragen en meer {#workspace-faq}
      + [Veelgestelde vragen](../analysis-workspace/workspace-faq/faq.md)
      + [Foutberichten](../analysis-workspace/workspace-faq/error-messages.md)
      + [Beperkingen](../analysis-workspace/workspace-faq/aw-limitations.md)
      + [Administratieve vereisten](../analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md)
      + [Toegankelijkheid](../analysis-workspace/workspace-faq/aw-accessibility.md)

+ Analytische dashboards {#cja-dashboards}
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
   + [Componenten in Analysis Workspace gebruiken](../components/use-components-in-workspace.md)
   + [Componentbeschrijvingen toevoegen](../components/add-component-descriptions.md)
   + Annotaties {#annotations}
      + [Overzicht van annotaties](../components/annotations/overview.md)
      + [Annotaties maken](../components/annotations/create-annotations.md)
      + [Annotaties beheren](../components/annotations/manage-annotations.md)
      + [Annotaties weergeven](../components/annotations/view-annotations.md)
      + [Mobiele annotaties](../components/annotations/mobile-annotations.md)
   + [Geplande projecten](../components/scheduled-projects-manager.md)
   + Soorten publiek {#audiences}
      + [Overzicht publiek](../components/audiences/audiences-overview.md)
      + [Soorten publiek maken en publiceren](../components/audiences/publish.md)
      + [Soorten publiek beheren](../components/audiences/manage.md)
   + Dimensies {#dimensions}
      + [Overzicht van Dimensionen](../components/dimensions/overview.md)
      + [Voorvertoningsafmetingen](../components/dimensions/view-dimensions.md)
      + [Afmetingen onderverdelingen](../components/dimensions/t-breakdown-fa.md)
      + [Afmetingen van tijd tot tijd](../components/dimensions/time-parting-dimensions.md)
      + [Afmetingen van hoge kardinaliteit](../components/dimensions/high-cardinality.md)
   + [Metrics](../components/apply-create-metrics.md)
   + Filters {#cja-filters}
      + [Overzicht](../components/filters/filters-overview.md)
      + [Filters maken](../components/filters/create-filters.md)
      + [Filters maken](../components/filters/filter-builder.md)
      + [Snelle filters](../components/filters/quick-filters.md)
      + [Opeenvolgende filters](../components/filters/seg-sequential-build.md)
      + [Filters delen](../components/filters/filters-share.md)
      + [Labelfilters](../components/filters/filters-tag.md)
      + [De lijst met filters filteren](../components/filters/filters-filter.md)
      + [Filters markeren als favorieten](../components/filters/filters-favorite.md)
      + [Filters goedkeuren](../components/filters/filters-approve.md)
      + [Filters kopiëren](../components/filters/filters-copy.md)
      + [Filters beheren](../components/filters/manage-filters.md)
      + [Operatoren](../components/filters/operators.md)
   + Berekende cijfers {#cja-calcmetrics}
      + [Overzicht](../components/calc-metrics/calc-metr-overview.md)
      + Workflow voor berekende metriek {#cm-workflow}
         + [Berekende waarden maken](../components/calc-metrics/cm-workflow/cm-workflow.md)
         + [Berekende maatstaven samenstellen](../components/calc-metrics/cm-workflow/cm-build-metrics.md)
         + [Metrische gegevens zoeken](../components/calc-metrics/cm-workflow/cm-finding.md)
         + [Type en attributie metrisch](../components/calc-metrics/cm-workflow/m-metric-type-alloc.md)
         + [Een metrische deelname maken](../components/calc-metrics/cm-workflow/participation-metric.md)
         + [Gefilterde metriek](../components/calc-metrics/cm-workflow/metrics-with-segments.md)
         + [Filters stapelen en vervangen](../components/calc-metrics/cm-workflow/cm-stack-seg.md)
         + [Berekende maateenheden filteren](../components/calc-metrics/cm-workflow/cm-filter.md)
         + [Berekende metriek markeren als favorieten](../components/calc-metrics/cm-workflow/cm-favorite.md)
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
   + Exporteren {#exports}
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

+ Report Builder {#cja-reportbuilder}
   + [Overzicht](../report-builder/report-buider-overview.md)
   + [Report Builder instellen](../report-builder/report-builder-setup.md)
   + [Een gegevensblok maken](../report-builder/create-a-data-block.md)
   + [Report Builder Hub](../report-builder/report-builder-hub.md)
   + [Een gegevensweergave selecteren](../report-builder/select-data-view.md)
   + [Een datumbereik selecteren](../report-builder/select-date-range.md)
   + [Werken met filters](../report-builder/work-with-filters.md)
   + [Dimensionen filteren](../report-builder/filter-dimensions.md)
   + [Gegevensblokken beheren](../report-builder/manage-reportbuilder.md)
   + [Workbooks plannen](../report-builder/schedule-reportbuilder.md)
   + [Beperkte labels](../report-builder/restricted-labels.md)
   + [Report Builder-instellingen](../report-builder/report-builder-settings.md)

+ Activity Manager rapporteren {#reporting-activity-manager}
   + [Overzicht](../reporting-activity-manager/reporting-activity-overview.md)
   + [Rapportactiviteiten weergeven](../reporting-activity-manager/reporting-activity.md)
   + [Rapportageverzoeken annuleren](../reporting-activity-manager/reporting-activity-cancel-requests.md)

+ Stikken {#stitching}
   + [Overzicht](../stitching/overview.md)
   + [Verstikte gegevenssets maken en beheren](../stitching/stitching-ui.md)
   + [Veelgestelde vragen](../stitching/faq.md)

+ Integraties van Adoben {#integrations}
   + [Overzicht](/help/integrations/overview.md)
   + [Adobe Analytics integreren](/help/integrations/aa.md)
   + [Doel integreren](/help/integrations/at.md)
   + [Journey Optimizer-gegevens integreren](/help/integrations/ajo.md)
   + [Beslissingsbeheergegevens integreren](/help/integrations/ajo-od.md)
   + [AI van klant integreren](/help/integrations/customer-ai.md)

+ Data Governance {#cja-privacy}
   + [Datagovernance](../privacy/privacy-overview.md)
   + [Controlelogboek](../privacy/audit-log.md)
   + [Door de klant beheerde toetsen](../privacy/cmk.md)

+ Gebruik hoofdletters en kleine letters {#cja-usecases}
   + [Gebruiksgevallen Customer Journey Analytics](../use-cases/cja-usecases.md)
   + Gegevens van Googles Analytics {#ga}
      + [Gegevens migreren uit Googles Analytics](../use-cases/ga/overview.md)
      + [Historische gegevens van Googles Analytics samenvoegen](../use-cases/ga/backfill.md)
      + [Gegevens voor streaming Googles Analytics configureren](../use-cases/ga/streaming.md)
      + [Rapport over gegevens over Googles Analytics](../use-cases/ga/report.md)
   + Gegevensinvoer {#data-ingestion}
      + [Gegevens van Marketo&#39;s Engage opnemen en gebruiken](../use-cases/data-ingestion/marketo.md)
      + [Experience Platforms publiek opnemen en gebruiken](../use-cases/data-ingestion/ingest-aep-segments.md)
   + Gegevensweergaven {#data-views}
      + [Gebruiksscenario&#39;s voor gegevensweergaven](../use-cases/data-views/data-views-usecases.md)
      + [Afmetingen en metriek van binding gebruiken](../use-cases/data-views/binding-dimensions-metrics.md)
      + [Samenvattingsgegevens gebruiken](../use-cases/data-views/summary-data.md)
   + Gegevens exporteren {#data-export}
      + [Overzicht](../use-cases/data-export/overview.md)
      + [BI-extensie](../use-cases/data-export/bi-extension.md)
      + [Gegevensbestanden exporteren](../use-cases/data-export/export-datasets.md)
      + [Volledige tabel exporteren](../use-cases/data-export/export-full-table.md)
      + [De Dienst van de vraag en de datasets van de Uitvoer](../use-cases/data-export/queryservice-export-datasets.md)
   + B2B {#b2b}
      + [Een B2B-voorbeeldproject](../use-cases/b2b/example.md)
   + Kanaalgegevens {#cross-channel}
      + [Gegevens via kanalen analyseren](../use-cases/cross-channel/cross-channel.md)
      + [Telefooncentrum en webgegevens importeren](../use-cases/cross-channel/call-center.md)
   + Adobe Analytics-gegevens {#aa-data}
      + [Afmetingen marketingkanaal gebruiken](../use-cases/aa-data/marketing-channels.md)
      + [Rapportsuites combineren met verschillende schema&#39;s](../use-cases/aa-data/combine-report-suites.md)
   + Complexe gegevens {#complex-data}
      + [Arrays van objecten gebruiken](../use-cases/object-arrays.md)
   + Stikken {#stitching}
      + [Gedeelde apparaten](/help/use-cases/stitching/shared-devices.md)
   + Afgeleide velden {#derived-fields}
      + [Verslag over doelstellingen](../use-cases/goals-using-derived-fields.md)

+ Labs {#labs}
   + [Gebruikershandleiding voor labels](../labs/labs.md)

+ Problemen oplossen {#troubleshooting}
   + [Gegevens vergelijken](../troubleshooting/compare.md)
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
   + [Gebruik weergeven en beheren](../technotes/estimate-usage.md)

+ [ Customer Journey Analytics API ](https://developer.adobe.com/cja-apis/docs/)
