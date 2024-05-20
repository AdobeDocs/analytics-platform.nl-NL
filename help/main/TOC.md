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
source-git-commit: e8057ea64c8a5393790700da2fee6144161cb58a
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 8%

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
      + [Adobe Analytics-gegevens in Customer Journey Analytics gebruiken](../getting-started/aa-vs-cja/aa-data-in-cja.md)
      + [Ondersteuning van Customer Journey Analytics-functies](../getting-started/aa-vs-cja/cja-aa.md)
      + [Vergelijk terminologie voor de gegevens van de Analyse die door de bron van de Analyse schakelaar worden overgegaan](../getting-started/aa-vs-cja/terminology.md)
      + [Gegevensverwerking in Adobe Analytics en Customer Journey Analytics vergelijken](../getting-started/aa-vs-cja/data-processing-comparisons.md)
      + [Virtuele rapportageomgevingen en sandboxomgevingen](../getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md)
      + [Verwerkingsregels, VISTA en classificaties versus Data Prep](../getting-started/aa-vs-cja/pr-vista-dataprep.md)
      + [STEUN, ECID, AACUSTOMID en de bronaansluiting voor Analytics](../getting-started/aa-vs-cja/aaid-ecid-adc.md)
   + [Evolutie uit Adobe Analytics](../getting-started/aa-to-cja.md)
   + [Gebruikershandleiding voor Adobe Analytics-gebruikers](../getting-started/aa-to-cja-user.md)

