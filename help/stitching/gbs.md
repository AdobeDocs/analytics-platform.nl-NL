---
title: Op grafiek gebaseerde stitching
description: Uitleg van op grafiek gebaseerde stitching
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
source-git-commit: 4ce1b22cce3416b8a82e5c56e605475ae6c27d88
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# Op grafiek gebaseerde stitching


In grafiek gebaseerd het stitching, specificeert u een gebeurtenisdataset evenals blijvende identiteitskaart (koekje) en namespace van voorbijgaande identiteitskaart (persoonsidentiteitskaart) voor die dataset. Op grafiek gebaseerde stitching leidt tot een nieuwe kolom voor stitched identiteitskaart in de nieuwe gestikte dataset. En gebruikt dan blijvende identiteitskaart om de identiteitsgrafiek van de Dienst van de Identiteit van het Experience Platform te vragen, gebruikend gespecificeerde namespace, om vastgemaakte identiteitskaart bij te werken.

![ grafiek-gebaseerd-stitching ](/help/stitching/assets/gbs.png)

## Hoe op grafieken gebaseerde stitching werkt

Met Stitching worden minimaal twee gegevenscontroles uitgevoerd in een bepaalde gegevensset.

- **Levend het stitching**: pogingen om elke hit (gebeurtenis) te verbinden aangezien het binnen komt, gebruikend blijvende identiteitskaart omhoog transient identiteitskaart voor geselecteerde namespace te kijken door de identiteitsgrafiek te vragen. Als de tijdelijke id beschikbaar is uit de zoekopdracht, wordt deze tijdelijke id onmiddellijk vastgezet.

