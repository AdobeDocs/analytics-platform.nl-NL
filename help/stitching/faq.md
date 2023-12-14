---
title: Veelgestelde vragen over tekst
description: Veelgestelde vragen over Stitching
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
exl-id: f4115164-7263-40ad-9706-3b98d0bb7905
source-git-commit: 53d394feb7d1132ad6339bae0e980f32bfe2ee6f
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 1%

---

# Veelgestelde vragen

Hier volgen een aantal veelgestelde vragen over stitching:

+++**Hoe kan ik stitching gebruiken om te zien hoe mensen zich van één kanaal aan een andere bewegen?**

U kunt een stroomvisualisatie met de dimensie van identiteitskaart van de Dataset gebruiken.

1. Aanmelden bij [Customer Journey Analytics](https://analytics.adobe.com) en maak een leeg Workspace-project.
2. Selecteer de **[!UICONTROL ** Visualisaties **]** en sleep een **[!UICONTROL ** Stroom **]** visualisatie naar het canvas aan de rechterkant.
3. Selecteer de **[!UICONTROL ** Componenten **]** aan de linkerkant en sleep de dimensie **[!UICONTROL ** Dataset-id **]** naar de middelste locatie met het label **[!UICONTROL ** Dimension of item **]**.
4. Dit stroomrapport is interactief. Als u de stromen naar volgende of vorige pagina&#39;s wilt uitbreiden, selecteert u een van de waarden. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

Als u de de afmetingspunten van identiteitskaart van de dataset zou willen anders noemen, kunt u een raadplegingsdataset gebruiken.

+++

+++**Hoe ver is het stitching replay bezoekers?**

Het terugkijkvenster voor het opnieuw beginnen hangt van uw gewenste frequentie van gegevens af [replay](explained.md). Als u bijvoorbeeld stitching instelt om gegevens eenmaal per week opnieuw af te spelen, is het terugzoekvenster voor het opnieuw afspelen zeven dagen. Als u stitching opstelling om gegevens elke dag opnieuw te spelen, is het raadplegingsvenster voor het opnieuw beginnen één dag.

+++

+++**Hoe worden gedeelde apparaten afgehandeld?**

In sommige situaties, is het mogelijk dat de veelvoudige mensen van het zelfde apparaat login. De voorbeelden omvatten een gedeeld apparaat thuis, gedeelde PCs in een bibliotheek, of een kiosk in een detailhandelsafzet.

De tijdelijke id negeert de blijvende id, zodat gedeelde apparaten als afzonderlijke personen worden beschouwd (zelfs als ze van hetzelfde apparaat afkomstig zijn).

+++

+++**Hoe kan stitching situaties verwerken waarin één persoon vele blijvende IDs heeft?**

In sommige situaties kan een individuele gebruiker veel permanente id&#39;s koppelen. Een voorbeeld hiervan is dat een gebruiker vaak de cookies van de browser wist of de persoonlijke/incognitomodus van de browser gebruikt.

Het aantal permanente id&#39;s is irrelevant ten gunste van de tijdelijke id. Eén gebruiker kan tot een willekeurig aantal apparaten behoren zonder dat dit invloed heeft op de mogelijkheid van de Customer Journey Analytics om aan de andere apparaten te hechten.

+++

+++**Zodra ik mijn Team van de Rekening van de Adobe van het Team met de gewenste informatie contacteer, hoe lang duurt het voor de opgeklapte dataset om beschikbaar te worden?**

Livestitching is ongeveer een week beschikbaar nadat de Adobe stitching mogelijk maakt. De beschikbaarheid van back-ups is afhankelijk van de hoeveelheid bestaande gegevens. Kleine datasets (minder dan 1 miljoen gebeurtenissen per dag) nemen doorgaans een paar dagen in beslag, terwijl grote gegevenssets (1 miljard gebeurtenissen per dag) een week of meer kunnen duren.

+++

+++**Wat is het verschil tussen apparaatanalyse (een functie in traditionele Analytics) en kanaalanalyse?**

[Apparaatanalyse](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html) is een functie die specifiek is voor traditionele Adobe Analytics en waarmee u kunt begrijpen hoe mensen op verschillende apparaten werken. Er zijn twee workflows om apparaatgegevens aan elkaar te koppelen: op het veld gebaseerde stitching en de apparaatgrafiek.

Kanaaloverschrijdende analyse is een gebruiksgeval specifiek voor Customer Journey Analytics die u toestaat om te begrijpen hoe de mensen over zowel apparaten als kanalen werken. Het stitches de de persoonsidentiteitskaart van een dataset, toestaand die dataset om naadloos met andere datasets worden gecombineerd. Deze functie werkt op vergelijkbare wijze in ontwerpen als op het veld gebaseerde koppelingen voor apparaatanalyse, maar de implementatie is anders vanwege de verschillende gegevensarchitectuur tussen traditionele analyse en Customer Journey Analytics. Zie [Stiksel](overview.md) en de [kanaalanalyse](../use-cases/cross-channel/cross-channel.md) Gebruik hoofdletters/kleine letters voor meer informatie.

+++

+++**Hoe behandelt Stitching privacyverzoeken?**

Adobe behandelt verzoeken om privacy in overeenstemming met de lokale en internationale wetgeving. Adobe biedt de [Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) verzoeken om toegang tot en verwijdering van gegevens in te dienen. De verzoeken zijn van toepassing op zowel de oorspronkelijke als de opgehaalde gegevensbestanden.

+++

+++**Wat gebeurt er als het veld Persistent-id in een of meer gebeurtenissen leeg is?**

Als het veld Persistent-id leeg is voor een gebeurtenis in een gegevensset die wordt vastgezet, kunt u de opgetekende id voor die gebeurtenis op twee manieren bepalen:

* Als het veld Tijdelijke id niet leeg is, gebruikt de Customer Journey Analytics de waarde in Voorlopige id als de titel-id.
* Als het veld Transient ID leeg is, laat Customer Journey Analytics de id Stitched leeg. In dit geval zijn Persistente ID, Transient ID en Stitched ID allemaal leeg voor de gebeurtenis. Deze soorten gebeurtenissen worden gelaten vallen van om het even welke verbinding van de Customer Journey Analytics gebruikend de dataset die wordt vastgemaakt waar Stitched ID als Persoon identiteitskaart werd gekozen.

+++


+++**Wat gebeurt er als het veld Tijdelijke id in een of meer gebeurtenissen plaatsaanduidingswaarden heeft, zoals &#39;Niet gedefinieerd&#39;?**

Wees voorzichtig met &#39;samenvouwen van persoon&#39;, wat optreedt wanneer het naaien wordt toegepast op gegevens die plaatsaanduidingswaarden gebruiken voor tijdelijke id&#39;s. In de onderstaande voorbeeldtabel worden niet-gedefinieerde personen-id&#39;s die afkomstig zijn van een gegevensset die afkomstig is van een CRM-systeem, gevuld met de waarde &#39;Ongedefinieerd&#39;, wat resulteert in een onjuiste weergave van personen.

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Transient ID (aanmeldings-id) | Id met titel (na opnieuw afspelen) |
|---|---|---|---|---|
| 1 | 2023-05-12 12:01 | 123 | - | **Cory** |
| 2 | 2023-05-12 12:02 | 123 | Cory | **Cory** |
| 3 | 2023-05-12 12:03 | 456 | Ongedefinieerd | **Ongedefinieerd** |
| 4 | 2023-05-12 12:04 | 456 | - | **Ongedefinieerd** |
| 5 | 2023-05-12 12:05 | 789 | Ongedefinieerd | **Ongedefinieerd** |
| 6 | 2023-05-12 12:06 | 012 | Ongedefinieerd | **Ongedefinieerd** |
| 7 | 2023-05-12 12:07 | 012 | - | **Ongedefinieerd** |
| 8 | 2023-05-12 12:03 | 789 | Ongedefinieerd | **Ongedefinieerd** |
| 9 | 2023-05-12 12:09 | 456 | - | **Ongedefinieerd** |
| 10 | 2023-05-12 12:02 | 123 | - | **Cory** |
| | | **4 apparaten** | **2 personen**:<br/>Gebeurtenissen 1, 4, 7, 9, 10 vervallen | **2 personen**:<br/>Cory, niet geverifieerd (samengevouwen tot één persoon) |

+++

+++**Hoe vergelijken de metriek in Customer Journey Analytics gestikte datasets met gelijkaardige metriek in Customer Journey Analytics unstitched datasets en met Adobe Analytics?**

Bepaalde metriek in Customer Journey Analytics zijn gelijkaardig aan metriek in traditionele Analytics, maar anderen zijn verschillend, afhankelijk van wat u vergelijkt. In de onderstaande tabel worden verschillende gangbare meetwaarden vergeleken:

| **Customer Journey Analytics, gebonden gegevens** | **Customer Journey Analytics ongestipte gegevens** | **Adobe Analytics** | **Analytics Ultimate met CDA** |
| ----- | ----- | ----- | ----- |
| **Mensen** = Aantal verschillende personen-id&#39;s waarbij de id met titel is gekozen als Persoon-id. **Mensen** hoger of lager dan **Unieke bezoekers** in het traditionele Adobe Analytics, afhankelijk van de uitkomst van het stitching-proces. | **Mensen** = Aantal verschillende persoon-id&#39;s op basis van de kolom die is geselecteerd als Persoon-id. **Mensen** in de gegevenssets van de bronconnector van Analytics is vergelijkbaar met **Unieke bezoekers** in het traditionele Adobe Analytics als `endUserIDs._experience.aaid.id` wordt gebruikt als persoon-id in de Customer Journey Analytics. | **Unieke bezoekers** = Aantal verschillende bezoeker-id&#39;s. **Unieke bezoekers** mag niet hetzelfde zijn als het aantal afzonderlijke **ECID** s. | Zie [Mensen](https://experienceleague.adobe.com/docs/analytics/components/metrics/people.html). |
| **Sessies**: Gedefinieerd op basis van de sessie-instellingen in de gegevensweergave Customer Journey Analytics. Tijdens het koppelingsproces kunnen afzonderlijke sessies van meerdere apparaten in één sessie worden gecombineerd. | **Sessies**: Gedefinieerd op basis van de sessie-instellingen die zijn opgegeven in de gegevensweergave Customer Journey Analytics. | **Bezoeken**: Zie [Bezoeken](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html). | **Bezoeken**: Gedefinieerd op basis van de sessie-instellingen die in het dialoogvenster [Virtuele CDA-rapportenpakket](https://experienceleague.adobe.com/docs/analytics/components/cda/setup.html). |
| **Gebeurtenissen** = aantal rijen in de gestikte gegevens in Customer Journey Analytics. Deze metrisch is typisch dicht bij **Voorval** in Adobe Analytics. Opmerking: de veelgestelde vragen hierboven hebben betrekking op rijen met een lege permanente id. | **Gebeurtenissen** = aantal rijen in de niet-ingestelde gegevens in Customer Journey Analytics. Deze metrisch is typisch dicht bij **Voorval** in Adobe Analytics. Merk op, echter, dat als om het even welke gebeurtenissen een lege identiteitskaart van de Persoon in de unstitched gegevens in het gegevensmeer van het Experience Platform hebben, deze gebeurtenissen niet inbegrepen in Customer Journey Analytics zijn. | **Voorval**: Zie [Voorval](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html). | **Voorval**: Zie [Voorval](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html). |

Andere meetgegevens zijn vergelijkbaar in Customer Journey Analytics en Adobe Analytics. Bijvoorbeeld het totale aantal voor Adobe Analytics [aangepaste gebeurtenissen](https://experienceleague.adobe.com/docs/analytics/components/metrics/custom-events.html) 1-100 is vergelijkbaar tussen traditionele Adobe Analytics en Customer Journey Analytics (al dan niet gestikt). [Verschillen in mogelijkheden](/help/getting-started/aa-vs-cja/cja-aa.md)), zoals deduplicatie van gebeurtenissen tussen Customer Journey Analytics en Adobe Analytics, kan leiden tot discrepantie tussen beide producten.

+++

+++**Kan de Customer Journey Analytics de gebieden van de Kaart van de Identiteit gebruiken?**

Nee, Customer Journey Analytics kan de identiteitskaartvelden momenteel niet gebruiken voor stitching.

+++
