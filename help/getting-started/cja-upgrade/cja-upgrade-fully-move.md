---
title: Evalueer hoe lang u Adobe Analytics na upgrade naar Customer Journey Analytics nodig hebt
description: Leer hoe lang u Adobe Analytics nodig hebt na de upgrade naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: f4440148d26e81938d029d4a077cd787c868f1be
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 0%

---

# Evalueer hoe lang u Adobe Analytics na upgrade naar Customer Journey Analytics nodig hebt {#evaluate-aa-needs}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-fully-move"
>title="Volledig verplaatsen naar Customer Journey Analytics"
>abstract="(Aanbevolen) Customer Journey Analytics is het belangrijkste analytische hulpmiddel voor uw organisatie. Uw organisatie kan echter nog steeds Adobe Analytics nodig hebben als deze sterk afhankelijk is van functies die exclusief zijn voor het hulpprogramma en deze workflows niet kunnen worden gewijzigd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-keep-aa"
>title="Beide analytische producten behouden"
>abstract="(Niet aanbevolen) Als u deze optie selecteert, worden in uw contract met Adobe zowel Adobe Analytics als Customer Journey Analytics opgenomen. Dit kan in de loop der tijd voor uw organisatie duurder zijn."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
>
>Deze documentatie zou als deel van [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) moeten worden gebruikt.

De meeste organisaties zullen Adobe Analytics uiteindelijk uitschakelen na de upgrade naar de Customer Journey Analytics. Dit komt door de kosten en complexiteit van het onderhoud van twee analytische omgevingen.

De Adobe raadt u echter aan uw Adobe Analytics-omgeving na de implementatie van Customer Journey Analytics gedurende een bepaalde periode in bedrijf te houden. In de volgende secties worden de redenen hiervoor beschreven, evenals de voorgestelde timing voor het uitschakelen van Adobe Analytics.

## Gebruikt Adobe Analytics tijdens en na een upgrade

Wanneer u besluit of en wanneer uw organisatie Adobe Analytics moet uitschakelen, moet u rekening houden met het volgende gebruik van Adobe Analytics tijdens en na een upgrade naar Customer Journey Analytics:

