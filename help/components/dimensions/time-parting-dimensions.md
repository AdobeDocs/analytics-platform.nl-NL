---
description: Bij tijdpartering wordt de tijdstempel van verzamelde hits gebruikt en wordt de reeks in betekenisvollere afmetingen opgedeeld, zoals "Uur van dag" of "Dag van week".
title: Tijduitsplitsende dimensies
uuid: c9fa7921-aa57-483c-b2f9-da55013ada17
translation-type: tm+mt
source-git-commit: 0c5bd5ce0b0ba4ba758a1ef1adf5a4a519e9cf8c
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 3%

---


# Tijduitsplitsende dimensies

Bij tijdpartering wordt de tijdstempel van verzamelde hits gebruikt en wordt de reeks in betekenisvollere afmetingen opgedeeld, zoals &quot;Uur van dag&quot; of &quot;Dag van week&quot;.

De tijd-ontledende dimensies zijn gebaseerd op de tijdzone van de rapportreeks of virtuele rapportreeks. Deze afmetingen zijn beschikbaar in Analysis Workspace en kunnen helpen om de volgende vragen te beantwoorden:

* Wat is, over een groot datumbereik, de populairste tijd van dag voor bezoekers om tot mijn plaats of app toegang te hebben?
* Zijn er dagen van de week of uren van de dag waarop de conversie hoger is op mijn site of app?
* Hoe vergelijk mijn weekendverkopen met mijn weekdagverkopen?
* Produceert een bepaalde marketing campagne hogere omzettingen in de ochtend, of in de namiddag?

>[!NOTE] De afmetingen voor tijdpartering zijn alleen beschikbaar in Analysis Workspace. Als u de afmetingen voor tijdpartering wilt gebruiken in andere Analytics-oplossingen, kunt u de plug-in [getTimeParting implementeren](https://docs.adobe.com/content/help/en/analytics/implementation/vars/plugins/gettimeparting.html).

Afmetingen van tijdpartering in Analysis Workspace zijn onder andere:

| Dimensie | Voorbeeldwaarden |
|--- |--- |
| Uur van dag | 0-23 |
| AM/PM | AM, PM |
| Weekdag | Maandag, dinsdag, woensdag, donderdag, vrijdag, zaterdag, zondag |
| Weekend/Weekdag | Weekend, weekdag |
| Dag van Maand | 1-31 |
| Maand van jaar | Januari-december |
| Dag van het Jaar | 1-366 |
| Kwartaal van jaar | Q1, Q2, Q3, Q4 |
