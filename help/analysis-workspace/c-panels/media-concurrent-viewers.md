---
title: Deelvenster Mediagelijktijdige viewers
description: Leer het deelvenster Mediagelijktijdige viewers in Analysis Workspace gebruiken en interpreteren.
feature: Panels
exl-id: a442fb9c-165f-4136-95e2-ce92b9280c25
role: User
source-git-commit: 8054aab28c405f6a9dd24306a086c78069032999
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 0%

---

# Deelvenster Mediagelijktijdige viewers {#media-concurrent-viewers-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaconcurrentviewers_button"
>title="Gelijktijdige viewers voor media"
>abstract="Maak een deelvenster om gelijktijdige viewers gedurende een bepaalde periode te analyseren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaconcurrentviewers_panel"
>title="Gelijktijdige viewers voor media"
>abstract="Analyseer gelijktijdige viewers in de loop der tijd, bekijk piekgelijktijdige pieken, en onderdruk naar keuze en vergelijk het gebruiken van segmenten, dimensies, dimensiepunten, of datumwaaiers."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert het de gezamenlijke kijkers van Media paneel in_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**&#x200B;_.<br/>_zie [&#x200B; Medium gezamenlijke kijkers paneel &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/panels/media-concurrent-viewers) voor_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


>[!NOTE]
>
>Het deelvenster Mediapubliek met een gemiddeld aantal minuten is alleen beschikbaar voor klanten die de invoegtoepassing voor de verzameling van streaming media voor Customer Journey Analytics hebben aangeschaft.
>
>Neem contact op met uw Adobe Sales-vertegenwoordiger of Adobe-accountteam voor meer informatie.
>

Met het deelvenster **[!UICONTROL Media concurrent viewers]** kunt u in de loop der tijd gelijktijdige viewers analyseren, met details over de piekfrequentie en de mogelijkheid om af te breken en te vergelijken.

U kunt gelijktijdige viewers analyseren om te zien waar de piekgelijktijdige uitvoering plaatsvond of waar drop-outs waardevolle insight hebben verschaft voor de kwaliteit van de inhoud en de betrokkenheid van de viewer. En voor hulp bij het oplossen van problemen of het plannen voor volume of schaal.

In Analysis Workspace is de metrische waarde voor Gelijktijdige viewers het aantal unieke personen dat uw mediastreams op een bepaald tijdstip weergeeft, ongeacht het aantal sessies.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; het gezamenlijke paneel van kijkers van Media &#x200B;](https://video.tv.adobe.com/v/26990/?quality=12&learn=on){target="_blank"} voor een demo video.

{{videoaa}}

>[!ENDSHADEBOX]

## Gebruiken

