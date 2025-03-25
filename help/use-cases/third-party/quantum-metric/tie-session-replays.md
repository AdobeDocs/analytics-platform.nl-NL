---
title: De metrische tijdsessie van Tie Quantum wordt opnieuw afgespeeld op gegevens in Customer Journey Analytics
description: Metrische Link Quantum-sessie wordt opnieuw afgespeeld met CJA-gegevens om beter te begrijpen waarom achter "wat" zit.
role: User, Admin
solution: Customer Journey Analytics
feature: Use Cases
hidefromtoc: true
hide: true
exl-id: fcc36457-4ce9-4c93-93e2-de03becfd5da
source-git-commit: 752e8564c341cf02b5378a12a820f52ca6164a3d
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# De metrische tijdsessie van Tie Quantum wordt opnieuw afgespeeld op gegevens in Customer Journey Analytics

Door Quantum Metric-sessiereplay te koppelen aan CJA-gegevens, kunnen klanten beter begrijpen waarom achter &quot;wat&quot; zit.  Workspace kan worden gebruikt om sessies met wrijving te ontdekken, dan kunt u hyperlinked zitting IDs klikken om zittingsreplay in Quantum Metric te onderzoeken.  Deze gegevens maken het mogelijk om gedrag binnen een sessie te bekijken en beter te begrijpen wat de wrijving van de consument stimuleert.  Door sessiereacties die aan CJA zijn gekoppeld, kunt u in uw ervaring kritieke context rond het gedrag van de klant vastleggen.

## Vereisten

Voor dit gebruiksgeval moet u de sessie-id van Quantum Metric naast de rest van de implementatie verzamelen. Zie [ Metrische Sessie IDs van het Quantum in Customer Journey Analytics ](collect-session-id.md) verzamelen om te leren hoe te om uw implementatie te wijzigen.

## Stap 1: Vorm Workspace om de dimensie van zitting-identiteitskaart aan te passen

Creeer een vrije vormlijst in Workspace en vorm het zodat de waarden van zittingidentiteitskaart verbindingen direct aan Metric Quantum zijn.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Workspace]** in het bovenste menu.
1. Selecteer een bestaand project of maak een project.
1. Creeer de lijst van de a [ Vrije vorm ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md).
1. Sleep de dimensie van sessie-id naar het Workspace-canvas.
1. Klik met de rechtermuisknop op de kolomkop voor de dimensie en selecteer vervolgens **[!UICONTROL Create hyperlinks for all dimension items]** .
1. Selecteer **[!UICONTROL Create a custom URL]** .
1. Plak de volgende URL-structuur:

   ```
   https://adobe.quantummetric.com/#/replay/cookie:$value
   ```

1. Klik op **[!UICONTROL Create]**.

Elke sessie-id is nu een klikbare koppeling. Zie [ hyperlinks in een vrije vormlijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md) voor meer informatie bij het toevoegen van hyperlinks aan de afmetingspunten van Analysis Workspace creëren.

## Stap 2 Weergavesessies vanuit Customer Journey Analytics

Zodra u een Instesting segment hebt gevonden waarvoor u zittingsreplay wilt onderzoeken, kunt u het op het paneel toepassen dat uw verbindingen van identiteitskaart van de zitting en filter door segment omvat. De lijst zal alle zittingen in dat segment terugkeren, en u kunt om het even welk van hen klikken om verder in Quantum Metric te onderzoeken.

Leer meer over Metrische zittingsreplay van Quantum bij [ https://www.quantummetric.com/platform/session-replay ](https://www.quantummetric.com/platform/session-replay). Voor om het even welke extra middelen gelieve uw Metrische vertegenwoordiger van de klantensteun van Quantum te contacteren of een verzoek door het Metrische Deel van het Verzoek van de Klant van Quantum [ ](https://community.quantummetric.com/s/public-support-page) voor te leggen.

