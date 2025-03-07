---
title: Wat is de Report Builder Hub in Customer Journey Analytics
description: Beschrijft de componenten van de Hub van Report Builder
role: User
feature: Report Builder
type: Documentation
exl-id: 119bd0b5-0d07-407f-b6e9-ef43352bad31
solution: Customer Journey Analytics
source-git-commit: bd2d45b9fc1380e36fc482ee75e1a9bbb26f6cf7
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Report Builder Hub

Met de Report Builder-hub kunt u gegevensblokken maken, bijwerken, verwijderen en beheren.

De Report Builder-hub bevat de knoppen Maken en Beheren, de lijst OPDRACHTEN en de deelvensters SNEL BEWERKEN.

<img src="./assets/hub51.png" width="50%" alt="Report Builder Hub"/>


## Knoppen maken en beheren

Met de knoppen Maken of Beheren kunt u nieuwe gegevensblokken maken of bestaande gegevensblokken beheren.

## Deelvenster OPDRACHTEN

Gebruik het deelvenster OPDRACHTEN voor toegang tot opdrachten die compatibel zijn met de geselecteerde cellen of een vorige handeling.

![ het paneel van Bevelen in de Hub van de Bouwer van het Rapport ](./assets/hub1.png)

### Opdrachten

| Weergegeven opdrachten | Beschikbaar als... | Doel |
|------|------------------|--------|
| Gegevensblok maken | Één of meerdere cellen wordt geselecteerd in het werkboek. | Wordt gebruikt om een gegevensblok te maken |
| Gegevensblok bewerken | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Wordt gebruikt om een gegevensblok te bewerken |
| Gegevensblok vernieuwen | De selectie bevat ten minste één gegevensblok. De opdracht vernieuwt alleen de gegevensblokken in de selectie. | Wordt gebruikt om een of meer gegevensblokken te vernieuwen |
| Alle gegevensblokken vernieuwen | Het werkboek bevat één of meerdere gegevensblokken. | Gebruikt om ALLE gegevensblokken in het werkboek te verfrissen |
| Gegevensblok kopiëren | De geselecteerde cel of het geselecteerde celbereik maakt deel uit van een of meer gegevensblokken. | Wordt gebruikt om een gegevensblok te kopiëren |
| Gegevensblok verwijderen | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Wordt gebruikt om een gegevensblok te verwijderen |

## Deelvenster SNEL BEWERKEN

Wanneer u een of meer gegevensblokken in een spreadsheet selecteert, geeft Report Builder het deelvenster SNEL BEWERKEN weer. U kunt het deelvenster SNEL BEWERKEN gebruiken om parameters in één gegevensblok te wijzigen of om parameters in meerdere gegevensblokken tegelijk te wijzigen.

![ Snel geeft paneel in Report Builder uit ](./assets/hub2.png)

De wijzigingen die u hebt aangebracht met de secties Snel bewerken zijn van toepassing op alle geselecteerde gegevensblokken.

### Gegevensweergaven

Gegevensblokken trekken gegevens uit een geselecteerde gegevensweergave. Als de veelvoudige gegevensblokken in een aantekenvel worden geselecteerd en zij trekken geen gegevens van de zelfde gegevensmening, de **verbindingsvertoningen van de meningen van Gegevens *Veelvoud*.**

Wanneer u de gegevensweergave wijzigt, nemen alle gegevensblokken in de selectie de nieuwe gegevensweergave over. Componenten in het gegevensblok komen overeen met de nieuwe gegevensweergave op basis van bijvoorbeeld de id die overeenkomt met ```evars``` . Als een component niet in een gegevensblok wordt gevonden, wordt een waarschuwingsbericht getoond en de component wordt verwijderd uit het gegevensblok.

Als u de gegevensweergave wilt wijzigen, selecteert u een nieuwe gegevensweergave in het keuzemenu.

![ de Hub van Report Builder die het drop-down menu van de gegevensmening toont.](./assets/image16.png)

### Datumbereik

**waaier van de Datum** toont de datumwaaier voor de geselecteerde gegevensblokken. Als de veelvoudige gegevensblokken met veelvoudige datumwaaiers worden geselecteerd, de **verbindingsvertoningen van de waaier van de Datum** *Veelvoud*.

### Segmenten

De **verbinding van Segmenten** toont een summiere lijst van de segmenten die door de geselecteerde gegevensblokken worden gebruikt. Als de veelvoudige gegevensblokken met veelvoudige toegepaste segmenten worden geselecteerd, de **verbindingsvertoningen van segmenten *Veelvoudig*.**
