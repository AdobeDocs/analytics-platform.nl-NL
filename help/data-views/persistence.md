---
title: Wat is dimensie persistentie in Customer Journey Analytics?
description: Dimension persistentie is een combinatie van allocatie en vervaldatum. Samen bepalen ze welke waarden voor dimensies behouden blijven.
exl-id: b8b234c6-a7d9-40e9-8380-1db09610b941
translation-type: tm+mt
source-git-commit: 16e43f5d938ac25445f382e5eba8fc12e0e67161
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 12%

---

# Persistentie

Dimension persistentie is een combinatie van allocatie en vervaldatum. Samen bepalen ze welke waarden voor dimensies behouden blijven. Adobe adviseert hoogst dat u binnen uw organisatie bespreekt hoe de veelvoudige waarden voor elke afmeting (toewijzing) worden behandeld en wanneer de afmetingswaarden het persisteren van gegevens (afloop) tegenhouden.

* Standaard gebruikt een afmetingswaarde [WAT?] toewijzing.
* Een waarde voor de dimensie gebruikt standaard de vervaldatum [!UICONTROL Session].

## Toewijzing

Toewijzing past een transformatie toe op de onderliggende waarde die u gebruikt. Tot de ondersteunde toewijzingsmodellen behoren:

* Meest recent
* Origineel
* Alle
* Eerste gekend
* Laatst bekend

### [!UICONTROL Most recent] toewijzing

Hier volgt een voor-en-na voorbeeld van [!UICONTROL Most recent]-toewijzing:

| Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
| --- | --- | --- | --- | --- | --- |
| tijdstempel (min) | 1 | 2 | 3 | 6 | 7 |
| oorspronkelijke waarden |  | C | B |  | A |
| Meest recente toewijzing |  | C | B | B | A |

### [!UICONTROL Original] toewijzing

Hier volgt een voor-en-na voorbeeld van [!UICONTROL Original]-toewijzing:

| Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
| --- | --- | --- | --- | --- | --- |
| tijdstempel (min) | 1 | 2 | 1 | 6 | 7 |
| oorspronkelijke waarden |  | C | B |  | A |
| Oorspronkelijke toewijzing |  | C | C | C | C |

### [!UICONTROL All] toewijzing

Deze nieuwe dimensie-toewijzing kan op zowel op serie-gebaseerde dimensies als enig-waardedimensies worden toegepast. Het werkt op dezelfde manier als het [!UICONTROL Participation] attributiemodel voor metriek. Het verschil is dat afzonderlijke waarden in het veld op verschillende punten kunnen verlopen. Stel dat er 5 gebeurtenissen zijn in een tekenreeksveld, waarbij de toewijzing is ingesteld op Alles en de vervaldatum op 5 minuten. Het volgende gedrag wordt verwacht:

| Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
| --- | --- | --- | --- | --- | --- |
| tijdstempel (min) | 3 | 2 | 3 | 6 | 7 |
| oorspronkelijke waarden | A | B | C |  | A |
| ná persistentie | A | A,B | A, B, C | B,C | A,C |

U ziet dat de waarde van A aanhoudt tot de markering van 5 minuten is bereikt, terwijl B en C aanhouden tot Actief 4 omdat er nog geen 5 minuten zijn verstreken voor die waarden. Merk op dat deze toewijzing tot een multi-getaxeerde dimensie van een enig-getaxeerd gebied zal leiden. Dit model moet ook op arraygebaseerde afmetingen worden ondersteund:

| Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
| --- | --- | --- | --- | --- | --- |
| tijdstempel (min) | 3 | 2 | 3 | 6 | 7 |
| oorspronkelijke waarden | A,B | C | B,C |  | A |
| ná persistentie | A,B | A, B, C | A, B, C | B,C | A, B, C |

### &quot;First Known&quot; en &quot;Last Known&quot; toewijzingen

Deze twee nieuwe toewijzingsmodellen nemen de eerste of laatste waargenomen waarde voor een dimensie binnen een gespecificeerd persistentiegereik (zitting, persoon, of douanetijdspanne met raadpleging) en passen het op alle gebeurtenissen binnen het gespecificeerde werkingsgebied toe. Voorbeeld:

| Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
| --- | --- | --- | --- | --- | --- |
| tijdstempel (min) | 1 | 2 | 3 | 6 | 7 |
| oorspronkelijke waarden |  | C | B |  | A |
| eerste gekend | C | C | C | C | C |
| laatst gekend | A | A | A | A | A |

De eerste of laatst bekende waarden kunnen worden toegepast op alleen een sessie of op het bereik van de persoon (het rapportagevenster) of op een aangepast, of op tijd gebaseerd bereik (in feite een personenbereik met toegevoegd terugzoekvenster).

## Verlopen

[!UICONTROL Expiration] Hiermee kunt u het persistentievenster voor een dimensie opgeven.

Er zijn vier manieren om een afmetingswaarde te verlopen:

* Sessie (standaard): Verloopt na een bepaalde sessie.
* Persoon: ?
* Tijd: U kunt de waarde van de dimensie instellen op verlopen na een opgegeven tijdsperiode of gebeurtenis.
* Metrisch: U kunt om het even welke bepaalde metriek als het afloopeind voor deze afmeting specificeren (b.v. metrisch &quot;van de Aankoop&quot;).
* Aangepast:

### Wat is het verschil tussen Toewijzing en Attributie?

**Toewijzing**: Denk aan toewijzing als &quot;gegevenstransformatie&quot; van de dimensie. Toewijzing vindt plaats voordat wordt gefilterd. Als u een filter maakt, zal dit wegvallen van de getransformeerde dimensie.

**Attributie**: Hoe verdeel ik het krediet van metrisch aan de dimensie die het wordt toegepast? Attributie vindt plaats na het filteren.
