---
title: Gedeelde componenteditor
description: Maak of bewerk gedeelde afmetingen en maatstaven.
exl-id: 3f6a808a-d6ac-4a47-a5e2-63b9f17952e8
source-git-commit: f03c82375a907821c8e3f40b32b4d4200a47323f
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Gedeelde componenteditor

Met de gedeelde componenteditor kunt u gedeelde afmetingen en maateenheden maken of bewerken. Het deelt vele elementen UI wanneer [&#x200B; het creëren van of het uitgeven van een gegevensmening &#x200B;](/help/data-views/create-dataview.md), maar deze interfaces zijn verschillend in doel:

* Met de componenteditor voor gegevensweergave kunt u componenten maken en bewerken die specifiek zijn voor die gegevensweergave. U kunt geen gedeelde afmetingen of metriek in de de componentenredacteur van de gegevensmening uitgeven. In deze interface, kunnen de gedeelde dimensies en metriek door het pictogram van de a ![&#x200B; Gedeelde component &#x200B;](/help/assets/icons/CCLibrary.svg) naast de componentennaam worden geïdentificeerd.
* Met de gedeelde componenteditor kunt u gedeelde afmetingen en metriek maken en bewerken. U kunt geen componenten uitgeven die tot één enkele gegevensmening in de gedeelde componentenredacteur behoren.

{het screenshot van de redacteur van 0} Component ![&#128279;](assets/component-editor.png)

De rechterbovenhoek bevat drie knoppen:

* **[!UICONTROL Close]** of **[!UICONTROL Cancel]** : als alle wijzigingen zijn opgeslagen, sluit de knop **[!UICONTROL Close]** de editor. Als er niet-opgeslagen wijzigingen zijn, sluit u de editor met de knop **[!UICONTROL Cancel]** zonder deze wijzigingen op te slaan.
* **[!UICONTROL Save]**: hiermee slaat u alle componenten op en opent u de editor.
* **[!UICONTROL Save and finish]**: slaat alle componenten op en sluit de editor.

De interface bevat drie hoofdkolommen/secties:

* **de gebiedsselecteur van het Schema**: plaats van het gewenste schemagebied (s) en sleep hen aan het inbegrepen componentengebied.
   * **Verbinding**: De actieve verbinding. Verander de actieve verbinding in de [&#x200B; gedeelde metriek &amp; dimensiemanager &#x200B;](smd-overview.md).
   * **lijst van de Component**: U kunt tussen het selecteren [!UICONTROL Schema fields] (netto nieuwe gedeelde afmetingen en metriek), of [!UICONTROL Metrics & Dimensions] (bestaande gedeelde componenten) van het drop-down menu kiezen.
   * **Onderzoek**: Gebruik het ![&#x200B; pictogram van het Onderzoek &#x200B;](/help/assets/icons/Search.svg) tekstonderzoek om van het gewenste schemagebied of gedeelde component door naam de plaats te bepalen. U kunt ![&#128279;](/help/assets/icons/Filter.svg) filters van het pictogram van de Filter {ook gebruiken 0} om onderaan de lijst van componenten te versmallen.  Het filter `Is not deprecated` is standaard actief.
   * **creeer afgeleid gebied**: Staat u toe om [&#x200B; een afgeleid gebied &#x200B;](/help/data-views/derived-fields/derived-fields.md) tot stand te brengen.
* **omvatten componenten**: De componenten die u om vormt worden gedeeld. Wanneer u gedeelde componenten maakt, kunt u meerdere schemavelden naar dit gebied slepen om meerdere componenten tegelijk te maken. Wanneer u gedeelde componenten bewerkt, kunt u meerdere componenten selecteren die u wilt bewerken. Hierin worden alle geselecteerde componenten in dit gebied weergegeven.
* **montages van de Component**: Wanneer het selecteren van een component in het inbegrepen componentengebied, kunnen alle beschikbare montages in deze kolom worden gevormd. Zie [&#x200B; montages van de Component &#x200B;](/help/data-views/component-settings/overview.md) voor alle beschikbare opties voor afmetingen en metriek. Als u Shift ingedrukt houdt en op meerdere elementen klikt in het gebied Componenten, kunt u alle veelvoorkomende velden tegelijk bewerken.
