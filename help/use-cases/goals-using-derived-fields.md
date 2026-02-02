---
title: Gebruik afgeleide gebieden om over doelstellingen te rapporteren
description: Begrijp hoe u Voortgekomen gebieden kunt gebruiken om over doelstellingen (doelstellingen) in uw projecten van Workspace te rapporteren.
solution: Customer Journey Analytics
feature: Use Cases
exl-id: 5cd838f7-e394-4a67-9d2e-e1d08a864ca0
role: User
source-git-commit: 39d3a233166e2ce2035df2ce821dd16181e5e13e
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 1%

---

# Gebruik afgeleide gebieden om over doelstellingen te rapporteren

Dit gebruiksgeval beschrijft hoe te om de macht van afgeleide gebieden te gebruiken om doelstellingen voor een specifieke dimensie te plaatsen en dan deze doelstellingen in uw project van Workspace te gebruiken.

Als u niet vertrouwd met afgeleide gebieden bent, verwijs naar het [&#x200B; leerprogramma &#x200B;](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/data-views/derived-fields-in-cja.html?lang=nl-NL) en [&#x200B; documentatie &#x200B;](../data-views/derived-fields/derived-fields.md) voor een inleiding.


## Doelstellingen definiëren

Als u doelen wilt definiëren, maakt u een nieuw afgeleid veld waarin u expliciet aangepaste numerieke waarden rechtstreeks of onrechtstreeks instelt met behulp van de waarden die het resultaat zijn van regels die eerder in uw afgeleide velddefinitie zijn opgenomen.


### Doelstellingen voor maandelijkse Cadeaubonnen

U wilt uitdrukkelijk doelstellingen voor uw bevelen van het giftecertificaat voor vier maanden, die van juli 2023 - oktober 2023 lopen plaatsen. Dit doet u als volgt:

1. Maak een nieuw afgeleid veld met de naam `Monthly Gift Certificate Orders Goal (Incremental)` .

1. Statische waarden instellen met een CASE WHEN-REGEL voor elke maand door een **[!UICONTROL Custom numeric value]** in te stellen. Zie de regel Maandelijkse Productdoelen hieronder.

   ![&#x200B; Maandelijkse Doelstellingen van het Product &#x200B;](assets/goals-derived-field-product-goals-1.png)


### Doelstellingen van inkomsten uit marketingkanalen

U wilt een maandelijks inkomstendoel voor elk van uw marketing kanalen plaatsen. Dit doet u als volgt:

1. Creeer een nieuw afgeleid gebied, gebruikend het [&#x200B; malplaatje van de de kanaalfunctie van de Marketing &#x200B;](/help/data-views/derived-fields/derived-fields.md#marketing-channels) met de naam `Monthly Marketing Channel Revenue Goal (Incremental)`.

1. Definieer alle regels om alle marketingkanalen correct te identificeren op basis van een combinatie van URL PARSE en CASE WHEN-regels. Bijvoorbeeld:

   ![&#x200B; Definitie van regels voor het op de markt brengen van kanaal afgeleid gebied &#x200B;](assets/goals-derived-field-marketing-channel-1.png)

1. Statische waarden expliciet instellen voor de specifieke marketingkanalen in een definitieve CASE WHEN-regel door een **[!UICONTROL Custom numeric value]** in te stellen. Deze waarden vertegenwoordigen de doelstellingen van de maandelijkse omzet. Zie de onderstaande regel [!DNL Monthly Goal] .

   ![&#x200B; Maandelijkse Doelen &#x200B;](assets/goals-derived-field-marketing-channel-2.png)



## Doelen gebruiken

Om doelstellingen in uw project van Workspace te gebruiken, gebruikt u de berekende metrische functionaliteit om het afgeleide gebied terug naar zijn originele statische waarde &quot;te normaliseren. Deze normalisatie wordt vereist aangezien de statische waarden u voor de afgeleide gebieden die doelstellingen bepalen, met elke gebeurtenis worden verhoogd.

### Doelstellingen voor maandelijkse Cadeaubonnen

1. Maak een berekend metrisch veld met de naam `Monthly Gift Certificate Orders Goal` , gedefinieerd als:

   ![&#x200B; het Doel van Orden &#x200B;](assets/calculated-metric-ordersgoals.png)

1. U kunt aanvullende berekende velden maken, bijvoorbeeld `% of Monthly Gift Certificate Orders Goal` , om de werkelijke voortgang ten opzichte van de doelen te laten zien, bijvoorbeeld:

   ![&#x200B; het Tarief van het Goal van Orden &#x200B;](assets/calculated-metric-ordersgoalspercent.png)

U kunt deze berekende metriek gebruiken om over vooruitgang in vrije vormlijsten en visualisaties te rapporteren. Bijvoorbeeld:

![&#x200B; Vrije lijst die marketing opbrengstdoelstellingen toont &#x200B;](assets/freeform-table-marketing-channel-revenue-goals.png)




### Doelstellingen van inkomsten uit marketingkanalen

1. Maak een berekend metrisch veld met de naam `Marketing Channel Revenue Goal` , gedefinieerd als:

   ![&#x200B; het Doel van de Opbrengst &#x200B;](assets/calculated-metric-revenuegoals.png)

1. U kunt aanvullende berekende velden maken, bijvoorbeeld `% of Marketing Channel Revenue Goal` , om de werkelijke voortgang ten opzichte van de doelen te laten zien, bijvoorbeeld:

   ![&#x200B; Percentage van het Gebied van Opbrengst &#x200B;](assets/calculated-metric-revenuegoalspercent.png)

U kunt deze berekende metriek gebruiken om over vooruitgang in vrije vormlijsten en visualisaties te rapporteren. Bijvoorbeeld:

![&#x200B; Vrije lijst die marketing opbrengstdoelstellingen toont &#x200B;](assets/freeform-table-product-order-goals.png)
