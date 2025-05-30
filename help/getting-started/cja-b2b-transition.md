---
title: Overgangshandleiding
description: Leer hoe u van Customer Journey Analytics naar Customer Journey Analytics B2B edition overschakelt
solution: Customer Journey Analytics
feature: Basics
role: User, Admin
badgePremium: label="B2B edition"
exl-id: d0e6398b-8080-4e36-b178-0cb91945d0c5
source-git-commit: 2fad11178853e08783b8f48671b504f50b6e0770
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Overgangsgeleider

{{draft-b2b}}

In deze handleiding wordt besproken hoe u van Customer Journey Analytics naar de B2B edition van Customer Journey Analytics kunt overstappen.

In het artikel wordt ervan uitgegaan dat u Customer Journey Analytics al in zekere mate gebruikt:

* U hebt [ verbindingen ](/help/connections/overview.md) die gegevens in Customer Journey Analytics opnemen.
* U hebt [ gegevensmeningen ](/help/data-views/data-views.md) die de gegevens van deze verbindingen gebruiken.
* U hebt [ projecten ](/help/analysis-workspace/home.md) met rapporten en visualisaties leveraging deze gegevensmeningen.

Als u Customer Journey Analytics niet eerder hebt gebruikt, verwijs naar de [ snelle startgids van B2B edition ](cja-b2b-quick-start-guide.md).

Als u een gebruiker van Adobe Analytics bent en van plan bent om Customer Journey Analytics B2B edition te gebruiken, verwijs eerst naar de [ verbetering van Adobe Analytics aan Customer Journey Analytics ](cja-upgrade/cja-upgrade-recommendations.md) documentatie.


## Bestaande implementatie

De bestaande implementatie van Customer Journey Analytics verandert helemaal niet zodra u een licentie en provisioning hebt voor Customer Journey Analytics B2B edition.

Alle bestaande verbindingen worden beschouwd als [ op persoon-gebaseerde verbindingen ](cja-b2b-concepts-features.md#connections-and-identifiers) en blijven zonder enige update werken. Alles dat op de gegevens van deze op persoon-gebaseerde verbindingen, zoals gegevensmeningen, werkruimteprojecten, segmenten, geplande uitvoer, alarm, en meer vertrouwt, blijft werken zoals oorspronkelijk gepland en voorgenomen.

>[!IMPORTANT]
>
>U kunt geen bestaande op persoon-gebaseerde verbindingen aan een op rekening-gebaseerde verbinding veranderen. Er is een nieuwe verbinding op basis van een account vereist om de B2B edition-functies te kunnen gebruiken.
>


## B2B-functies implementeren

Als u B2B-functies wilt implementeren in uw bestaande implementatie, moet u de volgende stappen uitvoeren:

1. Model uw B2B-gegevens. Customer Journey Analytics B2B edition gaat uit van ten minste gebeurtenisgegevens uit de tijdreeks van een account en profiteert van extra profiel- of opzoekrecordgegevens. Bijvoorbeeld accountgegevens, groepsgegevens kopen, opportuniteitsgegevens, gegevens over leden van marketinglijsten en meer.

   * Definieer welke id u als primaire account-id (account-id) wilt gebruiken. Vaak helpt een bestaande CRM of ander hulpmiddel (bijvoorbeeld: Demandbase) u om dat herkenningsteken te bepalen.
   * Identificeer extra id&#39;s voor de andere B2B-gegevens die u wilt gebruiken: globale account-id, opportuniteid, code van inkoopgroep en identificatie van persoon.

1. Bereid uw B2B-gegevens voor. Zorg ervoor dat u accountid&#39;s toevoegt en verzamelt voor alle gebeurtenisgegevens uit de tijdreeks en relevante recordgegevens. Op dezelfde manier zorg ervoor uw tijd-reeksen gebeurtenisgegevens en raadplegingsverslag andere herkenningstekens voor relevante gebeurtenissen bevat. Bijvoorbeeld: een gebeurtenis die de overgang naar een andere verkoopfase aangeeft, moet een opportuniteits-id hebben. En dat herkenningsteken zou deel van uw opportunityraadplegingsgegevens moeten uitmaken.

1. [ creeer een nieuwe op rekening-gebaseerde verbinding ](/help/connections/create-connection.md#account-based-connection). Selecteer welke facultatieve containers u wilt omvatten, [ datasets ](/help/connections/create-connection.md#add-datasets) toevoegen en de [ montages voor elke dataset ](/help/connections/create-connection.md#dataset-settings) bepalen. De gelijke van het gebruik [ door container ](cja-b2b-concepts-features.md#match-by-container) voor de datasets van het raadplegingsverslag wanneer dat mogelijk is.

1. [ creeer gegevensmeningen ](/help/data-views/create-dataview.md) die op uw nieuwe verbinding worden gebaseerd.

   * Zorg ervoor dat u alle relevante velden als metriek of afmetingen toevoegt uit de gegevens die u hebt ingevoerd.
   * Pas indien nodig componentinstellingen toe (zoals persistentie, kenmerk en meer).
   * Voeg zo nodig aanvullende afgeleide velden toe.

1. [ creeer werkruimteprojecten ](/help/analysis-workspace/build-workspace-project/create-projects.md) om inzichten op uw B2B- gegevens te melden en te bereiken. Gebruik specifieke eigenschappen B2B, zoals [ containers ](cja-b2b-concepts-features.md#containers), om diepe inzichten te bereiken.

   U kunt B2B (op persoon-gebaseerd) en B2B (op rekening-gebaseerde) rapporten en inzichten combineren, door het gebruik van veelvoudige [ panelen ](/help/analysis-workspace/c-panels/panels.md), in één werkruimteproject.
