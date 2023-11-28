---
title: Instellingen voor persistentiecomponenten
description: Bepaal hoe of of de waarden van de afmeting van één gebeurtenis aan volgende blijven.
exl-id: b8b234c6-a7d9-40e9-8380-1db09610b941
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: c343a729de4cb13473a7acc04e837b5e5f69809b
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 6%

---


# [!UICONTROL Persistence] componentinstellingen

[!UICONTROL Persistence] is de capaciteit voor een bepaalde afmetingswaarde om op metrisch voorbij de gebeurtenis betrekking te hebben het wordt geplaatst. Er wordt een combinatie van toewijzing en vervaldatum gebruikt.

![Het venster met gegevensweergaven markeert de Persistentie-opties](../assets/persistence.png)

* **Toewijzing** Hiermee kunt u bepalen welke waarde wordt behouden wanneer meer dan één dimensie-item tegelijk in één kolom kan blijven bestaan.

  >[!NOTE]
  >
  >Als u een [niet-standaard toewijzingsmodel](/help/data-views/component-settings/attribution.md) de reeks op metrisch in een rapport, het attributiemodel negeert de toewijzing u op de afmeting voor het zelfde rapport plaatst.
  >
  >Als u echter een [volledige tabelexport](/help/analysis-workspace/export/export-cloud.md) waarbij meerdere dimensies zijn inbegrepen, blijven de toewijzingsmodellen die op elke dimensie worden toegepast, behouden.

* **Verlopen** laat u bepalen hoe lang een afmetingspunt voorbij de gebeurtenis voortduurt het wordt geplaatst.

[!UICONTROL Persistence] is alleen beschikbaar voor dimensies en is retroactief voor de gegevens waarop deze worden toegepast. Het is een directe gegevenstransformatie die gebeurt alvorens het filtreren of andere analyseverrichtingen worden toegepast.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Set persistence] | Laat persistentie voor de afmeting toe. Als persistentie niet is ingeschakeld, heeft de dimensie alleen betrekking op metriek die in dezelfde gebeurtenis bestaan. Deze instelling is standaard uitgeschakeld. |
| [!UICONTROL Allocation] | Hier kunt u het toewijzingsmodel opgeven dat wordt gebruikt voor een dimensie voor persistentie. De opties zijn: [!UICONTROL Most recent], [!UICONTROL Original], [!UICONTROL Instance], [!UICONTROL All]. Vanaf 28 oktober 2021 wordt een terugzoekvenster van maximaal 90 dagen toegevoegd aan de [!UICONTROL Allocation] instellen. |
| [!UICONTROL Expiration] | Hier geeft u het venster voor persistentie voor een dimensie op. De opties zijn: [!UICONTROL Session] (standaard), [!UICONTROL Person], [!UICONTROL Custom Time], [!UICONTROL Metric]. Mogelijk moet u de afmeting van een aankoop kunnen verlopen (zoals interne zoektermen of andere gevallen waarin u zaken voor koopwaar gebruikt). De maximale vervaltijd die u kunt instellen, is 90 dagen. Als u een toewijzing van [!UICONTROL All], alleen [!UICONTROL Session] of [!UICONTROL Person] verlopen is beschikbaar. |

{style="table-layout:auto"}

## [!UICONTROL Allocation] instellingen

Details over de beschikbare toewijzingsinstellingen.

* **[!UICONTROL Most Recent]**: de meest recente (door tijdstempel) waarde in de dimensie blijft behouden. Alle volgende waarden die binnen de afloopperiode van de dimensie voorkomen, vervangen de eerder blijkende waarde. Als &quot;Geen waarde behandelen&quot; is ingeschakeld voor deze dimensie onder [Geen waardeopties](no-value-options.md)Lege waarden overschrijven eerder persistente waarden. Neem bijvoorbeeld de volgende tabel met [!UICONTROL Most recent] toewijzing en [!UICONTROL Session] vervaldatum:

  | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Waarden voor gegevensset |  | C | B |  | A |
  | Meest recente toewijzing |  | C | B | B | A |

