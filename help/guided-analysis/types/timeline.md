---
title: Tijdlijnweergave
description: Verken patronen in sessieactiviteiten.
feature: Guided Analysis
keywords: productanalyse
role: User
source-git-commit: ecdbe1b68aa0824bd9db4acefd3ef9059d9ac927
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# [!UICONTROL Timeline] weergave

De **[!UICONTROL Timeline]** in de weergave kunt u afzonderlijke sessies analyseren om te bepalen in welke patronen het gedrag voorkomt. Met de rechterrails kunt u de persoon-id selecteren die u wilt analyseren. In het middelste gebied worden de tijd, de waarde van de geselecteerde eigenschap en de duur voor elke gebeurtenis van die persoon weergegeven.

Voor deze analyse moet u de opdracht **[!UICONTROL Person ID]** standaardonderdeel voor [gegevensweergave](/help/data-views/component-reference.md#optional). Als u geen [!UICONTROL Person ID] aan de gegevensweergave wordt toegevoegd, wordt het volgende bericht weergegeven:

> De eigenschap PersonID is vereist voor deze analyse. Voeg PersonID toe aan de gegevensweergave.

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Wrijvingsexploratie**: Als u een steile druppel vindt in het dialoogvenster [Wrijving](friction.md) in deze weergave kunt u mogelijke oorzaken van die neerzetbewerking onderzoeken.
* **Foutgedrag**: Als gebruikers een fout in uw product tegenkomen, kunt u nagaan wat gebruikers voor of na het zien van die fout doen.
* **Validatie van gegevensverzameling**: Gegevensbeheerders kunnen deze weergave filteren om zichzelf te isoleren. Deze mening verstrekt een stevige manier om ervoor te zorgen dat de implementatie van uw organisatie zoals verwacht werkt.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Property]**: De eigenschap waarvoor u waarden wilt weergeven. De zittingsanalyse in het centrum toont waarden voor het bezit hier wordt geselecteerd dat. U kunt gegevens ook filteren op de geselecteerde eigenschap. Geldige operatoren voor het filter zijn [!UICONTROL Equals], [!UICONTROL Does not equal], [!UICONTROL Starts with], [!UICONTROL Ends with], [!UICONTROL Contains], [!UICONTROL Does not contain], [!UICONTROL Exists], en [!UICONTROL Does not exist].
* **[!UICONTROL Segments]**: Het segment dat u wilt meten. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen. Eén segment wordt ondersteund voor deze weergave.

## Diagraminstellingen

De [!UICONTROL Timeline] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Show as]**: geeft de gewenste eigenschapswaarden weer.
   * [!UICONTROL Show all]
   * [!UICONTROL Highlight]
   * [!UICONTROL View only]

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarop u trendgegevens wilt bekijken. Deze instelling heeft geen invloed op niet-trendweergaven, zoals de tijdlijn.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
