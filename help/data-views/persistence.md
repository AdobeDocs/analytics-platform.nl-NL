---
title: Wat is dimensie persistentie in Customer Journey Analytics?
description: Dimension persistentie is een combinatie van allocatie en vervaldatum. Samen bepalen zij hoe of of de waarden van de afmeting van de ene gebeurtenis naar de volgende blijven.
exl-id: b8b234c6-a7d9-40e9-8380-1db09610b941
translation-type: tm+mt
source-git-commit: 7370caf3495ff707698022889bf17528582da803
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 5%

---

# Persistentie

Dimension persistentie is een combinatie van allocatie en vervaldatum. Samen bepalen zij hoe of of de waarden van de afmeting van de ene gebeurtenis naar de volgende blijven. De persistentie van Dimension wordt gevormd op een afmeting binnen de Mening van Gegevens en is retroactief en niet-destructief aan de gegevens het wordt toegepast op. Dimension persistentie is een directe gegevenstransformatie die wordt toegepast op een dimensie die optreedt voordat filtering of andere analysebewerkingen worden uitgevoerd in de rapportage.

* Standaard is voor een waarde van een dimensie geen persistentie ingeschakeld.
* Wanneer een toewijzingsmodel standaard is ingeschakeld voor een dimensie, wordt een vervaldatum van [!UICONTROL Session] gebruikt.

## Toewijzing

Toewijzing past een transformatie toe op de onderliggende waarde die u gebruikt. Tot de ondersteunde toewijzingsmodellen behoren:

* Meest recent
* Origineel
* Alle

### [!UICONTROL Most recent] toewijzing

De meest recente toewijzing blijft de meest recente (door tijdstempel) waarde in de dimensie. De waarden die daarna in dezelfde sessie worden weergegeven, vervangen de waarde die eerder doorloopt. Als &quot;Geen waarde behandelen&quot; is geselecteerd op deze dimensie, worden de lege waarden vervangen door &quot;Geen waarde&quot; voordat persistentie wordt toegepast. Hier is een voor en na voorbeeld van [!UICONTROL Most recent] toewijzing die veronderstelt [!UICONTROL Session] voor vervaldatum wordt gebruikt en alle gebeurtenissen binnen [!UICONTROL Session] voorkomen:

| Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
| --- | --- | --- | --- | --- | --- |
| gegevenssetwaarden |  | C | B |  | A |
| Meest recente toewijzing |  | C | B | B | A |

### [!UICONTROL Original] toewijzing

De oorspronkelijke toewijzing blijft de oorspronkelijke waarde (in tijdstempel) binnen de dimensie gedurende een verloopperiode behouden. Hier volgt een voor-en-na voorbeeld van [!UICONTROL Original]-toewijzing:

| Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
| --- | --- | --- | --- | --- | --- |
| gegevenssetwaarden |  | C | B |  | A |
| Oorspronkelijke toewijzing |  | C | C | C | C |

### [!UICONTROL All] toewijzing

Deze dimensietoewijzing kan op zowel op serie-gebaseerde dimensies of enig-waardedimensies worden toegepast. Het werkt op dezelfde manier als het [!UICONTROL Participation] attributiemodel voor metriek. Een belangrijk verschil is dat dimensies met All-toewijzing kunnen worden gebruikt in filterdefinities. Stel dat er 5 gebeurtenissen zijn in een tekenreeksveld, waarbij de toewijzing is ingesteld op Alles en de vervaldatum op 5 minuten:

| Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
| --- | --- | --- | --- | --- | --- |
| gegevenssetwaarden | A | B | C |  | A |
| ná persistentie | A | A,B | A, B, C | A, B, C | A, B, C |

## Verlopen

[!UICONTROL Expiration] Hiermee kunt u het persistentievenster voor een dimensie opgeven.

Er zijn vier manieren om een afmetingswaarde te verlopen:

* Sessie (standaard): Verloopt na een bepaalde sessie.
* Persoon: Verloopt aan het einde van het rapportagevenster.
* Tijd: U kunt de waarde van de dimensie instellen op verlopen na een opgegeven tijdsperiode of gebeurtenis. Deze optie voor verlopen is alleen beschikbaar voor de toewijzingsmodellen Origineel en Recentste.
* Metrisch: U kunt om het even welke bepaalde metriek als het afloopeind voor deze afmeting specificeren (b.v. metrisch &quot;van de Aankoop&quot;). Deze vervaldatum is alleen beschikbaar voor oorspronkelijke en meest recente toewijzingsmodellen.

### Wat is het verschil tussen Toewijzing en Attributie?

**Toewijzing**: Beschouw toewijzing als een gegevenstransformatie naar de dimensie. Toewijzing vindt plaats voordat wordt gefilterd. Als u een filter maakt, zal dit wegvallen van de getransformeerde dimensie.

**Attributie**: Hoe verdeel ik het krediet van metrisch aan de dimensie die het wordt toegepast? Attributie is geen gegevenstransformatie, wordt toegepast tijdens gegevensaggregatie en heeft geen invloed op welke gegevens worden opgenomen met een filter.
