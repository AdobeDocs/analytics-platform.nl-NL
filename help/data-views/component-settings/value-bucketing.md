---
title: Instellingen van waardetekenmerken
description: Combineer numerieke waarden in een dimensie.
source-git-commit: af357167e65f4a577880832818221f6edbfc8b0a
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---


# Instellingen van component Value Bucketing

Wanneer u een gegevensweergave maakt of bewerkt, kunt u numerieke waarden combineren op basis van een bereik. Het is alleen beschikbaar voor dimensies die de gegevenstypen Geheel getal of Dubbel schema gebruiken.

De waarde emmer is waardevol wanneer u reeksen samen wilt groeperen in plaats van elk uniek aantal als afzonderlijk afmetingspunt te behandelen. Een emmertje van &#39;Tussen 5 en maximaal 10&#39; wordt bijvoorbeeld in Analysis Workspace weergegeven als een regelitem &#39;5 tot 10&#39;.

![Waardebeperking](../assets/value-bucketing.png)

Als u de flexibiliteit wilt om zowel over een gespikte als niet-gespikte dimensie rapporteren, sleep twee exemplaren van de component in de beschikbare dimensielijst. Laat het knippen op één afmeting toe, en maak het op andere onbruikbaar.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Bucket value] | Een selectievakje waarmee u bucketing kunt inschakelen. |
| [!UICONTROL Less than] | De bovengrens van het emmer van de eerste dimensie. |
| [!UICONTROL Including] [!UICONTROL and less than] | Grenzen van volgende emmers. |
| [!UICONTROL Greater than or equal to] | De ondergrens van het laatste afmetingsemmer. |
| [!UICONTROL Add bucket] | Hiermee kunt u nog een emmertje toevoegen aan een numerieke dimensie-emmer. U kunt maximaal 20 emmers in één dimensie toevoegen. |
