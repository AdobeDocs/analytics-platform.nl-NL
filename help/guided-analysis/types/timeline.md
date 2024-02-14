---
title: Tijdlijnweergave
description: Neem sessiegebeurtenissen op gebruikersniveau in de loop der tijd waar om ervaringspatronen te zoeken.
feature: Guided Analysis
keywords: productanalyse
role: User
source-git-commit: 6f3725653453e31244bfed34670782fe9d9c0c2f
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# [!UICONTROL Timeline] weergave

De **[!UICONTROL Timeline]** in de weergave kunt u sessiegebeurtenissen op gebruikersniveau in de loop der tijd observeren om ervaringspatronen te zoeken en betere gebruikersverhalen te vertellen. Met de linkerrails kunt u de stream filteren op eigenschapswaarden en segmenten. Met de rechterrails kunt u een keuze maken uit een gerandomiseerde lijst met gebruikers die voldoen aan de filtercriteria. In het middelste gebied wordt de stream voor de geselecteerde gebruiker per sessie weergegeven, die bestaat uit tijdstempel, eigenschapswaarden en duur. De duur is niet beschikbaar voor de laatste gebeurtenis in een bepaalde sessie.

>[!NOTE]
>
>De tijdlijnweergave vereist dat de **[!UICONTROL Person ID]** standaardonderdeel beschikbaar in de [gegevensweergave](/help/data-views/component-reference.md#optional). De opneming van identiteitskaart van de Persoon in een gegevensmening wordt beheerd door uw beheerder van de Customer Journey Analytics, die uw organisatie volledige privacycontrole over geeft wie tot deze gegevens kan toegang hebben.

Als een gegevensweergave niet de [!UICONTROL Person ID] toegevoegd, wordt het volgende bericht weergegeven:

* **Admins**: *De eigenschap PersonID is vereist voor deze analyse. Voeg een persoon-id toe aan de gegevensweergave.*
* **Niet-beheerders**: *De eigenschap PersonID is vereist voor deze analyse. Werk samen met de beheerder van de Customer Journey Analytics om persoon-id toe te voegen aan de gegevensweergave.*

![Tijdlijnscreenshot](../assets/timeline.png)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Wrijvingsexploratie**: Als u een steile druppel vindt in het dialoogvenster [Wrijving](friction.md) in deze weergave kunt u een segment van die gebruikers maken en het segment toepassen om mogelijke oorzaken te onderzoeken.
* **Foutgedrag**: Als gebruikers een productfout tegenkomen, kunt u nagaan wat gebruikers deden voor of na het zien van die fout.
* **Validatie van gegevensverzameling**: Gegevensbeheerders kunnen deze weergave naar hun eigen persoonlijke id filteren om te controleren of de implementatie van hun organisatie naar behoren werkt.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Property]**: De eigenschap waarvoor u gestreamde waarden wilt weergeven. In het midden van de stream worden waarden voor de geselecteerde eigenschap weergegeven. U kunt ook filters toepassen om de stream naar beneden te beperken tot meer relevante gegevens. Geldige operatoren voor het filter zijn [!UICONTROL Equals], [!UICONTROL Does not equal], [!UICONTROL Starts with], [!UICONTROL Ends with], [!UICONTROL Contains], [!UICONTROL Does not contain], [!UICONTROL Exists], en [!UICONTROL Does not exist].
* **[!UICONTROL Segments]**: Het segment dat u wilt analyseren. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen. Als u de weergave wilt beperken tot een specifieke persoon-id, kunt u hier filteren op die persoon-id. Eén segment wordt ondersteund voor deze weergave.

## Diagraminstellingen

De [!UICONTROL Timeline] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Show as]**: Geeft de gewenste eigenschapswaarden weer.
   * [!UICONTROL Show all]: Alle eigenschapswaarden in een sessie tonen.
   * [!UICONTROL Highlight]: Hiermee markeert u visueel eigenschapswaarden in een sessie die overeenkomen met de queryfilters.
   * [!UICONTROL View only]: Alleen eigenschapswaarden weergeven in een sessie die overeenkomen met de queryfilters.

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarop u trendgegevens wilt bekijken. Deze instelling heeft geen invloed op niet-trendweergaven, zoals de tijdlijn.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
