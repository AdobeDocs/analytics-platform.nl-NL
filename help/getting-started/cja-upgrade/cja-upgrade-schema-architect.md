---
title: Uw schema archiveren voor gebruik met Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: f932110a-ca9d-40d1-9459-064ef9cd23da
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Uw schema archiveren voor gebruik met Customer Journey Analytics {#upgrade-schema-architect}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-schema-architect"
>title="Een schema archiveren"
>abstract="Bespreek binnen uw organisatie de vereisten van gegevensinzameling, en bepaal hoe u een schema voor gebruik in Adobe Experience Platform wilt bouwen. Deze stap verschijnt omdat u het geadviseerde proces wilt gebruiken om een schema te gebruiken dat aan uw organisatie wordt aangepast. Het correct uitvoeren van deze stap is essentieel, aangezien een schema dat alle teams binnen uw organisatie zich richt op maakt gegevensopname beduidend gemakkelijker.<br><br> de geschatte tijd om alle relevante partijen in uw organisatie samen te brengen zich op een verenigd schema te richten is 1-2 maanden. Dit tijdkader hangt sterk af van het aantal teams die worden vereist om te coördineren, en het aantal dimensies + metriek om zich op te richten."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

Adobe raadt u aan een XDM-schema (Custom Experience Data Model) te maken dat u kunt gebruiken met de Web SDK wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics. U kunt ook het standaard Adobe Analytics-schema gebruiken, dat gebruikmaakt van de Adobe Analytics ExperienceEvent-veldgroep.

Een aangepast XDM-schema maakt een gestroomlijnd schema mogelijk dat is afgestemd op de behoeften van uw organisatie en de specifieke platformtoepassingen die u gebruikt. In tegenstelling tot het standaard Adobe Analytics-schema dat gebruikmaakt van de Adobe Analytics ExperienceEvent-veldgroep, hoeft u, wanneer wijzigingen in een aangepast XDM-schema vereist zijn, niet door duizenden ongebruikte velden te bladeren om het veld te zoeken dat moet worden bijgewerkt.

Voor meer informatie over deze schemaopties, zie [ uw schema voor Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-existing.md) kiezen.

Bekijk de volgende secties terwijl u uw XDM-schema gaat ontwerpen.

## Vermijd Adobe Analytics-beperkingen in uw XDM-schema

De onderliggende architectuur van Customer Journey Analytics biedt veel meer flexibiliteit dan Adobe Analytics. Het maken van een nieuw XDM-schema is een belangrijke manier om die flexibiliteit te ontgrendelen. Wanneer u een upgrade uitvoert naar Customer Journey Analytics, moet u voorkomen dat u overbodige Adobe Analytics-beperkingen in uw schema doorvoert.

>[!NOTE]
>
>De volgende informatie is nog niet volledig. Het zal in de nabije toekomst volledig zijn.

| Adobe Analytics-gegevensarchitectuur | XDM-schemaarchitectuur |
|---------|----------|
| De individuele metriek worden toegevoegd aan de de gegevensarchitectuur van Analytics.<br/> Bijvoorbeeld, in Adobe Analytics, hebt u verschillende eVar voor elke gebeurtenis. | Maak afzonderlijke metriek in de gegevensweergave in plaats van in het XDM-schema. Dit biedt meer flexibiliteit als u later wijzigingen wilt aanbrengen.<br/> Bijvoorbeeld, in Customer Journey Analytics, hebt u één enkele gebeurtenis in het schema, en het gebruik creeert gebeurtenissen in de gegevensmening. |
| Props en eVars zijn vereist om aangepaste variabelen te maken. |  |

## Identificeer uw gegevensteam en andere belanghebbenden door uw organisatie

>[!NOTE]
>
>Deze informatie is nog niet beschikbaar. Het zal in de nabije toekomst beschikbaar zijn.

## Overweeg andere Adobe Experience Platform-toepassingen die in uw organisatie worden gebruikt

>[!NOTE]
>
>Deze informatie is nog niet beschikbaar. Het zal in de nabije toekomst beschikbaar zijn.
