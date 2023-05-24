---
description: Adobe verstrekt diverse berekende metriek die u kunt gebruiken. Deze pagina bevat een overzicht van die metingen en het gebruik waarvoor ze zijn bedoeld.
title: Berekende standaardwaarden
feature: Calculated Metrics
exl-id: 08d11cce-170e-42a2-806f-e0a28b70a2dc
source-git-commit: 3f1112ebd2a4dfc881ae6cb7bd858901d2f38d69
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 1%

---

# Berekende standaardwaarden

Customer Journey Analytics verstrekt diverse berekende metriek om de gemeenschappelijkste gebruiks-gevallen te behandelen. Deze berekende maatstaven zijn standaard beschikbaar in Analysis Workspace.

Hieronder volgt een lijst van elke berekende metrische waarde die door Adobe wordt verstrekt, met de beoogde functie en de onderliggende formule die wordt gebruikt om deze te berekenen:

>[!NOTE]
>
>Naast de standaard berekende metriek die op deze pagina wordt beschreven, kunt u extra berekende metriek aan een gegevensmening ook toevoegen.
>
>U kunt:
> * Standaardberekende waarden toevoegen voor streamingmedia, zoals beschreven in [Berekende cijfers](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html)
> * Aangepaste berekende metriek maken van bestaande metriek, zoals beschreven in [Berekende en geavanceerde berekende (afgeleide) meetwaarden](/help/components/calc-metrics/cm-adv-functions.md).



