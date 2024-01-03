---
title: Een datumbereik maken
description: Maak een datumbereik voor rapportage.
feature: Calendar
exl-id: 3e4fa3cc-c14b-45e5-afbb-518ecfa0033e
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Een datumbereik maken

U kunt een datumbereik maken met een van de volgende twee methoden:

* Rechtstreeks in een werkruimteproject door op de knop &quot;`+`&#39;, naast de lijst met componenten voor het datumbereik aan de linkerkant
* Binnen de datumbereikmanager

U kunt als volgt een datumbereik maken in de datumbereikmanager:

1. Aanmelden bij [analytics.adobe.com](https://analytics.adobe.com) met uw Adobe-id-referenties.
1. Ga naar [!UICONTROL Components] > [!UICONTROL Date Ranges].
1. Klik op de knop [!UICONTROL Add] om het modale venster te openen waarin een datumbereik wordt gemaakt.

## Een modaal venster voor een datumbereik maken

Het modale venster heeft vier velden die u kunt bewerken:

* **Datumbereik**: Het datumbereik dat u voor deze component wilt gebruiken.
* **Titel**: De naam die u voor deze component wilt gebruiken. De titel wordt gebruikt in werkruimteprojecten.
* **Beschrijving**: De beschrijving die u voor deze component wilt gebruiken. De beschrijving is zichtbaar wanneer u op de knop ![i](../assets/i.png) pictogram.
* **Tags**: Gebruik labels om de datumbereiken te ordenen. Een datumbereik kan tot meerdere tags behoren.

## Een datumbereik selecteren

Als u in het modale venster op het datumbereik klikt, hebt u verschillende opties:

* **Kalender**: Selecteer de begin- en einddatum.
* **Roldatums gebruiken**: Schakel dit selectievakje in als u wilt dat het datumbereik wordt gewijzigd terwijl de tijd doorgaat. Schakel dit selectievakje niet in als u wilt dat het datumbereik statisch blijft.
* **Voorinstelling selecteren**: Gebruik deze vervolgkeuzelijst als u een aangepast datumbereik wilt dat is gebaseerd op een bereik dat standaard door de Adobe wordt aangeboden. Wanneer u een voorinstelling selecteert, kunt u het datumbereik verder aanpassen aan uw wensen. Dit heeft geen invloed op de voorinstelling die Adobe biedt.

## Roldatumbereiken

Als u een het rollen datumwaaier wilt, kunt u aanpassen wanneer het rolt. U kunt bepalen wanneer de begin- en einddatum onafhankelijk van elkaar worden verschoven.

* **Wanneer de datum begint**: Kies of de datum begint aan het begin van een tijdsperiode, aan het einde van een tijdsperiode of gebruik een vaste dag.
* **De gebruiksperiode**: Kies hoe vaak het datumbereik wordt verschoven. Je kunt het elke dag laten rollen, elke week, elke maand, elk kwartaal, of elk jaar.
* **Verschuiven**: Kies de verschuiving van het datumbereik. U kunt dagen, weken, maanden, kwarten of jaren toevoegen of verwijderen.

## Voorbeelden van roldatums

Sommige datumbereiken zijn handig in bepaalde rapporten.

Jaarlijks:

```text
Start: Start of current year
End: End of current day
```

Afgelopen donderdag tot en met donderdag:

```text
Start: Start of current week minus 3 days
End: Start of current week plus 4 days
```

Begrotingsjaar (bijvoorbeeld wanneer een boekjaar in december begint)

```text
Start: Start of current year minus 1 month
End: End of current year minus 1 month
```
