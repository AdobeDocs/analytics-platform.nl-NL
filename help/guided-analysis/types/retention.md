---
title: Bewaaranalyse
description: Meet hoeveel gebruikers uw product blijven gebruiken.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: c35a0ee0-e6b7-47b5-a5bc-308cde1585de
role: User
source-git-commit: ad181b5ba3de1a038c661159a159d234da6c3edf
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 0%

---

# Bewaaranalyse

De ![ Behoud ](/help/assets/icons/Retention.svg) **[!UICONTROL Retention]** analyse meet hoe de gebruikers uw product in tijd blijven gebruiken, die u kan helpen uw productmarkt begrijpen geschikt. In de analyse worden gebruikers op basis van twee belangrijke gebeurtenissen beoordeeld:

* Startgebeurtenis: de gebeurtenis die wordt gebruikt om gebruikers in aanmerking te laten komen voor opname in uw analyse.
* Geretourneerde gebeurtenis: een of meer gebeurtenissen waarmee een gebruiker moet werken om als terugkerende gebruiker in uw analyse te tellen.

In deze analyse, vertegenwoordigt de x-as van de grafiek de tijd sinds de eerste begingebeurtenis van een gebruiker en y-as het percentage gebruikers die met één of meerdere terugkeergebeurtenissen in dienst nemen. U kunt zowel behoud als kromme over duur bekijken, en de getoonde duur kan door de vraagmontages worden aangepast. Onder de grafiek, verstrekt een lijst samengevoegde gegevens met de optie om individuele cohorts te tonen, die een groep mensen zijn die de beginnende gebeurtenis op de zelfde datum deden.

+++ Video demo

>[!VIDEO](https://video.tv.adobe.com/v/3430503/?learn=on)

+++

![ Behoud ](../assets/retention.png)

## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **analyse van de Cohort**: De gebruikers van de groep in cohorts die op acties worden gebaseerd die zij, zoals sign-ups of aankopen nemen. U kunt vergelijken hoe goed deze groepen behouden en bepalen hoe te om de gebruikerservaring van elke groep te verbeteren.
* **de marktpas van het Product** past: Meet regelmatig gebruik van uw product en visualiseer als behoudkrommen. Grotere retentie betekent een grotere geschiktheid voor de productmarkt en wanneer de curve wordt afgevlakt, geeft dit aan hoe lang het duurt om uw pasvorm te bereiken. Bekijk deze analyse op een algemeen niveau of uitsplitsing naar afzonderlijke productkenmerken om dieper inzicht te krijgen.
* **de dienstanalyse van het Abonnement**: Als uw product een abonnement of een ander type van het terugkomende opbrengstmodel aanwendt, kunt u het percentage gebruikers zien die het grootste deel van uw product maken. U kunt bepaalde kwaliteiten en gedragingen identificeren die deze gebruikers vertonen.
* **Overeenkomst van de Gebruiker**: Evalueer hoe bepaalde types van gebruikers met uw product in dienst nemen, en vergelijk zij naast elkaar hoe vaak zij terugkeren. Een bepaald segment met een lagere retentie dan anderen kan u inzicht verschaffen in het verbeteren van mogelijke ondermaatse ervaringen die zij kunnen hebben.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Start event]**: De gebeurteniscriteria waarmee een gebruiker moet werken om in aanmerking te komen voor opname in uw analyse. Gebruikers die met de startgebeurtenis werken, worden meegeteld in de kolom &quot;Gebruikers&quot; van de tabel. Deze gebeurtenis fungeert als de noemer voor de getoonde bewaarpercentages. Eén gebeurtenis wordt ondersteund en eigenschapfilters kunnen zo nodig worden toegepast. Standaard zijn de start- en retourgebeurtenis gekoppeld. Dit houdt in dat een gebruiker de geselecteerde gebeurtenis één keer moet uitvoeren om in het cohort te worden opgenomen en vervolgens opnieuw moet worden geteld als een terugkerende gebruiker. In het menu Meer kunt u de start- en retourgebeurtenissen ontkoppelen als u wilt dat de actie die wordt geretourneerd verschilt van de handeling die wordt opgenomen.
* **[!UICONTROL Return events]**: De gebeurteniscriteria waarmee een gebruiker moet werken om te tellen als terugkerende gebruikers in de tijdsinterval. U kunt maximaal drie retourgebeurtenissen selecteren om de retentie te vergelijken.
* **[!UICONTROL Counted as]**: De telmethode die u wilt toepassen op bewaarde gebruikers. U kunt onder andere de volgende opties kiezen:
   * **[!UICONTROL Metric]**: geef het aantal [!UICONTROL Users] of de behouden [!UICONTROL Percentage of users] weer. De noemer voor het percentage gebruikers dat wordt behouden is de inbegrepen gebruikers voor de cohort en is het zelfde over alle duuremmers.
   * **[!UICONTROL Returning]**: Hiermee kunt u bepalen hoe terugkerende gebruikers worden geteld. U kunt onder andere de volgende opties kiezen:
      * **[!UICONTROL On or after]**: wordt vaak &#39;onbegrensd&#39; vasthouden genoemd. Met deze optie wordt een gebruiker geteld als deze op of na de opgegeven duur terugkeert. Bijvoorbeeld op dag 7 of op een willekeurig tijdstip na dag 7. Deze optie is handig om te laten zien hoe gebruikers doorgaan met het activeren en genereert als gevolg een vloeiendere retentiecurve.
      * **[!UICONTROL On exactly]**: wordt vaak &#39;gebonden&#39; retentie genoemd, deze optie telt een gebruiker als deze precies op de opgegeven duur terugkeert. Bijvoorbeeld, precies op dag 7. Deze optie is handig om aan te geven hoe gebruikers binnen bepaalde tijdframes terugkeren en genereert een retentiecurve met meer golving als gevolg. Opmerking: De cohortanalyse in Analysis Workspace gebruikt &quot;op exact&quot; tellen als basis voor haar analyse.
   * **[!UICONTROL Each]**: De tijdsperiode die u wilt instellen voor elke tijdsspanne. U kunt onder andere de volgende opties kiezen:
      * **[!UICONTROL Day/Week/Month]**: de beschikbare opties zijn afhankelijk van het geselecteerde datumbereik. Deze opties zijn identiek aan de instelling **[!UICONTROL Interval]** wanneer u het datumbereik en updates selecteert die automatisch worden ingesteld.
      * **[!UICONTROL Custom brackets]**: deze optie is alleen beschikbaar voor de instelling Bij elke. Hiermee kunt u gebruikers tellen over een groter tijdsbestek, bijvoorbeeld dag 7-10 in plaats van alleen dag 7.
   * **[!UICONTROL Duration settings]**: Staat u toe om de duuremmers te controleren die op de grafiek en de lijst worden getoond. Een tijdsduur is de periode na de startgebeurtenis dat de retourgebeurtenis heeft plaatsgevonden. Opmerking: gebruikers die in aanmerking komen voor tijdsemmers zijn gebaseerd op verstreken tijd, niet op kalenderdagen. Bijvoorbeeld, als een gebruiker voor een gebeurtenis om 11:55 PM op 6 September kwalificeert, dan voor een terugkeergebeurtenis om 12:05 AM op 7 September in aanmerking komt, zouden zij niet in het 1 dagduuremmertje verschijnen. Er moet een volledige periode van 24 uur verstrijken voordat de gebruiker in aanmerking komt voor het tijdsinterval van 1 dag. De beschikbare tijdsemmers zijn afhankelijk van het datumbereik dat u instelt.
      * **[!UICONTROL Auto durations]** definieert automatisch de tijdsemmers op basis van de lengte van het datumbereik en de nabijheid van de huidige dag waarop het datumbereik zich bevindt.
      * **[!UICONTROL Custom durations]** staat u toe om de vier die duuremmers aan te passen op de grafiek en de lijst worden getoond.
