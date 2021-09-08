---
title: Veelgestelde vragen over kanaalanalyse
description: Veelgestelde vragen voor kanaalanalyse
exl-id: 2ad78c19-4b13-495b-a0aa-44e0a3c95b5e
source-git-commit: 2be442915587780ce41f33b13e27b8cf44e239a6
workflow-type: tm+mt
source-wordcount: '976'
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

## Wat gebeurt er als het veld Persistent-id in een of meer gebeurtenissen leeg is?

Als het veld `Persistent ID` leeg is voor een gebeurtenis in een dataset die wordt gekoppeld aan een stitching op de basis van het veld, vult CCA `Stitched ID` voor die gebeurtenis op een van de volgende twee manieren in:
* Als het `Transient ID` gebied niet leeg is, gebruikt CCA de waarde in `Transient ID` als `Stitched ID`.
* Als het veld `Transient ID` leeg is, laat CCA ook de spatie `Stitched ID`. In dit geval zijn `Persistent ID`, `Transient ID` en `Stitched ID` allemaal leeg voor de gebeurtenis. Gebeurtenissen als deze worden weggelaten uit CJA in om het even welke verbinding CJA die de dataset gebruikt die wordt vastgemaakt waar `Stitched ID` als `Person ID` werd gekozen.

## Hoe vergelijken de metriek in CJA gestitched datasets met gelijkaardige metriek in CJA unstitched datasets en met traditionele Adobe Analytics?

Bepaalde metriek in CJA zijn gelijkaardig aan metriek in traditionele Analytics, maar anderen zijn vrij verschillend, afhankelijk van wat u vergelijkt. In de onderstaande tabel worden verschillende gangbare meetwaarden vergeleken:

| **CJA-gebonden gegevens** | **Niet-opgeslagen CJA-gegevens** | **Traditioneel Adobe Analytics** | **Analytics Ultimate met CDA** |
| ----- | ----- | ----- | ----- |
| **People** = Aantal van verschillende  `Person ID`s waar  `Stitched ID` wordt gekozen als  `Person ID`. **Afhankelijk van het resultaat van het stitching-proces kunnen** mensen hoger of lager zijn dan  **Unieke** bezoekers in het traditionele Adobe Analytics. | **People** = Aantal van verschillende  `Person ID`s die op de kolom wordt gebaseerd die als  `Person ID`. wordt geselecteerd **De gegevenssets van** Peoplein Adobe Analytics Connector (ADC) zijn vergelijkbaar met  **Unique** Visitorsin Traditional Adobe Analytics als  `endUserIDs. _experience. aaid.id` wordt gekozen zoals  `Person ID` in CJA. | **Unieke bezoekers** = Aantal verschillende bezoeker-id&#39;s. **Unieke bezoekers** mogen niet hetzelfde zijn als het aantal verschillende **ECID** s. | Zie [Personen](https://experienceleague.adobe.com/docs/analytics/components/metrics/people.html?lang=en). |
| **Sessies**: Wordt gedefinieerd op basis van de sessionisatie-instellingen die zijn opgegeven in de CJA-gegevensweergave. Tijdens het koppelingsproces kunnen afzonderlijke sessies van meerdere apparaten in één sessie worden gecombineerd. | **Sessies**: Wordt gedefinieerd op basis van de sessionisatie-instellingen die zijn opgegeven in de CJA-gegevensweergave. | **Bezoeken**: Zie  [Bezoekingen](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=en). | **Bezoeken**: Wordt gedefinieerd op basis van de sessionisatie-instellingen die zijn opgegeven in de virtuele- [rapportsuite](https://experienceleague.adobe.com/docs/analytics/components/cda/setup.html?lang=en) van CDA. |
| **Events** = aantal rijen in de gegevens in de bijlage in CJA. In het algemeen moet dit in traditionele Adobe Analytics bijna **voorkomen** zijn. Opmerking: de veelgestelde vragen hierboven hebben betrekking op rijen met een lege `Persistent ID`. | **Events** = aantal rijen in de ongeordende gegevens in CJA. In het algemeen moet dit in traditionele Adobe Analytics bijna **voorkomen** zijn. Merk op, echter, dat als om het even welke gebeurtenissen een lege `Person ID` in de ongestitched gegevens in het gegevensmeer van AEP hebben, deze gebeurtenissen (niet inbegrepen) in CJA zullen worden gelaten vallen. | **Voorvallen**: Zie  [Voorvallen](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html?lang=en). | **Voorvallen**: Zie  [Voorvallen](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html?lang=en). |

Andere metriek kunnen gelijkaardig zijn in CJA en traditionele Adobe Analytics. Het totale aantal voor Adobe Analytics [aangepaste gebeurtenissen](https://experienceleague.adobe.com/docs/analytics/components/metrics/custom-events.html?lang=en) (gebeurtenissen 1-100) moet in het algemeen zeer dicht bij de traditionele Adobe Analytics en CJA liggen (vast of niet gekoppeld). Dit is echter niet altijd het geval vanwege verschillen in mogelijkheden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-aa.html?lang=en), zoals het dedupliceren van gebeurtenissen tussen CJA en traditionele Adobe Analytics.[
