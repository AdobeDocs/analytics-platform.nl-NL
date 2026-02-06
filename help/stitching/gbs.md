---
title: Tekenen op basis van grafiek
description: Verklaart het concept en het werken van grafiek-gebaseerde stitching.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: ea5c9114-1fc3-4686-b184-2850acb42b5c
source-git-commit: b5afcfe2cac8aa12d7f4d0cf98658149707123e3
workflow-type: tm+mt
source-wordcount: '1741'
ht-degree: 0%

---

# Op grafiek gebaseerde stitching

In op grafiek-gebaseerde het stitching, specificeert u een gebeurtenisdataset, blijvende identiteitskaart (koekje) voor die dataset en gewenste persoonidentiteitskaart namespace van de identiteitsgrafiek. Op grafiek gebaseerde stitching probeert om de informatie van identiteitskaart van de persoon voor de gegevensanalyse van Customer Journey Analytics over om het even welke gebeurtenis ter beschikking te stellen. De permanente id wordt gebruikt om de identiteitsgrafiek op te vragen bij de Experience Platform Identity Service om de persoon-id op te halen uit de opgegeven naamruimte.

Als de informatie van identiteitskaart van de persoon niet voor een gebeurtenis kan worden teruggewonnen, wordt blijvende identiteitskaart gebruikt in plaats daarvan voor die *verbreken* gebeurtenis. Dientengevolge, in a [ gegevensmening ](/help/data-views/data-views.md) die met a [ verbinding ](/help/connections/overview.md) wordt geassocieerd die de dataset bevat die voor het stitching wordt toegelaten, bevat de de gegevensmeningscomponent van identiteitskaart van de persoon of de blijvende waarde van identiteitskaart op het gebeurtenisniveau.


![ grafiek-gebaseerd-stitching ](/help/stitching/assets/gbs.png)

## IdentityMap

Op grafiek-gebaseerde het stitching steunt het gebruik van de [`identityMap` gebiedsgroep ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#identity) in de volgende scenario&#39;s:

- Gebruik van de primaire identiteit in `identityMap` naamruimten om de persistentID te definiëren:
   - Als er meerdere primaire identiteiten voorkomen in verschillende naamruimten, worden de identiteiten in de naamruimten lexicografisch gesorteerd en wordt de eerste identiteit geselecteerd.
   - Wanneer meerdere primaire identiteiten in één naamruimte worden gevonden, wordt de eerste lexicografische beschikbare primaire identiteit geselecteerd.

  In het onderstaande voorbeeld resulteren naamruimten en identiteiten in een gesorteerde lijst met primaire identiteiten en ten slotte in de geselecteerde identiteit.

  <table style="table-layout:auto">
     <tr>
       <th>Naamruimten</th>
       <th>Lijst met identiteiten</th>
     </tr>
     <tr>
       <td>ECID</td>
       <td><pre lang="json"><code>[<br/>&nbsp;&nbsp;{"id": "ecid-3"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "primary": true},<br/>&nbsp;&nbsp;{"id": "ecid-1", "primary": true}<br/>&nbsp;]</code></pre></td>
     </tr>
     <tr>
       <td>CCID</td>
       <td><pre lang="json"><code>[<br/>&nbsp;&nbsp;{"id": "ccid-1"},<br/>&nbsp;&nbsp;{"id": "ccid-2", "primary": true}<br/>]</code></pre></td>
     </tr>
   </table>

  <table style="table-layout:auto">
    <tr>
      <th>Lijst met gesorteerde identiteiten</th>
      <th>Geselecteerde identiteit</th>
    </tr>
    <tr>
      <td><pre lang="json"><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>]<br/>NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</code></pre></td>
      <td><pre lang="json"><code>"id": "ccid-2",<br/>"namespace": "CCID"</code></pre></td>
    </tr>
  </table>

