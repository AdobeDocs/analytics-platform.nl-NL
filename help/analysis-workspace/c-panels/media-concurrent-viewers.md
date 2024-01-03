---
title: Deelvenster Mediagelijktijdige viewers
description: Het deelvenster Mediagelijktijdige viewers in Analysis Workspace gebruiken en interpreteren.
feature: Panels
exl-id: a442fb9c-165f-4136-95e2-ce92b9280c25
role: User
source-git-commit: d5d81caff62d4fb56a57739ddffb81787f684e23
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 0%

---

# Deelvenster Mediagelijktijdige viewers

U kunt gelijktijdige viewers analyseren om te begrijpen waar de piekgelijktijdige uitvoering plaatsvond of waar drop-outs waardevolle inzichten in de kwaliteit van de inhoud en de betrokkenheid van de kijker veroorzaakten, en om te helpen bij het oplossen van problemen of het plannen voor volume of schaal.

In Analysis Workspace is Gelijktijdige viewers het aantal unieke personen dat uw mediastream(s) op een bepaald tijdstip weergeeft, ongeacht het aantal sessies.

Met het deelvenster Mediagelijktijdige viewers kunt u in de loop van de tijd gelijktijdige viewers analyseren, met details over de piekfrequentie en de mogelijkheid om af te breken en te vergelijken.  Navigeer naar een gegevensweergave als u het deelvenster Mediagelijktijdige viewers wilt openen en de componenten Media Analytics wilt inschakelen. Klik vervolgens op het deelvensterpictogram helemaal links en sleep het deelvenster naar uw Analysis Workspace-project.

Hier volgt een video-overzicht van dit deelvenster:

>[!VIDEO](https://video.tv.adobe.com/v/330177/?quality=12)

## Deelvensterinvoer {#Input}

U kunt het deelvenster Mediagelijktijdige viewers configureren met de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---|---|
| Datumbereik van deelvenster | Het standaarddatumbereik van het deelvenster is Vandaag.  U kunt de presentatie bewerken om een enkele dag of maanden tegelijk weer te geven. <br> <br>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau).  Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Granulariteit | De standaardwaarde voor granulariteit is Minute. <br> <br>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau).  Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Samenvattingsnummers deelvenster | Er is een samenvattingsnummer beschikbaar om de datum- of tijdgegevens van gelijktijdige viewers weer te geven. Bij Maximaal worden details voor de piekfrequentie weergegeven. Bij Minimum worden details voor de dal weergegeven.  In het standaardvenster wordt alleen Maximum weergegeven, maar u kunt dit wijzigen in Minimum of zowel Maximaal als Minimaal.<br><br>Als u onderverdelingen gebruikt, wordt een samenvattingsaantal getoond voor elk. |
| Uitsplitsing naar serie | U kunt desgewenst de visualisatie opsplitsen in filters, dimensies, dimensiepunten of datumbereiken. <br><br>- U kunt maximaal 10 regels tegelijk weergeven. Uitsplitsingen zijn beperkt tot één niveau.<br><br>- Wanneer u een dimensie sleept, worden de bovenste dimensie-items automatisch geselecteerd op basis van het geselecteerde datumbereik van het deelvenster.<br><br>- Als u datumbereiken wilt vergelijken, sleept u twee of meer datumbereiken naar het filter voor reeksindeling. |

### Standaardweergave

![De standaardweergave Mediagelijktijdige viewers.](assets/concurrent-viewers-default.png)


### Uitsplitsingsweergave van reeksen

![De Media Gelijktijdige Viewers de mening van de de opsplitsing van de Reeks die 7 van 10 dimensies, segmenten of datumwaaiers toont.](assets/concurrent-viewers-series-breakdown.png)

## Deelvensteruitvoer {#Output}

Het deelvenster Mediagelijktijdige viewers retourneert een regeldiagram en een samenvattingsnummer met gegevens voor de maximum- en/of minimale gelijktijdige viewers.  Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren.

U kunt het deelvenster op elk gewenst moment bewerken en opnieuw samenstellen door op het bewerkingspotlood in de rechterbovenhoek te klikken.

Als u reeksindeling hebt geselecteerd, worden een regel in het lijndiagram en een samenvattingsnummer voor elke regel weergegeven:

![De uitvoer van Mediagelijktijdige viewers.](assets/concurrent-viewers-output.png)

### Gegevensbron

