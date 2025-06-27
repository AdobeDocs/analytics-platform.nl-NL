---
title: Deelvenster Tijd van afspelen van media
description: Leer hoe u het deelvenster Media Playback Time Spent in Analysis Workspace kunt gebruiken en interpreteren.
feature: Panels
exl-id: de0fdbea-71f0-445b-a1e4-c7e895f142d4
role: User
source-git-commit: 8054aab28c405f6a9dd24306a086c78069032999
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# Afspeeltijd van media in deelvenster {#media-playback-time-spent-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaplaybacktimespent_button"
>title="De afspeeltijd van media is verstreken"
>abstract="Maak een deelvenster voor het analyseren van het videoverbruik in de loop der tijd, met verschillende granulariteitsniveaus en de mogelijkheid om af te breken en te vergelijken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaplaybacktimespent_panel"
>title="De afspeeltijd van media is verstreken"
>abstract="Analyseer het videogebruik in de loop der tijd, selecteer diverse granulariteiten, en naar keuze onderverdeeld en vergelijk het gebruiken van segmenten, dimensies, afmetingspunten, of datumwaaiers."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_Dit artikel documenteert de media playbacktijd besteed paneel in_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**&#x200B;_.<br/>_zie [ de playbacktijd van Media besteed paneel ](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/panels/media-playback-time-spent) voor_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


>[!NOTE]
>
>Het deelvenster Mediapubliek met een gemiddeld aantal minuten is alleen beschikbaar voor klanten die de invoegtoepassing voor de verzameling van streaming media voor Customer Journey Analytics hebben aangeschaft.
>&#x200B;>Neem contact op met uw Adobe-verkoper of Adobe-accountteam voor meer informatie.
>

In het deelvenster **[!UICONTROL Media playback time spent]** kunt u het afspelen in de loop van de tijd analyseren met details over de piekfrequentie en de mogelijkheid om af te breken en te vergelijken.

In Analysis Workspace is de afspeeltijd de tijd die nodig is om uw mediastreams op een bepaald tijdstip weer te geven. Het omvat pauze, buffer, en tijd om te beginnen.

Klanten die de invoegtoepassing voor de verzameling van streaming media hebben aangeschaft, kunnen de afspeeltijd analyseren om waardevolle insight te winnen voor de kwaliteit van de inhoud en de betrokkenheid van de viewer. En om te helpen bij het oplossen van problemen of het plannen voor volume of schaal.

De bestede afspeeltijd kan u helpen begrijpen:

* waar de piek van de gelijktijdige optreden zich voordeed.

