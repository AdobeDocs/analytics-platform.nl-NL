---
title: Actieve weergave
description: Identificeer wie nieuw, behouden, terugkeren, of slapend is.
exl-id: 0a300bb2-7620-4e29-a6b5-542476893009
feature: Guided Analysis
source-git-commit: 4121c199e4a5050d84f57c69d7fb1d7b05007fcd
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# [!UICONTROL Active] weergave

De **Actief** view verschaft inzicht in de groei en de verwerving van gebruikers gedurende een specifieke periode. De horizontale as is een tijdinterval, terwijl de verticale as een maat van gebruikers is. Gebruikers worden opgesplitst in vier categorieën:

* **[!UICONTROL New]**: De gebruiker was actief tijdens de huidige periode, maar niet eerder. Kijk hoe ver de analyse terugkijkt door de muisaanwijzer op &#39;[!UICONTROL New users]in de legenda van het diagram. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **[!UICONTROL Repeat]**: De gebruiker was actief in de huidige en onmiddellijk vorige periode.
* **[!UICONTROL Return]**: De gebruiker was actief in de huidige periode en was niet actief in de onmiddellijk voorgaande periode, maar was voorheen actief op een bepaald punt. Kijk hoe ver de analyse terugkijkt door de muisaanwijzer op &#39;[!UICONTROL Return users]in de legenda van het diagram. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **[!UICONTROL Dormant]**: De gebruiker was actief in de onmiddellijk vorige periode, maar is niet actief in de huidige periode. slapende gebruikers tellen niet mee voor het totale aantal actieve gebruikers.

Alle actieve gebruikers (new + repeat + return) worden weergegeven als een tint boven de horizontale as, terwijl alle slapende gebruikers in oranje worden weergegeven onder de horizontale as.

Zie de [!UICONTROL Active] weergave in actie:

>[!VIDEO](https://video.tv.adobe.com/v/3421667/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **[!UICONTROL User retention and chur]n:** Biedt een duidelijke visualisatie rond periodes van hoog of laag vasthouden van de gebruiker. Als u deze periodes van hoge of lage retentie herkent, kunt u productbeslissingen nemen om een hoge retentie aan te moedigen of om de kans op koorts te minimaliseren.
* **[!UICONTROL Campaign assessment]**: Door een specifieke campagne te bekijken, kunt u niet alleen begrijpen hoeveel verkeer het heeft gegenereerd, maar ook hoe goed de campagne gebruikers heeft geholpen betrokken te blijven.
* **[!UICONTROL User lifecycle analysis]**: Door de actieve groei van gebruikers gedurende de hele levenscyclus van de gebruiker te analyseren, kunt u specifieke stadia bepalen waarin de betrokkenheid van de gebruiker afneemt. Als er bijvoorbeeld een hoge mate van slapende gebruikers is voor personen die zich in een instapfase bevinden, kan dit wijzen op bruikbaarheidsproblemen of op de behoefte aan betere begeleiding in het product.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Events]**: De gebeurtenis die u wilt meten. Aangezien dit weergavetype op gebruiker is gebaseerd, wordt een gebruiker die binnen de periode eenmaal met de gebeurtenis communiceert, als een actieve gebruiker geteld. U kunt één gebeurtenis in een vraag omvatten.
* **[!UICONTROL People]**: Het segment dat u wilt meten. U kunt één segment in een vraag omvatten.

## Diagraminstellingen

De [!UICONTROL Active] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Metric]**: De metrische waarde die u wilt meten. U kunt onder andere het aantal gebruikers en het percentage gebruikers kiezen.
* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere de opties Gestapelde balk en Gestapeld gebied kiezen.

## Tijdvergelijking toepassen

{{apply-time-comparison}}

![Vergelijking van actieve tijd](../assets/active-compare.png)

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
