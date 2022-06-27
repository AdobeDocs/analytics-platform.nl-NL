---
title: Virtuele rapportsuite, gegevensweergaven, AEP-sandboxen en de Bronverbinding voor analyse
description: Meer informatie over virtuele-rapporteringsomgevingen en sandboxomgevingen.
exl-id: 8f0358d1-85fe-4e1e-8724-8a7caa16328c
source-git-commit: 7c3bbe2829c83406b2e6824e509c34459ae00f94
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Virtuele rapportsuite, gegevensweergaven, AEP-sandboxen en de Bronverbinding voor analyse

Adobe biedt verschillende manieren om virtuele rapporteringsomgevingen en sandboxomgevingen te maken. Het is nuttig om de gelijkenissen en de verschillen tussen de volgende eigenschappen te begrijpen en hoe deze eigenschappen op [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en):

* Adobe Analytics Virtual Report-suites
* CJA-gegevensweergaven
* AEP-sandboxen

## Adobe Analytics Virtual Report Suites (VRS)

Zie voor meer informatie: [Overzicht van virtuele-rapportsuites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=en).

A VRS:

* Kan worden gebaseerd op Adobe Analytics-segmenten.
* Kan op niet-destructieve wijze op zowel historische als nieuwe gegevens worden toegepast.
* Staat u toe om één of vele virtuele meningen bovenop een het rapportreeks van Adobe Analytics voor gebruik door verschillende bedrijfsteams tot stand te brengen.
* Kan worden gebruikt om de toegang tot en het beheer van verschillende soorten gegevens voor verschillende gebruikers in Adobe Analytics te regelen.
* Optioneel [verwerking van rapporttijd](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=en) mogelijkheden voor Adobe Analytics. In dit geval kan een vrijwillige VUT-regeling worden gebruikt om een aangepaste definitie voor &quot;bezoek&quot; te maken.
* Wordt toegepast bij rapportruntime, gelijkend op segmentevaluatie. Dit is _na_ de gegevens zijn verzameld en opgeslagen in Adobe Analytics.
* Is vereist voor [Apparaatanalyse](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html?lang=en) in Adobe Analytics.
* Heeft hetzelfde aantal variabelen beschikbaar voor gebruik als standaard Analytics Report Suite (250 eVars, 250 props, 1000 events), hoewel VRS-curatie kan beperken welke variabelen aan gebruikers worden blootgesteld.
* Ondersteunt aangepaste kalenderopties.

Een virtuele rapportsuite is niet:

* Een middel om de rapportsuites te combineren.
* Beschikbaar in Adobe Analytics Data Warehouse.
* Beschikbaar als bron voor gegevensstromen in AEP via de Analytics Source Connector. Alleen volledige (niet-virtuele) rapportsuites zijn beschikbaar voor gebruik met de Bronconnector Analytics.


## CJA-gegevensweergaven

Zie voor meer informatie: [Overzicht van gegevensweergaven](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html?lang=en).

Een gegevensweergave:

* Kan worden gebaseerd op CJA-filters.
* Kan op niet-destructieve wijze op zowel historische als nieuwe gegevens worden toegepast.
* Staat u toe om één of vele virtuele meningen bovenop een verbinding te creëren CJA, voor gebruik door verschillende bedrijfsteams.
* Kan worden gebruikt om de toegang tot en het leiden van verschillende soorten gegevens voor verschillende gebruikers in CJA te controleren.
* Biedt krachtige, niet-destructieve opties voor het transformeren en verbeteren van gegevens die via een CJA-verbinding in CJA komen.
* Is gebaseerd op de rapport-tijd verwerkingsmogelijkheden van CJA.
* Hiermee kunnen gebruikers een aangepaste definitie maken voor &quot;sessie&quot;.
* Wordt toegepast bij rapportruntime, vergelijkbaar met een filterevaluatie. Dit is _na_ de Source Connector (Adobe Analytics of andere) schriftelijke gegevens heeft naar een gegevensset in het AEP data Lake, en _na_ de gegevens zijn via een CJA-verbinding in CJA ingevoerd.
* Hiermee wordt een onbeperkt aantal variabelen toegestaan, maar door curatie kan worden beperkt welke variabelen aan gebruikers worden blootgesteld
* Hiermee kunt u de containers voor gebeurtenissen, sessies en personen een aangepaste naam geven.
* Ondersteunt aangepaste kalenderopties.

Een gegevensweergave doet dit niet:

* Rechtstreeks een middel verstrekken om rapportsuites of andere datasets te combineren. In plaats daarvan, worden de datasets gecombineerd met in een verbinding CJA. De gecombineerde gegevens van de verbinding CJA zijn beschikbaar voor gebruik in alle gegevensmeningen die op die verbinding worden gebaseerd.

## AEP-sandboxen

Zie voor meer informatie: [Overzicht van sandboxen](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=en).

Een AEP-sandbox:

* Biedt een manier om één AEP-instantie te verdelen in afzonderlijke virtuele omgevingen (ontwikkelen, testen, stadium, productie, enz.) helpen bij het ontwikkelen en ontwikkelen van toepassingen voor digitale ervaringen.
* Kan worden beschouwd als een container die alle gegevens en toepassingen voor een bepaalde omgeving bevat.

Een AEP-sandbox doet dit niet:

* Verstrek gelijkaardige functies zoals virtuele rapportreeksen, verbindingen CJA of gegevensmeningen.
* Op zichzelf combineert het rapport reeksen met of zonder andere datasets. De gegevenssets in een sandbox kunnen echter worden gecombineerd binnen een CJA-verbinding.

Let op:

* Gegevens van verschillende sandboxen kunnen niet worden gecombineerd in CJA.
* De verbinding van de Bron van de Analyse verzendt rapportreeksgegevens _in_ een specifieke sandbox. Elk rapportpakket kan als bron voor één enkele zandbak worden gevormd. Zie de [Documentatie over de analytische bronaansluiting](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en) voor meer informatie .