* Waar is een offsite opgetreden.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ bestede tijd van de media ](https://video.tv.adobe.com/v/338699){target="_blank"} voor een demo video.

{{videoaa}}

>[!ENDSHADEBOX]


## Gebruiken

Een deelvenster **[!UICONTROL Media playback time spent]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Media playback time spent]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [ een paneel ](panels.md#create-a-panel) creëren.

1. Selecteer een gegevensweergave voor het deelvenster waarvoor componenten zijn geconfigureerd in de verzameling Streaming media.

1. Specificeer de [ input ](#panel-input) voor het paneel.

1. Neem de [ output ](#panel-output) voor het paneel waar.


### Deelvensterinvoer

U kunt het deelvenster Tijd voor afspelen van media configureren met de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---|---|
| Datumbereik van deelvenster | Het standaarddatumbereik van het deelvenster is Vandaag. U kunt de presentatie bewerken om een enkele dag of maanden tegelijk weer te geven.<br> Deze visualisatie is beperkt tot 1440 rijen van gegevens (bijvoorbeeld, 24 uur bij miniem-vlakke granulariteit). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Granulariteit | De standaardwaarde voor granulariteit is Minute.<br> Deze visualisatie is beperkt tot 1440 rijen van gegevens (bijvoorbeeld, 24 uur bij miniem-vlakke granulariteit). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Samenvattingsnummers deelvenster | Er is een samenvattingsnummer beschikbaar om datum- of tijdgegevens voor de afspeeltijd te zien. Bij Maximaal worden details voor de piekfrequentie weergegeven. Bij Minimum worden details voor de dal weergegeven. De som verhoogt de totale playbacktijd die voor de selectie wordt doorgebracht. De paneelstandaard toont slechts Maximum, maar u kunt het veranderen om Minimum, Som, of om het even welke combinatie drie te tonen.<br> als u onderverdelingen gebruikt, wordt een samenvattingsaantal getoond voor elk. |
| Uitsplitsing naar serie | U kunt desgewenst de visualisatie opsplitsen in segmenten, dimensies, dimensiepunten of datumbereiken.<p>- U kunt maximaal 10 regels tegelijk weergeven. Uitsplitsingen zijn beperkt tot één niveau.</p><p>- Wanneer u een dimensie sleept, worden de bovenste dimensie-items automatisch geselecteerd op basis van het datumbereik van het geselecteerde deelvenster.</p>- Als u datumbereiken wilt vergelijken, sleept u twee of meer datumbereiken naar het uitsplitsingssegment van de reeks. |
| Tijdnotatie | U kunt de afspeeltijd in `Hours:Minutes:Seconds` (standaard) of in `Minutes` (die in gehele getallen wordt weergegeven, naar boven afgerond op 0,5) weergeven. |
| Weergave datumvolgorde | Als u minstens twee segmenten van het datumbereik als reeksonderverdelingen hebt geplaatst, ziet u de optie om of bedekking (gebrek) of opeenvolgend te selecteren. Met Bedekking worden de lijnen weergegeven met een gemeenschappelijke beginpunt op de x-as, zodat deze parallel lopen. De lijnen met hun specifieke beginpunt op de x-as worden opeenvolgend weergegeven. Als de gegevenslijnen omhoog (bijvoorbeeld, eind segment 1 bij 8:44 pm en segment 2 begint bij 8:45 pm), dan tonen de lijnen in opeenvolging. |


![ de tijd doorgebrachte standaardmening van playbook van Media.](assets/mpts_default_view.png)

### Deelvensteruitvoer

In het deelvenster Afspeeltijd van media worden een regeldiagram en samenvattingsnummers geretourneerd met gegevens over de maximale, minimale en/of totale afspeeltijd. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren.

Op elk ogenblik, uitgezocht ![ geef de playbacktijd van Media uit doorbrengt paneel ](/help/assets/icons/Edit.svg) om het paneel uit te geven en opnieuw te bouwen.

Als u reeksindeling selecteert, worden een regel in het lijndiagram en een samenvattingsnummer voor elke regel weergegeven:

![ de media playbacktijd bestede output die een lijngrafiek en een samenvatting toont.](assets/mpts_outputs1.png)

### Gegevensbron

De enige metrische waarde die in dit deelvenster kan worden gebruikt, is Afspeeltijd.

| Metrisch | Beschrijving |
|---|---|
| Afspeeltijd besteed | Totaal `hours:minutes:seconds` (of `minutes` ) van inhoud die tijdens de geselecteerde granulariteit wordt weergegeven, inclusief pauze, buffer en begintijd. |

## Veelgestelde vragen

| Vraag | Antwoord |
|---|---|
| Waar is de tabel voor vrije vorm? Hoe kan ik de gegevensbron zien? | <p></p><p>De tabel Freeform is niet beschikbaar in deze weergave. Als u de gegevensbron wilt downloaden, selecteert u in het contextmenu in het lijndiagram de optie waarmee u het CSV-bestand wilt downloaden.</p> |
| <p>Waarom veranderde mijn granulariteit?</p> | <p>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken.</p><p></p><p>Wanneer u overschakelt van een groter datumbereik naar een kleiner datumbereik, wordt de granulariteit bijgewerkt naar het laagste detailniveau dat is toegestaan als het datumbereik wordt gewijzigd. Als u een hogere granulariteit wilt weergeven, bewerkt u het deelvenster en maakt u het opnieuw.</p> |
| <p></p><p>Hoe vergelijk ik videonamen, segmenten, inhoudstypen en meer?</p> | <p>Om deze in één enkele visualisatie te vergelijken, sleep segmenten, dimensies, of specifieke afmetingspunten in het segment van de reeksuitsplitsing.</p><p></p><p>De weergave is beperkt tot tien uitsplitsingen. Als u meer dan 10 wilt weergeven, moet u meerdere deelvensters gebruiken.</p> |
| Hoe vergelijk ik datumbereiken? | Om datumwaaiers in één enkele visualisatie te vergelijken, gebruik de reeksonderverdelingen door 2 of meer datumwaaiers te slepen. Deze datumbereiken overschrijven het datumbereik van het deelvenster. |
| Hoe kan ik het visualisatietype wijzigen? | <p></p><p>In dit deelvenster kunt u alleen de lijnen voor de tijdreeks visualiseren.</p> |
| Kan ik anomaliedetectie uitvoeren? | <p></p><p>Nee. Anomaly-detectie is niet beschikbaar voor dit deelvenster.</p> |


>[!MORELIKETHIS]
>
>[ creeer een paneel ](/help/analysis-workspace/c-panels/panels.md#create-a-panel)
>&#x200B;>[Mediagemiddelde minieme publiekspaneel ](average-minute-audience-panel.md)
>&#x200B;>[Deelvenster Mediagelijktijdige viewers ](media-concurrent-viewers.md)
>
