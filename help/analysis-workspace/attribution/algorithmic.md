---
title: Algoritmische attributie
description: Details over het algoritmische attributiemodel.
exl-id: ce174253-4864-4fb0-8a96-a134a9fc9fba
source-git-commit: f74b5e79b6713050869301adb95e2a73705330da
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# Algoritmische attributie

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

>[!NOTE]
>
>**[!UICONTROL Algorithmic attribution]** wordt momenteel beperkt getest. Zie [Adobe Analytics-functiereleases](https://experienceleague.adobe.com/docs/analytics/landing/an-releases.html) voor meer informatie.

Het algoritme [attributiemodel](models.md) in Analysis Workspace verschilt van andere modellen in die zin dat het statistische technieken gebruikt om krediet toe te wijzen over de dimensiepunten in uw rapport of vrije lijst. Zoals alle andere attributiemodellen in Analysis Workspace, kan het op om het even welke afmeting of metrisch worden gebruikt en steunt onbeperkte filters en onderverdelingen en verdeelt 100% van omzettingen aan de afmeting(en) in de lijst (ook genoemd geworden &quot;fractionele&quot;attributie).

Het algoritme dat wordt gebruikt voor attributie is gebaseerd op de Harsanyi Dividend van coöperatieve speltheorie. Het dividend van Harsanyi is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnaar) voor het verdelen van krediet onder spelers in een spel met ongelijke bijdragen aan de uitkomst.

Op hoog niveau wordt bij de berekening van de conversiekrediet voor elk aanraakpunt elk van de marketingaanraakpunten binnen een terugkijkvenster beschouwd als een coalitie van spelers waaraan een overschot op billijke wijze moet worden verdeeld. De overtollige verdeling van elke coalitie wordt bepaald volgens het overschot dat eerder door elke subcoalitie (of eerder deelnemende dimensie-items) recursief werd gecreëerd. Raadpleeg voor meer informatie de originele documenten van John Harsanyi en Lloyd Shapley:

* Shapley, Lloyd S. (1953). Een waarde voor spelletjes van één persoon. *Bijdragen aan de Theory of Games, 2(28)*, 307-317.
* Harsanyi, John C. (1963). Een vereenvoudigd onderhandelingsmodel voor het on-person coöperatieve spel. *International Economic Review 4(2)*, 194-220.

>[!NOTE]
>
>Het resultaat van Algorithmic-toewijzing verschilt alleen van andere modellen wanneer er meerdere aanraakpunten bestaan binnen het opgegeven terugzoekvenster. Conversies met één aanraakpunt krijgen 100% krediet ongeacht het attributiemodel.
