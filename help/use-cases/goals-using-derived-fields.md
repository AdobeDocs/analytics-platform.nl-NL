---
title: Gebruik afgeleide gebieden om over doelstellingen te rapporteren
description: Begrijp hoe u Voortgekomen gebieden kunt gebruiken om over doelstellingen (doelstellingen) in uw projecten van de Werkruimte te rapporteren.
solution: Customer Journey Analytics
feature: Use Cases
hide: true
hidefromtoc: true
source-git-commit: 69317871bae9ad2a0fecad6b1df1cc357094b05c
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 1%

---


# Gebruik afgeleide gebieden om over doelstellingen te rapporteren

Dit gebruiksgeval beschrijft hoe te om de macht van afgeleide gebieden te gebruiken om doelstellingen voor een specifieke dimensie te plaatsen en dan deze doelstellingen in uw project van de Werkruimte te gebruiken.

Als u niet vertrouwd bent met afgeleide gebieden, verwijs naar [zelfstudie](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/data-views/derived-fields-in-cja.html?lang=en) en [documentatie](../data-views/derived-fields/derived-fields.md) voor een inleiding.


## Doelstellingen definiëren

Als u doelen wilt definiëren, maakt u een nieuw afgeleid veld waarin u expliciet aangepaste numerieke waarden rechtstreeks of onrechtstreeks instelt met behulp van de waarden die het resultaat zijn van regels die eerder in uw afgeleide velddefinitie zijn opgenomen.


### Doelstellingen voor maandelijkse Cadeaubonnen

U wilt uitdrukkelijk doelstellingen voor uw bevelen van het giftecertificaat voor vier maanden, die van juli 2023 - oktober 2023 lopen plaatsen. Dit doet u als volgt:

1. Een nieuw afgeleid veld met de naam maken `Monthly Gift Certificate Orders Goal (Incremental)`.

1. Statische waarden instellen met een CASE WHERE-REGEL voor elke maand door een **[!UICONTROL Custom numeric value]**. Zie de regel Maandelijkse Productdoelen hieronder.

   ![Productdoelstellingen](assets/goals-derived-field-product-goals-1.png)


### Doelstellingen van inkomsten uit marketingkanalen

U wilt een maandelijks inkomstendoel voor elk van uw marketing kanalen plaatsen. Dit doet u als volgt:

1. Een nieuw afgeleid veld maken met de opdracht [Sjabloon voor marketingkanalen](/help/data-views/derived-fields/derived-fields.md#marketing-channels) met de naam `Monthly Marketing Channel Revenue Goal (Incremental)`.

1. Definieer alle regels om alle marketingkanalen correct te identificeren op basis van een combinatie van URL PARSE en CASE WHEN-regels. Bijvoorbeeld:

   ![Definitie van regels voor het afgeleide gebied van marketingkanalen](assets/goals-derived-field-marketing-channel-1.png)

1. Expliciet statische waarden, die maandelijkse opbrengstdoelstellingen vertegenwoordigen, voor de specifieke marketing kanalen in definitiefGEVAL WANNEER regel, door te plaatsen **[!UICONTROL Custom numeric value]**. Zie de [!DNL Monthly Goal] lijn hieronder.

   ![Maandelijkse doelstellingen](assets/goals-derived-field-marketing-channel-2.png)



## Doelen gebruiken

Om doelstellingen in uw project van de Werkruimte te gebruiken, gebruikt u de berekende metrische functionaliteit om het afgeleide gebied terug naar zijn originele statische waarde &quot;te normaliseren. Deze normalisatie wordt vereist aangezien de statische waarden u voor de afgeleide gebieden die doelstellingen bepalen, met elke gebeurtenis worden verhoogd.

### Doelstellingen voor maandelijkse Cadeaubonnen

1. Een berekend metrisch veld maken met de naam `Monthly Gift Certificate Orders Goal`, gedefinieerd als:

   ![Orders Goal](assets/calculated-metric-ordersgoals.png)

1. U kunt bijvoorbeeld aanvullende berekende velden maken `% of Monthly Gift Certificate Orders Goal`om de werkelijke vooruitgang ten opzichte van de doelstellingen te laten zien, bijvoorbeeld:

   ![Percentage bestellingen](assets/calculated-metric-ordersgoalspercent.png)

U kunt deze berekende metriek gebruiken om over vooruitgang in vrije vormlijsten en visualisaties te rapporteren. Bijvoorbeeld:

![Freeform-tabel met doelstellingen voor marketinginkomsten](assets/freeform-table-product-order-goals.png)


### Doelstellingen van inkomsten uit marketingkanalen

1. Een berekend metrisch veld maken met de naam `Marketing Channel Revenue Goal`, gedefinieerd als:

   ![Opbrengstdoelstelling](assets/calculated-metric-revenuegoals.png)

1. U kunt bijvoorbeeld aanvullende berekende velden maken `% of Marketing Channel Revenue Goal`om de werkelijke vooruitgang ten opzichte van de doelstellingen te laten zien, bijvoorbeeld:

   ![Opbrengstpercentage](assets/calculated-metric-revenuegoalspercent.png)

U kunt deze berekende metriek gebruiken om over vooruitgang in vrije vormlijsten en visualisaties te rapporteren. Bijvoorbeeld:

![Freeform-tabel met doelstellingen voor marketinginkomsten](assets/freeform-table-marketing-channel-revenue-goals.png)