Een deelvenster **[!UICONTROL Media concurrent viewers]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Media concurrent viewers]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [&#x200B; een paneel &#x200B;](panels.md#create-a-panel) creëren.

1. Selecteer een gegevensweergave voor het deelvenster waarvoor componenten zijn geconfigureerd in de verzameling Streaming media.

1. Specificeer de [&#x200B; input &#x200B;](#panel-input) voor het paneel.

1. Neem de [&#x200B; output &#x200B;](#panel-output) voor het paneel waar.

### Deelvensterinvoer

U kunt het deelvenster Mediagelijktijdige viewers configureren met de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---|---|
| **[!UICONTROL Panel date range]** | Het standaarddatumbereik van het deelvenster is Vandaag.  U kunt de presentatie bewerken om een enkele dag of maanden tegelijk weer te geven. <br> <br> Deze visualisatie is beperkt tot 1440 rijen van gegevens (bijvoorbeeld, 24 uur bij miniem-vlakke granulariteit).  Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| **[!UICONTROL Granularity]** | De standaardwaarde voor granulariteit is Minute.<br> Deze visualisatie is beperkt tot 1440 rijen van gegevens (bijvoorbeeld, 24 uur bij miniem-vlakke granulariteit).  Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| **[!UICONTROL Panel summary numbers]** | Er is een samenvattingsnummer beschikbaar om de datum- of tijdgegevens van gelijktijdige viewers weer te geven. Bij Maximaal worden details voor de piekfrequentie weergegeven. In **[!UICONTROL Minimum]** worden de details van de trog weergegeven.  In het standaardvenster wordt alleen Maximum weergegeven, maar u kunt dit wijzigen in Minimum of zowel Maximaal als Minimaal.<br><br> als u onderverdelingen gebruikt, wordt een samenvattingsaantal getoond voor elk. |
| **[!UICONTROL Series breakdown]** | U kunt desgewenst de visualisatie opsplitsen in segmenten, dimensies, dimensiepunten of datumbereiken.<br> u kunt tot 10 lijnen tegelijkertijd bekijken. Uitsplitsingen zijn beperkt tot één niveau.<br> wanneer het slepen van een afmeting, worden de hoogste afmetingspunten geselecteerd automatisch gebaseerd op de geselecteerde waaier van de paneeldatum.<br> om datumwaaiers te vergelijken, sleep 2 of meer datumwaaiers in het segment van de reeksindeling. |

Hier volgt een voorbeeld van het deelvenster dat is geconfigureerd voor **[!UICONTROL Minute]** granularity, met **[!UICONTROL Maximum only]** -samenvattingsnummers. En gesplitst naar **[!UICONTROL Other]**, **[!UICONTROL Table]**, **[!UICONTROL Mobile Phone]**, **[!UICONTROL Gaming Console]**, **[!UICONTROL Media Player]**, **[!UICONTROL Set-top Box]**, **[!UICONTROL Television]** .

![&#x200B; de Medium Gelijktijdige mening die van de Reeks van Kijkers 7 van 10 dimensies, segmenten of datumwaaiers tonen.](assets/concurrent-viewers-series-breakdown.png)

### Deelvensteruitvoer

Het deelvenster Mediagelijktijdige viewers retourneert een regeldiagram en een samenvattingsnummer met gegevens voor de maximum- en/of minimale gelijktijdige viewers.  Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren.

Op elk ogenblik, uitgezocht ![&#x200B; geef het gezamenlijke paneel van kijkers van Media &#x200B;](/help/assets/icons/Edit.svg) uit om het paneel uit te geven en opnieuw te bouwen.

Als u een reeksindeling selecteert, worden een regel in het lijndiagram en een samenvattingsnummer voor elke regel weergegeven:

![&#x200B; de Gelijktijdige output van Kijkers van Media.](assets/concurrent-viewers-output.png)

### Gegevensbron

De enige metrische waarde die in dit deelvenster kan worden gebruikt, is **[!UICONTROL Concurrent viewers]** :

| Metrisch | Beschrijving |
|---|---|
| **[!UICONTROL Concurrent viewers]** | Het aantal unieke personen dat uw mediastreams op een bepaald tijdstip weergeeft, ongeacht het aantal sessies. |

In deze weergave is geen tabel voor vrije vorm beschikbaar.  Als u de gegevensbron wilt weergeven, kunt u de gegevensbron downloaden in het contextmenu voor de visualisatie van het lijndiagram en **[!UICONTROL Download data as CSV]** selecteren.  Uitsplitsingen naar reeksen worden opgenomen.

![&#x200B; de Gelijktijdige die uitvoeropties van kijkers met &quot;gegevens van de Download als Csv&quot;worden benadrukt.](assets/concurrent-viewers-download-csv.png)

## Veelgestelde vragen

| Vraag | Antwoord |
|---|---|
| Waar is de tabel voor vrije vorm? Hoe kan ik de gegevensbron zien? | De tabel Freeform is niet beschikbaar in deze weergave.  U kunt de gegevensbron downloaden van het contextmenu van het lijndiagram en selecteren **[!UICONTROL Download data as CSV]**. |
| Waarom veranderde mijn granulariteit? | Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau).  Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken.<br><br> wanneer het veranderen van een grotere datumwaaier in kleinere, wordt granularity bijgewerkt aan het laagste die detail toelaat zodra de datumwaaier wordt veranderd. Als u een hogere granulariteit wilt weergeven, bewerkt u het deelvenster en maakt u het opnieuw. |
| Hoe vergelijk ik videonamen, segmenten, inhoudstypen en andere? | Om deze punten in één enkele visualisatie te vergelijken, sleep segmenten, dimensies, of specifieke afmetingspunten in het segment van de reeksuitsplitsing.<br><br> de mening is beperkt tot 10 uitsplitsingen.  Als u meer dan 10 wilt weergeven, moet u meerdere deelvensters gebruiken. |
| Hoe vergelijk ik datumbereiken? | Om datumwaaiers in één enkele visualisatie te vergelijken, gebruik de reeksonderverdelingen door 2 of meer datumwaaiers te slepen.  De datumbereiken overschrijven het datumbereik van het deelvenster. |
| Hoe kan ik het visualisatietype wijzigen? | In dit deelvenster kunt u alleen de lijnen voor de tijdreeks visualiseren. |
| Kan ik anomaliedetectie uitvoeren? | Nee.  Anomaly-detectie is niet beschikbaar voor dit deelvenster. |
| Waarom unieke personen gebruiken in plaats van actieve sessies? | Door unieke personen te gebruiken, kunt u ongewenste spikes verwijderen bij het weergeven van de grenzen (waar de sessies tegelijkertijd eindigen en beginnen). |
| Wat betekent het om gelijktijdige kijkers bij hogere granulariteit dan minuut te hebben? | Met een granulariteit die groter is dan een minuut, zijn gelijktijdige viewers de som van unieke gelijktijdige viewers voor alle minuten binnen dat tijdbereik.  Gelijktijdige viewers op uurniveau zijn bijvoorbeeld de som van unieke gelijktijdige viewers voor alle minuten in het uur. |
| Geeft het deelvenster Werkruimte dezelfde informatie als het rapport Gelijktijdige viewers? | Nee.  In Analysis Workspace wordt de metrische waarde voor Gelijktijdige viewers gedefinieerd als het aantal unieke personen dat uw mediastream op een bepaald tijdstip weergeeft. Ongeacht het aantal sessies.<br><br> dit metrisch is verschillend dan Gelijktijdige kijker die in de sectie van Rapporten rapporteert, die Gelijktijdige Actieve Zittingen gebruikt. Door unieke personen te gebruiken, worden ongewenste pieken bij de grenzen van de show verwijderd (waar sessies tegelijkertijd eindigen en beginnen). |

<!-- For more information about Media Concurrent Viewers, visit [MA doc page]( https://url). -->


>[!MORELIKETHIS]
>
>[&#x200B; creeer een paneel &#x200B;](/help/analysis-workspace/c-panels/panels.md#create-a-panel)
>&#x200B;>[De playbacktijd van media bestede paneel &#x200B;](media-playback-time-spent.md)
>&#x200B;>[Mediagemiddelde minieme publiekspaneel &#x200B;](average-minute-audience-panel.md)
>