---
title: Overzicht van productgebruik
description: Bekijk inzichten en rapporten over hoe uw organisatie Customer Journey Analytics gebruikt.
hide: true
hidefromtoc: true
source-git-commit: f337dfbd780aab4ae40534c5c1151dba35681b21
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Overzicht van productgebruik

{{release-limited-testing}}

Het gebruik van producten biedt uw organisatie de mogelijkheid om analysegegevens te bekijken over hoe uw organisatie Customer Journey Analytics gebruikt. Het is beschikbaar voor alle organisaties die Customer Journey Analytics gebruiken. Als deze optie is ingeschakeld, worden de volgende Adobe Experience Platform-componenten automatisch gemaakt en geactiveerd:

* Een schema in Adobe Experience Platform. Dit schema is in het bezit van het systeem, read-only, en kan niet worden uitgegeven.
* Een dataset in Adobe Experience Platform. Deze dataset is systeemeigendom, read-only, en kan niet worden uitgegeven.
* Een verbinding in Customer Journey Analytics. Deze verbinding is systeemeigendom, alleen-lezen en kan niet worden bewerkt.
* Een gegevensweergave in Customer Journey Analytics. U kunt deze gegevensweergave bewerken of meer gegevensweergaven maken met de bovenstaande verbinding. De eigenaar van de gegevensweergave is de persoon die het productgebruik voor uw organisatie inschakelt.

Alle gegevensinzameling en opstelling worden automatisch gevormd voor u zodra toegelaten. Elke keer dat een gebruiker een actie uitvoert in Analysis Workspace, wordt die actie bijgehouden en beschikbaar voor rapportage.

>[!IMPORTANT]
>
>Deze functie telt mee voor je contractuele rijlimieten in Adobe Experience Platform. Zorg ervoor dat uw organisatie de gegevens kan aanpassen die door deze eigenschap worden geproduceerd alvorens het toe te laten.

## Beschikbare afmetingen

Als u het productgebruik inschakelt, zijn de volgende afmetingen beschikbaar:

| Dimension | Beschrijving |
| --- | --- |
| Naam van handeling | Het type actie dat de gebruiker heeft uitgevoerd. U kunt deze dimensie als elke gewenste metrische waarde gebruiken door een kopie in de weergave-instellingen voor gegevens te maken. |
| Attributiemodel gebruikt | Het type attributiemodel dat de component gebruikt. |
| Component | Een afgeleid veld dat het componenttype en de componentnaam bevat. |
| Componenttype | Het type component dat is toegevoegd, verwijderd of gewijzigd. |
| Gebruiker aanmelden | De gebruiker die de handeling heeft uitgevoerd. |
| Gebruikt deelvenster | Het deelvenster waar de component is toegevoegd, verwijderd of gewijzigd. |
| Projectnaam | De vriendelijke naam van het project. |
| Projecttype | Het projecttype. |
| Gebruikers-id | De gebruikers-id die de gebeurtenis heeft geactiveerd. |
| Gebruikte visualisatie | De visualisatie die is toegevoegd, verwijderd of gewijzigd. |

Het gebruik van het product houdt geen individuele projectcomponenten bij wanneer een project slechts wordt geopend of bekeken. De gebruikersactie van het openen van een project wordt echter gevolgd.
