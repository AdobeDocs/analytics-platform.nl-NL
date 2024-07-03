---
title: Overzicht van tekenreeksen
description: Overzicht van stitching.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
exl-id: 1c42efac-b3d2-437b-8b0b-9c6fdfed8520
role: Admin
source-git-commit: 805eb9dc9ab287934dd15eb56d3ac35187c979d7
workflow-type: tm+mt
source-wordcount: '3752'
ht-degree: 1%

---

# Stiksel

{{select-package}}

Identiteitsstitching (of eenvoudig, stitching) is een krachtige eigenschap die de geschiktheid van een gebeurtenisdataset voor kanaalanalyse verhoogt. De analyse van het dwars-kanaal is een belangrijkste gebruiksgeval dat de Customer Journey Analytics kan behandelen, toestaand u om rapporten naadloos op veelvoudige datasets van verschillende kanalen te combineren en in werking te stellen, die op een gemeenschappelijke herkennings (persoonID) wordt gebaseerd.

Wanneer u datasets met gelijkaardige persoon IDs combineert, wordt de attributie gedragen over apparaten en kanalen. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Die gebruiker ontmoet een kwestie met hun orde, dan geeft uw team van de klantendienst een vraag om het te helpen oplossen. Met kanaalanalyse, kunt u de gebeurtenissen van het vraagcentrum aan de advertentie toeschrijven die zij oorspronkelijk klikte.

Jammer genoeg, niet alle op gebeurtenis-gebaseerde datasets die deel van uw verbinding in Customer Journey Analytics uitmaken zijn voldoende bevolkt met gegevens om deze attributie uit de doos te steunen. Vooral web-based of mobiel-gebaseerde ervaringsdatasets hebben vaak geen daadwerkelijke informatie van persoonidentiteitskaart beschikbaar over alle gebeurtenissen.

Door middel van tekenreeksen kunnen identiteiten binnen rijen van één gegevensset opnieuw worden ingesteld, zodat de persoon-id (naastgelegen ID) voor elke gebeurtenis beschikbaar is. Bij het zoeken naar gebruikersgegevens van zowel geverifieerde als niet-geverifieerde sessies wordt de gemeenschappelijke waarde van de tijdelijke id (de persoon-id) bepaald die kan worden gebruikt als een vergrendelde id. Door dit opnieuw activeren kunnen afwijkende records worden omgezet in één naadloze id voor analyse op persoonlijke niveau in plaats van op apparaat- of cookieniveau.

Customer Journey Analytics ondersteunt twee typen stitching: stitching op basis van velden en stitching op basis van grafieken.

## Vereisten

>[!IMPORTANT]
>
>Als niet aan alle voorwaarden wordt voldaan, kan de analyse van meerdere kanalen niet correct worden uitgevoerd.

Voordat u stitching gebruikt, moet u ervoor zorgen dat uw organisatie is voorbereid met het volgende:

