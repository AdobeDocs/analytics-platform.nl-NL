---
title: Instellingen voor persistentiecomponenten
description: Bepaal hoe of of de waarden van de afmeting van één gebeurtenis aan volgende blijven.
exl-id: b8b234c6-a7d9-40e9-8380-1db09610b941
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: d65171873f68835de0628b95158f01713eaacb6b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 5%

---


# [!UICONTROL Persistence] componentinstellingen {#persistence-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_dimension_persistence"
>title="Persistentie"
>abstract="Vorm het standaardtoewijzingsmodel dat op een dimensie wordt toegepast. Toewijzing is van toepassing vóór filters in rapportage. Zie voor meer informatie [ toewijzingsmontages ](/help/data-views/component-settings/persistence.md#allocation-settings), [ vervalmontages ](/help/data-views/component-settings/persistence.md#expiration-settings), [ bindende afmeting ](/help/data-views/component-settings/persistence.md#binding-dimension) en bindende metriek."

<!-- markdownlint-enable MD034 -->



[!UICONTROL Persistence] is de capaciteit voor een bepaalde afmetingswaarde om op metrisch voorbij de gebeurtenis betrekking te hebben het wordt geplaatst. Er wordt een combinatie van toewijzing en vervaldatum gebruikt.

![ de meningsvenster van Gegevens die de opties van de Persistentie benadrukken ](../assets/persistence.png)

* **Toewijzing** laat u bepalen welke waarde wordt gehouden wanneer meer dan één afmetingspunt in een tijd in één enkele kolom kan voortbestaan.

  >[!NOTE]
  >
  >Als u a [ niet-gebrek attributiemodel ](/help/data-views/component-settings/attribution.md) op metrisch in een rapport hebt geplaatst, negeert het attributiemodel de toewijzing u op de afmeting voor het zelfde rapport plaatst.
  >
  >Nochtans, wanneer het doen van a [ volledige lijstuitvoer ](/help/analysis-workspace/export/export-cloud.md) die veelvoudige dimensies omvat, behoudt de attributie de toewijzingsmodellen die op elke afmeting worden toegepast.

* **Vervalsing** laat u bepalen hoe lang een afmetingspunt voorbij de gebeurtenis voortduurt het wordt geplaatst.

[!UICONTROL Persistence] is alleen beschikbaar voor dimensies en is retroactief voor de gegevens waarop het is toegepast. Het is een directe gegevenstransformatie die gebeurt alvorens het filtreren of andere analyseverrichtingen worden toegepast.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Set persistence] | Laat persistentie voor de afmeting toe. Als persistentie niet is ingeschakeld, heeft de dimensie alleen betrekking op metriek die in dezelfde gebeurtenis bestaan. Deze instelling is standaard uitgeschakeld. |
| [!UICONTROL Allocation] | Hier kunt u het toewijzingsmodel opgeven dat wordt gebruikt voor een dimensie voor persistentie. De opties zijn: [!UICONTROL Most recent], [!UICONTROL Original], [!UICONTROL Instance], [!UICONTROL All] . Vanaf 28 oktober 2021 wordt een terugzoekvenster van maximaal 90 dagen toegevoegd aan de instelling voor [!UICONTROL Allocation] . |
| [!UICONTROL Expiration] | Hier geeft u het venster voor persistentie voor een dimensie op. De opties zijn: [!UICONTROL Session] (standaardwaarde), [!UICONTROL Person], [!UICONTROL Custom Time], [!UICONTROL Metric] . Mogelijk moet u de afmeting van een aankoop kunnen verlopen (zoals interne zoektermen of andere gevallen waarin u zaken voor koopwaar gebruikt). De maximale vervaltijd die u kunt instellen, is 90 dagen. Als u een toewijzing van [!UICONTROL All] selecteert, is alleen de vervaldatum [!UICONTROL Session] of [!UICONTROL Person] beschikbaar. |

{style="table-layout:auto"}

## [!UICONTROL Allocation] instellingen

Details over de beschikbare toewijzingsinstellingen.

* **[!UICONTROL Most Recent]**: hiermee wordt de meest recente (door tijdstempel) waarde in de dimensie gehandhaafd. Alle volgende waarden die binnen de afloopperiode van de dimensie voorkomen, vervangen de eerder blijkende waarde. Als &quot;Behandel &quot;Geen Waarde&quot;als waarde&quot;op deze afmeting onder [ wordt toegelaten Geen waardeopties ](no-value-options.md), beschrijven de lege waarden eerder voortgeduurde waarden. Neem bijvoorbeeld de volgende tabel met [!UICONTROL Most recent] toewijzing en [!UICONTROL Session] vervaldatum:

  | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Waarden voor gegevensset |  | C | B |  | A |
  | Meest recente toewijzing |  | C | B | B | A |

