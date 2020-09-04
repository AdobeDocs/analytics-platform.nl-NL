---
description: U kunt gegevens downloaden van Analysis Workspace door deze te kopiëren of in PDF- en CSV-indeling.
title: PDF- of CSV-bestanden downloaden
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: tm+mt
source-git-commit: 23856a744ce66ac03656d84f72b4bce4cdef253a
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 1%

---


# PDF- of CSV-bestanden downloaden vanuit Workspace

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset wijkt enigszins af van [Analysis Workspace in het traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Er zijn verschillende manieren waarop u gegevens uit Analysis Workspace kunt exporteren, afhankelijk van de gegevensset die u buiten het programma wilt analyseren en van de vraag wie de informatie moet ontvangen. Geëxporteerde gegevens kunnen de vorm hebben van gekopieerde gegevens, CSV- of PDF-bestanden. Een PDF heeft doorgaans de voorkeur als u visualisaties in het bestand wilt opnemen, terwijl een CSV (of gekopieerde gegevens) de voorkeur heeft als u gewoon gegevens zonder opmaak wilt.

>[!IMPORTANT]
>
> Sommige opties waarnaar op deze pagina wordt verwezen, zoals **Items als CSV downloaden**, momenteel in beperkte mate worden getest. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

## Project downloaden als CSV of PDF {#download-project}

U kunt een volledig project downloaden door naar **[!UICONTROL Project > Download as PDF (or as CSV)]**. Het gedownloade bestand bevat alle weergegeven (zichtbare) tabellen en visualisaties in het project. Een PDF heeft doorgaans de voorkeur als u visualisaties in het bestand wilt opnemen, terwijl een CSV-bestand de voorkeur heeft als u gewoon gegevens met normale tekst wilt.

![](assets/download-project.png)

Houd bij het downloaden van projecten rekening met:

* Het project kan worden opgeslagen of niet opgeslagen wanneer u een projectdownload aanvraagt. Alleen opgeslagen projecten kunnen echter worden [gepland](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/t-schedule-report.html).
* PDF-bestanden die in de browser worden gedownload, kunnen enkele minuten duren om te worden geëxporteerd, omdat het project opnieuw op Adobe-servers wordt uitgevoerd voordat het in PDF-indeling wordt gerenderd. We raden u aan het project pas te laten nadat de PDF in uw browser is gedownload. U kunt echter wijzigingen in het project blijven aanbrengen terwijl u wacht. Als een PDF langer dan 5 minuten duurt om te worden gerenderd, wordt u gevraagd om deze te e-mailen.
* PDF-downloads worden weergegeven als één pagina zonder paginering.
* Wanneer een project naar PDF wordt gerenderd, geven wij terug wat op de pagina is. Als een project visualisaties en deelvensters van aangepaste grootte heeft, moet u deze wijzigen om automatisch van grootte te zijn (knop in de rechterbovenhoek), zodat er geen afgekapte inhoud is.

## Gegevens kopiëren naar klembord (hotkey: Ctrl+C) {#copy-data}

De optie Klikken met rechtermuisknop **[!UICONTROL Copy to clipboard]** Hiermee kunt u snel gegevens uit Workspace kopiëren en elders plakken.

* Als u de weergegeven tabel wilt kopiëren, klikt u met de rechtermuisknop op de tabelkoptekst en kiest u **Gegevens naar klembord kopiëren**.
* Als u een subset van gegevens wilt kopiëren, maakt u een selectie in de tabel en klikt u met de rechtermuisknop > **Selectie naar klembord kopiëren**.

Daarnaast is de hotkey `Ctrl+C` Hiermee kopieert u de selectie naar het klembord. Nadat u de gegevens hebt gekopieerd, kunt u naar een ander gereedschap gaan en deze plakken (of op `Ctrl+V`).

![](assets/copy-selection.png)

## Gegevens downloaden als CSV {#download-data}

De optie Klikken met rechtermuisknop **[!UICONTROL Download data as CSV]** kunt u een gegevenslijst of de gegevensbron van om het even welke visualisatie als CSV downloaden.

* Klik met de rechtermuisknop in de koptekst van een tabel of visualisatie **[!UICONTROL Download data as CSV]**. Dit downloadt de getoonde gegevens in de lijst of de onderliggende gegevensbron voor visualisatie als CSV. Opmerking: Deze optie wordt niet ondersteund door de Kaartweergave.
* Als een selectie in de tabel wordt gemaakt, wordt de optie **[!UICONTROL Download selection as CSV]**. Alleen de selectie wordt met deze optie gedownload, in tegenstelling tot de volledige weergegeven tabel.

![](assets/download-data-viz.png)

## Items als CSV downloaden {#download-items}

Als u meer dan de zichtbare 400 rijen gegevens in een lijst wilt analyseren, klik de lijstkopbal of om het even welke rij met de rechtermuisknop aan en selecteer **Items downloaden als CSV (naam Dimension)**. Met deze optie kunt u maximaal 50.000 dimensieitems (op basis van de tabelsortering) exporteren voor de geselecteerde dimensie, met toegepaste filters en segmenten. Als u deze optie boven aan de tabel kiest, wordt de eerste afmeting in de tabel geëxporteerd. Hoewel er geen limieten gelden in de vrije-vormtabel, wordt aanbevolen de optie Items downloaden te gebruiken in tabellen met minder dan 20 kolommen om optimale prestaties te garanderen.

>[!TIP]
>
> Als uw afmeting groter is dan 50.000 items, downloadt u het bestand met verschillende maateenheden of past u een filter toe. U kunt bijvoorbeeld in één download aflopend sorteren op Bezoek en in een tweede download oplopend sorteren op Bezoek. Deze tip kan u helpen langer-staart punten terugwinnen.

U kunt meerdere taken uitvoeren binnen het project en zelfs naar een nieuw Workspace-project navigeren op hetzelfde tabblad terwijl de download bezig is. Het downloaden wordt onderbroken als u een nieuw browsertabblad opent. Het downloaden wordt geannuleerd als u Workspace volledig verlaat of het browsertabblad sluit.

![](assets/download-items.png)

### Bestand met gedownloade items

De functies van de tabel worden als volgt op het gedownloade bestand toegepast:

* Alle deelvenstersegmenten worden als filters toegepast.
* Uitsplitsingen **boven** de geselecteerde afmeting in de tabel wordt toegepast als filters boven elke kolom.
* Uitsplitsingen **onder** de geselecteerde afmeting in de tabel wordt verwijderd.

In het bovenstaande voorbeeld worden pagina-items gedownload met het deelvenstersegment (Nieuwe bezoekers) en de bovenstaande componenten (Marketing Channel = e-mail) toegepast als filters, en worden de onderliggende componenten (Type mobiel apparaat) verwijderd uit de gedownloade CSV.

![](assets/downloaded-file.png)

### Meldingen downloaden

Terwijl het bestand wordt gedownload, wordt een informatieve melding over de voortgang weergegeven. U kunt de download op elk gewenst moment annuleren door op **[!UICONTROL Cancel download]**. De toast sluiten **niet** het downloaden annuleren.

Nadat het bestand is voltooid, wordt een voltooiingsbericht weergegeven en wordt het bestand naar uw browser gedownload.

Als u meer dan één download tegelijk aanvraagt, ontvangt u een melding dat elke extra download in de wachtrij wordt geplaatst totdat de vorige download is voltooid.

![](assets/toast.png)

## Veelgestelde vragen {#faq}

| Vraag | Antwoord |
| --- | --- |
| Waarom is mijn gedownloade PDF één pagina? | De gedownloade PDF&#39;s worden momenteel niet door de werkruimte gepagineerd. |
| Kan ik meer dan 50.000 items exporteren met de optie Items downloaden als CSV? | Terwijl elke download tot 50.000 afmetingspunten kan bevatten, kunt u het soort van uw lijst veranderen om langere eindpunten terug te winnen, of een filter toepassen om specifiekere punten te downloaden. |
| Wat doet **[!UICONTROL Copy visualization]** doen? | **[!UICONTROL Copy visualization]** is geen exportoptie. Hiermee kunt u een visualisatie of een deelvenster van de ene plaats in Workspace naar de andere kopiëren. Bijvoorbeeld, van één paneel aan een andere in het zelfde project, of van één project aan een ander project. [De video bekijken](https://www.youtube.com/watch?v=lvmAdKNfWQw) |