| Metrische naam berekend | -functie | Formule |
|---------|----------|---------|
| Bouncepercentage | De verhouding tussen bezoeken die precies één gebeurtenis bevatten en het aantal bezoeken op die pagina. Hierdoor kunt u beter begrijpen welke dimensie-items de hoogste stuitsnelheid hebben of kunt u een totale stuitsnelheid van uw site in de loop van de tijd zien. | `[Bounces] / [Entries]` |
| Ontvangsten/bezoekers | Het gemiddelde bedrag aan inkomsten dat door elke individuele persoon aan de plaats wordt gegenereerd. | `[Revenue] / [Unique Visitors]` |
| Bestellingen/Bezoeker | Het gemiddelde aantal orders of transacties dat door elke individuele persoon tot de locatie wordt gegenereerd | `[Orders] / [Unique Visitors]` |
| Ontvangsten/bezoeken | Het gemiddelde bedrag aan inkomsten dat wordt gegenereerd door één enkel bezoek aan de locatie. | `[Revenue] / [Visits]` |
| Opbrengsten/opdracht | Het gemiddelde bedrag aan opbrengsten dat door elke voltooide transactie of opdracht op de locatie wordt gegenereerd. | `[Revenue] / [Orders]` |
| Bestellingen/bezoeken | Het percentage bezoeken aan de site dat resulteert in een voltooide transactie. | `[Orders] / [Visits]` |
| Paginaweergaven/bezoeken | Het gemiddelde aantal pagina&#39;s dat een gebruiker weergeeft tijdens één bezoek aan de site. | `[Page Views] / [Visits]` |
| Bezoeken/Bezoeker | Het gemiddelde aantal bezoeken dat een unieke persoon aan de site brengt. | `[Visits] / [Unique Visitors]` |
| Opnieuw laden / Pagina&#39;s | Het percentage paginaweergaven dat heeft geresulteerd in het opnieuw laden of vernieuwen van de pagina. | `[Reloads] / [Page Views]` |
| Gewogen stuiterende waarde | -functie | `IF([Visits] > PERCENTILE([Visits]), [Bounce Rate], 0)` |
| Assistenten bestellen | Het aantal keren dat een kanaal of bron heeft bijgedragen aan de reis van een klant naar een aankoop, maar niet tot de uiteindelijke aankoop heeft geleid. | `[Orders (Visit Participation)] - [Orders]` |
| Afsluitingsfrequentie | Het percentage personen dat de site verlaat na weergave van een bepaalde pagina. | `[Exits] / [Visits]` |
| Invoersnelheid | Het percentage personen dat op een bepaalde pagina de site is binnengekomen, in vergelijking met het totale aantal sessies op de site. | `[Entries] / [Visits]` |
| Gemiddelde tijd op de site | De gemiddelde hoeveelheid tijd die een persoon op de plaats doorbrengt alvorens weg te gaan of weg te navigeren. | `[Average Time Spent on Site (Seconds)]` |
| Tijd besteed/gebruiker (staat) | De duur van de tijd dat de gemiddelde persoon in een bepaalde staat doorbrengt terwijl hij op de plaats | `[Mobile App Users] (filter)`<br>`[Time Spent per Visitor (Seconds)] (metric)` |
| Gebruikers (mobiel) | Het totale aantal gebruikers van een mobiele app | `[Mobile App Users] (filter)`<br>`[Unique Visitors] (metric)` |
| Toepassingsgebruikers | Het totale aantal gebruikers van een mobiele app | `[Mobile App Users] (filter)`<br>`[Unique Visitors] (metric)` |
| Statusweergaven | Het aantal weergaven voor de verschillende staten of schermen van de app | `[Mobile App Users] (filter)`<br>`[Page Views] (metric)` |
| Handelingen | Het totale aantal acties dat in de app is uitgevoerd | `[Has an Action] (filter)`<br>`[Custom Link Instances] (metric)` |
| Koppelingsklikken bij overname | Het aantal keren dat de mensen op een verbinding klikken die wordt ontworpen om verkeer naar de plaats te drijven. | `[Campaign Click-throughs]` |
| Paginasnelheid | Het aantal extra paginaweergaven dat door een stuk inhoud wordt gegenereerd. Dit kan u helpen bepalen welke inhoud extra betrokkenheid drijft. | `[Page Views] / [Visits]` |
| Omzetsnelheid | Het percentage personen dat de gewenste actie heeft ondernomen, zoals een aankoop. | `[Orders] / [Visits]` |
| Gemiddelde sessieduur (mobiel) | De gemiddelde hoeveelheid tijd die personen gedurende één sessie aan de site doorbrengen. | Leeg |
| Experience Cloud ID-dekking | Het percentage personen met een Experience Cloud-id. | `[Visitors with Experience Cloud ID] / [Unique Visitors]` |
| Contentsnelheid | De snelheid waarmee nieuwe inhoud wordt gemaakt en gepubliceerd op de site en hoe snel de betrokkenheid van de gebruiker wordt gegenereerd. | `[Page Views] / [Visits]` |
| ITP 2.1 Unieke bezoekers / Unieke bezoekers | Het percentage unieke personen die een browser gebruiken die door ITP 2.1 koekjesbeperkingen wordt beïnvloed. Met andere woorden, klanten die geen implementatie CNAME gebruiken. (Dit geldt voor klanten die cookies instellen via JavaScript op de client.) | `[Unique Visitors metric with ITP Visitors filter] / [Unique Visitors]` |
| Unieke bezoekers/unieke bezoekers die na 7 dagen terugkeren | Het percentage unieke personen die na een periode van 7 of meer dagen terugkeren. | `[Unique Visitors metric with Users returning after 7 days filter] / [Unique Visitors]` |
| Paginaweergaven / Unieke bezoeker | Het gemiddelde aantal weergegeven pagina&#39;s voor elke unieke persoon van de site. | `[Page Views] / [Unique Visitors]` |
| Bezoekers | Het gemiddelde aantal bezoeken dat een unieke persoon aan de site brengt. | `[Visits] / [Unique Visitors]` |
| Geschatte unieke bezoekers (ITP 2.1) | Voor ITP-personen (gebruikers in Safari-browsers) deelt u Unieke bezoekers door 2 of minder. Deze berekende metrische waarde veronderstelt dat u koekjes gebruikend cliënt-kant JavaScript (het gebruiken van geen implementatie CNAME) plaatst. Implementaties die cookies instellen met JavaScript op de client werden beïnvloed vanaf ITP 2.1. Zie [Intelligente traceringspreventie](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) voor meer informatie. | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) filter] / [Unique Visitors metric + Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) filter]` |
| Paginaweergaven / geschatte unieke bezoekers (ITP 2.1) | Het gemiddelde aantal weergegeven pagina&#39;s voor geschatte unieke bezoekers (ITP 2.1). | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) filter] / [Unique Visitors (metric) with Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) filter]` |

{style="table-layout:auto"}
