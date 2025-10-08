---
title: Veelgestelde vragen over tekst
description: Veelgestelde vragen over Stitching
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
exl-id: f4115164-7263-40ad-9706-3b98d0bb7905
role: Admin
source-git-commit: 4cea79a6ba26a2e4f06bfc9c60fdfc03341a7d60
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 2%

---

# Veelgestelde vragen

Hier volgen een aantal veelgestelde vragen over stitching:

## Verplaatsen over kanalen

+++ Hoe kan ik stitching gebruiken om te zien hoe mensen zich van één kanaal aan een andere bewegen?

U kunt een stroomvisualisatie met de dimensie van identiteitskaart van de Dataset gebruiken.

1. Login aan [&#x200B; Customer Journey Analytics &#x200B;](https://analytics.adobe.com) en creeer een leeg project van Workspace.
2. Selecteer het **[!UICONTROL ** Visualisaties **]** lusje op de linkerzijde, en sleep a **[!UICONTROL **&#x200B; Stroom &#x200B;**]** visualisatie aan het canvas op het recht.
3. Selecteer het **[!UICONTROL ** lusje van Componenten **]** op de linkerzijde, en sleep dimensie **[!UICONTROL ** identiteitskaart van de Dataset **]** aan de centrumplaats geëtiketteerd **[!UICONTROL **&#x200B; Dimension of Punt &#x200B;**]**.
4. Dit stroomrapport is interactief. Als u de stromen naar volgende of vorige pagina&#39;s wilt uitbreiden, selecteert u een van de waarden. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

Als u de de afmetingspunten van identiteitskaart van de dataset zou willen anders noemen, kunt u een raadplegingsdataset gebruiken.

+++

## Opnieuw afspelen

+++ Hoe ver is het stitching replay bezoekers?

Het terugkijkvenster voor het opnieuw beginnen hangt van uw gewenste frequentie van gegevensreplay af. Als u bijvoorbeeld stitching instelt om gegevens eenmaal per week opnieuw af te spelen, is het terugzoekvenster voor het opnieuw afspelen zeven dagen. Als u stitching opstelling om gegevens elke dag opnieuw te spelen, is het raadplegingsvenster voor het opnieuw beginnen één dag.

+++

## Gedeelde apparaten

+++ Hoe worden gedeelde apparaten afgehandeld?

In sommige situaties, is het mogelijk dat de veelvoudige mensen van het zelfde apparaat login. De voorbeelden omvatten een gedeeld apparaat thuis, gedeelde PCs in een bibliotheek, of een kiosk in een detailhandelsafzet.

De tijdelijke id negeert de blijvende id, zodat gedeelde apparaten als afzonderlijke personen worden beschouwd (zelfs als ze van hetzelfde apparaat afkomstig zijn).

Zie [&#x200B; Gedeelde apparaten &#x200B;](/help/use-cases/stitching/shared-devices.md) gebruiksgeval voor meer details.

+++

## Veel permanente id&#39;s

+++ Hoe kan stitching situaties verwerken waarin één persoon vele blijvende IDs heeft?

In sommige situaties kan een individuele gebruiker veel permanente id&#39;s koppelen. Een voorbeeld hiervan is dat een gebruiker vaak de cookies van de browser wist of de persoonlijke/incognitomodus van de browser gebruikt.

Voor stitching in het veld is het aantal permanente id&#39;s niet relevant ten gunste van de tijdelijke id. Eén gebruiker kan tot een willekeurig aantal apparaten behoren zonder dat dit invloed heeft op de mogelijkheid van Customer Journey Analytics om apparaten aan te sluiten.

Voor op een grafiek gebaseerde stitching, kan één enkele persoon vele blijvende identiteitskaart in de identiteitsgrafiek hebben. Op grafiek gebaseerde stitching gebruikt blijvende identiteitskaart die op gespecificeerde namespace wordt gebaseerd. Als er een meer permanente id voor dezelfde naamruimte is, wordt de lexicografische eerste permanente id gebruikt.

+++

## Stikproces

+++ Wanneer ik mijn Adobe Account Team met de gewenste informatie contacteer, hoe lang duurt het voor de opgeklapte dataset beschikbaar wordt?

Livestitching is ongeveer een week beschikbaar nadat Adobe stitching inschakelt. De beschikbaarheid van back-ups is afhankelijk van de hoeveelheid bestaande gegevens. Kleine datasets (minder dan 1 miljoen gebeurtenissen per dag) nemen doorgaans een paar dagen in beslag, terwijl grote gegevenssets (1 miljard gebeurtenissen per dag) een week of meer kunnen duren.

+++

## Apparaatanalyse versus kanaalanalyse

+++ Wat is het verschil tussen apparaatanalyse (een functie in traditionele Analytics) en kanaalanalyse?

[&#x200B; dwars-apparaat analyseert &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html?lang=nl-NL) is een eigenschap specifiek voor traditionele Adobe Analytics die u toestaat om te begrijpen hoe de mensen over apparaten werken. Er zijn twee workflows om apparaatgegevens aan elkaar te koppelen: op het veld gebaseerde stitching en de apparaatgrafiek.

Kanaaloverschrijdende analyse is een gebruiksgeval specifiek voor Customer Journey Analytics dat u toestaat om te begrijpen hoe de mensen over zowel apparaten als kanalen werken. Het stitches de de persoonsidentiteitskaart van een dataset, toestaand die dataset om naadloos met andere datasets worden gecombineerd. Deze functie werkt op vergelijkbare wijze in ontwerpen als op het veld gebaseerde koppelingen voor apparaatanalyse, maar de implementatie is anders vanwege de verschillende gegevensarchitectuur tussen traditionele Analytics en Customer Journey Analytics. Zie [&#x200B; het Plaatsen &#x200B;](overview.md) en het [&#x200B; dwars-kanaalanalyse &#x200B;](../use-cases/cross-channel/cross-channel.md) gebruiksgeval voor meer informatie.

+++

## Privacy

+++ Hoe behandelt Stitching privacyverzoeken?

Adobe handelt privacyverzoeken af in overeenstemming met de lokale en internationale wetgeving. Adobe biedt [&#x200B; Adobe Experience Platform Privacy Service &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl-NL) aan om verzoeken van de gegevenstoegang en schrapping voor te leggen. De verzoeken zijn van toepassing op zowel de oorspronkelijke als de opgehaalde gegevensbestanden.

>[!IMPORTANT]
>
>Het ontvlechtingsproces, als onderdeel van privacyverzoeken, verandert begin 2025. In het huidige ontvlechtingsproces worden gebeurtenissen hernoemd met de nieuwste versie van bekende identiteiten. Deze herplaatsing van gebeurtenissen naar een andere identiteit kan ongewenste juridische gevolgen hebben. Om deze zorgen weg te nemen, werkt het nieuwe ontvlechtingsproces vanaf 2025 gebeurtenissen bij die het voorwerp van het privacyverzoek met blijvende identiteitskaart zijn.
> 

Stel de volgende gegevens in voor identiteiten, gebeurtenissen vóór het stitching en na het stitching.

| Identiteitskaart | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte |
|---|---|---|---|---|---|---|
|  | 1 | ts1 | 123 | ecid | Bob | CustId |
|  | 2 | ts2 | 123 | ecid | Alex | CustId |


| Gegevensset gebeurtenissen | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte |
|---|---|---|---|---|---|---|
| | 1 | ts0 | 123 | ecid | | |
| | 2 | ts1 | 123 | ecid | Bob | CustId |
| | 3 | ts2 | 123 | ecid | Alex | CustId |


| Stitched dataset | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte | Id met titel | Naamruimte met titel |
|---|---|---|---|---|---|---|---|---|
| | 1 | ts0 | 123 | ecid | | | Bob | CustId |
| | 2 | ts1 | 123 | ecid | Bob | CustId | Bob | CustId |
| | 3 | ts2 | 123 | ecid | Alex | CustId | Alex | CustId |


**Huidige proces voor privacyverzoek**

Wanneer een privacyverzoek voor klant met Loodje CustID wordt ontvangen, worden de rijen met doorhalingangen geschrapt. Andere gebeurtenissen krijgen een nieuwe naam met de identiteitskaart. Bijvoorbeeld, wordt eerste vastgemaakte identiteitskaart in de gestikte dataset bijgewerkt aan **Alex**.

| Identiteitskaart | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte |
|:---:|---|---|---|---|---|---|
| ![&#x200B; DeleteOutline &#x200B;](/help/assets/icons/DeleteOutline.svg) | ~~1~~ | ~~ts1~~ | ~~123~~ | ~~ecid~~ | ~~Loodje~~ | ~~CustId~~ |
|  | 2 | ts2 | 123 | ecid | Alex | CustId |


| Gegevensset gebeurtenissen | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte |
|:---:|---|---|---|---|---|---|
| | 1 | ts0 | 123 | ecid | | |
| ![&#x200B; DeleteOutline &#x200B;](/help/assets/icons/DeleteOutline.svg) | ~~2~~ | ~~ts1~~ | ~~123~~ | ~~ecid~~ | ~~Loodje~~ | ~~CustId~~ |
| | 3 | ts2 | 123 | ecid | Alex | CustId |


| Stitched dataset | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte | Id met titel | Naamruimte met titel |
|:---:|---|---|---|---|---|---|---|---|
| | 1 | ts0 | 123 | ecid | | | **Alex** | CustId |
| ![&#x200B; DeleteOutline &#x200B;](/help/assets/icons/DeleteOutline.svg) | ~~2~~ | ~~ts1~~ | ~~123~~ | ~~ecid~~ | ~~Loodje~~ | ~~CustId~~ | ~~Loodje~~ | ~~CustId~~ |
| | 3 | ts2 | 123 | ecid | Alex | CustId | Alex | CustId |


**Nieuw proces voor privacyverzoek**

Wanneer een privacyverzoek voor klant met Loodje CustID wordt ontvangen, worden de rijen met doorhalingangen geschrapt. Andere gebeurtenissen krijgen een nieuwe naam met de permanente id. Bijvoorbeeld, wordt eerste vastgemaakte identiteitskaart in de gestikte dataset bijgewerkt aan **123**.

| Identiteitskaart | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte |
|:---:|---|---|---|---|---|---|
| ![&#x200B; DeleteOutline &#x200B;](/help/assets/icons/DeleteOutline.svg) | ~~1~~ | ~~ts1~~ | ~~123~~ | ~~ecid~~ | ~~Loodje~~ | ~~CustId~~ |
|  | 2 | ts2 | 123 | ecid | Alex | CustId |


| Gegevensset gebeurtenissen | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte |
|:---:|---|---|---|---|---|---|
| | 1 | ts0 | 123 | ecid | | |
| ![&#x200B; DeleteOutline &#x200B;](/help/assets/icons/DeleteOutline.svg) | ~~2~~ | ~~ts1~~ | ~~123~~ | ~~ecid~~ | ~~Loodje~~ | ~~CustId~~ |
| | 3 | ts2 | 123 | ecid | Alex | CustId |


| Stitched dataset | Id | tijdstempel | blijvende id | permanente naamruimte | transient id | tijdelijke naamruimte | Id met titel | Naamruimte met titel |
|:---:|---|---|---|---|---|---|---|---|
| | 1 | ts0 | 123 | ecid | | | **123** | ecid |
| ![&#x200B; DeleteOutline &#x200B;](/help/assets/icons/DeleteOutline.svg) | ~~2~~ | ~~ts1~~ | ~~123~~ | ~~ecid~~ | ~~Loodje~~ | ~~CustId~~ | ~~Loodje~~ | ~~CustId~~ |
| | 3 | ts2 | 123 | ecid | Alex | CustId | Alex | CustId |

+++

## Lege permanente id-waarden

+++ Wat gebeurt er als het veld Persistent-id in een of meer gebeurtenissen leeg is?

Als het veld Persistent-id leeg is voor een gebeurtenis in een gegevensset die wordt vastgezet, kunt u de opgetekende id voor die gebeurtenis op twee manieren bepalen:

* Als het veld Transient ID niet leeg is, gebruikt Customer Journey Analytics de waarde in Transient ID als de Stitched ID.
* Als het veld Transient ID leeg is, laat Customer Journey Analytics de id Stitched leeg. In dit geval zijn Persistente ID, Transient ID en Stitched ID allemaal leeg voor de gebeurtenis. Deze typen gebeurtenissen worden uit elke Customer Journey Analytics-verbinding verwijderd met behulp van de gegevensset die wordt vastgezet, waarbij Stitched ID is gekozen als de Person-id.

+++


## Ongedefinieerde overgangswaarden voor id&#39;s

+++ Wat gebeurt er als het veld Tijdelijke id in een of meer gebeurtenissen plaatsaanduidingswaarden heeft, zoals `Undefined` ?

Wees voorzichtig met &#39;samenvouwen van persoon&#39;, wat optreedt wanneer het naaien wordt toegepast op gegevens die plaatsaanduidingswaarden gebruiken voor tijdelijke id&#39;s. In de onderstaande voorbeeldtabel worden niet-gedefinieerde personen-id&#39;s die afkomstig zijn van een gegevensset die afkomstig is van een CRM-systeem, gevuld met de waarde &#39;Ongedefinieerd&#39;, wat resulteert in een onjuiste weergave van personen.

| Gebeurtenis | Tijdstempel | Blijvende id (cookie-id) | Transient ID (aanmeldings-id) | Id met titel (na opnieuw afspelen) |
|---|---|---|---|---|
| 1 | 2023-05-12 12 :01 | 123 | - | **Cory** |
| 2 | 2023-05-12 12 :02 | 123 | Cory | **Cory** |
| 3 | 2023-05-12 12 :03 | 456 | Ongedefinieerd | **niet gedefiniëerd** |
| 4 | 2023-05-12 12 :04 | 456 | - | **niet gedefiniëerd** |
| 5 | 2023-05-12 12 :05 | 789 | Ongedefinieerd | **niet gedefiniëerd** |
| 6 | 2023-05-12 12 :06 | 012 | Ongedefinieerd | **niet gedefiniëerd** |
| 7 | 2023-05-12 12 :07 | 012 | - | **niet gedefiniëerd** |
| 8 | 2023-05-12 12 :03 | 789 | Ongedefinieerd | **niet gedefiniëerd** |
| 9 | 2023-05-12 12 :09 | 456 | - | **niet gedefiniëerd** |
| 10 | 2023-05-12 12 :02 | 123 | - | **Cory** |
| | | **4 apparaten** | **2 mensen**:<br/> Gebeurtenissen 1, 4, 7, 9, 10 gelaten vallen | **2 mensen**:<br/> Cory, Niet voor authentiek verklaard (doen ineenstorten aan één persoon) |

+++

## Metrische vergelijking

+++ Hoe verhouden de metriek in Customer Journey Analytics stitched datasets zich met gelijkaardige metriek in Customer Journey Analytics unstitched datasets en met Adobe Analytics?

Bepaalde metriek in Customer Journey Analytics lijken op metriek in traditionele Analytics, maar andere cijfers verschillen, afhankelijk van wat u vergelijkt. In de onderstaande tabel worden verschillende gangbare meetwaarden vergeleken:

| **Customer Journey Analytics stitched gegevens** | **Customer Journey Analytics unstitched gegevens** | **Adobe Analytics** | **Analytics Ultimate met CDA** |
| ----- | ----- | ----- | ----- |
| **Mensen** = Telling van verschillende Persoon IDs waar Stitched ID als identiteitskaart van de Persoon wordt gekozen. **Mensen** kunnen hoger of lager zijn dan **Unieke Bezoekers** in traditionele Adobe Analytics, afhankelijk van het resultaat van het stitching proces. | **Mensen** = Telling van verschillende Persoon IDs die op de kolom wordt gebaseerd die als identiteitskaart van de Persoon wordt geselecteerd. **Mensen** in Analytics bronschakelaardatasets is gelijkaardig aan **Unieke Bezoekers** in traditionele Adobe Analytics als `endUserIDs._experience.aaid.id` als identiteitskaart van de Persoon in Customer Journey Analytics wordt gebruikt. | **Unieke Bezoekers** = Telling van verschillende bezoeker IDs. **Unieke Bezoekers** kunnen niet het zelfde zijn als de telling van verschillende **ECID** s. | Zie [&#x200B; Mensen &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/people.html?lang=nl-NL). |
| **Sessies**: Gedefinieerd op basis van de sessiemontages in de Customer Journey Analytics gegevensweergave. Tijdens het koppelingsproces kunnen afzonderlijke sessies van meerdere apparaten in één sessie worden gecombineerd. | **Sessies**: Gedefinieerd op basis van de sessiemontages die zijn opgegeven in de gegevensweergave van Customer Journey Analytics. | **bezoeken**: Zie [&#x200B; bezoeken &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=nl-NL). | **bezoeken**: Gedefinieerd gebaseerd op de zittingsmontages die in de [&#x200B; worden gespecificeerd CDA virtuele rapportreeks &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/cda/setup.html?lang=nl-NL). |
| **Gebeurtenissen** = telling van rijen in de gestikte gegevens in Customer Journey Analytics. Dit metrisch is typisch dicht bij **Voorkomen** in traditionele Adobe Analytics. Opmerking: de veelgestelde vragen hierboven hebben betrekking op rijen met een lege permanente id. | **Gebeurtenissen** = telling van rijen in de unstitched gegevens in Customer Journey Analytics. Dit metrisch is typisch dicht bij **Voorkomen** in traditionele Adobe Analytics. Houd er echter rekening mee dat als er gebeurtenissen met een lege Person-id voorkomen in de niet-opgeslagen gegevens in het Experience Platform-gegevensmeer, deze gebeurtenissen niet in Customer Journey Analytics zijn opgenomen. | **Voorkomen**: Zie [&#x200B; Voorkomen &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html?lang=nl-NL). | **Voorkomen**: Zie [&#x200B; Voorkomen &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html?lang=nl-NL). |

Andere cijfers kunnen vergelijkbaar zijn in Customer Journey Analytics en Adobe Analytics. Bijvoorbeeld, is de totale telling voor Adobe Analytics [&#x200B; douanegebeurtenissen &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/custom-events.html?lang=nl-NL) 1-100 vergelijkbaar tussen traditionele Adobe Analytics en Customer Journey Analytics (of vastgemaakt of unstitched). [&#x200B; Verschillen in mogelijkheden &#x200B;](/help/getting-started/aa-vs-cja/cja-aa.md)) zoals gebeurtenis deduplicatie tussen Customer Journey Analytics versus Adobe Analytics kan discrepantie tussen de twee producten veroorzaken.

+++

## Identiteitskaart

+++ Kan Customer Journey Analytics de velden Identity Map gebruiken?

Ja, Customer Journey Analytics kan de gebieden van de Kaart van de Identiteit voor zowel [&#x200B; gebaseerd gebied &#x200B;](/help/stitching/fbs.md#identitymap) gebruiken en [&#x200B; grafiek die &#x200B;](/help/stitching/gbs.md#identitymap) stitching wordt gebaseerd.

+++

## Overschakelen naar op grafiek gebaseerde stitatie

+++ Moeten de gegevens opnieuw worden ingevoerd om van op het veld gebaseerde stitching naar op grafiek gebaseerde stitching over te schakelen?

Gegevens hoeven niet opnieuw in Experience Platform te worden ingevoerd, maar moeten in Customer Journey Analytics opnieuw worden geconfigureerd. Voer de volgende stappen uit:

1. Stel de nieuwe, op een grafiek gebaseerde, gestikte gegevensset in met behulp van op een grafiek gebaseerde stitching.
1. Maak een nieuwe tijdelijke verbinding met een zeer klein tijdvenster met gegevens.
1. Vorm de nieuwe grafiek gebaseerde dataset als deel van deze tijdelijke verbinding.
1. Controleer met deze nieuwe tijdelijke verbinding of de op grafiek gebaseerde stitching correct werkt.
1. Als op grafiek gebaseerde het stitching zoals verwacht werkt, verzoek om om om het even welke extra backfill voor de op grafiek gebaseerde dataset en ruilt dan de op gebied gebaseerde dataset in uw originele verbinding met de nieuwe op grafiek gebaseerde dataset.
1. Verwijder de tijdelijke verbinding.

+++

## Verstoring van de rapportage

+++ Zou er een verstoring zijn van bestaande rapporten?

Niet als u de hierboven beschreven stappen uitvoert. Anders vraagt u Adobe Consulting om aanvullende ondersteuning.

+++

## Een gegevensset inschakelen voor de identiteitsservice

+++ Hoe te om een dataset voor de Dienst van de Identiteit slechts toe te laten? 

U moet ervoor zorgen dat een dataset voor de Dienst van de Identiteit wordt toegelaten om de dataset in grafiek-gebaseerd het stitching te gebruiken.

U hoeft geen licentie te hebben voor Real-Time Customer Data Platform om gebruik te maken van op grafieken gebaseerde stitching. Grafiekgebaseerde stitching is gebaseerd op een beschikbare identiteitsgrafiek en niet op klantenprofielen in real time.

Als u alleen een gegevensset voor de identiteitsservice wilt inschakelen, gebruikt u een `POST` -aanvraag voor het `/datasets` -eindpunt dat alleen de tag `unifiedIdentity` gebruikt. Bijvoorbeeld:

```shell
curl -X POST \
  https://platform.adobe.io/data/foundation/catalog/dataSets \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {ORG_ID}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
    "schemaRef": {
        "id": "https://ns.adobe.com/{TENANT_ID}/schemas/31670881463308a46f7d2cb09762715",
        "contentType": "application/vnd.adobe.xed-full-notext+json; version=1"
    },
    "tags": {
       "unifiedIdentity": ["enabled:true"]
    }
  }'
```

Als u de tag `unifiedProfile` in de aanvraag gebruikt, maar geen licentie hebt voor Real-Time Customer Data Profile, wordt een fout geretourneerd.

Zie [&#x200B; een dataset creëren die voor Profiel en Identiteit &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/catalog/datasets/enable-for-profile#create-a-dataset-enabled-for-profile-and-identity) voor meer informatie wordt toegelaten.

+++ 
