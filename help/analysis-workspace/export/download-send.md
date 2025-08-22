---
description: Meer informatie over de verschillende mogelijkheden om gegevens te downloaden van uw Analysis Workspace-project.
title: Projecten en gegevens downloaden
feature: Curate and Share
exl-id: 1d8384ca-888c-482c-ab3e-d1b579217560
role: User
source-git-commit: 1cb9e18f79e8ca49b63aa7d8117ce6c61a020454
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# Projecten en gegevens downloaden

U kunt Analysis Workspace-projecten en -gegevens downloaden naar uw lokale apparaat. Deze download kan gegevens, een CSV-bestand (door komma&#39;s gescheiden gegevens) of een PDF-document (Portable Document Format) zijn.

* Selecteer de optie PDF als u visualisaties wilt opnemen in het gedownloade bestand.
* Selecteer de CSV en gekopieerde gegevensopties als u eenvoudig gegevens zonder opmaak nodig hebt.

De extra methodes om de gegevens van Customer Journey Analytics uit te voeren worden beschreven in het [ overzicht van de Uitvoer ](/help/analysis-workspace/export/export-project-overview.md).

## Een project downloaden als PDF- of CSV-bestand {#download-project}

![ het drop-down menu van het Project met de benadrukte opties van CSV van de Download en van PDF van de Download.](assets/download-project.png)

### Een project downloaden als PDF-bestand

Houd rekening met het volgende wanneer u een project downloadt als een PDF:

* Laat het project pas over nadat het project naar het werkstation is gedownload. Het downloaden kan enkele minuten duren, aangezien het project opnieuw wordt uitgevoerd op Adobe-servers, zodat de PDF kan renderen. U kunt wijzigingen in het project blijven aanbrengen terwijl het downloaden wordt uitgevoerd. Als een PDF langer dan 5 minuten duurt om terug te geven, wordt u ertoe aangezet om [ PDF ](../curate-share/send-schedule-files.md) in plaats daarvan te e-mailen.
* Downloads worden weergegeven als één pagina zonder paginering.
* De PDF bevat wat zichtbaar is op de browserpagina in Analysis Workspace. Om afgekapte inhoud te vermijden, uitgezocht ![ vergroot ](/help/assets/icons/Resize.svg) aan auto-grootte om het even welke douane-gerangschikte visualisaties of panelen.
* [ Hyperlinks ](/help/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md) binnen vrije vormlijsten zijn klikbaar in gedownloade PDF.

Een project downloaden als een PDF-bestand:

1. Selecteer **[!UICONTROL Project]** > **[!UICONTROL Download PDF]** .

   Een groene bar wordt getoond met het volgende bericht: ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Your download has been requested. Please wait.]**

1. Zodra uw download klaar is, verschijnt een groene bar met het volgende bericht: ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL *Naam van het project *PDF is klaar.]**

1. Selecteer **[!UICONTROL Download]** op de groene balk.

   Afhankelijk van uw browserinstellingen wordt de PDF automatisch gedownload naar de map die u eerder hebt geconfigureerd, of wordt u gevraagd een map te kiezen waarin de PDF wordt gedownload.

   De dossier - naam wordt samengesteld uit *projectnaam* - *naam van de rapportreeks* - *datum*. Bijvoorbeeld `Example Project - Omni-Channel - Luma - Jun 30, 2025.pdf` .

### Een project downloaden als een CSV-bestand

1. Selecteer **[!UICONTROL Project]** > **[!UICONTROL Download CSV]** .

   Afhankelijk van de browserinstellingen wordt het CSV-bestand automatisch gedownload naar een map die u eerder hebt geconfigureerd, of wordt u gevraagd een map te kiezen waarin het CSV-bestand wordt gedownload.

   De dossier - naam wordt samengesteld uit *projectnaam* - *naam van de rapportreeks* - *datum*. Bijvoorbeeld `Example Project - Omni-Channel - Luma - Jun 30, 2025.csv` .

## Gegevens in een visualisatie kopiëren naar het klembord {#copy-data}

Met de optie **[!UICONTROL Copy to clipboard]** in het contextmenu kunt u snel gegevens van Analysis Workspace kopiëren en de gegevens in een hulpprogramma van derden plakken.

* Als u de getoonde lijstgegevens wilt kopiëren, selecteer de lijstkopbal en selecteer **gegevens van het Exemplaar aan klembord** van het contextmenu.
* Als u een ondergroep van de gekopieerde gegevens wilt, maak een selectie in de lijst en selecteer **selectie van het Exemplaar aan klembord** van het contextmenu.

>[!TIP]
>
>U kunt hotkey **_gebruiken cmd + c_** (macOS) of **_ctrl + c_** (Vensters) om uw selectie aan het klembord te kopiëren. Dan gebruik **_cmd + v_** (macOS) of **_ctrl + v_** (Vensters) om de gegevens te kleven.


![ de selectie van het Exemplaar aan klembordoptie. ](assets/copy-clipboard.png){zoomable="yes"}

## Gegevens downloaden in een visualisatie als CSV-bestand {#download-data}

Met de download als CSV-opties in het contextmenu kunt u een gegevenslijst of de gegevensbron van een visualisatie als CSV downloaden.

Daartoe:

* Selecteer **[!UICONTROL Download data as CSV]** in het contextmenu in de koptekst van een tabel of visualisatie. Dit downloadt de getoonde gegevens in de lijst of de onderliggende gegevensbron voor visualisatie als CSV.

<!-- Only relevant as soon as CJA supports Map visualization 
  >[!NOTE]
  >
  >  Note: the Map visualization does not support this option.