De enige metrische waarde die in dit deelvenster kan worden gebruikt, zijn Gelijktijdige viewers:

| Metrisch | Beschrijving |
|---|---|
| Gelijktijdige viewers | Aantal unieke personen dat uw mediastream(s) op een bepaald tijdstip weergeeft, ongeacht het aantal sessies.<br><br>Dit is anders dan de Gelijktijdige viewer die rapporteert in de sectie Rapporten, waarin Gelijktijdige actieve sessies worden gebruikt.  Door unieke personen te gebruiken, worden ongewenste &#39;spikes&#39; verwijderd bij het weergeven van grenzen (waar sessies tegelijkertijd eindigen en beginnen). |

In deze weergave is geen tabel voor vrije vorm beschikbaar.  Als u de gegevensbron wilt weergeven, klikt u met de rechtermuisknop op het lijndiagram en downloadt u dit als een CSV-bestand.  Uitsplitsingen naar reeksen worden opgenomen.


![De uitvoeropties voor gelijktijdige viewers met &quot;Gegevens downloaden als CSV&quot; gemarkeerd.](assets/concurrent-viewers-download-csv.png)

## Veelgestelde vragen {#FAQ}

| Vraag | Antwoord |
|---|---|
| Waar is de tabel voor vrije vorm? Hoe kan ik de gegevensbron zien? | De tabel Freeform is niet beschikbaar in deze weergave.  U kunt de gegevensbron downloaden door met de rechtermuisknop op het lijndiagram te klikken en het CSV-bestand te downloaden. |
| Waarom veranderde mijn granulariteit? | Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau).  Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken.<br><br>Wanneer u van een groter datumbereik overschakelt op een kleiner datumbereik, wordt de granulariteit bijgewerkt naar het laagste detailniveau dat is toegestaan nadat het datumbereik is gewijzigd. Als u een hogere granulariteit wilt weergeven, bewerkt u het deelvenster en maakt u het opnieuw. |
| Hoe vergelijk ik namen van video&#39;s, filters, inhoudstypen, enzovoort? | Als u deze in één visualisatie wilt vergelijken, sleept u filters, dimensies of specifieke dimensiepunten in het filter voor de reeksafbraak.<br><br>De weergave is beperkt tot tien uitsplitsingen.  Als u meer dan 10 wilt weergeven, moet u meerdere deelvensters gebruiken. |
| Hoe vergelijk ik datumbereiken? | Om datumwaaiers in één enkele visualisatie te vergelijken, gebruik de reeksonderverdelingen door 2 of meer datumwaaiers te slepen.  Deze datumbereiken overschrijven het datumbereik van het deelvenster. |
| Hoe kan ik het visualisatietype wijzigen? | In dit deelvenster kunt u alleen de lijnen voor de tijdreeks visualiseren. |
| Kan ik anomaliedetectie uitvoeren? | Nee.  Anomaly-detectie is niet beschikbaar voor dit deelvenster. |
| Waarom unieke personen gebruiken in plaats van actieve sessies? | Door unieke personen te gebruiken, kunt u ongewenste spikes verwijderen bij het weergeven van de grenzen (waar de sessies tegelijkertijd eindigen en beginnen). |
| Wat betekent het om gelijktijdige kijkers bij hogere granulariteit dan minuut te hebben? | Met een granulariteit die groter is dan een minuut, zijn gelijktijdige viewers de som van unieke gelijktijdige viewers voor alle minuten binnen dat tijdbereik.  Gelijktijdige viewers op uurniveau zijn bijvoorbeeld de som van unieke gelijktijdige viewers voor alle minuten in het uur. |
| Geeft het deelvenster Werkruimte dezelfde informatie als het rapport Gelijktijdige viewers? | Nee.  In Analysis Workspace wordt onder Gelijktijdige viewers verstaan het aantal unieke personen dat uw mediastream op een bepaald tijdstip weergeeft, ongeacht het aantal sessies.<br><br>Dit is anders dan de Gelijktijdige viewer die rapporteert in de sectie Rapporten, waarin Gelijktijdige actieve sessies worden gebruikt.  Het gebruiken van unieke persoonrekeningen voor verwijdering van ongewenste pieken bij show grenzen-waar de zittingen en tezelfdertijd beëindigen en beginnen. |

<!-- For more information about Media Concurrent Viewers, visit [MA doc page]( https://url). -->
