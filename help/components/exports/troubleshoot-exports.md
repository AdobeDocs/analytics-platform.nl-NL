---
description: Logboeken beheren voor bestaande exportbewerkingen
keywords: Analysis Workspace
title: Problemen met mislukte exportbewerkingen oplossen
feature: Components
hide: true
hidefromtoc: true
source-git-commit: a2b2c6bca0557521ac7b6bcf635f467ca41731b7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Problemen met mislukte exportbewerkingen oplossen

Wanneer u [volledige tabellen exporteren van Analysis Workspace naar cloudinstellingen](/help/analysis-workspace/export/export-cloud.md)kunt u de status van deze exportbewerkingen bekijken vanuit de [Exporteren, tabblad](/help/components/exports/manage-exports.md) en van de [Tabblad Logs](/help/components/exports/manage-export-logs.md). Uit mislukte exportbewerkingen blijkt de status van [!UICONTROL **Mislukt**].

## Veelvoorkomende fouten en handelingen

Exporteren kan om verschillende redenen mislukken. In de volgende tabel worden enkele van de meest voorkomende redenen beschreven, met acties die u kunt uitvoeren om de fouten te verhelpen:

| Reden voor mislukking | Voorgestelde actie | Meer informatie |
|---------|----------|---------|
| Ongeldige locatie- of accountgegevens | Zorg ervoor dat uw gegevens en andere gegevens correct zijn voor het cloudaccount en de locatie waarnaar u exporteert. | [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md) en [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md). |
| Een afmeting of metrisch in het rapport werd verwijderd uit de gegevensmening | Neem contact op met de systeembeheerder om te zien welke componenten uit de gegevensweergave zijn verwijderd. Mogelijk moet u een andere gegevensweergave gebruiken bij het exporteren of componenten uit de tabel verwijderen die niet meer beschikbaar zijn. | [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md) |
| Een beleid van het gegevensbeheer dat door uw organisatie wordt afgedwongen beperkt componenten in uw lijst van worden uitgevoerd | Neem contact op met de systeembeheerder om te zien welke componenten niet mogen worden geëxporteerd. Verwijder de beperkte componenten voordat u gaat exporteren. | *Filter op beleid voor gegevensbeheer in gegevensweergaven* sectie in [Labels en beleid](/help/data-views/data-governance.md) |

## Contact opnemen met de Adobe Klantenservice

Als u problemen blijft ondervinden, neemt u contact op met de klantenservice van de Adobe. Wanneer u contact opneemt met de klantenservice voor een mislukte export, moet u de volgende informatie beschikbaar hebben:

* Exportnaam

* Id exporteren

* Instantie-id

* Naam gegevensweergave

* Locatie

* Account

* Bedrijfsnaam

* Verbinding

* Gegevens