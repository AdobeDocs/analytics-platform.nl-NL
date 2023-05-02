---
title: Deelvenster Gemiddelde media - geluid
description: Het deelvenster Mediagemiddelde - Minuut publiek in Analysis Workspace gebruiken en interpreteren.
feature: Panels
role: User, Admin
exl-id: be8371ee-8bc6-4a99-8527-dd94eab8a7f9
source-git-commit: 32c507cb9de4fcd146de0e9c828c54c5f4f1a062
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 1%

---


# Deelvenster Gemiddelde media - geluid

<!-- THIS FEATURE IS SCHEDULED FOR 2023 -->

Klanten van Media Analytics kunnen het gemiddelde minieme publiek deelvenster gebruiken om het gemiddelde verbruik van hun inhoud beter te begrijpen. Het gemiddelde minutenpubliek maakt vergelijkingen van programmering van om het even welke lengte of genre mogelijk. Bovendien kunnen klanten dit digitale gemiddelde minieme publiek vergelijken of toevoegen aan lineaire gemiddelde de minmetriek van TV. Dit deelvenster biedt meer flexibiliteit om het gemiddelde publiek voor aangepaste tijdsperiodes te meten en om te bepalen wanneer de classificatie van de duur na het feit is bijgewerkt. Het huidige gemiddelde minieme publiek metrisch werkt slechts als de duur bij verwerkingstijd beschikbaar is.

In Analysis Workspace is het gemiddelde aantal minuten voor het publiek de tijd die nodig is om de mediastream weer te geven gedeeld door de duur van de inhoud of de totale selectie van de periode en de geselecteerde granulariteit.

Het deelvenster Mediagemiddelde Minuut publiek biedt een analyse van het gemiddelde aantal minuten voor het publiek op basis van de specifieke inhoud die is geselecteerd als de duur beschikbaar wordt gesteld met behulp van classificaties.
Het deelvenster Gemiddelde minuten publiek biedt ook analyses over een geselecteerde tijdsperiode die door specifieke inhoud kunnen worden gefilterd, ongeacht of de duur beschikbaar is via classificaties. Als u het deelvenster Mediagemiddelde Minuut publiek wilt openen, navigeert u naar een rapportsuite met ingeschakelde componenten voor Media Analytics. Klik vervolgens op het deelvensterpictogram helemaal links en sleep het deelvenster naar uw Analysis Workspace-project.

<!-- For more information, see the Media Average Minute Audience introduction video:
<< replace with AMA video when available >> -->

