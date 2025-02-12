---
title: Overgang van de de bronschakelaar van de Analytics aan het Web SDK voor Customer Journey Analytics
description: Leer hoe u van de Analytics-bronconnector naar de Web SDK overschakelt wanneer u een upgrade naar Customer Journey Analytics uitvoert
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 4c0eef7d-7b0e-43b5-8126-d84d4fffd80c
source-git-commit: a462bdbff59e8d83d6948ef882e66690624c4847
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Overgang van de de bronschakelaar van de Analytics aan het Web SDK voor Customer Journey Analytics {#transition-from-source-connector}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector"
>title="Implementatie van analytische bronconnector"
>abstract="Met de bronaansluiting voor Analytics kunt u eenvoudig waarde ophalen uit Customer Journey Analytics, maar u moet zowel voor Adobe Analytics als voor Customer Journey Analytics betalen. Deze gids kan u helpen zich op een onafhankelijke implementatie van SDK van het Web bewegen."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in [ Customer Journey Analytics verbeteringschecklist ](https://gigazelle.github.io/cja-ttv/).

Er zijn inherente nadelen aan het gebruiken van de de bronschakelaar van de Analyse als uw enige implementatie voor Customer Journey Analytics.

Als uw organisatie reeds aan Customer Journey Analytics gebruikend slechts de de bronschakelaarimplementatie van de Analyse heeft bevorderd, adviseert Adobe transitioning aan een implementatie die de bronschakelaar van de Analyse (voor historische gegevens) gebruikt, samen met een nieuwe implementatie van het Web SDK (voor aan de gang zijnde gegevensinzameling).

## Voor- en nadelen van het exclusief gebruiken van de bronconnector Analytics

Voor informatie over de voordelen en de nadelen van het gebruiken van de Analyse bronschakelaar, zie [ Gebruik de Analytics bronschakelaar exclusief om aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-exclusively.md) te bevorderen.

## Overgang van de de bronschakelaar van de Analyse aan het Web SDK

Na is het proces op hoog niveau voor het overschakelen van uitsluitend het gebruiken van de Analytics bronschakelaar aan een implementatie die van zowel de Analytics bronschakelaar als een implementatie van SDK van het Web wordt samengesteld:

1. Creeer een implementatie van SDK van het Web, zoals die in [ wordt beschreven Gedetailleerde geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#detailed-recommended-upgrade-steps) in het artikel, [ Verbetering van Adobe Analytics aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).

   Nadat de implementatie van SDK van het Web wordt gevormd, ga met de volgende stappen verder.

1. [ creeer een schema XDM voor de bron van Analytics schakelaar ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md).

1. Wijs elke afmeting van Adobe Analytics van uw bron van Analytics aan de afmeting in het schema van SDK van het Web toe.

   1. 
      <!-- how do you get here -->

   1. Selecteer in de sectie **[!UICONTROL Map standard fields]** de tab **[!UICONTROL Custom]** .

   1. Selecteer **[!UICONTROL Add new mapping]** .

      ![ gebieden van het kaartschema ](assets/schema-mapping.png)

   1. Selecteer in **[!UICONTROL Source field]** een Adobe Analytics-veld in de veldgroep Adobe Analytics ExperienceEvent-sjabloon. Selecteer vervolgens in **[!UICONTROL Target field]** het XDM-veld waaraan u het wilt toewijzen.

   1. Herhaal dit proces voor elk veld in de Adobe Analytics ExperienceEvent-sjabloonveldgroep dat u gebruikt om gegevens te verzamelen in Adobe Analytics.

1. Voeg de dataset toe die automatisch met uw originele de bronschakelaar van de Analyse aan uw verbinding van Customer Journey Analytics werd gecreeerd.

   Voor meer informatie, zie [ de dataset van uw huidige Analytics bronschakelaar aan de verbinding ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md) toevoegen.

1. (Voorwaardelijk) als u raadplegingsdatasets gebruikt, moet u de raadplegingsdataset tot stand brengen en het toevoegen aan uw verbinding. Voor meer informatie, zie [ raadplegingsdatasets creëren om gegevens in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataset-lookup.md) te classificeren.

1. Verwijder de originele bronaansluiting voor Analytics. <!-- need to add steps somewhere about how to do this -->

1. [ creeer een nieuwe de bronschakelaar van de Analyse en kaartgebieden ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md).
