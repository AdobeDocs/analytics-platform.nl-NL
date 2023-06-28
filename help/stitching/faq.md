---
title: Veelgestelde vragen
description: Veelgestelde vragen over Stitching
solution: Customer Journey Analytics
feature: Stitching
source-git-commit: ec316d36c1e2ec6eb6e75e980ad3fed4ededfb94
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 0%

---

# Veelgestelde vragen

Hieronder vindt u enkele veelgestelde vragen over stitching:

## Hoe kan ik stitching gebruiken om te zien hoe mensen zich van één kanaal aan een andere bewegen?

U kunt een stroomvisualisatie met de dimensie van identiteitskaart van de Dataset gebruiken.

1. Aanmelden bij [Customer Journey Analytics](https://analytics.adobe.com) en maak een leeg Workspace-project.
2. Selecteer **[!UICONTROL ** Visualisaties **]** en sleep een **[!UICONTROL ** Stroom **]** visualisatie naar het canvas aan de rechterkant.
3. Selecteer **[!UICONTROL ** Componenten **]** aan de linkerkant en sleep de dimensie **[!UICONTROL ** Dataset-id **]** naar de middelste locatie met het label **[!UICONTROL ** Dimension of item **]**.
4. Dit stroomrapport is interactief. Als u de stromen naar volgende of vorige pagina&#39;s wilt uitbreiden, selecteert u een van de waarden. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

Als u de de afmetingspunten van identiteitskaart van de dataset zou willen anders noemen, kunt u een raadplegingsdataset gebruiken.

## Hoe ver is het stitching replay bezoekers?

Het terugkijkvenster voor het opnieuw beginnen hangt van uw gewenste frequentie van gegevens af [replay](explained.md). Als u bijvoorbeeld stitching instelt om gegevens eenmaal per week opnieuw af te spelen, is het terugzoekvenster voor opnieuw afspelen zeven dagen. Als u stitching opstelling om gegevens elke dag opnieuw te spelen, is het raadplegingsvenster voor het opnieuw beginnen één dag.

## Hoe worden gedeelde apparaten afgehandeld?

In sommige situaties, is het mogelijk dat de veelvoudige mensen van het zelfde apparaat login. De voorbeelden omvatten een gedeeld apparaat thuis, gedeelde PCs in een bibliotheek, of een kiosk in een detailhandelsafzet.

De tijdelijke id negeert de blijvende id, zodat gedeelde apparaten als afzonderlijke personen worden beschouwd (zelfs als ze van hetzelfde apparaat afkomstig zijn).

## Hoe kan stitching situaties verwerken waarin één persoon vele blijvende IDs heeft?

In sommige situaties kan een individuele gebruiker veel permanente id&#39;s koppelen. Een voorbeeld hiervan is dat een gebruiker vaak de cookies van de browser wist of de persoonlijke/incognitomodus van de browser gebruikt.

Het aantal permanente id&#39;s is irrelevant ten gunste van de tijdelijke id. Eén gebruiker kan tot een willekeurig aantal apparaten behoren zonder dat dit invloed heeft op de mogelijkheid van de Analytics van de Klant om apparaten te doorverbinden.

## Zodra ik mijn Team van de Rekening van de Adobe met de gewenste informatie contacteer, hoe lang duurt het voor de opgeklapte dataset beschikbaar wordt?

Livestitching is ongeveer een week beschikbaar nadat Adobe stitching mogelijk maakt. De beschikbaarheid van back-ups is afhankelijk van de hoeveelheid bestaande gegevens. Kleine datasets (minder dan 1 miljoen gebeurtenissen per dag) nemen doorgaans een paar dagen in beslag, terwijl grote gegevenssets (1 miljard gebeurtenissen per dag) een week of meer kunnen duren.

## Wat is het verschil tussen apparaatanalyse (een functie in traditionele Analytics) en kanaalanalyse?

[Apparaatanalyse](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html) is een functie die specifiek is voor traditionele Adobe Analytics en waarmee u kunt begrijpen hoe mensen op verschillende apparaten werken. Er zijn twee workflows om apparaatgegevens aan elkaar te koppelen: op het veld gebaseerde stitching en de apparaatgrafiek.

Kanaaloverschrijdende analyse is een gebruiksgeval specifiek voor Customer Journey Analytics die u toestaat om te begrijpen hoe de mensen over zowel apparaten als kanalen werken. Het stitches de de persoonsidentiteitskaart van een dataset, toestaand die dataset om naadloos met andere datasets worden gecombineerd. Deze functie werkt op vergelijkbare wijze in ontwerpen als op het veld gebaseerde stitching voor apparaatanalyse, maar de implementatie is anders vanwege de verschillende gegevensarchitectuur tussen traditionele Analytics en Customer Journey Analytics. Zie [Stiksel](overview.md) en de [kanaalanalyse](../use-cases/cross-channel/cross-channel.md) Gebruik hoofdletters/kleine letters voor meer informatie.

## Hoe behandelt Stitching GDPR en CCPA verzoeken?

Adobe behandelt verzoeken van de GDPR en de CCPA overeenkomstig de lokale en internationale wetgeving. Adobe biedt de [Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) verzoeken om toegang tot en verwijdering van gegevens in te dienen. De verzoeken zijn van toepassing op zowel de oorspronkelijke als de opgehaalde gegevensbestanden.

## Wat gebeurt er als het veld Persistent-id in een of meer gebeurtenissen leeg is?

Als het veld Persistent-id leeg is voor een gebeurtenis in een gegevensset die wordt vastgezet, kunt u de opgetekende id voor die gebeurtenis op twee manieren bepalen:

* Als het veld Transient ID niet leeg is, gebruikt Customer Journey Analytics de waarde in Transient ID als de Stitched ID.
* Als het veld Tijdelijke id leeg is, laat Customer Journey Analytics ook de lege id met titel. In dit geval zijn Persistente ID, Transient ID en Stitched ID allemaal leeg voor de gebeurtenis. Deze soorten gebeurtenissen worden gelaten vallen van om het even welke verbinding van Customer Journey Analytics gebruikend de dataset die waar Gestitched identiteitskaart als Persoon identiteitskaart werd gekozen.

## Hoe verhouden de metriek in Customer Journey Analytics gestikte datasets zich met gelijkaardige metriek in Customer Journey Analytics niet-stitched datasets en met traditionele Adobe Analytics?

Bepaalde metriek in Customer Journey Analytics zijn vergelijkbaar met metriek in traditionele Analytics, maar andere cijfers zijn anders, afhankelijk van wat u vergelijkt. In de onderstaande tabel worden verschillende gangbare meetwaarden vergeleken:

| **Customer Journey Analytics-gegevens** | **Customer Journey Analytics gegevens niet ingesloten** | **Traditioneel Adobe Analytics** | **Analytics Ultimate met CDA** |
| ----- | ----- | ----- | ----- |
| **Mensen** = Aantal verschillende personen-id&#39;s waarbij de id met titel is gekozen als Persoon-id. **Mensen** kan hoger of lager zijn dan **Unieke bezoekers** in het traditionele Adobe Analytics, afhankelijk van de uitkomst van het stitching-proces. | **Mensen** = Aantal verschillende persoon-id&#39;s op basis van de kolom die is geselecteerd als Persoon-id. **Mensen** in de datasets van de Adobe Source Connector is vergelijkbaar met **Unieke bezoekers** in het traditionele Adobe Analytics als `endUserIDs._experience.aaid.id` wordt gebruikt als persoon-id in Customer Journey Analytics. | **Unieke bezoekers** = Aantal verschillende bezoeker-id&#39;s. **Unieke bezoekers** mag niet hetzelfde zijn als het aantal afzonderlijke **ECID** s. | Zie [Mensen](https://experienceleague.adobe.com/docs/analytics/components/metrics/people.html). |
| **Sessies**: Gedefinieerd op basis van de sessie-instellingen in de gegevensweergave Customer Journey Analytics. Tijdens het koppelingsproces kunnen afzonderlijke sessies van meerdere apparaten in één sessie worden gecombineerd. | **Sessies**: Gedefinieerd op basis van de sessie-instellingen die zijn opgegeven in de gegevensweergave Customer Journey Analytics. | **Bezoeken**: Zie [Bezoeken](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html). | **Bezoeken**: Gedefinieerd op basis van de sessie-instellingen die zijn opgegeven in het dialoogvenster [Virtuele CDA-rapportenpakket](https://experienceleague.adobe.com/docs/analytics/components/cda/setup.html). |
| **Gebeurtenissen** = het aantal rijen in de gegevens in de naakte positie in Customer Journey Analytics. Deze metrisch is typisch dicht bij **Voorval** in het traditionele Adobe Analytics. Opmerking: de veelgestelde vragen hierboven hebben betrekking op rijen met een lege permanente id. | **Gebeurtenissen** = aantal rijen in de niet-ingestelde gegevens in Customer Journey Analytics. Deze metrisch is typisch dicht bij **Voorval** in het traditionele Adobe Analytics. Merk op, echter, dat als om het even welke gebeurtenissen een lege identiteitskaart van de Persoon in de unstitched gegevens in het gegevensmeer van het Experience Platform hebben, deze gebeurtenissen niet inbegrepen in Customer Journey Analytics zijn. | **Voorval**: Zie [Voorval](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html). | **Voorval**: Zie [Voorval](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html). |

Andere cijfers kunnen vergelijkbaar zijn in Customer Journey Analytics en traditionele Adobe Analytics. Bijvoorbeeld het totale aantal voor Adobe Analytics [aangepaste gebeurtenissen](https://experienceleague.adobe.com/docs/analytics/components/metrics/custom-events.html) 1-100 is vergelijkbaar tussen traditionele Adobe Analytics en Customer Journey Analytics (al dan niet gestikt). [Verschillen in mogelijkheden](/help/getting-started/aa-vs-cja/cja-aa.md)), zoals deduplicatie van gebeurtenissen tussen Customer Journey Analytics en traditionele Adobe Analytics, kan leiden tot discrepantie tussen beide producten.

## Kan Customer Journey Analytics de gebieden van de Kaart van de Identiteit gebruiken?

Nee, Customer Journey Analytics kan de identiteitskaartvelden momenteel niet gebruiken voor stitching.
