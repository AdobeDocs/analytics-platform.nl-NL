---
title: Overzicht van tekenreeksen
description: Overzicht van stitching.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
source-git-commit: 52d47e777e8c9f7e1e73f4131f19d7df280cb2a3
workflow-type: tm+mt
source-wordcount: '1322'
ht-degree: 0%

---

# Overzicht van tekenreeksen

Identiteitsstitching (of eenvoudig, stitching) is een krachtige eigenschap die de geschiktheid van een gebeurtenisdataset voor kanaalanalyse verhoogt. De analyse van het dwars-kanaal is een belangrijkste gebruiksgeval dat de Customer Journey Analytics kan behandelen, toestaand u om rapporten over veelvoudige datasets van verschillende kanalen naadloos te combineren en in werking te stellen, die op een gemeenschappelijke herkennings (persoonidentiteitskaart) worden gebaseerd.

Wanneer u datasets met gelijkaardige persoon IDs combineert, wordt de attributie gedragen over apparaten en kanalen. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Die gebruiker ontmoet een kwestie met hun orde, dan geeft uw team van de klantendienst een vraag om het te helpen oplossen. Met kanaalanalyse, kunt u de gebeurtenissen van het vraagcentrum aan de advertentie toeschrijven die zij oorspronkelijk klikte.

Jammer genoeg, niet alle op gebeurtenis-gebaseerde datasets die deel van uw verbinding in Customer Journey Analytics uitmaken zijn voldoende bevolkt met gegevens om deze attributie uit de doos te steunen. Vooral web-based of mobiel-gebaseerde ervaringsdatasets hebben vaak geen daadwerkelijke informatie van persoonidentiteitskaart beschikbaar over alle gebeurtenissen.

Door middel van tekenreeksen kunnen identiteiten binnen rijen van één gegevensset opnieuw worden ingesteld, zodat de persoon-id (naastgelegen ID) voor elke gebeurtenis beschikbaar is. Bij het zoeken naar gebruikersgegevens van zowel geverifieerde als niet-geverifieerde sessies wordt de gangbare waarde voor de tijdelijke id bepaald die kan worden gebruikt als aangesloten id. Door dit opnieuw activeren kunnen afwijkende records worden omgezet in één naadloze id voor analyse op persoonlijke niveau in plaats van op apparaat- of cookieniveau.

U profiteert van kanaalanalyse als u één of meerdere van uw gestikte datasets met andere datasets, zoals de gegevens van het vraagcentrum, als deel van het bepalen van uw verbinding van de Customer Journey Analytics combineert. Dit veronderstelt dat die andere datasets reeds een persoonsidentiteitskaart op elke rij, gelijkend op stitched ID bevatten.


## Vereisten

{{select-package}}

>[!IMPORTANT]
>
>Als niet aan alle voorwaarden wordt voldaan, kan de analyse van meerdere kanalen niet correct worden uitgevoerd.

Voordat u stitching gebruikt, moet u ervoor zorgen dat uw organisatie is voorbereid met het volgende:

* Importeer de gewenste gegevens naar Adobe Experience Platform:

   * Zie voor Adobe Analytics-gegevens [Adobe Analytics-rapportsuite gebruiken in Customer Journey Analytics](/help/getting-started/aa-vs-cja/aa-data-in-cja.md).
   * Zie voor andere typen gegevens [Een schema maken](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) en [Samenvattingsgegevens](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html) in de documentatie van Adobe Experience Platform.

* De dataset van de gebeurtenis in Adobe Experience Platform waarop u het stitching wilt toepassen moet twee kolommen hebben die bezoekers helpen identificeren:

   * A **blijvende id**, een id aanwezig op elke rij. Bijvoorbeeld een bezoekersidentiteitskaart die door een bibliotheek van het AppMeasurement van Adobe Analytics of een ECID wordt geproduceerd door de Dienst van de Identiteit van Adobe Experience Cloud.
   * A **transient ID**, een id die alleen op bepaalde rijen voorkomt. Een gehashte gebruikersnaam of e-mailadres bijvoorbeeld wanneer een bezoeker de verificatie uitvoert. U kunt vrijwel elke gewenste id gebruiken. Bij het plaatsen wordt in dit veld rekening gehouden met de werkelijke gegevens van de persoon-id. Voor de beste stitching resultaten, zou een transient identiteitskaart binnen de gebeurtenissen van de dataset minstens eens voor elke blijvende identiteitskaart moeten worden verzonden.
