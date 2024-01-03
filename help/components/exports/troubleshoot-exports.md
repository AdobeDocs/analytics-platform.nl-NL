---
description: Logboeken beheren voor bestaande exportbewerkingen
keywords: Analysis Workspace
title: Problemen met mislukte exportbewerkingen oplossen
feature: Components
exl-id: fbc25150-4390-40a2-9f17-aadf254258ad
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '390'
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
| Rijlimiet overschreden | Afhankelijk van het type licentie kunt u maximaal 3 miljoen, 30 miljoen, 150 miljoen of 300 miljoen rijen exporteren. Werk de tabel die u exporteert bij om het aantal rijen te verminderen. | [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md) |
| Geplande exportvervaldatum | De geplande export die u hebt geconfigureerd, is verlopen. De vervaldatum van het exporteren bijwerken. | [Exporteren beheren](/help/components/exports/manage-exports.md) |
| Dimension niet ondersteund | <p>Elke dimensie die aan alle volgende criteria voldoet, wordt niet ondersteund in Volledige tabelexport:</p> <ul><li>Is gemaakt van een veld dat deel uitmaakt van een array van objecten</li><li>Heeft persistentie ingeschakeld<li>Gebruikt geen bindende dimensie</li> | <ul><li>[Arrays van objecten gebruiken](/help/use-cases/object-arrays.md)</li><li>[Instellingen voor persistentiecomponenten](/help/data-views/component-settings/persistence.md)<li>[Bindingsafmetingen en metriek gebruiken in Customer Journey Analytics](/help/use-cases/data-views/binding-dimensions-metrics.md)</li> |
| Een beleid van het gegevensbeheer dat door uw organisatie wordt afgedwongen beperkt componenten in uw lijst van worden uitgevoerd | Neem contact op met de systeembeheerder om te zien welke componenten niet mogen worden geëxporteerd. Verwijder de beperkte componenten voordat u gaat exporteren. | *Filter op beleid voor gegevensbeheer in gegevensweergaven* sectie in [Labels en beleid](/help/data-views/data-governance.md) |

## Contact opnemen met de Adobe Klantenservice

Als u problemen blijft ondervinden, neemt u contact op met de klantenservice van de Adobe. Wanneer u contact opneemt met de klantenservice voor een mislukte export, moet u de volgende informatie beschikbaar hebben:

* Exportnaam

* Id exporteren

* Instantie-id

* Naam gegevensweergave

* Locatie

* Account

* Verbinding

* Bedrijfsnaam
