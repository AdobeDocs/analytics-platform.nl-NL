---
title: Veelgestelde vragen over kanaalanalyse
description: Veelgestelde vragen voor kanaalanalyse
exl-id: 2ad78c19-4b13-495b-a0aa-44e0a3c95b5e
solution: Customer Journey Analytics
feature: Cross-Channel Analytics
source-git-commit: 8e902022c07376fb3c13cad5fd5b1efa655c9424
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---

# Veelgestelde vragen

## Hoe kan ik CCA gebruiken om te zien hoe de mensen zich van één kanaal aan een andere bewegen?

U kunt een stroomvisualisatie met de dimensie van identiteitskaart van de Dataset gebruiken.

1. Aanmelden bij [analytics.adobe.com](https://analytics.adobe.com) en maak een leeg Workspace-project.
2. Klik op het tabblad Visualisatie aan de linkerkant en sleep een stroomvisualisatie naar het canvas aan de rechterkant.
3. Klik op het tabblad Componenten aan de linkerkant en sleep de dimensie &#39;Dataset ID&#39; naar de middelste locatie met het label &#39;Dimension of Item&#39;.
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

Als u de de afmetingspunten van identiteitskaart van de dataset zou willen anders noemen, kunt u een raadplegingsdataset gebruiken.

## Hoe ver terug brengt CCA bezoekers?

Het terugkijkvenster voor het opnieuw beginnen hangt van uw gewenste frequentie van gegevens af [replay](replay.md). Bijvoorbeeld, als u opstelling CCA om gegevens eens per week opnieuw te spelen, is het raadplegingsvenster voor het opnieuw beginnen zeven dagen. Als u opstelling CCA om gegevens elke dag opnieuw te spelen, is het raadplegingsvenster voor het opnieuw beginnen één dag.

## Hoe worden gedeelde apparaten afgehandeld?

In sommige situaties, is het mogelijk dat de veelvoudige mensen van het zelfde apparaat login. De voorbeelden omvatten een gedeeld apparaat thuis, gedeelde PCs in een bibliotheek, of een kiosk in een detailhandelsafzet.

De tijdelijke id negeert de blijvende id, zodat gedeelde apparaten als afzonderlijke personen worden beschouwd (zelfs als ze van hetzelfde apparaat afkomstig zijn).

## Hoe behandelt CCA situaties waarin één enkele persoon vele blijvende IDs heeft?

In sommige situaties kan een individuele gebruiker veel permanente id&#39;s koppelen. Voorbeelden zijn voorbeelden waarbij een gebruiker vaak browsercookies wist of de modus Private/Incognito van de browser gebruikt.

Het aantal permanente id&#39;s is irrelevant ten gunste van de tijdelijke id. Één enkele gebruiker kan tot om het even welk aantal apparaten behoren zonder de capaciteit van CCA te beïnvloeden om over apparaten te hechten.

## Zodra ik mijn Team van de Rekening van de Adobe met de gewenste informatie contacteer, hoe lang duurt het voor de opgeklapte dataset beschikbaar wordt?

Livemetching is ongeveer een week beschikbaar nadat Adobe Kanaalanalyse heeft ingeschakeld. De beschikbaarheid van back-ups is afhankelijk van de hoeveelheid bestaande gegevens. De kleine datasets (minder dan 1 miljoen gebeurtenissen per dag) nemen typisch een paar dagen, terwijl de grote datasets (1 miljard gebeurtenissen per dag) een week of meer kunnen vergen.

## Wat is het verschil tussen de Analysefuncties voor apparaten (een functie in traditionele Analytics) en de Analysemogelijkheden voor meerdere kanalen?

[Apparaatanalyse](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html) is een functie die specifiek is voor traditionele Adobe Analytics en waarmee u kunt begrijpen hoe mensen op verschillende apparaten werken. Er zijn twee workflows om apparaatgegevens aan elkaar te koppelen: op het veld gebaseerde stitching en de apparaatgrafiek.

[Kanaaloverschrijdende analyse](/help/cca/overview.md) is een eigenschap specifiek voor CJA die u toestaat om te begrijpen hoe de mensen over zowel apparaten als kanalen werken. Het re-sleutel is de persoon identiteitskaart van een dataset, die die dataset toestaat om naadloos met andere datasets worden gecombineerd. Deze functie werkt op vergelijkbare wijze in het ontwerp als in de praktijk gebaseerde stitching van CDA, maar de implementatie doet zich anders voor dan de verschillende gegevensarchitectuur tussen traditionele Analytics en CJA.

## Hoe behandelt de Analysefuncties van het Kanaal GDPR en CCPA verzoeken?

Adobe behandelt verzoeken van de GDPR en de CCPA overeenkomstig de lokale en internationale wetgeving. Adobe biedt de [Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) verzoeken om toegang tot en verwijdering van gegevens in te dienen. De verzoeken zijn van toepassing op zowel de oorspronkelijke als de opgehaalde gegevensbestanden.

## Wat gebeurt er als het veld Persistent-id in een of meer gebeurtenissen leeg is?

Als de `Persistent ID` Het veld is leeg voor een gebeurtenis in een gegevensset die wordt vastgezet met een stitching op de basis, CCA vult de `Stitched ID` voor dat evenement op twee manieren :

* Als de `Transient ID` veld is niet leeg, CCA gebruikt de waarde in `Transient ID` als de `Stitched ID`.
* Als de `Transient ID` veld is leeg, CCA verlaat ook het veld `Stitched ID` leeg. In dit geval: `Persistent ID`, `Transient ID`, en `Stitched ID` zijn allemaal leeg op de gebeurtenis. Deze soorten gebeurtenissen worden gelaten vallen van om het even welke verbinding CJA gebruikend de dataset die waar wordt vastgemaakt `Stitched ID` is gekozen als `Person ID`.

## Hoe vergelijken de metriek in CJA gestitched datasets met gelijkaardige metriek in CJA unstitched datasets en met traditionele Adobe Analytics?

Bepaalde metriek in CJA zijn gelijkaardig aan metriek in traditionele Analytics, maar anderen zijn vrij verschillend, afhankelijk van wat u vergelijkt. In de onderstaande tabel worden verschillende gangbare meetwaarden vergeleken:

| **CJA-gebonden gegevens** | **Niet-opgeslagen CJA-gegevens** | **Traditioneel Adobe Analytics** | **Analytics Ultimate met CDA** |
| ----- | ----- | ----- | ----- |
| **Mensen** = Aantal verschillende `Person ID`s waar `Stitched ID` wordt gekozen als `Person ID`. **Mensen** kan hoger of lager zijn dan **Unieke bezoekers** in het traditionele Adobe Analytics, afhankelijk van de uitkomst van het stitching-proces. | **Mensen** = Aantal verschillende `Person ID`s is gebaseerd op de geselecteerde kolom `Person ID`. **Mensen** in de datasets van de Adobe Source Connector is vergelijkbaar met **Unieke bezoekers** in het traditionele Adobe Analytics als `endUserIDs._experience.aaid.id` wordt gekozen als `Person ID` in CJA. | **Unieke bezoekers** = Aantal verschillende bezoeker-id&#39;s. **Unieke bezoekers** mag niet hetzelfde zijn als het aantal afzonderlijke **ECID** s. | Zie [Mensen](https://experienceleague.adobe.com/docs/analytics/components/metrics/people.html). |
| **Sessies**: Gedefinieerd op basis van de sessie-instellingen in de CJA-gegevensweergave. Tijdens het koppelingsproces kunnen afzonderlijke sessies van meerdere apparaten in één sessie worden gecombineerd. | **Sessies**: Gedefinieerd op basis van de sessie-instellingen die zijn opgegeven in de CJA-gegevensweergave. | **Bezoeken**: Zie [Bezoeken](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html). | **Bezoeken**: Gedefinieerd op basis van de sessie-instellingen die zijn opgegeven in het dialoogvenster [Virtuele CDA-rapportenpakket](https://experienceleague.adobe.com/docs/analytics/components/cda/setup.html). |
| **Gebeurtenissen** = aantal rijen in de gegevens in de bijlage in CJA. Deze metrisch is typisch dicht bij **Voorval** in het traditionele Adobe Analytics. Opmerking: de veelgestelde vragen hierboven hebben betrekking op rijen met een lege pagina `Persistent ID`. | **Gebeurtenissen** = aantal rijen in de niet-ingestelde gegevens in CJA. Deze metrisch is typisch dicht bij **Voorval** in het traditionele Adobe Analytics. Houd er echter rekening mee dat gebeurtenissen leeg zijn `Person ID` in de ongeordende gegevens in Experience Platform data Lake, zijn deze gebeurtenissen niet opgenomen in CJA. | **Voorval**: Zie [Voorval](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html). | **Voorval**: Zie [Voorval](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html). |

Andere metriek kunnen gelijkaardig in CJA en traditionele Adobe Analytics zijn. Bijvoorbeeld het totale aantal voor Adobe Analytics [aangepaste gebeurtenissen](https://experienceleague.adobe.com/docs/analytics/components/metrics/custom-events.html) 1-100 is over het algemeen vergelijkbaar tussen traditionele Adobe Analytics en CJA (al dan niet gestikt). [Verschillen in mogelijkheden](/help/getting-started/aa-vs-cja/cja-aa.md)), zoals het dedupliceren van gebeurtenissen tussen CJA en traditionele Adobe Analytics, kan leiden tot discrepantie tussen de twee producten.

## Kan CCA de gebieden van de Kaart van de Identiteit gebruiken?

Nee, CCA kan momenteel geen identiteitskaartvelden gebruiken.
