---
title: Veelgestelde vragen over attributie
description: Antwoorden op veelgestelde vragen over attributie.
feature: Attribution
exl-id: 3153d8c9-4ca8-4189-8a2f-511a87e8ac17
source-git-commit: c36dddb31261a3a5e37be9c4566f5e7ec212f53c
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 6%

---

# Veelgestelde vragen over attributie

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset wijkt enigszins af van [Analysis Workspace in het traditionele Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

**Wat is het regelitem &quot;Geen&quot; wanneer u een kenmerk gebruikt?**

Het regelitem Geen is een catch-all-item dat alle conversies vertegenwoordigt die zonder aanraakpunten in het terugzoekvenster zijn uitgevoerd. Probeer een langer tijdbereik op te nemen in het rapportvenster.

**Waarom zie ik soms data buiten mijn rapporteringsvenster wanneer het gebruiken van attributiemodellen?**

Deze extra datums zijn het gevolg van het terugzoekvenster van de bezoeker. Zie [Gegevens buiten rapportagevenster](https://helpx.adobe.com/analytics/kb/data-appearing-outside-reporting-window.html) in de KB Analytics voor meer informatie. Adobe is van plan om deze extra rijen in een aanstaande versie uit te filteren.

**Wanneer moet ik een terugzoekopdracht voor bezoekerskenmerk gebruiken?**

De keuze van de terugzoekfunctie voor attributie hangt af van het gebruikte geval. Als conversies doorgaans langer duren dan één bezoek, wordt het aangeraden een bezoeker terug te zoeken. Het maken van een gegevensweergave met een definitie voor een langer bezoek is ook een mogelijke oplossing.

**Hoe vergelijken props en eVars wanneer het gebruiken van attributie?**

Attribution wordt opnieuw berekend tijdens de runtime van het rapport, zodat er geen verschil is tussen een prop of eVar (of een andere dimensie) voor attributiemodellering. Props kunnen blijven bestaan met een terugzoekvenster of een toewijzingsmodel en instellingen voor eVar-toewijzing/vervaldatum worden genegeerd.

**Welke afmetingen en metriek worden niet gesteund?**

Het deelvenster Kenmerken ondersteunt alle afmetingen. Niet-ondersteunde meetgegevens zijn:

* Unieke bezoekers
* Bezoeken
* Voorvallen
* Paginaweergaven
* A4T-meetwaarden
* Metrische tijdwaarden
* Bounces
* Stuitpercentage
* Geopend
* Gesloten
* Pagina&#39;s niet gevonden
* Zoekopdrachten
* Bezoeken van één pagina
* Eenmalige toegang

**Hoe werkt attributie met filters?**

Attributie wordt altijd uitgevoerd voordat filters worden toegepast en globale filters worden uitgevoerd voordat andere rapportfilters worden toegepast.
