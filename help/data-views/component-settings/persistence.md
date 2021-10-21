---
title: Instellingen voor persistentiecomponenten
description: Bepaal hoe of of de waarden van de afmeting van één gebeurtenis aan volgende blijven.
exl-id: b8b234c6-a7d9-40e9-8380-1db09610b941
source-git-commit: e8f372692e60158ce7f30837ee4da0f922e1d752
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 6%

---


# [!UICONTROL Persistence] componentinstellingen

[!UICONTROL Persistence] is de capaciteit voor een bepaalde afmetingswaarde om op metrisch voorbij de gebeurtenis betrekking te hebben het wordt geplaatst. Er wordt een combinatie van toewijzing en vervaldatum gebruikt.

* **Toewijzing** Hiermee kunt u bepalen welke waarde wordt behouden wanneer meer dan één dimensie-item tegelijk in één kolom kan blijven bestaan.
* **Verlopen** laat u bepalen hoe lang een afmetingspunt voorbij de gebeurtenis voortduurt het wordt geplaatst.

[!UICONTROL Persistence] is alleen beschikbaar voor dimensies en is retroactief voor de gegevens waarop deze worden toegepast. Het is een directe gegevenstransformatie die gebeurt alvorens het filtreren of andere analyseverrichtingen worden toegepast.

![Persistentie](../assets/persistence.png)

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Set persistence] | Laat persistentie voor de dimensie toe. Als persistentie niet is ingeschakeld, heeft de dimensie alleen betrekking op metriek die in dezelfde gebeurtenis bestaan. Deze instelling is standaard uitgeschakeld. |
| [!UICONTROL Allocation] | Hier kunt u het toewijzingsmodel opgeven dat wordt gebruikt voor een dimensie voor persistentie. De opties zijn: [!UICONTROL Most recent], [!UICONTROL Original], [!UICONTROL Instance], [!UICONTROL All]. Vanaf 28 oktober 2021 wordt een terugzoekvenster van maximaal 90 dagen toegevoegd aan de [!UICONTROL Allocation] instellen. |
| [!UICONTROL Expiration] | Hier geeft u het venster voor persistentie voor een dimensie op. De opties zijn: [!UICONTROL Session] (standaard), [!UICONTROL Person], [!UICONTROL Custom Time], [!UICONTROL Metric]. Mogelijk moet u de afmeting van een aankoop kunnen verlopen (zoals interne zoektermen of andere gevallen waarin u zaken voor koopwaar gebruikt). De maximale vervaltijd die u kunt instellen, is 90 dagen. Als u een toewijzing van [!UICONTROL All], alleen [!UICONTROL Session] of [!UICONTROL Person] verlopen is beschikbaar. |

## [!UICONTROL Allocation] instellingen

Details over de beschikbare toewijzingsinstellingen.

* **[!UICONTROL Most Recent]**: Hiermee blijft de meest recente (door tijdstempel) waarde in de dimensie behouden. Alle volgende waarden die binnen de afloopperiode van de dimensie voorkomen, vervangen de eerder blijkende waarde. Als &quot;Geen waarde behandelen&quot; is ingeschakeld voor deze dimensie onder [Geen waardeopties](no-value-options.md)Lege waarden overschrijven eerder persistente waarden. Neem bijvoorbeeld de volgende tabel met [!UICONTROL Most recent] toewijzing en [!UICONTROL Session] vervaldatum:

   | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
   | --- | --- | --- | --- | --- | --- |
   | Waarden gegevensset |  | C | B |  | A |
   | Meest recente toewijzing |  | C | B | B | A |

* **[!UICONTROL Original]**: Houdt de oorspronkelijke waarde door timestamp in de dimensie voor de duur van de vervalperiode aanwezig. Als deze dimensie een waarde heeft, wordt deze niet overschreven wanneer een andere waarde wordt waargenomen bij een volgende gebeurtenis. Neem bijvoorbeeld de volgende tabel met [!UICONTROL Original] toewijzing en [!UICONTROL Session] vervaldatum:

   | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
   | --- | --- | --- | --- | --- | --- |
   | Waarden gegevensset |  | C | B |  | A |
   | Oorspronkelijke toewijzing |  | C | C | C | C |

* **[!UICONTROL All]**: Handelingen die vergelijkbaar zijn met de [!UICONTROL Participation] attributiemodel voor metriek. Hiermee worden alle waarden op gelijke wijze gehandhaafd, zodat elke waarde bij rapportage volledige creditering voor de maatstaf krijgt. Neem bijvoorbeeld de volgende tabel met [!UICONTROL All] toewijzing en [!UICONTROL Session] vervaldatum:

   | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
   | --- | --- | --- | --- | --- | --- |
   | Waarden gegevensset | A | B | C |  | A |
   | Alle toewijzingen | A | A,B | A, B, C | A, B, C | A, B, C |

## [!UICONTROL Expiration] instellingen

Details over de beschikbare vervalinstellingen.

* **Sessie**: Verloopt na een bepaalde sessie. Standaardvervalvenster.
* **Persoon**: Verloopt aan het einde van het rapportagevenster.
* **Tijd**: U kunt de waarde van de dimensie instellen op verlopen na een opgegeven periode (maximaal 90 dagen). Deze optie voor verlopen is alleen beschikbaar voor de toewijzingsmodellen Origineel en Recentste. Wanneer u op tijd gebaseerde vervaldatums gebruikt, worden waarden vóór het begin van het rapportagevenster (maximaal 90 dagen) in overweging genomen.
* **Metrisch**: Wanneer dit metrisch in een klap wordt gezien, onmiddellijk verlopen de persisted waarde in de afmeting. U kunt elke gewenste metrische waarde gebruiken als eindwaarde voor de vervaldatum voor deze dimensie. Deze optie voor verlopen is alleen beschikbaar voor de instellingen Origineel en Recentste toewijzing.
