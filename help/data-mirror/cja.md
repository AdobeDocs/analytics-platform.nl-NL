---
title: Customer Journey Analytics configureren
description: Begrijp hoe te om de verbindingen van Customer Journey Analytics, gegevensmeningen, en projecten voor Experience Platform Data Mirror voor Customer Journey Analytics te vormen
solution: Customer Journey Analytics
feature: Basics
role: Admin
hide: true
hidefromtoc: true
badgePremium: label="Beta"
source-git-commit: 9bd124ad651274b48052edc56bfb72358aa2d79a
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Customer Journey Analytics configureren

Als u de Experience Platform Data Mirror-functie voor Customer Journey Analytics wilt gebruiken, moet u verbindingen, gegevensweergaven en werkruimteprojecten maken of bijwerken om op modellen gebaseerde gegevens te gebruiken.

## Verbindingen

In uw verbinding, voeg de op model-gebaseerde datasets toe die de gegevens van de inheemse oplossingen van het gegevenspakhuis vertegenwoordigen. Deze datasets hebben het Model datasettype.

Wanneer u een model-gebaseerde dataset toevoegt die gespiegelde gegevens van een inheemse oplossing van het gegevenspakhuis bevat, zijn die gegevens gewoonlijk gebeurtenisgegevens. Zorg ervoor u de correcte montages voor de dataset selecteert. Selecteer bijvoorbeeld het juiste gegevenstype, veld voor identiteit en veld voor tijdstempel.


## Gegevensweergaven

Definieer velden in het op een model gebaseerde schema als componenten (maateenheden en afmetingen) in de gegevensweergave. De velden met gespiegelde gegevens zijn beschikbaar in de submap **[!UICONTROL Adhoc & Model-based fields]** van de map **[!UICONTROL Event datasets]** . De functionaliteiten van het gebruik, zoals [ afgeleide gebieden ](/help/data-views/derived-fields/derived-fields.md) of [ componentenmontages ](/help/data-views/component-settings/overview.md), om de componenten te wijzigen die op model-gebaseerde gebieden gebaseerd zijn.


## Workspace-projecten

Stel Workspace-projecten in die gegevens en dimensies uit uw modelgegevens gebruiken. Componenten die uiteindelijk gebaseerd zijn op gegevens in de native oplossing van het gegevenspakhuis. En worden bijgewerkt gebaseerd op de functionaliteit van de gegevensspiegel u hebt gevormd.

>[!MORELIKETHIS]
>
>[ Data Mirror snelle startgids: Spiegel en gebruik op model-gebaseerde gegevens ](data-mirror.md)
>