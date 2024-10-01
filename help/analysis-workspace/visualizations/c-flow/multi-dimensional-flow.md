---
description: Met een interdimensionale stroom kunt u gebruikerspaden in verschillende dimensies bekijken.
title: Interdimensionale stromen
feature: Visualizations
exl-id: 459166b1-a522-45b6-9d2c-69e3409e442e
role: User
source-git-commit: 80522177d5258e4b5046b3872483ce2b482ae77d
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Interdimensionale stromen

Met een interdimensionale stroom kunt u gebruikerspaden in verschillende dimensies bekijken. In dit artikel wordt getoond hoe u deze workflow kunt gebruiken voor twee gebruiksgevallen: interacties en gebeurtenissen voor mobiele apps en hoe campagnes webbezoeken aansturen

<!--
A dimension label at the top of each Flow column makes using multiple dimensions in a flow visualization more intuitive:

![An intero-dimensional flow highlighting multiple dimensions including Product, Page, OS version, and Time Spent.](assets/flow.png)
-->

## Interacties en gebeurtenissen voor mobiele apps

De [!UICONTROL Screen Name] -dimensie wordt gebruikt in deze voorbeeldstroom om te zien hoe gebruikers de verschillende schermen (scènes) in de app gebruiken. Het bovenste scherm dat wordt geretourneerd, is **[!UICONTROL luma: content: ios: en: home]** , de startpagina van de app:

![ de stroom die van A het Toegevoegde Punt toont.](assets/flowapp.png)

Als u de interactie tussen schermen en gebeurtenistypen (zoals toevoegen aan winkelwagentje, aankopen en andere) in deze app wilt verkennen, sleept u de **[!UICONTROL Event Types]** -dimensie en zet u deze neer:

* Boven op elke beschikbare stap in de flow, om die dimensie te vervangen:

  ![ de stroom van A die de afmeting van de Pagina toont sleept aan de veelvoudige gebieden.](assets/flowapp-replace.png)

* Buiten de huidige stroomvisualisatie om de dimensie toe te voegen:

  ![ de stroom van A die de afmeting van de Pagina toont aan het witte die ruimte aan het eind wordt gesleept.](assets/flowapp-add.png)

De stroomvisualisatie hieronder toont het resultaat van het toevoegen van de **[!UICONTROL  Event Types]** dimensie. De visualisatie biedt inzicht in de manier waarop gebruikers van mobiele apps verschillende schermen in de app doorlopen voordat ze producten aan een winkelwagentje toevoegen, de toepassing sluiten, een aanbieding krijgen en nog veel meer.

![ A fLow die de de afmetingsresultaten van de Pagina bij de bovenkant van de lijst tonen.](assets/flowapp-result.png)

## Hoe campagnes webbezoeken sturen

U wilt analyseren welke campagnes bezoeken aan de website aansturen. U maakt een stroomvisualisatie met de **[!UICONTROL Campaign Name]** als dimensie

![ de dimensie van de het Webcampagne van de stroom ](assets/flowweb.png)

U vervangt de laatste **[!UICONTROL Campaign Name]** -dimensie door de **[!UICONTROL Formatted Page Name]** -dimensie en voegt nog een **[!UICONTROL Formatted Page Name]** -dimensie toe aan het einde van de flowvisualisatie.

![ de naam van de het Webcampagne van de stroom en Web-pagina dimensie ](assets/flowweb-replace.png)

U kunt de muisaanwijzer boven een willekeurige stroom houden om meer details weer te geven. Welke campagnes bijvoorbeeld hebben geleid tot een afhandeling van winkelwagentjes.

![ de naam van de het Webcampagne van de stroom en Web-pagina dimensie hover ](assets/flowweb-hover.png)
