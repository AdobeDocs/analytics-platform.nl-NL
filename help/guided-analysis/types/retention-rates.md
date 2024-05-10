---
title: Bewaarpercentages
description: Meet hoeveel gebruikers uw product blijven gebruiken.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: c35a0ee0-e6b7-47b5-a5bc-308cde1585de
role: User
source-git-commit: 2b8afe1dbac5057f867437e2bfce27f3bd752d57
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Bewaarpercentages

De **[!UICONTROL Retention rates]** in deze weergave kunnen gebruikers het gebruik van uw product in de loop der tijd herhalen, zodat u beter kunt begrijpen wat de geschiktheid van de productmarkt is. In deze weergave geeft de horizontale as het aantal dagen weer dat is verstreken sinds de eerste betrokkenheid van een gebruiker en geeft de verticale as het percentage weer van de gebruikers die zich opnieuw engageren.

Deze analyse telt gebruikers op twee belangrijke gebeurtenissen worden gebaseerd die:

* De gebeurtenis van het begin: De eerste keer een gebruiker die met de gebeurtenis binnen de datumwaaier in dienst neemt
* Retourgebeurtenis: de meest recente keer dat een gebruiker zich met de gebeurtenis heeft beziggehouden binnen het geanalyseerde datumbereik

Het emmertje voor de duur &quot;Dag 0&quot; vertegenwoordigt de eerste tijd dat een gebruiker zich met de gebeurtenis heeft beziggehouden en is altijd precies gelijk aan 100%. Dit emmertje is de noemer die wordt gebruikt om het percentage van behouden gebruikers te berekenen.

De volgende tijdsemmers tellen het aantal gebruikers die op of na die duur terugkwamen. Dit aantal is de teller die wordt gebruikt om het percentage van behouden gebruikers te berekenen.

* Als een gebruiker slechts eenmaal in het gewenste datumbereik (de initiële service) aan de gebeurtenis deelneemt, worden deze alleen weergegeven in het duursegment &quot;Dag 0&quot;.
* Als een gebruiker meerdere dagen na de eerste keer in aanmerking komt voor opname in de analyse, worden deze dagen weergegeven in het meest recente kwalificatieduur en in alle tijdssegmenten vóór de gebeurtenis. Dit type berekening wordt soms &quot;niet-begrensde retentie&quot; genoemd. U kunt deze berekening-instelling wijzigen in de querytrack.

Gebruikers die in aanmerking komen voor tijdsemmers, zijn gebaseerd op verstreken tijd, niet op kalenderdag. Bijvoorbeeld, als een gebruiker voor een gebeurtenis om 11:55 PM op 6 September kwalificeert, dan voor een terugkeergebeurtenis om 12:05 AM op 7 September in aanmerking komt, zouden zij niet in het 1 dagduuremmertje verschijnen. Er moet een volledige periode van 24 uur verstrijken voordat de gebruiker in aanmerking komt voor het tijdsinterval van 1 dag.

