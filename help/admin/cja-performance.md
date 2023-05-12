---
title: CJA-prestaties optimaliseren
description: Aanbevolen procedures voor het optimaliseren van CJA-prestaties
solution: Customer Journey Analytics
role: Admin
hide: true
hide-from-toc: true
source-git-commit: a546c52d2a686c38f7a9a23e0c541568c2918495
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---


# CJA-prestaties optimaliseren

>[!NOTE]
>
>Voor het optimaliseren van de prestatiefactoren van de werkruimte raadpleegt u [Optimaliseren [!UICONTROL Analysis Workspace] prestaties](/help/analysis-workspace/workspace-faq/optimizing-performance.md).

Deze factoren beïnvloeden de algehele CJA prestatie:

| Factor | Definitie | Beïnvloed door | Optimalisatie |
| --- | --- | --- | --- |
| Filtercomplexiteit | Ingewikkelde filters kunnen een aanzienlijke invloed hebben op de projectprestaties. | Factoren die een filter complexer maken (in aflopende volgorde van impact) zijn: <ul><li>Operatoren van &quot;contains,&quot;, &quot;contains any of&quot;, &quot;match,&quot; &quot;start with&quot; of &quot;ends with&quot; </li><li>Opeenvolgend filteren, vooral wanneer dimensiebeperkingen (Binnen/Na) worden gebruikt </li><li>Het aantal unieke dimensie-items binnen de afmetingen die in het filter worden gebruikt (pagina = &#39;A&#39; als pagina 10 unieke items bevat, is sneller dan Pagina = &#39;A&#39; als pagina 100000 unieke items bevat) </li><li>Aantal verschillende gebruikte afmetingen (bijvoorbeeld Pagina = &#39;Home&#39; en Pagina = &#39;Zoekresultaten&#39; zijn sneller dan eVar 1 = &#39;red&#39; en eVar 2 = &#39;blue&#39;)</li><li>Veel OR-operatoren (in plaats van AND)</li><li>Geneste containers met een verschillend bereik (bv. &quot;Actief&quot; in &quot;Bezoek&quot; in &quot;Bezoeker&quot;)</li></ul> | Sommige complexiteitsfactoren kunnen niet worden voorkomen, maar zoeken naar mogelijkheden om de complexiteit van uw filters te verminderen. Over het algemeen geldt dat hoe specifieker u kunt zijn met uw filtercriteria, des te beter. Bijvoorbeeld:<ul><li>Bij containers is het gebruik van één container boven aan het filter sneller dan een reeks geneste containers.</li><li>Met operatoren is &#39;equals&#39; sneller dan &#39;contains&#39; en is &#39;equals any of&#39; sneller dan &#39;contains any of&#39;.</li><li>Met vele criteria, EN zullen de exploitanten sneller zijn dan een reeks van OF exploitanten.</li></ul> Zoek naar kansen om vele OF verklaringen in één enkele &quot;evenaart om het even welk van&quot;verklaring te verminderen.<br> |
| Complexiteit van visualisatie (filters, meetgegevens, filters) | Het type visualisatie (bijvoorbeeld fallout versus een vrije-vormlijst) dat op zich aan een project wordt toegevoegd beïnvloedt niet zeer veel projectprestaties. Het is de complexiteit van de visualisatie die de verwerkingstijd vergroot. | Factoren die complexiteit toevoegen aan een visualisatie zijn:<ul><li>Bereik van gevraagde gegevens</li><li>Aantal toegepaste filters; filters die bijvoorbeeld worden gebruikt als rijen van een vrije-vormtabel</li><li>Gebruik van complexe filters</li><li>[Statisch item](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) rijen of kolommen in vrije-vormtabellen</li><li>Filters die worden toegepast op rijen in vrije-vormtabellen</li><li>Aantal inbegrepen metriek, vooral berekende metriek die filters gebruiken</li></ul> | Als u merkt dat uw projecten niet zo snel laden als u zou willen, probeer vervangend sommige filters met eVars en filters, waar mogelijk.<br><br>Als u voortdurend filters en berekende metriek voor gegevenspunten gebruikt die voor uw zaken belangrijk zijn, denk na verbeterend uw implementatie om deze gegevenspunten directer te vangen. Als u tagbeheer gebruikt zoals Adobe Experience Platform Launch en verwerkingsregels voor Adobe, kunt u snel en gemakkelijk implementatiewijzigingen doorvoeren. |
| Capaciteit datacenter | De hoeveelheid rapporteringscapaciteit u en andere klanten binnen een Adobe gegevenscentrum delen. | Dit wordt beïnvloed door het aantal gezamenlijke vragen die door uw organisatie en andere organisaties binnen uw gegevenscentrum worden gemaakt. | Uw organisatie heeft recht op een ingestelde capaciteit en als het systeem onder een lichte belasting staat, zal Adobe meer capaciteit naar u verschuiven, boven en boven uw recht op vergoeding. |



