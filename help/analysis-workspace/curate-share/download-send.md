---
description: U kunt opgeslagen en niet-opgeslagen projecten downloaden in PDF- en CSV-indeling.
title: PDF- of CSV-bestanden downloaden
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: tm+mt
source-git-commit: fc5a462f3d216d8cae3ce060a45ec79a44c4c918
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 3%

---


# PDF- of CSV-bestanden downloaden

>[!NOTE] U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U kunt opgeslagen en niet-opgeslagen projecten downloaden in PDF- en CSV-indeling.

De naam van het PDF- of CSV-bestand komt overeen met de huidige naam van het project. Voor niet-opgeslagen projecten bevat het gedownloade bestand de niet-opgeslagen wijzigingen in het project. Niet-opgeslagen projecten kunt u niet plannen in PDF of CSV.

Houd dit in gedachten:

* We ondersteunen ook de Fallout-visualisatie in CSV-indeling.
* Wanneer wij een project aan PDF teruggeven, geven wij enkel wat op de pagina is. Als een project visualisaties en deelvensters van aangepaste grootte heeft, moet u deze wijzigen om automatisch van grootte te zijn (knop in de rechterbovenhoek), zodat er geen afgekapte inhoud is.
* PDF&#39;s die in de browser worden gedownload, kunnen enkele minuten in beslag nemen om te worden geëxporteerd. Dit komt omdat we het hele project opnieuw moeten uitvoeren op onze servers voordat we het in PDF-indeling kunnen renderen. We raden u aan het project pas te laten nadat de PDF in uw browser is gedownload. U kunt echter wijzigingen in het project blijven aanbrengen terwijl u wacht.
* Als u zeer lange werkruimteprojecten hebt, worden PDF&#39;s momenteel geëxporteerd als één grote pagina in plaats van als een gepagineerd document. We werken aan een verbetering van de PDF-export naar Workspace die paginering mogelijk maakt.

1. Maak of open een project.
1. Klik op **[!UICONTROL Project]** > **[!UICONTROL Download CSV (or Download PDF).]**

Op 11 april 2019 zijn er verschillende wijzigingen aangebracht in het **[!CSV downloaden]** (en **[!Ckopiëren naar klembord]**) van Analysis Workspace om de opmaak van geëxporteerde gegevens te verwijderen.
* Het scheidingsteken voor duizendtallen wordt niet meer opgenomen. (Het decimale scheidingsteken blijft opgenomen en blijft in de indeling die onder **[!UICONTROL Components > Report Settings > Thousands Separator]**) is gedefinieerd.)
* Er worden geen valutasymbolen weergegeven.
* Er worden geen percentagesymbolen weergegeven.
* Percentages worden in decimale vorm uitgedrukt; Zo wordt 75% weergegeven als 0,75.
* Tijd wordt weergegeven in seconden.
* In kleurentabellen worden alleen onbewerkte waarden weergegeven. percentages worden verwijderd.
* Als een getal ongeldig is, wordt een lege cel weergegeven.

>[!NOpmerking:]
>
> Numerieke waarden die een komma als decimaalteken gebruiken, blijven in het geëxporteerde CSV-bestand worden vermeld.