* **[!UICONTROL Original]**: behoudt de oorspronkelijke waarde met een tijdstempel die binnen de dimensie aanwezig is gedurende de verloopperiode. Als deze dimensie een waarde heeft, wordt deze niet overschreven wanneer een andere waarde wordt waargenomen bij een volgende gebeurtenis. Neem bijvoorbeeld de volgende tabel met [!UICONTROL Original] toewijzing en [!UICONTROL Session] vervaldatum:

  | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Waarden voor gegevensset |  | C | B |  | A |
  | Oorspronkelijke toewijzing |  | C | C | C | C |

* **[!UICONTROL All]**: werkt hetzelfde als het [!UICONTROL Participation] -attributiemodel voor metriek. Hiermee worden alle waarden op gelijke wijze gehandhaafd, zodat elke waarde bij rapportage volledige creditering voor de maatstaf krijgt. Neem bijvoorbeeld de volgende tabel met [!UICONTROL All] toewijzing en [!UICONTROL Session] vervaldatum:

  | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Waarden voor gegevensset | A | B | C |  | A |
  | Alle toewijzingen | A | A,B | A,B,C | A,B,C | A,B,C |

* **[!UICONTROL First Known]** en **[!UICONTROL Last Known]**: (19 januari 2022) Deze twee toewijzingsmodellen voldoen aan de gebruiksscenario&#39;s &quot;entry&quot; en &quot;exit&quot;. Zij nemen de eerste of laatste waargenomen waarde voor een afmeting binnen een gespecificeerd persistentieschema (zitting, persoon, of douanetijdspanne met raadpleging) en passen het op alle gebeurtenissen binnen het gespecificeerde werkingsgebied toe. Voorbeeld:

  | Dimension | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Tijdstempel (min) | 1 | 2 | 3 | 6 | 7 |
  | Oorspronkelijke waarden |  | C | B |  | A |
  | Eerste gekend | C | C | C | C | C |
  | Laatst bekend | A | A | A | A | A |

## [!UICONTROL Expiration] instellingen

Details over de beschikbare vervalinstellingen.

* **Zitting**: Verloopt na een bepaalde zitting. Standaardvervalvenster.
* **Persoon**: Verloopt aan het eind van het rapporteringsvenster.
* **Tijd van de Douane**: Verloopt na een gespecificeerde tijdspanne (tot 90 dagen). Deze optie voor verlopen is alleen beschikbaar voor de toewijzingsmodellen Origineel en Recentste. Wanneer u op tijd gebaseerde vervaldatums gebruikt, worden waarden vóór het begin van het rapportagevenster (maximaal 90 dagen) in overweging genomen.
* **Metrisch**: Wanneer dit metrisch in een gebeurtenis wordt gezien, onmiddellijk verlopen de persistente waarde in de dimensie. U kunt elke gewenste metrische waarde gebruiken als eindwaarde voor de vervaldatum voor deze dimensie. Deze optie voor verlopen is alleen beschikbaar voor de instellingen Origineel en Recentste toewijzing.

## [!UICONTROL Binding Dimension]

Een vervolgkeuzelijst waarmee u de persistentie van een waarde voor de dimensie kunt binden aan waarden van de dimensie in een andere dimensie. Tot de geldige opties behoren andere afmetingen die in de gegevensweergave zijn opgenomen.

Zie [ Gebruikend bindende dimensies en metriek in Customer Journey Analytics ](../../use-cases/data-views/binding-dimensions-metrics.md) voor voorbeelden rond hoe te om bindende dimensies effectief te gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/342694/?quality=12)

## [!UICONTROL Binding Metric]

Een vervolgkeuzelijst waarin u een metrische waarde kunt kiezen die als een bindende trigger fungeert. Mogelijke geldige opties zijn meetgegevens die zijn opgenomen in de gegevensweergave.

Deze instelling wordt alleen weergegeven wanneer het Dimension Binding lager is in de objectarray dan de component. Wanneer metrisch binden in een gebeurtenis aanwezig is, worden de afmetingswaarden gekopieerd van de gebeurtenis-vlakke afmeting neer aan het lagere schemaniveau van de bindende afmeting.

Zie het tweede voorbeeld onder [ Gebruikend bindende dimensies en metriek in Customer Journey Analytics ](../../use-cases/data-views/binding-dimensions-metrics.md) voor meer informatie rond hoe te om bindende metriek effectief te gebruiken.
