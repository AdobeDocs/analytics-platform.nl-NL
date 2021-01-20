---
title: Veelgestelde vragen over kanaalanalyse
description: Veelgestelde vragen voor kanaalanalyse
translation-type: tm+mt
source-git-commit: dca995fc271b02a26568ed8d4a672b96f10b0a18
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---


# Veelgestelde vragen

## Hoe kan ik CCA gebruiken om te zien hoe de mensen zich van één kanaal aan een andere bewegen?

U kunt een stroomvisualisatie met de dimensie van identiteitskaart van de Dataset gebruiken.

1. Meld u aan bij [analytics.adobe.com](https://analytics.adobe.com) en maak een leeg Workspace-project.
2. Klik op het tabblad Visualisatie aan de linkerkant en sleep een stroomvisualisatie naar het canvas aan de rechterkant.
3. Klik op het tabblad Componenten aan de linkerkant en sleep de dimensie &#39;Dataset ID&#39; naar de middelste locatie met de naam &#39;Dimension of Item&#39;.
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

Als u de de afmetingspunten van identiteitskaart van de dataset zou willen anders noemen, kunt u een raadplegingsdataset gebruiken.

## Hoe ver terug brengt CCA bezoekers?

Het terugkijkvenster voor het opnieuw beginnen hangt van uw gewenste frequentie van gegevens [replay](replay.md) af. Bijvoorbeeld, als u opstelling CCA om gegevens eens per week opnieuw te spelen, is het raadplegingsvenster voor het opnieuw beginnen 7 dagen. Als u opstelling CCA om gegevens elke dag opnieuw te spelen, is het raadplegingsvenster voor het opnieuw beginnen 1 dag.

## Hoe worden gedeelde apparaten afgehandeld?

In sommige situaties is het mogelijk dat meerdere personen zich aanmelden bij hetzelfde apparaat. De voorbeelden omvatten een gedeeld apparaat thuis, gedeelde PCs in een bibliotheek, of een kiosk in een detailhandelsafzet.

De tijdelijke id negeert de blijvende id, zodat gedeelde apparaten als afzonderlijke personen worden beschouwd (zelfs als ze van hetzelfde apparaat afkomstig zijn).

## Hoe behandelt CCA situaties waarin één enkele persoon een groot aantal blijvende IDs heeft?

In sommige situaties kan een individuele gebruiker een groot aantal permanente id&#39;s koppelen. Voorbeelden zijn voorbeelden waarbij een gebruiker vaak browsercookies wist of de modus Private/Incognito van de browser gebruikt.

Het aantal permanente id&#39;s is irrelevant ten gunste van de tijdelijke id. Één enkele gebruiker kan tot om het even welk aantal apparaten behoren zonder de capaciteit van CCA te beïnvloeden om over apparaten te hechten.

## Wanneer ik met de gewenste informatie contact opneem met mijn accountmanager, hoe lang duurt het dan voordat de opgehaalde gegevensset beschikbaar is?

Livemetching is ongeveer 1 week beschikbaar nadat Adobe Kanaalanalyse heeft ingeschakeld. De beschikbaarheid van back-ups is afhankelijk van de hoeveelheid bestaande gegevens. Kleine datasets (minder dan 1 miljoen gebeurtenissen per dag) nemen doorgaans een paar dagen in beslag, terwijl grote gegevenssets (1 miljard gebeurtenissen per dag) een week of meer kunnen duren.

## Hoe behandelt de Analysefuncties van het Kanaal GDPR en CCPA verzoeken?

Adobe behandelt verzoeken van de GDPR en de CCPA overeenkomstig de lokale en internationale wetgeving. Adobe biedt de [Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) aan om verzoeken om gegevenstoegang en verwijdering in te dienen. De verzoeken zijn van toepassing op zowel de oorspronkelijke als de opgehaalde gegevensbestanden.
