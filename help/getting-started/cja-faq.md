---
title: Veelgestelde vragen over Customer Journey Analytics
description: Customer Journey Analytics - Veelgestelde vragen.
exl-id: 778ed2de-bc04-4b09-865e-59e386227e06
solution: Customer Journey Analytics
feature: FAQ
role: User
source-git-commit: 80d5a864e063911b46ff248f2ea89c1ed0d14e32
workflow-type: tm+mt
source-wordcount: '2342'
ht-degree: 0%

---

# Veelgestelde vragen

Adobe Customer Journey Analytics is het product van de volgende generatie. In dit artikel worden antwoorden gegeven op veelgestelde vragen over Customer Journey Analytics. Voor meer informatie raadpleegt u [Ondersteuning van Customer Journey Analytics-functies](/help/getting-started/aa-vs-cja/cja-aa.md).

## 1. Vereisten {#prerequisites}

+++**Moet ik [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] for [!UICONTROL Customer Journey Analytics]?**

Nee, [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] niet vereist zijn voor [!UICONTROL Customer Journey Analytics]. Ze worden zelfs nog niet ondersteund.

+++


+++**Moet ik [!UICONTROL Experience Cloud ID] (ECID) voor [!UICONTROL Customer Journey Analytics]?**

Nee, [!UICONTROL Customer Journey Analytics] steunt om het even welke identiteitskaart in een dataset, of dat is [!UICONTROL ECID] of een andere id die u kiest.

+++


+++**Wat moet ik doen als ik mijn gegevens moet extraheren, transformeren, laden? [!UICONTROL Customer Journey Analytics]?**