+ Gegevensinname {#cja-data-ingestion}
   + [Overzicht van gegevensinscriptie](../data-ingestion/data-ingestion.md)
   + Hulplijnen voor snel starten samenstellen en gebruiken{#ingest-use-guides}
      + [Adobe Analytics](../data-ingestion/analytics.md)
      + Adobe Experience Platform Edge Network {#edge-network}
         + [Web SDK](../data-ingestion/aepwebsdk.md)
         + [Mobiele SDK](../data-ingestion/aepmobilesdk.md)
         + [Server-API](../data-ingestion/serverapi.md)
      + [Batchgegevens](../data-ingestion/batch.md)
      + [Streaming gegevens](../data-ingestion/streaming.md)
      + [Bronaansluitingen](../data-ingestion/sources.md)

+ Verbindingen {#cja-connections}
   + [Overzicht van verbindingen](../connections/overview.md)
   + [Verbinding maken of bewerken](../connections/create-connection.md)
   + [Verbindingen beheren](../connections/manage-connections.md)
   + [Gecombineerde gegevenssets voor gebeurtenissen](../connections/combined-dataset.md)
   + [Standaardzoekopdrachten](../connections/standard-lookups.md)

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
      + [Waardebeperking](../data-views/component-settings/value-bucketing.md)
   + [Standaardcomponentverwijzing](../data-views/component-reference.md)
   + [BI-extensie](../data-views/bi-extension.md)
   + [Afgeleide velden](../data-views/derived-fields/derived-fields.md)
   + [Labels en beleid](../data-views/data-governance.md)

+ Werkruimteprojecten {#cja-workspace}
   + [Overzicht van Analysis Workspace](../analysis-workspace/home.md)
   + [Basisanalyse uitvoeren](../analysis-workspace/perform-basic-analysis.md)
   + [Geavanceerde analyse uitvoeren](../analysis-workspace/perform-adv-analysis.md)
   + Projecten {#build-workspace-project}
      + [Overzicht van projecten](../analysis-workspace/build-workspace-project/freeform-overview.md)
      + [Projecten maken](/help/analysis-workspace/build-workspace-project/create-projects.md)
      + [Projecten opslaan](../analysis-workspace/build-workspace-project/save-projects.md)
      + Mappen in werkruimte {#workspace-folders}
         + [Mappen in werkruimte](../analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)
         + [Mappen en submappen maken](../analysis-workspace/build-workspace-project/workspace-folders/create-folders.md)
         + [Mappen verwijderen](../analysis-workspace/build-workspace-project/workspace-folders/delete-folders.md)
         + [Projecten toevoegen](../analysis-workspace/build-workspace-project/workspace-folders/add-projects.md)
         + [Een project verwijderen](../analysis-workspace/build-workspace-project/workspace-folders/remove-projects.md)
         + [Een nieuw project opslaan](../analysis-workspace/build-workspace-project/workspace-folders/save-new-project-folder.md)
      + [Hotkeys (sneltoetsen)](../analysis-workspace/build-workspace-project/fa-shortcut-keys.md)
      + [Kleurenpaletten](../analysis-workspace/build-workspace-project/color-palettes.md)
      + [Dichtheid weergeven](../analysis-workspace/build-workspace-project/view-density.md)
   + Visualisaties {#visualizations}
      + [Overzicht van visualisaties](../analysis-workspace/visualizations/freeform-analysis-visualizations.md)
      + [Gegevensbronnen beheren](../analysis-workspace/visualizations/t-sync-visualization.md)
      + Vrije-vormtabel {#freeform-table}
         + [Vrije-vormtabel](../analysis-workspace/visualizations/freeform-table/freeform-table.md)
         + Instellingen voor kolommen en rijen {#column-row-settings}
            + [Kolominstellingen](../analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)
            + [Rijinstellingen](../analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)
            + [Dynamische versus statische items](../analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md)
         + [Tabellen filteren en sorteren](../analysis-workspace/visualizations/freeform-table/filter-and-sort.md)
         + [Totalen werkruimte](../analysis-workspace/visualizations/freeform-table/workspace-totals.md)
      + Cohorttabel {#cohort-table}
         + [Wat is cohortanalyse?](../analysis-workspace/visualizations/cohort-table/cohort-analysis.md)
         + [Een rapport voor cohortanalyse configureren](../analysis-workspace/visualizations/cohort-table/t-cohort.md)
         + [Gebruiksgevallen van cohortanalyse](../analysis-workspace/visualizations/cohort-table/cohort-use-cases.md)
      + Uitval {#fallout}
         + [Overzicht van uitval](../analysis-workspace/visualizations/fallout/fallout-flow.md)
         + [Een fallout-visualisatie configureren](../analysis-workspace/visualizations/fallout/configuring-fallout.md)
         + [Interdimensionale uitval](../analysis-workspace/visualizations/fallout/configuring-interdimensional-fallout.md)
         + [Filters toepassen in falloutanalyse](../analysis-workspace/visualizations/fallout/compare-segments-fallout.md)
      + Stroom {#flow}
         + [Overzicht van stroom](../analysis-workspace/visualizations/c-flow/flow.md)
         + [Een stroomvisualisatie configureren](../analysis-workspace/visualizations/c-flow/create-flow.md)
         + [Interdimensionale stromen](../analysis-workspace/visualizations/c-flow/multi-dimensional-flow.md)
      + [Gebied en gebied gestapeld](../analysis-workspace/visualizations/area.md)
      + [Stapel en balk gestapeld](../analysis-workspace/visualizations/bar.md)
      + [Bullet](../analysis-workspace/visualizations/bullet-graph.md)
      + [Combodiagram](../analysis-workspace/visualizations/combo-charts.md)
      + [Donut](../analysis-workspace/visualizations/donut.md)
      + [Histogram](../analysis-workspace/visualizations/histogram.md)
      + [Horizontale balk en horizontale balk gestapeld](../analysis-workspace/visualizations/horizontal-bar.md)
      + [Intelligente bijschriften](../analysis-workspace/visualizations/intelligent-captions.md)
      + [Samenvatting van metrische sleutel](../analysis-workspace/visualizations/key-metric.md)
      + [Lijn](../analysis-workspace/visualizations/line.md)
      + [Scatterplot](../analysis-workspace/visualizations/scatterplot.md)
      + [Samenvattingsnummer en Samenvattingswijziging](../analysis-workspace/visualizations/summary-number-change.md)
      + [Tekst](../analysis-workspace/visualizations/text.md)
      + [Boomstructuur](../analysis-workspace/visualizations/treemap.md)
      + [Venn](../analysis-workspace/visualizations/venn.md)
   + Deelvensters {#panels}
      + [Overzicht van deelvensters](../analysis-workspace/c-panels/panels.md)
      + [Kenmerk, deelvenster](../analysis-workspace/c-panels/attribution.md)
      + [Leeg deelvenster](../analysis-workspace/c-panels/blank-panel.md)
      + [Deelvenster Experimentatie](../analysis-workspace/c-panels/experimentation.md)
      + [Deelvenster Vrije vorm](../analysis-workspace/c-panels/freeform-panel.md)
      + [Deelvenster Gemiddelde media - geluid](/help/analysis-workspace/c-panels/average-minute-audience-panel.md)
      + [Deelvenster Snelle inzichten](../analysis-workspace/c-panels/quickinsight.md)
      + [Deelvenster Mediagelijktijdige viewers](../analysis-workspace/c-panels/media-concurrent-viewers.md)
      + [Media afspelen tijd besteed, deelvenster](../analysis-workspace/c-panels/media-playback-time-spent.md)
   + Projecten cureren, delen en plannen {#curate-share}
      + [Menu Delen](../analysis-workspace/curate-share/send-schedule-files.md)
      + [Cursieve projecten](../analysis-workspace/curate-share/curate.md)
      + [Projecten delen](../analysis-workspace/curate-share/share-projects.md)
      + [Deelbare koppelingen maken](../analysis-workspace/curate-share/shareable-links.md)
      + [Alleen-weergeven projecten](../analysis-workspace/curate-share/view-only-projects.md)
   + Exporteren {#export}
      + [Overzicht van exporteren](../analysis-workspace/export/export-project-overview.md)
      + [Downloaden](../analysis-workspace/export/download-send.md)
      + [Verzenden naar anderen](../analysis-workspace/export/t-schedule-report.md)
      + [Naar de cloud exporteren](../analysis-workspace/export/export-cloud.md)
   + Anomaliedetectie {#anomaly-detection}
      + [Overzicht van anomalische detectie](../analysis-workspace/c-anomaly-detection/anomaly-detection.md)
      + [anomalieën weergeven in Analysis Workspace](../analysis-workspace/c-anomaly-detection/view-anomalies.md)
      + [Statistische technieken voor de opsporing van anomalieën](../analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)
   + Voorspelling {#forecasting}
      + [Overzicht van de prognoses](../analysis-workspace/c-forecast/forecasting.md)
      + [Prognoses weergeven in Analysis Workspace](../analysis-workspace/c-forecast/view-forecasts.md)
      + [Statistische technieken voor de prognose](../analysis-workspace/c-forecast/statistics-forecasting.md)
   + [Gebruikersvoorkeuren](../analysis-workspace/user-preferences.md)
   + Veelgestelde vragen over Workspace {#workspace-faq}
      + [Veelgestelde vragen](../analysis-workspace/workspace-faq/faq.md)
      + [Foutberichten](../analysis-workspace/workspace-faq/error-messages.md)
      + [Analysis Workspace-beperkingen](../analysis-workspace/workspace-faq/aw-limitations.md)
      + [Administratieve vereisten](../analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md)
      + [Toegankelijkheid in Analysis Workspace](../analysis-workspace/workspace-faq/aw-accessibility.md)

+ Analysedashboards {#cja-dashboards}
   + [Analysedashboards - Overzicht](../mobile-app/home.md)
   + [Curatortaken](../mobile-app/curator.md)
   + [Een mobiele scorecard maken](../mobile-app/create-scorecard.md)
   + [Mobiele scorecards beheren](../mobile-app/manage-scorecard.md)
   + [Stel managers in voor het gebruik van dashboards](../mobile-app/set-up-execs.md)
   + [Snelle handleiding voor gebruikers](../mobile-app/executive.md)

+ Analyse met instructies {#guided-analysis}
   + [Overzicht](../guided-analysis/overview.md)
   + Eigenschappenmatrix {#feature-matrix}
      + [Betrokkenheid](../guided-analysis/types/engagement.md)
   + Trechter {#funnel}
      + [Wrijvingsweergave](../guided-analysis/types/friction.md)
      + [Conversietrends, weergave](../guided-analysis/types/conversion-trends.md)
   + Gevolgen {#impact}
      + [Weergave opheffen](../guided-analysis/types/release.md)
      + [Weergave voor eerste gebruik](../guided-analysis/types/first-use.md)
   + Bewaren {#retention}
      + [Bewaarpercentages](../guided-analysis/types/retention-rates.md)
   + Trends {#trends}
      + [Gebruiksweergave](../guided-analysis/types/usage.md)
      + [Frequentieweergave](../guided-analysis/types/frequency.md)
   + Groei van gebruikers {#user-growth}
      + [Actieve weergave](../guided-analysis/types/active.md)
      + [Netto-groeiweergave](../guided-analysis/types/net-growth.md)
   + Gebruikersstroom {#streams}
      + [Tijdlijn](../guided-analysis/types/timeline.md)
   + [Industriële gebruiksgevallen](../guided-analysis/industry-use-cases.md)
   + [Veelgestelde vragen](../guided-analysis/faq.md)

+ Onderdelen {#cja-components}
   + [Overzicht van componenten](../components/overview.md)
   + [Componenten in Analysis Workspace gebruiken](../components/use-components-in-workspace.md)
   + [Componentbeschrijvingen toevoegen](../components/add-component-descriptions.md)
   + Annotaties {#annotations}
      + [Overzicht van annotaties](../components/annotations/overview.md)
      + [Annotaties maken](../components/annotations/create-annotations.md)
      + [Annotaties beheren](../components/annotations/manage-annotations.md)
      + [Annotaties weergeven](../components/annotations/view-annotations.md)
      + [Mobiele annotaties](../components/annotations/mobile-annotations.md)
   + [Gepland project](../components/scheduled-projects-manager.md)
   + Soorten publiek {#audiences}
      + [Overzicht publiek](../components/audiences/audiences-overview.md)
      + [Soorten publiek maken en publiceren](../components/audiences/publish.md)
      + [Soorten publiek beheren](../components/audiences/manage.md)
   + Dimensies {#dimensions}
      + [Overzicht van Dimensionen](../components/dimensions/overview.md)
      + [Voorvertoningsafmetingen](../components/dimensions/view-dimensions.md)
      + [Afmetingen onderverdelingen](../components/dimensions/t-breakdown-fa.md)
      + [Afmetingen van tijd tot tijd](../components/dimensions/time-parting-dimensions.md)
      + [Dimensionen met zeer hoge kardinaliteit](../components/dimensions/high-cardinality.md)
   + [Metrics](../components/apply-create-metrics.md)
   + Filters {#cja-filters}
      + [Overzicht van filters](../components/filters/filters-overview.md)
      + [Filters maken](../components/filters/create-filters.md)
      + [Filters delen](../components/filters/filters-share.md)
      + [Labelfilters](../components/filters/filters-tag.md)
      + [De lijst met filters filteren](../components/filters/filters-filter.md)
      + [Filters markeren als favorieten](../components/filters/filters-favorite.md)
      + [Filters goedkeuren](../components/filters/filters-approve.md)
      + [Filters kopiëren](../components/filters/filters-copy.md)
      + [Snelle filters](../components/filters/quick-filters.md)
      + [Filter builder](../components/filters/filter-builder.md)
      + [Filters beheren](../components/filters/manage-filters.md)
      + [Operatoren](../components/filters/operators.md)
   + Berekende cijfers {#cja-calcmetrics}
      + [Overzicht van berekende metriek](../components/calc-metrics/calc-metr-overview.md)
      + Workflow voor berekende metriek {#cm-workflow}
         + [Workflow voor berekende metriek](../components/calc-metrics/cm-workflow/cm-workflow.md)
         + [Metrische gegevens zoeken](../components/calc-metrics/cm-workflow/cm-finding.md)
         + [Metrische gegevens samenstellen](../components/calc-metrics/cm-workflow/cm-build-metrics.md)
         + [Type en attributie metrisch](../components/calc-metrics/cm-workflow/m-metric-type-alloc.md)
         + [Een metrische deelname maken](../components/calc-metrics/cm-workflow/participation-metric.md)
         + [Gefilterde metriek](../components/calc-metrics/cm-workflow/metrics-with-segments.md)
         + [Filters stapelen en vervangen](../components/calc-metrics/cm-workflow/cm-stack-seg.md)
         + [Gefilterde en gewogen cijfers](../components/calc-metrics/cm-workflow/cm-weighted-metric.md)
         + [Berekende maateenheden filteren](../components/calc-metrics/cm-workflow/cm-filter.md)
         + [Berekende metriek markeren als favorieten](../components/calc-metrics/cm-workflow/cm-favorite.md)
         + [Berekende cijfers kopiëren](../components/calc-metrics/cm-workflow/cm-copy.md)
         + [Functies gebruiken](../components/calc-metrics/cm-workflow/cm-using-functions.md)
         + [Berekende maatstaven voor tags](../components/calc-metrics/cm-workflow/cm-tagging.md)
         + [Berekende waarden goedkeuren](../components/calc-metrics/cm-workflow/cm-approving.md)
         + [Berekende maatstaven delen](../components/calc-metrics/cm-workflow/cm-sharing.md)
         + [Berekende metrische manager](../components/calc-metrics/cm-workflow/cm-manager.md)
      + [Berekende standaardwaarden](../components/calc-metrics/default-calcmetrics.md)
      + [Basisfuncties](../components/calc-metrics/cm-functions.md)
      + [Geavanceerde functies](../components/calc-metrics/cm-adv-functions.md)
   + Kalender- en datumbereiken {#cja-date-ranges}
      + [Overzicht van kalender- en datumbereiken](../components/date-ranges/calendar.md)
      + [Een datumbereik maken](../components/date-ranges/create.md)
      + [Datumbereiken beheren](../components/date-ranges/manage.md)
      + [Aangepaste datumbereiken maken](../components/date-ranges/custom-date-ranges.md)
      + [Datumvergelijking](../components/date-ranges/time-comparison.md)
   + Uitvoer {#exports}
      + [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md)
      + [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md)
      + [Cloud-exportlocaties beheren](/help/components/exports/manage-export-locations.md)
      + [Exporteren beheren](/help/components/exports/manage-exports.md)
      + [Exportlogboeken beheren](/help/components/exports/manage-export-logs.md)
      + [Problemen met exporteren oplossen](/help/components/exports/troubleshoot-exports.md)
   + Gegevenswoordenboek {#data-dictionary}
      + [Overzicht van gegevenswoordenboek](../components/data-dictionary/data-dictionary-overview.md)
      + [Componentinformatie weergeven in gegevenswoordenboek](../components/data-dictionary/view-data-dictionary.md)
      + [Onderdeelitems bewerken in het gegevenswoordenboek](../components/data-dictionary/edit-entries-data-dictionary.md)
      + [Gezondheid gegevenswoordenboek controleren](../components/data-dictionary/monitor-data-dictionary-health.md)

+ Report Builder {#cja-reportbuilder}
   + [Overzicht van Report Builder](../report-builder/report-buider-overview.md)
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

+ Stiksel {#stitching}
   + [Overzicht](../stitching/overview.md)
   + [Hoe stitching werkt](../stitching/explained.md)
   + [Verstikte gegevenssets maken en beheren](../stitching/stitching-ui.md)
   + [Veelgestelde vragen](../stitching/faq.md)

+ Adobe-integratie {#integrations}
   + [Adobe-oplossingen integreren met overzicht van Customer Journey Analytics](/help/integrations/overview.md)
   + [Adobe Analytics integreren met Customer Journey Analytics](/help/integrations/aa.md)
   + [Journey Optimizer-gegevens integreren met Customer Journey Analytics](/help/integrations/ajo.md)
   + [Beslissingsbeheergegevens integreren met Customer Journey Analytics](/help/integrations/ajo-od.md)
   + [AI van klant integreren met Customer Journey Analytics](/help/integrations/customer-ai.md)

+ Data Governance {#cja-privacy}
   + [Gegevensbeheer](../privacy/privacy-overview.md)
   + [Controlelogboek](../privacy/audit-log.md)
   + [Door de klant beheerde toetsen](../privacy/cmk.md)

+ Gebruik hoofdletters {#cja-usecases}
   + [Gebruiksgevallen Customer Journey Analytics](../use-cases/cja-usecases.md)
   + Gegevens Googles Analytics {#ga}
      + [Overzicht van migreren van Googles Analytics naar Customer Journey Analytics](../use-cases/ga/overview.md)
      + [Historische gegevens van Googles Analytics opnemen in platform](../use-cases/ga/backfill.md)
      + [Gegevens voor streaming Googles Analytics configureren in Platform](../use-cases/ga/streaming.md)
      + [Rapport over gegevens over Googles Analytics in Customer Journey Analytics](../use-cases/ga/report.md)
   + Gegevensinvoer {#data-ingestion}
      + [Gegevens van Marketo Engage in Adobe Experience Platform opnemen en in Customer Journey Analytics rapporteren](../use-cases/data-ingestion/marketo.md)
      + [Adobe Experience Platform-publiek vertalen in Customer Journey Analytics](../use-cases/data-ingestion/ingest-aep-segments.md)
   + Gegevensweergaven {#data-views}
      + [Gebruiksscenario&#39;s voor gegevensweergaven](../use-cases/data-views/data-views-usecases.md)
      + [Afmetingen en metriek van binding gebruiken](../use-cases/data-views/binding-dimensions-metrics.md)
   + Gegevens exporteren {#data-export}
      + [Overzicht](../use-cases/data-export/overview.md)
      + [BI-extensie](../use-cases/data-export/bi-extension.md)
      + [Gegevensbestanden exporteren](../use-cases/data-export/export-datasets.md)
      + [Volledige tabel exporteren](../use-cases/data-export/export-full-table.md)
      + [De Dienst van de vraag en de datasets van de Uitvoer](../use-cases/data-export/queryservice-export-datasets.md)
   + B2B {#b2b}
      + [Een B2B-voorbeeldproject](../use-cases/b2b/example.md)
      + [Gegevens op accountniveau toevoegen als een opzoekgegevensset](../use-cases/b2b/b2b.md)
   + Kanaalgegevens {#cross-channel}
      + [Gegevens via kanalen analyseren](../use-cases/cross-channel/cross-channel.md)
      + [Telefooncentrum en webgegevens importeren](../use-cases/cross-channel/call-center.md)
   + Adobe Analytics-gegevens {#aa-data}
      + [Afmetingen marketingkanaal gebruiken](../use-cases/aa-data/marketing-channels.md)
      + [Rapportsuites combineren met verschillende schema&#39;s](../use-cases/aa-data/combine-report-suites.md)
   + Complexe gegevens {#complex-data}
      + [Arrays van objecten gebruiken](../use-cases/object-arrays.md)
   + Afgeleide velden {#derived-fields}
      + [Gebruik afgeleide gebieden om over doelstellingen te rapporteren](../use-cases/goals-using-derived-fields.md)

+ Labs {#labs}
   + [Gebruikershandleiding voor labels](../labs/labs.md)

+ Problemen oplossen {#troubleshooting}
   + [Adobe Analytics-gegevens vergelijken met Customer Journey Analytics-gegevens](../troubleshooting/compare.md)
   + [De consistentie van metriek en het aantal van het publiekslidmaatschap tussen CDP In real time en Customer Journey Analytics](../troubleshooting/consistency-rcdp-cja.md)
   + [Gebrek aan machtigingen](../troubleshooting/lack-of-permissions.md)

+ Technische notities {#technotes}
   + [Toegangsbeheer](../technotes/access-control.md)
   + [Gegevenscentra](../technotes/data-centers.md)
   + [Gevolgen van verwijdering](../technotes/deletion.md)
   + [Domeinen](../technotes/domains.md)
   + [Woordenlijst](../technotes/glossary.md)
   + [Guardrails](../technotes/guardrails.md)
   + [IP-adressen](../technotes/ip-addresses.md)
   + [Prestaties van Customers Journey Analytics optimaliseren](../technotes/optimizing-performance.md)
   + [Gebruik weergeven en beheren](../technotes/estimate-usage.md)

+ [Customer Journey Analytics-API](https://developer.adobe.com/cja-apis/docs/)
