---
title: Veelgestelde vragen over Customer Journey Analytics
description: Customer Journey Analytics - Veelgestelde vragen.
exl-id: 778ed2de-bc04-4b09-865e-59e386227e06
solution: Customer Journey Analytics
feature: FAQ
role: User
source-git-commit: 220ebd7dbc3fa75d221690cd6e5828bd94395434
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---

# Veelgestelde vragen

Adobe Customer Journey Analytics is het product van de volgende generatie. In dit artikel worden antwoorden gegeven op veelgestelde vragen over Customer Journey Analytics. Voor meer informatie, herzie [ de eigenschapsteun van Customer Journey Analytics ](/help/getting-started/aa-vs-cja/cja-aa.md).

## 1. Vereisten {#prerequisites}

+++**heb ik [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] voor [!UICONTROL Customer Journey Analytics] nodig?**

Nee, [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] zijn niet vereist voor [!UICONTROL Customer Journey Analytics] . Ze worden zelfs nog niet ondersteund.

+++


+++**heb ik [!UICONTROL Experience Cloud ID] (ECID) voor [!UICONTROL Customer Journey Analytics] nodig?**

Nr, [!UICONTROL Customer Journey Analytics] steunt om het even welke identiteitskaart in een dataset, of dat [!UICONTROL ECID] of een andere identiteitskaart is u kiest.

+++


+++**wat als ik (Extraheren, Transformeren, Lading) mijn gegevens voorafgaand aan [!UICONTROL Customer Journey Analytics] moet ETL?**

