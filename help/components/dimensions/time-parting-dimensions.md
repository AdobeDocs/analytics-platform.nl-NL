---
description: Bij tijdpartering wordt de tijdstempel van verzamelde gebeurtenissen gebruikt en wordt deze in meer betekenisvolle dimensies gesplitst, zoals "Uur van dag" of "Dag van week".
title: Afmetingen van tijd tot tijd
feature: Dimensions
exl-id: 5c3c2867-58de-4765-a4e1-91eac1891b38
role: User
source-git-commit: 6a279ac39e6b94200ff93ac1a3796d202e6349c7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Afmetingen van tijd-paring in Analysis Workspace

Het ontleden van de tijd neemt timestamp van verzamelde gebeurtenissen en breekt het in zinvollere dimensies, zoals **Uur van Dag** of **Dag van Week**.

De tijd-ontledende afmetingen zijn gebaseerd op de tijdzone van de gegevensmening. Deze afmetingen zijn beschikbaar in Analysis Workspace en kunnen helpen om de volgende vragen te beantwoorden:

* Wat is, over een groot datumbereik, de populairste tijd van dag voor mensen om tot mijn plaats of app toegang te hebben?
* Zijn er dagen van de week of uren van de dag waarop de conversie hoger is op mijn site of app?
* Hoe vergelijk mijn weekendverkopen met mijn weekdagverkopen?
* Produceert een bepaalde marketing campagne hogere omzettingen in de ochtend, of in de namiddag?

| Dimension | Voorwaarden |
|--- |--- |
| **[!UICONTROL Hour of Day]** | 0-23 |
| **[!UICONTROL AM/PM]** | AM, PM |
| **[!UICONTROL Day of Week]** | Maandag, dinsdag, woensdag, donderdag, vrijdag, zaterdag, zondag |
| **[!UICONTROL Weekday/Weekend]** | Weekdag, Weekend |
| **[!UICONTROL Day of Month]** | 1-31 |
| **[!UICONTROL Month of Year]** | Januari-december |
| **[!UICONTROL Day of Year]** | 1-366 |
| **[!UICONTROL Quarter of Year]** | Q1, Q2, Q3, Q4 |
