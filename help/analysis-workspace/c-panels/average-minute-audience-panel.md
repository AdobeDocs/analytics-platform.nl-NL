---
title: Deelvenster Gemiddelde media - geluid
description: Het deelvenster Mediagemiddelde minuut in Analysis Workspace gebruiken en interpreteren.
feature: Panels
role: User, Admin
exl-id: c55b5534-a9a6-47f1-8b43-c8c0b8686c53
source-git-commit: e4d4ff530d28e692301ca0671e055a164b9f7035
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 0%

---

# Deelvenster Gemiddeld aantal minuten voor publiek

>[!NOTE]
>
>Het deelvenster Mediapubliek met een gemiddelde minuut is alleen beschikbaar voor klanten die de invoegtoepassing voor het streamen van media-verzamelingen voor Customer Journey Analytics hebben aangeschaft.
>
>Neem contact op met uw Adobe-verkoper of accountteam van de Adobe om de invoegtoepassing voor de verzameling van streaming media aan te schaffen.

In Analysis Workspace is het gemiddelde aantal minuten voor het publiek de tijd die nodig is om de mediastream weer te geven gedeeld door de duur van de inhoud of de totale selectie van de periode en de geselecteerde granulariteit.

Met het deelvenster Mediapubliek per minuut kunt u het gemiddelde verbruik van uw inhoud beter begrijpen door programma&#39;s van elke lengte of genre te vergelijken. U kunt bijvoorbeeld het gemiddelde verbruik begrijpen wanneer u een 30 minuten durende sitcom vergelijkt met een sportevenement van 3 uur.

Bovendien kunt u het deelvenster Mediagemiddelde aantal minuten publiek gebruiken om dit digitale gemiddelde minutenpubliek te vergelijken of toe te voegen aan lineaire gemiddelde tijdmetingen voor tv.

Het gemiddelde minieme deelvenster van het publiek van Media biedt de volgende voordelen ten opzichte van de metrische waarde Gemiddelde Minuut publiek:

* Ondersteunt aangepaste tijdsperioden

* Hiermee kunt u de classificatie van de tijdsduur bijwerken nadat de weergaven zijn verwerkt (als deze niet aanwezig was of moet worden gecorrigeerd)

  Als u dit deed toen het gebruiken van metrisch, zal het of niet bestaan (als de classificatie niet aanwezig was) of het zal verouderd zijn (als de classificatie aanwezig maar onjuist was).

## Het deelvenster Gemiddelde minuten voor publiek in Media openen

1. Ga in Analysis Workspace naar een rapportsuite met componenten die zijn ingeschakeld via de invoegtoepassing voor het streamen van media-verzamelingen.

1. Selecteer in de linkernavigatiebalk de optie **Deelvensters** pictogram.

   ![Pictogram Deelvensters in linkernav](assets/panels-icon.png)

1. Sleep de [!UICONTROL **Gemiddeld aantal minuten voor medium**] op het canvas in Analysis Workspace.

