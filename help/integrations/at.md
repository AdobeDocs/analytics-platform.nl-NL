---
title: Doelrapportage
description: Adobe Target integreren met Customer Journey Analytics
feature: Experience Platform Integration
role: User
exl-id: 0b52af5b-b65c-4929-9ca3-547a640936f3
source-git-commit: 81e08ecb593b6ba789c479d0e648cbe7ba0a82d6
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Doelrapportage

Met Target Reporting in Customer Journey Analytics kunt u Adobe Target-activiteiten direct in Customer Journey Analytics meten en rapporteren. Deze functionaliteit is vergelijkbaar met wat wordt uitgevoerd in Adobe Analytics (AA) via Analytics for Target (A4T), maar met de connectiviteit met Adobe Experience Platform (AEP).

Door de de opzoekdataset van de Indeling van het Doel (die door gebrek in Experience Platform) in een Verbinding van Customer Journey Analytics beschikbaar is, hebben de gebruikers nu juiste blootstelling aan de het melden van het Doel hulpmiddelen, de Orde van het Doel attributie, en andere eigenschappen. Met slechts enkele kleine voorbereidingen en aanpassingen in de Customer Journey Analytics-gegevensweergave kunnen deze activiteiten onmiddellijk beschikbaar worden gesteld voor alle gebruikers die Target-gegevens rechtstreeks naar CJA willen verzenden.

## Primaire voordelen

* Marketers kunnen Customer Journey Analytics succesmetriek op elk ogenblik dynamisch toepassen op Activiteitenrapporten van het Doel. U hoeft niet alles op te geven voordat u de activiteit uitvoert.
* Marketers kunnen gebruikmaken van Customer Journey Analytics-functies, zoals het deelvenster Experimentatie, om de personalisatie van hun website verder te analyseren.
* Marktdeelnemers kunnen één bron voor rapportage voor Adobe Journey Optimizer en Target hebben. Beide verpersoonlijkingsproducten kunnen met Customer Journey Analytics voor een holistischer mening van uw Webverpersoonlijking worden verbonden.

## Notities en overwegingen

Uw activiteit van het Doel moet [&#x200B; Customer Journey Analytics als rapporteringsbron &#x200B;](https://experienceleague.adobe.com/nl/docs/target/using/integrate/cja/target-reporting-in-cja) gebruiken.

Zodra de Dataset van de Gebeurtenis van de Classificatie van het Doel aan een verbinding is toegevoegd, zijn er een paar kleine aanpassingen die binnen de gegevensmening moeten worden aangebracht zodra deze componenten als afmetingen zijn toegevoegd, die omvatten:

* Vaststelling van persistentie om vergelijkbaar te zijn met hoe het in Doel wordt gevolgd (vraag een consultant van Target of de klant om de juiste instellingen te controleren).

* Vaststelling van persistentie aan ALLE, waardoor meerdere doelactiviteiten gelijktijdig kunnen worden bijgehouden en niet door toekomstige of vorige activiteiten kunnen worden overschreven.

## Meer gedetailleerde informatie

Zie [&#x200B; Doel rapporterend in Adobe Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/target/using/integrate/cja/target-reporting-in-cja) in de documentatie van het Doel voor meer informatie.

Zie het [&#x200B; paneel van de Experimentatie &#x200B;](../analysis-workspace/c-panels/experimentation.md) voor meer informatie over hoe de analisten verschillende gebruikerservaring, marketing, of overseinenvariaties kunnen vergelijken om te bepalen wat het best in het drijven van een specifiek resultaat is. U kunt de lift en het vertrouwen van om het even welk A/B experiment van om het even welk experimentatieplatform evalueren - online, off-line, van de oplossingen van Adobe zoals Doel of Journey Optimizer, en zelfs BYO (breng-uw-eigen) gegevens.