- Gebruik van naamruimte `identityMap` om de persistentID te definiëren:
   - Wanneer meerdere waarden voor persistentID worden gevonden in een naamruimte `identityMap` , wordt de eerste lexicografische beschikbare identiteit gebruikt.

  In het onderstaande voorbeeld hebt u ECID geselecteerd als de naamruimte die u wilt gebruiken. Die selectie resulteert in een gesorteerde lijst van identiteiten, en tenslotte de geselecteerde identiteit.

  <table style="table-layout:auto">
     <tr>
       <th>Naamruimten</th>
       <th>Lijst met identiteiten</th>
     </tr>
     <tr>
       <td>ECID</td>
       <td><pre lang="json"><code>[<br/>&nbsp;&nbsp;{"id": "ecid-3"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "primary": true},<br/>&nbsp;&nbsp;{"id": "ecid-1", "primary": true}<br/>]</code></pre></td>
     </tr>
     <tr>
       <td>CCID</td>
       <td><pre lang="json"><code>[<br/>&nbsp;&nbsp;{"id": "ccid-1"},<br/>&nbsp;&nbsp;{"id": "ccid-2", "primary": true}<br/>]</code></pre></td>
     </tr>
   </table>

  <table style="table-layout:auto">
    <tr>
      <th>Lijst met gesorteerde identiteiten</th>
      <th>Geselecteerde identiteit</th>
    </tr>
    <tr>
      <td><pre lang="json"><code>[<br/>&nbsp;&nbsp;"id": "ecid-1",<br/>&nbsp;&nbsp;"id": "ecid-2",<br/>&nbsp;&nbsp;"id": "ecid-3"<br/>]</code></pre></td>
      <td><pre lang="json"><code>"id": "ecid-1",<br/>"namespace": "ECID"</code></pre></td>
    </tr>
  </table>


## Hoe op grafieken gebaseerde stitching werkt

Met Stitching worden minimaal twee gegevenscontroles uitgevoerd in een bepaalde gegevensset.

- **Levend het stitching**: pogingen om elke hit (gebeurtenis) te stikken aangezien het binnen komt, gebruikend blijvende identiteitskaart om persoonsidentiteitskaart voor geselecteerde namespace op te zoeken door de identiteitsgrafiek te vragen. Als de persoon-id beschikbaar is in de zoekopdracht, wordt deze persoon-id onmiddellijk vastgezet.