1. Om het paneel te vormen, ga verder met [Deelvensterinvoer](#panel-inputs).

## Deelvensterinvoer {#Input}

Met de invoerinstellingen die in deze sectie worden beschreven, kunt u het deelvenster Medium voor een gemiddeld aantal minuten publiek configureren.

1. Beginnen met het maken van een mediapomagina voor een publiek, zoals wordt beschreven in [Het deelvenster Gemiddelde minuten voor publiek in Media openen](#access-the-media-average-minute-audience-panel).

1. Configureer de volgende invoerinstellingen:

   | Instelling | Beschrijving |
   |---------|------------|
   | **Datumbereik van deelvenster** | Het standaarddatumbereik van het deelvenster is [!UICONTROL **Deze maand**]. U kunt de presentatie bewerken om één dag of meerdere maanden tegelijk weer te geven. <br></br> Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
   | [!UICONTROL **Een segment hier neerzetten (of een andere component)**] | Net als andere deelvensters worden met deze instelling de selecties gefilterd op basis van segmenten die u hebt gemaakt. Dit is een goede manier om naar specifieke platforms, levende stromen, of andere gemeenschappelijke media segmenten te kijken. |
   | [!UICONTROL **Metrisch berekenen voor**] | Kies of u het gemiddelde minipubliek voor een bepaald stuk inhoud wilt zien, of als u het gemiddelde minipubliek gedurende een aangepaste periode wilt zien:<ul><li>**Specifieke inhoud:** Dit is alleen beschikbaar als de duur is bijgewerkt met behulp van classificaties. Als de duur niet beschikbaar is, of als u het gemiddelde minipubliek voor een tijdreeks met veelvoudige stukken of inhoud zonder een specifieke toegewezen duur (zoals tijdens een levende stroom of een gebeurtenis) wilt bekijken, dan zou u moeten selecteren [!UICONTROL **Aangepaste tijdsperiode**]. (U kunt Duur instellen met Classificaties voor of na de verwerkingstijd.)</li><li>**Aangepaste tijdsperiode:** Dit is beschikbaar ongeacht of de duur beschikbaar wordt gesteld met behulp van classificaties.</li></ul> <p>Met deze instelling wijzigt u de workflow en de rapportuitvoer.</p> |

1. Doorgaan met [Specifieke inhoud](#specific-content) of [Aangepaste tijdsperiode](#custom-time-period), afhankelijk van de optie die u in het dialoogvenster [!UICONTROL **Metrisch berekenen voor**] vervolgkeuzelijst.

### Specifieke inhoud

1. Als u [!UICONTROL **Specifieke inhoud**] in de [!UICONTROL **Metrisch berekenen voor**] vervolgkeuzemenu wanneer [configureren, van deelvensterinvoer](#panel-inputs)geeft u de volgende configuratieopties op:

   | Instelling | Beschrijving |
   |---------|------------|
   | [!UICONTROL **Rapporteringsdimensie**] | Wanneer u specifieke inhoud kiest, kunt u de rapportoutput selecteren om of de videonaam of de gebieden van identiteitskaart van de inhoud te gebruiken om de inhoud en zijn bijbehorend gemiddeld minipubliek voor de geselecteerde tijdspanne te tonen. |
   | [!UICONTROL **Inhoud filteren op (optioneel)**] | Kies hoe u de specifieke inhoud wilt filteren, afhankelijk van de gewenste weergave of de structuur van de gegevens. <ul>[!UICONTROL **Tonen, seizoen, aflevering**]: Hiermee geeft u de beschikbare weergaven in de vervolgkeuzelijst weer, die u kunt filteren met een zoekopdracht (of door de weergavenaam vanuit de linkerkolom te slepen en neer te zetten). Je kunt je selectie daar beëindigen om alle seizoenen van je show te zien, of je kunt filteren op individuele seizoenen en dan op individuele afleveringen. Deze instelling geeft de gegevens voor deze shows, seizoenen of episodes voor de geselecteerde tijdsperiode weer.</li><li>[!UICONTROL **Aangepaste dimensie**]: Als uw shownaam onder een douaneafmeting is, kunt u het vinden of door in de afmeting (facultatieve) drop-down te zoeken of door het linkerkolomonderzoek te gebruiken. Het dimensie-item wordt automatisch gevuld op basis van die selectie en wordt behandeld als een aflevering.</li><li>[!UICONTROL **Geen**]: Hiermee geeft u alle namen van video&#39;s weer met gemiddelde minutenpublieksgegevens voor de selectie die u hebt gekozen. (Deze opties zijn standaard geselecteerd.)</li></ul> |

1. Doorgaan met [Geavanceerde instellingen voor specifieke inhoud](#specific-content-advanced-settings) geavanceerde instellingen configureren.

### Geavanceerde instellingen voor specifieke inhoud

1. Met [!UICONTROL **Specifieke inhoud**] geselecteerd in het dialoogvenster [!UICONTROL **Metrisch berekenen voor**] vervolgkeuzelijst, selecteert u [!UICONTROL **Geavanceerde instellingen tonen**] en geeft u vervolgens de volgende configuratieopties op:

   | Instelling | Beschrijving |
   |---------|------------|
   | Tabelinstellingen | Bij de standaardinstelling worden de berekeningswaarden in de tabel weergegeven. In deze tabel worden de teller en de noemer van het gemiddelde aantal minuten voor het publiek weergegeven als de voorafgaande kolommen in de tabel. Als u deze optie uitschakelt, worden deze twee kolommen verwijderd. Alleen het gemiddelde aantal minuten voor het publiek blijft staan naast de naam van de video of de inhoud-id. |
   | Tijd besteed metrisch | U kunt de doorgebrachte standaardinhoudstijd kiezen, die alleen inhoudstijd omvat, of u kunt ervoor kiezen om de doorgebrachte media tijd te gebruiken, die inhoud en tijd bij elkaar als tellerberekening voor het gemiddelde minipubliek omvat. |

1. Selecteren [!UICONTROL **Opbouwen**] om het mediapictogram voor het publiek per minuut te maken.

1. Doorgaan met [Deelvensteruitvoer](#panel-output) voor informatie over het gebruik van het deelvenster Medium voor een gemiddeld aantal minuten publiek.

### Aangepaste tijdsperiode

1. Als u [!UICONTROL **Aangepaste tijdsperiode**] in de [!UICONTROL **Metrisch berekenen voor**] vervolgkeuzemenu wanneer [configureren, van deelvensterinvoer](#panel-inputs)geeft u de volgende configuratieopties op:

   | Instelling | Beschrijving |
   |---------|------------|
   | Granulariteit | De standaardgranulariteit is [!UICONTROL **5 minuten**], maar u kunt een van de granulariteiten kiezen die worden gebruikt als noemer voor de tijdreeks binnen de totale tijdsperiode die u hebt geselecteerd in de kalenderselectie. Als u bijvoorbeeld 12:00 tot 12:30 pm met een granulariteit van 5 minuten selecteert, wordt het gemiddelde aantal minuten voor het hele half uur en zes rijen geretourneerd met het gemiddelde aantal minuten voor elke periode van 5 minuten. Deze rijen worden gebruikt als datapoints voor de grafiek van de tijdreeks. |
   | [!UICONTROL **Inhoud filteren op (optioneel)**] | Kies hoe u de specifieke inhoud wilt filteren, afhankelijk van de gewenste weergave of de structuur van de gegevens. <ul>[!UICONTROL **Tonen, seizoen, aflevering**]: Hiermee geeft u de beschikbare weergaven in de vervolgkeuzelijst weer, die u kunt filteren met een zoekopdracht (of door de weergavenaam vanuit de linkerkolom te slepen en neer te zetten). Je kunt je selectie daar beëindigen om alle seizoenen van je show te zien, of je kunt filteren op individuele seizoenen en dan op individuele afleveringen. Deze instelling geeft de gegevens voor deze shows, seizoenen of episodes voor de geselecteerde tijdsperiode weer.</li><li>[!UICONTROL **Aangepaste dimensie**]: Als uw shownaam onder een douaneafmeting is, kunt u het vinden of door in de afmeting (facultatieve) drop-down te zoeken of door het linkerkolomonderzoek te gebruiken. Het dimensie-item wordt automatisch gevuld op basis van die selectie en wordt behandeld als een aflevering.</li><li>[!UICONTROL **Geen**]: Hiermee geeft u alle namen van video&#39;s weer met gemiddelde minutenpublieksgegevens voor de selectie die u hebt gekozen. (Deze opties zijn standaard geselecteerd.)</li></ul> |

1. Doorgaan met [Geavanceerde instellingen voor aangepaste tijdsperiode](#custom-time-period-advanced-settings) geavanceerde instellingen configureren.

### Geavanceerde instellingen voor aangepaste tijdsperiode

1. Met [!UICONTROL **Aangepaste tijdsperiode**] geselecteerd in het dialoogvenster [!UICONTROL **Metrisch berekenen voor**] vervolgkeuzelijst, selecteert u [!UICONTROL **Geavanceerde instellingen tonen**] en geeft u vervolgens de volgende configuratieoptie op:

   | Instelling | Beschrijving |
   |---------|------------|
   | Tabelinstellingen | Met de standaardinstelling worden de berekeningswaarden in de tabel weergegeven. In deze tabel worden de teller en de noemer van het gemiddelde aantal minuten voor het publiek weergegeven als de voorafgaande kolommen in de tabel. Als u deze optie uitschakelt, worden deze twee kolommen verwijderd, zodat alleen het gemiddelde aantal minuten naast de tijdsperiode overblijft. |

1. Selecteren [!UICONTROL **Opbouwen**] om het mediapictogram voor het publiek per minuut te maken.

1. Doorgaan met [Deelvensteruitvoer](#panel-output) voor informatie over het gebruik van het deelvenster Medium voor een gemiddeld aantal minuten publiek.

## Deelvensteruitvoer

De uitvoer van het deelvenster is afhankelijk van de keuze [!UICONTROL **Specifieke inhoud**] of [!UICONTROL **Aangepaste tijdsperiode**] in de [!UICONTROL **Metrisch berekenen voor**] vervolgkeuzemenu wanneer [configureren, van deelvensterinvoer](#panel-inputs).

### Specifieke inhoud

In het deelvenster Gemiddelde minieme publiek voor Media wordt het volgende geretourneerd:

* Totaal gemiddeld aantal minuten voor uw volledige selectie
* Filters en een gemiddeld aantal minuten voor de afzonderlijke video&#39;s die in een tabel worden weergegeven
* De tijd van de inhoud en videolengte (duur) als die geavanceerde het plaatsen werd geselecteerd

Als u het deelvenster op elk gewenst moment wilt bewerken en opnieuw wilt samenstellen, selecteert u het pictogram Bewerken (potlood) in de rechterbovenhoek.

![Standaardweergave](assets/specific-content-panel-output.png)

### Specifieke inhoudsgegevensbron

In het deelvenster Gemiddelde minieme doelgroep van Media wordt alleen de metrische waarde Gemiddelde minutenpubliek gebruikt om gegevens te verzamelen. In het deelvenster kunnen geen indelingen of andere maatstaven worden gebruikt.

| Metrisch | Beschrijving |
|--------|-------------|
| Gemiddeld aantal minuten publiek | De weergavetijd van de mediastream gedeeld door de videolengte (duur) die via Classificaties wordt aangeboden. |

### Aangepaste tijdsperiode {#custom-time-period-output}

In het deelvenster Gemiddelde minieme publiek voor Media wordt het volgende geretourneerd:

* Het totale gemiddelde aantal minuten voor uw volledige selectie

* Het maximum en minimum gemiddelde aantal minuten

* De grafiek van de lijnreeks die het gemiddelde minieme publiek over de volledige selectie toont.

* Een tabel waarin de filters en het gemiddelde aantal minuten voor de granulariteiten worden weergegeven, evenals de tijd die de inhoud heeft doorgebracht en de granulariteit voor elke tijdsperiode

  Deze tabel wordt alleen weergegeven als de optie onder geavanceerde instellingen wordt aangeroepen [!UICONTROL **Berekening weergeven in tabel**] is geselecteerd.

Als u het deelvenster op elk gewenst moment wilt bewerken en opnieuw wilt samenstellen, selecteert u het pictogram Bewerken (potlood) in de rechterbovenhoek.

![gelijktijdige viewer-uitvoer](assets/custom-time-period-panel-output.png)

### Gegevensbron aangepaste tijdperiode

In het deelvenster Gemiddelde minieme doelgroep van Media wordt alleen de metrische waarde Gemiddelde minutenpubliek gebruikt om gegevens te verzamelen. In het deelvenster kunnen geen indelingen of andere maatstaven worden gebruikt.

| Metrisch | Beschrijving |
|---|---|
| Gemiddeld aantal minuten publiek | De weergavetijd van de mediastream gedeeld door de totale selectie of geselecteerde granulariteit in minuten. |
