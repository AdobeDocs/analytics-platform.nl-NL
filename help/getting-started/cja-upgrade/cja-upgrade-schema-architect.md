---
title: Uw schema archiveren voor gebruik met Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: f932110a-ca9d-40d1-9459-064ef9cd23da
source-git-commit: 59089146b8e56db3b0b4084615f99dc65899b74f
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Uw schema archiveren voor gebruik met Customer Journey Analytics

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

Adobe raadt u aan een XDM-schema (Experience Data Model) te maken bij de upgrade naar Customer Journey Analytics. Een XDM-schema maakt een gestroomlijnd schema mogelijk dat is afgestemd op de behoeften van uw organisatie en de specifieke platformtoepassingen die u gebruikt. Wanneer veranderingen in het schema worden vereist, moet u niet door duizenden ongebruikte gebieden bewegen om het gebied te vinden dat het bijwerken vereist.

Bekijk de volgende secties terwijl u uw XDM-schema gaat ontwerpen.

## Vermijd Adobe Analytics-beperkingen in uw XDM-schema

De onderliggende architectuur van Customer Journey Analytics biedt veel meer flexibiliteit dan Adobe Analytics. Het maken van een nieuw XDM-schema is een belangrijke manier om die flexibiliteit te ontgrendelen. Wanneer u een upgrade uitvoert naar Customer Journey Analytics, moet u voorkomen dat u overbodige Adobe Analytics-beperkingen in uw schema doorvoert.

| Adobe Analytics-gegevensarchitectuur | XDM-schemaarchitectuur |
|---------|----------|
| De individuele metriek worden toegevoegd aan de de gegevensarchitectuur van Analytics.<br/> Bijvoorbeeld, in Adobe Analytics, hebt u een verschillende eVar voor elke gebeurtenis. | Maak afzonderlijke metriek in de gegevensweergave in plaats van in het XDM-schema. Dit biedt meer flexibiliteit als u later wijzigingen wilt aanbrengen.<br/> bijvoorbeeld, in Customer Journey Analytics, hebt u één enkele gebeurtenis in het schema, en het gebruik leidt gebeurtenissen in de gegevensmening. |
| Props en eVars zijn vereist om aangepaste variabelen te maken. | B2 |
| A3 | B3 |

## Identificeer uw gegevensteam en andere belanghebbenden door uw organisatie


## Overweeg andere Adobe Experience Platform-toepassingen die in uw organisatie worden gebruikt



1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
