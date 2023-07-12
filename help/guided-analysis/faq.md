---
title: Veelgestelde vragen over analyse met instructies
description: Veelgestelde vragen over de analyse met instructies.
exl-id: 32bfce23-a59c-45cb-b1cd-82f048fb13d2
feature: Guided Analysis
source-git-commit: 23d3e6a9662cda932a376c09849ab078d22830dc
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Veelgestelde vragen over analyse met instructies

{{release-limited-testing}}

Veelgestelde vragen over de analyse met instructies.

+++**Beschikt iedereen over een analyse met instructies?**

Neen; Analyse met instructies is een betaalde aanvulling op Customer Journey Analytics. Neem contact op met het accountteam van Adobe als u deze invoegtoepassing wilt gaan gebruiken.

+++

+++**Welke implementatiewijzigingen zijn vereist om de analyse met instructies te gebruiken?**

Als u Analysis Workspace al in Customer Journey Analytics gebruikt, zijn er geen aanvullende implementatiewijzigingen nodig. Voor de analyse met instructies worden dezelfde gegevensweergaven en -verbindingen gebruikt als voor Analysis Workspace. Het proces om aan boord te hebben en om het even welk projecttype te gebruiken is identiek voor al Customer Journey Analytics, met inbegrip van Geleide analyse.

+++

+++**Hoe verhouden termen zich tot elkaar binnen en buiten de analyse met instructies?**

Bij een analyse met instructies worden termen gebruikt die vaker worden gebruikt in de productanalyse. U kunt naar deze tabel verwijzen bij het schakelen tussen de analyse met instructies en Analysis Workspace.

| Geleide analyseperiode | Analysis Workspace term |
| --- | --- |
| Gebeurtenis | Metrisch |
| Gebruikers | Mensen |
| Eigenschap | Dimension |
| Waarde | Dimension-item |
| Segment | Filter |

{style="table-layout:auto"}

+++

+++**Wat zijn enkele verschillen ten aanzien van de wijze waarop Analysis Workspace en Guided analysis de benadering bepalen?**

Hoewel Analysis Workspace en de analyse met instructies dezelfde onderliggende gegevens gebruiken, is de manier waarop u met elk gereedschap query&#39;s voor die gegevens kunt maken anders.

* **Analysis Workspace is een op dimensies gerichte ervaring.** Tabellen bestaan meestal uit rijen voor dimensiepunten, terwijl kolommen meestal metriek zijn. U kunt filters op zowel rijen als kolommen toepassen om de gewenste gegevens te verkrijgen.

* **De geleide analyse is een gebeurtenis-gecentreerde ervaring.** De visualisaties richten zich op gebeurtenissen, gebruikend afmetingen en filters om die gegevens aan te vullen.

![Structuur](assets/structure.png)

Kijk in het volgende voorbeeld naar de gegevens op de homepage van uw website. Teams stellen gelijkaardige vragen, maar de analyse benadering kan verschillend zijn.

* Een typisch afmetingsgecentreerde benadering van Analysis Workspace zou zijn: &quot;Hoeveel paginameningen heeft de homepage ontvangen?&quot;

  ![Dimension gecentreerd](assets/dimension-centered.png)

* Een typisch gebeurtenis-gecentreerde Geleide analyse benadering zou zijn, &quot;hoeveel gebruikers de homepage hebben bekeken?&quot;

  ![Gebeurtenis gecentreerd](assets/event-centered.png)

Deze instructies illustreren twee verschillende methoden om hetzelfde rapport te bereiken, afhankelijk van uw gebeurtenisbeheerstrategie.

+++
