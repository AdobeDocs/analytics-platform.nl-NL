---
title: Virtuele rapportsuites, de meningen van Gegevens, de zandbakken van Adobe Experience Platform, en de de bronschakelaar van de Analyse
description: Meer informatie over virtuele-rapporteringsomgevingen en sandboxomgevingen.
exl-id: 8f0358d1-85fe-4e1e-8724-8a7caa16328c
feature: Basics
role: User
source-git-commit: eb9b749a5c61da3b4b5d2eeeed93bf5e4702a415
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Virtuele rapportsuites, de meningen van Gegevens, de zandbakken van Adobe Experience Platform, en de de bronschakelaar van de Analyse

Adobe biedt verschillende manieren om virtuele rapportageomgevingen en sandboxomgevingen te maken. Het is nuttig om de gelijkenissen en de verschillen tussen de volgende eigenschappen te begrijpen en hoe deze eigenschappen op de [ bron van Analytics schakelaar ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) betrekking hebben:

* Adobe Analytics Virtual Report-suites
* Customer Journey Analytics-gegevensweergaven
* Adobe Experience Platform-sandboxen

## Adobe Analytics Virtual Report-suites

Voor meer informatie, zie: [ het Virtuele overzicht van de rapportreeksen ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html).

Een virtuele rapportsuite:

* Kan worden gebaseerd op Adobe Analytics-segmenten.
* Kan op niet-destructieve wijze op zowel historische als nieuwe gegevens worden toegepast.
* Staat u toe om één of vele virtuele meningen bovenop een het rapportreeks van Adobe Analytics voor gebruik door verschillende bedrijfsteams tot stand te brengen.
* Kan worden gebruikt om de toegang tot en het beheer van verschillende soorten gegevens voor verschillende gebruikers in Adobe Analytics te regelen.
* Verstrekt facultatieve [ rapport-tijd verwerkings ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html) mogelijkheden voor Adobe Analytics. In dit geval kan een virtuele rapportsuite worden gebruikt om een aangepaste definitie voor &quot;visit&quot; te maken.
* Wordt toegepast bij rapportruntime, gelijkend op segmentevaluatie. Dit is _nadat_ de gegevens binnen Adobe Analytics zijn verzameld en zijn opgeslagen.
* Wordt vereist voor [ Analytics van het Apparaat ](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html) in Adobe Analytics.
* Beschikt over hetzelfde aantal variabelen voor gebruik als standaard Analytics Report Suite (250 eVars, 250 props, 1000 events), hoewel de virtuele reekscuratie van het rapport kan beperken welke variabelen aan gebruikers worden blootgesteld.
* Ondersteunt aangepaste kalenderopties.

Een virtuele rapportsuite is niet:

* Een middel om de rapportsuites te combineren.
* Beschikbaar in Adobe Analytics Data Warehouse.
* Beschikbaar als bron voor gegevensstromen in Adobe Experience Platform via de bronschakelaar van de Analytics. Alleen volledige (niet-virtuele) rapportsuites zijn beschikbaar voor gebruik met de bronconnector van Analytics.


## Customer Journey Analytics-gegevensweergaven

Voor meer informatie, zie: [ overzicht van de meningen van Gegevens ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html).

Een gegevensweergave:

* Kan worden gebaseerd op Customer Journey Analytics-segmenten.
* Kan op niet-destructieve wijze op zowel historische als nieuwe gegevens worden toegepast.
* Hiermee kunt u een of meer virtuele weergaven vóór een Customer Journey Analytics-verbinding maken, voor gebruik door verschillende zakelijke teams.
* Kan worden gebruikt om de toegang tot en het beheer van verschillende soorten gegevens voor verschillende gebruikers in Customer Journey Analytics te regelen.
* Biedt krachtige, niet-destructieve opties voor het transformeren en verbeteren van gegevens die via een Customer Journey Analytics-verbinding naar Customer Journey Analytics komen.
* Is gebaseerd op de rapport-tijd verwerkingsmogelijkheden van Customer Journey Analytics.
* Hiermee kunnen gebruikers een aangepaste definitie maken voor &quot;sessie&quot;.
* Wordt toegepast bij rapportruntime, gelijkend op een segmentevaluatie. Dit is _nadat_ de Schakelaar van Source (Adobe Analytics of andere) gegevens aan een dataset in het de gegevensmeer van Adobe Experience Platform heeft geschreven, en _nadat_ de gegevens in Customer Journey Analytics via een verbinding van Customer Journey Analytics zijn opgenomen.
* Hiermee wordt een onbeperkt aantal variabelen toegestaan, maar door curatie kan worden beperkt welke variabelen aan gebruikers worden blootgesteld
* Hiermee kunt u de containers voor gebeurtenissen, sessies en personen een aangepaste naam geven.
* Ondersteunt aangepaste kalenderopties.

Een gegevensweergave doet dit niet:

* Rechtstreeks een middel verstrekken om rapportsuites of andere datasets te combineren. In plaats daarvan worden datasets gecombineerd met in een Customer Journey Analytics-verbinding. De gecombineerde gegevens van de verbinding van Customer Journey Analytics zijn beschikbaar voor gebruik in alle gegevensmeningen die op die verbinding worden gebaseerd.

## Adobe Experience Platform-sandboxen

Voor meer informatie, zie: [ het overzicht van Sandboxen ](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=nl).

Een Adobe Experience Platform-sandbox:

* Biedt een manier om één Adobe Experience Platform-instantie in afzonderlijke virtuele omgevingen (ontwikkelen, testen, testen, stadium, productie, enz.) te verdelen om toepassingen voor digitale ervaringen te ontwikkelen en te ontwikkelen.
* Kan worden beschouwd als een container die alle gegevens en toepassingen voor een bepaalde omgeving bevat.

Een Adobe Experience Platform-sandbox doet dit niet:

* Verstrek gelijkaardige functies zoals virtuele rapportseries, de verbindingen van Customer Journey Analytics of gegevensmeningen.
* Op zichzelf combineert het rapport reeksen met of zonder andere datasets. De gegevenssets in een sandbox kunnen echter worden gecombineerd binnen een Customer Journey Analytics-verbinding.

Let op:

* Gegevens van verschillende sandboxen kunnen niet worden gecombineerd in Customer Journey Analytics.
* De schakelaar van Source Analytics verzendt rapportreeksgegevens _in_ een specifieke zandbak. Elk rapportpakket kan als bron voor één enkele zandbak worden gevormd. Zie de [ documentatie van de bronschakelaar van de Analyse ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) voor meer details.
