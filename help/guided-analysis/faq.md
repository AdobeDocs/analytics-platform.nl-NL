---
title: Veelgestelde vragen over analyse met instructies
description: Veelgestelde vragen voor analyse met instructies.
exl-id: b6f92d47-6c09-4338-9dc5-b30bbfbe9f7f
feature: Guided Analysis
keywords: productanalyse
role: User
source-git-commit: d6f26da108a2c840838ac71d9b98f45cd145ad3e
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Veelgestelde vragen over analyse met instructies

Veelgestelde vragen voor geleide analyse.

+++**heeft mijn organisatie toegang tot geleide analyse?**

Alle Customers Journey Analytics bevatten weergaven met instructies voor de analyse. Zie de [ provisioning ](overview.md#provisioning) sectie op de overzichtspagina om meer over de meningen te leren die uw pakket CJA ontgrendelt.

+++

+++**Welke implementatieveranderingen worden vereist om geleide analyse te gebruiken?**

Als u vandaag al Customer Journey Analytics gebruikt, zijn geen extra implementatieveranderingen nodig. De geleide analyse gebruikt de zelfde [ meningen van Gegevens ](../data-views/data-views.md) en [ Verbindingen ](../connections/overview.md) zoals andere interfaces CJA zoals [ Analysis Workspace ](../analysis-workspace/home.md).

Om uw eind toe te laten - gebruikers om met geleide analyse het meest succesvol te zijn, wordt het geadviseerd u een sterk gebeurtenisschema en beheersstrategie op zijn plaats in Adobe Experience Platform en [ meningen van Gegevens ](../data-views/data-views.md) hebt.

+++

+++**wanneer zou u geleide analyse of Analysis Workspace moeten gebruiken?**

**Geleide analyse** kan gebruikers helpen snel inzichten van hoge kwaliteit krijgen. Het is nuttig voor productteams, gebruikers die betrouwbaarder met gegevens willen werken, en zelfs analisten als eerste begin aan diepere analyse.

**[Analysis Workspace](../analysis-workspace/home.md)** is een meer vrije ruimte die u verder in de gegevens laat duiken om meer inzichten te ontdekken. Het is handig voor analisten en veeleisende gebruikers die de gegevens goed begrijpen en er diep in willen duiken.

+++

+++**hoe vergelijkt de terminologie tussen geleide analyse en Analysis Workspace?**

De geleide analyse en [ Analysis Workspace ](../analysis-workspace/home.md) richten zich op de meeste zeer belangrijke terminologie, met een paar kleine verschillen.

| Geleide analyseperiode | Analysis Workspace term |
| --- | --- |
| Gebeurtenis (binair 1/0 metrisch) | Metrisch |
| Gebruikers | Mensen |
| Dimension | Dimension |
| Dimension-item | Dimension-item |
| Segment | Filter |
| Filter | Rapportfilter |
| Berekende metrisch, Metrisch | Berekende metrische waarde |

{style="table-layout:auto"}

+++

+++**wat zijn sommige verschillen in hoe geleid analyse en de benadering die van Analysis Workspace rapporteert?**

Terwijl [ Analysis Workspace ](../analysis-workspace/home.md) en geleide analyse de zelfde onderliggende gegevens gebruiken, de manier dat elk hulpmiddel u toelaat om vragen van die gegevens te vormen is verschillend.

* **Analysis Workspace is een dimensie-gecentreerde ervaring.** Tabellen bestaan meestal uit dimensionale rijen, terwijl kolommen meestal metriek zijn. Filters kunnen zowel in rijen als in kolommen worden toegepast om de gewenste gegevens te verkrijgen.

* **Geleide analyse is een gebeurtenis en gebruiker-gecentreerde ervaring.** Elke analyse begint met het selecteren van gebeurtenissen, waarna dimensies en filters kunnen worden toegevoegd om die gebeurtenisgegevens te verfijnen.

![ Analysis Workspace en geleide analysemeningen ](assets/structure.png){style="border:1px solid gray"}

Kijk in het volgende voorbeeld naar de gegevens op de homepage van uw website. Teams stellen gelijkaardige vragen, maar de analyse benadering kan verschillend zijn.

* Een typisch afmetingsgecentreerde benadering van Analysis Workspace zou zijn: &quot;Laten we naar de homepage kijken en zien hoeveel paginameningen het ontving.&quot;

  ![ gecentreerd Dimension ](assets/dimension-centered.png){style="border:1px solid gray"}

* Een typisch gebeurtenis en gebruiker-gecentreerde geleide analyse benadering zou zijn, &quot;hoeveel gebruikers de homepage hebben bezocht?&quot;

  ![ Gecentreerde Gebeurtenis ](assets/event-centered.png){style="border:1px solid gray"}

+++