- **Replay het stitching**: *speelt* gegevens opnieuw die op bijgewerkte identiteiten van de identiteitsgrafiek worden gebaseerd. In dit stadium worden hits van voorheen onbekende apparaten (permanente id&#39;s) vastgezet naarmate de identiteitsgrafiek de identiteit van een naamruimte heeft opgelost. Twee parameters bepalen replay: **frequentie** en **raadplegingsvenster**. Adobe biedt de volgende combinaties van deze parameters aan:
   - **Dagelijkse raadpleging op een dagelijkse frequentie**: De gegevens respeelt elke dag met een terugkijkvenster van 24 uur terug. Deze optie biedt een voordeel dat het aantal keren opnieuw wordt afgespeeld, maar niet-geverifieerde profielen moeten op dezelfde dag dat ze uw site bezoeken, worden geverifieerd.
   - **wekelijkse raadpleging op een wekelijkse frequentie**: De gegevens respeelt eens per week met een wekelijks terugkijkvenster (zie [ opties ](#options)) opnieuw. Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Niet-opgeslagen gegevens van minder dan een week oud worden echter pas opnieuw verwerkt wanneer de gegevens wekelijks opnieuw worden afgespeeld.
   - **biwekelijkse raadpleging op een wekelijkse frequentie**: De gegevens respeelt eens per week met een tweewekelijkse raadplegingsvenster (zie [ opties ](#options)) opnieuw. Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Onverwachte gegevens van minder dan twee weken oud worden echter pas opnieuw verwerkt wanneer de volgende week opnieuw wordt afgespeeld.
   - **Maandelijkse raadpleging op een wekelijkse frequentie**: De gegevens replay elke week met een maandelijks terugkijkvenster (zie [ opties ](#options)). Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Niet-opgeslagen gegevens van minder dan een maand oud worden echter pas opnieuw verwerkt wanneer de gegevens wekelijks opnieuw worden afgespeeld.

- **Privacy**: Wanneer op privacy betrekking hebbende verzoeken, naast het verwijderen van de gevraagde identiteit uit de brondataset worden ontvangen, moet om het even welk stitching van die identiteit over niet voor authentiek verklaarde gebeurtenissen worden ongedaan gemaakt. De identiteit moet ook uit het identiteitsdiagram worden verwijderd om te voorkomen dat op een grafiek gebaseerde stitching wordt toegepast voor die specifieke identiteit.

  >[!IMPORTANT]
  >
  >Het ontvlechtingsproces, als onderdeel van privacyverzoeken, verandert begin 2025. In het huidige ontvlechtingsproces worden gebeurtenissen hernoemd met de nieuwste versie van bekende identiteiten. Deze herplaatsing van gebeurtenissen naar een andere identiteit kan ongewenste juridische gevolgen hebben. Om deze zorgen weg te nemen, werkt het nieuwe ontvlechtingsproces vanaf 2025 gebeurtenissen bij die het voorwerp van het privacyverzoek met blijvende identiteitskaart zijn.
  > 

Gegevens buiten het terugzoekvenster worden niet opnieuw afgespeeld. Een profiel moet binnen een bepaald terugkijkvenster voor een ongeautoriseerd bezoek en een voor authentiek verklaard bezoek worden voor authentiek verklaard om samen worden geïdentificeerd. Als een apparaat eenmaal is herkend, wordt het vanaf dat punt live vastgezet.

Bekijk de volgende twee identiteitsgrafiekupdates in de loop der tijd voor bezoeker A (met blijvende identiteitskaart `246`) en bezoeker B (met blijvende identiteitskaart `3579`), en hoe deze updates de stappen in op grafiek-gebaseerde het stitching beïnvloeden.

![ Grafiek 3579 van de Identiteit ](assets/identity-graphs.svg)

U kunt een identiteitsgrafiek over tijd voor een specifiek profiel bekijken gebruikend de [ Kijker van de Grafiek van de Identiteit ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-viewer). Zie ook [ Dienst die van de Identiteit logica ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-linking-logic) verbindt om een beter begrip van de gebruikte logica te krijgen wanneer het verbinden van identiteiten.

### Stap 1: Actief stitching

Met live stitching wordt geprobeerd elke gebeurtenis na het verzamelen aan bekende informatie op dat moment uit de identiteitsgrafiek te koppelen.

+++ Details

| | Tijd | Blijvende id <br/>`ECID` | Namespace <br/>`Email` ![ DataMapping ](/help/assets/icons/DataMapping.svg) | Resulterende ID (na live stitch) |
|--:|---|---|---|---|
| 1 | 2023-05-12 11 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) *niet gedefiniëerd* | `246` |
| 2 | 2023-05-12 14 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 3 | 2023-05-12 15 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 4 | 2023-05-12 17 :00 | `3579` | `3579` ![ Branch1 ](/help/assets/icons/Branch1.svg) *niet gedefiniëerd* | `3579` |
| 5 | 2023-05-12 19 :00 | `3579` | `3579` ![ Branch1 ](/help/assets/icons/Branch1.svg) `ted.w@gmail.com` | `ted.w@gmail.com` |
| 6 | 2023-05-13 15 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 7 | 2023-05-13 16 :30 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `a.b@yahoo.co.uk`<br/>`246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}

U kunt zien hoe de resulterende id voor elke gebeurtenis wordt opgelost. Gebaseerd op de tijd, blijvende identiteitskaart, en de raadpleging van de identiteitsgrafiek voor de gespecificeerde persoonidentiteitskaart namespace.
Wanneer de raadpleging aan meer dan één resulterende identiteitskaart (zoals voor gebeurtenis 7) overneemt, wordt lexicografische eerste identiteitskaart die door de identiteitsgrafiek is teruggekeerd geselecteerd (`a.b@yahoo.co.uk` in het voorbeeld).

+++

### Stap 2: Spatiëring opnieuw afspelen

Met regelmatige intervallen (afhankelijk van het gekozen terugkijkvenster) worden historische gegevens die op de meest recente versie van de identiteitsgrafiek zijn gebaseerd opnieuw berekend door de stitching van het afspelen op het tijdstip van het interval.

+++ Details

Met een replay het stitching gebeuren in 2023-05-13 16 :30, met een configuratie van het terugkijkvenster van 24 uur, worden sommige gebeurtenissen van de steekproef opnieuw vastgemaakt (die door ![ wordt vermeld Replay ](/help/assets/icons/Replay.svg)).

| | Tijd | Blijvende id <br/>`ECID` | Namespace <br/>`Email` ![ DataMapping ](/help/assets/icons/DataMapping.svg) | Resulterende ID <br/> (na live verstikking) | Resulterende ID <br/> (na 24 uur opnieuw afspelen) |
|---|---|---|---|---|---|
| 2 | 2023-05-12 14 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `bob.a@gmail.com` |
| 3 | 2023-05-12 15 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `bob.a@gmail.com` |
| ![ Replay ](/help/assets/icons/Replay.svg) 4 | 2023-05-12 17 :00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` | `ted.w@gmail.com` |
| ![ Replay ](/help/assets/icons/Replay.svg) 5 | 2023-05-12 19 :00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `ted.w@gmail.com` | `ted.w@gmail.com` |
| ![ Replay ](/help/assets/icons/Replay.svg) 6 | 2023-05-13 15 :00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![ Replay ](/help/assets/icons/Replay.svg) 7 | 2023-05-13 16 :30 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg)`a.b@yahoo.co.uk`<br/>`246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}


Met replay het stitching gebeuren bij 2023-05-13 16 :30, met een configuratie van het 7 dagterugkijkvenster, worden alle gebeurtenissen van de steekproef re-stitched.


| | Tijd | Blijvende id <br/>`ECID` | Namespace <br/>`Email` ![ DataMapping ](/help/assets/icons/DataMapping.svg) | Resulterende ID <br/> (na live verstikking) | Resulterende ID <br/> (na 7 dagen opnieuw afspelen) |
|---|---|---|---|---|---|
| ![ opnieuw spelen ](/help/assets/icons/Replay.svg) 1 | 2023-05-12 11 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) *niet gedefiniëerd* | `246` | `a.b@yahoo.co.uk` |
| ![ Replay ](/help/assets/icons/Replay.svg) 2 | 2023-05-12 14 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![ Replay ](/help/assets/icons/Replay.svg) 3 | 2023-05-12 15 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![ Replay ](/help/assets/icons/Replay.svg) 4 | 2023-05-12 17 :00 | `3579` | `3579` ![ Branch1 ](/help/assets/icons/Branch1.svg) `ted.w@gmail.com` | `3579` | `ted.w@gmail.com` |
| ![ Replay ](/help/assets/icons/Replay.svg) 5 | 2023-05-12 19 :00 | `3579` | `3579` ![ Branch1 ](/help/assets/icons/Branch1.svg) `ted.w@gmail.com` | `ted.w@gmail.com` | `ted.w@gmail.com` |
| ![ Replay ](/help/assets/icons/Replay.svg) 6 | 2023-05-13 15 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `a.b@yahoo.co.uk` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![ Replay ](/help/assets/icons/Replay.svg) 7 | 2023-05-13 16 :30 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `a.b@yahoo.co.uk`<br/>`246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}

+++

### Stap 3: Privacy-aanvraag

Wanneer u een privacyverzoek ontvangt, wordt de resulterende id verwijderd in alle records voor de gebruiker op wie de privacyaanvraag betrekking heeft.

+++ Details

De volgende lijst vertegenwoordigt de zelfde gegevens zoals hierboven, maar toont het effect dat een privacyverzoek (bijvoorbeeld bij 2023-05-13 18 :00) voor de steekproefgebeurtenissen heeft.

| | Tijd | Blijvende id <br/>`ECID` | Namespace <br/>`Email` ![ DataMapping ](/help/assets/icons/DataMapping.svg) | Resulterende ID (na privacyverzoek) |
|--:|---|---|---|---|
| ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) 1 | 2023-05-12 11 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `a.b@yahoo.co.uk` | `246` |
| ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) 2 | 2023-05-12 14 :00 | `246` | `246`![ Branch1 ](/help/assets/icons/Branch1.svg) `a.b@yahoo.co.uk` | `246` |
| ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) 3 | 2023-05-12 15 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `a.b@yahoo.co.uk` | `246` |
| ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) 4 | 2023-05-12 17 :00 | `3579` | `3579` ![ Branch1 ](/help/assets/icons/Branch1.svg) `ted.w@gmail.com` | `3579` |
| ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) 5 | 2023-05-12 19 :00 | `3579` | `3579` ![ Branch1 ](/help/assets/icons/Branch1.svg) `ted.w@gmail.com` | `3579` |
| ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) 6 | 2023-05-13 15 :00 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `a.b@yahoo.co.uk` | `246` |
| ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) 7 | 2023-05-13 16 :30 | `246` | `246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `a.b@yahoo.co.uk`<br/>`246` ![ Branch1 ](/help/assets/icons/Branch1.svg) `bob.ab@gmail.com` | `246` |

{style="table-layout:auto"}

+++

## Vereisten

De volgende voorwaarden zijn specifiek van toepassing op op grafiek gebaseerde stitching:

- De gebeurtenisdataset in Adobe Experience Platform, waarop u het stitching wilt toepassen, moet één kolom hebben die een profiel op elke rij, **blijvende identiteitskaart** identificeert. Bijvoorbeeld een bezoeker-id die is gegenereerd door een Adobe Analytics AppMeasurement-bibliotheek of een ECID die is gegenereerd door de Experience Platform Identity Service.
- De identiteitsgrafiek van de Dienst van de Identiteit van Experience Platform moet op zandbakniveau worden opgesteld, alvorens op grafiek-gebaseerde stitching toe te laten.
   - De identiteitsgrafiek moet een naamruimte hebben (bijvoorbeeld `Email` of `Phone` ) die u tijdens het naaien wilt gebruiken om de persoon-id op te lossen.
   - De identiteitsgrafiek moet met identiteitsinformatie van om het even welke relevante datasets (van type *gebeurtenis* of *profiel* worden bevolkt en die minstens twee nuttige namespaces met de waarden van identiteitskaart bevatten).
   - Alle datasets die dergelijke relevante identiteiten houden moeten [ worden toegelaten voor de gegevensopname van de identiteitsgrafiek ](faq.md#enable-a-dataset-for-the-identity-service). Hierdoor wordt gegarandeerd dat inkomende identiteiten na verloop van tijd uit alle benodigde bronnen aan de grafiek worden toegevoegd.
   - Als de grafiek al een tijdje het Real-Time Klantgegevensprofiel of Adobe Journey Optimizer gebruikt, moet de grafiek al in zekere mate zijn ingesteld.<br/> als historische het stitching backfill ook voor de dataset wordt vereist die met op grafiek-gebaseerde het stitching wordt toegelaten, zou de grafiek historische identiteiten voor de volledige periode reeds moeten bevatten, om gewenste het stitching resultaten te verkrijgen.
- Als u op grafiek-gebaseerde het stitching wilt gebruiken en u de gebeurtenisdataset om aan de identiteitsgrafiek vooruitloopt bij te dragen, zou u de dataset voor de dienst van de Identiteit [ moeten toelaten.](/help/stitching/faq.md#enable-a-dataset-for-the-identity-service)
- Ononderbroken identiteitskaart en persoonsidentiteitskaart kunnen met [ identityMap ](#identitymap) worden gebruikt. Of blijvende identiteitskaart en persoonsidentiteitskaart kunnen gebieden van het schema zijn XDM, in welk geval de gebieden [ als identiteit ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity?lang=en) in het schema moeten worden bepaald.

>[!NOTE]
>
>U **** vereist geen vergunning van het Platform van Gegevens van de Klant in real time voor op grafiek-gebaseerd het stitching. Het **Prime** pakket of hoger van Customer Journey Analytics omvat de vereiste rechten van de Dienst van de Identiteit van Experience Platform.


## Beperkingen

De volgende beperkingen zijn specifiek van toepassing op op grafiek gebaseerde stitching:

- Tijdstempels worden niet in aanmerking genomen wanneer wordt gezocht naar de persoon-id met behulp van de opgegeven naamruimte. Het is dus mogelijk dat een permanente id wordt gekoppeld aan een persoon-id uit een record met een eerdere tijdstempel.
- In scenario&#39;s voor gedeelde apparaten, waarbij de naamruimte in de grafiek meerdere identiteiten bevat, wordt de eerste lexicografische identiteit gebruikt. Als namespace grenzen en prioriteiten als deel van de versie van grafiek-verbinden regels worden gevormd, wordt de laatste voor authentiek verklaarde identiteit van de gebruiker gebruikt. Zie [ Gedeelde apparaten ](/help/use-cases/stitching/shared-devices.md) voor meer informatie.
- Er geldt een harde limiet van drie maanden voor het terugvullen van identiteiten in de identiteitsgrafiek. Als u geen Experience Platform-toepassing gebruikt, zoals Real-time Customer Data Platform, kunt u de identiteitsgrafiek weergeven door identiteiten te herstellen.
- De [ Garanties van de Dienst van de Identiteit ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/guardrails) zijn van toepassing. Zie, bijvoorbeeld, de volgende [ statische grenzen ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/guardrails#static-limits):
   - Maximumaantal identiteiten in een grafiek: 50.
   - Maximum aantal koppelingen naar een identiteit voor één batch-opname: 50.
   - Maximum aantal identiteiten in een XDM-record voor grafiekopname: 20.
   - Minimumaantal identiteiten in een XDM-record voor opnemen van grafieken: 2.
