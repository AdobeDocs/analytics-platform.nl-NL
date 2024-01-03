---
title: Veelgestelde vragen over analyse met instructies
description: Veelgestelde vragen over de analyse met instructies.
exl-id: b6f92d47-6c09-4338-9dc5-b30bbfbe9f7f
feature: Guided Analysis
keywords: productanalyse
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Veelgestelde vragen over analyse met instructies

Veelgestelde vragen over de analyse met instructies.

+++**Hoe kan mijn organisatie worden voorzien voor Geleide analyse?**

Analyse met instructies maakt deel uit van Adobe Product Analytics, een betaalde aanvulling op de Customer Journey Analytics. Neem contact op met het accountteam van de Adobe als u deze invoegtoepassing wilt gaan gebruiken.

+++

+++**Welke implementatiewijzigingen zijn vereist om de analyse met instructies te gebruiken?**

Als u vandaag al Customer Journey Analytics gebruikt, zijn geen extra implementatieveranderingen nodig. De geleide analyse gebruikt zelfde [Gegevensweergaven](../data-views/data-views.md) en [Verbindingen](../connections/overview.md) zoals andere CJA-interfaces zoals [Analysis Workspace](../analysis-workspace/home.md).

Als u eindgebruikers wilt laten profiteren van de analyse met instructies, kunt u het beste een krachtig gebeurtenisschema en beheerstrategie toepassen in Adobe Experience Platform en [Gegevensweergaven](../data-views/data-views.md).

+++

+++**Wanneer moet u de analyse met instructies of Analysis Workspace gebruiken?**

**Analyse met instructies** kunnen gebruikers helpen snel inzicht van hoge kwaliteit te krijgen. Het is nuttig voor productteams, gebruikers die betrouwbaarder met gegevens willen werken, en zelfs analisten als eerste begin aan diepere analyse.

**[Analysis Workspace](../analysis-workspace/home.md)** Dit is een vrijere ruimte waarmee u verder in de gegevens kunt duiken om meer inzichten aan het licht te brengen. Het is handig voor analisten en veeleisende gebruikers die de gegevens goed begrijpen en er diep in willen duiken.

+++

+++**Hoe vergelijk de terminologie tussen Guided analysis en Analysis Workspace?**

De geleide analyse gebruikt termijnen die vaker onder productteams worden gebruikt. U kunt naar deze tabel verwijzen wanneer u schakelt tussen de analyse Met instructies en [Analysis Workspace](../analysis-workspace/home.md).

| Geleide analyseperiode | Analysis Workspace term |
| --- | --- |
| Gebeurtenis | Metrisch |
| Gebruikers | Mensen |
| Eigenschap | Dimension |
| Waarde | Dimension-item |
| Segment | Filter |

{style="table-layout:auto"}

+++

+++**Wat zijn enkele verschillen ten aanzien van de rapportage van Guided analysis en Analysis Workspace?**

while [Analysis Workspace](../analysis-workspace/home.md) en de analyse Met instructies gebruikt de zelfde onderliggende gegevens, de manier dat elk hulpmiddel u toelaat om vragen van die gegevens te vormen is verschillend.

* **Analysis Workspace is een op dimensies gerichte ervaring.** Tabellen bestaan meestal uit dimensionale rijen, terwijl kolommen doorgaans metriek zijn. Filters kunnen zowel in rijen als in kolommen worden toegepast om de gewenste gegevens te verkrijgen.

* **Analyse met instructies is een gebeurtenis en gebruikergerichte ervaring.** Elke analyse begint met het selecteren van gebeurtenissen, waarna dimensies en filters kunnen worden toegevoegd om die gebeurtenisgegevens te verfijnen.

![Analysis Workspace- en Guided-analyseweergaven](assets/structure.png)

Kijk in het volgende voorbeeld naar de gegevens op de homepage van uw website. Teams stellen gelijkaardige vragen, maar de analyse benadering kan verschillend zijn.

* Een typisch afmetingsgecentreerde benadering van Analysis Workspace zou zijn: &quot;Laten we naar de homepage kijken en zien hoeveel paginameningen het ontving.&quot;

  ![Dimension gecentreerd](assets/dimension-centered.png)

* Een typische gebeurtenis en gebruiker-gecentreerde Geleide analyse zou benadering zijn: &quot;Hoeveel gebruikers hebben onze homepage bezocht?&quot;

  ![Gebeurtenis gecentreerd](assets/event-centered.png)

+++
