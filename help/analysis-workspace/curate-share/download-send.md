---
description: U kunt opgeslagen en niet-opgeslagen projecten downloaden in PDF- en CSV-indelingen.
title: PDF- of CSV-bestanden downloaden
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: tm+mt
source-git-commit: 387e9755d963e70a9ba8dbc5f1f01f83541b5511
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 3%

---


# PDF- of CSV-bestanden downloaden

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U kunt opgeslagen en niet-opgeslagen projecten downloaden in PDF- en CSV-indelingen.

De naam van het PDF- of CSV-bestand komt overeen met de huidige naam van het project. Voor unsaved projecten, omvat het gedownloade dossier de unsaved veranderingen in het project. Merk op dat u niet unsaved projecten in PDF of CSV kunt plannen.

Houd dit in gedachten:

* Wij steunen ook de Fallout visualisatie in CSV formaat.
* Wanneer wij een project aan PDF teruggeven, geven wij enkel wat op de pagina is. Als een project douane-gerangschikte visualisaties en panelen heeft, moet u hen veranderen om auto-gerangschikt (knoop in hoogste juiste hoek) te zijn zodat er geen beknot inhoud zal zijn.
* PDFs die in browser wordt gedownload kan verscheidene notulen vergen om uit te voeren. Dit is omdat wij het volledige project op onze servers moeten opnieuw in werking stellen alvorens het in formaat terug te geven PDF. Wij adviseren niet het verlaten van het project tot PDF in uw browser downloadt. Nochtans, kunt u blijven veranderingen in het project aanbrengen terwijl u wacht.
* Wij zijn ons ervan bewust dat als u zeer lange werkruimteprojecten hebt, PDFs momenteel als één reuzenpagina, eerder dan als gepagineerd document uitvoert. Wij werken aan een verbetering aan de uitvoer van de Werkruimte PDF die voor paginering zal toestaan.

1. Creeer of open een project.
1. Klik op **[!UICONTROL Project]** > **[!UICONTROL Download CSV (or Download PDF).]**

Op 11 april 2019 werden verschillende wijzigingen aangebracht in **[!CSV downloads]** en **[!Copy to Clipboard]**) uit de Werkruimte van de Analyse om het formatteren uit uitgevoerde gegevens te verwijderen.
* De duizenden separator is niet meer inbegrepen. (Het decimale scheidingsteken blijft inbegrepen, en zal aan het formaat houden dat onder wordt bepaald **[!UICONTROL Components > Report Settings > Thousands Separator]**).
* Er worden geen valutasymbolen weergegeven.
* Geen percentensymbolen worden getoond.
* Percentages zijn in decimale vorm; Zo wordt 75% weergegeven als 0,75.
* De tijd wordt getoond in seconden.
* De Lijsten van de cohort tonen ruwe slechts waarden; percentages worden verwijderd.
* Als een aantal ongeldig is, wordt een lege cel getoond.

>[!NOTE]
>
>De numerieke waarden die een komma als decimaalteken gebruiken zullen in uitgevoerde CSV blijven worden geciteerd.
