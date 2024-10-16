---
title: Tijdlijnweergave
description: Neem sessiegebeurtenissen op gebruikersniveau in de loop der tijd waar om ervaringspatronen te zoeken.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
role: User
exl-id: d3da9257-a133-46c8-8fac-1a33d3372bb7
source-git-commit: ce04e69d2c933f893eeeff04abb0f56fb4000e6f
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# [!UICONTROL Timeline] weergave

De ![ mening van de Chronologie ](/help/assets/icons/Timeline.svg) **[!UICONTROL Timeline]** staat u toe om gebruiker-vlakke zittingsgebeurtenissen in tijd waar te nemen om ervaringspatronen te vinden en betere gebruikersverhalen te vertellen. Met de linkerrails kunt u de stream filteren op eigenschapswaarden en segmenten. Met de rechterrails kunt u een keuze maken uit een gerandomiseerde lijst met gebruikers die voldoen aan de filtercriteria. In het middelste gebied wordt de stream voor de geselecteerde gebruiker per sessie weergegeven, die bestaat uit tijdstempel, eigenschapswaarden en duur. De duur is niet beschikbaar voor de laatste gebeurtenis in een bepaalde sessie.

>[!VIDEO](https://video.tv.adobe.com/v/3427810/?learn=on)

>[!NOTE]
>
>De mening van de Chronologie vereist dat de **[!UICONTROL Person ID]** standaardcomponent in de [ gegevensmening ](/help/data-views/component-reference.md#optional) beschikbaar is. De opneming van identiteitskaart van de Persoon in een gegevensmening wordt beheerd door uw beheerder van de Customer Journey Analytics, die uw organisatie volledige privacycontrole over geeft wie tot deze gegevens kan toegang hebben.

Als de component [!UICONTROL Person ID] niet is toegevoegd aan een gegevensweergave, wordt het volgende bericht weergegeven:

* **Admins**: *het bezit PersonID wordt vereist voor deze analyse. Gelieve te voegen identiteitskaart van de Persoon aan de gegevensmening toe.*
* **niet-admins**: *het bezit PersonID wordt vereist voor deze analyse. Gelieve te werken met uw beheerder van de Customer Journey Analytics om identiteitskaart van de Persoon aan de gegevensmening toe te voegen.*

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Verkenning van de Wrijving**: Als u een steile daling in de [ mening van de Wrijving ](funnel.md) vindt, kunt u een segment van die gebruikers tot stand brengen en het segment in deze mening toepassen om potentiële oorzaken te onderzoeken.
* **het gedrag van de Fout**: Als de gebruikers een productfout ontmoeten, kunt u onderzoeken welke gebruikers vóór of na het zien van die fout deden.
* **de inzamelingsbevestiging van Gegevens**: De beheerders van gegevens kunnen deze mening aan hun eigen identiteitskaart van de Persoon filtreren om te bevestigen dat de implementatie van hun organisatie zoals verwacht werkt.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Property]**: De eigenschap waarvoor u gestreamde waarden wilt weergeven. In het midden van de stream worden waarden voor de geselecteerde eigenschap weergegeven. U kunt ook filters toepassen om de stream naar beneden te beperken tot meer relevante gegevens. Geldige operatoren voor het filter zijn [!UICONTROL Equals] , [!UICONTROL Does not equal] , [!UICONTROL Starts with] , [!UICONTROL Ends with] , [!UICONTROL Contains] , [!UICONTROL Does not contain] , [!UICONTROL Exists] en [!UICONTROL Does not exist] .
* **[!UICONTROL Segments]**: Het segment dat u wilt analyseren. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen. Als u de weergave wilt beperken tot een specifieke persoon-id, kunt u hier filteren op die persoon-id. Eén segment wordt ondersteund voor deze weergave.

## Diagraminstellingen

De weergave [!UICONTROL Timeline] biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Show as]** - Geeft de gewenste eigenschapswaarden weer.
   * [!UICONTROL Show all]: geef alle eigenschapswaarden in een sessie weer.
   * [!UICONTROL Highlight]: hiermee markeert u visueel de eigenschapswaarden in een sessie die overeenkomen met de queryfilters.
   * [!UICONTROL View only]: alleen eigenschapswaarden weergeven in een sessie die overeenkomen met de queryfilters.

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u trendgegevens wilt weergeven. Deze instelling heeft geen invloed op niet-trendweergaven, zoals de tijdlijn.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
