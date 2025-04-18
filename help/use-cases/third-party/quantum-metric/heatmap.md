---
title: Quantum Metric heatmaps gebruiken met Customer Journey Analytics
description: Begrijp beter de betrokkenheid op paginaniveau en optimaliseer pagina's op basis van consumentengedrag met behulp van Quantum Metric heatmap-gegevens.
role: User, Admin
solution: Customer Journey Analytics
feature: Use Cases
hidefromtoc: true
hide: true
exl-id: d861135f-42a4-45ac-8b11-41f151bfce92
source-git-commit: 25a2c549c27918f80202bde4cd30e305f4a295f3
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# Quantum Metric heatmaps gebruiken met Customer Journey Analytics

Door Quantum Metric heatmapping aan CJA-gegevens te koppelen, kunt u de betrokkenheid op paginaniveau beter begrijpen en pagina&#39;s optimaliseren op basis van consumentengedrag. Workspace kan worden gebruikt om consumentengebruikersstromen te begrijpen en te zien welke paden consumenten volgen van de ene pagina naar de andere. Vervolgens kunt u op URL&#39;s van hypergekoppelde pagina klikken om visueel te koppelen hoe gebruikers de inhoud gebruiken. Door Quantum Metric Heatmapping aan CJA te koppelen, kunt u nu interacties op paginaniveau koppelen aan bedrijfsresultaten en uw analyse naar het volgende niveau brengen.

De lijst zal alle zittingen in dat segment terugkeren, en u kunt om het even welke hen klikken om verder in QM te onderzoeken.  Meer informatie over Quantum Metric session replay vindt u op https://www.quantummetric.com/platform/session-replay

## Vereisten

U moet op het pakket van UX Ops van Metrische Quantum **van UX** gerechtigd zijn om tot de mogelijkheden van de heatmap van Quantum Metric toegang te hebben.

## Stap 1: Creeer een vrije lijst in Workspace en vorm het zodat de waarden van zittingidentiteitskaart verbindingen direct aan Metric Quantum zijn.

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
1. Test een van de koppelingen om te zien of deze wordt geopend in de URL terwijl de extensie Quantum Metric zichtbaar is. Deze koppelingen worden geopend op een nieuw tabblad, zodat uw Workspace-project open blijft.

## Stap 2: heatmaps weergeven door op koppelingen in Customer Journey Analytics te klikken

Nadat u een pagina hebt gevonden die u wilt verkennen, kunt u deze toepassen op het gewenste deelvenster. De tabel retourneert een URL waarmee u met behulp van Quantum Metric warmtekaarten, schuifdiepte en belangrijke zones voor interactie kunt verkennen. Zie [ het Metrische overzicht van het Kwartaalproduct van de heatmap ](https://www.quantummetric.com/platform/interaction-heatmaps) voor meer informatie. U kunt uw Metrische vertegenwoordiger van de klantensteun van Quantum ook contacteren of een verzoek indienen door het [ Metrische Portaal van het Verzoek van de Klant van Quantum Metrisch ](https://community.quantummetric.com/s/public-support-page).
