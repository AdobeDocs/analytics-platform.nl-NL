---
description: Het ontleden van de tijd neemt de timestamp van verzamelde hits en breekt het in zinvollere dimensies, zoals "Uren van Dag" of "Dag van Week".
title: Tijduitsplitsende dimensies
uuid: c9fa7921-aa57-483c-b2f9-da55013ada17
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 3%

---


# Tijduitsplitsende dimensies

Het ontleden van de tijd neemt de timestamp van verzamelde hits en breekt het in zinvollere dimensies, zoals &quot;Uren van Dag&quot; of &quot;Dag van Week&quot;.

De tijd-scheidende afmetingen zijn gebaseerd op de tijdzone van de rapportreeks of virtuele rapportreeks. Deze afmetingen zijn beschikbaar in de Werkruimte van de Analyse en kunnen helpen om de volgende vragen te beantwoorden:

* Over een grote datumwaaier, wat is de populairste tijd van dag voor bezoekers om tot mijn plaats of app toegang te hebben?
* Zijn er dagen van de week of uren van de dag waarop de omzetting op mijn plaats of app hoger is?
* Hoe verhoudt mijn weekendverkoop zich tot mijn weekdagverkoop?
* Verleent een bepaalde marketing campagne hogere omzettingen in de ochtend, of in de namiddag?

>[!NOTE]
>
>De tijd-scheidende afmetingen zijn slechts beschikbaar in de Werkruimte van de Analyse. Om tijd-paring afmetingen in andere oplossingen van de Analyse te gebruiken, kunt u uitvoeren [getTimeParting plug-in](https://docs.adobe.com/content/help/en/analytics/implementation/vars/plugins/gettimeparting.html).

De tijd-scheidende afmetingen in de Werkruimte van de Analyse omvatten:

| Afmetingen | Voorbeeldwaarden |
|--- |--- |
| Uur van de dag | 0-23 |
| AM/PM | AM, PM |
| Weekdag | Maandag, dinsdag, woensdag, donderdag, vrijdag, zaterdag, zondag |
| Weekend/Weekdag | Weekend, Weekdag |
| Dag van Maand | 1-31 |
| Maand van het Jaar | januari-december |
| Dag van Jaar | 1-366 |
| Kwartaal van het jaar | Q1, Q2, Q3, Q4 |
