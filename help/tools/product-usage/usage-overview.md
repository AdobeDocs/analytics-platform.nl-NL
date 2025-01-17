---
title: Overzicht van productgebruik
description: Bekijk inzichten en rapporten over hoe uw organisatie Customer Journey Analytics gebruikt.
exl-id: 3806ca7c-ee90-4222-9ffd-2e791c4550e5
source-git-commit: 9e29a16fc8d2cfe9a7a2e926b5f592280b2c1c7a
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Overzicht van productgebruik

{{release-limited-testing}}

Het gebruik van producten biedt uw organisatie de mogelijkheid om analysegegevens te bekijken over hoe uw organisatie Customer Journey Analytics gebruikt. Het is beschikbaar voor alle organisaties die Customer Journey Analytics gebruiken. Als deze optie is ingeschakeld, worden de volgende Adobe Experience Platform-componenten automatisch gemaakt en geactiveerd. Deze componenten zijn allemaal systeemeigendom, alleen-lezen en kunnen niet worden bewerkt.

* Een schema in Adobe Experience Platform
* Een dataset in Adobe Experience Platform
* Een verbinding in Customer Journey Analytics
* Een gegevensweergave in Customer Journey Analytics

Alle gegevensinzameling en opstelling worden automatisch gevormd voor u zodra toegelaten. Elke keer dat een gebruiker een actie uitvoert in Analysis Workspace, wordt die actie bijgehouden en beschikbaar voor rapportage.

>[!IMPORTANT]
>
>Deze functie telt mee voor je contractuele rijlimieten in Adobe Experience Platform. Zorg ervoor dat uw organisatie de gegevens kan aanpassen die door deze eigenschap worden geproduceerd alvorens het toe te laten.

## Productgebruik inschakelen

**[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL Product Usage]**

Het navigeren aan deze sectie van de interface in Customer Journey Analytics neemt u aan [ montages van Gegevens ](data-settings.md) waar u deze eigenschap kunt toelaten.

## Beschikbare afmetingen

Als u het productgebruik inschakelt, zijn de volgende afmetingen beschikbaar. Als u dimensie-instellingen wilt wijzigen, maakt u een kopie van de gegevensweergave die eigendom is van het systeem en gebruikt u de gekopieerde gegevensweergave in Analysis Workspace.

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
