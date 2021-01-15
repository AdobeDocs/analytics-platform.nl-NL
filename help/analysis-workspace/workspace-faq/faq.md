---
description: Veelgestelde vragen over Workspace
title: Veelgestelde vragen
translation-type: tm+mt
source-git-commit: 3dc9d0d0a1f65a4205120895c35aa508f080c25d
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 43%

---


# Veelgestelde vragen

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

| Vraag | Antwoord |
|--- |--- |
| Wat zijn de eerste vereisten voor het gebruik van Analysis Workspace? | Voor het gebruik van Analysis Workspace is een werkende Customer Journey Analytics-implementatie vereist. Zorg ervoor dat uw organisatie gegevens naar de Adobe Experience Platform stuurt voordat u het hulpprogramma gebruikt. |
| Wat zijn de vereisten inzake beheer en toegang voor Analysis Workspace? | Zie [Beheervereisten](/help/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Heeft het gebruik van Analysis Workspace invloed op gegevensverzameling? | Aangezien Analysis Workspace een rapportagetool is, heeft de tool geen invloed op de dataverzameling. U kunt componenten lukraak naar een project slepen om te zien wat er gebeurt, zonder negatieve gevolgen. Sleep verschillende combinaties van dimensies en metrics naar uw Workspace-project om te zien wat er beschikbaar is. Als u per ongeluk een ongeldige component naar uw Workspace-project sleept of een stap terug wilt gaan, drukt u op Ctrl + Z (Windows) of Cmd + Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door in het menu linksboven te klikken op *[!UICONTROL Project] > [!UICONTROL New]*. |
| Hoe implementeert u Analysis Workspace? | Er is geen speciale implementatie vereist. Analysis Workspace is beschikbaar voor alle bedrijven Customer Journey Analytics. Nochtans, zijn de standaardtoestemmingen op inhoud (zoals projectcomponenten) van toepassing, en voor het leiden en het delen van projecten. Zie [Vereisten voor beheer en toegang](/help/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Hoe kan ik de prestaties van Analysis Workspace optimaliseren? | Zie [Prestaties optimaliseren](/help/analysis-workspace/workspace-faq/optimizing-performance.md). |

## Problemen oplossen

**Wanneer ik een metric sleep, zie ik het bericht &quot;Ongeldige data&quot;.**

De melding &quot;Ongeldige data&quot; betekent dat Adobe geen data kan retourneren met de combinatie van dimensies en metrics die in het rapport wordt gebruikt. Zo kunnen twee metrics die boven op elkaar zijn gestapeld, niet als data worden geretourneerd, omdat er geen manier is om twee metrics op die manier weer te geven. Plaats de metriek in plaats daarvan naast elkaar.

**Wanneer ik een metric sleep, zie ik geen echte data - alleen maar nullen.**

Als u een werkruimterapport hebt gemaakt maar er geen gegevens zijn, kunt u een aantal dingen controleren:

* Controleer de rapportreeks tweemaal en zorg ervoor het met gegevens wordt bevolkt.
* Als u een segment in uw rapport toepaste, zouden de segmentcriteria geen gegevens kunnen aanpassen. Verwijder het segment of pas de segmentdefinitie aan.
* Controleer de datumwaaier in de hogere juiste hoek en zorg ervoor het aan een waarde wordt geplaatst die u zou verwachten.
* Navigeer naar uw website en gebruik [Foutopsporing](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html) om te controleren of de gegevens worden verzameld.