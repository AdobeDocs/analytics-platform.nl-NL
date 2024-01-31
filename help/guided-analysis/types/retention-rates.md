---
title: Bewaarpercentages
description: Meet hoeveel gebruikers uw product blijven gebruiken.
feature: Guided Analysis
keywords: productanalyse
exl-id: c35a0ee0-e6b7-47b5-a5bc-308cde1585de
role: User
source-git-commit: 715d6f33b3cd3f1188e0bd3e6aa3785346c4c302
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# Bewaarpercentages

De **[!UICONTROL Retention rates]** toont het percentage gebruikers dat na hun eerste betrokkenheid binnen het gewenste datumbereik terugkeert. De horizontale as geeft het aantal dagen weer sinds de eerste betrokkenheid van een gebruiker. De verticale as geeft het percentage weer van de gebruikers die zich opnieuw engageren.

Deze analyse telt gebruikers op twee belangrijke gebeurtenissen worden gebaseerd die:

* De gebeurtenis van het begin: De eerste keer een gebruiker die met de gebeurtenis binnen de datumwaaier in dienst neemt
* Retourgebeurtenis: de meest recente keer dat een gebruiker zich met de gebeurtenis heeft beziggehouden binnen het geanalyseerde datumbereik

Het emmertje voor de duur &quot;Dag 0&quot; vertegenwoordigt de eerste tijd dat een gebruiker zich met de gebeurtenis heeft beziggehouden en is altijd precies gelijk aan 100%. Dit emmertje is de noemer die wordt gebruikt om het percentage van behouden gebruikers te berekenen.

De volgende tijdsemmers tellen het aantal gebruikers die op of na die duur terugkwamen. Dit aantal is de teller die wordt gebruikt om het percentage van behouden gebruikers te berekenen.

* Als een gebruiker slechts eenmaal in het gewenste datumbereik (de initiële service) aan de gebeurtenis deelneemt, worden deze alleen weergegeven in het duursegment &quot;Dag 0&quot;.
* Als een gebruiker meerdere dagen na de eerste keer in aanmerking komt voor opname in de analyse, worden deze dagen weergegeven in het meest recente kwalificatieduur en in alle tijdssegmenten vóór de gebeurtenis. Dit type berekening wordt soms &quot;niet-begrensde retentie&quot; genoemd.
* Als een gebruiker gedurende het geconfigureerde datumbereik meerdere keren met de gebeurtenis werkt, worden alleen de eerste en laatste gebeurtenissen in de analyse opgenomen.

![Schermafbeelding met retentiesnelheden](../assets/retention-rates.png)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Cohortanalyse**: Groepeer gebruikers in cohorten op basis van handelingen die ze uitvoeren, zoals aanmelden of aankopen. U kunt vergelijken hoe goed deze groepen behouden en bepalen hoe te om de gebruikerservaring van elke groep te verbeteren.
* **Abonnementsserviceanalyse**: Als uw product een abonnement of een ander type terugkerende inkomstenmodel gebruikt, kunt u het percentage zien van gebruikers die het meeste van uw product maken. U kunt bepaalde kwaliteiten en gedragingen identificeren die deze gebruikers vertonen om beter te begrijpen hoe uw productmarkt past.
* **Gebruikersbetrokkenheid**: Evalueer hoe bepaalde typen gebruikers met uw product werken en vergelijk naast elkaar hoe vaak ze retourneren. Een bepaald segment met een lagere retentie dan anderen kan u inzicht verschaffen in het verbeteren van mogelijke ondermaatse ervaringen die zij kunnen hebben.

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

* **[!UICONTROL Auto durations]**: Stel de tijdsduur automatisch in op basis van de lengte van het datumbereik en de nabijheid van de huidige dag waarop het datumbereik zich bevindt. De emmers van de duur zijn gebogen voor de gemeenschappelijkste gebruiksgevallen.
* **[!UICONTROL Custom durations]**: Stel handmatig de gewenste verstreken intervallen in. U kunt vier tijdsduur instellen.

De beschikbare tijdsemmers zijn afhankelijk van het datumbereik dat u instelt.

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarmee u de retentiegegevens wilt weergeven. Mogelijke geldige opties zijn Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben, wat invloed heeft op automatisch ingestelde tijdsemmers.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

Als u een datumbereik selecteert dat dicht bij de huidige dag ligt, worden gebruikers die aanvankelijk te dicht bij de huidige dag komen, niet opgenomen. Deze analyse geeft altijd alle gebruikers de kans om in alle periodeemmers worden opgenomen. Een bericht onder de kalenderkiezer verstrekt informatie rond de datumwaaier waar de gebruikers, en het interval ingaan dat slechts voor terugkerende gebruikers wordt gereserveerd:

* **Gebruikers analyseren die de startgebeurtenis hebben uitgevoerd in [Datuminterval]**: Als een gebruiker binnen dit datumbereik met de gebeurtenis werkt, worden deze opgenomen in de analyse. Dit datumbereik garandeert alle gebruikers voldoende tijd om in aanmerking te komen voor alle tijdssegmenten. Dit datumbereik kan anders zijn dan de datum die u hebt geselecteerd als deze dicht bij de huidige dag ligt.
* **Gegevens van [Datuminterval] alleen de analyse kan voltooien**: Als een gebruiker zich voor de eerste keer binnen deze periode aansluit, worden de volgende **niet** opgenomen in de analyse. Voor recente datumbereiken zouden deze gebruikers niet in de gelegenheid zijn om voor alle tijdssegmenten in aanmerking te komen. Voor datumbereiken in het verleden waren deze gebruikers actief buiten het geselecteerde datumbereik.

## Cohortingtabel

De tabel onder het diagram biedt een geaggregeerde weergave (vergelijkbaar met diagramgegevens) en een volledige cohortingtabel. De volledige cohortingtabel bevat details over elk datuminterval en wanneer gebruikers betrokken zijn.
