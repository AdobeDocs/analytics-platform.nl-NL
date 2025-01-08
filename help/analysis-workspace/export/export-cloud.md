---
description: Leer hoe u een Analysis Workspace-project exporteert naar een locatie in de cloud.
keywords: Analysis Workspace
title: Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk
feature: Curate and Share
exl-id: 072eadcc-43ff-42e3-86ee-82062fa02eba
role: User
source-git-commit: 18a1cfcddfc8b2d1c70af57518c0b8d848b4ca5d
workflow-type: tm+mt
source-wordcount: '2226'
ht-degree: 1%

---

# Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk

U kunt volledige Workspace-tabellen exporteren vanuit Customer Journey Analytics en exporteren naar opgegeven cloudinstellingen.

Andere methodes om de rapporten van de Customer Journey Analytics uit te voeren zijn ook beschikbaar, zoals die in [ overzicht van de Uitvoer ](/help/analysis-workspace/export/export-project-overview.md) wordt beschreven.

## Volledige tabelexport begrijpen

U kunt volledige tabellen van Analysis Workspace naar cloudproviders exporteren, zoals Google, Azure, Amazon en Adobe.

[ Voordelen om volledige lijsten naar de wolk ](#advantages-of-exporting-to-the-cloud) uit te voeren omvatten de capaciteit om miljoenen rijen uit te voeren, berekende metriek, structuurgegevensoutput in samengevoegde waarden, en meer omvatten.

Houd rekening met het volgende wanneer u volledige tabellen exporteert:

* Alvorens u naar de wolk uitvoert, zorg ervoor dat uw lijsten, uw milieu, en uw toestemmingen aan de [ uitvoervereisten ](#export-requirements) voldoen.

* Sommige [ eigenschappen ](#unsupported-features) en [ componenten ](#unsupported-components) worden niet gesteund wanneer het uitvoeren van volledige lijsten aan de wolk.

Gebruik het volgende proces bij het exporteren van volledige tabellen naar de cloud:

1. [Een cloudaccount configureren](/help/components/exports/cloud-export-accounts.md)

1. [Een locatie op de account configureren](/help/components/exports/cloud-export-locations.md)

1. [Een volledige tabel exporteren vanuit Workspace](#export-full-tables-from-analysis-workspace)

1. [ gegevens van de Toegang in de wolk ](#view-exported-data-and-manifest-file) en [ leiden de uitvoer in Adobe ](/help/components/exports/manage-exports.md)

![ het volledige proces van de lijstuitvoer dat in stappen 1 door 4 wordt beschreven.](assets/export-full-table-process.png)

## Volledige tabellen exporteren vanuit Analysis Workspace

>[!NOTE]
>
>Alvorens u gegevens uitvoert zoals die in deze sectie worden beschreven, leer meer over de volledige lijstuitvoer in [ begrijpen volledige de lijstuitvoer ](#understand-full-table-export) sectie hierboven.

Volledige tabellen exporteren uit Analysis Workspace:

1. Als u niet reeds hebt, vorm een de uitvoerrekening en plaats, zoals die in [ wordt beschreven vormt de rekeningen van de wolkenuitvoer ](/help/components/exports/cloud-export-accounts.md).

1. Klik in Analysis Workspace met de rechtermuisknop op de tabel met vrije vorm die de gegevens bevat die u wilt exporteren.

1. Selecteer [!UICONTROL **Uitvoer volledige lijst**].

   ![ de vrije lijst van de Vrije vorm drop-down menu met de Uitvoer volledige benadrukte lijst.](assets/export-full-table.png)

1. In het [!UICONTROL **Nieuwe volledige de lijstuitvoer**] dialoogvakje, specificeer de volgende informatie:

   | Veldnaam | Functie |
   |---------|----------|
   | Naam | Geef een naam op voor het exporteren. Deze naam wordt weergegeven in de lijst Exporteren. |
   | Tags | U kunt een bestaande tag toepassen op de exportbewerking of u kunt een nieuwe tag maken en deze toepassen. <p>Als u een bestaande tag op het exporteren wilt toepassen, selecteert u de gewenste tags in het keuzemenu. Om het even welke markeringen in uw bedrijf zijn beschikbaar om <!-- double-check this --> toe te passen.</p> <p>Als u een nieuwe tag wilt maken, typt u de naam van de nieuwe tag en drukt u op Enter.</p><p>Houd rekening met het volgende wanneer u labels toepast op een exportbewerking: <ul><li>Tags die u toepast, kunnen in de exporttabel worden gefilterd of doorzocht.</li> <li>De markeringen die op een project worden toegepast worden niet automatisch toegepast wanneer het uitvoeren van een volledige lijst, zoals die in &quot;worden beschreven vormen kolommen op de de uitvoerpagina&quot;in [ worden beschreven leiden uitvoer ](/help/components/exports/manage-exports.md). (Alternatief, wanneer [ een volledig project voor de uitvoer ](/help/analysis-workspace/export/t-schedule-report.md) plant, worden om het even welke markeringen die op het project worden toegepast automatisch toegepast op de uitvoer.) <!-- Right now we don't have a column for them on the exports table, so this isn't true. Jaden is adding the column. --></li></ul> |
   | Beschrijving | Voeg een beschrijving toe aan het exporteren. U kunt verkiezen om beschrijvingen als kolom in de [ pagina van Uitvoer ](/help/components/exports/manage-exports.md) te bekijken wanneer het bekijken van de uitvoer. |
   | Gegevens, weergave | Selecteer de gegevensweergave met de componenten die u wilt opnemen in het exporteren. Het drop-down menu van de mening van Gegevens wordt gevestigd in de upper-left hoek van de dialoog en kan door het pictogram van de gegevensmening ![ het pictogram van de gegevensmening ](assets/data-view-icon.png) worden geïdentificeerd.  <p>**Nota:** als u een gegevensmening kiest die componenten mist die reeds inbegrepen in uw gegevenslijst zijn, dan wordt u ertoe aangezet om de gegevenslijst te ontruimen en het opnieuw te creëren gebruikend componenten die in de geselecteerde gegevensmening inbegrepen zijn. </p> |
   | Venster Opzoeken | Selecteer het rapporttijdkader dat u in elk exportbestand wilt opnemen. De opties omvatten [!UICONTROL **vandaag**], [!UICONTROL **Gisteren**], [!UICONTROL **Laatste 7 dagen**], [!UICONTROL **Laatste 30 dagen**], [!UICONTROL **Deze week**], en [!UICONTROL **Deze maand**]. <p>Deze optie wordt niet getoond wanneer de [!UICONTROL **frequentie van de Uitvoer**] aan [!UICONTROL **wordt geplaatst verzendt nu (eenmalig)**]. |
   | Gegevenstabel | Hiermee geeft u de tabel voor vrije vorm weer die u exporteert. U kunt de gegevenstabel wijzigen door componenten van het linkerpaneel naar de lijst te slepen. De tabel wordt dynamisch bijgewerkt terwijl u componenten toevoegt aan het canvas.  <p>Om het even welke segmenten die op de volledige lijst in het project werden toegepast verschijnen bij de bovenkant van elke individuele kolom in de lijst.</p> |
   | Wissen | Wist de inhoud van de gegevenstabel. Zo kunt u direct een nieuwe tabel maken in het dialoogvenster Nieuwe volledige tabel exporteren. |
   | Exportfrequentie | Stel het schema in voor hoe vaak het exporteren moet plaatsvinden. <p>U kunt kiezen [!UICONTROL **nu (eenmalig)**] verzenden om de uitvoer slechts eenmaal te verzenden. Wanneer u deze optie selecteert, wordt het exporteren onmiddellijk gestart.<p>U kunt er ook voor kiezen de exportbewerking volgens een bepaald schema te verzenden. Wanneer het verzenden op een programma, omvatten de opties [!UICONTROL **Dagelijks**], [!UICONTROL **wekelijks**], [!UICONTROL **Maandelijks tegen dag van de week**], [!UICONTROL **Maandelijks tegen dag van de maand**], [!UICONTROL **jaarlijks tegen dag van de maand**], en [!UICONTROL **jaarlijks tegen specifieke datum**]. </p><p>Houd rekening met het volgende wanneer u een exportfrequentie selecteert:</p><ul><li>De opties in het [!UICONTROL **venster van de Lookback**] gebied veranderen afhankelijk van wat u hier selecteert.<!-- if they're doing Daily, then we might not let them look back to the last year... --></li><li>Afhankelijk van de optie die u kiest, worden extra configuratievelden weergegeven.</li></ul> |
   | Starten bij | De dag en tijd waarop de geplande export moet beginnen. <p>Deze optie is alleen beschikbaar wanneer u een geplande exportfrequentie kiest.</p> |
   | Einde op | De dag en tijd waarop de geplande export verloopt. De geplande export wordt niet meer uitgevoerd na de datum en tijd die u instelt. <p>Deze optie is alleen beschikbaar wanneer u een geplande exportfrequentie kiest.</p> |
   | Bestandsindeling | Geef op of de geëxporteerde gegevens de indeling .csv of .json moeten hebben. |
   | Account | Selecteer de exportaccount voor de cloud waarin u de gegevens wilt verzenden. <p>Of als u nog geen cloudaccount hebt geconfigureerd die u wilt gebruiken, kunt u een nieuwe account configureren:<ol><li>Selecteer [!UICONTROL **toevoegen rekening**], dan specificeer de volgende informatie:<ul><li>[!UICONTROL **de rekeningsnaam van de Plaats**]: Specificeer een naam voor de plaatsrekening. Deze naam wordt weergegeven wanneer u een locatie maakt </li><li>[!UICONTROL **de rekeningsbeschrijving van de Plaats**]: Verstrek een korte beschrijving van de rekening helpen het van andere rekeningen van het zelfde rekeningtype onderscheiden.</li><li>[!UICONTROL **het type van Rekening**]: Selecteer het type van wolkenrekening u naar uitvoert. Beschikbare accounttypen zijn Amazon S3 Role ARN, Google Cloud Platform, Azure SAS, Azure RBAC, Snowflake en AEP Data Landing Zone.</li></ul><li>Om klaar te zijn met het vormen van uw rekening, ga met de verbinding hieronder die aan het [!UICONTROL **type van Rekening**] beantwoordt u selecteerde:<ul><li>[ AEP Gegevens het Landing Zone ](/help/components/exports/cloud-export-accounts.md#aep-data-landing-zone)</li><li>[ Amazon S3 Rol ARN ](/help/components/exports/cloud-export-accounts.md#amazon-s3-role-arn)</li><li>[ Google Cloud Platform ](/help/components/exports/cloud-export-accounts.md#google-cloud-platform)</li><li>[ Azure SAS ](/help/components/exports/cloud-export-accounts.md#azure-sas)</li><li>[ Azure RBAC ](/help/components/exports/cloud-export-accounts.md#azure-rbac)</li><li>[ Snowflake ](/help/components/exports/cloud-export-accounts.md#snowflake)</li></ul></ol> |
   | Locatienaam | Selecteer de locatie op de account waarnaar u de exportgegevens wilt verzenden.<p>Of, als u niet reeds de plaats hebt gevormd die u op de rekening wilt gebruiken die u selecteerde, kunt u een nieuwe plaats vormen:<ol><li>Selecteer [!UICONTROL **plaats**] toevoegen, dan specificeer de volgende informatie: <ul><li>[!UICONTROL **Naam**]: De naam van de plaats.</li><li>[!UICONTROL **Beschrijving**]: Verstrek een korte beschrijving van de plaats helpen het van andere plaatsen op de rekening onderscheiden.</li><li>[!UICONTROL **rekening van de Plaats**]: Selecteer de rekening waar u de plaats wilt tot stand brengen.</li></ul><li>Om uw plaats te beëindigen vormen, ga met de verbinding hieronder voort die aan het accounttype beantwoordt dat u op het [!UICONTROL **de rekening van de Plaats**] gebied selecteerde:<ul><li>[ AEP Gegevens die Zone ](/help/components/exports/cloud-export-locations.md#aep-data-landing-zone) aanvoeren.</li><li>[ Amazon S3 Rol ARN ](/help/components/exports/cloud-export-locations.md#amazon-s3-role-arn)</li><li>[ Google Cloud Platform ](/help/components/exports/cloud-export-locations.md#google-cloud-platform)</li><li>[ Azure SAS ](/help/components/exports/cloud-export-locations.md#azure-sas)</li><li>[ Azure RBAC ](/help/components/exports/cloud-export-locations.md#azure-rbac)</li><li>[ Snowflake ](/help/components/exports/cloud-export-locations.md#snowflake)</li></ul> |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**] om de uitvoer te bewaren.

   Gegevens worden verzonden naar de cloudaccount die u hebt opgegeven met de opgegeven frequentie.

1. (Facultatief) na u creeert de uitvoer, of u verkoos om het nu of op een bepaald programma te verzenden, kunt u het bekijken en beheren op de [ pagina van Uitvoer ](/help/components/exports/manage-exports.md) en het bekijken in de [ logboeken van de Uitvoer ](/help/components/exports/manage-export-logs.md).</p>

## Exporteren beheren

Nadat het gegeven van Analysis Workspace wordt uitgevoerd, kunt u uitgeven, opnieuw uitvoeren, dupliceren, markering, of bestaande uitvoer schrappen, zoals die in [ wordt beschreven beheert uitvoer ](/help/components/exports/manage-exports.md).

## Geëxporteerde gegevens en manifestbestand weergeven

### Geëxporteerde gegevens

De uitgevoerde gegevens zijn beschikbaar als gecomprimeerd dossier in de wolkenbestemming die u vormde, zoals die in [ wordt beschreven vormt wolkenuitvoerrekeningen ](/help/components/exports/cloud-export-accounts.md) en [ vormt wolkenuitvoerplaatsen ](/help/components/exports/cloud-export-locations.md).

De bestandsnaam van het gecomprimeerde bestand is als volgt, afhankelijk van of u CSV of JSON hebt gekozen als bestandsindeling:

* `cja-export-{reportInstanceId}-{idx}.csv.gz`

* `cja-export-{reportInstanceId}-{idx}.json.gz`

>[!NOTE]
>
>U kiest het dossierformaat in het [!UICONTROL **formaat van het Dossier**] gebied wanneer het uitvoeren van de lijst, zoals die in [ wordt beschreven Uitvoer volledige lijsten van Analysis Workspace ](#export-full-tables-from-analysis-workspace).

### Manifest-bestand

Een manifestbestand met de bestandsnaam `cja-export-{reportInstanceId}-{idx}.json.gz` wordt geleverd bij elke geslaagde exportlevering die ten minste één bestand bevat. Met het manifestbestand kunt u bevestigen dat alle bestanden zijn geleverd. Het bevat de volgende informatie:

* Een lijst met alle geleverde bestanden

* De MD5-controlesom van elk bestand

<!-- add in  what the file name, structure, and file format will be -->

## Voordelen van exporteren naar de cloud

Door gegevens van Customers Journey Analytics naar de cloud te exporteren, kunt u:

* Exporteer naar een gedeelde locatie, zoals Adobe Experience Platform Data Landing Zone, Google Cloud Platform, Microsoft Azure, Amazon S3 of Snowflake.

* Sla grote hoeveelheden historische gegevens op.

  Dit type van gegevens kan worden gebruikt om tendensen op lange termijn te ontdekken om bedrijfsintelligentie te bereiken, en uiteindelijk tot betere bedrijfsbesluitvorming te leiden.

* Exporteer volledige tabellen die duizenden of miljoenen rijen bevatten (3 miljoen, 30 miljoen, 150 miljoen of 300 miljoen rijen, afhankelijk van het type licentie). Met andere exportmethoden kunt u maximaal 50.000 rijen exporteren.

* Berekende metriek opnemen in de geëxporteerde gegevens van de Customer Journey Analytics.

* De gegevensoutput van de structuur als samengevoegde waarden.

* Eén keer of volgens een schema exporteren. (Ook beschikbaar met [ andere uitvoeropties ](/help/analysis-workspace/export/export-project-overview.md).)

* Bestanden exporteren in de CSV- of JSON-indeling. (Ook beschikbaar met [ andere uitvoeropties ](/help/analysis-workspace/export/export-project-overview.md).)

* Tabellen exporteren die meerdere afmetingen bevatten.

## Exportvereisten {#export-requirements}

### Minimumvereisten

Zorg ervoor dat uw lijsten, uw milieu, en uw toestemmingen aan de volgende vereisten voldoen:

* **Lijsten:** Alle lijsten moeten minstens één afmeting in de rij en één metrisch in elke kolom omvatten om met een full-table uitvoer te worden gesteund.

* **Milieu:** zorg ervoor dat de [ IP adressen ](/help/technotes/ip-addresses.md) en [ Domeinen ](/help/technotes/domains.md) die door Customer Journey Analytics worden gebruikt door de firewall van hun organisatie worden toegestaan.

* **Toestemmingen:** in Adobe Admin Console, moeten de gebruikers een productprofiel worden toegewezen dat de [!UICONTROL **Volledige die toestemming heeft van de Uitvoer van de Lijst**] aan het wordt toegewezen om volledige lijsten uit te voeren. Voor informatie over het toewijzen van een toestemming aan een productprofiel in de Admin Console, zie {de toestemming van de Customer Journey Analytics van 0} in Admin Console ](/help/technotes/access-control.md).[

  >[!NOTE]
  >
  >  De gebruikers die de [ rol van Admin van het Product ](/help/technotes/access-control.md#product-admin-role) worden toegewezen hebben altijd toegang tot de uitvoer volledige lijsten; deze gebruikers moeten niet worden toegewezen de [!UICONTROL **Volledige toestemming van de Uitvoer van de Lijst**].


### Niet-ondersteunde functies

De volgende functies worden niet ondersteund en worden automatisch verwijderd uit het exporteren van volledige tabellen:

* Percentage
* Totalen
* Zoeken, filteren
* Statische rijen
* Datum uitlijnen
* Dynamische afmetingen

  Voor meer informatie, zie [ Dynamische versus statische afmetingspunten in vrije vormlijsten ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md).
* Dimensionen in de eerste uitsplitsing worden omgezet en toegevoegd als een secundaire dimensie in de rij van de geëxporteerde tabel; andere uitsplitsingen worden niet in de tabel opgenomen
* Sorteren wordt niet ondersteund voor de meeste gegevenssets; gegevens kunnen worden gesorteerd voor kleine gegevenssets

### Niet-ondersteunde componenten

De volgende componenten worden niet ondersteund en Analysis Workspace vraagt u deze uit uw tabel te verwijderen wanneer u een volledige-tabelexport uitvoert:

* Berekende metriek die basis of geavanceerde functies in de metrische definitie gebruiken (zie [ Basisfuncties ](/help/components/calc-metrics/cm-functions.md) en [ Geavanceerde functies ](/help/components/calc-metrics/cm-adv-functions.md) voor meer informatie)
* De componenten die door een beheerder van worden uitgevoerd beperkt zijn (zie de *Filter op het beleid van de Overheid van Gegevens in gegevensmeningen* sectie in [ Etiketten en beleid ](/help/data-views/data-governance.md) voor meer informatie)
* Elke dimensie die aan alle volgende criteria voldoet:
   * Is gecreeerd van een gebied dat deel van een [ serie van voorwerpen ](/help/use-cases/object-arrays.md) uitmaakt (gelijkend op multi-waardevariabelen in Adobe Analytics)
   * Heeft [ toegelaten persistentie ](/help/data-views/component-settings/persistence.md)
   * Gebruikt niet a [ bindende afmeting ](/help/use-cases/data-views/binding-dimensions-metrics.md)
* De veelvoudige afmetingen die van gebieden zijn die verschillende [ series van voorwerpen ](/help/use-cases/object-arrays.md) van verwijzingen voorzien. (Meerdere afmetingen die verwijzen naar dezelfde array van objecten zijn toegestaan.)
* Meer dan 5 dimensies en 5 metriek per rapport (maximaal 5 dimensies en 5 metriek worden gesteund)
* In tabelkolommen:
   * Datumbereiken
   * Dimensies
* In tabelrijen:
   * Berekende cijfers
   * Metrics
   * Datumbereiken
   * Filters

### Attributiegedrag

De volledige lijstuitvoer steunt berekende metriek die een niet-standaardattributiemodel (zoals die in de *sectie van het niet-standaardattributiemodel van het Gebruik* in [ montages van de Kolom ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md) wordt beschreven) gebruiken.

Als een niet-gebrek attributiemodel in een rapport wordt gebruikt, wordt het toewijzingsmodel dat in het rapport wordt gebruikt of genegeerd, afhankelijk van of het rapport één enkele afmeting of veelvoudige dimensies heeft:

* **voor rapporten die metrische attributie in één enkele afmeting omvatten:** [ Metrische attributie ](/help/data-views/component-settings/attribution.md) treedt het [ toewijzingsmodel ](/help/data-views/component-settings/persistence.md) met voeten zoals normaal wanneer het gebruiken van metrische attributie.

  Een metrische kenmerk &quot;first touch&quot; heeft bijvoorbeeld voorrang op een &quot;meest recente&quot; dimensie-toewijzing.

* **voor rapporten die metrische attributie op veelvoudige dimensies tezelfdertijd omvatten:** [ Metrische attributie ](/help/data-views/component-settings/attribution.md) wordt toegepast naast het afmetings [ toewijzingsmodel ](/help/data-views/component-settings/persistence.md).

  Bijvoorbeeld, wordt een &quot;eerste aanraking&quot;metrische attributie toegepast naast een &quot;meest recente&quot;afmetingstoewijzing. Bovendien, zal de metrische attributie op post-toegewezen paren van afmetingspunten worden toegepast alsof zij één dimensiepunten waren, eerder dan op elk afmetingspunt onafhankelijk zoals normaal in een lijst Freeform wordt gedaan.

  >[!NOTE]
  >
  >Multidimensionale rapporten worden alleen ondersteund wanneer u gegevens exporteert naar de cloud, zoals in dit artikel wordt beschreven.

## Vergelijking van de volledige uitvoer van tabellen (in Customer Journey Analytics) naar Data Warehouse (in Adobe Analytics)

Als u eerder Data Warehouse hebt gebruikt om Adobe Analytics-gegevens te exporteren, kunt u met de volgende tabel de verschillen begrijpen tussen het exporteren van volledige tabellen in Customer Journey Analytics en het exporteren van gegevens met Data Warehouse in Adobe Analytics.


| Functie | Volledige tabelexport in Customer Journey Analytics | Data Warehouse in Adobe Analytics |
|---------|----------|---------|
| Een aangepast rapport maken | Ja | Ja |
| Berekende cijfers | Ja | Nee |
| Segmenten | Ja | Beperkt |
| Dimensies | Limiet van 5 | Onbeperkt |
| Metrics | Limiet van 5 | Onbeperkt |
| Rijen rapporteren | Limiet van 3 miljoen, 30 miljoen, 150 miljoen of 300 miljoen, afhankelijk van de omvang | Onbeperkt |
| Aantal rapporten | Onbeperkt | Onbeperkt |
| Ad hoc (eenmalige) levering | Ja | Ja |
| Terugkerende levering plannen | Ja | Ja |
| E-maillevering | Nee | Ja |
| FTP / SFTP | Nee | Verouderde ondersteuning |
| Azure | Ja | Ja |
| Amazon S3 | Ja | Ja |
| Google Cloud Platform | Ja | Ja |
| Snowflake | Ja | Nee |
| Leveringsfrequentie | Dagelijks | Uurlijks |
