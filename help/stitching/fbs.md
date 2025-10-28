---
title: Veldgebaseerde stitching
description: Uitleg van het concept en de werking van veldoverstikken
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: e5cb55e7-aed0-4598-a727-72e6488f5aa8
source-git-commit: 359fe2a718ccef816377083aceb2652b4a905072
workflow-type: tm+mt
source-wordcount: '1776'
ht-degree: 2%

---

# Veldgebaseerde stitching

In het op gebied-gebaseerde stitching specificeert u een gebeurtenisdataset evenals blijvende identiteitskaart (koekje) en persoonsidentiteitskaart voor die dataset. Op veld gebaseerde stitching voegt een nieuwe gestikte kolom van identiteitskaart aan de gebeurtenisdataset toe en werkt deze vastgemaakte identiteitskaart bij die op rijen wordt gebaseerd die een persoonsidentiteitskaart voor die specifieke blijvende identiteitskaart hebben. <br/> u kunt op gebied-gebaseerde het stitching gebruiken wanneer het gebruiken van Customer Journey Analytics als standalone oplossing (die geen toegang tot de Dienst van de Identiteit van Experience Platform en bijbehorende identiteitsgrafiek heeft). Of als u de beschikbare identiteitsgrafiek niet wilt gebruiken.

![&#x200B; Op gebied-gebaseerde het stitching &#x200B;](/help/stitching/assets/fbs.png)


## IdentityMap

Op veld gebaseerde stitching steunt het gebruik van de [`identityMap` gebiedsgroep &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/composition#identity) in de volgende scenario&#39;s:

- Gebruik van de primaire identiteit in `identityMap` naamruimten om de persistentID te definiëren:
   - Als meerdere primaire identiteiten in verschillende naamruimten worden gevonden, worden de identiteiten in de naamruimten lexigrafisch gesorteerd en wordt de eerste identiteit geselecteerd.
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


- Gebruik van naamruimte `identityMap` om de permanente id of de persoon-id of beide te definiëren:
   - Als er meerdere waarden voor de permanente id of persoon-id worden gevonden in een naamruimte `identityMap` , wordt de eerste lexicografische beschikbare waarde gebruikt.
   - Naamruimten voor permanente id&#39;s en personen-id moeten elkaar uitsluiten.

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

## Hoe veldomstandigheden stitching werkt

Met Stitching worden minimaal twee gegevenscontroles uitgevoerd in een bepaalde gegevensset.

- **Levend het stitching**: pogingen om elke hit (gebeurtenis) te stikken aangezien het binnen komt. Hits van apparaten die *nieuw* aan de dataset (nooit voor authentiek verklaard) zijn worden typisch niet vastgemaakt op dit niveau. Hits van reeds herkende apparaten worden onmiddellijk vastgezet.

- **Replay het stitching**: *speelt* gegevens opnieuw die op unieke herkenningstekens (persoon IDs) worden gebaseerd. In dit stadium worden treffers van eerder onbekende apparaten (permanente id&#39;s) vastgezet (aan personen-id&#39;s). Replay wordt bepaald door twee parameters: **frequentie** en **raadplegingsvenster**. Adobe biedt de volgende combinaties van deze parameters aan:
   - **Dagelijkse raadpleging op een dagelijkse frequentie**: De gegevens respeelt elke dag met een terugkijkvenster van 24 uur terug. Deze optie biedt een voordeel dat het aantal keren opnieuw wordt afgespeeld, maar niet-geverifieerde profielen moeten op dezelfde dag dat ze uw site bezoeken, worden geverifieerd.
   - **wekelijkse raadpleging op een wekelijkse frequentie**: De gegevens respeelt eens per week met een wekelijks terugkijkvenster (zie [&#x200B; opties &#x200B;](#options)) opnieuw. Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Niet-opgeslagen gegevens van minder dan een week oud worden echter pas opnieuw verwerkt wanneer de gegevens wekelijks opnieuw worden afgespeeld.
   - **biwekelijkse raadpleging op een wekelijkse frequentie**: De gegevens respeelt eens per week met een tweewekelijkse raadplegingsvenster (zie [&#x200B; opties &#x200B;](#options)) opnieuw. Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Onverwachte gegevens van minder dan twee weken oud worden echter pas opnieuw verwerkt wanneer de volgende week opnieuw wordt afgespeeld.
   - **Maandelijkse raadpleging op een wekelijkse frequentie**: De gegevens replay elke week met een maandelijks terugkijkvenster (zie [&#x200B; opties &#x200B;](#options)). Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Niet-opgeslagen gegevens van minder dan een maand oud worden echter pas opnieuw verwerkt wanneer de gegevens wekelijks opnieuw worden afgespeeld.

- **Privacy**: Wanneer op privacy betrekking hebbende verzoeken worden ontvangen, naast het verwijderen van de gevraagde identiteit, moet om het even welk stitching van die identiteit over niet voor authentiek verklaarde gebeurtenissen worden ongedaan gemaakt.

  >[!IMPORTANT]
  >
  >Het ontvlechtingsproces, als onderdeel van privacyverzoeken, verandert begin 2025. In het huidige ontvlechtingsproces worden gebeurtenissen hernoemd met de nieuwste versie van bekende identiteiten. Deze herplaatsing van gebeurtenissen naar een andere identiteit kan ongewenste juridische gevolgen hebben. Om deze zorgen weg te nemen, werkt het nieuwe ontvlechtingsproces vanaf 2025 gebeurtenissen bij die het voorwerp van het privacyverzoek met blijvende identiteitskaart zijn.
  > 


Gegevens buiten het terugzoekvenster worden niet opnieuw afgespeeld. Een profiel moet binnen een bepaald terugkijkvenster voor een ongeautoriseerd bezoek voor authentiek verklaren en een voor authentiek verklaard bezoek om samen worden geïdentificeerd. Zodra een apparaat wordt herkend, wordt dat apparaat vanaf dat punt voorwaarts gericht.

### Stap 1: Actief stitching

Live stilzetten probeert elke gebeurtenis bij de verzameling aan te sluiten op bekende apparaten en kanalen.

+++ Details

Overweeg het volgende voorbeeld, waar het Loodje verschillende gebeurtenissen als deel van een gebeurtenisdataset registreert.

*Gegevens aangezien het de dag verscheen het wordt verzameld:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Persoon-id | Id met titel (na liveslot) |
|---|---|---|---|---|
| 1 | 2023-05-12 12 :01 | `246` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`246`** |
| 2 | 2023-05-12 12 :02 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` |
| 3 | 2023-05-12 12 :03 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 4 | 2023-05-12 12 :04 | `246` | - | **`Bob`** |
| 5 | 2023-05-12 12 :05 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 6 | 2023-05-12 12 :06 | `246` | - | **`Bob`** |
| 7 | 2023-05-12 12 :07 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` |
| 8 | 2023-05-12 12 :03 | `3579` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** |
| 9 | 2023-05-12 12 :09 | `3579` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** |
| 10 | 2023-05-12 12 :02 | `81911` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`81911`** |
| 11 | 2023-05-12 12 :05 | `81911` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) |
| 12 | 2023-05-12 12 :12 | `81911` | - | **`Bob`** |
| | | **3 apparaten** | | **4 mensen**:<br/>`246`, `Bob`, `3579`, `81911` |

Zowel niet-geverifieerde als geverifieerde gebeurtenissen op nieuwe apparaten worden als afzonderlijke personen geteld (tijdelijk). Niet-geverifieerde gebeurtenissen op herkende apparaten worden live stilgezet.

Attributie werkt wanneer de identificerende aangepaste variabele aan een apparaat is gekoppeld. In het bovenstaande voorbeeld worden alle gebeurtenissen behalve de gebeurtenissen 1, 8, 9 en 10 live verbonden (ze gebruiken allemaal de id `Bob` ). Als u de stitching live uitvoert, wordt de geroteerde id voor gebeurtenis 4, 6 en 12 opgelost.

Vertraagde gegevens (gegevens met een tijdstempel van meer dan 24 uur oud) worden op de &#39;best mogelijke manier&#39; verwerkt, waarbij de voorkeur wordt gegeven aan het koppelen van huidige gegevens voor de hoogste kwaliteit.

+++ 

### Stap 2: Spatiëring opnieuw afspelen

Met regelmatige intervallen (eenmaal per week of eenmaal per dag, afhankelijk van het gekozen terugkijkvenster) worden historische gegevens opnieuw berekend op basis van de apparaten die het nu herkent. Als een apparaat aanvankelijk gegevens verzendt terwijl niet voor authentiek verklaard en dan login, replay stitching bindt die niet voor authentiek verklaarde gebeurtenissen aan de correcte persoon.

+++ Details

In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar worden verschillende getallen weergegeven op basis van het opnieuw afspelen van de gegevens.

*De zelfde gegevens na replay:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Persoon-id | Id met titel (na liveslot) | Id met titel (na opnieuw afspelen) |
|---|---|---|---|---|---|
| 1 | 2023-05-12 12 :01 | `246` | - | `246` | **`Bob`** |
| 2 | 2023-05-12 12 :02 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` | `Bob` ![&#x200B; Pijl omhoog &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) |
| 3 | 2023-05-12 12 :03 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` |
| 4 | 2023-05-12 12 :04 | `246` | - | **`Bob`** | `Bob` |
| 5 | 2023-05-12 12 :05 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` |
| 6 | 2023-05-12 12 :06 | `246` | - | **`Bob`** | `Bob` |
| 7 | 2023-05-12 12 :07 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` | `Bob` |
| 8 | 2023-05-12 12 :03 | `3579` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** | **`3579`** |
| 9 | 2023-05-12 12 :09 | `3579` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** | **`3579`** |
| 10 | 2023-05-12 12 :02 | `81911` | - | `81911` | **`Bob`** |
| 11 | 2023-05-12 12 :05 | `81911` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` ![&#x200B; Pijl omhoog &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) |
| 12 | 2023-05-12 12 :12 | `81911` | - | **`Bob`** | `Bob` |
| | | **3 apparaten** | | **4 mensen**:<br/>`246`, `Bob`, `3579`, `81911` | **2 mensen**:<br/>`Bob`, `3579` |

{style="table-layout:auto"}

Attributie werkt wanneer de identificerende aangepaste variabele aan een apparaat is gekoppeld. In het bovenstaande voorbeeld worden gebeurtenis 1 en 10 vastgezet als resultaat van het opnieuw afspelen, waarbij alleen gebeurtenis 8 en 9 niet worden vastgezet. En het aantal mensen (cumulatief) verminderen tot 2.

+++ 

### Stap 3: Privacy-aanvraag

Wanneer u een privacyverzoek ontvangt, wordt de opgeslagen id verwijderd in alle records voor de gebruiker waarop de privacyaanvraag betrekking heeft.

+++ Details

De volgende lijst vertegenwoordigt de zelfde gegevens zoals hierboven, maar toont het effect dat een privacyverzoek voor Loodje op de gegevens na verwerking het heeft. De rijen waar het Loodje voor authentiek wordt verklaard worden verwijderd (2, 3, 5, 7, en 11) samen met het verwijderen van Loodje als persoonsidentiteitskaart voor andere rijen.

*De zelfde gegevens na een privacyverzoek voor Loodje:*

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Persoon-id | Id met titel (na liveslot) | Id met titel (na opnieuw afspelen) | Persoon-id | Id met titel (na privacyverzoek) |
|---|---|---|---|---|---|---|---|
| 1 | 2023-05-12 12 :01 | `246` | - | `246` | **`Bob`** | - | `246` |
| 2 | 2023-05-12 12 :02 | `246` | Loodje ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` | `Bob` ![&#x200B; Pijl omhoog &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `246` |
| 3 | 2023-05-12 12 :03 | `246` | Loodje ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `246` |
| 4 | 2023-05-12 12 :04 | `246` | - | **`Bob`** | `Bob` | - | `246` |
| 5 | 2023-05-12 12 :05 | `246` | Loodje ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `246` |
| 6 | 2023-05-12 12 :06 | `246` | - | **`Bob`** | `Bob` | - | `246` |
| 7 | 2023-05-12 12 :07 | `246` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` | `Bob` | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `246` |
| 8 | 2023-05-12 12 :03 | `3579` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** | **`3579`** | - | `3579` |
| 9 | 2023-05-12 12 :09 | `3579` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | - | **`3579`** | **`3579`** | - | `3579` |
| 10 | 2023-05-12 12 :02 | `81911` | - | `81911` | **`Bob`** | - | `81911` |
| 11 | 2023-05-12 12 :05 | `81911` | `Bob` ![&#x200B; Juiste Pijl &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowRight_18_N.svg) | `Bob` ![&#x200B; Pijl neer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) | `Bob` ![&#x200B; Pijl omhoog &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowUp_18_N.svg) | <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> | `81911` |
| 12 | 2023-05-12 12 :12 | `81911` | - | **`Bob`** | `Bob` | - | `81911` |
| | | **3 apparaten** | | **4 mensen**:<br/> 246, `Bob`, `3579`, `81911` | **2 mensen**:<br/> Loodje, `3579` |  | **3 mensen**:<br/>`246`, `3579`, `81911` |

+++ 

## Vereisten

De volgende voorwaarden zijn specifiek van toepassing op veldomstandigheden:

- De dataset van de gebeurtenis in Adobe Experience Platform, waarop u het stitching wilt toepassen, moet twee kolommen hebben die helpen profielen identificeren:

   - A **blijvende identiteitskaart**, een herkenningsteken beschikbaar op elke rij. Bijvoorbeeld een bezoeker-id die is gegenereerd door een Adobe Analytics AppMeasurement-bibliotheek of een ECID die is gegenereerd door de Adobe Experience Platform Identity Service.
   - A **persoonsidentiteitskaart**, een herkenningsteken beschikbaar op slechts sommige rijen. Een gehashte gebruikersnaam of e-mailadres bijvoorbeeld wanneer een profiel wordt geverifieerd. U kunt vrijwel elke gewenste id gebruiken. Stitching beschouwt dit gebied om de daadwerkelijke informatie van persoonidentiteitskaart te houden. Voor de beste stitching resultaten, zou een persoon ID binnen de gebeurtenissen van de dataset minstens eens voor elke blijvende identiteitskaart moeten worden verzonden. Als u van plan bent om deze dataset binnen een verbinding van Customer Journey Analytics te omvatten, is het verkieslijk dat de andere datasets ook een gelijkaardige gemeenschappelijke herkenningsteken hebben.

<!--
- Both columns (persistent ID and person ID) must be defined as an identity field with an identity namespace in the schema for the dataset you want to stitch. When using identity stitching in Real-time Customer Data Platform, using the [`identityMap` field group](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/composition#identity), you still need to add identity fields with an identity namespace. This identification of identity fields is required as Customer Journey Analytics stitching does not support the `identityMap` field group. When adding an identity field in the schema, while also using the `identityMap` field group, do not set the additional identity field as a primary identity. Setting an additional identity field as primary identity interferes with the `identityMap` field group used for Real-time Customer Data Platform.

-->

## Beperkingen

De volgende beperkingen zijn specifiek van toepassing op veldomstandigheden:

- De huidige mogelijkheden voor opnieuw aanbieden zijn beperkt tot één stap (permanente id voor de persoon-id). Het opnieuw activeren van meerdere stappen (bijvoorbeeld een permanente id van een persoon-id en een andere persoon-id) wordt niet ondersteund.
- Als een apparaat door meerdere personen wordt gedeeld en het totale aantal overgangen tussen gebruikers groter is dan 50.000, stopt Customer Journey Analytics met het naaien van gegevens voor dat apparaat.
- Aangepaste id-kaarten die in uw organisatie worden gebruikt, worden niet ondersteund.
- Het plaatsen is case-sensitive. Voor datasets die door de de bronschakelaar van de Analyse worden geproduceerd, adviseert Adobe om het even welke regels van VISTA of verwerkingsregels te herzien die op het gebied van identiteitskaart van de Persoon van toepassing zijn. Deze controle zorgt ervoor dat geen van deze regels nieuwe vormen van zelfde identiteitskaart introduceert. U moet er bijvoorbeeld voor zorgen dat er geen VISTA- of verwerkingsregels zijn die een lagere waarde invoeren voor het veld met de persoon-id voor slechts een gedeelte van de gebeurtenissen.
- Bij het aanbrengen van titels worden velden niet gecombineerd of samengevoegd.
- Het veld Persoon-id moet één type id (id&#39;s uit één naamruimte) bevatten. Het veld Personen-id mag bijvoorbeeld geen combinatie bevatten van aanmeldings-id&#39;s en e-mailadressen.
- Als er meerdere gebeurtenissen plaatsvinden met dezelfde tijdstempel voor dezelfde permanente id, maar met verschillende waarden in het veld Personen-id, wordt de id op basis van alfabetische volgorde geselecteerd door stitching. Dus als de blijvende id A twee gebeurtenissen heeft met dezelfde tijdstempel en een van de gebeurtenissen Bob opgeeft en de andere de Ann, selecteert de stitching Ann.
- Wees voorzichtig met scenario&#39;s waarin de persoon-id&#39;s plaatsaanduidingswaarden bevatten, bijvoorbeeld `Undefined` . Zie [&#x200B; Veelgestelde vragen &#x200B;](faq.md) voor meer informatie.
- U kunt niet dezelfde naamruimte gebruiken, zowel de permanente id als de persoon-id. Naamruimten moeten elkaar uitsluiten.
