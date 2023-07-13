---
title: Weergave opheffen
description: Vergelijk de prestaties in gelijke perioden vóór en na de release.
feature: Guided Analysis
source-git-commit: a635c43c129ea45b270e304f4310b95124709b2a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Weergave opheffen

{{release-limited-testing}}

De **Geen** de weergave toont een vergelijking van de manier waarop de belangrijkste indicatoren vóór en na een bepaalde datum zijn uitgevoerd. De horizontale as van dit rapport is een tijdinterval, terwijl de verticale as de gewenste belangrijkste indicatoren meet. Een verticale balk in het midden van het diagram geeft de datum aan die u voor en na wilt vergelijken. Deze datum is doorgaans een opmerkelijke wijziging van het product waarop u wilt meten, zoals een update van het product of het starten van de campagne.

![Geen](../assets/release.png)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Algemene prestatiebeoordeling:** Het vergelijken van algemene zeer belangrijke indicatoren, zoals betrokkenheidsmaatregelen, kan u helpen bepalen als een bepaalde versie over het geheel genomen succesvol was.
* **Toezicht**: Als er bepaalde maatregelen zijn waarvan u verwacht dat ze vlak blijven wanneer er wijzigingen worden aangebracht, zoals webvitalen zoals laadtijd of logins, vergelijkt u deze voor en na de release om ervoor te zorgen dat de release geen onbedoelde gevolgen heeft.
* **Aanpassing van functies**: Als een productupdate zich op het verbeteren van een bepaalde eigenschap concentreert, kunt u deze mening gebruiken om het gebruik van die eigenschap vóór en na de productupdate direct te vergelijken.
* **Bugdetectie**: Het volgen van het aantal fouten vóór en na een versie kan een vroege indicator van klantenkwesties verstrekken. Als u onmiddellijk na een release een toename van fouten opmerkt, kunt u samenwerken met ontwikkelingsteams of ontwikkelingsteams om het probleem te identificeren en te verhelpen, zodat de klant niet meer last krijgt.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Belangrijkste indicatoren**: De gebeurtenissen die u per gebruiker wilt meten. Elke geselecteerde toetsindicator wordt weergegeven als een gekleurde lijn. Aan de tabel wordt een rij toegevoegd die de gebeurtenis vertegenwoordigt. U kunt maximaal drie gebeurtenissen opnemen.
* **Factoren**: De datum die u voor en na wilt vergelijken.
* **Mensen**: Het segment dat u wilt meten. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen.

## Diagraminstellingen

De weergave Vrijgeven biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **Metrisch**: De metrische waarde die u wilt meten. Opties omvatten [!UICONTROL Events per user], [!UICONTROL Percentage of users], [!UICONTROL Events], [!UICONTROL Sessions], en [!UICONTROL Users].
* **Type diagram**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere Lijn kiezen.

## Datumbereik

De datumselectie in de effectbeoordeling werkt anders dan andere analysetypen, aangezien het verslag zich rond de datum bevindt die in de queryrail is gespecificeerd. De volgende opties zijn beschikbaar:

* **Interval**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Geldige opties zijn [!UICONTROL Daily], [!UICONTROL Weekly], [!UICONTROL Monthly], en [!UICONTROL Quarterly]. Het wijzigen van het interval heeft invloed op de opties die beschikbaar zijn voor de periode Voor en Na.
* **Voor en na de periode**: De hoeveelheid tijd die voor en na de datum moet worden geanalyseerd die in de querytrack wordt opgegeven. Welke opties beschikbaar zijn, is afhankelijk van de [!UICONTROL Interval] selectie.
