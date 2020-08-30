---
description: Veelgestelde vragen over Workspace
title: Veelgestelde vragen en werkruimte voor probleemoplossing
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 42%

---


# Veelgestelde vragen

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

| Vraag | Antwoord |
|--- |--- |
| Wat zijn de eerste vereisten voor het gebruiken van de Werkruimte van de Analyse? | Het gebruiken van de Werkruimte van de Analyse vereist een werkende implementatie van de Analyse van de Reis van de Klant. Zorg ervoor uw organisatie gegevens naar het Platform van de Ervaring van Adobe alvorens het hulpmiddel verzendt te gebruiken. |
| Wat zijn het Beleid en de toegangsvereisten voor de Werkruimte van de Analyse? | Zie [Beheervereisten](/help/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Zal het gebruiken van de Werkruimte van de Analyse gegevensinzameling beïnvloeden? | Aangezien Analysis Workspace een rapportagetool is, heeft de tool geen invloed op de dataverzameling. U kunt componenten lukraak naar een project slepen om te zien wat er gebeurt, zonder negatieve gevolgen. Sleep verschillende combinaties van dimensies en metrics naar uw Workspace-project om te zien wat er beschikbaar is. Als u per ongeluk een ongeldige component naar uw Workspace-project sleept of een stap terug wilt gaan, drukt u op Ctrl + Z (Windows) of Cmd + Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door in het menu linksboven te klikken op *[!UICONTROL Project] > [!UICONTROL New]*. |
| Hoe voert u de Werkruimte van de Analyse uit? | Er is geen speciale uitvoering nodig. De Werkruimte van de analyse is beschikbaar aan alle Analytics van de Reis van de BedrijfsKlant. Nochtans, zijn de standaardtoestemmingen aan inhoud (zoals projectcomponenten) van toepassing, en voor het krullen van en het delen van projecten. Zie [Beheer- en toegangsvereisten](/help/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Hoe kan ik de prestaties van de Werkruimte van de Analyse optimaliseren? | Zie [Prestaties optimaliseren](/help/analysis-workspace/workspace-faq/optimizing-performance.md). |

## Problemen oplossen

**Wanneer ik een metric sleep, zie ik het bericht &quot;Ongeldige data&quot;.**

De melding &quot;Ongeldige data&quot; betekent dat Adobe geen data kan retourneren met de combinatie van dimensies en metrics die in het rapport wordt gebruikt. Zo kunnen twee metrics die boven op elkaar zijn gestapeld, niet als data worden geretourneerd, omdat er geen manier is om twee metrics op die manier weer te geven. In plaats daarvan, plaats de metriek zij aan zij.

**Wanneer ik een metric sleep, zie ik geen echte data - alleen maar nullen.**

Als u met succes een werkruimterapport creeerde maar er geen gegevens zijn, zijn er een paar dingen u kunt controleren:

* Controleer de rapportreeks tweemaal en zorg ervoor het met gegevens wordt bevolkt.
* Als u een segment in uw rapport toepaste, zouden de segmentcriteria geen gegevens kunnen aanpassen. Verwijder het segment of pas de segmentdefinitie aan.
* Controleer de datumwaaier in de hogere juiste hoek en zorg ervoor het aan een waarde wordt geplaatst die u zou verwachten.
* Navigeer aan uw website en gebruik [Foutopsporing](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html) om te bevestigen dat gegevens worden verzameld.