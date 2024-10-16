---
title: Weergave opheffen
description: Vergelijk de prestaties in gelijke perioden vóór en na de release.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: 93e6e4f1-bbe4-4a6c-8ec3-54d1f9a8b847
role: User
source-git-commit: ce04e69d2c933f893eeeff04abb0f56fb4000e6f
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# [!UICONTROL Release impact] weergave

De ![ mening van de Versie ](/help/assets/icons/Release.svg) **[!UICONTROL Release impact]** toont een vergelijking van hoe de zeer belangrijke indicatoren vóór en na een bepaalde datum presteerden. De horizontale as van dit rapport is een tijdinterval, terwijl de verticale as de gewenste belangrijkste indicatoren meet. Een verticale balk in het midden van het diagram geeft de datum aan die u voor en na wilt vergelijken. Deze datum is doorgaans een opmerkelijke wijziging van het product waarop u wilt meten, zoals een update van het product of het starten van de campagne.

>[!VIDEO](https://video.tv.adobe.com/v/3421665/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Algemene prestatiesevaluatie:** het vergelijken van algemene zeer belangrijke indicatoren, zoals betrokkenheidsmaatregelen, kan u helpen bepalen als een bepaalde versie algemeen succesvol was.
* **Controle**: De vitale metriek van het spoor die u zou verwachten om vlak te blijven wanneer de veranderingen, zoals ladingstijd of aantal logins worden aangebracht. Gebruik dit analysetype om hen vóór en na een versie te vergelijken om ervoor te zorgen dat het geen onbedoelde gevolgen had.
* **Goedkeuring van de Eigenschap**: Als een productupdate op het verbeteren van een bepaalde eigenschap wordt geconcentreerd, kunt u deze mening gebruiken om het gebruik van die eigenschap vóór en na de productupdate direct te vergelijken.
* **opsporing van het insect**: Het volgen van het aantal fouten vóór en na een versie kan een vroege indicator van klantenkwesties verstrekken. Als u onmiddellijk na een release een toename van fouten opmerkt, kunt u samenwerken met ontwikkelingsteams of ontwikkelingsteams om het probleem te identificeren en te verhelpen, zodat de klant niet meer te lijden krijgt.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen dit meningstype en [ Eerste gebruik ](first-use-impact.md).
* **[!UICONTROL Key indicators]**: De gebeurtenissen die u per gebruiker wilt meten. Elke geselecteerde toetsindicator wordt weergegeven als een gekleurde lijn. Aan de tabel wordt een rij toegevoegd die de gebeurtenis vertegenwoordigt. U kunt maximaal drie gebeurtenissen opnemen.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. De opties zijn [!UICONTROL Events per user] , [!UICONTROL Percentage of users] , [!UICONTROL Events] , [!UICONTROL Sessions] en [!UICONTROL Users] .
* **[!UICONTROL Factors]**: De datum die u voor en na wilt vergelijken.
* **[!UICONTROL Segments]**: Het segment dat u wilt meten. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen.

## Diagraminstellingen

De weergave Vrijgeven biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. De opties zijn [!UICONTROL Line] en [!UICONTROL Bar] .

## Datumbereik

De datumselectie in de effectbeoordeling werkt anders dan andere analysetypen, aangezien het verslag zich rond de datum bevindt die in de queryrail is gespecificeerd. De volgende opties zijn beschikbaar:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Geldige opties zijn [!UICONTROL Daily] , [!UICONTROL Weekly] , [!UICONTROL Monthly] en [!UICONTROL Quarterly] . Het wijzigen van het interval heeft invloed op de opties die beschikbaar zijn voor de periode Voor en Na.
* **[!UICONTROL Before and after period]**: De hoeveelheid tijd die moet worden geanalyseerd voor en na de datum die is opgegeven in de querytrack. Welke opties beschikbaar zijn, is afhankelijk van de selectie van [!UICONTROL Interval] .
