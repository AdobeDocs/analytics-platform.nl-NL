---
title: Effectanalyse vrijgeven
description: Vergelijk de prestaties in gelijke perioden vóór en na de release.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: 93e6e4f1-bbe4-4a6c-8ec3-54d1f9a8b847
role: User
source-git-commit: d492220eaf12242a870f3826b31edd3d1ea99a3b
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# [!UICONTROL Release impact] analyse {#release-impact}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_workspace_guidedanalysis_releaseimpact_button"
>title="Geen effect"
>abstract="Vergelijk de prestaties in gelijke perioden vóór en na de release."

<!-- markdownlint-enable MD034 -->

De ![ 2} analyse van de Versie ](/help/assets/icons/Release.svg) {toont een vergelijking van hoe de belangrijkste indicatoren vóór en na een bepaalde datum presteerden. **[!UICONTROL Release impact]** De horizontale as van dit rapport is een tijdinterval, terwijl de verticale as de gewenste belangrijkste indicatoren meet. Een verticale balk in het midden van het diagram geeft de datum aan die u voor en na wilt vergelijken. Deze datum is doorgaans een opmerkelijke wijziging van het product waarop u wilt meten, zoals een update van het product of het starten van de campagne.

>[!VIDEO](https://video.tv.adobe.com/v/3421665/?learn=on)

## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **Algemene prestatiesevaluatie:** het vergelijken van algemene zeer belangrijke indicatoren, zoals betrokkenheidsmaatregelen, kan u helpen bepalen als een bepaalde versie algemeen succesvol was.
* **Controle**: De vitale metriek van het spoor die u zou verwachten om vlak te blijven wanneer de veranderingen, zoals ladingstijd of aantal logins worden aangebracht. Gebruik deze analyse om ze voor en na een release te vergelijken om er zeker van te zijn dat het geen onbedoelde gevolgen had.
* **Goedkeuring van de Eigenschap**: Als een productupdate op het verbeteren van een bepaalde eigenschap wordt geconcentreerd, kunt u deze analyse gebruiken om het gebruik van die eigenschap vóór en na de productupdate direct te vergelijken.
* **opsporing van het insect**: Het volgen van het aantal fouten vóór en na een versie kan een vroege indicator van klantenkwesties verstrekken. Als u onmiddellijk na een release een toename van fouten opmerkt, kunt u samenwerken met ontwikkelingsteams of ontwikkelingsteams om het probleem te identificeren en te verhelpen, zodat de klant niet meer te lijden krijgt.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen deze analyse en [ Eerste gebruikseffect ](first-use-impact.md).
* **[!UICONTROL Key indicators]**: De gebeurtenissen die u per gebruiker wilt meten. Elke geselecteerde toetsindicator wordt weergegeven als een gekleurde lijn. Aan de tabel wordt een rij toegevoegd die de gebeurtenis vertegenwoordigt. U kunt maximaal drie gebeurtenissen opnemen.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. De opties zijn [!UICONTROL Events per user] , [!UICONTROL Percentage of users] , [!UICONTROL Events] , [!UICONTROL Sessions] en [!UICONTROL Users] .
* **[!UICONTROL Factors]**: De datum die u voor en na wilt vergelijken.
* **[!UICONTROL Segments]**: Het segment dat u wilt meten. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen.

### Diagraminstellingen

De [!UICONTROL Release impact] -analyse biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. De opties zijn [!UICONTROL Line] en [!UICONTROL Bar] .

### Datumbereik

De datum waarop de effectanalyse wordt geselecteerd, is anders dan de andere analyses, aangezien het verslag betrekking heeft op de datum die in de vraagspoorlijn is gespecificeerd. De volgende opties zijn beschikbaar:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Geldige opties zijn [!UICONTROL Daily] , [!UICONTROL Weekly] , [!UICONTROL Monthly] en [!UICONTROL Quarterly] . Het wijzigen van het interval heeft invloed op de opties die beschikbaar zijn voor de periode Voor en Na.
* **[!UICONTROL Before and after period]**: De hoeveelheid tijd die moet worden geanalyseerd voor en na de datum die is opgegeven in de querytrack. Welke opties beschikbaar zijn, is afhankelijk van de selectie van [!UICONTROL Interval] .


<!--
## Example

See below for an example of the analysis.

![Release impact](../assets/release-impact.png)

-->
