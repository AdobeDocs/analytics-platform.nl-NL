---
title: Overzicht van berekende metriek
description: Meer informatie over
exl-id: c9205c95-8b01-4177-a89c-038886f41d3d
translation-type: tm+mt
source-git-commit: a0ea2be203aa2e0df7b195e259b6d98c0c027652
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 4%

---

# Overzicht van berekende metriek

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Berekende en Geavanceerde Berekende (of Afgeleide) Metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen. Met onze gereedschappen voor berekende meetwaarden kunt u op zeer flexibele wijze metriek bouwen, beheren en beheren. Met deze services kunt u als marketers, productmanagers en analisten vragen stellen over de gegevens zonder dat u uw implementatie hoeft te wijzigen.

U kunt

* Creeer gefilterde metriek die bij rapportruntime worden afgeleid, zonder het moeten de implementatie veranderen. Deze kunnen historisch worden bekeken omdat ze zijn gebaseerd op filters.
* (Alleen Geavanceerde berekende cijfers) Filter op maateenheden. U kunt bijvoorbeeld een metrische waarde maken voor &quot;Nieuwe bezoekers&quot;, met een aantal personen voor wie dit de eerste sessie is.
* (Alleen geavanceerde berekende statistieken) Neem statistische functies op om uw gegevens beter te kunnen beschrijven. Bijvoorbeeld, kunt u het aantal punten in een rapport tellen of in het aantal standaardafwijkingen voor elk punt toevoegen.

## Berekende meetwaarden versus geavanceerde berekende meetwaarden

Hier volgt een vergelijking van de mogelijkheden Berekende meetwaarden en Geavanceerde berekende meetwaarden:

| Builder-opties | Berekende standaarden | Geavanceerde berekende (Afgeleide) Metriek |
|---|---|---|
| Indelingstypen (decimaal, tijd, percentage, valuta) | Ja | Ja |
| Wijzigingen in de kenmerken (standaard, lineair, deelname, enz.) | Ja | Ja |
| Metrische typen (standaard, totaal | Ja | Ja |
| Basisoperatoren (toevoegen, verwijderen, vermenigvuldigen, verdelen) | Ja | Ja |
| Filters toepassen | Nee | Ja |
| [Basisfuncties (aantal, abs-waarde, gemiddelde, enz.)](/help/components/calc-metrics/cm-functions.md) | Nee | Ja |
| [Geavanceerde functies (regressie, indien/toen, t-score, enz.)](/help/components/calc-metrics/cm-adv-functions.md) | Nee | Ja |

## Gereedschappen

| Gereedschap | Mogelijkheden |
|--- |--- |
| Berekende metrische bouwer | <ul><li>Creeer berekende en geavanceerde berekende metriek gebruikend geavanceerde toewijzingsmodellen.</li><li>Filters inline toevoegen aan metrische formules.</li><li>Vergelijk filters in hetzelfde rapport. Vergelijk bijvoorbeeld lokale bezoekers met internationale bezoekers.</li><li>Gebruik statistische functies.</li><li> Geef gedetailleerde metrische beschrijvingen op (toon wat het doet, waar het wordt gebruikt, waar het NIET wordt gebruikt).</li><li>Kopieer definities naar nieuwe metriek.</li><li>Een inline metrische voorvertoning weergeven.</li><li>Metrische polariteit instellen die aangeeft of het goed of slecht is als een bepaalde aangepaste gebeurtenis (metrisch) wordt verhoogd.</li><li>Metrische codes.</li></ul> |
| Berekende standaard-beheer | <ul><li>Deel metriek met anderen.</li><li>Metriek goedkeuren en krullen.</li><li>Organiseer uw gegevens (tag) zodat mensen ze kunnen vinden.</li><li>Metrische gegevens verwijderen.</li><li>Naam metriek wijzigen.</li></ul> |
| API voor berekende cijfers | Deel van de Adobe Analytics 2.0 API-set. |

## Sjablonen voor berekende metriek in CJA

| Berekende metrische naam | Berekende metrische beschrijving |
| --- | --- |
| Sessies per persoon | Gemiddeld aantal sessies per persoon |
| Beginsnelheid van sessie | Het percentage van tijd dat om het even welk afmetingspunt op de eerste gebeurtenis van een zitting voorkwam. |
| Eindfrequentie sessie | Het percentage van tijd dat om het even welk afmetingspunt op de laatste gebeurtenis van een zitting voorkwam. |
| Tijd besteed per persoon | De gemiddelde hoeveelheid tijd die een persoon aan om het even welk bepaald afmetingspunt heeft doorgebracht. |
| Tijd besteed per sessie | De gemiddelde hoeveelheid tijd die een persoon per Zitting aan om het even welk bepaald afmetingspunt doorbracht. |
