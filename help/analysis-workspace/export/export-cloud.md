---
description: Exporteer een Analysis Workspace-project naar een locatie in de cloud.
keywords: Analysis Workspace
title: Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk
feature: Curate and Share
hide: true
hidefromtoc: true
source-git-commit: eb7ba8dd7809164bdcddb0d484754376d5b7ca9e
workflow-type: tm+mt
source-wordcount: '1612'
ht-degree: 2%

---

# Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk

U kunt volledige tabellen van Workspace vanuit Customer Journey Analytics exporteren en exporteren naar opgegeven cloud-doelen.

Er zijn ook andere methoden beschikbaar voor het rapporteren van Customer Journey Analytics-exporteurs, zoals beschreven in [Overzicht van exporteren](/help/analysis-workspace/export/export-project-overview.md).

## Volledige tabellen exporteren vanuit Analysis Workspace

>[!NOTE]
>
>Voordat u gegevens exporteert zoals beschreven in deze sectie, moet u controleren of de tabel voldoet aan de [Exportvereisten](#export-requirements).

Volledige tabellen exporteren uit Analysis Workspace:

1. Indien u dit nog niet hebt gedaan, configureert u een exportaccount en -locatie, zoals beschreven in [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md).

1. Klik in Analysis Workspace met de rechtermuisknop op de tabel met vrije vorm die de gegevens bevat die u wilt exporteren.

1. Selecteren [!UICONTROL **Volledige tabel exporteren**].

   ![volledige tabel exporteren](assets/export-full-table.png)

1. In de [!UICONTROL **Nieuwe volledige tabelexport**] geeft u de volgende informatie op:

   | Veldnaam | -functie |
   |---------|----------|
   | Naam | Geef een naam op voor het exporteren. Deze naam wordt weergegeven in de lijst Exporteren. |
   | Tags | U kunt een bestaande tag toepassen op de exportbewerking of u kunt een nieuwe tag maken en deze toepassen. <p>Als u een bestaande tag op het exporteren wilt toepassen, selecteert u de gewenste tags in het keuzemenu. Alle tags in uw bedrijf kunnen worden toegepast<!-- double-check this -->.</p> <p>Als u een nieuwe tag wilt maken, typt u de naam van de nieuwe tag en drukt u op Enter.</p><p>Houd rekening met het volgende wanneer u labels toepast op een exportbewerking: <ul><li>Tags die u toepast, kunnen in de exporttabel worden gefilterd of doorzocht.</li> <li>De markeringen die op een project worden toegepast worden niet automatisch toegepast wanneer het uitvoeren van een volledige lijst, zoals die in &quot;worden beschreven vormen kolommen op de de uitvoerpagina&quot;in [Exporteren beheren](/help/components/exports/manage-exports.md). (Alternatief, wanneer [een volledig project voor exporteren plannen](/help/analysis-workspace/export/t-schedule-report.md), worden alle tags die op het project zijn toegepast, automatisch toegepast op het exporteren.)  <!-- Right now we don't have a column for them on the exports table, so this isn't true. Jaden is adding the column. --></li></ul> |
   | Beschrijving | Voeg een beschrijving toe aan het exporteren. U kunt beschrijvingen als een kolom weergeven in het dialoogvenster [Pagina exporteren](/help/components/exports/manage-exports.md) bij het weergeven van exportbewerkingen. |
   | Gegevens, weergave | Selecteer de gegevensweergave met de componenten die u wilt opnemen in het exporteren. Het vervolgkeuzemenu in de weergave Gegevens bevindt zich in de linkerbovenhoek van het dialoogvenster en kan worden geïdentificeerd door het pictogram van de gegevensweergave![pictogram gegevensweergave](assets/data-view-icon.png).  <p>**Opmerking:** Als u een gegevensweergave kiest waarin componenten ontbreken die al in de gegevenstabel zijn opgenomen, wordt u gevraagd de gegevenstabel te wissen en opnieuw te maken met gebruik van componenten die in de geselecteerde gegevensweergave zijn opgenomen. </p> |
   | Venster Opzoeken | Selecteer het rapporttijdkader dat u in elk exportbestand wilt opnemen. Opties omvatten [!UICONTROL **Vandaag**], [!UICONTROL **Gisteren**], [!UICONTROL **Laatste 7 dagen**], [!UICONTROL **Laatste 30 dagen**], [!UICONTROL **Deze week**], en [!UICONTROL **Deze maand**]. |
   | Wissen | Wist de inhoud van de gegevenstabel. Zo kunt u direct een nieuwe tabel maken in het dialoogvenster Nieuwe volledige tabel exporteren. |
   | Exportfrequentie | Stel het schema in voor hoe vaak het exporteren moet plaatsvinden. <p>U kunt [!UICONTROL **Nu verzenden (één keer)**] om de export slechts eenmaal te verzenden. Wanneer u deze optie selecteert, wordt het exporteren onmiddellijk gestart.<p>U kunt er ook voor kiezen de exportbewerking volgens een bepaald schema te verzenden. Bij verzending volgens een schema omvatten de opties: [!UICONTROL **Dagelijks**], [!UICONTROL **Wekelijks**], [!UICONTROL **Maandelijks op dag van de week**], [!UICONTROL **Maandelijks op dag van de maand**], [!UICONTROL **Jaarlijks op dag van de maand**], en [!UICONTROL **Jaarlijks op specifieke datum**]. </p><p>Houd rekening met het volgende wanneer u een exportfrequentie selecteert:</p><ul><li>De opties in het dialoogvenster [!UICONTROL **Venster Opzoeken**] het veld wordt gewijzigd, afhankelijk van wat u hier selecteert.<!-- if they're doing Daily, then we might not let them look back to the last year... --></li><li>Afhankelijk van de optie die u kiest, worden extra configuratievelden weergegeven.</li></ul> |
   | Starten bij | De dag en tijd waarop de geplande export moet beginnen. <p>Deze optie is alleen beschikbaar wanneer u een geplande exportfrequentie kiest.</p> |
   | Einde op | De dag en tijd waarop de geplande export verloopt. De geplande export wordt niet meer uitgevoerd na de datum en tijd die u instelt. <p>Deze optie is alleen beschikbaar wanneer u een geplande exportfrequentie kiest.</p> |
   | Bestandsindeling | Geef op of de geëxporteerde gegevens de indeling .csv of .json moeten hebben. |
   | Account | Selecteer de exportaccount voor de cloud waarin u de gegevens wilt verzenden. <p>Zie voor meer informatie [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md).</p> |
   | Locatienaam | Selecteer de locatie op de account waarnaar u de exportgegevens wilt verzenden. <p>Zie voor meer informatie [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md).</p><p>U kunt de [!UICONTROL **Nieuwe locatie toevoegen**] om een nieuwe locatie voor een bestaande exportaccount te maken. |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**] om het exporteren op te slaan.

   Gegevens worden verzonden naar de cloudaccount die u hebt opgegeven met de opgegeven frequentie.

