---
title: Veelgestelde vragen over analyse met instructies
description: Veelgestelde vragen over de analyse met instructies.
exl-id: 32bfce23-a59c-45cb-b1cd-82f048fb13d2
feature: Guided Analysis
source-git-commit: 2b1e0ce53016634e0cb32f9256fa48e02f2a5323
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Veelgestelde vragen over analyse met instructies

Veelgestelde vragen over de analyse met instructies.

+++**Hoe kan mijn organisatie worden voorzien voor Geleide analyse?**

Analyse met instructies is een betaalde aanvulling op Customer Journey Analytics. Neem contact op met het accountteam van Adobe als u deze invoegtoepassing wilt gaan gebruiken.

+++

+++**Welke implementatiewijzigingen zijn vereist om de analyse met instructies te gebruiken?**

Als u vandaag reeds Customer Journey Analytics gebruikt, zijn geen extra implementatieveranderingen nodig. De geleide analyse gebruikt zelfde [Gegevensweergaven](../data-views/data-views.md) en [Verbindingen](../connections/overview.md) zoals andere CJA-interfaces zoals [Analysis Workspace](../analysis-workspace/home.md).

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

* **Analysis Workspace is een op dimensies gerichte ervaring.** Tabellen bestaan meestal uit dimensionale rijen, terwijl kolommen doorgaans metriek zijn. U kunt filters toepassen in zowel rijen als kolommen om de gewenste gegevens te verkrijgen.

* **De geleide analyse is een gebeurtenis-gecentreerde ervaring.** Elke analyse begint met het selecteren van gebeurtenissen, waarna dimensies en filters kunnen worden toegevoegd om die gebeurtenisgegevens te verfijnen.

![Structuur](assets/structure.png)

Kijk in het volgende voorbeeld naar de gegevens op de homepage van uw website. Teams stellen gelijkaardige vragen, maar de analyse benadering kan verschillend zijn.

* Een typisch afmetingsgecentreerde benadering van Analysis Workspace zou zijn: &quot;Laten we naar de homepage kijken en zien hoeveel paginameningen het ontving.&quot;

  ![Dimension gecentreerd](assets/dimension-centered.png)

* Een typisch gebeurtenis-gecentreerde Geleide analyse benadering zou zijn, &quot;hoeveel gebruikers de homepage hebben bekeken?&quot;

  ![Gebeurtenis gecentreerd](assets/event-centered.png)

+++