| Gebruikt Adobe Analytics tijdens en na de upgrade | Toelichting |
|---------|----------|
| Gegevensvergelijking naast elkaar uitvoeren | Adobe raadt u aan de Adobe Analytics-omgeving gedurende een bepaalde periode in bedrijf te houden nadat uw nieuwe Customer Journey Analytics-omgeving is gestart en gegevens zijn verzameld. Dit is de beste manier om de gegevens van uw Customer Journey Analytics naast elkaar te vergelijken met uw Adobe Analytics-gegevens.<p>Schakel Adobe Analytics niet uit totdat u de gegevens in uw Customer Journey Analytics-omgeving goed vindt.</p><p>**Nota:** de Adobe adviseert een nieuwe implementatie van het Web SDK voor uw milieu van de Customer Journey Analytics, samen met de Analyse bronschakelaar voor historische gegevens. [Meer informatie](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</p> |
| Historische gegevens van Adobe Analytics behouden | Adobe raadt u aan uw Adobe Analytics-omgeving gedurende een bepaalde periode met de bronaansluiting voor Analytics op zijn plaats te houden nadat uw nieuwe Customer Journey Analytics-omgeving is gestart en gegevens zijn verzameld. Dit is de beste manier om historische Adobe Analytics-gegevens in Customer Journey Analytics te brengen.<p>Nadat u genoeg historische gegevens in Customer Journey Analytics met uw nieuwe implementatie van SDK van het Web hebt verzameld, kunt u de de bronschakelaar van Analytics volledig verwijderen. Doe dit wanneer u zich alleen op de historische gegevens in u kunt baseren die met de nieuwe implementatie van het Web SDK van de Customer Journey Analytics worden verzameld.</p><p>**Nota:** de Adobe adviseert een nieuwe implementatie van het Web SDK voor uw milieu van de Customer Journey Analytics, samen met de Analyse bronschakelaar voor historische gegevens. [Meer informatie](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md)</p> |
| Gegevensfeeds of andere Adobe Analytics-functies gebruiken | Een klein aantal functies is nog niet volledig beschikbaar in de Customer Journey Analytics. Als u toegang tot deze functies nodig hebt, kan het nodig zijn om Adobe Analytics in combinatie met Customer Journey Analytics te gebruiken totdat deze functies beschikbaar zijn. <p>Functies die niet volledig beschikbaar zijn in de Customer Journey Analytics zijn onder andere gegevensfeeds en bijdrageanalyse. Voor een volledige lijst van eigenschappen die nog niet beschikbaar zijn, zie [ de eigenschapsteun van de Customer Journey Analytics ](/help/getting-started/aa-vs-cja/cja-aa.md).</p> |

## Procedure en tijdlijn voor het uitschakelen van Adobe Analytics {#disable-adobe-analytics}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-disable-appmeasurement-third-pary"
>title="Een systeem voor tagbeheer van derden uitschakelen"
>abstract="Als de Web SDK-gegevens volledig functioneel zijn, werkt u samen met uw tagbeheer om de bibliotheek met AppMeasurementen uit uw externe tagbeheersysteem te verwijderen.<br><br> Geschatte tijd om deze stap uit te voeren hangt van het gemak af om AppMeasurement van uw product van het markeringsbeheer, evenals de versiecyclus onbruikbaar te maken die uw organisatie aanwendt om markeringscode op te stellen en te beheren."

<!-- markdownlint-enable MD034 -->

Uw bestaande implementatie van Adobe Analytics is een zeer belangrijk deel van een succesvolle verbetering aan Customer Journey Analytics, zoals die in de sectie hierboven wordt beschreven, [ Gebruik van Adobe Analytics tijdens en na een verbetering ](#uses-of-adobe-analytics-during-and-after-an-upgrade).

Wanneer u Adobe Analytics niet meer nodig hebt voor de in de bovenstaande sectie beschreven doeleinden, gebruikt u de volgende informatie om Adobe Analytics te verwijderen:

1. Stop met gegevens verzamelen met Adobe Analytics.

   Nadat u tevreden bent met de vergelijkingen naast elkaar van uw gegevens van Adobe Analytics en uw gegevens van de Customer Journey Analytics, kunt u ophouden verzamelend gegevens met uw implementatie van Adobe Analytics. De nieuwe gegevens van Adobe Analytics zullen niet meer aan Customer Journey Analytics door de de bronschakelaar van de Analyse stromen.

   De gegevens die u vóór dit punt hebt verzameld in uw Adobe Analytics-omgeving, zijn echter nog steeds beschikbaar als historische gegevens in de Customer Journey Analytics via de bronconnector van Analytics.

   Dit proces verschilt afhankelijk van de methode voor gegevensverzameling die u hebt gebruikt om Adobe Analytics te implementeren:

+++ AppMeasurement

   [ maak de gegevensinzameling van het AppMeasurement ](/help/getting-started/cja-upgrade/cja-upgrade-disable-appmeasurement.md) onbruikbaar.

+++

+++ Extensie Analytics (Tags)

   Schakel de extensie Analytics in de labels uit.

+++

+++ API

   Schakel API-gegevensverzameling uit.

+++

+++ Derden

   Werk met de tagbeheerder om de bibliotheek met AppMeasurementen te verwijderen uit het tagbeheersysteem van derden.

+++

1. Verwijder Adobe Analytics als service uit de gegevensstroom.

   Met SDK van het Web volledig functioneel, werk met uw beheerder van het Platform om Adobe Analytics als dienst uit de datastream te verwijderen.

   Voordat u Adobe Analytics verwijdert als service, moet u ervoor zorgen dat de gebruikers van Analytics Customer Journey Analytics gebruiken in plaats van Adobe Analytics.

1. Verwijder volledig de bronschakelaar van de Analyse.

   Nadat u genoeg historische gegevens in Customer Journey Analytics met uw nieuwe implementatie van SDK van het Web hebt verzameld, kunt u de de bronschakelaar van Analytics volledig verwijderen.

   Doe dit wanneer u niet meer de historische gegevens van uw milieu van Adobe Analytics door de Analytics bronschakelaar nodig hebt, en u kunt zich alleen op de historische gegevens baseren u met de nieuwe implementatie van SDK van het Web verzamelde.

