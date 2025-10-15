---
description: Leer hoe u presentaties in pptx-indeling kunt genereren op basis van Workspace-rapporten.
keywords: Analysis Workspace
title: Presentaties genereren op basis van Workspace-rapporten
feature: Curate and Share
role: User
hide: true
hidefromtoc: true
source-git-commit: 680799fdf18703acbd0569e25b41e6ecbc154d62
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Gegevensverhaal: presentaties genereren op basis van Workspace-rapporten {#generate-powerpoint}

U kunt .pptx-presentaties automatisch genereren van Analysis Workspace-projecten. Bij het genereren van presentaties identificeert Customer Journey Analytics automatisch belangrijke inzichten en zet deze om in dia&#39;s die klaar zijn voor gebruik door belanghebbenden.

Deze functionaliteit vermindert de tijd en moeite die nodig zijn om bevindingen uit uw Workspace-projecten te onthullen en stelt u in staat om snel verhalen van managers te maken en zakelijke impact te communiceren.

## Een .pptx-presentatie genereren op basis van een Workspace-project

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-powerpoint-include-visualizations"
>title="Opgenomen deelvensters en visualisaties"
>abstract="Kies de deelvensters en visualisaties die u in de presentatie wilt opnemen. U kunt maximaal 50 visualisaties opnemen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-presentation-emphasized-components"
>title="Gemarkeerde componenten"
>abstract="Kies maximaal 5 metriek en 5 dimensies van uw visualisaties die u in de presentatie wilt benadrukken. De maatstaven die u kiest, worden cursief weergegeven, de afmetingen worden vet weergegeven en de dimensie-items worden in een contrasterende kleur weergegeven."

<!-- markdownlint-enable MD034 -->

1. Ga naar het Workspace-project dat de gegevens bevat die u als basis voor uw presentatie wilt gebruiken.

1. Selecteer **[!UICONTROL Generate slides]** rechtsboven op de pagina.

1. Geef de volgende informatie op:

   | Optie | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Cover title]** | Geef een titel op voor de presentatie. Deze titel wordt weergegeven op de titeldia van de presentatie. |
   | **[!UICONTROL Include presenter name]** | Geef de naam van de presentator op. Deze naam wordt weergegeven op de titeldia van de presentatie, onder de titel van de omslag. |
   | **[!UICONTROL Panels and visualizations to include]** | Kies de deelvensters en de visualisatie die u in de presentatie wilt opnemen. U kunt maximaal 50 visualisaties opnemen.<p>De meeste deelvensters en visualisaties worden ondersteund. Voor informatie over niet gestaafde panelen en visualisatie, zie [&#x200B; Niet gestaafde projectelementen en eigenschappen &#x200B;](#unsupported-project-elements-and-features).</p> |
   | **[!UICONTROL Panel and visualization descriptions]** | |
   | **[!UICONTROL Annotations]** | |
   | **[!UICONTROL Emphasize components]** | Kies maximaal 5 metriek en 5 dimensies van uw visualisaties die u in de presentatie wilt benadrukken.<p>Wanneer geen nadruk wordt toegepast, tonen de componenten in presentaties als volgt:<ul><li>**Metriek en afmetingen:** Cursief</li><li>**de punten van Dimension:** Citatietekens</li></ul></p><p>Wanneer de nadruk wordt toegepast, tonen de componenten in presentaties als volgt:</p><ul><li>**Metriek en afmetingen:** Cursief en gewaagd</li><li>**de punten van Dimension:** Vet wanneer de overeenkomstige afmeting wordt benadrukt<p>Er wordt ook een kleur toegepast op het dimensie-item wanneer het dimensie-item in het diagram wordt gemarkeerd.</p></li></ul> |

(Voorwaardelijk) selecteer **[!UICONTROL Default theme]** als u uw dia&#39;s met het standaardthema wilt worden geproduceerd.

1. Selecteer of u een standaardthema wilt gebruiken of een aangepaste sjabloon wilt uploaden:

   * **[!UICONTROL Default theme]**:

   * **[!UICONTROL Upload template]**:





## Dia&#39;s uit een eerder gegenereerde presentatie bewerken


## Een gegenereerde .pptx-presentatie downloaden

## Niet-ondersteunde projectelementen en -functies {#unsupported}

De volgende Analysis Workspace-elementen en -functies die in een project worden gebruikt, worden niet ondersteund bij het genereren van dia&#39;s:

* Kenmerk, deelvenster

  Dit deelvenster wordt zo gedimd weergegeven wanneer de configuratieopties worden weergegeven.

  Alle andere panelen kunnen in dia&#39;s worden omvat die van een project van Workspace worden geproduceerd.

* Sommige visualisaties

  De meeste visualisaties kunnen in dia&#39;s worden omvat die van een project van Workspace worden geproduceerd. De volgende visualisaties kunnen echter niet worden opgenomen en worden weergegeven als grijs wanneer de configuratieopties worden weergegeven:

   * Cohortingtabel

   * Reiscanvas

   * Opsommingsteken

   * Combo

   * Spreiding

   * Treemap

* Uitsplitsingen

* Analyses met instructies


