---
title: Instellingen voor persistentiecomponenten
description: Bepaal hoe of of de waarden van de afmeting van één gebeurtenis aan volgende blijven.
exl-id: b8b234c6-a7d9-40e9-8380-1db09610b941
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: c94e97723a4ed30e675144e02196c93016b13235
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 4%

---


# [!UICONTROL Persistence] Component instellingen {#persistence-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_dimension_persistence"
>title="Volharding"
>abstract="Configureer het standaardtoewijzingsmodel dat op een dimensie wordt toegepast. Toewijzing is van toepassing vóór filters in rapportage. Zie voor meer informatietoewijzingsinstellingen[](/help/data-views/component-settings/persistence.md#allocation-settings), [verloopinstellingen](/help/data-views/component-settings/persistence.md#expiration-settings), [bindingsdimensies](/help/data-views/component-settings/persistence.md#binding-dimension) en [bindingsstatistieken](/help/data-views/component-settings/persistence.md#binding-metric)."

<!-- markdownlint-enable MD034 -->



[!UICONTROL Persistence] is de capaciteit voor een bepaalde afmetingswaarde om op metrisch voorbij de gebeurtenis betrekking te hebben het wordt geplaatst. Er wordt een combinatie van toewijzing en vervaldatum gebruikt.

![Venster met gegevensweergaven waarin de opties voor persistentie worden gemarkeerd](../assets/persistence.png)

* **Met toewijzing** kunt u bepalen welke waarde wordt behouden wanneer er meer dan één dimensie-item tegelijk in één kolom kan blijven staan.

  >[!NOTE]
  >
  >Als u een [niet-standaard toeschrijvingsmodel](/help/data-views/component-settings/attribution.md) heeft ingesteld voor een metrische waarde in een rapport, negeert het toeschrijvingsmodel de toewijzing die u hebt ingesteld voor de dimensie voor hetzelfde rapport.
  >
  >Wanneer u echter een [volledige tabelexport](/help/analysis-workspace/export/export-cloud.md) uitvoert die meerdere dimensies bevat, blijven bij attributie de toewijzingsmodellen behouden die op elke dimensie zijn toegepast.

* **Met vervaldatum** kunt u bepalen hoe lang een dimensie-item blijft bestaan na de gebeurtenis waarop het is ingesteld.

[!UICONTROL Persistence] is alleen beschikbaar voor dimensies en heeft terugwerkende kracht tot de gegevens waarop deze worden toegepast. Het is een directe gegevenstransformatie die gebeurt alvorens het filtreren of andere analyseverrichtingen worden toegepast.

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

  | Dimension | Raak 1 | Raak 2 | Raak 3 | Raak 4 | Actief 5 |
  | --- | --- | --- | --- | --- | --- |
  | Waarden voor gegevensset | A | B | C |  | A |
  | Alle toewijzing | A | A,B | A,B,C | A,B,C | A,B,C |

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
* **Persoon die Venster** meldt: Verloopt aan het eind van het rapporteringsvenster.
* **Globale Rekening die Venster** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} meldt: Verloopt aan het eind van het rapporteringsvenster.
* **Rekening die Venster** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"} meldt: Verloopt aan het eind van het rapporteringsvenster.
* **Opportunity Reporting Window** [!BADGE B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}: Verloopt aan het einde van het rapportagevenster.
* **Rapportagevenster** [!BADGE voor inkoopgroep B2B-editie]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}: Verloopt aan het einde van het rapportagevenster.
* **Aangepaste tijd**: Vervalt na een opgegeven periode (maximaal 90 dagen). Deze optie voor verlopen is alleen beschikbaar voor de toewijzingsmodellen Origineel en Recentste. Wanneer u op tijd gebaseerde vervaldatums gebruikt, worden waarden vóór het begin van het rapportagevenster (maximaal 90 dagen) in overweging genomen.
* **Metrisch**: Wanneer dit metrisch in een gebeurtenis wordt gezien, onmiddellijk verlopen de persistente waarde in de dimensie. U kunt elke gewenste metrische waarde gebruiken als eindwaarde voor de vervaldatum voor deze dimensie. Deze optie voor verlopen is alleen beschikbaar voor de instellingen Origineel en Recentste toewijzing.


## [!UICONTROL Binding Dimension]

Een vervolgkeuzelijst waarmee u de persistentie van een waarde voor de dimensie kunt binden aan waarden van de dimensie in een andere dimensie. Tot de geldige opties behoren andere afmetingen die in de gegevensweergave zijn opgenomen.

Zie [ Gebruikend bindende dimensies en metriek in Customer Journey Analytics ](../../use-cases/data-views/binding-dimensions-metrics.md) voor voorbeelden rond hoe te om bindende dimensies effectief te gebruiken.


>[!BEGINSHADEBOX]

Zie ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Bindingsafmetingen](https://video.tv.adobe.com/v/342694/?quality=12&learn=on){target="_blank"} voor een demovideo.

>[!ENDSHADEBOX]


## [!UICONTROL Binding Metric]

Een vervolgkeuzelijst waarin u een metrische waarde kunt kiezen die fungeert als een bindende trigger. Geldige opties zijn onder meer metrische gegevens die zijn opgenomen in de gegevensweergave.

Deze instelling wordt alleen weergegeven als de bindingsdimensie in de objectmatrix lager is dan de component. Wanneer metrisch binden in een gebeurtenis aanwezig is, worden de afmetingswaarden gekopieerd van de gebeurtenis-vlakke afmeting neer aan het lagere schemaniveau van de bindende afmeting.

Zie het tweede voorbeeld onder [ Gebruikend bindende dimensies en metriek in Customer Journey Analytics ](../../use-cases/data-views/binding-dimensions-metrics.md) voor meer informatie rond hoe te om bindende metriek effectief te gebruiken.
