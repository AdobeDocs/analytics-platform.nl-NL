---
description: Meer informatie over Veelgestelde vragen over werkruimten en tips voor het oplossen van problemen.
title: Veelgestelde vragen
feature: FAQ
exl-id: d7233b26-9887-4b71-ad46-3c6ffe27d904
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 41%

---

# Veelgestelde vragen

| Vraag | Antwoord |
|--- |--- |
| **Wat zijn de eerste vereisten voor het gebruik van Analysis Workspace?** | Voor het gebruik van Analysis Workspace in Customer Journey Analytics is een werkende Customer Journey Analytics-implementatie vereist. Zorg ervoor dat uw organisatie gegevens naar de Adobe Experience Platform stuurt voordat u het hulpprogramma gebruikt. |
| **Wat zijn de vereisten inzake beheer en toegang voor Analysis Workspace?** | Zie [Beheervereisten](/help/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| **Heeft het gebruik van Analysis Workspace invloed op gegevensverzameling?** | Aangezien Analysis Workspace een rapportagetool is, heeft de tool geen invloed op de dataverzameling. U kunt componenten lukraak naar een project slepen om te zien wat er gebeurt, zonder negatieve gevolgen. Sleep verschillende combinaties van dimensies en metriek in uw werkruimteproject om te zien wat beschikbaar aan u is. Als u per ongeluk een ongeldige component naar uw Workspace-project sleept of een stap terug wilt gaan, drukt u op Ctrl + Z (Windows) of Cmd + Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door in het menu linksboven te klikken op *[!UICONTROL Project] > [!UICONTROL New]*. |
| **Hoe kan ik Analysis Workspace implementeren?** | Er is geen speciale implementatie vereist. Analysis Workspace is beschikbaar voor alle bedrijven die Customer Journey Analytics zijn. Nochtans, zijn de standaardtoestemmingen op inhoud (zoals projectcomponenten) van toepassing, en voor het leiden en het delen van projecten. Zie [Beheer- en toegangseisen](/help/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| **Hoe kan ik Analysis Workspace optimaliseren?** | Zie [Prestaties optimaliseren](/help/admin/optimizing-performance.md). |

## Problemen oplossen

**Wanneer ik een metric sleep, zie ik het bericht &quot;Ongeldige data&quot;.**

De melding &quot;Ongeldige data&quot; betekent dat Adobe geen data kan retourneren met de combinatie van dimensies en metrics die in het rapport wordt gebruikt. Zo kunnen twee metrics die boven op elkaar zijn gestapeld, niet als data worden geretourneerd, omdat er geen manier is om twee metrics op die manier weer te geven. Plaats de metriek in plaats daarvan naast elkaar.

**Wanneer ik een metric sleep, zie ik geen echte data - alleen maar nullen.**

Als u een werkruimterapport hebt gemaakt maar er geen gegevens zijn, kunt u een aantal dingen controleren:

* Als u een filter in uw rapport toepaste, zouden de filtercriteria geen gegevens kunnen aanpassen. Probeer het filter te verwijderen of de filterdefinitie aan te passen.
* Controleer de datumwaaier in de hogere juiste hoek en zorg ervoor het aan een waarde wordt geplaatst die u zou verwachten.
* Ga naar uw website en gebruik de [Foutopsporing](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) om te controleren of er gegevens worden verzameld.
