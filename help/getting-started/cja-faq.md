---
title: Customer Journey Analytics Veelgestelde vragen
description: Customer Journey Analytics - Veelgestelde vragen.
exl-id: 778ed2de-bc04-4b09-865e-59e386227e06
translation-type: tm+mt
source-git-commit: 6de1907e74eb0323bde921f4400e27bcdf06cdd1
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 1%

---

# Veelgestelde vragen

[!UICONTROL Customer Journey Analytics] (CJA) is ons product van de volgende generatie. Hieronder volgen antwoorden op veelgestelde vragen over CJA. Raadpleeg [Ondersteuning van Customer Journey Analytics-functies](/help/getting-started/cja-aa.md) voor meer informatie.

## 1. Vereisten

| Aantal | Vraag | Antwoord |
| --- | --- | --- |
| a | Heb ik [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] voor [!UICONTROL Customer Journey Analytics] nodig? | Nee, [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] zijn niet vereist voor [!UICONTROL Customer Journey Analytics]. Ze worden zelfs nog niet ondersteund. |
| b | Heb ik [!UICONTROL Experience Cloud ID] (ECID) voor [!UICONTROL Customer Journey Analytics] nodig? | Nr, [!UICONTROL Customer Journey Analytics] steunt om het even welke identiteitskaart in een dataset, of dat [!UICONTROL ECID] of een andere identiteitskaart is u kiest. |
| c | Wat als ik (Extraheren, Transformeren, Laden) mijn gegevens vóór [!UICONTROL Customer Journey Analytics] moet ETL? | Customer Journey Analytics bevat [Data Prep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/api/overview.html)-mogelijkheden om uw gegevens te helpen transformeren voordat u deze in Adobe Experience Platform data Lake plaatst. Als u ETL nodig hebt nadat de gegevens al zijn ingevoerd, biedt [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/platform-learn/tutorials/queries/understanding-query-service.html?lang=en#queries) een aantal beperkte opties, maar hiervoor zijn mogelijk extra kosten van toepassing. |

## 2. Gegevens vastleggen (Kanaaloverschrijdende analyse)

| Aantal | Vraag | Antwoord |
| --- | --- | --- |
| a | Kan [!UICONTROL Customer Journey Analytics] &quot;aansluiten&quot;over apparaten of over datasets? | Ja. [!UICONTROL Customer Journey Analytics] heeft een stitching oplossing genoemd  [Kanaal Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/cca/overview.html)  (CCA). Het laat u de persoonsidentiteitskaart van een dataset re-key, die een naadloze combinatie veelvoudige datasets toelaat. |
| b | Wordt het stitching van anoniem gedrag aan voor authentiek verklaard gedrag gesteund? | Ja. [Cross-Channel ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/cca/overview.html) Analytics bekijkt gebruikersgegevens van zowel geverifieerde als niet-geverifieerde sessies om een aangesloten id te genereren. |
| c | Hoe werkt &#39;replay&#39; in CCA? | CCA &quot;replay&quot;gegevens die op unieke herkenningstekens worden gebaseerd het heeft geleerd. Bij opnieuw afspelen worden nieuwe apparaten aan de verbinding vastgezet. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/cca/replay.html?lang=en#step-1%3A-live-stitching) |
| d | Hoe werkt het stitching van historische gegevens (backfill) in CCA? | Wanneer deze optie voor het eerst is ingeschakeld, biedt Adobe een back-up van opgeslagen gegevens die teruggaat tot het begin van de vorige maand (tot 60 dagen). Om deze backfill te kunnen uitvoeren, moet de tijdelijke id bestaan in de niet-opgeslagen gegevens die veel terug in de tijd zijn. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/cca/overview.html?lang=en#enable-cross-channel-analytics) |

## 3. Gegevens ophalen in [!UICONTROL Customer Journey Analytics]

| Aantal | Vraag | Antwoord |
| --- | --- | --- |
| a | Kan ik gegevens van verschillende [!UICONTROL Adobe Experience Platform] zandbakken in één [!UICONTROL Customer Journey Analytics] verbinding combineren? | Nee, u hebt geen toegang tot gegevens in verschillende sandboxen. U kunt alleen gegevenssets combineren die zich binnen dezelfde sandbox bevinden. [Meer informatie](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-connections/create-connection.html#select-sandbox-and-datasets) |
| b | Wat is de verwachte latentie voor [!UICONTROL Customer Journey Analytics] op [!UICONTROL Adobe Experience Platform]? | <ul><li>Onder normale belasting: &lt; 60 minuten <br>**Opmerking:** In het geval van een ongebruikelijk hoog gegevensvolume door de pijpleiding, kan het tot 24 uur duren.</li><li>Backfill-gegevens (tot 13 maanden aan gegevens, ongeacht de grootte): &lt; 4 weken</li></ul> |
| c | Hoe verbind ik online gegevens met off-line gegevens in [!UICONTROL Customer Journey Analytics]? | Zolang de persoonidentiteitskaart tussen datasets aanpast, [!UICONTROL Customer Journey Analytics] filters, attributie, stroom, fallout, enz. kan verbinden over datasets. |
| d | Hoe breng ik mijn off-line gegevens in [!UICONTROL Customer Journey Analytics]? | Met uw recht op Customer Journey Analytics kunt u gegevens in het Experience Platform invoeren. Vervolgens kunt u verbindingen maken met die gegevens en gegevensweergaven in [!UICONTROL Customer Journey Analytics], voor rapportage in Analysis Workspace. Het team voor gegevens aan boord van het Experience Platform kan u, indien nodig, aanbevelingen of advies geven. |
| e | Hoe krijg ik [!UICONTROL Adobe Analytics] gegevens in [!UICONTROL Customer Journey Analytics]? | [!UICONTROL Adobe Analytics] gegevens kunnen via de  [Adobe Analytics Source Connector](https://docs.adobe.com/content/help/en/experience-platform/sources/connectors/adobe-applications/analytics.html) op het Experience Platform worden aangesloten. De meeste [!UICONTROL Adobe Analytics] gebieden worden gebracht over in formaat XDM, maar andere gebieden zijn nog niet beschikbaar (zoals [!UICONTROL Marketing Channels] afmetingen). |
| f | Hoe lang duurt het om datasetelementen in een gegevensmening samen te stellen? | Een paar uur om te beginnen en een paar dagen om een back-up te maken van de laatste 13 maanden van gegevens. |
| g | Is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen? | Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klant identiteitskaart gebruiken, die geen PII is. |

## 4. Traditionele [!UICONTROL Adobe Analytics]-componenten

| Aantal | Vraag | Antwoord |
| --- | --- | --- |
| a | Kan ik filters (segmenten) van Customer Journey Analytics aan Experience Platform Verenigd Profiel, of andere toepassingen van Experience Cloud delen/publiceren? | Nog niet, maar we werken actief aan het leveren van deze capaciteit. |
| b | Wat is er gebeurd met mijn oude eVar-omgeving? | Vars, props en gebeurtenissen in de traditionele Adobe Analytics-betekenis bestaan niet meer in [!UICONTROL Customer Journey Analytics]. U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd. |
| c | Waar zijn al mijn zitting en veranderlijke persistentie montages nu? | [!UICONTROL Customer Journey Analytics] Hiermee past u al deze instellingen toe tijdens de rapporttijd. Deze instellingen worden nu live weergegeven in de gegevensweergave. De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken! |
| d | Wat gebeurt er met onze bestaande segmenten/berekende maatstaven? | [!UICONTROL Customer Journey Analytics] gebruikt niet langer eVars, props of gebeurtenissen en gebruikt in plaats daarvan een AEP-schema. Dit betekent geen van de bestaande segmenten of de cijfers van de calc compatibel met [!UICONTROL Customer Journey Analytics] zijn. |
| e | Hoe behandelt [!UICONTROL Customer Journey Analytics] `Uniques Exceeded` beperkingen? | [!UICONTROL Customer Journey Analytics] heeft geen unieke waardebeperkingen, dus hoeft u zich daar geen zorgen over te maken! |
| f | Als ik een bestaande [!DNL Data Workbench] klant ben, kan ik nu naar [!UICONTROL Customer Journey Analytics] gaan? | Het hangt af van uw gebruikscase. Werk met uw Adobe-accountteam. Je huidige gebruiksscenario&#39;s zijn mogelijk al geschikt voor Customer Journey Analytics. |

## 5. Implicaties van het verwijderen van gegevenscomponenten

Wat het schrappen van gegevens betreft, gaat het om zes soorten componenten: zandbak, schema, dataset, verbinding, gegevensmening, en het project van de Werkruimte. Hier zijn enkele mogelijke scenario&#39;s voor het verwijderen van een van deze componenten:

| Als u... | Dit gebeurt... |
| --- | --- |
| Een sandbox verwijderen in [!UICONTROL Adobe Experience Platform] | Als u een sandbox verwijdert, wordt de gegevensstroom naar [!UICONTROL Customer Journey Analytics]-verbindingen met gegevenssets in die sandbox gestopt. Verbindingen in CJA die zijn gekoppeld aan de verwijderde sandbox worden momenteel niet automatisch verwijderd. |
| Schrap een schema in [!UICONTROL Adobe Experience Platform] maar niet de dataset/s verbonden aan dit schema | [!UICONTROL Adobe Experience Platform] staat niet toe dat schema&#39;s worden geschrapt die één of meerdere datasets verbonden aan hen hebben. Nochtans, kan Admin met de aangewezen reeks rechten de datasets eerst schrappen en dan het schema schrappen. |
| Een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform]-gegevensmeer | Het schrappen van een dataset in het gegevensmeer van AEP zal gegevensstroom van die dataset aan om het even welke Verbindingen van CJA tegenhouden die die dataset omvatten. Om het even welke gegevens van die dataset worden niet automatisch geschrapt van bijbehorende Verbindingen CJA. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics] | U kunt momenteel geen dataset verwijderen binnen een verbinding die is opgeslagen. U moet de gehele verbinding verwijderen en opnieuw beginnen. (Klanten die de CJA SKU hebben aangeschaft, kunnen echter een gegevensset in de [!UICONTROL Adobe Experience Platform]-gebruikersinterface verwijderen.) |
| Een batch uit een gegevensset verwijderen (in [!UICONTROL Adobe Experience Platform]) | Als een partij uit een [!UICONTROL Adobe Experience Platform] dataset wordt geschrapt, zal de zelfde partij uit om het even welke Verbindingen worden verwijderd CJA die die specifieke partij bevatten.  CJA wordt op de hoogte gesteld van het verwijderen van batches in [!UICONTROL Adobe Experience Platform]. |
| Een batch **verwijderen tijdens het invoegen** in [!UICONTROL Customer Journey Analytics] | Als er slechts één partij in de dataset is, zullen geen gegevens of gedeeltelijke gegevens van die partij in [!UICONTROL Customer Journey Analytics] verschijnen. De inname wordt teruggedraaid. Als, bijvoorbeeld, er 5 partijen in de dataset zijn en 3 van hen reeds zijn opgenomen toen de dataset werd geschrapt, zullen de gegevens van die 3 partijen in [!UICONTROL Customer Journey Analytics] verschijnen. |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Op dezelfde manier zullen om het even welke projecten van de Werkruimte die van gegevensmeningen in de geschrapte verbinding afhangen ophouden werkend.</li></ul> |
| Een gegevensweergave verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutenmelding zal erop wijzen dat om het even welke projecten van de Werkruimte die van deze geschrapte gegevensmening afhangen niet meer werkend zullen zijn. |