Customer Journey Analytics omvat [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/api/overview.html) mogelijkheden om u te helpen uw gegevens om te zetten voordat u deze in het gegevensmeer van Adobe Experience Platform plaatst. Als u ETL nodig hebt nadat de gegevens al zijn ingevoerd, [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/platform-learn/tutorials/queries/understanding-query-service.html#queries) bevat een aantal beperkte opties, hoewel er wellicht extra kosten mee gemoeid zijn.

+++


## 2. Vastleggingsgegevens {#stitching}

+++**Kan [!UICONTROL Customer Journey Analytics] &quot;aansluiten&quot; op verschillende apparaten of op verschillende gegevenssets?**

Ja. [!UICONTROL Customer Journey Analytics] heeft [Stiksel](../stitching/overview.md) functionaliteit die over voor authentiek verklaarde en niet voor authentiek verklaarde gebeurtenissen binnen een dataset werkt. Door deze stitching kunnen afwijkende records worden omgezet in één naadloze id, voor analyse op het niveau van de persoon.
Bovendien wanneer een gemeenschappelijke namespaceID (identiteitskaart van de Persoon wordt gebruikt over datasets binnen een [Verbinding](/help/connections/overview.md)kunt u de analyse uitvoeren op een naadloze combinatie van meerdere gegevenssets, &#39;genest&#39; op persoonlijke niveau.

+++


+++**Wordt het stitching van anoniem gedrag aan voor authentiek verklaard gedrag gesteund?**

Ja. [Stiksel](../stitching/overview.md) kijkt naar gebruikersgegevens van zowel voor authentiek verklaarde als niet voor authentiek verklaarde zittingen om een vastgemaakte identiteitskaart te produceren.

+++


+++**Hoe werkt &#39;replay&#39; in stitching?**

Gegevens worden opnieuw afgespeeld op basis van unieke id&#39;s die het heeft geleerd. Replay is bedoeld om aanvankelijk niet-geverifieerde gebeurtenissen te koppelen aan apparaten die in de tussentijd zijn geïdentificeerd. [Meer informatie](../stitching/overview.md)

+++


+++**Hoe werkt het stitching van historische gegevens (backfill)?**

Als deze optie voor het eerst is ingeschakeld, wordt een back-up van opgeslagen gegevens gemaakt die teruggaat tot het begin van de vorige maand (tot 60 dagen). Om deze backfill te kunnen uitvoeren, moet de tijdelijke id bestaan in de niet-opgeslagen gegevens die veel terug in de tijd zijn. [Meer informatie](../stitching/overview.md)

+++


+++**Wat is het verwachte gedrag voor records met niet-opgeslagen profielgegevens?**

**Voorbeeldscenario**: U sluit zich aan bij twee datasets in een verbinding van de Customer Journey Analytics door te gebruiken `CRMid` als de persoon-id. Een ervan is een webgebeurtenisdataset met `CRMid` in alle records. De andere dataset is een de profielgegevensreeks van CRM. 40% van de gegevensset CRM heeft `CRMid` aanwezig in de de gebeurtenisgegevensreeks van het Web. De andere 60% zijn niet aanwezig in de de gebeurtenisdataset van het Web - verschijnen deze verslagen in rapportering in Analysis Workspace?<p> **Antwoord**: Profielrijen waaraan geen gebeurtenissen zijn gekoppeld, worden in Customer Journey Analytics opgeslagen. U kunt ze echter pas in Analysis Workspace bekijken als er een gebeurtenis met die id wordt weergegeven.

+++

## 3. Gegevens ophalen in [!UICONTROL Customer Journey Analytics] {#ingest}

+++**Kan ik gegevens combineren van verschillende [!UICONTROL Adobe Experience Platform] sandboxen in één [!UICONTROL Customer Journey Analytics] verbinding?**

Nee, u hebt geen toegang tot gegevens in verschillende sandboxen. U kunt alleen gegevenssets combineren die zich binnen dezelfde sandbox bevinden. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html#select-sandbox-and-datasets)

+++


+++**Hoe maak ik verbinding met online gegevens in [!UICONTROL Customer Journey Analytics]?**

Zolang de persoonidentiteitskaart tussen datasets aanpast, [!UICONTROL Customer Journey Analytics] kan filters, attributie, stroom, reserve, etc. over datasets verbinden.

+++


+++**Hoe kan ik mijn offline gegevens overbrengen naar [!UICONTROL Customer Journey Analytics]?**

Met uw recht op Customer Journey Analytics kunt u gegevens in het Experience Platform invoeren. U kunt vervolgens verbindingen maken met die gegevens en gegevensweergaven in [!UICONTROL Customer Journey Analytics], voor rapportage in Analysis Workspace. Het team voor gegevens aan boord van het Experience Platform kan u, indien nodig, aanbevelingen of advies geven.

+++


+++**Hoe krijg ik [!UICONTROL Adobe Analytics] gegevens in [!UICONTROL Customer Journey Analytics]?**

[!UICONTROL Adobe Analytics] gegevens kunnen via de [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Meeste [!UICONTROL Adobe Analytics] velden worden overgebracht in XDM-indeling, maar andere velden zijn nog niet beschikbaar.

+++


+++**Hoe lang duurt het om datasetelementen in een gegevensmening samen te stellen?**

Een paar uur om te beginnen en een paar dagen om een back-up te maken van de laatste 13 maanden van gegevens.

+++


+++**Is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen?**

Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klant identiteitskaart gebruiken, die geen PII is.

+++


+++**Wat zijn de grenzen voor het opnemen voorbij of toekomstige data/timestamps in de gegevensreeksen van de de gebeurtenisgebeurtenissen van de Customer Journey Analytics?**

<ul><li>Met betrekking tot eerdere datums/tijdstempels: gebeurtenisgegevens tot tien jaar oud.</li><li>Met betrekking tot toekomstige datums/tijdstempels: gebeurtenisgegevens (voorspellend) tot één maand in de toekomst.</li></ul>

+++


## 4. Latentieoverwegingen {#latency}

>[!NOTE]
>Er is geen vaste gegevensgrootte in Customer Journey Analytics en Adobe kan zich dus niet vastleggen op een standaardinnametijd. Adobe werkt actief aan het reduceren van deze latentie door nieuwe updates en optimalisatie van inname.

<ul><li>Live-gegevens of -gebeurtenissen: verwerkt en opgenomen binnen 90 minuten, zodra gegevens beschikbaar zijn in Adobe Experience Platform. (Batchgrootte &gt; 50 miljoen rijen: langer dan 90 minuten.)</li><li>Kleine backfills: binnen zeven dagen<li>Grote achtergronden: binnen 30 dagen</li></ul>

Adobe heeft onlangs gewijzigd hoe gegevens in de Customer Journey Analytics worden verwerkt:

<ul><li>Alle gebeurtenisgegevens met een tijdstempel van minder dan 24 uur oud worden gestreamd.</li><li>Alle gebeurtenisgegevens met een tijdstempel van meer dan 24 uur oud (zelfs als deze zich in dezelfde batch bevinden als nieuwere gegevens) worden beschouwd als backfill en krijgen een lagere prioriteit.</li></ul>

## 5. Rolvenster instellen voor [!UICONTROL Connection] gegevensbewaring {#data-retention}

De [**[!UICONTROL Enable rolling data window]**instellen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html#create-connection) Hiermee kunt u de gegevensbewaring van Customers Journey Analytics definiëren als een schuifvenster in maanden (drie maanden, zes maanden enzovoort). Deze is ingesteld op een [!UICONTROL connection] niveau, niet op [!UICONTROL dataset] niveau. Het bewaren van gegevens is gebaseerd op de tijdstempels van de gebeurtenisdataset en is slechts op gebeurtenisdatasets van toepassing. Er bestaat geen instelling voor gegevensbehoud voor profiel- of opzoekgegevenssets omdat er geen relevante tijdstempels zijn.

Het belangrijkste voordeel is dat u alleen gegevens opslaat of rapporteert die van toepassing zijn en nuttig zijn, en oudere gegevens verwijdert die niet meer nuttig zijn. Het helpt u onder uw contractgrenzen te blijven en vermindert het risico van overleeftijdskosten.

## 6. Gevolgen van het verwijderen van gegevenscomponenten {#deletion}

Voor gegevensschrapping, zou u over zes types van componenten moeten bezorgd zijn: zandbak, schema, dataset, verbinding, gegevensmening, en het project van de Werkruimte. Hier zijn enkele mogelijke scenario&#39;s voor het verwijderen van een van deze componenten:

| Als u... | Dit gebeurt... |
| --- | --- |
| Een sandbox verwijderen in [!UICONTROL Adobe Experience Platform] | Als u een sandbox verwijdert, wordt de gegevensstroom niet meer uitgevoerd [!UICONTROL Customer Journey Analytics] verbindingen met gegevenssets in die sandbox. Momenteel [!UICONTROL Connections] in Customer Journey Analytics die aan de verwijderde sandbox is gekoppeld, worden niet automatisch verwijderd. |
| Schema&#39;s verwijderen in [!UICONTROL Adobe Experience Platform], maar niet de dataset(s) die aan dit schema zijn gekoppeld | [!UICONTROL Adobe Experience Platform] het schrappen van [!UICONTROL schemas] die een of meer [!UICONTROL datasets] geassocieerd met hen. Nochtans, kan Admin met de aangewezen reeks rechten de datasets eerst schrappen en dan het schema schrappen. |
| Een gegevensset verwijderen in het dialoogvenster [!UICONTROL Adobe Experience Platform] gegevensmeer | Het schrappen van een dataset in het gegevensmeer van Adobe Experience Platform houdt gegevensstroom van die dataset aan om het even welke Verbindingen van de Customer Journey Analytics die die dataset omvatten. Om het even welke gegevens van die dataset worden automatisch geschrapt van de bijbehorende verbindingen van de Customer Journey Analytics. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics] | Contacteer uw Team van de Rekening van de Adobe om in beweging het proces te plaatsen om een dataset binnen een verbinding te schrappen die is bewaard. |
| Een batch verwijderen uit een dataset (in [!UICONTROL Adobe Experience Platform]) | Als een partij uit een [!UICONTROL Adobe Experience Platform] dataset, wordt de zelfde partij verwijderd uit om het even welke verbindingen van de Customer Journey Analytics die die specifieke partij bevatten. Customer Journey Analytics is op de hoogte gesteld van het verwijderen van partijen in [!UICONTROL Adobe Experience Platform]. |
| Een batch verwijderen **tijdens de inname** in [!UICONTROL Customer Journey Analytics] | Als er slechts één partij in de dataset is, verschijnen geen gegevens of gedeeltelijke gegevens van die partij in [!UICONTROL Customer Journey Analytics]. De inname wordt teruggedraaid. Bijvoorbeeld, als er vijf partijen in de dataset zijn en drie van hen reeds zijn opgenomen toen de dataset werd geschrapt, verschijnen de gegevens van die drie partijen in [!UICONTROL Customer Journey Analytics]. |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Op dezelfde manier werken om het even welke projecten van de Werkruimte die van gegevensmeningen in de geschrapte verbinding afhangen.</li></ul> |
| Een gegevensweergave verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutenmelding wijst erop dat om het even welke projecten van de Werkruimte die van deze geschrapte gegevensmening afhangen zullen ophouden werkend. |

## 7. Overwegingen bij het samenvoegen van rapportagesets in de Customer Journey Analytics {#merge-reportsuite}

Als u van plan bent Adobe Analytics-gegevens in te nemen via de [Adobe Analytics-bronaansluiting](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html)Houd bij het samenvoegen van twee of meer Adobe Analytics-rapportreeksen rekening met deze gevolgen.

| Probleem | Overwegingen |
| --- | --- |
| Variabelen | Variabelen zoals [!UICONTROL eVars] mag niet in een andere dan de rapporteereeksen worden uitgelijnd. EVar1 in rapportsuite 1 verwijst bijvoorbeeld naar **[!UICONTROL Page]**. In rapportsuite 2 kan eVar1 verwijzen naar **[!UICONTROL Internal Campaign]**, hetgeen leidt tot gemengde en onjuiste rapportage. |
| [!UICONTROL Sessions] en [!UICONTROL People] aantal | Ze worden gededupliceerd door de rapportsuites. Hierdoor komen aantallen mogelijk niet overeen. |
| Metrische deduplicatie | Hiermee dupliceert u instanties van een metrische waarde (bijvoorbeeld [!UICONTROL Orders]) als meerdere rijen dezelfde transactie-id hebben (bijvoorbeeld [!UICONTROL Purchase ID]). Hiermee voorkomt u dat belangrijke meetgegevens te veel worden geteld. Dientengevolge, metriek als [!UICONTROL Orders] mag niet worden opgeteld bij hele rapportopties. |
| Valuta | De conversie van valuta wordt nog niet ondersteund in de Customer Journey Analytics. Als de rapportsuites u probeert samen te voegen verschillende basisvaluta&#39;s gebruiken, kunnen de problemen zich voordoen. |
| [!UICONTROL Persistence] | [Persistentie](../data-views/component-settings/persistence.md) breidt zich over rapportseries uit, die gevolgen hebben [!UICONTROL filters], [!UICONTROL attribution], enzovoort. Het is mogelijk dat getallen niet correct worden opgeteld. |
| [!UICONTROL Classifications] | [!UICONTROL Classifications] niet automatisch gededupliceerd worden bij het samenvoegen van rapportsuites. Wanneer u meerdere classificatiebestanden in één bestand combineert [!UICONTROL lookup] dataset, kon u problemen ontmoeten. |

## 8. [!UICONTROL Adobe Analytics] componenten

+++**Kan ik delen/publiceren [!UICONTROL audiences] van [!DNL Customer Journey Analytics] op Experience Platform Real-Time CDP, of andere toepassingen van de Experience Cloud?**

U kunt [publiek maken en publiceren](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/audiences/publish) geïdentificeerd in Customer Journey Analytics aan het Profiel van de Klant in real time in Adobe Experience Platform voor klant gericht en verpersoonlijking.

+++

+++**Wat is er gebeurd met mijn oude [!UICONTROL eVar] instellen?**

[!UICONTROL eVars], [!UICONTROL props], en [!UICONTROL events] in de zin van Adobe Analytics niet meer bestaan in [!UICONTROL Customer Journey Analytics]. U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd.

+++

+++**Waar zijn al mijn zitting en veranderlijke persistentie montages nu?**

[!UICONTROL Customer Journey Analytics] Hiermee past u al deze instellingen tijdens het rapport toe en deze instellingen worden nu live weergegeven in gegevensweergaven. De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken.

+++

+++**Wat gebeurt er met uw bestaande segmenten/berekende metriek?**

[!UICONTROL Customer Journey Analytics] gebruikt niet langer eVars, props of gebeurtenissen en gebruikt in plaats daarvan een Adobe Experience Platform-schema. Dit betekent dat geen van de bestaande segmenten of berekende maatstaven compatibel is met [!UICONTROL Customer Journey Analytics].

+++

+++**Hoe werkt [!UICONTROL Customer Journey Analytics] handgreep `Uniques Exceeded` beperkingen?**

[!UICONTROL Customer Journey Analytics] heeft geen unieke waardebeperkingen, dus hoeft u zich daar geen zorgen over te maken!

+++

+++**Als ik een bestaande [!DNL Data Workbench] klant, kan ik naar [!UICONTROL Customer Journey Analytics] nu?**

Het hangt van uw gebruiksgeval af, dus werk met uw team van de Rekening van de Adobe. Uw huidige gebruikscase is mogelijk al geschikt voor Customer Journey Analytics.

+++

## 9. De verbindingsgrootte schatten {#estimate-size}

Zie [Gebruik schatten en beheren](/help/technotes/estimate-usage.md).

## 10. Over gebruiksoverschrijdingen {#overage}

De gebruikslimieten worden regelmatig gecontroleerd en door de Adobe afgedwongen. &quot;Rijen van gegevens&quot;: de dagelijkse gemiddelde rijen van gegevens die beschikbaar zijn voor analyse binnen de Customer Journey Analytics.

Bijvoorbeeld, laten wij zeggen uw contract u aan één miljoen rijen van gegevens machtigt. Stel dat u op dag 1 van het gebruik van Customer Journey Analytics twee miljoen rijen gegevens uploadt. Op dag 2, schrapt u 1 miljoen rijen en houdt uw gebruik bij dat gecommitteerde maximum (namelijk één miljoen rijen van gegevens) voor de rest van uw Termijn van de Vergunning. Afhankelijk van uw contractvoorwaarden, kunt u nog steeds geproreerde overgebruikskosten voor dag 1 maken, aangezien u uw licentierechten voor &quot;rijen met gegevens&quot; hebt overschreden.

## 11. Verschillen in onderzoeksgegevens {#discrepancies}

Soms ziet u dat het totale aantal gebeurtenissen dat door uw verbinding wordt opgenomen afwijkt van het aantal rijen in de gegevensset in [!UICONTROL Adobe Experience Platform]. In dit voorbeeld heeft de dataset &quot;B2B Impression&quot; 7650 rijen, maar de dataset bevat 3830 rijen in [!UICONTROL Adobe Experience Platform]. Er zijn verschillende redenen waarom er verschillen kunnen optreden en de volgende stappen kunnen worden uitgevoerd om een diagnose te stellen:

1. Verdeel deze dimensie door **[!UICONTROL Platform Dataset ID]** en u merkt twee datasets met de zelfde grootte maar verschillend **[!UICONTROL Platform Dataset IDs]**. Elke dataset heeft 3825 verslagen. Dat betekent [!UICONTROL Customer Journey Analytics] vijf records genegeerd wegens ontbrekende personen-id&#39;s of ontbrekende tijdstempels:

   ![uitsplitsing](assets/data-size2.png)

1. Als u bovendien incheckt [!UICONTROL Adobe Experience Platform], is er geen dataset met ID &quot;5f21c12b732044194bffc1d0&quot;, vandaar dat iemand deze specifieke dataset van schrapte [!UICONTROL Adobe Experience Platform] wanneer de eerste verbinding is gemaakt. Later werd het opnieuw toegevoegd aan de Customer Journey Analytics, maar een ander [!UICONTROL Platform Dataset ID] is gegenereerd door [!UICONTROL Adobe Experience Platform].

Meer informatie over de [implicaties van gegevensset en het schrappen van verbindingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html#implications-of-deleting-data-components) in [!UICONTROL Customer Journey Analytics] en [!UICONTROL Adobe Experience Platform].


## 12. Regionale gegevensverzameling

De Adobe Experience Cloud maakt gebruik van regionale gegevensverzameling (Regional Data Collection, RDC), zodat interacties tussen uw bezoekers en Adobe- en niet-Adobe-oplossingen zo dicht mogelijk bij uw bezoekers kunnen plaatsvinden. Zodra de gegevens regionaal bij een Centrum van de Inzameling van Gegevens (DCC, ook gekend als plaats van de Rand, deel van de Edge Network van het Platform) worden verzameld, door:sturen het over een veilige verbinding aan de relevante oplossingen die op de configuratie van uw gegevensstroom en/of gebeurtenis het door:sturen worden gebaseerd.

![Gegevensstroom met behulp van Edge Network](https://experienceleague.adobe.com/docs/experience-platform/assets/collection.png)

Bij het regionale gegevensverzamelingsproces worden de volgende stappen uitgevoerd:

1. DNS lost automatisch de inzameling hostname aan het IP adres van het Centrum van de Inzameling van Gegevens dichtst bij de bezoeker op.
1. De bezoeker verzendt de gegevens naar die locatie.
1. De gegevens worden onmiddellijk door:sturen over een veilige verbinding aan de oplossingen die door de datastream of gebeurtenis door:sturen configuratie worden bepaald.

Het gebruik van regionale gegevensverzameling biedt verschillende voordelen:

* **Prestaties**: Met de RDC maken uw bezoekers verbinding met de dichtstbijzijnde DCC. Deze optimalisatie biedt de snelste responstijd, wat resulteert in nauwkeurigere tracking en snellere laadtijden.
* **Redundantie**: Als de communicatie tussen de DCC en uw DPC wordt onderbroken, slaat de RDC-infrastructuur van de Adobe gegevens lokaal op en stuurt deze door naar de DPC wanneer de communicatie wordt hersteld.

De regionale distributiesector omvat momenteel de volgende locaties (afhankelijk van de verandering):


| RDC-type | Centra voor gegevensverzameling |
| --- | --- |
| Algemeen (standaard) | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Alleen Amerika | Oregon, Virginia |
| Alleen Europa | Ierland, Parijs |
| Alleen Azië - Stille Oceaan | Mumbai, Singapore, Tokio, Sydney |

{style="table-layout:auto"}

Wanneer de gegevens het regionale gegevenscentrum raken, bepaalt de configuratie van de gegevensstroom hoe de gegevens verder worden verpletterd.

Customer Journey Analytics vereist datasets van Adobe Experience Platform, zodat vereist uw datastream/gebeurtenis die configuratie door:sturen de dienst van Adobe Experience Platform om de gegevens van het regionale gegevenscentrum aan het gegevenscentrum te leiden waar uw instantie van Adobe Experience Platform wordt gevestigd. Customer Journey Analytics en zijn ondersteunende diensten en infrastructuur worden op hetzelfde Adobe Experience Platform-exemplaar ingezet.


Zie [Overzicht van gegevensverzameling](https://experienceleague.adobe.com/docs/experience-platform/collection/home.html) voor meer informatie over het proces van gegevensverzameling buiten de Adobe Experience Platform Edge Network en haar regionale datacentra.
