---
title: Betrokkenheidsanalyse
description: Begrijp de breedte en diepte van eigenschapbetrokkenheid.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
role: User
exl-id: 8a48ad3b-fa30-497e-8306-f8d881b1a335
source-git-commit: d492220eaf12242a870f3826b31edd3d1ea99a3b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# [!UICONTROL Engagement] analyse {#engagement}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_workspace_guidedanalysis_engagement_button"
>title="Beheer"
>abstract="Begrijp de breedte en diepte van eigenschapbetrokkenheid."

<!-- markdownlint-enable MD034 -->


De ](/help/assets/icons/EngagementGraph.svg) **[!UICONTROL Engagement]** analyse 0} EngagementGraph verstrekt inzicht in hoe vaak een eigenschap tegenover hoeveel mensen het gebruikt wordt. ![ Deze analyse werkt het best wanneer het vergelijken van verscheidene eigenschappen aan elkaar. Het helpt investeringsbeslissingen te voeden door te begrijpen wat uw kern, macht, eenmalig, en twijfelachtige eigenschappen zijn.

De eigenschappen die naar de bovenkant van deze visualisatie trekken wijzen erop dat zij vaak onder betrokken gebruikers worden gebruikt. De eigenschappen die naar het recht van deze visualisatie trekken wijzen erop dat zij wijd onder uw actieve gebruikers worden geadopteerd. Het gemiddelde aantal keren dat een functie wordt gebruikt, verdeelt de grafiek horizontaal. Het mediane percentage actieve gebruikers verdeelt de grafiek verticaal. Medianen worden berekend op basis van de gebeurtenissen die in de query zijn geselecteerd, niet alle gegevens.

* De eigenschappen in top-left van de matrijs zijn uw **macht** eigenschappen; zij worden niet wijd goedgekeurd, maar vaak gebruikt door betrokken gebruikers.
* De eigenschappen in het hoogste recht van de matrijs zijn uw **hoge gevolgen** eigenschappen; zij worden zowel wijd goedgekeurd als vaak gebruikt.
* De eigenschappen in de bodem-linkerzijde van de matrijs zijn uw **lage gevolgen** eigenschappen; zij worden niet wijd goedgekeurd of vaak gebruikt.
* De eigenschappen in het bodem-recht van de matrijs zijn uw **eenmalig** eigenschappen; zij worden wijd goedgekeurd, maar niet vaak gebruikt.

>[!VIDEO](https://video.tv.adobe.com/v/3429489/&learn=on)


## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **Betrokkenheid door eigenschap**: U kunt een directe correlatie tussen overeenkomst en goedkeuring van een specifieke eigenschap vestigen. Begrijpen welke eigenschappen het meest worden gebruikt kan helpen bepalen welke eigenschappen om in verder te investeren.
* **ontdekt ondergebruikte eigenschappen**: De eigenschappen met laag actieve gebruikers maar het hoge gebruik kunnen op een machtseigenschap wijzen, die waardevol maar niet ontdekt of gebruikt door de bredere bevolking is. U kunt overwegen de ontdekkingsmogelijkheden van deze functies te verbeteren, zodat meer gebruikers deze kunnen benutten.
* **verbeter populaire eigenschappen**: De eigenschappen met hoge actieve gebruikers maar het lage gebruik kan erop wijzen dat een eigenschap hoogst gevraagd maar ondergebruikt is. Deze situaties bieden mogelijkheden om meer van uw gebruikers te leren over welke verbeteringen de eigenschap voor hen waardevoller zouden maken.
* **creeer op eigenschap-gebaseerde segmenten**: Het bekijken eigenschapgebruik op deze manier om extra analysekansen te veroorzaken. Maak een segment voor elk punt in het diagram om verder in die gebruikersgroep te duiken en pas die lessen toe op uw strategie voor de gebruikersbetrokkenheid.
* **de goedkeuring A/B van de Eigenschap het testen**: Vergelijk het gebruik van veelvoudige eigenschappen over verschillende groepen gebruikers. Voeg segmenten in de vraagrail toe om het verschil in eigenschapgebruik over zeer belangrijke gebruikersgroepen te bepalen.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Events]**: De gebeurtenissen die u wilt meten. Elke gebeurtenis vertegenwoordigt het gebruik van een bepaalde functie en wordt weergegeven als een punt binnen de matrix. U kunt maximaal tien gebeurtenissen opnemen. De mediaan wordt berekend op basis van de geselecteerde gebeurtenissen.
* **[!UICONTROL Counted as]**: langs de x-as, kunt u het gemiddelde percentage van dagelijkse, wekelijkse, maandelijkse, of driemaandelijkse actieve gebruikers meten. Op de y-as worden de gemiddelde tijden per gebruiker automatisch aangepast op basis van de selectie van de x-as.
* **[!UICONTROL Segments]**: De segmenten die u wilt meten. Elk geselecteerd segment verdubbelt het aantal getekende punten in het diagram en de rijen in de tabel. U kunt maximaal drie segmenten opnemen.

>[!TIP]
>
>Als meerdere gebeurtenissen het gebruik van één functie vertegenwoordigen, kunt u een nieuwe gebeurtenis afleiden die de functie in Gegevens vertegenwoordigt.

### Diagraminstellingen

De [!UICONTROL Engagement] -analyse biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Medians]**: Bepaal waar de mediaanlijnen worden weergegeven en hoe de uitgezette punten zich verhouden tot die medianen.
   * **[!UICONTROL Standard]**: geef de absolute waarde van het gebruik en de betrokkenheid weer.
   * **[!UICONTROL Normalized]**: relatieve wijzigingen ten opzichte van elke mediaan tonen.
* **[!UICONTROL Top events overlay]**: Zie hoe uw gebeurtenissen bezig zijn in vergelijking met de top 20 van gebeurtenissen, op basis van recentie en relevantie van bedrijf en gebruiker (hetzelfde algoritme dat wordt toegepast op de gebeurteniskiezer in de querytrack).

### Tijdvergelijking

{{apply-time-comparison}}

### Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u trendgegevens wilt weergeven. Bij deze analyse wordt [!UICONTROL Interval] op dezelfde manier behandeld als [!UICONTROL Counted as] in de querytrack. Uuractieve gebruikers worden niet ondersteund.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

<!--
## Example

See below for an example of the analysis.

![Enagement compare](../assets/engagement-compare.png)
-->
