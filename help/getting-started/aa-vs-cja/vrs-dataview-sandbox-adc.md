---
title: Virtuele rapportsuites, de meningen van Gegevens, de zandbakken van Adobe Experience Platform, en de de bronschakelaar van de Analyse
description: Meer informatie over virtuele-rapporteringsomgevingen en sandboxomgevingen.
exl-id: 8f0358d1-85fe-4e1e-8724-8a7caa16328c
feature: Basics
role: User
source-git-commit: 46d799ad2621d83906908a3f60a59a1027c6518c
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Virtuele rapportsuites, de meningen van Gegevens, de zandbakken van Adobe Experience Platform, en de de bronschakelaar van de Analyse

Adobe biedt verschillende manieren om virtuele rapporteringsomgevingen en sandboxomgevingen te maken. Het is nuttig om de gelijkenissen en de verschillen tussen de volgende eigenschappen te begrijpen en hoe deze eigenschappen op [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html):

* Adobe Analytics Virtual Report-suites
* Weergaven van Customer Journey Analytics-gegevens
* Adobe Experience Platform-sandboxen

## Adobe Analytics Virtual Report-suites

Zie voor meer informatie: [Overzicht van virtuele-rapportsuites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html).

Een virtuele rapportsuite:

* Kan worden gebaseerd op Adobe Analytics-segmenten.
* Kan op niet-destructieve wijze op zowel historische als nieuwe gegevens worden toegepast.
* Staat u toe om één of vele virtuele meningen bovenop een het rapportreeks van Adobe Analytics voor gebruik door verschillende bedrijfsteams tot stand te brengen.
* Kan worden gebruikt om de toegang tot en het beheer van verschillende soorten gegevens voor verschillende gebruikers in Adobe Analytics te regelen.
* Optioneel [verwerking van rapporttijd](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html) mogelijkheden voor Adobe Analytics. In dit geval kan een virtuele rapportsuite worden gebruikt om een aangepaste definitie voor &quot;visit&quot; te maken.
* Wordt toegepast bij rapportruntime, gelijkend op segmentevaluatie. Dit is _na_ de gegevens zijn verzameld en opgeslagen in Adobe Analytics.
* Is vereist voor [Apparaatanalyse](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html) in Adobe Analytics.
* Beschikt over hetzelfde aantal variabelen voor gebruik als standaard Analytics Report Suite (250 eVars, 250 props, 1000 events), hoewel de virtuele reekscuratie van het rapport kan beperken welke variabelen aan gebruikers worden blootgesteld.
* Ondersteunt aangepaste kalenderopties.

Een virtuele rapportsuite is niet:

* Een middel om de rapportsuites te combineren.
* Beschikbaar in Adobe Analytics Data Warehouse.
* Beschikbaar als bron voor gegevensstromen in Adobe Experience Platform via de bronschakelaar van de Analytics. Alleen volledige (niet-virtuele) rapportsuites zijn beschikbaar voor gebruik met de bronconnector van Analytics.


## Weergaven van Customer Journey Analytics-gegevens

Zie voor meer informatie: [Overzicht van gegevensweergaven](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html).

Een gegevensweergave:

* Kan worden gebaseerd op Customer Journey Analytics-filters.
* Kan op niet-destructieve wijze op zowel historische als nieuwe gegevens worden toegepast.
* Staat u toe om één of vele virtuele meningen bovenop een verbinding van de Customer Journey Analytics, voor gebruik door verschillende bedrijfsteams tot stand te brengen.
* Kan worden gebruikt om de toegang tot en het leiden van verschillende soorten gegevens voor verschillende gebruikers in Customer Journey Analytics te controleren.
* Biedt krachtige, niet-destructieve opties voor het transformeren en verbeteren van gegevens die via een Customer Journey Analytics in Customer Journey Analytics komen.
* Is gebaseerd op de rapport-tijd verwerkingsmogelijkheden van Customer Journey Analytics.
* Hiermee kunnen gebruikers een aangepaste definitie maken voor &quot;sessie&quot;.
* Wordt toegepast bij rapportruntime, vergelijkbaar met een filterevaluatie. Dit is _na_ de Source Connector (Adobe Analytics of andere) schriftelijke gegevens heeft naar een dataset in het Adobe Experience Platform data Lake, en _na_ de gegevens zijn in Customer Journey Analytics via een verbinding van de Customer Journey Analytics opgenomen.
* Hiermee wordt een onbeperkt aantal variabelen toegestaan, maar door curatie kan worden beperkt welke variabelen aan gebruikers worden blootgesteld
* Hiermee kunt u de containers voor gebeurtenissen, sessies en personen een aangepaste naam geven.
* Ondersteunt aangepaste kalenderopties.

Een gegevensweergave doet dit niet:

* Rechtstreeks een middel verstrekken om rapportsuites of andere datasets te combineren. In plaats daarvan, worden de datasets gecombineerd met in een verbinding van de Customer Journey Analytics. De gecombineerde gegevens van de verbinding van de Customer Journey Analytics zijn beschikbaar voor gebruik in alle gegevensmeningen die op die verbinding worden gebaseerd.

## Adobe Experience Platform-sandboxen

Zie voor meer informatie: [Overzicht van sandboxen](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=nl).

Een Adobe Experience Platform-sandbox:

* Biedt een manier om één Adobe Experience Platform-instantie in aparte virtuele omgevingen te verdelen (ontwikkelen, testen, stadium, productie, enz.) helpen bij het ontwikkelen en ontwikkelen van toepassingen voor digitale ervaringen.
* Kan worden beschouwd als een container die alle gegevens en toepassingen voor een bepaalde omgeving bevat.

Een Adobe Experience Platform-sandbox doet dit niet:

* Verstrek gelijkaardige functies zoals virtuele rapportseries, de verbindingen van de Customer Journey Analytics of gegevensmeningen.
* Op zichzelf combineert het rapport reeksen met of zonder andere datasets. De gegevenssets in een sandbox kunnen echter worden gecombineerd binnen een Customer Journey Analytics-verbinding.

Let op:

* Gegevens van verschillende sandboxen kunnen niet worden gecombineerd binnen de Customer Journey Analytics.
* De verbinding van de Bron Analyse verzendt rapportreeksgegevens _in_ een specifieke sandbox. Elk rapportpakket kan als bron voor één enkele zandbak worden gevormd. Zie de [Documentatie over de bronaansluiting voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) voor meer informatie .
