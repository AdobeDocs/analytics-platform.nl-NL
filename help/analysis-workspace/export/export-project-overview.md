---
description: Begrijp de methoden die beschikbaar zijn voor exporteren vanuit Analysis Workspace.
keywords: Analysis Workspace
title: Projectgegevens exporteren
feature: Curate and Share
exl-id: 3d467050-4bf0-4bdb-b7d2-eba67fbd526d
role: User
source-git-commit: 70daf2251576bc3b473e63b3bb7c48f2d16dbffe
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Overzicht van exporteren

U kunt (een deel van) Customer Journey Analytics-projecten exporteren uit Analysis Workspace. U kunt Customer Journey Analytics-rapporten exporteren om een aantal redenen, zoals gebruik in gereedschappen van derden of combinatie met externe gegevens.

In de volgende secties worden de ondersteunde bestandstypen, de verschillende exportmethoden en de voordelen van elke methode beschreven.

## Ondersteunde bestandstypen

U kunt Customer Journey Analytics-rapporten exporteren als een PDF-, CSV- of JSON-bestand.

* **PDF:** verstrekt een gemakkelijke manier om visuele gegevens met belanghebbenden te delen. PDF-bestanden bevatten alle weergegeven (zichtbare) tabellen en visualisaties in het project.

* **CSV:** staat u toe om ruwe gegevens in een spreadsheettoepassing, zoals Excel te bekijken. CSV-bestanden bevatten gegevens zonder opmaak.

* **JSON:** verstrekt een open standaarddossierformaat voor het delen van gegevens.

## Exportmethoden

Er zijn verschillende methoden beschikbaar als u vanuit Analysis Workspace wilt exporteren. Wanneer u een exportmethode kiest, moet u bedenken wat u wilt exporteren en wie er toegang toe moet krijgen.

| Exportmethode | Gebruik deze methode als u... |
|---------|----------|
| [ Download aan uw werkstation ](/help/analysis-workspace/export/download-send.md) | <li>Download projecten naar uw persoonlijke werkstation.</li><li>Alleen ad-hocgegevens downloaden (niet gepland).</li> <li>Download maximaal 50.000 rijen.</li> <!--true? Are there 2 different options to download to your workstation?--> <!-- is this emailing it? --> |
| [ verzendt naar andere gebruikers ](/help/analysis-workspace/curate-share/t-schedule-report.md) | <li>E-mail geëxporteerde Customer Journey Analytics-gegevens naar andere gebruikers in uw organisatie.</li><li>Verzend de e-mail ad hoc of volgens een schema.</li> <li>Neem maximaal 50.000 rijen op in de e-mail.</li> <!--true?--> |
| [ Uitvoer naar een wolkentoepassing ](/help/analysis-workspace/export/export-cloud.md) | <li>Exporteren naar een cloudlocatie, zoals <ul><li>Adobe Experience Platform Data Landing Zone</li><li>Google Cloud Platform</li><li>Microsoft Azure</li><li>Amazon S3</li><li>Snowflake</li></ul></li><li>Gegevens ad hoc of volgens een schema exporteren.</li><li>Grotere hoeveelheden Customer Journey Analytics-gegevens opslaan.</li><li>Exporteer volledige tabellen die duizenden of miljoenen rijen bevatten.<!-- What other things? Wiki talks about things that aren't even possible in Data Warehouse. What are they? --> </li> |

{style="table-layout:auto"}
