---
title: Invoer en uitvoer van het deelvenster Media Playback Time Spelling
description: Wat zijn de instellingen voor invoer en uitvoer van de afspeeltijd van media?
feature: Panels
role: User, Admin
exl-id: 8130e870-9ea6-4f1c-b434-0cbe135e8b68
source-git-commit: a9ba9def94a2f156f6d2d8e59c0155a492c3978c
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Invoer en uitvoer van deelvenster Media afspeeltijd {#Inputs-and-outputs}

U kunt het deelvenster Tijd voor afspelen van media aanpassen met de volgende invoer- en uitvoerinstellingen.

## Deelvensterinvoer {#Input}

U kunt het deelvenster Tijd voor afspelen van media configureren met de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---|---|
| Datumbereik van deelvenster | Het standaarddatumbereik van het deelvenster is Vandaag. U kunt de presentatie bewerken om een enkele dag of maanden tegelijk weer te geven.<br>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Granulariteit | De standaardwaarde voor granulariteit is Minute.<br>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Samenvattingsnummers deelvenster | Er is een samenvattingsnummer beschikbaar om datum- of tijdgegevens voor de afspeeltijd te zien. Bij Maximaal worden details voor de piekfrequentie weergegeven. Bij Minimum worden details voor de dal weergegeven. De som verhoogt de totale playbacktijd die voor de selectie wordt doorgebracht. De paneelstandaard toont slechts Maximum, maar u kunt het veranderen om Minimum, Som, of om het even welke combinatie drie te tonen.<br>Als u onderverdelingen gebruikt, wordt een samenvattingsaantal getoond voor elk. |
| Uitsplitsing naar serie | U kunt desgewenst de visualisatie opsplitsen in segmenten, dimensies, dimensiepunten of datumbereiken.<p>- U kunt maximaal 10 regels tegelijk weergeven. Uitsplitsingen zijn beperkt tot één niveau.</p><p>- Wanneer u een dimensie sleept, worden de bovenste dimensie-items automatisch geselecteerd op basis van het geselecteerde datumbereik van het deelvenster.</p>- Als u datumbereiken wilt vergelijken, sleept u twee of meer datumbereiken naar het filter voor reeksindeling. |
| Tijdnotatie | U kunt de afspeeltijd in een van beide uren weergeven:Minutes:Seconden (standaardwaarde) of in minuten (die in gehele getallen wordt weergegeven, naar boven afgerond op 0,5). |
| Weergave datumvolgorde | Als u ten minste twee segmenten van het datumbereik als reeksonderverdelingen hebt geplaatst, ziet u de optie om een overlay (standaard) of een sequentiële overlay te selecteren. Met overlay worden de lijnen weergegeven met een gemeenschappelijke beginpunt op de x-as, zodat deze parallel lopen, terwijl bij sequentieel de lijnen met hun specifieke beginpunt op de x-as worden weergegeven. Als de gegevenslijnen omhoog (bijvoorbeeld, eind segment 1 bij 8:44 pm en segment 2 begint bij 8:45 pm), dan zullen de lijnen in opeenvolging tonen. |

### Standaardweergave

![Standaardweergave](../assets/mpts_default_view.png)

## Deelvensteruitvoer {#Output}

In het deelvenster Afspeeltijd van media worden een regeldiagram en samenvattingsnummers geretourneerd met gegevens over de maximale, minimale en/of totale afspeeltijd. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren.

U kunt het deelvenster op elk gewenst moment bewerken en opnieuw samenstellen door op het bewerkingspotlood in de rechterbovenhoek te klikken.

Als u reeksindeling hebt geselecteerd, worden een regel in het lijndiagram en een samenvattingsnummer voor elke regel weergegeven:

![media playback tijd bestede output](../assets/mpts_outputs1.png)

### Gegevensbron

De enige metrische waarde die in dit deelvenster kan worden gebruikt, is Afspeeltijd.

| Metrisch | Beschrijving |
|---|---|
| Afspeeltijd besteed | Totaal aantal uren:minutes:seconden (of minuten) van de inhoud die tijdens de geselecteerde granulariteit wordt weergegeven, inclusief pauze, buffer en begintijd. |