-->

* Selecteer **[!UICONTROL Download selection as CSV]** in het contextmenu in een tabel. Alleen de selectie wordt met deze optie gedownload, in tegenstelling tot de volledige weergegeven tabel.

![ de gegevens van de Download als optie CSV.](assets/download-data-as-csv.png)

## Items downloaden als een CSV-bestand {#download-items}

Als u meer dan de zichtbare 400 rijen van gegevens in een lijst wilt analyseren, de uitgezochte **punten van de Download als CSV (_naam van Dimension_)** van het contextmenu van de lijstkopbal of om het even welke rij. Met deze optie exporteert u maximaal 50.000 dimensieitems (op basis van de tabelsortering) voor de geselecteerde dimensie, met sorteeropties en toegepaste filters. Als u deze optie boven aan de tabel selecteert, wordt de eerste afmeting in de tabel geëxporteerd.

![ de punten van de Download als CSV (Pagina) optie.](assets/download-items-as-csv.png)

Geen grenzen worden afgedwongen in de freeform lijst. Om optimale prestaties te garanderen, wordt aanbevolen deze optie te gebruiken in tabellen met minder dan 20 kolommen.

>[!TIP]
>
> Als uw afmeting meer dan 50.000 items bevat, downloadt u het bestand met verschillende maateenheden of past u een segment toe. U kunt bijvoorbeeld in één download aflopend sorteren op Bezoek en in een tweede download oplopend sorteren op Bezoek. Deze tip kan u helpen langer-staart punten terugwinnen.

U kunt meerdere taken uitvoeren in het project en zelfs naar een nieuw Workspace-project navigeren op hetzelfde tabblad terwijl het downloaden wordt uitgevoerd. Het downloaden wordt onderbroken als u een nieuw browsertabblad opent. Het downloaden wordt geannuleerd als u Workspace volledig verlaat of het browsertabblad sluit.


### Bestand met gedownloade items {#items-file}

De volgende functies van een vrije-vormtabel worden toegepast op het gedownloade bestand:

* Alle deelvenstersegmenten worden als filters toegepast.
* De onderbrekingen **boven** de geselecteerde afmeting in de lijst worden toegepast als filters boven elke kolom.
* De onderbrekingen **onder** worden de geselecteerde afmeting in de lijst verwijderd.

![ het gedownloade.csv- dossier dat in Excel wordt geopend.](assets/download-items-file.png)

### Meldingen downloaden {#notifications}

Terwijl het bestand wordt gedownload, worden de volgende meldingen weergegeven:

* Een blauwe **[!UICONTROL _naam van de Lijst _-_ Dimension _.csv is gevraagd._ x _% volledig]**&#x200B;die op de vooruitgang wijzen. Selecteer **[!UICONTROL Cancel download]**&#x200B;als u het downloaden wilt annuleren. Selecteer ![ CrossSize100 ](/help/assets/icons/CrossSize100.svg) als u het bericht wilt sluiten, dat niet de download annuleert.
* Een groene **[!UICONTROL _naam van de Lijst _-_ Dimension _.csv is gedownload]**&#x200B;voltooiingsbericht zodra de dossierdownload wordt voltooid. Het bestand wordt gedownload naar de downloadmap die voor uw browser is geconfigureerd.

Als u meer dan één download tegelijk aanvraagt, ontvangt u een melding dat elke extra download in de wachtrij wordt geplaatst totdat de vorige download is voltooid.


## Gevoelige gegevens downloaden {#sensitive}

Stel zich het beleid van het a [ gegevensbeheer ](/help/data-views/data-governance.md) voor dat de download van gegevens verhindert. En dat dit beleid is ingeschakeld in de gegevensweergave waarop u rapporteert. Als gevolg hiervan worden bij het downloaden (bijvoorbeeld wanneer u PDF-bestanden e-mailt of deelt) van projecten de gegevensvelden gemarkeerd als gevoelig. In Analysis Workspace kunt u deze velden nog steeds analyseren. Als u een project probeert te e-mailen of op een andere manier te delen, worden de gevoelige gegevensvelden als leeg weergegeven in het PDF- of CSV-bestand.

Als gegevensvelden met het label Gevoelig in de gegevensweergave worden opgenomen, is de optie voor het selecteren en kopiëren van gegevens van het scherm beperkt voor alle gegevens in de gegevensweergave.

## Veelgestelde vragen {#faq}

| Vraag | Antwoord |
| --- | --- |
| Waarom bestaat mijn gedownloade PDF uit slechts één pagina? | De [ functionaliteit van de Download PDF ](#download-as-csv-or-pdf) pagineert gedownloade PDFs niet. |
| Kan ik meer dan 50.000 items exporteren met de optie **[!UICONTROL Download items as CSV]** ? | Terwijl elke download tot 50.000 afmetingspunten kan bevatten, kunt u het soort van uw lijst veranderen om langere eindpunten terug te winnen, of een filter toepassen om specifiekere punten te downloaden. |
| Wat doet **[!UICONTROL Copy visualization]**? | In tegenstelling tot [!UICONTROL **gegevens van het Exemplaar aan klembord**] of [!UICONTROL **selectie van het Exemplaar aan klembord**], is de **[!UICONTROL Copy visualization]** optie van het contextmenu geen uitvoeroptie. Deze optie staat u toe om een visualisatie [ te kopiëren of ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu) een paneel [ van één plaats in Workspace aan een andere te kopiëren. ](/help/analysis-workspace/c-panels/panels.md#context-menu) Bijvoorbeeld van het ene naar het andere deelvenster in hetzelfde project of van het ene naar het andere project. |