1. (Optioneel) Nadat u de exportbewerking hebt gemaakt, kunt u de bewerking nu of volgens een bepaald schema weergeven en beheren in het dialoogvenster [Pagina exporteren](/help/components/exports/manage-exports.md) en bekijk het in de [Logboeken exporteren](/help/components/exports/manage-export-logs.md).</p>

## Voordelen van exporteren naar de cloud

Door gegevens van Customers Journey Analytics naar de cloud te exporteren, kunt u:

* Exporteer naar een gedeelde locatie, zoals Adobe Experience Platform Data Landing Zone, Google Cloud Platform, Microsoft Azure, Amazon S3 of Snowflake.

* Sla grote hoeveelheden historische gegevens op.

  Dit type van gegevens kan worden gebruikt om tendensen op lange termijn te ontdekken om bedrijfsintelligentie te bereiken, en uiteindelijk tot betere bedrijfsbesluitvorming te leiden.

* Exporteer volledige tabellen die duizenden of miljoenen rijen bevatten. Met andere exportmethoden kunt u maximaal 50.000 rijen exporteren.

* Berekende metriek opnemen in de geëxporteerde gegevens van de Customer Journey Analytics.

* De gegevensoutput van de structuur als samengevoegde waarden.

* Exporteer ad hoc of volgens een schema. (Ook beschikbaar bij [andere exportopties](/help/analysis-workspace/export/export-project-overview.md).)

