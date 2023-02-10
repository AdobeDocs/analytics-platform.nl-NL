---
git-repo: https://github.com/AdobeDocs/analytics-platform.nl-NL
cloud: Experience Cloud
product: adobe analytics
sub-product: customer journey
solution: Customer Journey Analytics
type: Documentation
index: true
user-guide-title: Handleiding voor Customer Journey Analytics
user-guide-description: Leer meer over Customer Journey Analytics (CJA) en hoe u Analysis Workspace kunt gebruiken met data van Experience Platform.
breadcrumb-title: Handleiding voor Customer Journey Analytics
source-git-commit: 7ee35a3d1e5b4335d87ac3649585a9a4d079bdf5
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 33%

---


# Handleiding voor Customer Journey Analytics {#using}

+ Release-opmerkingen {#releases}
   + [Meest recente release](../release-notes/latest.md)
   + [2023 releases](../release-notes/2023.md)
   + [2022 introducties](../release-notes/2022.md)
   + [Release 2021](../release-notes/2021.md)
   + [2020 introducties](../release-notes/2020.md)
   + [CJA-releases](../release-notes/releases.md)
   + [CJA-documentatieupdates](../release-notes/doc-changes.md)

+ [Overzicht van Customer Journey Analytics](../getting-started/cja-overview.md)

+ Aan de slag {#cja-getting-started}
   + [Snelle startgids](../getting-started/cja-getting-started.md)
   + [Openingspagina](../getting-started/landing.md)
   + [Veelgestelde vragen](../getting-started/cja-faq.md)

+ Customer Journey Analytics en Adobe Analytics {#compare-aa-cja}
   + [Evolutie uit Adobe Analytics ](../getting-started/aa-to-cja.md)
   + [Gebruikershandleiding voor Adobe Analytics-gebruikers](../getting-started/aa-to-cja-user.md)
   + Vergelijking met Adobe Analytics {#cja-aa-comparison}
      + [Adobe Analytics-gegevens gebruiken in Customer Journey Analytics](../getting-started/aa-vs-cja/aa-data-in-cja.md)
      + [Ondersteuning voor Customer Journey Analytics-functies](../getting-started/aa-vs-cja/cja-aa.md)
      + [Vergelijk terminologie voor de gegevens van de Analyse die door de Bronschakelaar van de Analyse worden overgegaan](../getting-started/aa-vs-cja/terminology.md)
      + [Gegevensverwerking vergelijken in Adobe Analytics en CJA](../getting-started/aa-vs-cja/data-processing-comparisons.md)
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
   + [Labels en beleid](../data-views/data-governance.md)


+ Werkruimteprojecten {#cja-workspace}
   + [Overzicht van Analysis Workspace](../analysis-workspace/home.md)
   + [Basisanalyse uitvoeren](../analysis-workspace/perform-basic-analysis.md)
   + [Geavanceerde analyse uitvoeren](../analysis-workspace/perform-adv-analysis.md)

   + Projecten {#build-workspace-project}
      + [Overzicht van projecten](../analysis-workspace/build-workspace-project/freeform-overview.md)
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
         + [Pagineren, filteren en tabellen sorteren](../analysis-workspace/visualizations/freeform-table/filter-and-sort.md)

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
   + Attribution IQ {#attribution}
      + [Overzicht van attributie](../analysis-workspace/attribution/overview.md)
      + [Attributiemodellen en terugzoekvensters](../analysis-workspace/attribution/models.md)
      + [Algoritmische attributie](../analysis-workspace/attribution/algorithmic.md)
      + [Aanbevolen werkwijzen voor kenmerken](../analysis-workspace/attribution/best-practices.md)
      + [Veelgestelde vragen](../analysis-workspace/attribution/faq.md)
   + Virtual Analyst {#virtual-analyst}
      + [Overzicht van Virtual Analyst](../analysis-workspace/virtual-analyst/overview.md)
      + Anomaliedetectie {#anomaly-detection}
         + [Overzicht van anomaliedetectie](../analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md)
         + [Anomalieën weergeven in Analysis Workspace](../analysis-workspace/virtual-analyst/c-anomaly-detection/view-anomalies.md)
         + [Statistische technieken voor anomaliedetectie](../analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md)
   + [Gebruikersvoorkeuren](../analysis-workspace/user-preferences.md)

   + Veelgestelde vragen over Workspace {#workspace-faq}
      + [Veelgestelde vragen](../analysis-workspace/workspace-faq/faq.md)
      + [Analysis Workspace-prestaties optimaliseren](../analysis-workspace/workspace-faq/optimizing-performance.md)
      + [Foutberichten](../analysis-workspace/workspace-faq/error-messages.md)
      + [Beperkingen van Analysis Workspace](../analysis-workspace/workspace-faq/aw-limitations.md)
      + [Beheervereisten](../analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md)
      + [Toegankelijkheid in Analysis Workspace](../analysis-workspace/workspace-faq/aw-accessibility.md)
      + [Lange staart in Analysis Workspace](../analysis-workspace/workspace-faq/long-tail.md)












+ Onderdelen {#cja-components}
   + [Overzicht van onderdelen](../components/overview.md)
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
      + [Een filter maken](../components/filters/create-filters.md)
      + [Filters beheren](../components/filters/manage-filters.md)
      + [Snelle filters](../components/filters/quick-filters.md)
      + [Ad-hocfilters](../components/filters/ad-hoc-filters.md)
      + [Operatoren](../components/filters/operators.md)
   + Berekende statistieken {#cja-calcmetrics}
      + [Overzicht van berekende metriek](../components/calc-metrics/calc-metr-overview.md)
      + Workflow voor berekende statistieken {#cm-workflow}
         + [Workflow voor berekende standaard](../components/calc-metrics/cm-workflow/cm-workflow.md)
         + [Cijfers zoeken](../components/calc-metrics/cm-workflow/cm-finding.md)
         + [Cijfers samenstellen](../components/calc-metrics/cm-workflow/cm-build-metrics.md)
         + [Type cijfers en attributie](../components/calc-metrics/cm-workflow/m-metric-type-alloc.md)
         + [Een eenvoudige indicator voor &quot;Paginaweergaven per bezoek&quot; maken](../components/calc-metrics/cm-workflow/cm-pvv.md)
         + [Gefilterde metriek](../components/calc-metrics/cm-workflow/metrics-with-segments.md)
         + [Segmenten stapelen en vervangen](../components/calc-metrics/cm-workflow/cm-stack-seg.md)
         + [Gefilterde en gewogen cijfers](../components/calc-metrics/cm-workflow/cm-weighted-metric.md)
         + [Functies gebruiken](../components/calc-metrics/cm-workflow/cm-using-functions.md)
         + [Participatiecijfers](../components/calc-metrics/cm-workflow/participation-metric.md)
         + [Berekende standaard een label geven](../components/calc-metrics/cm-workflow/cm-tagging.md)
         + [Berekende standaard goedkeuren](../components/calc-metrics/cm-workflow/cm-approving.md)
         + [Berekende standaard delen](../components/calc-metrics/cm-workflow/cm-sharing.md)
         + [Berekende standaard-beheer](../components/calc-metrics/cm-workflow/cm-manager.md)
      + [Basisfuncties](../components/calc-metrics/cm-functions.md)
      + [Geavanceerde functies](../components/calc-metrics/cm-adv-functions.md)
   + Datumbereiken {#cja-date-ranges}
      + [Overzicht van datumbereiken](../components/date-ranges/overview.md)
      + [Een datumbereik maken](../components/date-ranges/create.md)
      + [Datumbereiken beheren](../components/date-ranges/manage.md)
      + [Overzicht van agenda](../components/date-ranges/calendar.md)
      + [Aangepaste datumbereiken maken](../components/date-ranges/custom-date-ranges.md)
      + [Datumvergelijking](../components/date-ranges/time-comparison.md)

+ Analysedashboards {#cja-dashboards}
   + [Analysedashboards - Overzicht](../mobile-app/home.md)
   + [Curatortaken](../mobile-app/curator.md)
   + [Een mobiele scorecard maken](../mobile-app/create-scorecard.md)
   + [Stel managers in voor het gebruik van dashboards](../mobile-app/set-up-execs.md)
   + [Snelle handleiding voor executive gebruikers](../mobile-app/executive.md)

+ Report Builder {#cja-reportbuilder}
   + [Overzicht van Report Builder](../report-builder/report-buider-overview.md)
   + [Report Builder instellen](../report-builder/report-builder-setup.md)
   + [Een gegevensblok maken](../report-builder/create-a-data-block.md)
   + [Report Builder Hub](../report-builder/report-builder-hub.md)
   + [Een datumbereik selecteren](../report-builder/select-date-range.md)
   + [Werken met filters](../report-builder/work-with-filters.md)
   + [Dimension filteren](../report-builder/filter-dimensions.md)
   + [Gegevensblokken beheren](../report-builder/manage-reportbuilder.md)
   + [Workbooks plannen](../report-builder/schedule-reportbuilder.md)
   + [Beperkte labels](../report-builder/restricted-labels.md)
   + [Report Builder-instellingen](../report-builder/report-builder-settings.md)

+ Kanaaloverschrijdende analyse {#cca}
   + [Overzicht van kanaalanalyse](../cca/overview.md)
   + [Hoe herspeelt u](../cca/replay.md)
   + [Veelgestelde vragen over kanaalanalyse](../cca/faq.md)

+ Adobe-integratie {#integrations}
   + [Adobe-oplossingen integreren met CJA-overzicht](/help/integrations/overview.md)
   + [Adobe Analytics met Customer Journey Analytics integreren](/help/integrations/aa.md)
   + [Journey Optimizer-gegevens integreren met CJA](/help/integrations/ajo.md)
   + [AI-gegevens van klanten integreren met CJA](/help/integrations/customer-ai.md)

+ Data Governance {#cja-privacy}
   + [Data Governance](../privacy/privacy-overview.md)
   + [Controlelogboek](../privacy/audit-log.md)
   + [Door de klant beheerde toetsen](../privacy/cmk.md)

+ Gebruik hoofdletters {#cja-usecases}
   + [Customer Journey Analytics-gebruik](../use-cases/cja-usecases.md)
   + Google Analytics {#ga}
      + [Gegevens migreren van Google Analytics naar CJA-overzicht](../use-cases/ga/overview.md)
      + [Historische gegevens van Google Analytics opnemen in Platform](../use-cases/ga/backfill.md)
      + [Gegevens van streaming Google Analytics in Platform configureren](../use-cases/ga/streaming.md)
      + [Rapport over gegevens over Google Analytics in CJA](../use-cases/ga/report.md)
   + Gegevensinvoer {#data-ingestion}
      + [Marketo Engage-gegevens in AEP opnemen en rapporteren in CJA](../use-cases/data-ingestion/marketo.md)
      + [AEP-publiek vertalen in CJA](../use-cases/data-ingestion/ingest-aep-segments.md)
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

+ Labs {#labs}
   + [Gebruikershandleiding voor labels](../labs/labs.md)

+ Problemen oplossen {#troubleshooting}
   + [Adobe Analytics-gegevens vergelijken met CJA-gegevens](../troubleshooting/compare.md)
   + [Consistentie van metriek en het tellen van het publieksenlidmaatschap tussen CDP In real time en CJA](../troubleshooting/consistency-rcdp-cja.md)

+ [Verklarende woordenlijst](../getting-started/cja-glossary.md)

+ [CJA API](https://developer.adobe.com/cja-apis/docs/)