<!-- >[!VIDEO](https://video.tv.adobe.com/v/330177/?quality=12) -->

## Deelvensterinvoer {#Input}

U kunt het deelvenster Medium Gemiddelde miniatuur publiek configureren met behulp van de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---------|------------|
| Datumbereik van deelvenster | Het standaarddatumbereik van het deelvenster is Vandaag. U kunt de presentatie bewerken om een enkele dag of maanden tegelijk weer te geven. <br></br> Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Sleep een segment hier naartoe (of een andere component) | Net als andere deelvensters worden met deze instelling de selecties gefilterd op basis van segmenten die u hebt gemaakt. Dit is een goede manier om naar specifieke platforms, levende stromen, of andere gemeenschappelijke media segmenten te kijken. |
| Metrisch berekenen voor | Met deze instelling kunt u kiezen of u het gemiddelde aantal minuten voor een bepaald gedeelte van de inhoud wilt weergeven door *specifieke inhoud* of als u het gemiddelde aantal minuten voor een bepaalde periode wilt zien, selecteert u *aangepaste tijdsperiode*. <br></br>Specifieke inhoud werkt alleen als de duur is bijgewerkt met behulp van classificaties. Als de duur niet beschikbaar is, of als u het gemiddelde minipubliek voor een tijdreeks met veelvoudige stukken van inhoud of inhoud zonder een specifieke toegewezen duur (zoals tijdens een levende stroom of een gebeurtenis) wilt bekijken, dan zou u de periode van de douanetijd moeten selecteren. Met deze instelling wijzigt u de workflow en de rapportuitvoer. |

### Specifieke inhoud

| Instelling | Beschrijving |
|---------|------------|
| Rapportagedimensies | Wanneer u specifieke inhoud kiest, kunt u de rapportoutput selecteren om of de videonaam of de gebieden van identiteitskaart van de inhoud te gebruiken om de inhoud en zijn bijbehorend gemiddeld minipubliek voor de geselecteerde tijdspanne te tonen. |
| Inhoud filteren op (optioneel) | U kunt de specifieke inhoud filteren op basis van de gewenste weergave of de structuur van de gegevens. |
| Tonen, seizoen, aflevering | Als u &#39;Tonen, seizoen, aflevering&#39; selecteert, worden uw beschikbare shows weergegeven in de vervolgkeuzelijst. U kunt deze opties filteren met een zoekopdracht (of door de weergavenaam vanuit de linkerkolom te slepen en neer te zetten). Je kunt je selectie daar beëindigen om alle seizoenen van je show te zien, of je kunt filteren op individuele seizoenen en dan op individuele afleveringen. Deze instelling geeft de gegevens voor deze shows, seizoenen of episodes voor de geselecteerde tijdsperiode weer. |
| Aangepaste dimensie | Als uw shownaam onder een douaneafmeting is, kunt u het vinden of door in de afmeting (facultatieve) daling te zoeken of door het linkerkolomonderzoek te gebruiken. Het dimensie-item wordt automatisch gevuld op basis van die selectie en wordt behandeld als een aflevering. |
| Geen | U kunt *Geen* om alle videonamen te tonen die gemiddelde minieme publieksgegevens voor de selectie hebben u gekozen. |

### Geavanceerde instellingen voor specifieke inhoud

| Instelling | Beschrijving |
|---------|------------|
| Tabelinstellingen | Bij de standaardinstelling worden de berekeningswaarden in de tabel weergegeven. In deze tabel worden de teller en de noemer van het gemiddelde aantal minuten voor het publiek weergegeven als de voorafgaande kolommen in de tabel. Als u deze optie uitschakelt, worden deze twee kolommen verwijderd. Alleen het gemiddelde aantal minuten voor het publiek blijft staan naast de naam van de video of de inhoud-id. |
| Tijd besteed metrisch | U kunt de doorgebrachte standaardinhoudstijd kiezen, die alleen inhoudstijd omvat, of u kunt ervoor kiezen om de doorgebrachte media tijd te gebruiken, die inhoud en tijd bij elkaar als tellerberekening voor het gemiddelde minipubliek omvat. |

### Aangepaste tijdsperiode

| Instelling | Beschrijving |
|---------|------------|
| Granulariteit | De standaardgranulariteit is 5 minuten, maar u kunt elk van de granulariteiten kiezen die worden gebruikt als noemer voor de tijdreeks binnen de totale tijdsperiode die is geselecteerd in de kalenderselectie. Als u bijvoorbeeld 12:00 tot 12:30 pm met een granulariteit van 5 minuten selecteert, wordt het gemiddelde aantal minuten voor het hele half uur en zes rijen met het gemiddelde aantal minuten voor elke periode van 5 minuten geretourneerd. Deze rijen worden gebruikt als datapoints voor de grafiek van de tijdreeks. |
| Inhoud filteren op (optioneel) | U kunt de specifieke inhoud filteren op basis van de gewenste weergave of de structuur van de gegevens. |
| Tonen, seizoen, aflevering | Selecteren *Tonen, seizoen, aflevering* geeft de beschikbare weergaven weer in de vervolgkeuzelijst, die u kunt filteren via een zoekopdracht (of door de weergavenaam vanuit de linkerkolom te slepen en neer te zetten). Je kunt je selectie daar beëindigen om alle seizoenen van je show te zien, of je kunt filteren op individuele seizoenen en dan op individuele afleveringen. Deze instelling geeft de gegevens voor deze shows, seizoenen of episodes voor de geselecteerde tijdsperiode weer. |
| Aangepaste dimensie | Als uw shownaam onder een douaneafmeting is, kunt u het vinden of door in de afmeting (facultatieve) daling te zoeken of door het linkerkolomonderzoek te gebruiken. Het dimensie-item wordt automatisch gevuld op basis van die selectie en wordt behandeld als een aflevering. |
| Geen | U kunt *Geen* om alle videonamen over de gekozen tijdsperiode te tonen. |

### Geavanceerde instellingen voor aangepaste tijdsperiode

| Instelling | Beschrijving |
|---------|------------|
| Tabelinstellingen | Met de standaardinstelling worden de berekeningswaarden in de tabel weergegeven. In deze tabel worden de teller en de noemer van het gemiddelde aantal minuten voor het publiek weergegeven als de voorafgaande kolommen in de tabel. Als u deze optie uitschakelt, worden deze twee kolommen verwijderd, zodat alleen het gemiddelde aantal minuten naast de tijdsperiode overblijft. |


## Uitvoer van deelvenster Specifieke inhoud

Het deelvenster Mediagemiddelde Minuut publiek retourneert het volgende:

* Totaal gemiddeld aantal minuten voor uw volledige selectie
* Filters en een gemiddeld aantal minuten voor de afzonderlijke video&#39;s die in een tabel worden weergegeven
* De tijd van de inhoud en videolengte (duur) als die geavanceerde het plaatsen werd geselecteerd

Als u het deelvenster op elk gewenst moment wilt bewerken en opnieuw wilt samenstellen, klikt u op het potlood aan de rechterbovenzijde.

![Standaardweergave](assets/specific-content-panel-output.png)


### Specifieke inhoudsgegevensbron

De enige metrische waarde die in dit paneel kan worden gebruikt is Gemiddeld Minuut publiek.

| Metrisch | Beschrijving |
|--------|-------------|
| Gemiddeld aantal minuten publiek | De weergavetijd van de mediastream gedeeld door de videolengte (duur) die via Classificaties wordt aangeboden. |

## Uitvoer deelvenster Aangepaste tijdsperiode {#custom-time-period-output}

Het deelvenster Mediagemiddelde Minuut publiek retourneert het totale gemiddelde aantal minuten voor de volledige selectie, het maximale en minimale gemiddelde aantal minuten voor het publiek en de grafiek van de lijnreeks die het gemiddelde aantal minuten voor het hele selectieproces weergeeft. In de onderstaande tabel worden de filters en het gemiddelde aantal minuten voor de granulariteiten weergegeven, evenals de tijd die de inhoud heeft doorgebracht en de granulariteit voor elke tijdsperiode als die geavanceerde instelling was geselecteerd.

Als u het deelvenster op elk gewenst moment wilt bewerken en opnieuw wilt samenstellen, klikt u op het potlood aan de rechterbovenzijde.

![gelijktijdige viewer-uitvoer](assets/custom-time-period-panel-output.png)

### Gegevensbron aangepaste tijdsperiode

De enige metrische waarde die in dit paneel kan worden gebruikt is Gemiddelde Minuut publiek:

| Metrisch | Beschrijving |
|---|---|
| Gemiddeld aantal minuten publiek | De weergavetijd van de mediastream gedeeld door de totale selectie of geselecteerde granulariteit in minuten. |



<!-- For more information about Media Average Minute Audience, visit [MA doc page]( https://url). -->