* Bestanden exporteren in de CSV- of JSON-indeling. (Ook beschikbaar bij [andere exportopties](/help/analysis-workspace/export/export-project-overview.md).)

* Tabellen exporteren die meerdere afmetingen bevatten.

## Exportvereisten {#export-requirements}

### Minimumvereisten

Tabellen moeten minstens één dimensie in de rij en één metrische dimensie in elke kolom bevatten om met een volledig-lijstuitvoer te worden gesteund.

De beheerders zouden ervoor moeten zorgen dat de IP adressen in [IP adressen die door Customer Journey Analytics worden gebruikt](/help/admin/ip-addresses.md) zijn inbegrepen in de firewall lijst van gewenste personen.

### Niet-ondersteunde functies

De volgende functies worden niet ondersteund en worden automatisch verwijderd uit het exporteren van volledige tabellen:

* Percentage
* Totalen
* Zoeken, filteren
* Statische rijen
* Datum uitlijnen
* Dynamische afmetingen

  Zie voor meer informatie [Dynamische versus statische dimensie-items in vrije-vormtabellen](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md).
* Dimensionen in de eerste uitsplitsing worden omgezet en toegevoegd als een secundaire dimensie in de rij van de geëxporteerde tabel; andere uitsplitsingen worden niet in de tabel opgenomen
* Sorteren wordt niet ondersteund voor de meeste gegevenssets; gegevens kunnen worden gesorteerd voor kleine gegevenssets

### Niet-ondersteunde componenten

De volgende componenten worden niet ondersteund en Analysis Workspace vraagt u deze uit uw tabel te verwijderen wanneer u een volledige-tabelexport uitvoert:

* Berekende metriek die geavanceerde functies in metrische definitie gebruiken (zie [Geavanceerde functies](/help/components/calc-metrics/cm-adv-functions.md) voor meer informatie )
* Componenten die door een beheerder zijn beperkt van export (zie de *Filter op beleid voor gegevensbeheer in gegevensweergaven* sectie in [Labels en beleid](/help/data-views/data-governance.md) voor meer informatie )
* Meer dan 5 dimensies en 5 metriek per rapport (maximaal 5 dimensies en 5 metriek worden gesteund)
* In tabelkolommen:
   * Datumbereiken
   * Dimensies
* In tabelrijen:
   * Berekende standaarden
   * Metrics
   * Datumbereiken
   * Filters

### Attributiegedrag

Volledige tabelexport ondersteunt berekende maateenheden die een niet-standaard toewijzingsmodel gebruiken (zoals beschreven in het dialoogvenster *Niet-standaard toewijzingsmodel gebruiken* sectie in [Kolominstellingen](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)).

Als een niet-gebrek attributiemodel in een rapport wordt gebruikt, wordt het toewijzingsmodel dat in het rapport wordt gebruikt of genegeerd, afhankelijk van of het rapport één enkele afmeting of veelvoudige dimensies heeft:

* **Voor rapporten die metrische attributie in één enkele afmeting omvatten:** [Metrische kenmerk](/help/data-views/component-settings/attribution.md) overschrijft de [toewijzingsmodel](/help/data-views/component-settings/persistence.md) zoals gewoonlijk bij het gebruiken van metrische attributie.

  Een metrische kenmerk &quot;first touch&quot; heeft bijvoorbeeld voorrang op een &quot;meest recente&quot; dimensie-toewijzing.

