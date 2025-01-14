---
title: Instellingen van waardetekenmerken
description: Combineer numerieke waarden in een dimensie.
exl-id: 52f9abf6-69f1-47d0-86ab-57123bc178d5
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: e4e0c3cf2e865454837df6626c3b1b09f119f07f
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 1%

---

# [!UICONTROL Value Bucketing] componentinstellingen {#value-bucketing-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_dimension_valuebucketing"
>title="Waardebeperking"
>abstract="Emmerwaarden in specifieke bereiken. Deze waaiers verschijnen als afmetingspunten in rapporten."

<!-- markdownlint-enable MD034 -->


Wanneer u een gegevensweergave maakt of bewerkt, kunt u numerieke waarden combineren op basis van een bereik. Het is alleen beschikbaar voor dimensies die de gegevenstypen Geheel getal of Dubbel schema gebruiken.

![ het emmer van de Waarde ](../assets/value-bucketing.png)

De waarde emmer is waardevol wanneer u reeksen samen wilt groeperen in plaats van elk uniek aantal als afzonderlijk afmetingspunt te behandelen. Een emmertje van &#39;Tussen 5 en maximaal 10&#39; wordt bijvoorbeeld in Analysis Workspace weergegeven als een regelitem &#39;5 tot 10&#39;.

Als u de flexibiliteit wilt om zowel over een gespikte als niet-gespikte dimensie rapporteren, sleep twee exemplaren van de component in de beschikbare dimensielijst. Laat het knippen op één afmeting toe, en maak het op andere onbruikbaar.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Bucket value] | Een selectievakje waarmee u bucketing kunt inschakelen. |
| [!UICONTROL Less than] | De bovengrens van het emmer van de eerste dimensie. |
| [!UICONTROL Including] [!UICONTROL and less than] | Grenzen van volgende emmers. |
| [!UICONTROL Greater than or equal to] | De ondergrens van het laatste afmetingsemmer. |
| [!UICONTROL Add bucket] | Hiermee kunt u nog een emmertje toevoegen aan een numerieke dimensie-emmer. U kunt maximaal 20 emmers in één dimensie toevoegen. |

{style="table-layout:auto"}
