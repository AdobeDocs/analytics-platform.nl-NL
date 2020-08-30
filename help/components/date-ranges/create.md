---
title: Een datumbereik maken
description: Creeer een datumwaaier voor gebruik in rapportering.
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---


# Een datumbereik maken

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U kunt een waaier van de douanedatum tot stand brengen gebruikend één van beiden van de volgende twee methodes:

* Direct in een werkruimteproject door te klikken &quot;`+`&#39; knoop naast de lijst van de componenten van de datumwaaier op de linkerzijde
* Binnen de datumbereikmanager

Om een datumwaaier in de manager van de datumwaaier tot stand te brengen:

1. Aanmelden bij [Analytics.adobe.com](https://analytics.adobe.com) het gebruiken van uw geloofsbrieven van AdobeID.
1. Ga naar [!UICONTROL Components] > [!UICONTROL Date Ranges].
1. Klik op de [!UICONTROL Add] knoop om het modale venster te openen dat tot een datumwaaier leidt.

## Creeer een modaal venster van het datumbereik

Het modaal venster heeft vier gebieden u kunt uitgeven:

* **Datumbereik**: De datumwaaier u voor deze component wilt.
* **Titel**: De naam u voor deze component wilt. De titel wordt gebruikt in werkruimteprojecten.
* **Beschrijving**: De beschrijving u voor deze component wilt. De beschrijving wordt gezien wanneer het klikken van ![i](../assets/i.png) pictogram.
* **Labels**: Gebruik tags om de datumbereiken te ordenen. Een datumwaaier kan tot veelvoudige markeringen behoren.

## Een datumbereik selecteren

Wanneer het klikken van de datumwaaier in het modale venster, hebt u verscheidene opties:

* **Agenda**: Selecteer de begin- en einddatum.
* **Roldatums gebruiken**: Controleer deze doos als u de datumwaaier wilt veranderen aangezien de tijd verdergaat. Controleer deze doos niet als u uw datumwaaier statisch wilt blijven.
* **Voorinstelling selecteren**: Gebruik deze dropdown als u een waaier wilt van de douanedatum die op een waaier wordt gebaseerd die Adobe door gebrek aanbiedt. Wanneer u vooraf ingesteld selecteert, kunt u de datumwaaier verder aanpassen om uw behoeften aan te passen. Het beïnvloedt vooraf ingesteld niet dat Adobe aanbiedt.

## Roldatumbereik

Als u een het rollen datumwaaier wilt, kunt u aanpassen wanneer het rolt. U kunt controleren wanneer de begin en einddatums onafhankelijk van elkaar rollen.

* **Wanneer de datum begint**: Kies als de datum aan het begin van een tijdspanne, aan het eind van een tijdspanne begint, of gebruik een vaste dag.
* **De periode waarin**: Kies hoe vaak de datumwaaier rollen. Je kunt het elke dag laten rollen, elke week, elke maand, elk kwartaal, of elk jaar.
* **Compensatie**: Kies de compensatie van de datumwaaier. U kunt dagen, weken, maanden, kwartalen of jaren toevoegen of aftrekken.

## Voorbeelden van roldatums

Sommige datumwaaiers kunnen in bepaalde rapporten nuttig zijn.

Tot op heden jaar:

```text
Start: Start of current year
End: End of current day
```

Afgelopen donderdag tot donderdag:

```text
Start: Start of current week minus 3 days
End: Start of current week plus 4 days
```

Begrotingsjaar (bijvoorbeeld indien een boekjaar in december begint)

```text
Start: Start of current year minus 1 month
End: End of current year minus 1 month
```