* **Voor rapporten die metrische attributie op veelvoudige dimensies tezelfdertijd omvatten:** [Metrische kenmerk](/help/data-views/component-settings/attribution.md) wordt toegepast naast de dimensie [toewijzingsmodel](/help/data-views/component-settings/persistence.md).

  Bijvoorbeeld, wordt een &quot;eerste aanraking&quot;metrische attributie toegepast naast een &quot;meest recente&quot;afmetingstoewijzing. Bovendien, zal de metrische attributie op post-toegewezen paren van afmetingspunten worden toegepast alsof zij één dimensiepunten waren, eerder dan op elk afmetingspunt onafhankelijk zoals normaal in een lijst Freeform wordt gedaan.

  >[!NOTE]
  >
  >Multidimensionale rapporten worden alleen ondersteund wanneer u gegevens exporteert naar de cloud, zoals in dit artikel wordt beschreven.

## Exporteren beheren

Nadat gegevens uit Analysis Workspace zijn geëxporteerd, kunt u bestaande exportbewerkingen bewerken, opnieuw exporteren, dupliceren, labelen of verwijderen, zoals wordt beschreven in [Exporteren beheren](/help/components/exports/manage-exports.md).

## Geëxporteerde gegevens en manifestbestand weergeven

### Geëxporteerde gegevens

Geëxporteerde gegevens zijn beschikbaar als een gecomprimeerd bestand in de cloudbestemming die u hebt geconfigureerd, zoals beschreven in [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md) en [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md).

De bestandsnaam van het gecomprimeerde bestand is als volgt, afhankelijk van of u CSV of JSON hebt gekozen als bestandsindeling:

* `cja-export-{reportInstanceId}-{idx}.csv.gz`

* `cja-export-{reportInstanceId}-{idx}.json.gz`

>[!NOTE]
>
>U kiest de bestandsindeling in het dialoogvenster [!UICONTROL **Bestandsindeling**] veld bij het exporteren van de tabel, zoals beschreven in [Volledige tabellen exporteren vanuit Analysis Workspace](#export-full-tables-from-analysis-workspace).

### Manifest-bestand

Een manifestbestand met een bestandsnaam van `cja-export-{reportInstanceId}-{idx}.json.gz` wordt meegeleverd bij elke succesvolle exportlevering die ten minste één bestand bevat. Met het manifestbestand kunt u bevestigen dat alle bestanden zijn geleverd. Het bevat de volgende informatie:

* Een lijst met alle geleverde bestanden

* De grootte van elk bestand

* De tijdstempel van elk bestand

<!-- add in  what the file name, structure, and file format will be -->

## Vergelijking van de volledige uitvoer van tabellen (in Customer Journey Analytics) naar Data Warehouse (in Adobe Analytics)

Als u eerder Data Warehouse hebt gebruikt om Adobe Analytics-gegevens te exporteren, kunt u met de volgende tabel de verschillen begrijpen tussen het exporteren van volledige tabellen in Customer Journey Analytics en het exporteren van gegevens met Data Warehouse in Adobe Analytics.


| Functie | Volledige tabelexport in Customer Journey Analytics | Data Warehouse in Adobe Analytics |
|---------|----------|---------|
| Een aangepast rapport maken | Ja | Ja |
| Berekende standaarden | Ja | Nee |
| Segmenten | Ja | Beperkt |
| Dimensies | Limiet van 5 | Onbeperkt |
| Metrics | Limiet van 5 | Onbeperkt |
| Rijen rapporteren | Limiet van 3 miljoen, 30 miljoen, 150 miljoen of 300 miljoen, afhankelijk van de omvang | Onbeperkt |
| Aantal rapporten | Onbeperkt | Onbeperkt |
| Ad hoc levering | Ja | Ja |
| Terugkerende levering plannen | Ja | Ja |
| E-maillevering | Nee | Ja |
| FTP / SFTP | Nee | Verouderde ondersteuning |
| Azure | Ja | Ja |
| Amazon S3 | Ja | Ja |
| Google Cloud Platform | Ja | Ja |
| Snowflake | Ja | Nee |
| Leveringsfrequentie | Dagelijks | Uurlijks |
