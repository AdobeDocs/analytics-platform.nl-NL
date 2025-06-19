---
description: Leer hoe u berekende metriek maakt.
title: Berekende waarden maken
feature: Calculated Metrics
exl-id: 55ed36c1-99ca-400a-bc2b-661994cbf720
source-git-commit: b3c7ceedec7b3f6a916e97bab38fd55f1d6c7f51
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Berekende waarden maken

Standaard kunnen alleen beheerders berekende metriek maken. Gebruikers hebben rechten om berekende metriek weer te geven, vergelijkbaar met de manier waarop gebruikers andere componenten (zoals segmenten, annotaties en meer) weergeven.

Nochtans, kunnen de beheerders de **[!UICONTROL Calculated Metric Creation]** toestemming voor **[!UICONTROL Reporting Tools]** in **[!UICONTROL Edit permissions for CJA Workspace Access]** aan gebruikers via [ Admin Console ](/help/technotes/access-control.md#user-level-access) geven.


U kunt op de volgende manieren een berekende metrische waarde maken:

![ Manieren om metrisch ](assets/create-metric.png) te creëren

* **A**. Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer **[!UICONTROL Calculated metrics]** . Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) [!UICONTROL **[!UICONTROL Add]**] van de [[!UICONTROL Calculated metrics] manager ](/help/components/calc-metrics/cm-workflow/cm-manager.md).
* **B**. In een project van Workspace, van het linkerpaneel van Componenten, voegt de uitgezochte ![ ](/help/assets/icons/Add.svg) bij ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Metriek** toe.
* **C**. Selecteer **[!UICONTROL Create metric from selection]** in een Workspace-project in het contextmenu in de kolomkop Metrics. In het submenu kunt u een functie selecteren of **[!UICONTROL Open in calculated metric builder]** selecteren. <br/> als u een functie selecteert, wordt berekende metrisch bepaald als project-slechts metrisch. Wanneer u later dit metrisch uitgeeft, door [ Info van de Component ](/help/components/use-components-in-workspace.md#component-info) popup, ziet u een bericht in de [ Berekende metrische bouwer ](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md).
* **D**. Selecteer in een Workspace-project **[!UICONTROL Components]** in het menu en selecteer **[!UICONTROL Create metric]** .
* **E**. In een Workspace-project gebruikt u de sneltoets **[!UICONTROL shift+cmd+c]** (macOS) of **[!UICONTROL shift+ctrl+c]** (Windows).

Om nieuwe berekende metrisch te bepalen, gebruikt u [ Berekende metrische bouwer ](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md).


## Workflow

Overweeg de volgende workflow voordat u berekende metriek maakt:

| Werkstroomtaak | Beschrijving |
| --- | --- |
| Berekende meetwaarden plannen | Met name voor metriek die officieel &quot;goedgekeurd&quot; zal worden, is het zinvol om te schetsen welke berekende meetwaarden op grote schaal zullen worden gebruikt en hoe ze zullen worden gedefinieerd. |
| [ bouwt ](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md) berekende metriek | U kunt berekende en geavanceerde berekende maatstaven maken en bewerken voor gebruik in [!DNL Customer Journey Analytics] -componenten. |
| ](cm-tagging.md) berekende metriek van de markering 0}[ | Berekende maatstaven voor eenvoudige organisatie en delen. Zie hoe u labels kunt plannen en toewijzen voor eenvoudige en geavanceerde zoekopdrachten en organisatie. |
| [ keur ](cm-approving.md) berekende metriek goed | Goedkeuren van berekende maatstaven om deze canonicaal te maken. |
| Berekende meetwaarden gebruiken | Gebruik de berekende metriek in uw projecten. |
| [ Deel ](cm-sharing.md) berekende metriek | Deel uw berekende metriek met andere individuen, groepen, of organisaties. |
| ](cm-filter.md) berekende metriek van de Filter 0} {[ | Filter berekende metriek op markeringen, eigenaars, en andere filters (toon allen, Mijne, Gedeeld met me, Favorieten, en Goedgekeurd.) |
| Markeer berekende metriek als [ favorieten ](cm-finding.md) | Metrische gegevens als favorieten markeren is een andere manier om ze te ordenen voor gebruiksgemak. |