- **Replay het stitching**: *speelt* gegevens opnieuw die op bijgewerkte identiteiten van de identiteitsgrafiek worden gebaseerd. In dit stadium worden hits van voorheen onbekende apparaten (permanente id&#39;s) vastgezet naarmate de identiteitsgrafiek de identiteit van een naamruimte heeft opgelost. Replay wordt bepaald door twee parameters: **frequentie** en **raadplegingsvenster**. Adobe biedt de volgende combinaties van deze parameters aan:
   - **Dagelijkse raadpleging op een dagelijkse frequentie**: De gegevens respeelt elke dag met een terugkijkvenster van 24 uur terug. Deze optie biedt een voordeel dat het aantal keren wordt afgespeeld, maar niet-geregistreerde bezoekers moeten zich op dezelfde dag verifiëren dat ze uw site bezoeken.
   - **wekelijkse raadpleging op een wekelijkse frequentie**: De gegevens respeelt eens per week met een wekelijks terugkijkvenster (zie [ opties ](#options)) opnieuw. Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Niet-opgeslagen gegevens van minder dan een week oud worden echter pas opnieuw verwerkt wanneer de gegevens wekelijks opnieuw worden afgespeeld.
   - **biwekelijkse raadpleging op een wekelijkse frequentie**: De gegevens respeelt eens per week met een tweewekelijkse raadplegingsvenster (zie [ opties ](#options)) opnieuw. Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Onverwachte gegevens van minder dan twee weken oud worden echter pas opnieuw verwerkt wanneer de volgende week opnieuw wordt afgespeeld.
   - **Maandelijkse raadpleging op een wekelijkse frequentie**: De gegevens replay elke week met een maandelijks terugkijkvenster (zie [ opties ](#options)). Deze optie houdt een voordeel dat unauthenticated zittingen een veel mildere tijd toestaat om voor authentiek te verklaren. Niet-opgeslagen gegevens van minder dan een maand oud worden echter pas opnieuw verwerkt wanneer de gegevens wekelijks opnieuw worden afgespeeld.

- **Privacy**: Wanneer op privacy betrekking hebbende verzoeken, naast het verwijderen van de gevraagde identiteit uit de brondataset worden ontvangen, moet om het even welk stitching van die identiteit over niet voor authentiek verklaarde gebeurtenissen worden ongedaan gemaakt. De identiteit moet ook uit het identiteitsdiagram worden verwijderd om te voorkomen dat op een grafiek gebaseerde stitching wordt toegepast voor die specifieke identiteit.

  >[!IMPORTANT]
  >
  >Het ontvlechtingsproces, als onderdeel van privacyverzoeken, verandert begin 2025. In het huidige ontvlechtingsproces worden gebeurtenissen hernoemd met de nieuwste versie van bekende identiteiten. Deze herplaatsing van gebeurtenissen naar een andere identiteit kan ongewenste juridische gevolgen hebben. Om deze zorgen weg te nemen, werkt het nieuwe ontvlechtingsproces vanaf 2025 gebeurtenissen bij die het voorwerp van het privacyverzoek met blijvende identiteitskaart zijn.
  > 

Gegevens buiten het terugzoekvenster worden niet opnieuw afgespeeld. Een bezoeker moet binnen een bepaald terugkijkvenster voor een ongeautoriseerd bezoek en een voor authentiek verklaard bezoek voor authentiek verklaren om samen worden geïdentificeerd. Als een apparaat eenmaal is herkend, wordt het vanaf dat punt live vastgezet.

Bekijk de volgende twee identiteitsgrafieken voor blijvende id `246` en `3579`, hoe deze identiteitsgrafieken in tijd worden bijgewerkt, en hoe deze updates de stappen in op grafiek-gebaseerde het stitching beïnvloeden.

![ Grafiek 246 van de Identiteit ](assets/identity-graph-246.svg)
![ Grafiek 3579 van de Identiteit ](assets/identity-graph-3579.svg)

U kunt een identiteitsgrafiek over tijd voor een specifiek profiel bekijken gebruikend de [ Kijker van de Grafiek van de Identiteit ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-viewer). Zie ook [ Dienst die van de Identiteit logica ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-linking-logic) verbindt om een beter begrip van de gebruikte logica te krijgen wanneer het verbinden van identiteiten.

### Stap 1: Actief stitching

Met live stitching wordt geprobeerd elke gebeurtenis na het verzamelen aan bekende informatie op dat moment uit de identiteitsgrafiek te koppelen.

+++ Details

| | Tijd | Blijvende id <br/>`ECID` | Namespace <br/>`Email` ![ Grafiek ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataMapping_18_N.svg) | Id met titel (na liveslot) |
|--:|---|---|---|---|
| 1 | 2023-05-12 11:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) *niet gedefiniëerd* | `246` |
| 2 | 2023-05-12 14:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 3 | 2023-05-12 15:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 4 | 2023-05-12 17:00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) *niet gedefiniëerd* | `3579` |
| 5 | 2023-05-12 19:00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `ted.w@gmail.com` |
| 6 | 2023-05-13 15:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` |
| 7 | 2023-05-13 16:30 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk`<br/>`246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}

U kunt zien hoe voor elke gebeurtenis de vastgezette id wordt opgelost. Gebaseerd op de tijd, blijvende identiteitskaart, en de raadpleging van de identiteitsgrafiek voor gespecificeerde namespace (tegelijkertijd).
Wanneer de raadpleging aan meer dan één vastgemaakte identiteitskaart (zoals voor gebeurtenis 7) oplost, wordt lexicografische eerste identiteitskaart die door de identiteitsgrafiek is teruggekeerd geselecteerd (`a.b@yahoo.co.uk` in het voorbeeld).

+++

### Stap 2: Spatiëring opnieuw afspelen

Met regelmatige intervallen (afhankelijk van het gekozen terugkijkvenster) worden historische gegevens die op de meest recente versie van de identiteitsgrafiek zijn gebaseerd opnieuw berekend door de stitching van het afspelen op het tijdstip van het interval.

+++ Details

Met een replay het stitching gebeuren in 2023-05-13 16:30, met een configuratie van het terugkijkvenster van 24 uur, worden sommige gebeurtenissen van de steekproef opnieuw vastgezet (die door ![ wordt vermeld Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg)).

| | Tijd | Blijvende id <br/>`ECID` | Namespace <br/>`Email` ![ Grafiek ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataMapping_18_N.svg) | Gestikte identiteitskaart <br/> (na levende steek) | Gestikte identiteitskaart <br/> (na replay 24 uren) |
|---|---|---|---|---|---|
| 2 | 2023-05-12 14:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `bob.a@gmail.com` |
| 3 | 2023-05-12 15:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `bob.a@gmail.com` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 4 | 2023-05-12 17:00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` | `ted.w@gmail.com` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 5 | 2023-05-12 19:00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `ted.w@gmail.com` | `ted.w@gmail.com` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 6 | 2023-05-13 15:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 7 | 2023-05-13 16:30 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk`<br/>`246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}


Met replay het stitching gebeuren bij 2023-05-13 16:30, met een configuratie van het terugkijkvenster van 7 dagen, worden alle gebeurtenissen van de steekproef re-stitched.


| | Tijd | Blijvende id <br/>`ECID` | Namespace <br/>`Email` ![ Grafiek ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataMapping_18_N.svg) | Gestikte identiteitskaart <br/> (na levende steek) | Gestikte identiteitskaart <br/> (na replay 7 dagen) |
|---|---|---|---|---|---|
| ![ opnieuw spelen ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 1 | 2023-05-12 11:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) *niet gedefiniëerd* | `246` | `a.b@yahoo.co.uk` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 2 | 2023-05-12 14:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 3 | 2023-05-12 15:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.a@gmail.com` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 4 | 2023-05-12 17:00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` | `ted.w@gmail.com` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 5 | 2023-05-12 19:00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `ted.w@gmail.com` | `ted.w@gmail.com` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 6 | 2023-05-13 15:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `bob.a@gmail.com` | `a.b@yahoo.co.uk` |
| ![ Replay ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Replay_18_N.svg) 7 | 2023-05-13 16:30 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk`<br/>`246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.ab@gmail.com` | `a.b@yahoo.co.uk` | `a.b@yahoo.co.uk` |

{style="table-layout:auto"}

+++

### Stap 3: Privacy-aanvraag

Wanneer u een privacyverzoek ontvangt, wordt de opgeslagen id verwijderd in alle records voor de gebruiker waarop de privacyaanvraag betrekking heeft.

+++ Details

In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar ziet u het effect dat een privacyverzoek (bijvoorbeeld in 2023-05-13 18:00) heeft voor de voorbeeldgebeurtenissen.

| | Tijd | Blijvende id <br/>`ECID` | Namespace <br/>`Email` ![ Grafiek ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataMapping_18_N.svg) | Id met titel (na privacyverzoek) |
|--:|---|---|---|---|
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 1 | 2023-05-12 11:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `246` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 2 | 2023-05-12 14:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `246` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 3 | 2023-05-12 15:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `246` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 4 | 2023-05-12 17:00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 5 | 2023-05-12 19:00 | `3579` | `3579` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `ted.w@gmail.com` | `3579` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 6 | 2023-05-13 15:00 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk` | `246` |
| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_RemoveCircle_18_N.svg"/> 7 | 2023-05-13 16:30 | `246` | `246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `a.b@yahoo.co.uk`<br/>`246` ![ Verbinding ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Branch1_18_N.svg) `bob.ab@gmail.com` | `246` |

{style="table-layout:auto"}

+++

## Vereisten

De volgende voorwaarden zijn specifiek van toepassing op op grafiek gebaseerde stitching:

- De gebeurtenisdataset in Adobe Experience Platform, waarop u het stitching wilt toepassen, moet één kolom hebben die een bezoeker op elke rij, **blijvende identiteitskaart** identificeert. Bijvoorbeeld een bezoekersidentiteitskaart die door een bibliotheek van het AppMeasurement van Adobe Analytics of een ECID wordt geproduceerd door de Dienst van de Identiteit van het Experience Platform.
- Ononderbroken identiteitskaart moet ook [ als identiteit ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) in het schema worden bepaald.
- De identiteitsgrafiek van de Dienst van de Identiteit van het Experience Platform moet een namespace (bijvoorbeeld `Email`, of `Phone`) hebben u tijdens het stitching wilt gebruiken om **voorbijgaande identiteitskaart** op te lossen. Zie [ Dienst van de Identiteit van het Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home) voor meer informatie.

>[!NOTE]
>
>U **** vereist geen vergunning van Real-time Customer Data Platform voor op grafiek-gebaseerde het stitching. Het **Prime** pakket of hoger van Customer Journey Analytics omvat de vereiste rechten van de Dienst van de Identiteit van het Experience Platform.


## Beperkingen

De volgende beperkingen zijn specifiek van toepassing op op grafiek gebaseerde stitching:

- Tijdstempels worden niet in aanmerking genomen wanneer wordt gezocht naar de tijdelijke id die de opgegeven naamruimte gebruikt. Het is dus mogelijk dat een permanente id is gekoppeld aan een tijdelijke id uit een record met een eerdere tijdstempel.
- Geen ondersteuning voor gedeelde apparaten. Wanneer meerdere identiteiten worden geretourneerd, wordt de eerste lexicografische identiteit gebruikt door de identiteitsgrafiek op te vragen met behulp van een naamruimte.
- Er geldt een harde limiet van drie maanden voor het terugvullen van identiteiten in de identiteitsgrafiek. Als u geen Experience Platform-toepassing gebruikt, zoals Real-time Customer Data Platform, kunt u de identiteitsgrafiek weergeven door de identiteiten te herstellen.
- De [ Garanties van de Dienst van de Identiteit ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/guardrails) zijn van toepassing. Zie, bijvoorbeeld, de volgende [ statische grenzen ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/guardrails#static-limits):
   - Maximumaantal identiteiten in een grafiek: 50.
   - Maximum aantal koppelingen naar een identiteit voor één batch-opname: 50.
   - Maximum aantal identiteiten in een XDM-record voor grafiekopname: 20.
   - Minimumaantal identiteiten in een XDM-record voor opnemen van grafieken: 2.
