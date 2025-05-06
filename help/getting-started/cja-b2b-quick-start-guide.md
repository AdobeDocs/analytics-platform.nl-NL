---
title: Customer Journey Analytics B2B-handleiding voor snel starten
description: Snelstartgids voor de B2B edition of Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Basics
role: User, Admin
badgePremium: label="B2B edition"
exl-id: ff8d419e-5cc6-4e1b-8cf8-9dbaa8054179
source-git-commit: 326a82e93c0c8d57db224023ed5f3a7ab94a8997
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---


# B2B edition-handleiding voor snel starten

{{draft-b2b}}

Als u Customer Journey Analytics B2B edition wilt implementeren, moet u eerst de specifieke concepten en functies van B2B begrijpen. Ook moet u bekend zijn met de traditionele workflow om Customer Journey Analytics te implementeren.

In dit document wordt de nadruk gelegd op de specifieke workflow voor de implementatie van Customer Journey Analytics.

## Vereisten

Voor de implementatie van Customer Journey Analytics B2B edition gelden de volgende voorwaarden:

* U hebt de noodzakelijke [ toegangscontrole en de toestemmingen ](/help/technotes/access-control.md) om beleidstaken in Customer Journey Analytics te verstrekken.
* U hebt het invoegpakket voor Customer Journey Analytics B2B edition aangeschaft.


## Workflow

| Taak | Details |
| --- | --- |
| **Stap 1: Krijg B2B- gegevens in Experience Platform** | Deze stap, uitgevoerd in Experience Platform, omvat verschillende substappen:<ul><li>**Stap 1a: Bereid uw gegevensschema** voor: Het Model van de Gegevens van de Ervaring van Adobe van het gebruik [ (XDM) ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) om B2B- gegevens te standaardiseren en [ schema&#39;s ](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/schemas/b2b) voor uw B2B- gegevens te bepalen.</li><li>**Stap 1b: Creeer een dataset die op het schema** wordt gebaseerd: De gegevens in Platform bestaan uit datasets, zoals rekeningsgegevens, opportuniteitsgegevens, het kopen van groepsgegevens, campagnegegevens, marketing lijstgegevens, e-maildatasets, de datasets van CRM, POS datasets, en meer. Elke dataset bestaat uit een schema en partijen gegevens. U kunt [ tot een dataset in Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/create-datasets.html) leiden.</li><li>**Stap 1c: Samenvatting gegevens in Experience Platform**: U hebt [ verscheidene opties ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home).</li></ul> |
| **Stap 2: Creeer verbindingen tussen platformdatasets en Customer Journey Analytics** | Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over de datasets van Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Workspace vestigen. U hebt extra opties wanneer u een verbinding met de B2B edition vormt. <br> zie [ creeer of geef een verbinding ](/help/connections/create-connection.md) uit. |
| **Stap 3: Creeer gegevensmeningen** | Een gegevensmening is gefilterde a ** mening van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, toewijzing en meer. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen. U hebt extra opties wanneer u een gegevensmening vormt wanneer u de B2B edition hebt.<br> zie [ een gegevensmening ](/help/data-views/create-dataview.md) creëren. |
| **Stap 4: Rapport over uw dwars-kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de B2B gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br> zie [ basisanalyse ](/help/analysis-workspace/perform-basic-analysis.md) uitvoeren en [ geavanceerde analyse ](/help/analysis-workspace/perform-adv-analysis.md) uitvoeren. |

<!--

## Use Case

The [B2B Use Case ](../data-ingestion/data-ingestion.md) document provides an example use case on how to implement Customer  Journey Analytics B2B Edition.

-->