---
title: Samenvattingsinstellingen gegevensgroep
description: De details en op hoe te om dimensies van datasets te vormen om u te verzekeren kunt behoorlijk over summiere gegevens rapporteren.
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: cba5904191b0602557903b5b9f32a2b793c8207d
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# [!UICONTROL Summary data group] componentinstellingen

Een summiere gegevensgroep leidt tot een vereniging tussen alle dimensies in de groepering en gebruikt om dimensies van summiere datasets met andere dimensies voor het melden te combineren.

![ Summiere de componentenmontages van de gegevensgroep ](/help/data-views/assets/summary-data-group.png)

Een groep dimensies maken:

1. Selecteer een dimensie.
1. Selecteer ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Summary data group]**.
1. Schakel **[!UICONTROL Create grouping]** in.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Dimension]** een dimensie die u wilt groeperen met de geselecteerde dimensie in de eerste stap. Merk op dat alleen de afmetingen die u al hebt toegevoegd aan de gegevensweergave beschikbaar zijn in de vervolgkeuzelijst.
1. Schakel **[!UICONTROL Hide in reporting]** desgewenst in om de gegroepeerde dimensie te verbergen voor rapportage. Als u deze optie inschakelt, is dit vergelijkbaar met het afzonderlijk configureren van **[!UICONTROL Hide in reporting]** voor de gegroepeerde dimensie. Zie [ montages van de Component ](overview.md) voor meer informatie.
1. Naar keuze, om extra dimensies aan de groepering toe te voegen, ![ voegt toe ](/help/assets/icons/Add.svg) **[!UICONTROL Add dimension to group]**.<br/> u kunt tot negen dimensies toevoegen, aangezien een summiere gegevensgroep een grens van tien dimensies heeft.

## Zelfde componentinstellingen

Bij het groeperen van afmetingen moet u ervoor zorgen dat de instellingen voor [!UICONTROL Substring] , [!UICONTROL Behavior (Lower case)] en [!UICONTROL Include exclude values] voor elk van de afmetingen die deel uitmaken van de groep, gelijk zijn. Anders kan elke dimensie van de groep mogelijk verschillende resultaten vóór de groepering retourneren.
Bijvoorbeeld:

1. U hebt een samenvattingsgegevensgroep gemaakt voor `campaign_code` (onderdeel van samenvattingsgegevens) en `tracking_code` (onderdeel van uw gebeurtenisgegevens).
1. U hebt [!UICONTROL Behavior (Lower case)] toegepast op de `campaign_code` -dimensie, maar niet op de `tracking_code` -dimensie.

Waarden in `tracking_code` kunnen mogelijk anders worden weergegeven dan in `campaign_code` .

>[!IMPORTANT]
>
>Zorg ervoor dat u de dimensies van slechts één dimensie groepeert en dat u geen groepering van meerdere dimensies toepast. Als u bijvoorbeeld een groepering maakt door de `campaign_name` -dimensie aan de `tracking_code` -dimensie toe te voegen, maakt u niet ook een groepering voor de `campaign_name` -dimensie.
>

