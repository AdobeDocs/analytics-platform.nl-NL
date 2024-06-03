---
title: Bewaarpercentages
description: Meet hoeveel gebruikers uw product blijven gebruiken.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: c35a0ee0-e6b7-47b5-a5bc-308cde1585de
role: User
source-git-commit: f4a235d90ad44dbb192b74a03accc7ad4a39e986
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---

# Bewaarpercentages

De **[!UICONTROL Retention rates]** Bekijk hoe gebruikers uw product in de loop van de tijd blijven gebruiken, zodat u beter kunt begrijpen welke producten op de markt zijn. In de analyse worden gebruikers op basis van twee belangrijke gebeurtenissen beoordeeld:

* De gebeurtenis van het begin: De eerste keer een gebruiker die met de begingebeurtenis binnen de datumwaaier wordt geëngageerd
* Geretourneerde gebeurtenis: de meest recente tijd dat een gebruiker zich met de terugkeergebeurtenis binnen het geanalyseerde datumbereik bediende

In deze weergave vertegenwoordigt de x-as van de grafiek de tijd sinds de begingebeurtenis van een gebruiker en vertegenwoordigt de y-as het percentage gebruikers dat met de geretourneerde gebeurtenis(sen) werkt. U kunt zowel behoud als kromme over duur bekijken, en de getoonde duur kan door de vraagmontages worden aangepast. Onder de grafiek, verstrekt een lijst samengevoegde gegevens met de optie om individuele cohorts te tonen, die een groep mensen zijn die de beginnende gebeurtenis op de zelfde datum deden.

![Schermafbeelding met retentiesnelheden](../assets/retention-rates.png){style="border:1px solid gray"}

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Cohortanalyse**: Groepeer gebruikers in cohorten op basis van handelingen die ze uitvoeren, zoals aanmelden of aankopen. U kunt vergelijken hoe goed deze groepen behouden en bepalen hoe te om de gebruikerservaring van elke groep te verbeteren.
* **Geschiktheid van de productmarkt**: Meet het regelmatige gebruik van uw product en visualiseer het als retentiecurven. Grotere retentie betekent een grotere geschiktheid voor de productmarkt en wanneer de curve wordt afgevlakt, geeft dit aan hoe lang het duurt om uw pasvorm te bereiken. Bekijk deze analyse op een algemeen niveau of uitsplitsing naar afzonderlijke productkenmerken om dieper inzicht te krijgen.
* **Abonnementsserviceanalyse**: Als uw product een abonnement of een ander type terugkerende inkomstenmodel gebruikt, kunt u het percentage zien van gebruikers die het meeste van uw product maken. U kunt bepaalde kwaliteiten en gedragingen identificeren die deze gebruikers vertonen.
* **Gebruikersbetrokkenheid**: Evalueer hoe bepaalde typen gebruikers met uw product werken en vergelijk naast elkaar hoe vaak ze retourneren. Een bepaald segment met een lagere retentie dan anderen kan u inzicht verschaffen in het verbeteren van mogelijke ondermaatse ervaringen die zij kunnen hebben.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Start event]**: De gebeurteniscriteria waarmee een gebruiker moet werken om in aanmerking te komen voor opname in uw analyse. Gebruikers die met de startgebeurtenis werken, worden meegeteld in de kolom &quot;Gebruikers&quot; van de tabel. Dit is de noemer voor de getoonde aanhoudingspercentages. Eén gebeurtenis wordt ondersteund en eigenschapfilters kunnen zo nodig worden toegepast. Standaard zijn de start- en retourgebeurtenis gekoppeld. Dit houdt in dat een gebruiker de geselecteerde gebeurtenis één keer moet uitvoeren om in het cohort te worden opgenomen en vervolgens opnieuw moet worden geteld als een terugkerende gebruiker. In het menu Meer kunt u de start- en retourgebeurtenissen ontkoppelen als u wilt dat de actie die wordt geretourneerd verschilt van de handeling die wordt opgenomen.
* **[!UICONTROL Return events]**: De gebeurteniscriteria waarmee een gebruiker moet werken om te tellen als terugkerende gebruikers in de periodeemmers. U kunt maximaal drie retourgebeurtenissen selecteren om de retentie te vergelijken.
* **[!UICONTROL Counted as]**: De telmethode die u wilt toepassen op bewaarde gebruikers. U kunt onder andere de volgende opties kiezen:
   * **[!UICONTROL Metric]**: Toon het aantal van [!UICONTROL Users] of de [!UICONTROL Percentage of users] behouden. De noemer voor het percentage gebruikers dat wordt behouden, is de inbegrepen gebruikers voor het cohort en is voor alle periodeemmers gelijk.
   * **[!UICONTROL Returning]**: Hiermee kunt u bepalen hoe terugkerende gebruikers worden geteld. U kunt onder andere de volgende opties kiezen:
      * **[!UICONTROL On or after]**: Wordt vaak &#39;onbegrensd&#39; vasthouden genoemd, dan telt deze optie een gebruiker wanneer deze op of na de opgegeven duur terugkeert. Bijvoorbeeld op dag 7 of op een willekeurig tijdstip na dag 7. Deze optie is handig voor het weergeven van de manier waarop gebruikers blijven werken en genereert als gevolg hiervan een vloeiendere retentiecurve.
      * **[!UICONTROL On exactly]**: Wordt vaak &#39;gebonden&#39; retentie genoemd, deze optie telt een gebruiker als deze exact op de opgegeven duur terugkeert. Bijvoorbeeld, precies op dag 7. Deze optie is handig om aan te geven hoe gebruikers binnen bepaalde tijdframes terugkeren en genereert een retentiecurve met meer golving als gevolg. Opmerking: De cohortanalyse in Analysis Workspace gebruikt &quot;op exact&quot; tellen als basis voor haar analyse.
   * **[!UICONTROL Each]**: De tijdsperiode die u wilt gebruiken voor elk tijdssegment. U kunt onder andere de volgende opties kiezen:
      * **[!UICONTROL Day/Week/Month]**: De beschikbare opties zijn afhankelijk van het geselecteerde datumbereik. Deze opties zijn identiek aan de **[!UICONTROL Interval]** als u het datumbereik selecteert, wordt die instelling automatisch bijgewerkt.
      * **[!UICONTROL Custom brackets]**: Deze optie is alleen beschikbaar voor de instelling Bij elke. Hiermee kunt u gebruikers tellen over een groter tijdsbestek, bijvoorbeeld dag 7-10 in plaats van alleen dag 7.
   * **[!UICONTROL Duration settings]**: Staat u toe om de tijdsemmers te controleren die op de grafiek en de lijst worden getoond. Een tijdsduur is de periode na de startgebeurtenis dat de retourgebeurtenis heeft plaatsgevonden. Opmerking: gebruikers die in aanmerking komen voor tijdsemmers zijn gebaseerd op verstreken tijd, niet op kalenderdagen. Bijvoorbeeld, als een gebruiker voor een gebeurtenis om 11:55 PM op 6 September kwalificeert, dan voor een terugkeergebeurtenis om 12:05 AM op 7 September in aanmerking komt, zouden zij niet in het 1 dagduuremmertje verschijnen. Er moet een volledige periode van 24 uur verstrijken voordat de gebruiker in aanmerking komt voor het tijdsinterval van 1 dag. De beschikbare tijdsemmers zijn afhankelijk van het datumbereik dat u instelt.
      * **[!UICONTROL Auto durations]** Hiermee worden automatisch de tijdsemmers gedefinieerd op basis van de lengte van het datumbereik en de nabijheid van de huidige dag waarop het datumbereik zich bevindt.
      * **[!UICONTROL Custom durations]** staat u toe om de vier die duuremmers aan te passen op de grafiek en de lijst worden getoond.