- Onder andere het samenvoegen van geverifieerde en niet-geverifieerde gebruikersgegevens wordt opgenomen. Zorg ervoor dat u aan de toepasselijke wetten en verordeningen, met inbegrip van het verkrijgen van noodzakelijke eindgebruikertoestemmingen voldoet, alvorens het stitching op een gebeurtenisdataset te activeren. Zie [Identiteitsvelden definiëren in de gebruikersinterface](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie .

- Importeer de gewenste gegevens naar Adobe Experience Platform:

   - Zie voor Adobe Analytics-gegevens [Adobe Analytics-rapportsuite gebruiken in Customer Journey Analytics](/help/getting-started/aa-vs-cja/aa-data-in-cja.md).
   - Zie voor andere typen gegevens [Een schema maken](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui) en [Samenvattingsgegevens](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home) in de documentatie van Adobe Experience Platform.

U profiteert van kanaalanalyse als u één of meerdere van uw gestikte datasets met andere datasets, zoals de gegevens van het vraagcentrum, als deel van het bepalen van uw verbinding van de Customer Journey Analytics combineert. Deze verbindingsconfiguratie veronderstelt dat die andere datasets reeds een persoonsidentiteitskaart op elke rij, gelijkend op vastgemaakte identiteitskaart bevatten.


## Beperkingen

>[!IMPORTANT]
>
>- Geen ondersteuning voor `identityMap` als de blijvende id. U moet een specifieke herkenningsteken in de dataset bepalen (bijvoorbeeld `ECID`) als de permanente id.
>
>- Pas om het even welke verandering toe die u aan het schema van de brongebeurtenisdataset ook aan het nieuwe gestikte datasetschema aanbrengt, anders breekt het de gestikte dataset.
>
>- Als u de brondataset verwijdert, stopt de gestikte dataset verwerking en wordt verwijderd door het systeem.
>
>- De etiketten van het gebruik van gegevens worden niet automatisch verspreid aan het gestikte datasetschema. Als u de etiketten van het gegevensgebruik hebt die op het schema van de brondataset worden toegepast, moet u deze etiketten van het gegevensgebruik manueel op het gestikte datasetschema toepassen. Zie [Labels voor gegevensgebruik beheren in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview) voor meer informatie .

Stikken is een baanbrekende en robuuste functie, maar heeft beperkingen op de manier waarop het kan worden gebruikt.

- Alleen gegevenssets voor gebeurtenissen worden ondersteund. Andere datasets, zoals raadplegingsdatasets, worden niet gesteund.
- Bij het aanbrengen van een stift wordt het veld dat voor stitching wordt gebruikt, op geen enkele wijze getransformeerd. Bij het aanbrengen van tekenreeksen wordt de waarde in het opgegeven veld gebruikt zoals deze bestaat in de ongeordende gegevensset in het gegevensmeer.
- Het stitching proces is case-sensitive. Als bijvoorbeeld soms het woord &#39;Bob&#39; in het veld wordt weergegeven en soms het woord &#39;BOB&#39; wordt weergegeven, worden deze id&#39;s behandeld als twee aparte personen.

Zorg ervoor dat u het stikken niet verwart met:

- De samenvoeging van twee of meer datasets. Stitching is slechts op één dataset van toepassing. Het samenvoegen van datasets vindt plaats als resultaat van vestiging een verbinding van de Customer Journey Analytics en het selecteren van zelfde persoonsidentiteitskaart over de geselecteerde datasets in de verbinding.

- De verbinding van twee datasets. In Customer Journey Analytics, wordt een verbinding vaak gebruikt voor raadplegingen of classificaties in Analysis Workspace. Hoewel het stitching gebruikmaakt verbind zich aan functionaliteit, impliceert het proces zelf meer dan verbindingen.


## Veldgebaseerde stitching

U geeft een gegevensset voor gebeurtenissen op, evenals de permanente id (cookie) en de tijdelijke id (ID van persoon) voor die gegevensset. Op veld gebaseerde stitching leidt tot een nieuwe gestippelde kolom van identiteitskaart in de nieuwe gestikte dataset en werkt deze stitched ID kolom bij die op rijen wordt gebaseerd die een transient identiteitskaart voor die specifieke blijvende identiteitskaart hebben. <br/>U kunt op gebied-gebaseerde het stitching gebruiken wanneer het gebruiken van Customer Journey Analytics als standalone oplossing (die geen toegang tot de Dienst van de Identiteit van het Experience Platform en bijbehorende identiteitsgrafiek heeft). Of als u de beschikbare identiteitsgrafiek niet wilt gebruiken.

![Veldgebaseerde stitching](/help/stitching/assets/fbs.png)

### Hoe veldomstandigheden stitching werkt

Met Stitching worden minimaal twee gegevenscontroles uitgevoerd in een bepaalde gegevensset.

- **Actief stiteren**: pogingen om elke hit (gebeurtenis) aan te hechten zodra deze wordt weergegeven. Hits van apparaten die &quot;nieuw&quot;aan de dataset (nooit voor authentiek verklaard) zijn worden typisch niet vastgemaakt op dit niveau. Hits van reeds herkende apparaten worden onmiddellijk vastgezet.

- **Replay stitching**: De gegevens worden opnieuw afgespeeld op basis van unieke id&#39;s (transient ID&#39;s) die door de id zijn geleerd. In dit stadium worden treffers van eerder onbekende apparaten (permanente id&#39;s) vastgezet (aan transient ID&#39;s). Adobe biedt twee herhalingsintervallen:
   - **Dagelijks**: Gegevens worden elke dag opnieuw afgespeeld met een terugzoekvenster van 24 uur. Deze optie biedt een voordeel dat het aantal keren wordt afgespeeld, maar niet-geregistreerde bezoekers moeten zich op dezelfde dag verifiëren dat ze uw site bezoeken.
   - **Wekelijks**: Gegevens worden één keer per week opnieuw afgespeeld met het geselecteerde terugzoekvenster (zie [opties](#options)). Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Niet-opgeslagen gegevens van minder dan een week oud worden echter pas opnieuw verwerkt wanneer de gegevens wekelijks opnieuw worden afgespeeld.

- **Privacy**: Wanneer verzoeken met betrekking tot privacy worden ontvangen, moet, naast het verwijderen van de gevraagde identiteit, elke koppeling van die identiteit tussen niet-geverifieerde gebeurtenissen ongedaan worden gemaakt.

Gegevens buiten het terugzoekvenster worden niet opnieuw afgespeeld. Een bezoeker moet binnen een bepaald terugkijkvenster voor een ongeautoriseerd bezoek en een voor authentiek verklaard bezoek voor authentiek verklaren om samen worden geïdentificeerd. Als een apparaat eenmaal is herkend, wordt het vanaf dat punt live vastgezet.

#### Stap 1: Actief stitching

Live stilzetten probeert elke gebeurtenis bij de verzameling aan te sluiten op bekende apparaten en kanalen.

+++ Details

Overweeg het volgende voorbeeld, waar het Loodje verschillende gebeurtenissen als deel van een gebeurtenisdataset registreert.

*Gegevens zoals deze op de dag van verzameling werden weergegeven:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Transient ID (aanmeldings-id) | Id met titel (na liveslot) |
|---|---|---|---|---|
| 1 | 2023-05-12 12:01 | `246` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`246`** |
| 2 | 2023-05-12 12:02 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` |
| 3 | 2023-05-12 12:03 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 4 | 2023-05-12 12:04 | `246` | - | **`Bob`** |
| 5 | 2023-05-12 12:05 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 6 | 2023-05-12 12:06 | `246` | - | **`Bob`** |
| 7 | 2023-05-12 12:07 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` |
| 8 | 2023-05-12 12:03 | `3579` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** |
| 9 | 2023-05-12 12:09 | `3579` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** |
| 10 | 2023-05-12 12:02 | `81911` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`81911`** |
| 11 | 2023-05-12 12:05 | `81911` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 12 | 2023-05-12 12:12 | `81911` | - | **`Bob`** |
| | | **3 apparaten** | | **4 personen**:<br/>`246`, `Bob`, `3579`, `81911` |

Zowel niet-geverifieerde als geverifieerde gebeurtenissen op nieuwe apparaten worden als afzonderlijke personen geteld (tijdelijk). Niet-geverifieerde gebeurtenissen op herkende apparaten worden live stilgezet.

Attributie werkt wanneer de identificerende aangepaste variabele aan een apparaat is gekoppeld. In het bovenstaande voorbeeld worden alle gebeurtenissen behalve de gebeurtenissen 1, 8, 9 en 10 live vernaakt (ze gebruiken allemaal de `Bob` id). Als u de stitching live uitvoert, wordt de geroteerde id voor gebeurtenis 4, 6 en 12 opgelost.

Vertraagde gegevens (gegevens met een tijdstempel van meer dan 24 uur oud) worden op de &#39;best mogelijke manier&#39; verwerkt, waarbij de voorkeur wordt gegeven aan het koppelen van huidige gegevens voor de hoogste kwaliteit.

+++

#### Stap 2: Spatiëring opnieuw afspelen

Met regelmatige intervallen (eenmaal per week of eenmaal per dag, afhankelijk van het gekozen terugkijkvenster) worden historische gegevens opnieuw berekend op basis van de apparaten die het nu herkent. Als een apparaat aanvankelijk gegevens verzendt terwijl niet voor authentiek verklaard en dan login, replay stitching bindt die niet voor authentiek verklaarde gebeurtenissen aan de correcte persoon.

+++ Details

In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar worden verschillende getallen weergegeven op basis van het opnieuw afspelen van de gegevens.

*Dezelfde gegevens na afspelen:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Transient ID (aanmeldings-id) | Id met titel (na liveslot) | Id met titel (na opnieuw afspelen) |
|---|---|---|---|---|---|
| 1 | 2023-05-12 12:01 | `246` | - | `246` | **`Bob`** |
| 2 | 2023-05-12 12:02 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` | `Bob` ![Pijl-omhoog](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) |
| 3 | 2023-05-12 12:03 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` |
| 4 | 2023-05-12 12:04 | `246` | - | **`Bob`** | `Bob` |
| 5 | 2023-05-12 12:05 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` |
| 6 | 2023-05-12 12:06 | `246` | - | **`Bob`** | `Bob` |
| 7 | 2023-05-12 12:07 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` | `Bob` |
| 8 | 2023-05-12 12:03 | `3579` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** | **`3579`** |
| 9 | 2023-05-12 12:09 | `3579` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** | **`3579`** |
| 10 | 2023-05-12 12:02 | `81911` | - | `81911` | **`Bob`** |
| 11 | 2023-05-12 12:05 | `81911` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` ![Pijl-omhoog](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) |
| 12 | 2023-05-12 12:12 | `81911` | - | **`Bob`** | `Bob` |
| | | **3 apparaten** | | **4 personen**:<br/>`246`, `Bob`, `3579`, `81911` | **2 personen**:<br/>`Bob`, `3579` |

{style="table-layout:auto"}

Attributie werkt wanneer de identificerende aangepaste variabele aan een apparaat is gekoppeld. In het bovenstaande voorbeeld worden gebeurtenis 1 en 10 vastgezet als resultaat van het opnieuw afspelen, waarbij alleen gebeurtenis 8 en 9 niet worden vastgezet. En het aantal mensen (cumulatief) verminderen tot 2.

+++

#### Stap 3: Privacy-aanvraag

Wanneer u een privacyverzoek ontvangt, wordt de opgeslagen id verwijderd in alle records voor de gebruiker waarop de privacyaanvraag betrekking heeft.

+++ Details

De volgende lijst vertegenwoordigt de zelfde gegevens zoals hierboven, maar toont het effect dat een privacyverzoek voor Loodje op de gegevens na verwerking het heeft. De rijen waar het Loodje voor authentiek wordt verklaard worden verwijderd (2, 3, 5, 7, en 11) samen met het verwijderen van Loodje als voorbijgaande identiteitskaart voor andere rijen.

*Dezelfde gegevens na een privacyverzoek voor Bob:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Transient ID (aanmeldings-id) | Id met titel (na liveslot) | Id met titel (na opnieuw afspelen) | Transient ID (aanmeldings-id) | Id met titel (na privacyverzoek) |
|---|---|---|---|---|---|---|---|
| 1 | 2023-05-12 12:01 | `246` | - | `246` | **`Bob`** | - | `246` |
| 2 | 2023-05-12 12:02 | `246` | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` | `Bob` ![Pijl-omhoog](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `246` |
| 3 | 2023-05-12 12:03 | `246` | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `246` |
| 4 | 2023-05-12 12:04 | `246` | - | **`Bob`** | `Bob` | - | `246` |
| 5 | 2023-05-12 12:05 | `246` | Bob ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `246` |
| 6 | 2023-05-12 12:06 | `246` | - | **`Bob`** | `Bob` | - | `246` |
| 7 | 2023-05-12 12:07 | `246` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` | `Bob` | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `246` |
| 8 | 2023-05-12 12:03 | `3579` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** | **`3579`** | - | `3579` |
| 9 | 2023-05-12 12:09 | `3579` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** | **`3579`** | - | `3579` |
| 10 | 2023-05-12 12:02 | `81911` | - | `81911` | **`Bob`** | - | `81911` |
| 11 | 2023-05-12 12:05 | `81911` | `Bob` ![Pijl-rechts](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![Pijl-omlaag](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` ![Pijl-omhoog](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `81911` |
| 12 | 2023-05-12 12:12 | `81911` | - | **`Bob`** | `Bob` | - | `81911` |
| | | **3 apparaten** | | **4 personen**:<br/>246 `Bob`, `3579`, `81911` | **2 personen**:<br/>Bob `3579` |  | **3 personen**:<br/>`246`, `3579`, `81911` |

+++

### Vereisten

De volgende voorwaarden zijn specifiek van toepassing op veldomstandigheden:

- De dataset van de gebeurtenis in Adobe Experience Platform, waarop u het stitching wilt toepassen, moet twee kolommen hebben die bezoekers helpen identificeren:

   - A **blijvende id**, een id die beschikbaar is op elke rij. Bijvoorbeeld een bezoekersidentiteitskaart die door een bibliotheek van het AppMeasurement van Adobe Analytics of een ECID wordt geproduceerd door de Dienst van de Identiteit van Adobe Experience Cloud.
   - A **transient ID**, een id die alleen op bepaalde rijen beschikbaar is. Een gehashte gebruikersnaam of e-mailadres bijvoorbeeld wanneer een bezoeker de verificatie uitvoert. U kunt vrijwel elke gewenste id gebruiken. Stitching beschouwt dit gebied om de daadwerkelijke informatie van persoonidentiteitskaart te houden. Voor de beste stitching resultaten, zou een transient identiteitskaart binnen de gebeurtenissen van de dataset minstens eens voor elke blijvende identiteitskaart moeten worden verzonden. Als u van plan bent om deze dataset binnen een verbinding van de Customer Journey Analytics te omvatten, is het verkieslijk dat de andere datasets ook een gelijkaardige gemeenschappelijke herkenningsteken hebben.

- Beide kolommen (blijvende identiteitskaart en voorbijgaande identiteitskaart) moeten als identiteitsgebied met een identiteitsnaamruimte in het schema voor de dataset worden bepaald u wilt heksen. Als u identiteitsstitching gebruikt in Real-time Customer Data Platform, kunt u de opdracht [`identityMap` veldgroep](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#identity), moet u nog identiteitsgebieden met een identiteitsnaamruimte toevoegen. Deze identificatie van identiteitsvelden is vereist omdat het stitching van de Customer Journey Analytics geen ondersteuning biedt voor de `identityMap` veldgroep. Wanneer u een identiteitsveld toevoegt in het schema en ook de opdracht `identityMap` veldgroep, stel het extra identiteitsveld niet in als primaire identiteit. Als u een extra identiteitsveld instelt als primaire identiteit, wordt `identityMap` veldgroep gebruikt voor Real-time Customer Data Platform.

### Beperkingen

De volgende beperkingen zijn specifiek van toepassing op veldomstandigheden:

- De huidige mogelijkheden voor opnieuw aanvragen zijn beperkt tot één stap (permanente id tot tijdelijke id). Het opnieuw activeren in meerdere stappen (bijvoorbeeld een blijvende id naar een tijdelijke id en een andere tijdelijke id) wordt niet ondersteund.
- Als een apparaat door veelvoudige mensen wordt gedeeld en het totale aantal overgangen tussen gebruikers overschrijdt 50.000, houdt de Customer Journey Analytics het stitching van gegevens voor dat apparaat op.
- Aangepaste id-kaarten die in uw organisatie worden gebruikt, worden niet ondersteund.
- Het plaatsen is case-sensitive. Voor datasets die door de de bronschakelaar van de Analyse worden geproduceerd, adviseert de Adobe om het even welke regels van VISTA of verwerkingsregels te herzien die op het transient gebied van identiteitskaart van toepassing zijn. Deze controle zorgt ervoor dat geen van deze regels nieuwe vormen van zelfde identiteitskaart introduceert. U moet er bijvoorbeeld voor zorgen dat er geen VISTA- of verwerkingsregels zijn die een lagere waarde invoeren in het veld met de tijdelijke id voor slechts een gedeelte van de gebeurtenissen.
- Bij het aanbrengen van titels worden velden niet gecombineerd of samengevoegd.
- Het veld Tijdelijke id moet één type id (id&#39;s uit één naamruimte) bevatten. Het veld Tijdelijke id mag bijvoorbeeld geen combinatie bevatten van aanmeldings-id&#39;s en e-mailid&#39;s.
- Als er meerdere gebeurtenissen plaatsvinden met dezelfde tijdstempel voor dezelfde permanente id, maar met verschillende waarden in het veld voor de tijdelijke id, wordt de id geselecteerd door stitching op basis van alfabetische volgorde. Dus als de blijvende id A twee gebeurtenissen heeft met dezelfde tijdstempel en een van de gebeurtenissen Bob opgeeft en de andere de Ann, selecteert de stitching Ann.
- Wees voorzichtig met scenario&#39;s waarin de tijdelijke id&#39;s plaatsaanduidingswaarden bevatten, bijvoorbeeld `Undefined`. Zie de [Veelgestelde vragen](faq.md) voor meer informatie .


## Op grafiek gebaseerde stitching

U geeft een gebeurtenisgegevensset op, evenals de permanente id (cookie) en de naamruimte van de tijdelijke id (persoon-id) voor die gegevensset. Op grafiek gebaseerde stitching leidt tot een nieuwe kolom voor stitched identiteitskaart in de nieuwe gestikte dataset. En gebruikt dan blijvende identiteitskaart om de identiteitsgrafiek van de Dienst van de Identiteit van het Experience Platform te vragen, gebruikend gespecificeerde namespace, om vastgemaakte identiteitskaart bij te werken.

![Op grafiek gebaseerde stitching](/help/stitching/assets/gbs.png)

### Hoe op grafieken gebaseerde stitching werkt

Met Stitching worden minimaal twee gegevenscontroles uitgevoerd in een bepaalde gegevensset.

- **Actief stiteren**: probeert elke hit (gebeurtenis) tijdens de invoer te verbinden met de permanente id om de tijdelijke id voor de geselecteerde naamruimte op te zoeken door de identiteitsgrafiek op te vragen. Als de tijdelijke id beschikbaar is uit de zoekopdracht, wordt deze tijdelijke id onmiddellijk vastgezet.

- **Replay stitching**: Hiermee worden gegevens opnieuw afgespeeld op basis van bijgewerkte identiteiten uit de identiteitsgrafiek. In dit stadium worden hits van voorheen onbekende apparaten (permanente id&#39;s) vastgezet naarmate de identiteitsgrafiek de identiteit van een naamruimte heeft opgelost. Adobe biedt twee herhalingsintervallen:
   - **Dagelijks**: Gegevens worden elke dag opnieuw afgespeeld met een terugzoekvenster van 24 uur. Deze optie biedt een voordeel dat het aantal keren wordt afgespeeld, maar niet-geregistreerde bezoekers moeten zich op dezelfde dag verifiëren dat ze uw site bezoeken.
   - **Wekelijks**: Gegevens worden één keer per week opnieuw afgespeeld met het terugzoekvenster (zie [opties](#options)). Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Niet-opgeslagen gegevens van minder dan een week oud worden echter pas opnieuw verwerkt wanneer de gegevens wekelijks opnieuw worden afgespeeld.

- **Privacy**: Wanneer verzoeken met betrekking tot privacy worden ontvangen, moet, naast het verwijderen van de gevraagde identiteit uit de brondataset, het stikken van die identiteit over niet-geverifieerde gebeurtenissen ongedaan worden gemaakt. De identiteit moet ook uit het identiteitsdiagram worden verwijderd om te voorkomen dat op een grafiek gebaseerde stitching wordt toegepast voor die specifieke identiteit.

Gegevens buiten het terugzoekvenster worden niet opnieuw afgespeeld. Een bezoeker moet binnen een bepaald terugkijkvenster voor een ongeautoriseerd bezoek en een voor authentiek verklaard bezoek voor authentiek verklaren om samen worden geïdentificeerd. Als een apparaat eenmaal is herkend, wordt het vanaf dat punt live vastgezet.

Bekijk de volgende twee identiteitsgrafieken voor blijvende id `246` en `3579`, hoe deze identiteitsgrafieken in de loop der tijd worden bijgewerkt en hoe deze updates invloed hebben op de stappen in op een grafiek gebaseerde stitching.

![Identiteitsgrafiek 246](assets/identity-graph-246.svg)
![Identiteitsgrafiek 3579](assets/identity-graph-3579.svg)

U kunt een identiteitsgrafiek in tijd voor een specifiek profiel bekijken gebruikend [Identity Graph Viewer](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-viewer). Zie ook [Identity Service linking-logica](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-linking-logic) om een beter inzicht te krijgen in de logica die wordt gebruikt bij het koppelen van identiteiten.

#### Stap 1: Actief stitching

Met live stitching wordt geprobeerd elke gebeurtenis na het verzamelen aan bekende informatie op dat moment uit de identiteitsgrafiek te koppelen.

+++ Details

| | Tijd | Blijvende id<br/>`ECID` | Naamruimte<br/>`Email` ![Grafiek](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataMapping_18_N.svg) | Id met titel (na liveslot) |
|--:|---|---|---|---|
| 1 | 2023-05-12 11:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) *ongedefinieerd* | `246` |
| 2 | 2023-05-12 14:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 3 | 2023-05-12 15:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 4 | 2023-05-12 17:00 | `3579` | `3579` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) *ongedefinieerd* | `3579` |
| 5 | 2023-05-12 19:00 | `3579` | `3579` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `ted.w@gmail.com` |
| 6 | 2023-05-13 15:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 7 | 2023-05-13 16:30 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk`<br/>`246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}

U kunt zien hoe voor elke gebeurtenis de vastgezette id wordt opgelost. Gebaseerd op de tijd, blijvende identiteitskaart, en de raadpleging van de identiteitsgrafiek voor gespecificeerde namespace (tegelijkertijd).
Wanneer de zoekopdracht wordt omgezet in meer dan één gebonden id (zoals bij gebeurtenis 7), wordt de lexicografische eerste id die door de identiteitsgrafiek wordt geretourneerd, geselecteerd (`a.b@yahoo.co.uk` in het voorbeeld).

+++

#### Stap 2: Spatiëring opnieuw afspelen

Met regelmatige intervallen (afhankelijk van het gekozen terugkijkvenster) worden historische gegevens die op de meest recente versie van de identiteitsgrafiek zijn gebaseerd opnieuw berekend door de stitching van het afspelen op het tijdstip van het interval.

+++ Details

Met een replay het stitching gebeuren bij 2023-05-13 16:30, met een configuratie van het 24-uurs terugkijkvenster, worden sommige gebeurtenissen van de steekproef opnieuw genest (die door wordt vermeld ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg)).

| | Tijd | Blijvende id<br/>`ECID` | Naamruimte<br/>`Email` ![Grafiek](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataMapping_18_N.svg) | Id met titel<br/>(na liveslot) | Id met titel<br/>(na 24 uur opnieuw afspelen) |
|---|---|---|---|---|---|
| 2 | 2023-05-12 14:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `bob.a@gmail.com` |
| 3 | 2023-05-12 15:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `bob.a@gmail.com` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 4 | 2023-05-12 17:00 | `3579` | `3579` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` | `ted.w@gmail.com` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 5 | 2023-05-12 19:00 | `3579` | `3579` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `ted.w@gmail.com` | `ted.w@gmail.com` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 6 | 2023-05-13 15:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 7 | 2023-05-13 16:30 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk`<br/>`246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}


Met replay het stitching gebeuren bij 2023-05-13 16:30, met een configuratie van het terugkijkvenster van 7 dagen, worden alle gebeurtenissen van de steekproef re-stitched.


| | Tijd | Blijvende id<br/>`ECID` | Naamruimte<br/>`Email` ![Grafiek](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataMapping_18_N.svg) | Id met titel<br/>(na liveslot) | Id met titel<br/>(na 7 dagen opnieuw afspelen) |
|---|---|---|---|---|---|
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 1 | 2023-05-12 11:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) *ongedefinieerd* | `246` | `a.b@yahoo.co.uk` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 2 | 2023-05-12 14:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 3 | 2023-05-12 15:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 4 | 2023-05-12 17:00 | `3579` | `3579` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` | `ted.w@gmail.com` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 5 | 2023-05-12 19:00 | `3579` | `3579` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `ted.w@gmail.com` | `ted.w@gmail.com` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 6 | 2023-05-13 15:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![Opnieuw afspelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 7 | 2023-05-13 16:30 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk`<br/>`246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}

+++

#### Stap 3: Privacy-aanvraag

Wanneer u een privacyverzoek ontvangt, wordt de opgeslagen id verwijderd in alle records voor de gebruiker waarop de privacyaanvraag betrekking heeft.

+++ Details

In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar ziet u het effect dat een privacyverzoek (bijvoorbeeld in 2023-05-13 18:00) heeft voor de voorbeeldgebeurtenissen.

| | Tijd | Blijvende id<br/>`ECID` | Naamruimte<br/>`Email` ![Grafiek](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataMapping_18_N.svg) | Id met titel (na privacyverzoek) |
|--:|---|---|---|---|
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 1 | 2023-05-12 11:00 | `246` | `246`  ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `246` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 2 | 2023-05-12 14:00 | `246` | `246`  ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `246` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 3 | 2023-05-12 15:00 | `246` | `246`  ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `246` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 4 | 2023-05-12 17:00 | `3579` | `3579` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 5 | 2023-05-12 19:00 | `3579` | `3579` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 6 | 2023-05-13 15:00 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `246` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 7 | 2023-05-13 16:30 | `246` | `246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk`<br/>`246` ![Koppeling](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.ab@gmail.com` | `246` |

{style="table-layout:auto"}

+++

### Vereisten

De volgende voorwaarden zijn specifiek van toepassing op op grafiek gebaseerde stitching:

- De gebeurtenisdataset in Adobe Experience Platform, waarop u het stitching wilt toepassen, moet één kolom hebben die een bezoeker op elke rij, identificeert **blijvende id**. Bijvoorbeeld een bezoekersidentiteitskaart die door een bibliotheek van het AppMeasurement van Adobe Analytics of een ECID wordt geproduceerd door de Dienst van de Identiteit van Adobe Experience Cloud.
- De identiteitsgrafiek van de Dienst van de Identiteit van het Experience Cloud moet een namespace (bijvoorbeeld `Email`, of `Phone`) die u tijdens het stikken wilt gebruiken om het **transient ID**. Zie [Experience Platform Identity Service](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home) voor meer informatie .

>[!NOTE]
>
>U doet dat **niet** een Real-time Customer Data Platform-licentie vereisen voor op grafiek gebaseerde stitching. De **Selecteren** of hoger pakket Customer Journey Analytics bevat de vereiste rechten voor de gebruikersidentiteitsservice.



### Beperkingen

De volgende beperkingen zijn specifiek van toepassing op op grafiek gebaseerde stitching:

- Tijdstempels worden niet in aanmerking genomen wanneer wordt gezocht naar de tijdelijke id die de opgegeven naamruimte gebruikt. Het is dus mogelijk dat een permanente id is gekoppeld aan een tijdelijke id uit een record met een eerdere tijdstempel.
- Geen ondersteuning voor gedeelde apparaten. Wanneer meerdere identiteiten worden geretourneerd, wordt de eerste lexicografische identiteit gebruikt door de identiteitsgrafiek op te vragen met behulp van een naamruimte.
- Er geldt een harde limiet van drie maanden voor het terugvullen van identiteiten in de identiteitsgrafiek. Als u geen Experience Platform-toepassing gebruikt, zoals Real-time Customer Data Platform, kunt u de identiteitsgrafiek weergeven door de identiteiten te herstellen.
- De [Identiteitsservicehandleidingen](https://experienceleague.adobe.com/en/docs/experience-platform/identity/guardrails) van toepassing. Zie bijvoorbeeld het volgende [statische limieten](https://experienceleague.adobe.com/en/docs/experience-platform/identity/guardrails#static-limits):
   - Maximumaantal identiteiten in een grafiek: 50.
   - Maximum aantal koppelingen naar een identiteit voor één batch-opname: 50.
   - Maximum aantal identiteiten in een XDM-record voor grafiekopname: 20.
   - Minimumaantal identiteiten in een XDM-record voor opnemen van grafieken: 2.


## Sstitching gebruiken

Zodra uw organisatie aan allen voldoet [voorwaarden](#prerequisites) en begrijpt gemeenschappelijk [beperkingen](#limitations) specifieke methode voor stitching ([op het veld gebaseerd](#limitations-1) en [op basis van grafiek](#limitations-2)), kunt u deze stappen volgen om te beginnen met het gebruik van stitching in de Customer Journey Analytics.

### Opties

Selecteer de opties voor stitching. Het pakket van de Customer Journey Analytics bepaalt beschikbare opties voor de aanvankelijke backfill duur, raadplegingsvenster, replay frequentie, en maximumaantal datasets die voor het stitching worden toegestaan. Zie de [Productbeschrijving Customer Journey Analytics](https://helpx.adobe.com/legal/product-descriptions/customer-journey-analytics.html) voor meer informatie .

| | Customer Journey Analytics<br/>Selecteren | Customer Journey Analytics<br/>Eerste | Customer Journey Analytics<br/>Ultieme |
|---|---|---|---|
| Eenmalige duur van de backfill-functie | 13 maanden | 13 maanden | 25 maanden |
| Zoekvenster en herhalingsfrequentie | <li>1 dag, elke dag</li><li>tot 7 dagen, wekelijks</li> | <li>1 dag, elke dag</li><li>tot 14 dagen, wekelijks</li> | <li>1 dag, elke dag</li><li>tot 30 dagen, wekelijks</li> |
| Maximumaantal gegevenssets dat is toegestaan voor stitching | 5 | 10 | 50 |

### Ondersteuning aanvragen

1. Neem contact op met de Klantenondersteuning van de Adobe met de volgende informatie:

   - Een verzoek om stitching in te schakelen.
   - De dataset-id voor de gegevensset die u opnieuw wilt invoeren.
   - De kolomnaam (identiteitspad en naamruimte) van de permanente id voor de gewenste gegevensset (de id die op elke rij wordt weergegeven).
   - Voor op veld gebaseerde stitching, de kolomnaam van transient identiteitskaart voor de gewenste dataset (persoonsidentificatie, die ook als verbinding tussen datasets in de context van een verbinding dienst doet). Voor op een grafiek gebaseerde stitching, de identiteitsnaamruimte die voor het vragen van de identiteitsgrafiek moet worden gebruikt.
   - Uw voorkeur voor terugkijkvenster en herhalingsfrequentie. Zie het Customer Journey Analytics pakket voor de [opties](#options) beschikbaar.
   - Naam van sandbox.


2. De klantenondersteuning van de Adobe werkt samen met Adobe-engineering om het aansluiten bij ontvangst van uw verzoek mogelijk te maken. Als deze optie is ingeschakeld, wordt in Adobe Experience Platform een nieuwe opnieuw weergegeven gegevensset met een nieuwe kolom met een naastgelegen id weergegeven. De Steun van de Klant van de Adobe kan identiteitskaart van de nieuwe dataset verstrekken.

3. Als deze optie voor het eerst is ingeschakeld, wordt een back-up van de gegevens gemaakt. Zie het Customer Journey Analytics pakket voor de [option](#options) beschikbaar.

4. Als u de nieuwe gestikte dataset in een dwars-kanaalanalyse wilt gebruiken, moet u de nieuwe gestikte dataset aan een toevoegen [verbinding](../connections/overview.md) in de Customer Journey Analytics. Voeg vervolgens andere gegevenssets toe die vereist zijn voor kanaalanalyse en selecteer de juiste persoon-id voor elke gegevensset.

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

