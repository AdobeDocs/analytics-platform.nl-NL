---
title: Tijdlijnweergave
description: Maak kennis met ervaringspatronen en vertel betere gebruikersverhalen.
feature: Guided Analysis
keywords: productanalyse
role: User
source-git-commit: d7e1092e1b2b4e9decd8d601c4b6415b13f1e02a
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# [!UICONTROL Timeline] weergave

De **[!UICONTROL Timeline]** in de weergave kunt u sessiegebeurtenissen op gebruikersniveau gedurende een periode observeren om ervaringspatronen te zoeken en betere gebruikersverhalen te vertellen. Met de linkerrails kunt u filteren op eigenschapswaarden die u wilt streamen en met de rechterrails kunt u de persoon-id selecteren die u wilt analyseren. In het middelste gebied wordt de stream per sessie weergegeven, die bestaat uit tijdstempel, eigenschapswaarden en duur. De duur is niet beschikbaar voor de laatste gebeurtenis in een bepaalde sessie.

>[!NOTE]
>
>De tijdlijnweergave vereist dat de **[!UICONTROL Person ID]** standaardonderdeel beschikbaar in de [gegevensweergave](/help/data-views/component-reference.md#optional). De opname van Person-id in een gegevensweergave wordt beheerd door uw Adobe Analytics-gegevensbeheerder, waardoor organisaties volledig controle hebben over de privacy van de organisatie over wie toegang heeft tot deze gegevens.

Als een gegevensweergave niet de [!UICONTROL Person ID] toegevoegd, wordt het volgende bericht weergegeven:
* **Admins**: De eigenschap PersonID is vereist voor deze analyse. Voeg een persoon-id toe aan de gegevensweergave.
* **Niet-beheerders**: De eigenschap PersonID is vereist voor deze analyse. Werk samen met de beheerder van de Customer Journey Analytics om persoon-id toe te voegen aan de gegevensweergave.

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Wrijvingsexploratie**: Als u een steile druppel vindt in het dialoogvenster [Wrijving](friction.md) in deze weergave kunt u een segment van die gebruikers maken en het segment toepassen om mogelijke oorzaken te onderzoeken.
* **Foutgedrag**: Als gebruikers een productfout tegenkomen, kunt u nagaan wat gebruikers deden voor of na het zien van die fout.
* **Validatie van gegevensverzameling**: De beheerders van gegevens kunnen deze mening aan hun eigen identiteitskaart van de Persoon filtreren, en het gebruiken om te bevestigen dat de implementatie van uw organisatie zoals verwacht werkt.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Property]**: De eigenschap waarvoor u gestreamde waarden wilt weergeven. In het midden van de stream worden waarden voor de geselecteerde eigenschap weergegeven. U kunt filters ook toepassen om de stream te beperken tot meer releasegegevens. Geldige operatoren voor het filter zijn [!UICONTROL Equals], [!UICONTROL Does not equal], [!UICONTROL Starts with], [!UICONTROL Ends with], [!UICONTROL Contains], [!UICONTROL Does not contain], [!UICONTROL Exists], en [!UICONTROL Does not exist].
* **[!UICONTROL Segments]**: Het segment dat u wilt analyseren. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen. Als u de weergave wilt beperken tot een specifieke persoon-id, kunt u hier filteren op die persoon-id. Eén segment wordt ondersteund voor deze weergave.

## Diagraminstellingen

De [!UICONTROL Timeline] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Show as]**: Geeft de gewenste eigenschapswaarden weer.
   * [!UICONTROL Show all]: Alle eigenschapswaarden in een sessie tonen.
   * [!UICONTROL Highlight]: Markeer visueel de eigenschapswaarden in een sessie die overeenkomen met de queryfilters.
   * [!UICONTROL View only]: Alleen de eigenschapswaarden weergeven in een sessie die overeenkomt met de queryfilters.

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarop u trendgegevens wilt bekijken. Deze instelling heeft geen invloed op niet-trendweergaven, zoals de tijdlijn.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