Als u van plan bent om deze dataset binnen een verbinding van de Customer Journey Analytics te omvatten, is het verkieslijk dat de andere datasets ook een gelijkaardige gemeenschappelijke herkenningsteken hebben.

* Onder andere het samenvoegen van geverifieerde en niet-geverifieerde gebruikersgegevens wordt opgenomen. Zorg ervoor dat u aan de toepasselijke wetten en verordeningen, met inbegrip van het verkrijgen van noodzakelijke eindgebruikertoestemmingen voldoet, alvorens het stitching op een gebeurtenisdataset te activeren.


## Sstitching gebruiken

Zodra uw organisatie aan alle voorwaarden voldoet en begrijpt [beperkingen](#limitations)kunt u de volgende stappen volgen om het stitching in de Customer Journey Analytics te beginnen:

### Ondersteuning aanvragen

1. Neem contact op met de Klantenondersteuning van de Adobe met de volgende informatie:

   * Een verzoek om stitching in te schakelen.
   * De dataset-id voor de gegevensset die u opnieuw wilt invoeren.
   * De kolomnaam van blijvende identiteitskaart voor de gewenste dataset (Identifier die op elke rij verschijnt).
   * De kolomnaam van transient identiteitskaart voor gewenste dataset (persoonsidentificatie, die ook als verbinding tussen datasets in de context van een verbinding dienst doet).
   * Je voorkeur van [replay](explained.md) frequentie en terugkijklengte. De opties omvatten een replay eens per week met een 7 dagen terugkijkvenster, of een replay elke dag met een 1 dag terugkijkvenster.
   * Naam van sandbox.


2. De klantenondersteuning van de Adobe werkt samen met Adobe-engineering om het aansluiten bij ontvangst van uw verzoek mogelijk te maken. Als deze optie is ingeschakeld, wordt in Adobe Experience Platform een nieuwe, opnieuw weergegeven gegevensset met een nieuwe kolom Titel ID weergegeven. De Steun van de Klant van de Adobe kan identiteitskaart van de nieuwe dataset verstrekken.

3. Als de Adobe voor het eerst is ingeschakeld, wordt een back-up van de gegevens gemaakt die 60 dagen teruggaat.

4. Als u de nieuwe gestikte dataset in een dwars-kanaalanalyse wilt gebruiken, moet u het aan een toevoegen [verbinding](../connections/overview.md) in Customer Journey Analytics samen met andere vereiste gegevensreeksen. Kies correcte persoon identiteitskaart voor elke dataset.

5. [Een gegevensweergave maken](/help/data-views/create-dataview.md) op basis van de verbinding.

<!-- To do: Paragraph on backfill once product and marketing determine the best way forward. -->

Zodra de gegevensmening opstelling is, kunt u uw Customer Journey Analytics het melden analyse over kanalen en apparaten in werking stellen.

<!-- Uncomment once stitching UI is available (for limited testing)..

### Do It Yourself

|Positive|[!BADGE New Feature]{type=Positive before-title="false"}|

{{release-limited-testing-section}}

Alternatively, you can set up and use stitching through the Customer Journey Analytics user interface:

1. Go to the [Create and manage stitched datasets](stitching-ui.md) and follow steps to rekey your dataset.

2. [Create a connection](/help/connections/create-connection.md) in Customer Journey Analytics using the newly generated dataset and any other datasets that you want to include. Choose the correct person ID for each dataset.

3. [Create a connection](/help/connections/create-connection.md) in Customer Journey Analytics using the newly generated dataset and any other datasets that you want to include. Choose the correct person ID for each dataset.
   
4. [Create a data view](/help/data-views/create-dataview.md) based on the connection.

Once the data view is set up, the cross-channel analysis in Customer Journey Analytics is just like any other analysis in Customer Journey Analytics, except now the data operates across channels and devices.

-->


## Beperkingen

>[!IMPORTANT]
>
>* Pas om het even welke verandering toe die u aan het globale schema van de gebeurtenisdataset ook aan het nieuwe gesloten datasetschema aanbrengt, anders breekt het de gestikte dataset.
>
>* Als u de brondataset verwijdert, stopt de gestikte dataset verwerking en wordt verwijderd door het systeem.
>
>* De etiketten van het gebruik van gegevens worden niet automatisch verspreid aan het gestikte datasetschema. Als u de etiketten van het gegevensgebruik hebt die op het schema van de brondataset worden toegepast, moet u deze etiketten van het gegevensgebruik op het gestikte datasetschema manueel toepassen. Zie [Labels voor gegevensgebruik beheren in Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=en) voor meer informatie .

Stikken is een baanbrekende en robuuste functie, maar heeft beperkingen op de manier waarop het kan worden gebruikt.

* De huidige mogelijkheden voor opnieuw aanvragen zijn beperkt tot één stap (permanente id tot tijdelijke id). Het opnieuw activeren in meerdere stappen (bijvoorbeeld een blijvende id naar een tijdelijke id en een andere tijdelijke id) wordt niet ondersteund.
* Alleen gegevenssets voor gebeurtenissen worden ondersteund. Andere datasets, zoals raadplegingsdatasets, worden niet gesteund.
* Aangepaste id-kaarten die in uw organisatie worden gebruikt, worden niet ondersteund.
* Bij het aanbrengen van een stift wordt het veld dat voor stitching wordt gebruikt, op geen enkele wijze getransformeerd. Bij het aanbrengen van tekenreeksen wordt de waarde in het opgegeven veld gebruikt zoals deze bestaat in de ongeordende gegevensset in het gegevensmeer. Het stitching proces is case-sensitive. Als bijvoorbeeld soms het woord &#39;Bob&#39; in het veld wordt weergegeven en soms het woord &#39;BOB&#39; wordt weergegeven, worden deze id&#39;s behandeld als twee aparte personen.
* Het plaatsen is case-sensitive. Voor datasets die door de de bronschakelaar van de Analyse worden geproduceerd, adviseert de Adobe om het even welke regels van VISTA of verwerkingsregels te herzien die op het transient gebied van identiteitskaart van toepassing zijn. Deze controle zorgt ervoor dat geen van deze regels nieuwe vormen van zelfde identiteitskaart introduceert. U moet er bijvoorbeeld voor zorgen dat er geen VISTA- of verwerkingsregels zijn die een lagere waarde invoeren in het veld met de tijdelijke id voor slechts een gedeelte van de gebeurtenissen.
* Bij het aanbrengen van titels worden velden niet gecombineerd of samengevoegd.
* Het veld transient ID moet één type id bevatten (id&#39;s uit één naamruimte). Het veld Tijdelijke id mag bijvoorbeeld geen combinatie bevatten van aanmeldings-id&#39;s en e-mailid&#39;s.
* Als er meerdere gebeurtenissen plaatsvinden met dezelfde tijdstempel voor dezelfde permanente id, maar met verschillende waarden in het veld voor de tijdelijke id, wordt de id geselecteerd door stitching op basis van alfabetische volgorde. Dus als de blijvende id A twee gebeurtenissen heeft met dezelfde tijdstempel en een van de gebeurtenissen Bob opgeeft en de andere de Ann, selecteert u Ann door te stitching.
* Als een apparaat door veelvoudige mensen wordt gedeeld en het totale aantal overgangen tussen gebruikers overschrijdt 50.000, houdt de Customer Journey Analytics het stitching van gegevens voor dat apparaat op.
* Wees voorzichtig met scenario&#39;s waarin de tijdelijke id&#39;s plaatsaanduidingswaarden bevatten, bijvoorbeeld &#39;Ongedefinieerd&#39;. Zie [Veelgestelde vragen](faq.md) voor meer informatie .

Let op het verschil tussen aanstikken en:

* De samenvoeging van twee of meer datasets. Stitching is slechts op één dataset van toepassing. Het samenvoegen van datasets komt als resultaat van vestiging een verbinding van de Customer Journey Analytics voor en het selecteren van zelfde identiteitskaart van de Persoon over de geselecteerde datasets in de verbinding.

* De verbinding van twee datasets. In Customer Journey Analytics, wordt een verbinding vaak gebruikt voor raadplegingen of classificaties in Analysis Workspace. Hoewel het stitching gebruikmaakt verbind zich aan functionaliteit, impliceert het proces zelf meer dan verbindingen.