* **[!UICONTROL Segments]**: De segmenten die u wilt meten. Elk geselecteerd segment voegt een rij toe aan de cohortingtabel. U kunt maximaal drie segmenten opnemen.

### Diagraminstellingen

De [!UICONTROL Retention] -analyse biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. De opties zijn [!UICONTROL Bar] en [!UICONTROL Line] .

### Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarmee u de retentiegegevens wilt weergeven. Mogelijke geldige opties zijn Dagelijks, Wekelijks en Maandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben, die van invloed zijn op de opties voor de tijdsduur van een emmertje.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

Als u een datumbereik selecteert dat dicht bij de huidige dag ligt, worden gebruikers die aanvankelijk te dicht bij de huidige dag komen, niet opgenomen. Deze analyse geeft altijd alle gebruikers de kans om in alle periodeemmers worden opgenomen. Een bericht onder de kalenderkiezer verstrekt informatie over de datumwaaier waar de gebruikers, en het interval ingaan dat slechts voor terugkerende gebruikers wordt gereserveerd:

* **[!UICONTROL Analyzing users who did the start event in [Date interval]]**: Als een gebruiker binnen dit datumbereik verbinding maakt met de gebeurtenis, worden deze opgenomen in de analyse. Dit datumbereik garandeert alle gebruikers voldoende tijd om in aanmerking te komen voor alle tijdssegmenten. Dit datumbereik kan anders zijn dan de datum die u hebt geselecteerd als deze dicht bij de huidige dag ligt.
* **[!UICONTROL Data from [Date interval] is reserved to complete the analysis]**: Als een gebruiker voor het eerst binnen deze periode aangaat, zijn zij **niet** inbegrepen in de analyse. Voor recente datumbereiken zouden deze gebruikers niet in de gelegenheid zijn om voor alle tijdssegmenten in aanmerking te komen. Voor datumbereiken in het verleden waren deze gebruikers actief buiten het geselecteerde datumbereik.
