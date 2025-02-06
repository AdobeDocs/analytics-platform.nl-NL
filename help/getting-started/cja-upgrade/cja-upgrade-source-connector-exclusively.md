---
title: Gebruik de bronschakelaar van de Analyse uitsluitend om aan Customer Journey Analytics te bevorderen
description: Leer hoe u de bronaansluiting voor Analytics en kaartvelden maakt
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 34e5f97b-c936-4de6-acc9-5774bc908655
source-git-commit: 971600fcc7d8a5aac4ad39812ab4a7af69d45ccc
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Gebruik de bronschakelaar van de Analyse uitsluitend om aan Customer Journey Analytics te bevorderen {#use-source-connector-exclusively}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector-exclusively"
>title="Gebruik de bronaansluiting voor Analytics"
>abstract="(Niet aanbevolen) U kunt niet integreren met andere Adobe Experience Platform-services of Adobe Analytics uitschakelen via de bronconnector van Analytics. Het binden van gegevens uit andere bronnen vereist waarschijnlijk stitching. Aan al deze vereisten in de vragenlijst voldoen om deze optie te selecteren."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in de [ controlelijst van de Customer Journey Analytics verbetering ](https://gigazelle.github.io/cja-ttv/).

Hoewel het niet wordt geadviseerd, kunt u de bron van Analytics schakelaar als enige implementatiepad voor Customer Journey Analytics gebruiken. Nochtans, wegens de inherente nadelen verbonden aan dit type van verbetering, adviseert de Adobe het gebruiken van de Analytics bronschakelaar in combinatie met een nieuwe implementatie van het Web SDK van het Experience Platform. Voor meer informatie over dit geadviseerde verbeteringsweg, zie [ Geadviseerde weg wanneer bevordering van Adobe Analytics aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).

Gebruik de informatie in de lijst hieronder om de voordelen en de nadelen te begrijpen van het gebruiken van de bronschakelaar exclusief.

Als u besluit om de Analytics bronschakelaar als enige implementatieweg voor Customer Journey Analytics te gebruiken, volg de implementatiestappen die in [ worden beschreven Samenvatten en gegevens gebruiken gebruikend bronschakelaars ](/help/data-ingestion/sources.md).

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>Minder tijdrovend en veeleisend upgradepad. <p>Gegevens worden snel en eenvoudig naar de Customer Journey Analytics gemigreerd.</p></li></ul> | <ul><li>**Gegevens wordt niet verzonden naar Edge Network**: <p>Dit leidt tot de volgende nadelen:</p><ul><li>Het hoogste niveau van [ latentie ](/help/technotes/guardrails.md#latencies) in het melden van over alle verbeteringswegen; niet geoptimaliseerd voor verpersoonlijkingsgebruiksgevallen in real time.</li><li>Gegevens kunnen niet worden gedeeld met andere Adobe Experience Platform-toepassingen; ze zijn beperkt tot alleen Customers Journey Analytics</li><li>Reliant op de nomenclatuur van Adobe Analytics (prop, eVar, gebeurtenis, enzovoort)</li></ul><li>**Moeilijk om naar het Web SDK in de toekomst te bewegen**: Uiteindelijk, zult u waarschijnlijk toegang tot de voordelen willen die door het Web SDK van het Experience Platform worden verstrekt. Om te beginnen het Web SDK van het Experience Platform te gebruiken, moet u een nieuwe implementatie doen.</li><li>**gebruikt de het gebiedsgroep van de Gebeurtenis van de Ervaring van Analytics in uw schema**: Deze gebiedsgroep voegt vele gebeurtenissen van Adobe Analytics toe die niet nodig in uw schema van de Customer Journey Analytics zijn.  Dit kan leiden tot een overzichtelijker, complex schema dan wat anders voor Customer Journey Analytics nodig is.</li><li>**vereist vergunningen voor zowel Adobe Analytics als Customer Journey Analytics**: Het gebruiken van de Analyse bronschakelaar vereist dat u voor zowel Adobe Analytics als Customer Journey Analytics betaalt.</li></ul> |

{style="table-layout:auto"}
