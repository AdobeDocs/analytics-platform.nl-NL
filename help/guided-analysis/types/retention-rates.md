---
title: Bewaarpercentages
description: Meet hoeveel gebruikers uw product blijven gebruiken.
feature: Guided Analysis
keywords: productanalyse
source-git-commit: 74525c4ce9ad1fd3f3abf35a9d9cb2c521d23874
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 0%

---

# Bewaarpercentages

De **[!UICONTROL Retention rates]** toont het percentage gebruikers dat na hun eerste betrokkenheid binnen het gewenste datumbereik terugkeert. De horizontale as geeft het aantal dagen weer sinds de eerste betrokkenheid van een gebruiker. De verticale as geeft het percentage weer van de gebruikers die zich opnieuw engageren.

Deze analyse telt gebruikers op twee belangrijke gebeurtenissen worden gebaseerd die:

* De eerste keer dat een gebruiker de gebeurtenis binnen het datumbereik heeft gebruikt
* De meest recente tijd dat een gebruiker de gebeurtenis binnen het geanalyseerde datumbereik heeft gebruikt

Het emmertje voor de duur &quot;dag 0&quot; vertegenwoordigt de eerste keer dat een gebruiker zich met de gebeurtenis begeeft en is altijd precies gelijk aan 100%. De hoeveelheid tijd die verstrijkt tussen de initiële service en de retourservice bepaalt waar de gebruiker onder staat.

* Als een gebruiker slechts eenmaal in het gewenste datumbereik (de initiële service) aan de gebeurtenis deelneemt, worden deze alleen weergegeven in het duursegment &quot;dag 0&quot;.
* Als een gebruiker meerdere dagen na de eerste keer in aanmerking komt voor opname in de analyse, worden deze dagen weergegeven in het meest recente kwalificatieduur en in alle tijdssegmenten vóór de gebeurtenis.
* Als een gebruiker gedurende het geconfigureerde datumbereik meerdere keren met de gebeurtenis werkt, worden alleen de eerste en laatste gebeurtenissen in de analyse opgenomen.

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Cohortanalyse**: Groepeer gebruikers in cohorten op basis van gebeurtenissen zoals aanmeldingen of aankopen. U kunt de kleverigheid van deze groepen vergelijken en bepalen hoe u de gebruikerservaring van die groep kunt verbeteren.
* **Abonnementsserviceanalyse**: Als uw product een abonnement of een ander type terugkerende inkomstenmodel gebruikt, kunt u het percentage zien van gebruikers die het meeste van uw product maken. Degenen die uw product of service niet gebruiken, zullen waarschijnlijk liever naar huis gaan, zodat u deze gebruikers kunt identificeren en hierop kunt concentreren.
* **Gebruikersbetrokkenheid**: Evalueer hoe bepaalde typen gebruikers met uw product werken en vergelijk naast elkaar hoe vaak ze retourneren. Een bepaald segment met een steile retentiecurve dan anderen u van inzicht kunnen voorzien rond het verbeteren van potentiële subpar ervaringen die zij zouden kunnen hebben.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Start & return event]**: De gebeurteniscriteria waarmee een gebruiker moet werken om in aanmerking te komen voor opname in uw analyse. Eén gebeurtenis wordt ondersteund, maar u kunt eigenschapfilters opnemen.
* **[!UICONTROL People]**: De segmenten die u wilt meten. Elk geselecteerd segment voegt een rij toe aan de cohortingtabel. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De [!UICONTROL Retention rates] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Metric]**: Hoe wilt u meten welke gebruikers behouden zijn? Opties omvatten [!UICONTROL Users retained] en [!UICONTROL Percentage of users retained].
* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Bar] en [!UICONTROL Line].

## Duur-instellingen

Hiermee kunt u bepalen hoe gebruikers in de analyse worden weergegeven op basis van het aantal verstreken dagen.

* **[!UICONTROL Auto durations]**: Stel de tijdsduur automatisch in op basis van de lengte van het datumbereik en de nabijheid van de huidige dag waarop het datumbereik zich bevindt.
* **[!UICONTROL Custom durations]**: Stel handmatig de gewenste verstreken dagen in. U kunt vier tijdsduur instellen.

U kunt geen duur instellen die langer is dan de tijd die een gebruiker nodig heeft om een gebeurtenis uit te voeren en die in aanmerking komt voor het laatste tijdssegment voordat de huidige dag wordt bereikt. Als de huidige datum bijvoorbeeld 30 september is en uw geconfigureerde datumbereik 1 september tot en met 30 september, is de maximale duur voor dit datumbereik 14 dagen.

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum die u retentiegegevens wilt weergeven. Mogelijke geldige opties zijn Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben, wat invloed heeft op automatisch ingestelde duurdagen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

Als u een datumbereik selecteert dat dicht bij de huidige dag ligt, worden gebruikers die aanvankelijk te dicht bij de huidige dag komen, niet opgenomen. Deze analyse geeft altijd alle gebruikers de kans om in alle periodeemmers worden opgenomen. Een bericht onder de kalenderkiezer verstrekt informatie rond de datumwaaier waar de gebruikers, en het interval ingaan dat slechts voor terugkerende gebruikers wordt gereserveerd:

* **De eerste analyseren [Datuminterval] van de cohort [Datumbereik]**: Als een gebruiker binnen dit datumbereik met de gebeurtenis werkt, worden deze opgenomen in de analyse. Dit datumbereik garandeert alle gebruikers voldoende tijd om in aanmerking te komen voor alle tijdssegmenten. Dit datumbereik kan anders zijn dan de datum die u hebt geselecteerd als deze dicht bij de huidige dag ligt.
* **De definitieve [Datuminterval] alleen de analyse kan voltooien**: Als een gebruiker voor de eerste keer binnen dit interval met de gebeurtenis werkt, zijn de volgende **niet** opgenomen in de analyse. De gebruikers die aanvankelijk met de gebeurtenis binnen dit interval in werking stellen zouden geen kans hebben om voor alle duuremmers in aanmerking te komen, of zijn buiten de gewenste datumwaaier.

## Cohortingtabel

De tabel onder het diagram biedt een geaggregeerde weergave (vergelijkbaar met diagramgegevens) en een volledige cohortingtabel. De volledige cohortingtabel bevat details over elk datuminterval en wanneer gebruikers betrokken zijn.