Customer Journey Analytics omvat [ Prep van Gegevens ](https://experienceleague.adobe.com/docs/experience-platform/data-prep/api/overview.html) mogelijkheden helpen uw gegevens omzetten alvorens het in het de gegevensmeer van Adobe Experience Platform te zetten. Als u ETL nodig hebt nadat het gegeven reeds is opgenomen, [ verstrekt de Dienst van de Vraag van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/tutorials/queries/understanding-query-service.html#queries) sommige beperkte opties, hoewel er extra betrokken kosten kunnen zijn.

+++


## 2. Vastleggingsgegevens {#stitching}

+++**kan [!UICONTROL Customer Journey Analytics] &quot;verbinden&quot;over apparaten of over datasets?**

Ja. [!UICONTROL Customer Journey Analytics] heeft [ Stitching ](../stitching/overview.md) functionaliteit die over voor authentiek verklaarde en niet voor authentiek verklaarde gebeurtenissen binnen een dataset werkt. Door deze stitching kunnen afwijkende records worden omgezet in één naadloze id, voor analyse op het niveau van de persoon.
Voorts wanneer een gemeenschappelijke namespaceidentiteitskaart (identiteitskaart van de Persoon) over datasets binnen a [ Verbinding ](/help/connections/overview.md) wordt gebruikt, kunt u analyse op een naadloze combinatie veelvoudige datasets in werking stellen, &quot;vastgemaakt&quot;op het persoonniveau.

+++


+++**stitching van anoniem gedrag aan voor authentiek verklaard gesteund gedrag?**

Ja. [ Stitching ](../stitching/overview.md) kijkt gebruikersgegevens van zowel voor authentiek verklaarde als niet voor authentiek verklaarde zittingen om een vastgemaakte identiteitskaart te produceren.

+++


+++**hoe &quot;replay&quot;werk in het stitching?**

Gegevens worden opnieuw afgespeeld op basis van unieke id&#39;s die het heeft geleerd. Replay is bedoeld om aanvankelijk niet-geverifieerde gebeurtenissen te koppelen aan apparaten die in de tussentijd zijn geïdentificeerd. [Meer informatie](../stitching/overview.md)

+++


+++**hoe het stitching van historische gegevens (backfill) werk?**

Als Adobe voor het eerst is ingeschakeld, wordt een back-up van opgeslagen gegevens gemaakt die teruggaat naar de door u geselecteerde gegevens (maximaal 25 maanden, afhankelijk van het Customer Journey Analytics-pakket waarop u recht hebt). Om deze backfill te kunnen uitvoeren, moet de tijdelijke id bestaan in de niet-opgeslagen gegevens die veel terug in de tijd zijn. [Meer informatie](../stitching/overview.md)

+++


+++**wat is het verwachte gedrag voor niet-gestikte verslagen van de profielgegevensreeks?**

**scenario van het Voorbeeld**: U sluit zich aan bij twee datasets in een verbinding van Customer Journey Analytics door `CRMid` als Persoon identiteitskaart te gebruiken. Eén is een webgebeurtenisdataset met `CRMid` in alle records. De andere dataset is een de profielgegevensreeks van CRM. 40% van de gegevensset CRM heeft `CRMid` aanwezig in de gegevensset voor webgebeurtenissen. De andere 60% zijn niet aanwezig in de de gebeurtenisdataset van het Web - verschijnen deze verslagen in rapportering in Analysis Workspace?<p> **Antwoord**: De rijen van het profiel die geen gebeurtenissen verbonden aan hen hebben worden opgeslagen in Customer Journey Analytics. U kunt ze echter pas in Analysis Workspace bekijken als er een gebeurtenis met die id wordt weergegeven.

+++

## 3. Gegevens ophalen in [!UICONTROL Customer Journey Analytics] {#ingest}

+++**Kan ik gegevens van verschillende [!UICONTROL Adobe Experience Platform] zandbakken in één [!UICONTROL Customer Journey Analytics] verbinding combineren?**

Nee, u hebt geen toegang tot gegevens in verschillende sandboxen. U kunt alleen gegevenssets combineren die zich binnen dezelfde sandbox bevinden. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html#select-sandbox-and-datasets)

+++


+++**Hoe verbind ik online gegevens met off-line gegevens in [!UICONTROL Customer Journey Analytics]?**

Zolang de persoonidentiteitskaart tussen datasets aanpast, kan [!UICONTROL Customer Journey Analytics] segmenten, attributie, stroom, reserve, etc. over datasets verbinden.

+++


+++**Hoe breng ik mijn off-line gegevens in [!UICONTROL Customer Journey Analytics]?**

Met je recht op Customer Journey Analytics kun je gegevens invoeren in Experience Platform. Vervolgens kunt u verbindingen maken met die gegevens en gegevensweergaven in [!UICONTROL Customer Journey Analytics] voor rapportage in Analysis Workspace. Het Experience Platform-team voor gegevens over instapkaarten kan u indien nodig helpen aanbevelingen te doen of advies in te winnen.

+++


+++**hoe ik [!UICONTROL Adobe Analytics] gegevens in [!UICONTROL Customer Journey Analytics] krijg?**

[!UICONTROL Adobe Analytics] gegevens kunnen met Experience Platform door de [ Analytics bronschakelaar ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) worden verbonden. De meeste velden van het type [!UICONTROL Adobe Analytics] worden overgedragen in de XDM-indeling, maar andere velden zijn nog niet beschikbaar.

+++


+++**hoe lang duurt het om datasetelementen in een gegevensmening samen te stellen?**

Een paar uur om te beginnen en een paar dagen om een back-up te maken van de laatste 13 maanden van gegevens.

+++


+++**is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen?**

Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klant identiteitskaart gebruiken, die geen PII is.

+++


+++**wat zijn de grenzen voor het opnemen voorbij of toekomstige data/timestamps in de gebeurtenisdatasets van Customer Journey Analytics?**

* Met betrekking tot eerdere datums/tijdstempels: gebeurtenisgegevens tot tien jaar oud.
* Met betrekking tot toekomstige datums/tijdstempels: gebeurtenisgegevens (voorspellend) tot één maand in de toekomst.

+++


## 4. Latentieoverwegingen {#latency}

>[!NOTE]
>
>Er is geen vaste gegevensgrootte in Customer Journey Analytics en Adobe kan zich dus niet vastleggen op een standaardinnametijdstip. Adobe werkt actief aan het verkleinen van deze latentie door nieuwe updates en optimalisatie van inname.

* Live-gegevens of -gebeurtenissen: verwerkt en opgenomen binnen 90 minuten, zodra gegevens beschikbaar zijn in Adobe Experience Platform. (Batchgrootte > 50 miljoen rijen: langer dan 90 minuten.) Als stikken ingeschakeld is, kan de inname tot 4 uur duren. Zie [ guardrails ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/guardrails) voor meer details.
* Kleine backfills: binnen zeven dagen
* Grote achtergronden: binnen 30 dagen

Adobe heeft onlangs de manier gewijzigd waarop gegevens in Customer Journey Analytics worden verwerkt:

* Gebeurtenisgegevens voor de &#39;huidige&#39; dag worden gestreamd als live-gegevens. Om het even welke gegevens met een gebeurtenistijd voorafgaand aan 11 :59: 59 pm (23 :59: 59) op de vorige dag wordt behandeld als backfill.
* Alle gebeurtenisgegevens met een tijdstempel van meer dan 24 uur oud (zelfs als deze zich in dezelfde batch bevinden als nieuwere gegevens) worden beschouwd als backfill en krijgen een lagere prioriteit.

## 5. Stel het schuifvenster in voor [!UICONTROL Connection] gegevensbehoud {#data-retention}

Met de instelling [**[!UICONTROL Enable rolling data window]**](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html#create-connection) kunt u Customer Journey Analytics-gegevensbewaring definiëren als een schuivend venster in maanden (drie maanden, zes maanden enzovoort). Deze wordt ingesteld op een [!UICONTROL connection] -niveau, niet op een [!UICONTROL dataset] -niveau. Het bewaren van gegevens is gebaseerd op de tijdstempels van de gebeurtenisdataset en is slechts op gebeurtenisdatasets van toepassing. Er bestaat geen instelling voor gegevensbehoud voor profiel- of opzoekgegevenssets omdat er geen relevante tijdstempels zijn.

Het belangrijkste voordeel is dat u alleen gegevens opslaat of rapporteert die van toepassing zijn en nuttig zijn, en oudere gegevens verwijdert die niet meer nuttig zijn. Het helpt u onder uw contractgrenzen te blijven en vermindert het risico van overleeftijdskosten.

## 6. Gevolgen van het verwijderen van gegevenscomponenten {#deletion}

Voor gegevensschrapping, zou u over zes types van componenten moeten ongerust zijn: zandbak, schema, dataset, verbinding, gegevensmening, en het project van Workspace. Hier zijn enkele mogelijke scenario&#39;s voor het verwijderen van een van deze componenten:

| Als u... | Dit gebeurt... |
| --- | --- |
| Een sandbox verwijderen in [!UICONTROL Adobe Experience Platform] | Als u een sandbox verwijdert, wordt de gegevensstroom gestopt naar alle [!UICONTROL Customer Journey Analytics] -verbindingen met gegevenssets in die sandbox. Verbindingen, gegevensweergaven, metriek en afmetingen met betrekking tot deze verwijderde sandbox worden ook verwijderd. | |
| Schrap een schema in [!UICONTROL Adobe Experience Platform], maar niet de dataset/s verbonden aan dit schema | [!UICONTROL Adobe Experience Platform] staat het verwijderen van [!UICONTROL schemas] waaraan een of meer [!UICONTROL datasets] is gekoppeld, niet toe. Nochtans, kan Admin met de aangewezen reeks rechten de datasets eerst schrappen en dan het schema schrappen. |
| Een gegevensset verwijderen uit het gegevenspeer [!UICONTROL Adobe Experience Platform] | Als u een gegevensset in het gegevensmeer van Adobe Experience Platform verwijdert, stopt u de gegevensstroom van die gegevensset naar Customer Journey Analytics-verbindingen die die gegevensset bevatten. Om het even welke gegevens van die dataset worden automatisch geschrapt van de bijbehorende verbindingen van Customer Journey Analytics. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics] | Neem contact op met uw Adobe-accountteam om het verwijderen van een gegevensset binnen een verbinding die is opgeslagen, in beweging te brengen. |
| Een batch uit een dataset verwijderen (in [!UICONTROL Adobe Experience Platform]) | Als een batch uit een [!UICONTROL Adobe Experience Platform] dataset wordt verwijderd, wordt dezelfde batch verwijderd uit Customer Journey Analytics-verbindingen die die specifieke batch bevatten. Customer Journey Analytics wordt in [!UICONTROL Adobe Experience Platform] op de hoogte gesteld van het verwijderen van batches. |
| Schrap een partij **terwijl het** in [!UICONTROL Customer Journey Analytics] wordt opgenomen | Als er slechts één batch in de dataset staat, worden geen gegevens of gedeeltelijke gegevens van die batch weergegeven in [!UICONTROL Customer Journey Analytics]. De inname wordt teruggedraaid. Bijvoorbeeld, als er vijf partijen in de dataset zijn en drie van hen reeds zijn opgenomen toen de dataset werd geschrapt, verschijnen de gegevens van die drie partijen in [!UICONTROL Customer Journey Analytics]. |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Op dezelfde manier werken alle Workspace-projecten die afhankelijk zijn van gegevensweergaven in de verwijderde verbinding, niet meer.</li></ul> |
| Een gegevensweergave verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutbericht geeft aan dat Workspace-projecten die van deze verwijderde gegevensweergave afhankelijk zijn, niet meer werken. |

## 7. Overwegingen bij het samenvoegen van rapportenpakketten in Customer Journey Analytics {#merge-reportsuite}

Als u van plan bent om de gegevens van Adobe Analytics door de [ bron van Adobe Analytics schakelaar ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) in te voeren, overweeg deze vertakkingen wanneer het samenvoegen van twee of meer het rapportreeksen van Adobe Analytics.

| Probleem | Overwegingen |
| --- | --- |
| Variabelen | Variabelen zoals [!UICONTROL eVars] worden mogelijk niet uitgelijnd in hele rapportsuites. EVar1 in rapportsuite 1 verwijst bijvoorbeeld mogelijk naar **[!UICONTROL Page]** . In rapportsuite 2 verwijst eVar1 mogelijk naar **[!UICONTROL Internal Campaign]** , wat leidt tot gemengde en onjuiste rapportage. |
| [!UICONTROL Sessions] en [!UICONTROL People] counts | Ze worden gededupliceerd door de rapportsuites. Hierdoor komen aantallen mogelijk niet overeen. |
| Metrische deduplicatie | Hiermee dupliceert u instanties van een metrische waarde (bijvoorbeeld [!UICONTROL Orders] ) als meerdere rijen dezelfde transactie-id hebben (bijvoorbeeld [!UICONTROL Purchase ID] ). Hiermee voorkomt u dat belangrijke meetgegevens te veel worden geteld. Dientengevolge, kunnen de metriek zoals [!UICONTROL Orders] niet over rapportsuites optellen. |
| Valuta | Valuta-conversie wordt nog niet ondersteund in Customer Journey Analytics. Als de rapportsuites u probeert samen te voegen verschillende basisvaluta&#39;s gebruiken, kunnen de problemen zich voordoen. |
| [!UICONTROL Persistence] | [ persistentie ](../data-views/component-settings/persistence.md) breidt zich over rapportsuites uit, die [!UICONTROL segments], [!UICONTROL attribution], etc. beïnvloedt. Het is mogelijk dat getallen niet correct worden opgeteld. |
| [!UICONTROL Classifications] | [!UICONTROL Classifications] wordt niet automatisch gededupliceerd bij het samenvoegen van rapportsuites. Wanneer u meerdere classificatiebestanden combineert in één [!UICONTROL lookup] -dataset, kunnen er problemen optreden. |

## 8. [!UICONTROL Adobe Analytics] componenten

+++**Kan ik [!UICONTROL audiences] van [!DNL Customer Journey Analytics] aan Experience Platform Real-Time CDP, of andere toepassingen van Experience Cloud delen/publiceren?**

U kunt [ publiek ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/audiences/publish) creëren en publiceren dat in Customer Journey Analytics aan het Profiel van de Klant in real time in Adobe Experience Platform wordt geïdentificeerd voor klant die en verpersoonlijking richt.

+++

+++**wat gebeurde met mijn oude [!UICONTROL eVar] plaatsen?**

[!UICONTROL eVars] , [!UICONTROL props] en [!UICONTROL events] in de Adobe Analytics-zin bestaan niet meer in [!UICONTROL Customer Journey Analytics] . U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd.

+++

+++**waar zijn al mijn zitting en veranderlijke persistentie montages nu?**

[!UICONTROL Customer Journey Analytics] past al deze instellingen toe tijdens de rapporttijd en deze instellingen worden nu live weergegeven in gegevensweergaven. De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken.

+++

+++**wat aan uw bestaande segmenten/berekende metriek gebeurt?**

[!UICONTROL Customer Journey Analytics] gebruikt niet langer variabelen, profielen of gebeurtenissen en gebruikt in plaats daarvan geen Adobe Experience Platform-schema. Dit betekent dat geen van de bestaande segmenten of berekende maateenheden compatibel is met [!UICONTROL Customer Journey Analytics] .

+++

+++**hoe [!UICONTROL Customer Journey Analytics] handvat `Uniques Exceeded` beperkingen?**

[!UICONTROL Customer Journey Analytics] heeft geen unieke waardebeperkingen en hoeft u zich daar dus geen zorgen over te maken!

+++

+++**als ik een bestaande [!DNL Data Workbench] klant ben, kan ik [!UICONTROL Customer Journey Analytics] nu bewegen?**

Het hangt af van uw gebruikscase. Werk dus samen met uw Adobe-accountteam. Je huidige gebruikscase is mogelijk al geschikt voor Customer Journey Analytics.

+++

## 9. De verbindingsgrootte schatten {#estimate-size}

Zie [ het gebruik van Verbindingen ](/help/connections/manage-connections.md#usage).

## 10. Over gebruiksoverschrijdingen {#overage}

De gebruikslimieten worden regelmatig gecontroleerd en afgedwongen door Adobe. &quot;Rijen van gegevens&quot;: de dagelijkse gemiddelde rijen van gegevens die in Customer Journey Analytics voor analyse beschikbaar zijn.

Uw contract geeft u bijvoorbeeld recht op één miljoen rijen met gegevens. Stel dat je op dag 1 van Customer Journey Analytics twee miljoen rijen gegevens uploadt. Op dag 2, schrapt u 1 miljoen rijen en houdt uw gebruik bij dat gecommitteerde maximum (namelijk één miljoen rijen van gegevens) voor de rest van uw Termijn van de Vergunning. Afhankelijk van uw contractvoorwaarden, kunt u nog steeds geproreerde overgebruikskosten voor dag 1 maken, aangezien u uw licentierechten voor &quot;rijen met gegevens&quot; hebt overschreden.

## 11. Verschillen in onderzoeksgegevens {#discrepancies}

Soms ziet u dat het totale aantal gebeurtenissen dat door de verbinding wordt opgenomen, verschilt van het aantal rijen in de gegevensset in [!UICONTROL Adobe Experience Platform] . In dit voorbeeld heeft de dataset &quot;B2B Impression&quot; 7650 rijen, maar de dataset bevat 3830 rijen in [!UICONTROL Adobe Experience Platform]. Er zijn verschillende redenen waarom er verschillen kunnen optreden en de volgende stappen kunnen worden uitgevoerd om een diagnose te stellen:

1. Verdeel deze dimensie door **[!UICONTROL Platform Dataset ID]** en u merkt twee datasets met de zelfde grootte maar verschillend **[!UICONTROL Platform Dataset IDs]**. Elke dataset heeft 3825 verslagen. Dat betekent dat [!UICONTROL Customer Journey Analytics] vijf records heeft genegeerd omdat de persoon-id&#39;s ontbreken of er tijdstempels ontbreken:

   ![ verdeling ](assets/data-size2.png)

1. Als u [!UICONTROL Adobe Experience Platform] incheckt, is er bovendien geen gegevensset met ID &quot;5f21c12b732044194bffc1d0&quot;, vandaar dat iemand deze specifieke gegevensset heeft verwijderd uit [!UICONTROL Adobe Experience Platform] toen de eerste verbinding werd gemaakt. Later werd het bestand opnieuw aan Customer Journey Analytics toegevoegd, maar er werd een andere [!UICONTROL Platform Dataset ID] gegenereerd door [!UICONTROL Adobe Experience Platform] .

Lees meer over de [ implicaties van dataset en verbindingsschrapping ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html#implications-of-deleting-data-components) in [!UICONTROL Customer Journey Analytics] en [!UICONTROL Adobe Experience Platform].


## 12. Regionale gegevensverzameling

De Adobe Experience Cloud maakt gebruik van regionale gegevensverzameling (Regional Data Collection, RDC), zodat de interactie tussen uw bezoekers en Adobe en niet-Adobe-oplossingen zo dicht mogelijk bij uw bezoekers plaatsvindt. Zodra de gegevens regionaal bij een Centrum van de Inzameling van Gegevens (DCC, ook als plaats van Edge, deel van het Platform Edge Network) worden verzameld, door:sturen het over een veilige verbinding aan de relevante oplossingen die op de configuratie van uw gegevensstroom en/of gebeurtenis het door:sturen worden gebaseerd.

![ stroom van Gegevens gebruikend de Netwerken van de Rand ](https://experienceleague.adobe.com/docs/experience-platform/assets/collection.png)

Bij het regionale gegevensverzamelingsproces worden de volgende stappen uitgevoerd:

1. DNS lost automatisch de inzameling hostname aan het IP adres van het Centrum van de Inzameling van Gegevens dichtst bij de bezoeker op.
1. De bezoeker verzendt de gegevens naar die locatie.
1. De gegevens worden onmiddellijk door:sturen over een veilige verbinding aan de oplossingen die door de datastream of gebeurtenis door:sturen configuratie worden bepaald.

Het gebruik van regionale gegevensverzameling biedt verschillende voordelen:

* **Prestaties**: Met RDC, verbinden uw bezoekers met dichtste DCC. Deze optimalisatie biedt de snelste responstijd, wat resulteert in nauwkeurigere tracking en snellere laadtijden.
* **Overtolligheid**: Als er een verstoring in communicatie tussen DCC en uw DPC is, bewaart de infrastructuur van Adobe RDC gegevens plaatselijk, dan door:sturen het aan DPC wanneer de mededelingen worden hersteld.

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


Zie [ het overzicht van de inzameling van Gegevens ](https://experienceleague.adobe.com/docs/experience-platform/collection/home.html) voor meer informatie over het proces van gegevensinzameling voorbij Adobe Experience Platform Edge Network en zijn regionale gegevenscentra.
