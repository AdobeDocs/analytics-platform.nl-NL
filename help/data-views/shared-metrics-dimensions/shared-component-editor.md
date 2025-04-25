---
title: Gedeelde componenteditor
description: Maak of bewerk gedeelde afmetingen en maatstaven.
source-git-commit: d2c6605cc440c293aca279c1583bac964055d277
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Gedeelde componenteditor

Met de gedeelde componenteditor kunt u gedeelde afmetingen en maateenheden maken of bewerken. Het deelt vele elementen UI wanneer [ het creëren van of het uitgeven van een gegevensmening ](/help/data-views/create-dataview.md), maar deze interfaces zijn verschillend in doel:

* Met de componenteditor voor gegevensweergave kunt u componenten maken en bewerken die specifiek zijn voor die gegevensweergave. U kunt geen gedeelde afmetingen of metriek in de de componentenredacteur van de gegevensmening uitgeven. In deze interface, kunnen de gedeelde dimensies en metriek door het pictogram van de a ![ Gedeelde component ](/help/assets/icons/CCLibrary.svg) naast de componentennaam worden geïdentificeerd.
* Met de gedeelde componenteditor kunt u gedeelde afmetingen en metriek maken en bewerken. U kunt geen componenten uitgeven die tot één enkele gegevensmening in de gedeelde componentenredacteur behoren.

{het screenshot van de redacteur van 0} Component ](assets/component-editor.png)![

De rechterbovenhoek bevat drie knoppen:

* **[!UICONTROL Close]** of **[!UICONTROL Cancel]** : als alle wijzigingen zijn opgeslagen, sluit de knop **[!UICONTROL Close]** de editor. Als er om het even welke niet bewaarde veranderingen zijn, sluit de ** [!UICONTROL Cancel] knoop de redacteur zonder die veranderingen op te slaan.
* **[!UICONTROL Save]**: hiermee slaat u alle componenten op en opent u de editor.
* **[!UICONTROL Save and finish]**: slaat alle componenten op en sluit de editor.

De interface bevat drie hoofdkolommen/secties:

* **de gebiedsselecteur van het Schema**: plaats van het gewenste schemagebied (s) en sleep hen aan het inbegrepen componentengebied.
   * **Verbinding**: De actieve verbinding. Verander de actieve verbinding in de [ gedeelde metriek &amp; dimensiemanager ](smd-overview.md).
   * **drop-down van de Lijst van de Component**: U kunt tussen het selecteren [!UICONTROL Schema fields] (netto nieuwe gedeelde afmetingen en metriek), of [!UICONTROL Metrics & Dimensions] (bestaande gedeelde componenten) kiezen.
   * **Onderzoek**: Gebruik het ![ pictogram van het Onderzoek ](/help/assets/icons/Search.svg) tekstonderzoek om van het gewenste schemagebied of gedeelde component door naam de plaats te bepalen. U kunt ](/help/assets/icons/Filter.svg) filters van het pictogram van de Filter {ook gebruiken 0} om onderaan de lijst van componenten te versmallen. ![ Het filter `Is not deprecated` is standaard actief.
   * **creeer afgeleid gebied**: Staat u toe om [ een afgeleid gebied ](/help/data-views/derived-fields/derived-fields.md) tot stand te brengen.
* **omvatten componenten**: De componenten die u om vormt worden gedeeld. Wanneer u gedeelde componenten maakt, kunt u meerdere schemavelden naar dit gebied slepen om meerdere componenten tegelijk te maken. Wanneer u gedeelde componenten bewerkt, kunt u meerdere componenten selecteren die u wilt bewerken. Hierin worden alle geselecteerde componenten in dit gebied weergegeven.
* **montages van de Component**: Wanneer het selecteren van een component in het inbegrepen componentengebied, kunnen alle beschikbare montages in deze kolom worden gevormd. Zie [ montages van de Component ](/help/data-views/component-settings/overview.md) voor alle beschikbare opties voor afmetingen en metriek. Als u Shift ingedrukt houdt en op meerdere elementen klikt in het gebied Componenten, kunt u alle veelvoorkomende velden tegelijk bewerken.
