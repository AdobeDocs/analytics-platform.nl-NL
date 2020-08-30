---
title: Algoritmische attributie
description: Gegevens over het algoritmische toewijzingsmodel.
translation-type: tm+mt
source-git-commit: e32311ce4975107e1b7ca2cb2eaadc2c68a93c92
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 4%

---


# Algoritmische attributie

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

>[!NOTE]
>
>**[!UICONTROL Algorithmic attribution]** wordt momenteel beperkt getest. Zie [Adobe Analytics-functies](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html) voor meer informatie .

Het algoritme [toewijzingsmodel](models.md) in de Werkruimte van de Analyse verschilt van andere modellen in zoverre dat het statistische technieken gebruikt om krediet over de afmetingspunten in uw rapport of freeform lijst toe te wijzen. Zoals alle andere attributiemodellen in de Werkruimte van de Analyse, kan het op om het even welke afmeting of metrisch worden gebruikt en steunt onbeperkte segmentatie en onderverdelingen en verdeelt 100% van omzettingen in de afmeting(s) in de lijst (ook genoemd geworden &quot;fractionele&quot;attributie).

Het algoritme dat voor attributie wordt gebruikt, is gebaseerd op het Harsanyi Dividend van de coöperatieve speltheorie. Het Harsanyi-dividend is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnares econoom) voor het verdelen van krediet onder spelers in een spel met ongelijke bijdragen aan de uitkomst.

Op een hoog niveau wordt bij de berekening van de toerekening van het conversiekrediet voor elk touchpoint elk van de marketingtouchpoints in een terugkijkvenster beschouwd als een coalitie van spelers waaraan een overschot billijk moet worden verdeeld. De overtollige verdeling van elke coalitie wordt bepaald op basis van het overschot dat eerder door elke subcoalitie (of eerder deelnemende dimensiepunten) recursief werd gecreeerd. Voor meer details, zie de originele documenten van John Harsanyi en Lloyd Shapley:

* Shapley, Lloyd S. (1953). Een waarde voor persoonlijke spelletjes. *Bijdragen aan de Theorie van de Spelen, 2(28)*, 307-317.
* Harsanyi, John C. (1963). Een vereenvoudigd onderhandelingsmodel voor het &quot;n-person&quot;-coöperatief spel. *Internationale economische evaluatie 4(2)*, 194-220.

>[!NOTE]
>
>Het resultaat van Algoritmische attributie verschilt slechts van andere modellen wanneer veelvoudige touchpoints binnen het bepaalde terugkijkvenster bestaan. De versies met één enkel touchpoint ontvangen 100% krediet ongeacht attributiemodel.
