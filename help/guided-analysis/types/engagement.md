---
title: Weergave Betrokkenheid
description: Begrijp de breedte en diepte van eigenschapbetrokkenheid.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
role: User
exl-id: 8a48ad3b-fa30-497e-8306-f8d881b1a335
source-git-commit: 670443a8caf6b71f49fc63a23b5328609864a9be
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# [!UICONTROL Engagement] weergave

De **[!UICONTROL Engagement]** de mening verstrekt inzicht in hoe vaak een eigenschap tegenover hoeveel mensen het gebruikt. Deze analyse werkt het best wanneer het vergelijken van verscheidene eigenschappen aan elkaar. Het helpt investeringsbeslissingen te voeden door te begrijpen wat uw kern, macht, eenmalig, en twijfelachtige eigenschappen zijn.

De eigenschappen die naar de bovenkant van deze visualisatie trekken wijzen erop dat zij vaak onder betrokken gebruikers worden gebruikt. De eigenschappen die naar het recht van deze visualisatie trekken wijzen erop dat zij wijd onder uw actieve gebruikers worden geadopteerd. Het gemiddelde aantal keren dat een functie wordt gebruikt, verdeelt de grafiek horizontaal. Het mediane percentage actieve gebruikers verdeelt de grafiek verticaal. Medianen worden berekend op basis van de gebeurtenissen die in de query zijn geselecteerd, niet alle gegevens.

* Functies in de linkerbovenhoek van de matrix zijn uw **macht** kenmerken; deze worden niet op grote schaal toegepast, maar worden vaak gebruikt door betrokken gebruikers.
* Functies in de rechterbovenhoek van de matrix zijn uw **hoge impact** kenmerken; zij worden zowel op grote schaal toegepast als veelvuldig gebruikt.
* Functies linksonder in de matrix zijn uw **laag effect** kenmerken; zij worden niet op grote schaal toegepast of worden niet vaak gebruikt.
* Functies rechtsonder in de matrix zijn uw **eenmalig** kenmerken; zij worden op grote schaal toegepast, maar niet vaak gebruikt.

>[!VIDEO](https://video.tv.adobe.com/v/3429489/&learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Betrokkenheid bij onderdeel**: U kunt een directe correlatie tot stand brengen tussen de betrokkenheid en de acceptatie van een specifieke functie. Begrijpen welke eigenschappen het meest worden gebruikt kan helpen bepalen welke eigenschappen om in verder te investeren.
* **Ongebruikte functies ontdekken**: Functies met weinig actieve gebruikers maar een hoog gebruik kunnen wijzen op een energiebron, die waardevol is maar niet wordt ontdekt of gebruikt door de bevolking in het algemeen. U kunt overwegen de ontdekkingsmogelijkheden van deze functies te verbeteren, zodat meer gebruikers deze kunnen benutten.
* **Populaire functies verbeteren**: Functies met een hoog actieve gebruiker maar een laag gebruik kunnen erop wijzen dat een functie sterk wordt aangevraagd, maar onderbenut. Deze situaties bieden mogelijkheden om meer van uw gebruikers te leren over welke verbeteringen de eigenschap voor hen waardevoller zouden maken.
* **Op functies gebaseerde segmenten maken**: Op deze manier kunt u het gebruik van de functie weergeven om extra analysemogelijkheden te creëren. Maak een segment voor elk punt in het diagram om verder in die gebruikersgroep te duiken en pas die lessen toe op uw strategie voor de gebruikersbetrokkenheid.
* **Aanname van functies A/B testen**: Vergelijk het gebruik van meerdere functies in verschillende groepen gebruikers. Voeg segmenten in de vraagrail toe om het verschil in eigenschapgebruik over zeer belangrijke gebruikersgroepen te bepalen.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Events]**: De gebeurtenissen die u wilt meten. Elke gebeurtenis vertegenwoordigt het gebruik van een bepaalde functie en wordt weergegeven als een punt binnen de matrix. U kunt maximaal tien gebeurtenissen opnemen. De mediaan wordt berekend op basis van de geselecteerde gebeurtenissen.
* **[!UICONTROL Counted as]**: Langs de x-as kunt u het gemiddelde percentage van dagelijkse, wekelijkse, maandelijkse of driemaandelijkse actieve gebruikers meten. Op de y-as worden de gemiddelde tijden per gebruiker automatisch aangepast op basis van de selectie van de x-as.
* **[!UICONTROL Segments]**: De segmenten die u wilt meten. Elk geselecteerd segment verdubbelt het aantal getekende punten in het diagram en de rijen in de tabel. U kunt maximaal drie segmenten opnemen.

>[!TIP]
>
>Als meerdere gebeurtenissen het gebruik van één functie vertegenwoordigen, kunt u een nieuwe gebeurtenis afleiden die de functie in Gegevens vertegenwoordigt.

## Diagraminstellingen

De [!UICONTROL Engagement] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Medians]**: Bepaal waar de mediaanlijnen worden weergegeven en hoe de uitgezette punten zich verhouden tot die medianen.
   * **[!UICONTROL Standard]**: De absolute waarde van gebruik en betrokkenheid weergeven.
   * **[!UICONTROL Normalized]**: relatieve wijzigingen ten opzichte van elke mediaan tonen.
* **[!UICONTROL Top events overlay]**: Bekijk hoe uw gebeurtenissen zich verhouden tot de top 20 van gebeurtenissen, op basis van recency en relevantie van bedrijf en gebruiker (hetzelfde algoritme dat wordt toegepast op de gebeurteniskiezer in de queryrail).

## Tijdvergelijking

{{apply-time-comparison}}

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarop u trendgegevens wilt bekijken. Dit weergavetype wordt behandeld [!UICONTROL Interval] vergelijkbaar met [!UICONTROL Counted as] in de querytrack. Uuractieve gebruikers worden niet ondersteund.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
