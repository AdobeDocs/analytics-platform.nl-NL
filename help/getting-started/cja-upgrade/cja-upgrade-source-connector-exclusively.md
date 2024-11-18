---
title: Gebruik de bronschakelaar van de Analyse uitsluitend om aan Customer Journey Analytics te bevorderen
description: Leer hoe u de bronaansluiting voor Analytics en kaartvelden maakt
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 07570641949e17d30b7f9f5b38eb95c29c5176c0
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Gebruik de bronschakelaar van de Analyse uitsluitend om aan Customer Journey Analytics te bevorderen

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in de [ controlelijst van de Customer Journey Analytics verbetering ](https://gigazelle.github.io/cja-ttv/).

Hoewel het niet wordt geadviseerd, kunt u de bron van Analytics schakelaar als enige implementatiepad voor Customer Journey Analytics gebruiken. Nochtans, wegens de inherente nadelen verbonden aan dit type van verbetering, adviseert de Adobe het gebruiken van de de bronschakelaar van de Analyse samen met een nieuwe implementatie van het Web SDK van het Experience Platform. Voor meer informatie over dit geadviseerde verbeteringsweg, zie [ Geadviseerde weg wanneer bevordering van Adobe Analytics aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).

Gebruik de volgende informatie om de voordelen en de nadelen van het gebruiken van de bronschakelaar exclusief te begrijpen:

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>Minder tijdrovend en veeleisend upgradepad. <p>Gegevens worden snel en eenvoudig naar de Customer Journey Analytics gemigreerd.</p></li></ul> | <ul><li>**Gegevens wordt niet verzonden naar Edge Network**: <p>Dit leidt tot de volgende nadelen:</p><ul><li>Het hoogste niveau van [ latentie ](/help/technotes/guardrails.md#latencies) in het melden van over alle verbeteringswegen; niet geoptimaliseerd voor verpersoonlijkingsgebruiksgevallen in real time.</li><li>Gegevens kunnen niet worden gedeeld met andere Adobe Experience Platform-toepassingen; ze zijn beperkt tot alleen Customers Journey Analytics</li><li>Reliant op de nomenclatuur van Adobe Analytics (prop, eVar, gebeurtenis, enzovoort)</li></ul><li>**Moeilijk om naar het Web SDK in de toekomst te bewegen**: Uiteindelijk, zult u waarschijnlijk toegang tot de voordelen willen die door het Web SDK van het Experience Platform worden verstrekt. om te beginnen het Web SDK van het Experience Platform te gebruiken, moet u een nieuwe implementatie doen.</li><li>**gebruikt de het gebiedsgroep van de Gebeurtenis van de Ervaring van Analytics in uw schema**: Deze gebiedsgroep voegt vele gebeurtenissen van Adobe Analytics toe die niet nodig in uw schema van de Customer Journey Analytics zijn.  Dit kan leiden tot een overzichtelijker, complex schema dan wat anders voor Customer Journey Analytics nodig is.</li><li>**vereist vergunningen voor zowel Adobe Analytics als Customer Journey Analytics**: Het gebruiken van de Analyse bronschakelaar vereist dat u voor zowel Adobe Analytics als Customer Journey Analytics betaalt.</li></ul> |

{style="table-layout:auto"}

