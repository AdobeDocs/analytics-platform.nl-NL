---
title: Experience Platform-soorten publiek analyseren in Customer Journey Analytics
description: Leer hoe u het Experience Platform-publiek in Customer Journey Analytics analyseert.
solution: Customer Journey Analytics
feature: Audiences
role: Admin
exl-id: 095cae34-1337-464a-9682-3c899295c0a8
source-git-commit: 4f1299595077a1756a6ad0c4f5ef5e0247ab4973
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Experience Platform-publiek in Customer Journey Analytics analyseren {#analyze-audiences-RTCDP}

Nadat u [ een configuratie van de publieksanalyse ](/help/connections/audience-analysis/audience-analysis-configure.md) creeert, worden de publieksgegevens beschikbaar als nieuwe dimensies in de gegevensmeningen waar u hen vormt om worden gecreeerd. U kunt de nieuwe publieksafmetingen overal in Analysis Workspace gebruiken als u toegang hebt tot een gegevensweergave waaraan de afmetingen voor de publieksanalyse zijn toegevoegd.

## De overzichtsjabloon Publiek gebruiken

Een overzichtsjabloon voor het publiek is beschikbaar in Customer Journey Analytics.

<!-- Can you also use the new audience dimensions in any project, regardless of whether it's a template? I assume so -->

<!-- What are the names of the new dimensions? Are they customized to whatever your audience names are in AEP, or are they always the same? Are they the dimensions available in the Audience overview template? (Audience Name, Audience Origin, Exited Audience Name, Exited Audience Origin; Audience Description, Exited Audience Description). Metrics included (Distinct Audiences) -->

Voor informatie over hoe te om tot het overzichtsmalplaatje van het Publiek toegang te hebben, zie [ Toegang en stel een malplaatje ](/help/analysis-workspace/templates/use-templates.md#access-and-run-a-template) in werking in [ malplaatjes van het Gebruik ](/help/analysis-workspace/templates/use-templates.md).

Het overzichtssjabloon Publiek bevat de volgende deelvensters:

## Overzicht van het gebruik

Hiermee worden gegevens weergegeven voor alle soorten publiek met gebruiksgebeurtenissen die aan de geselecteerde gegevensweergave zijn gekoppeld. Gegevens over het lidmaatschap van het publiek worden dagelijks bijgewerkt vanuit Experience Platform. Gegevens worden altijd weergegeven voor gisteren, dus als u het datumbereik van het deelvenster wijzigt, worden er onjuiste gegevens weergegeven.

Gebruik de tabel in dit deelvenster om het gedrag van het publiek beter te begrijpen. Sleep de dimensie Omschrijving van het publiek van de geselecteerde gegevensmening en voeg het als onderbreking toe. Of gebruik een andere interactiedimensie (zoals Pagina, Actie, enzovoort) als de indeling.

## Bovenste deelvenster voor reacties

Toont waar het publiek werd gecreeerd, of in RTCDP, Customer Journey Analytics, etc.

Gebruik de tabel in dit deelvenster om beter te begrijpen hoe de oorsprong van het publiek andere factoren kan beïnvloeden. Sleep de dimensie van de Naam van het publiek van de geselecteerde gegevensmening en voeg het als onderbreking toe. Of gebruik een andere interactiedimensie (zoals Pagina, Actie, enzovoort) als de indeling.

## Deelvenster Overlap van publiek

Hiermee worden gegevens weergegeven voor alle soorten publiek met gebruiksgebeurtenissen die aan de geselecteerde gegevensweergave zijn gekoppeld. Gegevens worden altijd weergegeven voor gisteren, dus als u het datumbereik van het deelvenster wijzigt, worden er onjuiste gegevens weergegeven.

Selecteer maximaal drie soorten publiek in de tabel in dit deelvenster om te zien hoe ze elkaar overlappen in het corresponderende Venn-diagram.

## Gebruiksvenster voor uitgesloten publiek

Toont gegevens voor alle verlaten publiek met gebruiksgebeurtenissen die met de geselecteerde gegevensmening worden geassocieerd. Gegevens worden altijd weergegeven voor gisteren, dus als u het datumbereik van het deelvenster wijzigt, worden er onjuiste gegevens weergegeven. &quot;Beëindigde doelgroepen&quot; zijn doelgroepen waarin mensen met gebruiksgebeurtenissen gisteren zijn vertrokken of verlaten.

Gebruik de tabel in dit deelvenster om het gedrag van het publiek beter te begrijpen. Sleep de dimensie Beschrijving van publiek verlaten van de geselecteerde gegevensmening en voeg het als onderbreking toe. Of gebruik een andere interactiedimensie of metrisch (zoals Pagina, Actie, enzovoort) als uitsplitsing.

## Bovenkant verlaten deelvenster voor publiek

Toont waar elk publiek dat verlaat oorspronkelijk werd gecreeerd, of in RTCDP, Customer Journey Analytics, etc.

Gebruik de tabel in dit deelvenster om beter te begrijpen hoe de oorsprong van het publiek andere factoren kan beïnvloeden. Sleep de Afmeting van de Naam van het Beëindigde publiek van de geselecteerde gegevensmening en voeg het als onderbreking toe. Of gebruik een andere interactiedimensie of metrisch (zoals Pagina, Actie, enzovoort) als uitsplitsing.
