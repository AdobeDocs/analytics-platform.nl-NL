---
title: Quantum Metric heatmaps gebruiken met Customer Journey Analytics
description: Begrijp beter de betrokkenheid op paginaniveau en optimaliseer pagina's op basis van consumentengedrag met behulp van Quantum Metric heatmap-gegevens.
role: User, Admin
solution: Customer Journey Analytics
feature: Use Cases
hidefromtoc: true
hide: true
exl-id: d861135f-42a4-45ac-8b11-41f151bfce92
source-git-commit: a0f82948895f3eac86cf00df1dec8abc2f723fc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Quantum Metric heatmaps gebruiken met Customer Journey Analytics

Door Quantum Metric heatmapping aan CJA-gegevens te koppelen, kunt u de betrokkenheid op paginaniveau beter begrijpen en pagina&#39;s optimaliseren op basis van consumentengedrag. Workspace kan worden gebruikt om consumentengebruikersstromen te begrijpen en te zien welke paden consumenten volgen van de ene pagina naar de andere. Vervolgens kunt u op URL&#39;s van hypergekoppelde pagina klikken om visueel te koppelen hoe gebruikers de inhoud gebruiken.

De lijst zal alle zittingen in dat segment terugkeren, en u kunt om het even welke hen klikken om verder in QM te onderzoeken.  Meer informatie over Quantum Metric session replay vindt u op https://www.quantummetric.com/platform/session-replay

## Vereisten

Voor dit gebruiksgeval moet u de sessie-id van Quantum Metric naast de rest van de implementatie verzamelen. Zie [ Metrische Sessie IDs van het Quantum in Customer Journey Analytics ](collect-session-id.md) verzamelen om te leren hoe te om uw implementatie te wijzigen.

U moet op het pakket van UX Ops van Metrische Quantum **van UX** gerechtigd zijn om tot de mogelijkheden van de heatmap van Quantum Metric toegang te hebben.

## Creeer een vrije vormlijst in Workspace en vorm het zodat de waarden van zittingidentiteitskaart verbindingen direct aan Metric Quantum zijn.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Workspace]** in het bovenste menu.
1. Selecteer een bestaand project of maak een project.
1. Creeer de lijst van de a [ Vrije vorm ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md).
1. Sleep de pagina-URL-afmeting naar het Workspace-canvas.
1. Klik met de rechtermuisknop op de kolomkop voor de dimensie en selecteer vervolgens **[!UICONTROL Create hyperlinks for all dimension items]** .
1. Selecteer **[!UICONTROL Create a custom URL]** .
1. Plak de volgende URL-structuur:

   ```
   $value?qm-visible=true
   ```

1. Klik op **[!UICONTROL Create]**.

1. Klik op Maken en test vervolgens een van de koppelingen om te zien of deze wordt geopend in de URL met de extensie QM open. Opmerking: deze wordt op een apart tabblad geopend, zodat u uw werk niet verliest.


## Heatmaps weergeven door op koppelingen in Customer Journey Analytics te klikken

Nadat u een pagina hebt gevonden waarvoor u de warmteverdeling wilt bekijken, kunt u deze toepassen op het deelvenster waarin de URL zich bevindt. De tabel retourneert een URL waarmee u de heatmaps voor de pagina in kwestie, de schuifdiepte en belangrijke zones voor interactie kunt verkennen.  Meer informatie over metrische Quantum-Heatmaps vindt u op https://www.quantummetric.com/platform/interaction-heatmaps


