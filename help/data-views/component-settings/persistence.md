---
title: Instellingen voor persistentiecomponenten
description: Bepaal hoe of of de waarden van de afmeting van één gebeurtenis aan volgende blijven.
exl-id: b8b234c6-a7d9-40e9-8380-1db09610b941
source-git-commit: af357167e65f4a577880832818221f6edbfc8b0a
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 6%

---


# Instellingen voor persistentiecomponenten

Persistentie is de capaciteit voor een bepaalde afmetingswaarde om op metrisch voorbij de gebeurtenis betrekking te hebben het wordt geplaatst. Er wordt een combinatie van toewijzing en vervaldatum gebruikt.

* **Met** toewijzingen kunt u bepalen welke waarde wordt behouden wanneer meerdere dimensie-items tegelijk in één kolom kunnen blijven staan.
* **Met** Verlopen kunt u bepalen hoe lang een dimensie-item zich na de gebeurtenis bevindt waarop het is ingesteld.

Persistentie is alleen beschikbaar voor dimensies en is retroactief voor de gegevens waarop deze wordt toegepast. Het is een directe gegevenstransformatie die gebeurt alvorens het filtreren of andere analyseverrichtingen worden toegepast.

![Persistentie](../assets/persistence.png)

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Set persistence] | Laat persistentie voor de dimensie toe. Als persistentie niet is ingeschakeld, heeft de dimensie alleen betrekking op metriek die in dezelfde gebeurtenis bestaan. Deze instelling is standaard uitgeschakeld. |
| [!UICONTROL Allocation] | Hier kunt u het toewijzingsmodel opgeven dat wordt gebruikt voor een dimensie voor persistentie. De opties zijn: [!UICONTROL Most recent], [!UICONTROL Original], [!UICONTROL Instance], [!UICONTROL All]. |
| [!UICONTROL Expiration] | Hier geeft u het venster voor persistentie voor een dimensie op. De opties zijn: [!UICONTROL Session] (standaardwaarde), [!UICONTROL Person], [!UICONTROL Custom Time], [!UICONTROL Metric]. Mogelijk moet u de afmeting van een aankoop kunnen verlopen (zoals interne zoektermen of andere gevallen waarin u zaken voor koopwaar gebruikt). De maximale vervaltijd die u kunt instellen, is 90 dagen. Als u een toewijzing van [!UICONTROL All] selecteert, is slechts [!UICONTROL Session] of [!UICONTROL Person] afloop beschikbaar. |

## Toewijzingsinstellingen

Details over de beschikbare toewijzingsinstellingen.

* **Recentste versie**: Hiermee blijft de meest recente (door tijdstempel) waarde in de dimensie behouden. Alle volgende waarden die binnen de afloopperiode van de dimensie voorkomen, vervangen de eerder blijkende waarde. Als &quot;Geen waarde behandelen&quot; als een waarde&quot; is ingeschakeld op deze dimensie onder [Geen waardeopties](no-value-options.md), overschrijven lege waarden eerder aanhouden waarden. Neem bijvoorbeeld de volgende tabel met de toewijzing [!UICONTROL Most recent] en de vervaldatum [!UICONTROL Session]:

   | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
   | --- | --- | --- | --- | --- | --- |
   | Waarden gegevensset |  | C | B |  | A |
   | Meest recente toewijzing |  | C | B | B | A |

* **Origineel**: Houdt de oorspronkelijke waarde door timestamp in de dimensie voor de duur van de vervalperiode aanwezig. Als deze dimensie een waarde heeft, wordt deze niet overschreven wanneer een andere waarde wordt waargenomen bij een volgende gebeurtenis. Neem bijvoorbeeld de volgende tabel met de toewijzing [!UICONTROL Original] en de vervaldatum [!UICONTROL Session]:

   | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
   | --- | --- | --- | --- | --- | --- |
   | Waarden gegevensset |  | C | B |  | A |
   | Oorspronkelijke toewijzing |  | C | C | C | C |

* **Alles**: Deze methode werkt op dezelfde manier als het  [!UICONTROL Participation] attributiemodel voor metriek. Hiermee worden alle waarden op gelijke wijze gehandhaafd, zodat elke waarde bij rapportage volledige creditering voor de maatstaf krijgt. Neem bijvoorbeeld de volgende tabel met de toewijzing [!UICONTROL All] en de vervaldatum [!UICONTROL Session]:

   | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
   | --- | --- | --- | --- | --- | --- |
   | Waarden gegevensset | A | B | C |  | A |
   | Alle toewijzingen | A | A,B | A, B, C | A, B, C | A, B, C |

## Expiratie-instellingen

Details over de beschikbare vervalinstellingen.

* **Sessie**: Verloopt na een bepaalde sessie. Standaardvervalvenster.
* **Persoon**: Verloopt aan het einde van het rapportagevenster.
* **Tijd**: U kunt de waarde van de dimensie instellen op verlopen na een opgegeven periode (maximaal 90 dagen). Deze optie voor verlopen is alleen beschikbaar voor de toewijzingsmodellen Origineel en Recentste. Wanneer u op tijd gebaseerde vervaldatums gebruikt, worden waarden vóór het begin van het rapportagevenster (maximaal 90 dagen) in overweging genomen.
* **Metrisch**: Wanneer dit metrisch in een klap wordt gezien, onmiddellijk verlopen de persisted waarde in de afmeting. U kunt elke gewenste metrische waarde gebruiken als eindwaarde voor de vervaldatum voor deze dimensie. Deze optie voor verlopen is alleen beschikbaar voor de instellingen Origineel en Recentste toewijzing.
