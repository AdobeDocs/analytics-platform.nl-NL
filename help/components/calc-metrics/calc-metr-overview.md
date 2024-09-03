---
title: Overzicht van berekende metriek
description: Leer over gefilterde metriek die bij rapportruntime worden afgeleid.
feature: Calculated Metrics
exl-id: c9205c95-8b01-4177-a89c-038886f41d3d
role: User
source-git-commit: 61c1fe48ebe8ebff5b7104cebae1ce7b62289b7d
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 2%

---

# Overzicht van berekende metriek

Berekende en Geavanceerde berekende metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen. Met onze gereedschappen voor berekende meetwaarden kunt u op zeer flexibele wijze metriek bouwen, beheren en beheren. Met deze services kunt u als marketers, productmanagers en analisten vragen stellen over de gegevens zonder dat u uw implementatie hoeft te wijzigen.

U kunt

* Creeer gefilterde metriek die bij rapportruntime worden afgeleid, zonder het moeten de implementatie veranderen. Deze kunnen historisch worden bekeken omdat ze zijn gebaseerd op filters.
* (Alleen Geavanceerde berekende cijfers) Filter op maateenheden. U kunt bijvoorbeeld een metrische waarde maken voor &quot;Nieuwe personen&quot;, met een aantal personen voor wie dit de eerste sessie is.
* (Alleen geavanceerde berekende statistieken) Neem statistische functies op om uw gegevens beter te kunnen beschrijven. Bijvoorbeeld, kunt u het aantal punten in een rapport tellen of in het aantal standaardafwijkingen voor elk punt toevoegen.

## Berekende meetwaarden versus geavanceerde berekende meetwaarden

Hier volgt een vergelijking van de mogelijkheden Berekende meetwaarden en Geavanceerde berekende meetwaarden:

| Builder-opties | Berekende standaarden | Geavanceerde berekende cijfers |
|---|---|---|
| Formattypen (decimaal, tijd, percentage, valuta | Ja | Ja |
| Wijzigingen in de kenmerken (standaard, lineair, deelname, enz.) | Ja | Ja |
| Metrische typen (standaard, totaal | Ja | Ja |
| Basisoperatoren (toevoegen, verwijderen, vermenigvuldigen, verdelen) | Ja | Ja |
| Filters toepassen | Nee | Ja |
| [ Basisfuncties (telling, abs waarde, gemiddelde, enz.) ](/help/components/calc-metrics/cm-functions.md) | Nee | Ja |
| [ Geavanceerde functies (regressie, als/toen, t-score, enz.) ](/help/components/calc-metrics/cm-adv-functions.md) | Nee | Ja |

## Gereedschappen

| Gereedschap | Mogelijkheden |
|--- |--- |
| Berekende metrische builder | <ul><li>Creeer berekende en geavanceerde berekende metriek gebruikend geavanceerde toewijzingsmodellen.</li><li>Filters inline toevoegen aan metrische formules.</li><li>Vergelijk filters in hetzelfde rapport. Vergelijk bijvoorbeeld lokale personen met internationale personen.</li><li>Gebruik statistische functies.</li><li> Geef gedetailleerde metrische beschrijvingen op (toon wat het doet, waar het moet worden gebruikt, waar NIET).</li><li>Kopieer definities naar nieuwe metriek.</li><li>Geef een inline metrische voorvertoning op.</li><li>Metrische polariteit instellen die aangeeft of het goed of slecht is als een bepaalde aangepaste gebeurtenis (metrisch) wordt verhoogd.</li><li>Metrische waarden van tags.</li></ul> |
| Berekende metrische manager | <ul><li>Deel metriek met anderen.</li><li>Metriek goedkeuren en krullen.</li><li>Organiseer uw gegevens (tag) zodat mensen ze kunnen vinden.</li><li>Metrische gegevens verwijderen.</li><li>Wijzig de naam van metriek.</li></ul> |
| API voor Berekende waarden | Onderdeel van de Customer Journey Analytics API-set. |

## Sjablonen voor berekende statistieken in Customer Journey Analytics

| Berekende metrische naam | Berekende metrische beschrijving |
| --- | --- |
| Sessies per persoon | Gemiddeld aantal sessies per persoon |
| Beginsnelheid van sessie | Het percentage van tijd dat om het even welk afmetingspunt op de eerste gebeurtenis van een zitting voorkwam. |
| Eindfrequentie sessie | Het percentage van tijd dat om het even welk afmetingspunt op de laatste gebeurtenis van een zitting voorkwam. |
| Tijd besteed per persoon | De gemiddelde hoeveelheid tijd die een persoon aan om het even welk bepaald afmetingspunt heeft doorgebracht. |
| Tijd besteed per sessie | De gemiddelde hoeveelheid tijd die een persoon per Zitting aan om het even welk bepaald afmetingspunt doorbracht. |
