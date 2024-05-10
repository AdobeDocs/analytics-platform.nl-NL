---
title: Weergave Betrokkenheid
description: Begrijp de breedte en breedte van de betrokkenheid van functies.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
role: User
source-git-commit: 2b8afe1dbac5057f867437e2bfce27f3bd752d57
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# [!UICONTROL Engagement] weergave

De **[!UICONTROL Engagement]** de mening verstrekt inzicht in hoe vaak een eigenschap tegenover hoeveel mensen het gebruikt. Deze analyse werkt het best wanneer het vergelijken van verscheidene eigenschappen aan elkaar.

Kenmerken die naar de bovenkant van deze visualisatie trekken, geven aan dat deze vaak wordt bezocht door de personen die deze functie gebruiken. De eigenschappen die naar het recht van deze visualisatie trekken wijzen erop dat het grootste deel van gebruikers die met de eigenschap in dienst nemen. Het gemiddelde aantal keren dat een functie wordt gebruikt, verdeelt de grafiek horizontaal. Het mediaanpercentage van dagelijkse actieve gebruikers verdeelt de grafiek verticaal.

* De eigenschappen in top-left van de matrijs betekenen dat een eigenschap niet wijd wordt aangenomen. Onder de mensen die het gebruiken, gebruiken ze het echter vaak.
* De eigenschappen in het hoogste recht van de matrijs betekenen dat een eigenschap zowel wijd als vaak wordt gebruikt.
* De eigenschappen in het bodem-recht van de matrijs betekenen dat een eigenschap algemeen wordt aangenomen, maar niet vaak gebruikt.
* De eigenschappen in de bodem-linkerzijde van de matrijs betekenen dat een eigenschap niet wijd wordt goedgekeurd, noch wordt het vaak gebruikt.

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Betrokkenheid bij onderdeel**: U kunt een directe correlatie tot stand brengen tussen de betrokkenheid en de acceptatie van een specifieke functie. Begrijpen welke eigenschappen het meest worden gebruikt kan helpen bepalen welke eigenschappen om voorrang te geven aan het verbeteren.
* **Onderbenutte functies ontdekken**: Functies met weinig actieve gebruikers maar een hoog gebruik kunnen wijzen op een verborgen, maar waardevolle functie. U kunt deze typen functies aan meer gebruikers beschikbaar maken.
* **Populaire functies verbeteren**: Functies met een hoog actieve gebruiker maar een laag gebruik kunnen erop wijzen dat een functie sterk wordt aangevraagd, maar onderbenut. Overweeg te investeren in het verbeteren van deze functies, zodat ze vaker worden gebruikt.
* **Op functies gebaseerde segmenten maken**: Door te analyseren hoe vaak een functie wordt gebruikt in verhouding tot het aantal gebruikers dat de functie toepast, kunt u bepalen welke typen gebruikers een bepaalde functie gebruiken. U kunt segmenten maken op basis van gebruikers die een functie handmatig gebruiken of op basis van gebruikers die die functie vaak gebruiken.
* **Aanname van functies A/B testen**: Vergelijk het gebruik van meerdere functies met behulp van segmenten. Voeg de segmenten van elke cohort in vraagspoor toe om het verschil in eigenschapgebruik gemakkelijk te bepalen.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Events]**: De gebeurtenissen die u wilt meten. Deze gebeurtenissen vertegenwoordigen doorgaans het gebruik van een bepaalde functie. Elke selectie wordt vertegenwoordigd als een punt binnen de matrix. U kunt maximaal tien gebeurtenissen opnemen.
* **[!UICONTROL Counted as]**: Bepaal de details van hoe de x-as gebruikers telt. U kunt het gemiddelde percentage van dagelijkse, wekelijkse, maandelijkse, of driemaandelijkse actieve gebruikers meten. Op de y-as worden de gemiddelde tijden per gebruiker automatisch aangepast op basis van de selectie van de x-as.
* **[!UICONTROL Segments]**: De segmenten die u wilt meten. Elk geselecteerd segment verdubbelt het aantal getekende punten in het diagram en de rijen in de tabel. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De [!UICONTROL Engagement] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Medians]**: Bepaal waar de mediaanlijnen worden weergegeven en hoe de uitgezette punten zich verhouden tot die medianen.
   * **[!UICONTROL Standard]**: De absolute waarde van gebruik en betrokkenheid weergeven.
   * **[!UICONTROL Normalized]**: relatieve wijzigingen ten opzichte van elke mediaan tonen.
* **[!UICONTROL Top events overlay]**: Zie hoe uw gebeurtenissen werken in vergelijking met de meest voorkomende gebeurtenissen.

## Tijdvergelijking

{{apply-time-comparison}}

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarop u trendgegevens wilt bekijken. Dit weergavetype wordt behandeld [!UICONTROL Interval] vergelijkbaar met [!UICONTROL Counted as] in de querytrack. Uuractieve gebruikers worden niet ondersteund.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
