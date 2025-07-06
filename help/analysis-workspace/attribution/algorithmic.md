---
title: Algorithmic Attribution
description: Begrijp de details van het algoritmische attributiemodel.
feature: Attribution
role: User, Admin
exl-id: dd2b2a5b-9c36-4534-999f-f96604f29eab
source-git-commit: ce4a21b1a1e89f14316a92fbdce38281db61e666
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Algorithmic, toewijzing

Het de attributenmodel van het Algorithmic [ ](models.md) in Analysis Workspace verschilt van andere modellen in die zin dat het statistische technieken gebruikt om krediet over de afmetingspunten in uw rapport of vrije vormlijst toe te wijzen. Net als alle andere attributiemodellen in Analysis Workspace, kan algoritmische attributie worden gebruikt voor elke dimensie of metrisch. Algorithmic-toewijzing ondersteunt onbeperkte segmentatie en uitsplitsingen en verdeelt 100% van de conversies naar een of meer dimensies in de tabel (ook wel &quot;fractionele&quot; attributie genoemd).


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Algorithmic attributie ](https://video.tv.adobe.com/v/36205?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


Het algoritme dat wordt gebruikt voor attributie is gebaseerd op de Harsanyi Dividend van coöperatieve speltheorie. Het dividend van Harsanyi is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnaar) om krediet te verstrekken onder spelers in een spel met ongelijke bijdragen aan de uitkomst.

Op hoog niveau wordt bij de berekening van de toerekening van het conversiecrediet voor elk aanraakpunt elk van de marketingaanraakpunten binnen een terugkijkvenster beschouwd als een coalitie van spelers. Voor die coalitie van spelers moet een overschot billijk worden verdeeld. De overtollige verdeling van elke coalitie is afhankelijk van het overschot dat elke subcoalitie eerder recursief heeft gecreëerd.

Raadpleeg voor meer informatie de originele documenten van John Harsanyi en Lloyd Shapley:

* Shapley, Lloyd S.1953. Een waarde voor spelletjes van één persoon. *bijdragen aan de Theorie van Spelen, 2 (28)*, 307-317.
* Harsanyi, John C. (1963) Een vereenvoudigd onderhandelingsmodel voor het on-person coöperatieve spel. *Internationale Economische Controle 4 (2)*, 194-220.

>[!NOTE]
>
>Het resultaat van Algorithmic-toewijzing verschilt alleen van andere modellen wanneer er meerdere aanraakpunten bestaan binnen het opgegeven terugzoekvenster. Conversies met één aanraakpunt krijgen 100% krediet ongeacht het attributiemodel.
