---
title: Gebruik de bronaansluiting Analytics uitsluitend voor een upgrade naar Customer Journey Analytics
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

# Gebruik de bronaansluiting Analytics uitsluitend voor een upgrade naar Customer Journey Analytics {#use-source-connector-exclusively}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector-exclusively"
>title="Gebruik de bronaansluiting voor Analytics"
>abstract="(Niet aanbevolen) U kunt niet integreren met andere Adobe Experience Platform-services of Adobe Analytics uitschakelen via de bronconnector van Analytics. Het binden van gegevens uit andere bronnen vereist waarschijnlijk stitching. Aan al deze vereisten in de vragenlijst voldoen om deze optie te selecteren."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in [ Customer Journey Analytics verbeteringschecklist ](https://gigazelle.github.io/cja-ttv/).

Hoewel dit niet wordt aanbevolen, kunt u de bronconnector Analytics gebruiken als het enige implementatiepad voor Customer Journey Analytics. Vanwege de inherente nadelen die aan dit type upgrade zijn gekoppeld, raadt Adobe u echter aan de bronconnector voor Analytics te gebruiken in combinatie met een nieuwe implementatie van Experience Platform Web SDK. Voor meer informatie over dit geadviseerde verbeteringsweg, zie [ Geadviseerde weg wanneer bevordering van Adobe Analytics aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).

Gebruik de informatie in de lijst hieronder om de voordelen en de nadelen te begrijpen van het gebruiken van de bronschakelaar exclusief.

Als u besluit om de Analytics bronschakelaar als enige implementatieweg voor Customer Journey Analytics te gebruiken, volg de implementatiestappen die in [ worden beschreven Ingest en gebruik gegevens gebruikend bronschakelaars ](/help/data-ingestion/sources.md).

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>Minder tijdrovend en veeleisend upgradepad. <p>Gegevens worden snel en eenvoudig naar Customer Journey Analytics gemigreerd.</p></li></ul> | <ul><li>**Gegevens worden niet verzonden naar Edge Network**: <p>Dit leidt tot de volgende nadelen:</p><ul><li>Het hoogste niveau van [ latentie ](/help/technotes/guardrails.md#latencies) in het melden van over alle verbeteringswegen; niet geoptimaliseerd voor verpersoonlijkingsgebruiksgevallen in real time.</li><li>Gegevens kunnen niet worden gedeeld met andere Adobe Experience Platform-toepassingen; ze zijn alleen beperkt tot Customer Journey Analytics</li><li>Reliant op de Adobe Analytics-nomenclatuur (prop, eVar, event, enzovoort)</li></ul><li>**Moeilijk om naar het Web SDK in de toekomst te bewegen**: Uiteindelijk, zult u waarschijnlijk toegang tot de voordelen willen die door het Web SDK van Experience Platform worden verstrekt. Als u de Experience Platform Web SDK wilt gaan gebruiken, moet u een nieuwe implementatie uitvoeren.</li><li>**gebruikt de het gebiedsgroep van de Gebeurtenis van de Ervaring van Analytics in uw schema**: Deze gebiedsgroep voegt vele gebeurtenissen van Adobe Analytics toe die niet nodig in uw schema van Customer Journey Analytics zijn.  Dit kan leiden tot een overzichtelijker, complex schema dan wat anders nodig is voor Customer Journey Analytics.</li><li>**vereist vergunningen voor zowel Adobe Analytics als Customer Journey Analytics**: Het gebruiken van de Analytics bronschakelaar vereist dat u voor zowel Adobe Analytics als Customer Journey Analytics betaalt.</li></ul> |

{style="table-layout:auto"}
