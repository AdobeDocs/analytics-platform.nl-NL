---
title: Begrijp uw implementatie van Adobe Analytics en hoe het uw verbetering aan Customer Journey Analytics beïnvloedt
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: b9cff809-6df7-4d75-9bc1-0cc12074d355
source-git-commit: 5ce69400a01566728f374d68ac08a981adfd8b6e
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 1%

---

# Begrijp uw implementatie van Adobe Analytics en hoe het uw verbetering aan Customer Journey Analytics beïnvloedt

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in de [ controlelijst van de Customer Journey Analytics verbetering ](https://gigazelle.github.io/cja-ttv/).

Adobe Analytics kan op verschillende manieren worden geïmplementeerd. Bij de upgrade naar de Customer Journey Analytics zijn niet alle upgradepaden beschikbaar voor alle Adobe Analytics-implementaties. Het aanbevolen upgradepad is echter altijd beschikbaar, ongeacht de manier waarop Adobe Analytics in uw organisatie is geïmplementeerd.

Gebruik de onderstaande informatie voor meer informatie over uw huidige Adobe Analytics-implementatie en over de upgradepaden die beschikbaar zijn voor uw organisatie.

Neem contact op met uw Adobe als u meer specifiek advies, advies of ondersteuning nodig hebt.

| Bestaande Adobe Analytics-implementatie | Beschrijving | Beschikbare upgradepaden |
|---------|----------|----------|
| AppMeasurement | AppMeasurement voor JavaScript is historisch gezien een gemeenschappelijke methode geweest voor de implementatie van Adobe Analytics.<p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics met AppMeasurement voor JavaScript uitvoeren ](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview)</p> | <ul><li>(Aanbevolen) Nieuwe implementatie van de Web SDK van het Experience Platform met de Verbinding van de Analytics Source</li><li>Nieuwe implementatie van het Web SDK van het Experience Platform</li><li>Adobe Analytics migreren naar de web SDK</li><li>Analytics Source Connector</li></ul> |
| Adobe Analytics-extensie (tags) | <p>Tags in Adobe Experience Platform zijn een oplossing voor tagbeheer waarmee u naast andere coderingsvereisten ook analytische code kunt implementeren. Adobe biedt integratie met andere oplossingen en producten aan, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.</p><p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend de uitbreiding van Analytics ](https://experienceleague.adobe.com/en/docs/analytics/implementation/launch/overview)</p> | <ul><li>(Aanbevolen) Nieuwe implementatie van de Web SDK van het Experience Platform met de Verbinding van de Analytics Source</li><li>Nieuwe implementatie van het Web SDK van het Experience Platform</li><li>Adobe Analytics migreren naar de web SDK</li><li>Analytics Source Connector</li></ul> |
| Experience Platform Web SDK (alloy.js) | De Experience Platform Web SDK is de huidige geadviseerde methode van de Adobe om Adobe Analytics uit te voeren. Met de Adobe Experience Platform-Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. <p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics met de Edge Network van Adobe Experience Platform uitvoeren ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/overview)</p> | <ul><li>(Aanbevolen) Nieuwe implementatie van de Web SDK van het Experience Platform met de Verbinding van de Analytics Source</li><li>De Adobe Analytics Web SDK-implementatie configureren om gegevens naar het platform te verzenden</li></ul> |
| Experience Platform Web SDK-extensie (tags) | De SDK van het Web van de Experience Platform is de huidige geadviseerde methode van de Adobe om Adobe Analytics voor Webgegevens uit te voeren. Met de Adobe Experience Platform-Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. <p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend het Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/web-sdk/overview)</p> | <ul><li>(Aanbevolen) Nieuwe implementatie van de Web SDK van het Experience Platform met de Verbinding van de Analytics Source</li><li>De Adobe Analytics Web SDK-implementatie configureren om gegevens naar het platform te verzenden</li></ul> |
| Experience Platform Mobile SDK | De Experience Platform Mobile SDK is de momenteel aanbevolen methode van de Adobe voor het implementeren van Adobe Analytics for mobile-gegevens. Met de Adobe Experience Platform-Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden.<p>De Adobe Experience Platform Mobile SDK helpt de oplossingen en services van de Adobe voor Experiencen Cloud in uw mobiele apps te ondersteunen. </p><p>Voor meer informatie over dit implementatietype, zie [ Adobe Analytics uitvoeren gebruikend Adobe Experience Platform Mobile SDK ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/mobile-sdk/overview)</p> | <ul><li>(Aanbevolen) Nieuwe implementatie van de Web SDK van het Experience Platform met de Verbinding van de Analytics Source</li><li>De Adobe Analytics Web SDK-implementatie configureren om gegevens naar het platform te verzenden</li></ul> |

{style="table-layout:auto"}
