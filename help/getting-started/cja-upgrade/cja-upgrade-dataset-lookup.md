---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 33cfff3f675fc03c3444531e8426cb806cdf8559
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Opzoekgegevenssets maken om gegevens in Customer Journey Analytics te classificeren

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

Net als classificatiegegevens in Adobe Analytics zijn opzoekgegevenssets de methode voor het classificeren van gegevens in Customer Journey Analytics.

Wanneer het gebruiken van de Bron van Analytics schakelaar, worden sommige standaardraadplegingsdatasets automatisch toegepast in rapporttijd. Voor meer informatie, zie [ standaardraadplegingen aan uw datasets ](/help/connections/standard-lookups.md) toevoegen.

Om gegevens met een nieuwe implementatie van het Web SDK van het Experience Platform te classificeren, moet u een raadplegingsdataset voor elke dimensie tot stand brengen die gegevens bevat die u wilt classificeren.

Om raadplegingsdatasets voor gebruik in Customer Journey Analytics tot stand te brengen:

1. Maak in AEP een nieuw schema. Dit is een nieuw schema dat voor raadplegingsdatasets specifiek is. U kunt geen bestaand schema gebruiken.

1. U moet een nieuwe schemaklasse tot stand brengen die voor raadplegingen is.

1. Creeer een raadplegingsdataset van dat.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
