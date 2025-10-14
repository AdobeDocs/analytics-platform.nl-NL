---
title: Metrische gegevens van het type Quantum toevoegen aan Customer Journey Analytics
description: Gebruik Quantum Metric voor het verzamelen van gegevens van gebruikersreizen en gedrag, en dan aandrijf CJA van die verzamelde gegevens om rijkere inzichten te trekken.
role: User, Admin
solution: Customer Journey Analytics
feature: Use Cases
hidefromtoc: true
hide: true
exl-id: ea8795fe-f5aa-458f-9e01-53ff1ffe6372
source-git-commit: 03e9fb37684f8796a18a76dc0a93c4e14e6e7640
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 1%

---

# Metrische gegevens van het type Quantum toevoegen aan Customer Journey Analytics

>[!IMPORTANT]
>
>De Quantum Metric source-connector is op dit moment nog niet beschikbaar.

CJA ontgrendelt rapport-tijd controle van de QM gegevens, opeenvolgende gegevensanalyse, rijke attributie, en andere geavanceerde rapportering.  QM kan naar AEP worden verzonden door of de QM bronschakelaar of de uitbreiding van de Codes van de Metriek van de Quantum te gebruiken.

## Stap 1: Een Quantum Metric source-connector maken

1. Login aan [&#x200B; experience.adobe.com &#x200B;](https://experience.adobe.com).
1. Navigeer naar [!UICONTROL Experience Platform] > [!UICONTROL Connections] > [!UICONTROL Sources] .
1. Voeg de Metrische bronschakelaar van het Quantum toe, en volg de herinneringen aan voltooiing.

Zie [&#x200B; Adobe Experience Platform bronschakelaars &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/home) voor meer informatie.

## Stap 2: Een verbinding maken in Customer Journey Analytics

Het creëren van een bronschakelaar voor Metrische gegevens Quantum leidt automatisch tot een dataset in Adobe Experience Platform. Voeg deze dataset aan een nieuwe of bestaande [&#x200B; verbinding &#x200B;](/help/connections/overview.md) in Customer Journey Analytics toe.

1. Login aan [&#x200B; experience.adobe.com &#x200B;](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Connections]** (optioneel vanuit **[!UICONTROL Data management]** ) in het bovenste menu.
1. Geef de verbinding een naam, en voeg de Metrische dataset van het Aantal aan de verbinding toe.
1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>Terwijl u Metrische gegevens Quantum aan de zelfde verbinding zoals de rest van uw gegevens van Customer Journey Analytics kunt toevoegen, kunnen die gegevens niet samen zonder gemeenschappelijke persoonsidentiteitskaart tussen de twee datasets worden vastgemaakt. Als dit gedrag wordt gewenst, adviseert Adobe het gebruiken van de [&#x200B; uitbreiding van de Markering &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/destinations/catalog/analytics/quantum-metric) in plaats van de bronschakelaar.

## Stap 3: Een gegevensweergave maken in Customer Journey Analytics

Creeer a [&#x200B; gegevensmening &#x200B;](/help/data-views/data-views.md) om afmeting en metrische montages te vormen.

1. Login aan [&#x200B; experience.adobe.com &#x200B;](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Data views]** (optioneel vanuit **[!UICONTROL Data management]** ) in het bovenste menu.
1. Selecteer de gewenste gegevensweergave of maak een gegevensweergave.
1. Zoek de gewenste metrische afmetingen en metriek van Quantum in de lijst van schemagebieden op het recht, en sleep hen aan de afmetingen en het metriekgebied in het centrum.
1. Gebruik de juiste ruit om elke gewenste afmeting en metrisch te vormen.

## Stap 4: rapportage en analyse starten in Customer Journey Analytics

Nu de gegevens beschikbaar zijn in Customer Journey Analytics, kunt u beginnen met het rapporteren van gegevens.

1. Login aan [&#x200B; experience.adobe.com &#x200B;](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Workspace]** in het bovenste menu.
1. Selecteer een bestaand project of maak een project.
1. Sleep een gewenste metrische dimensie van Quantum of metrisch naar het Workspace-canvas om de gegevens te analyseren.