![Schermafbeelding met retentiesnelheden](../assets/retention-rates.png){style="border:1px solid gray"}

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Cohortanalyse**: Groepeer gebruikers in cohorten op basis van handelingen die ze uitvoeren, zoals aanmelden of aankopen. U kunt vergelijken hoe goed deze groepen behouden en bepalen hoe te om de gebruikerservaring van elke groep te verbeteren.
* **Geschiktheid van de productmarkt**: Meet het regelmatige gebruik van uw product en visualiseer het als retentiecurven. Grotere retentie betekent een grotere geschiktheid voor de productmarkt en wanneer de curve wordt afgevlakt, geeft dit aan hoe lang het duurt om uw pasvorm te bereiken. Bekijk deze analyse op een algemeen niveau of uitsplitsing naar afzonderlijke productkenmerken om dieper inzicht te krijgen.
* **Abonnementsserviceanalyse**: Als uw product een abonnement of een ander type terugkerende inkomstenmodel gebruikt, kunt u het percentage zien van gebruikers die het meeste van uw product maken. U kunt bepaalde kwaliteiten en gedragingen identificeren die deze gebruikers vertonen.
* **Gebruikersbetrokkenheid**: Evalueer hoe bepaalde typen gebruikers met uw product werken en vergelijk naast elkaar hoe vaak ze retourneren. Een bepaald segment met een lagere retentie dan anderen kan u inzicht verschaffen in het verbeteren van mogelijke ondermaatse ervaringen die zij kunnen hebben.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Start event]**: De gebeurteniscriteria waarmee een gebruiker moet werken om in aanmerking te komen voor opname in uw analyse. Gebruikers die de gebeurtenis start starten, worden opgenomen in het eerste segment met gebruikers dat in totaal 100% bedraagt. Eén gebeurtenis wordt ondersteund, maar u kunt eigenschapfilters opnemen. U kunt de start- en retourgebeurtenissen aan elkaar koppelen met het menu met drie punten. Door de start- en retourgebeurtenissen aan elkaar te koppelen, zijn de criteria voor het eerste tijdsinterval en de daaropvolgende tijdsduur van de emmers hetzelfde.
* **[!UICONTROL Return events]**: De gebeurteniscriteria waarmee een gebruiker moet werken om in aanmerking te komen voor opname in volgende tijdssegmenten. U kunt maximaal drie retourgebeurtenissen selecteren. Elke terugkeergebeurtenis produceert een zij-aan-zij analyse met andere inbegrepen terugkeergebeurtenissen.
* **[!UICONTROL Counted as]**: De telmethode die u wilt toepassen op bewaarde gebruikers. U kunt onder andere de volgende opties kiezen:
   * **[!UICONTROL Metric]**: Tel het aantal van [!UICONTROL Users retained] of de [!UICONTROL Percentage of users retained].
   * **[!UICONTROL Returning]**: Standaard bevat deze analyse gebruikers in het emmertje dat ze hebben geretourneerd en alle voorafgaande emmers. Deze instelling wijzigen in **[!UICONTROL On exactly]** om gebruikers alleen op te nemen in het exacte emmer waarvoor zij in aanmerking komen.
   * **[!UICONTROL Each]**: De tijdsperiode die u wilt gebruiken voor elk tijdssegment. Deze instelling is identiek aan de instelling **[!UICONTROL Interval]** instellen wanneer u het datumbereik selecteert.
   * **[!UICONTROL Duration settings]**: Hiermee kunt u bepalen hoe gebruikers in de analyse worden weergegeven op basis van het aantal verstreken dagen. De beschikbare tijdsemmers zijn afhankelijk van het datumbereik dat u instelt. **[!UICONTROL Auto durations]** stelt automatisch tijdsemmers in op basis van de lengte van het datumbereik en de nabijheid van de huidige dag waarop het datumbereik zich bevindt. **[!UICONTROL Custom durations]** kunt u vier tijdsemmers met de gewenste intervallen handmatig instellen.
* **[!UICONTROL Segments]**: De segmenten die u wilt meten. Elk geselecteerd segment voegt een rij toe aan de cohortingtabel. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De [!UICONTROL Retention rates] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Bar] en [!UICONTROL Line]. De lijnvisualisatie toont visueel Dag 0 in de grafiek.

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarmee u de retentiegegevens wilt weergeven. Mogelijke geldige opties zijn Dagelijks, Wekelijks en Maandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben, die van invloed zijn op de opties voor de tijdsduur van een emmertje.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

Als u een datumbereik selecteert dat dicht bij de huidige dag ligt, worden gebruikers die aanvankelijk te dicht bij de huidige dag komen, niet opgenomen. Deze analyse geeft altijd alle gebruikers de kans om in alle periodeemmers worden opgenomen. Een bericht onder de kalenderkiezer verstrekt informatie over de datumwaaier waar de gebruikers, en het interval ingaan dat slechts voor terugkerende gebruikers wordt gereserveerd:

* **[!UICONTROL Analyzing users who did the start event in [Date interval]]**: Als een gebruiker binnen dit datumbereik met de gebeurtenis werkt, worden deze opgenomen in de analyse. Dit datumbereik garandeert alle gebruikers voldoende tijd om in aanmerking te komen voor alle tijdssegmenten. Dit datumbereik kan anders zijn dan de datum die u hebt geselecteerd als deze dicht bij de huidige dag ligt.
* **[!UICONTROL Data from [Date interval] is reserved to complete the analysis]**: Als een gebruiker zich voor de eerste keer binnen deze periode aansluit, worden de volgende **niet** opgenomen in de analyse. Voor recente datumbereiken zouden deze gebruikers niet in de gelegenheid zijn om voor alle tijdssegmenten in aanmerking te komen. Voor datumbereiken in het verleden waren deze gebruikers actief buiten het geselecteerde datumbereik.

## Cohortingtabel

De tabel onder het diagram biedt een geaggregeerde weergave (vergelijkbaar met diagramgegevens) en een volledige cohortingtabel. De volledige cohortingtabel bevat gegevens over elk datuminterval en het tijdstip waarop gebruikers betrokken zijn.
