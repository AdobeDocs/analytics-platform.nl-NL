---
title: Ga van de bron van Analytics schakelaar naar Web SDK voor Customer Journey Analytics
description: Leer hoe te zich aan het Web SDK van de de bronschakelaar van de Analyse wanneer bevordering aan Customer Journey Analytics te bewegen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 4c0eef7d-7b0e-43b5-8126-d84d4fffd80c
source-git-commit: a1feb2e8458169ed208da2c42fab62d25e1015bb
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Ga van de bron van Analytics schakelaar naar Web SDK voor Customer Journey Analytics

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in de [ controlelijst van de Customer Journey Analytics verbetering ](https://gigazelle.github.io/cja-ttv/).

Er zijn inherente nadelen aan het gebruiken van de bron van Analytics schakelaar als uw enige implementatie voor Customer Journey Analytics. Als uw organisatie reeds aan Customer Journey Analytics gebruikend slechts de de bronschakelaarimplementatie van de Analyse heeft bevorderd, zou u moeten overwegen zich aan een implementatie van SDK van het Web te bewegen.

De Adobe adviseert gebruikend de Analytics bronschakelaar (voor het brengen van historische gegevens), samen met een nieuwe implementatie van het Web SDK (voor aan de gang zijnde gegevensinzameling).

## Voor- en nadelen van het exclusief gebruiken van de bronconnector Analytics

Voor informatie over de voordelen en de nadelen van het gebruiken van de Analyse bronschakelaar, zie [ Gebruik de Analytics bronschakelaar exclusief om aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-exclusively.md) te bevorderen.

## Van de bron van Analytics schakelaar aan het Web SDK

Na is het proces op hoog niveau om van de de bronschakelaar van de Analyse aan een implementatie te bewegen die van zowel de de bronschakelaar van de Analyse als een implementatie van SDK van het Web wordt samengesteld:

1. Creeer een implementatie van SDK van het Web, zoals die in [ wordt beschreven Gedetailleerde geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#detailed-recommended-upgrade-steps) in het artikel, [ Verbetering van Adobe Analytics aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).

   Nadat de implementatie van SDK van het Web wordt gevormd, ga met de volgende stappen verder.

1. Bepaal of u het schema van Adobe Analytics of een schema XDM in uw implementatie van SDK van het Web zult gebruiken.

   Voor meer informatie, zie [ uw schema voor Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-existing.md) kiezen.

1. (Voorwaardelijk) als u van plan bent om het schema van Adobe Analytics met uw implementatie van SDK van het Web te gebruiken, voeg de dataset toe die automatisch door de de bronschakelaar van de Analyse aan uw verbinding van de Customer Journey Analytics werd gecreeerd.

   Voor meer informatie, zie [ de gegevensset van de bron van Analytics toevoegen aan de verbinding ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md).

1. (Voorwaardelijk) als u van plan bent om een schema XDM met uw implementatie van SDK van het Web te gebruiken:

   1. [ creeer een schema XDM voor de bron van Analytics schakelaar ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md).

   1. Voeg de dataset toe die automatisch met uw originele de bronschakelaar van de Analyse aan uw verbinding van de Customer Journey Analytics werd gecreeerd.

      Voor meer informatie, zie [ de dataset van uw huidige Analytics bronschakelaar aan de verbinding ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md) toevoegen.

   1. Verwijder de originele bronaansluiting voor Analytics. <!-- need to add steps somewhere about how to do this -->

   1. [ creeer een nieuwe de bronschakelaar van de Analyse en kaartgebieden ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md).