* **[!UICONTROL Segments]**: De segmenten die u wilt meten. Elk geselecteerd segment voegt een rij toe aan de cohortingtabel. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De [!UICONTROL Retention rates] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Bar] en [!UICONTROL Line].

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarmee u de retentiegegevens wilt weergeven. Mogelijke geldige opties zijn Dagelijks, Wekelijks en Maandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben, die van invloed zijn op de opties voor de tijdsduur van een emmertje.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

Als u een datumbereik selecteert dat dicht bij de huidige dag ligt, worden gebruikers die aanvankelijk te dicht bij de huidige dag komen, niet opgenomen. Deze analyse geeft altijd alle gebruikers de kans om in alle periodeemmers worden opgenomen. Een bericht onder de kalenderkiezer verstrekt informatie over de datumwaaier waar de gebruikers, en het interval ingaan dat slechts voor terugkerende gebruikers wordt gereserveerd:

* **[!UICONTROL Analyzing users who did the start event in [Date interval]]**: Als een gebruiker binnen dit datumbereik met de gebeurtenis werkt, worden deze opgenomen in de analyse. Dit datumbereik garandeert alle gebruikers voldoende tijd om in aanmerking te komen voor alle tijdssegmenten. Dit datumbereik kan anders zijn dan de datum die u hebt geselecteerd als deze dicht bij de huidige dag ligt.
* **[!UICONTROL Data from [Date interval] is reserved to complete the analysis]**: Als een gebruiker zich voor de eerste keer binnen deze periode aansluit, worden de volgende **niet** opgenomen in de analyse. Voor recente datumbereiken zouden deze gebruikers niet in de gelegenheid zijn om voor alle tijdssegmenten in aanmerking te komen. Voor datumbereiken in het verleden waren deze gebruikers actief buiten het geselecteerde datumbereik.
