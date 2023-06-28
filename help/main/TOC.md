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
source-git-commit: cf6da1f126933f17e05fb458f52dff93c1601891
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 25%

---


# Adobe Customer Journey Analytics Guide {#using}

+ [Adobe Customer Journey Analytics Guide](../getting-started/cja-landing.md)

+ Release-opmerkingen {#releases}
   + [Meest recente release](../release-notes/latest.md)
   + [2023 releases](../release-notes/2023.md)
   + [2022 introducties](../release-notes/2022.md)
   + [Release 2021](../release-notes/2021.md)
   + [2020 introducties](../release-notes/2020.md)
   + [Customer Journey Analytics-releases](../release-notes/releases.md)
   + [Customer Journey Analytics-documentupdates](../release-notes/doc-changes.md)

+ Aan de slag {#cja-overview}
   + [Overzicht van Customer Journey Analytics](../getting-started/cja-overview.md)
   + [Snelle startgids](../getting-started/cja-getting-started.md)
   + [Openingspagina](../getting-started/landing.md)
   + [Veelgestelde vragen](../getting-started/cja-faq.md)
   + [Customer Journey Analytics tot BI-oplossingen vergelijken](../getting-started/cja-vs-bi.md)

+ Customer Journey Analytics en Adobe Analytics {#compare-aa-cja}
   + [Evolutie uit Adobe Analytics](../getting-started/aa-to-cja.md)
   + [Gebruikershandleiding voor Adobe Analytics-gebruikers](../getting-started/aa-to-cja-user.md)
   + Vergelijking met Adobe Analytics {#cja-aa-comparison}
      + [Adobe Analytics-gegevens gebruiken in Customer Journey Analytics](../getting-started/aa-vs-cja/aa-data-in-cja.md)
      + [Ondersteuning voor Customer Journey Analytics-functies](../getting-started/aa-vs-cja/cja-aa.md)
      + [Vergelijk terminologie voor de gegevens van de Analyse die door de Bronschakelaar van de Analyse worden overgegaan](../getting-started/aa-vs-cja/terminology.md)
      + [Gegevensverwerking in Adobe Analytics en Customer Journey Analytics vergelijken](../getting-started/aa-vs-cja/data-processing-comparisons.md)
      + [Virtuele rapportageomgevingen en sandboxomgevingen](../getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md)
      + [Verwerkingsregels, VISTA en classificaties versus Data Prep](../getting-started/aa-vs-cja/pr-vista-dataprep.md)
      + [STEUN, ECID, AACUSTOMID en de Analytics Source Connector](../getting-started/aa-vs-cja/aaid-ecid-adc.md)

+ Gegevensopname {#cja-data-ingestion}
   + [Overzicht van gegevensinname](../data-ingestion/data-ingestion.md)
   + Hulplijnen voor snel starten samenstellen en gebruiken{#ingest-use-guides}
      + [Adobe Analytics](../data-ingestion/analytics.md)
      + [Adobe Experience Platform Web SDK en Edge Network](../data-ingestion/aepwebsdk.md)
      + [Batchgegevens](../data-ingestion/batch.md)
      + [Streaming gegevens](../data-ingestion/streaming.md)
      + [Bronaansluitingen](../data-ingestion/sources.md)

+ Verbindingen {#cja-connections}
   + [Overzicht van verbindingen](../connections/overview.md)
   + [Verbinding maken](../connections/create-connection.md)
   + [Verbindingen beheren](../connections/manage-connections.md)
   + [Gecombineerde gegevenssets voor gebeurtenissen](../connections/combined-dataset.md)
   + [Standaardzoekopdrachten](../connections/standard-lookups.md)
   + [Kanaaloverschrijdende analyse](../connections/cca.md)

+ Gegevens {#cja-dataviews}
   + [Overzicht van gegevensweergaven](../data-views/data-views.md)
   + [Een gegevensweergave maken of bewerken](../data-views/create-dataview.md)
   + Componentinstellingen {#component-settings}
      + [Overzicht van componentinstellingen](../data-views/component-settings/overview.md)
      + [Attributie](../data-views/component-settings/attribution.md)
      + [Gedraging](../data-views/component-settings/behavior.md)
      + [Indeling](../data-views/component-settings/format.md)
      + [Waarden uitsluiten opnemen](../data-views/component-settings/include-exclude-values.md)
      + [Metrische deduplicatie](../data-views/component-settings/metric-deduplication.md)
      + [Geen waardeopties](../data-views/component-settings/no-value-options.md)
      + [Persistentie](../data-views/component-settings/persistence.md)
      + [Subtekenreeks](../data-views/component-settings/substring.md)
      + [Waardebeperking](../data-views/component-settings/value-bucketing.md)
   + [Standaardcomponentverwijzing](../data-views/component-reference.md)
   + [SQL Connector](../data-views/sql-connector.md)
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
      + [Kleurpaletten](../analysis-workspace/build-workspace-project/color-palettes.md)
      + [Dichtheid weergeven](../analysis-workspace/build-workspace-project/view-density.md)

   + Visualisaties {#visualizations}
      + [Overzicht van visualisaties](../analysis-workspace/visualizations/freeform-analysis-visualizations.md)
      + [Databronnen beheren](../analysis-workspace/visualizations/t-sync-visualization.md)

      + Vrije-vormentabel {#freeform-table}
         + [Vrije-vormentabel](../analysis-workspace/visualizations/freeform-table/freeform-table.md)
         + Instellingen voor kolommen en rijen {#column-row-settings}
            + [Kolominstellingen](../analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)
            + [Rij-instellingen](../analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)
            + [Dynamische versus statische items](../analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md)

         + [Tabellen filteren en sorteren](../analysis-workspace/visualizations/freeform-table/filter-and-sort.md)

         + [Workspace-totalen](../analysis-workspace/visualizations/freeform-table/workspace-totals.md)

      + Cohorttabel {#cohort-table}
         + [Wat is cohortanalyse?](../analysis-workspace/visualizations/cohort-table/cohort-analysis.md)
         + [Een rapport voor cohortanalyse configureren](../analysis-workspace/visualizations/cohort-table/t-cohort.md)
         + [Gebruiksgevallen van cohortanalyse](../analysis-workspace/visualizations/cohort-table/cohort-use-cases.md)

      + Uitval {#fallout}
         + [Overzicht van uitval](../analysis-workspace/visualizations/fallout/fallout-flow.md)
         + [Een uitvalvisualisatie configureren](../analysis-workspace/visualizations/fallout/configuring-fallout.md)
         + [Interdimensionale uitval](../analysis-workspace/visualizations/fallout/configuring-interdimensional-fallout.md)
         + [Filters toepassen in falloutanalyse](../analysis-workspace/visualizations/fallout/compare-segments-fallout.md)


      + Stroom {#flow}
         + [Overzicht van stroom](../analysis-workspace/visualizations/c-flow/flow.md)
         + [Een stroomvisualisatie configureren](../analysis-workspace/visualizations/c-flow/create-flow.md)
         + [Interdimensionale stromen](../analysis-workspace/visualizations/c-flow/multi-dimensional-flow.md)
      + [Gebied en gestapeld gebied](../analysis-workspace/visualizations/area.md)

      + [Balkgrafiek en gestapelde-balkgrafiek](../analysis-workspace/visualizations/bar.md)
      + [Staafdiagram](../analysis-workspace/visualizations/bullet-graph.md)
      + [Combodiagram](../analysis-workspace/visualizations/combo-charts.md)
      + [Cirkeldiagram](../analysis-workspace/visualizations/donut.md)
      + [Histogram](../analysis-workspace/visualizations/histogram.md)
      + [Horizontale-balkgrafiek en horizontale-balkgrafiek gestapeld](../analysis-workspace/visualizations/horizontal-bar.md)
      + [Intelligente bijschriften](../analysis-workspace/visualizations/intelligent-captions.md)
      + [Samenvatting van metrische sleutel](../analysis-workspace/visualizations/key-metric.md)
      + [Lijn](../analysis-workspace/visualizations/line.md)
      + [Spreidingsdiagram](../analysis-workspace/visualizations/scatterplot.md)
      + [Cijferoverzicht en Wijzigingsoverzicht](../analysis-workspace/visualizations/summary-number-change.md)
      + [Tekst](../analysis-workspace/visualizations/text.md)
      + [Boomstructuur](../analysis-workspace/visualizations/treemap.md)
      + [Venn](../analysis-workspace/visualizations/venn.md)

   + Deelvensters {#panels}
      + [Overzicht van deelvensters](../analysis-workspace/c-panels/panels.md)
      + [Deelvenster voor attributie](../analysis-workspace/c-panels/attribution.md)
      + [Leeg deelvenster](../analysis-workspace/c-panels/blank-panel.md)
      + [Deelvenster Experimentatie](../analysis-workspace/c-panels/experimentation.md)
      + [Deelvenster Vrije vorm](../analysis-workspace/c-panels/freeform-panel.md)
      + [Deelvenster Snelle inzichten](../analysis-workspace/c-panels/quickinsight.md)
      + [Deelvenster voor gelijktijdige mediaviewers](../analysis-workspace/c-panels/media-concurrent-viewers.md)
      + Tijd van afspelen van media besteed {#media-playback-timespent}
         + [Overzicht](../analysis-workspace/c-panels/media-playback-timespent/media-playback-time-spent.md)
         + [Invoer- en uitvoerinstellingen](../analysis-workspace/c-panels/media-playback-timespent/panel-inputs-outputs.md)
         + [Veelgestelde vragen](../analysis-workspace/c-panels/media-playback-timespent/faqs.md)

   + Projecten cureren, delen en plannen {#curate-share}
      + [Menu Delen](../analysis-workspace/curate-share/send-schedule-files.md)
      + [Cursieve projecten](../analysis-workspace/curate-share/curate.md)
      + [Projecten delen](../analysis-workspace/curate-share/share-projects.md)
      + [Deelbare koppelingen maken](../analysis-workspace/curate-share/shareable-links.md)
      + [Alleen-weergeven -projecten](../analysis-workspace/curate-share/view-only-projects.md)
      + [PDF- of CSV-bestanden downloaden](../analysis-workspace/curate-share/download-send.md)
      + [Projecten plannen](../analysis-workspace/curate-share/t-schedule-report.md)

   + Virtual Analyst {#virtual-analyst}
      + [Overzicht van Virtual Analyst](../analysis-workspace/virtual-analyst/overview.md)
      + Anomaliedetectie {#anomaly-detection}
         + [Overzicht van anomaliedetectie](../analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md)
         + [Anomalieën weergeven in Analysis Workspace](../analysis-workspace/virtual-analyst/c-anomaly-detection/view-anomalies.md)
         + [Statistische technieken voor anomaliedetectie](../analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md)
   + [Gebruikersvoorkeuren](../analysis-workspace/user-preferences.md)

   + Veelgestelde vragen over Workspace {#workspace-faq}
      + [Veelgestelde vragen](../analysis-workspace/workspace-faq/faq.md)
      + [Foutberichten](../analysis-workspace/workspace-faq/error-messages.md)
      + [Beperkingen van Analysis Workspace](../analysis-workspace/workspace-faq/aw-limitations.md)
      + [Beheervereisten](../analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md)
      + [Toegankelijkheid in Analysis Workspace](../analysis-workspace/workspace-faq/aw-accessibility.md)
      + [Lange staart in Analysis Workspace](../analysis-workspace/workspace-faq/long-tail.md)

+ Analysedashboards {#cja-dashboards}
   + [Analysedashboards - Overzicht](../mobile-app/home.md)
   + [Curatortaken](../mobile-app/curator.md)
   + [Een mobiele scorecard maken](../mobile-app/create-scorecard.md)
   + [Stel managers in voor het gebruik van dashboards](../mobile-app/set-up-execs.md)
   + [Snelle handleiding voor executive gebruikers](../mobile-app/executive.md)

+ Analyse met instructies {#guided-analysis}
   + [Overzicht](../guided-analysis/overview.md)
   + Typen analyses {#analysis-types}
      + [Overzicht](../guided-analysis/analysis-types/overview.md)
      + [Trechter](../guided-analysis/analysis-types/funnel.md)
      + [Trends](../guided-analysis/analysis-types/trends.md)
      + [Groei van gebruikers](../guided-analysis/analysis-types/user-growth.md)
   + [Veelgestelde vragen](../guided-analysis/faq.md)

+ Onderdelen {#cja-components}
   + [Overzicht van onderdelen](../components/overview.md)
   + [Componentbeschrijvingen toevoegen](../components/add-component-descriptions.md)

   + Annotaties {#annotations}
      + [Overzicht van annotaties](../components/annotations/overview.md)
      + [Annotaties maken](../components/annotations/create-annotations.md)
      + [Annotaties beheren](../components/annotations/manage-annotations.md)
      + [Annotaties weergeven](../components/annotations/view-annotations.md)
      + [Mobiele annotaties](../components/annotations/mobile-annotations.md)

   + Soorten publiek {#audiences}
      + [Overzicht van soorten publiek](../components/audiences/audiences-overview.md)
      + [Soorten publiek maken en publiceren](../components/audiences/publish.md)
      + [Soorten publiek beheren](../components/audiences/manage.md)

   + Dimensies {#dimensions}
      + [Voorvertoningsdimensies](../components/dimensions/view-dimensions.md)
      + [Uitsplitsingsdimensies](../components/dimensions/t-breakdown-fa.md)
      + [Tijduitsplitsende dimensies](../components/dimensions/time-parting-dimensions.md)
      + [Dimension met zeer hoge kardinaliteit](../components/dimensions/high-cardinality.md)

   + [Metrics](../components/apply-create-metrics.md)

   + Filters {#cja-filters}
      + [Overzicht van filters](../components/filters/filters-overview.md)
      + [Filters maken](../components/filters/create-filters.md)
      + [Snelle filters](../components/filters/quick-filters.md)
      + [Filter builder](../components/filters/filter-builder.md)
      + [Filters beheren](../components/filters/manage-filters.md)
      + [Operatoren](../components/filters/operators.md)

   + Berekende standaarden {#cja-calcmetrics}
      + [Overzicht van berekende metriek](../components/calc-metrics/calc-metr-overview.md)
      + Workflow voor berekende standaard {#cm-workflow}
         + [Workflow voor berekende standaard](../components/calc-metrics/cm-workflow/cm-workflow.md)
         + [Cijfers zoeken](../components/calc-metrics/cm-workflow/cm-finding.md)
         + [Metrische gegevens samenstellen](../components/calc-metrics/cm-workflow/cm-build-metrics.md)
         + [Type en attributie metrisch](../components/calc-metrics/cm-workflow/m-metric-type-alloc.md)
         + [Een metrische waarde voor Paginaweergaven per bezoek maken](../components/calc-metrics/cm-workflow/cm-pvv.md)
         + [Een &quot;Deelname&quot;-metrisch maken](../components/calc-metrics/cm-workflow/participation-metric.md)
         + [Gefilterde metriek](../components/calc-metrics/cm-workflow/metrics-with-segments.md)
         + [Filters stapelen en vervangen](../components/calc-metrics/cm-workflow/cm-stack-seg.md)
         + [Gefilterde en gewogen cijfers](../components/calc-metrics/cm-workflow/cm-weighted-metric.md)
         + [Functies gebruiken](../components/calc-metrics/cm-workflow/cm-using-functions.md)
         + [Berekende standaard een label geven](../components/calc-metrics/cm-workflow/cm-tagging.md)
         + [Berekende standaard goedkeuren](../components/calc-metrics/cm-workflow/cm-approving.md)
         + [Berekende standaard delen](../components/calc-metrics/cm-workflow/cm-sharing.md)
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

   + Gegevenswoordenboek {#data-dictionary}
      + [Overzicht van gegevenswoordenboek](../components/data-dictionary/data-dictionary-overview.md)
      + [Componentinformatie weergeven in gegevenswoordenboek](../components/data-dictionary/view-data-dictionary.md)
      + [Onderdeelitems in gegevenswoordenboek bewerken](../components/data-dictionary/edit-entries-data-dictionary.md)
      + [Gezondheid gegevenswoordenboek controleren](../components/data-dictionary/monitor-data-dictionary-health.md)

+ Report Builder {#cja-reportbuilder}
   + [Overzicht van Report Builder](../report-builder/report-buider-overview.md)
   + [Report Builder instellen](../report-builder/report-builder-setup.md)
   + [Een gegevensblok maken](../report-builder/create-a-data-block.md)
   + [Report Builder Hub](../report-builder/report-builder-hub.md)
   + [Een gegevensweergave selecteren](../report-builder/select-data-view.md)
   + [Een datumbereik selecteren](../report-builder/select-date-range.md)
   + [Werken met filters](../report-builder/work-with-filters.md)
   + [Dimension filteren](../report-builder/filter-dimensions.md)
   + [Gegevensblokken beheren](../report-builder/manage-reportbuilder.md)
   + [Workbooks plannen](../report-builder/schedule-reportbuilder.md)
   + [Beperkte labels](../report-builder/restricted-labels.md)
   + [Report Builder-instellingen](../report-builder/report-builder-settings.md)

+ Stiksel {#stitching}
   + [Overzicht](../stitching/overview.md)
   + [Hoe stikken werkt](../stitching/explained.md)
   + [Verstikte gegevenssets maken en beheren](../stitching/stitching-ui.md)
   + [Veelgestelde vragen](../stitching/faq.md)

+ Kanaaloverschrijdende analyse {#cca}
   + [Overzicht van kanaalanalyse](../cca/overview.md)
   + [Hoe herspeelt u](../cca/replay.md)
   + [Veelgestelde vragen over kanaalanalyse](../cca/faq.md)

+ Adobe-integratie {#integrations}
   + [Adobe-oplossingen integreren met Customer Journey Analytics-overzicht](/help/integrations/overview.md)
   + [Adobe Analytics met Customer Journey Analytics integreren](/help/integrations/aa.md)
   + [Journey Optimizer-gegevens integreren met Customer Journey Analytics](/help/integrations/ajo.md)
   + [Beslissingsbeheergegevens integreren met Customer Journey Analytics](/help/integrations/ajo-od.md)
   + [AI van klant integreren met Customer Journey Analytics](/help/integrations/customer-ai.md)

+ Data Governance {#cja-privacy}
   + [Data Governance](../privacy/privacy-overview.md)
   + [Controlelogboek](../privacy/audit-log.md)
   + [Door de klant beheerde toetsen](../privacy/cmk.md)

+ Gebruik hoofdletters {#cja-usecases}
   + [Customer Journey Analytics-gebruik](../use-cases/cja-usecases.md)

   + Google Analytics {#ga}
      + [Gegevens migreren van Google Analytics naar Customer Journey Analytics-overzicht](../use-cases/ga/overview.md)
      + [Historische gegevens van Google Analytics opnemen in Platform](../use-cases/ga/backfill.md)
      + [Gegevens van streaming Google Analytics in Platform configureren](../use-cases/ga/streaming.md)
      + [Rapport over gegevens over Google Analytics in Customer Journey Analytics](../use-cases/ga/report.md)

   + Gegevensinvoer {#data-ingestion}
      + [Marketo Engage-gegevens in Adobe Experience Platform opnemen en in Customer Journey Analytics rapporteren](../use-cases/data-ingestion/marketo.md)
      + [Adobe Experience Platform-publiek vertalen in Customer Journey Analytics](../use-cases/data-ingestion/ingest-aep-segments.md)
   + Gegevensweergaven {#data-views}
      + [Gebruiksscenario&#39;s voor gegevensweergaven](../use-cases/data-views/data-views-usecases.md)
      + [Afmetingen en metriek van binding gebruiken](../use-cases/data-views/binding-dimensions-metrics.md)

   + B2B {#b2b}
      + [Gegevens op accountniveau toevoegen als een opzoekgegevensset](../use-cases/b2b/b2b.md)

   + Kanaalgegevens {#cross-channel}
      + [Gegevens via kanalen analyseren](../use-cases/cross-channel/cross-channel.md)
      + [Telefooncentrum en webgegevens importeren](../use-cases/cross-channel/call-center.md)

   + Adobe Analytics-gegevens {#aa-data}
      + [Afmetingen marketingkanaal gebruiken](../use-cases/aa-data/marketing-channels.md)
      + [Rapportsuites combineren met verschillende schema&#39;s](../use-cases/aa-data/combine-report-suites.md)

   + Complexe gegevens {#complex-data}
      + [Arrays van objecten gebruiken](../use-cases/object-arrays.md)

+ Beheer {#cja-admin}
   + [Toegangsbeheer](../admin/cja-access-control.md)
   + [Gebruik weergeven en beheren](../admin/estimate-usage.md)
   + [Gevolgen van verwijdering](../admin/cja-deletion.md)
   + [Customer Journey Analytics-prestaties optimaliseren](../admin/optimizing-performance.md)

+ Labs {#labs}
   + [Gebruikershandleiding voor labels](../labs/labs.md)

+ Problemen oplossen {#troubleshooting}
   + [Adobe Analytics-gegevens vergelijken met Customer Journey Analytics-gegevens](../troubleshooting/compare.md)
   + [Consistentie van metriek en het aantal van het publiekslidmaatschap tussen CDP In real time en Customer Journey Analytics](../troubleshooting/consistency-rcdp-cja.md)

+ [Customer Journey Analytics glossarium](../getting-started/cja-glossary.md)

+ [Customer Journey Analytics API](https://developer.adobe.com/cja-apis/docs/)