* **[!UICONTROL Original]**: Houdt de oorspronkelijke waarde door timestamp in de dimensie voor de duur van de vervalperiode. Als deze dimensie een waarde heeft, wordt deze niet overschreven wanneer een andere waarde wordt waargenomen bij een volgende gebeurtenis. Neem bijvoorbeeld de volgende tabel met [!UICONTROL Original] toewijzing en [!UICONTROL Session] vervaldatum:

  | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Waarden voor gegevensset |  | C | B |  | A |
  | Oorspronkelijke toewijzing |  | C | C | C | C |

* **[!UICONTROL All]**: Werkt op dezelfde manier als de [!UICONTROL Participation] attributiemodel voor metriek. Hiermee worden alle waarden op gelijke wijze gehandhaafd, zodat elke waarde bij rapportage volledige creditering voor de maatstaf krijgt. Neem bijvoorbeeld de volgende tabel met [!UICONTROL All] toewijzing en [!UICONTROL Session] vervaldatum:

  | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Waarden voor gegevensset | A | B | C |  | A |
  | Alle toewijzingen | A | A,B | A, B, C | A, B, C | A, B, C |

* **[!UICONTROL First Known]** en **[!UICONTROL Last Known]**: (19 januari 2022) Deze twee toewijzingsmodellen voldoen aan de &quot;entry&quot; - en &quot;exit&quot; - criteria. Zij nemen de eerste of laatste waargenomen waarde voor een afmeting binnen een gespecificeerd persistentieschema (zitting, persoon, of douanetijdspanne met raadpleging) en passen het op alle gebeurtenissen binnen het gespecificeerde werkingsgebied toe. Voorbeeld:

  | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Tijdstempel (min) | 1 | 2 | 3 | 6 | 7 |
  | Oorspronkelijke waarden |  | C | B |  | A |
  | Eerste gekend | C | C | C | C | C |
  | Laatst bekend | A | A | A | A | A |

## [!UICONTROL Expiration] instellingen

Details over de beschikbare vervalinstellingen.

* **Sessie**: Verloopt na een bepaalde sessie. Standaardvervalvenster.
* **Persoon**: Verloopt aan het einde van het rapportagevenster.
* **Aangepaste tijd**: Verloopt na een opgegeven periode (maximaal 90 dagen). Deze optie voor verlopen is alleen beschikbaar voor de toewijzingsmodellen Origineel en Recentste. Wanneer u op tijd gebaseerde vervaldatums gebruikt, worden waarden vóór het begin van het rapportagevenster (maximaal 90 dagen) in overweging genomen.
* **Metrisch**: Wanneer deze metrische waarde in een gebeurtenis wordt gezien, verlopen onmiddellijk de persistente waarde in de dimensie. U kunt elke gewenste metrische waarde gebruiken als eindwaarde voor de vervaldatum voor deze dimensie. Deze optie voor verlopen is alleen beschikbaar voor de instellingen Origineel en Recentste toewijzing.

## [!UICONTROL Binding Dimension]

Een vervolgkeuzelijst waarmee u de persistentie van een waarde voor de dimensie kunt binden aan waarden van de dimensie in een andere dimensie. Tot de geldige opties behoren andere afmetingen die in de gegevensweergave zijn opgenomen.

Zie [De bindingsafmetingen en metriek gebruiken in Customer Journey Analytics](../../use-cases/data-views/binding-dimensions-metrics.md) voor voorbeelden over hoe u op effectieve wijze bindingsdimensies kunt gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/342694/?quality=12)

## [!UICONTROL Binding Metric]

Een vervolgkeuzelijst waarin u een metrische waarde kunt kiezen die als een bindende trigger fungeert. Mogelijke geldige opties zijn meetgegevens die zijn opgenomen in de gegevensweergave.

Deze instelling wordt alleen weergegeven wanneer het Dimension Binding lager is in de objectarray dan de component. Wanneer metrisch binden in een gebeurtenis aanwezig is, worden de afmetingswaarden gekopieerd van de gebeurtenis-vlakke afmeting neer aan het lagere schemaniveau van de bindende afmeting.

Zie het tweede voorbeeld onder [De bindingsafmetingen en metriek gebruiken in Customer Journey Analytics](../../use-cases/data-views/binding-dimensions-metrics.md) voor meer informatie over hoe te om bindende metriek effectief te gebruiken.
