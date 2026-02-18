---
title: Overgang van de de bronschakelaar van de Analytics aan het Web SDK voor Customer Journey Analytics
description: Leer hoe u van de Analytics-bronconnector naar de Web SDK overschakelt wanneer u een upgrade naar Customer Journey Analytics uitvoert
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 4c0eef7d-7b0e-43b5-8126-d84d4fffd80c
source-git-commit: 5faf9668475818773c645b69915ddd5182500aea
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---

# Overgang van de de bronschakelaar van de Analytics aan het Web SDK voor Customer Journey Analytics {#transition-from-source-connector}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector"
>title="Implementatie van analytische bronconnector"
>abstract="Met de bronaansluiting voor Analytics kunt u eenvoudig waarde ophalen uit Customer Journey Analytics, maar u moet zowel voor Adobe Analytics als voor Customer Journey Analytics betalen. Deze gids kan u helpen zich op een onafhankelijke implementatie van SDK van het Web bewegen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector-delete"
>title="De bestaande bronconnector voor Analytics verwijderen"
>abstract="De bronschakelaar van Analytics die u momenteel hebt is niet compatibel met het douaneschema van uw organisatie. De gegevens staan echter nog steeds in het pakket Analytics-rapporten. Deze stap verwijdert de huidige bronschakelaar van de Analyse zodat kunt u het ontspannen gebruikend het correcte schema in een verdere stap.<br><br> alvorens u de bronschakelaar schrapt, zou u met anderen in uw organisatie kunnen willen coördineren om ervoor te zorgen dat de verwijdering van de bronschakelaar geen rapportering binnen uw organisatie beïnvloedt. Deze coördinatie kan enkele weken duren."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

Er zijn inherente nadelen aan het gebruiken van de de bronschakelaar van de Analyse als uw enige implementatie voor Customer Journey Analytics.

Als uw organisatie reeds aan Customer Journey Analytics gebruikend slechts de de bronschakelaarimplementatie van de Analyse heeft bevorderd, adviseert Adobe transitioning aan een nieuwe implementatie van het Web SDK voor aan de gang zijnde gegevensinzameling, en het gebruiken van de Analytics bronschakelaar slechts voor historische gegevens.

## Voor- en nadelen van het exclusief gebruiken van de bronconnector Analytics

Voor informatie over de voordelen en de nadelen van het gebruiken van de Analyse bronschakelaar, zie [&#x200B; Gebruik de Analytics bronschakelaar exclusief om aan Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-alternative-source-connector.md) te bevorderen.

## Overgang van de de bronschakelaar van de Analyse aan het Web SDK

Na is het proces op hoog niveau voor het overschakelen van uitsluitend het gebruiken van de Analytics bronschakelaar aan een implementatie die van zowel de Analytics bronschakelaar als een implementatie van SDK van het Web wordt samengesteld:

1. Creeer een implementatie van SDK van het Web, zoals die in [&#x200B; wordt beschreven Gedetailleerde geadviseerde verbeteringsstappen &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#detailed-recommended-upgrade-steps) in het artikel, [&#x200B; Verbetering van Adobe Analytics aan Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).

   Nadat de implementatie van SDK van het Web wordt gevormd, ga met de volgende stappen verder.

1. [&#x200B; creeer een schema XDM voor de bron van Analytics schakelaar &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md).

1. Wijs elke afmeting van Adobe Analytics van uw bron van Analytics aan de afmeting in het schema van SDK van het Web toe.

   1. Selecteer in de sectie **[!UICONTROL Map standard fields]** de tab **[!UICONTROL Custom]** .

   1. Selecteer **[!UICONTROL Add new mapping]**.

      ![&#x200B; gebieden van het kaartschema &#x200B;](assets/schema-mapping.png)

   1. Selecteer in **[!UICONTROL Source field]** een Adobe Analytics-veld in de veldgroep Adobe Analytics ExperienceEvent-sjabloon. Selecteer vervolgens in **[!UICONTROL Target field]** het XDM-veld waaraan u het wilt toewijzen.

   1. Herhaal dit proces voor elk veld in de Adobe Analytics ExperienceEvent-sjabloonveldgroep dat u gebruikt om gegevens te verzamelen in Adobe Analytics.

1. Voeg de dataset toe die automatisch met uw originele de bronschakelaar van de Analyse aan uw verbinding van Customer Journey Analytics werd gecreeerd.

   Voor meer informatie, zie [&#x200B; de dataset van uw huidige Analytics bronschakelaar aan de verbinding &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md) toevoegen.

1. (Voorwaardelijk) als u raadplegingsdatasets gebruikt, moet u de raadplegingsdataset tot stand brengen en het toevoegen aan uw verbinding. Voor meer informatie, zie [&#x200B; raadplegingsdatasets creëren om gegevens in Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-dataset-lookup.md) te classificeren.

1. Verwijder de originele bronaansluiting voor Analytics. <!-- need to add steps somewhere about how to do this -->

1. [&#x200B; creeer een nieuwe de bronschakelaar van de Analyse en kaartgebieden &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md).

{{upgrade-final-step}}
