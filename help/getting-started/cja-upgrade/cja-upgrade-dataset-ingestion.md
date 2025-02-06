---
title: Gegevenssetopname controleren bij upgrade naar Customer Journey Analytics
description: Leer hoe te om gegevenssetopname te controleren wanneer het bevorderen aan Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 35fcd213-d831-4da0-b946-f6f0d8561f60
source-git-commit: 3b1012a302200192fd31fd6a9ed94f96323eb595
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Gegevenssetopname controleren bij upgrade naar Customer Journey Analytics {#monitor-ingestion}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-dataset-validate"
>title="Gegevens in de gegevensset valideren"
>abstract="Nu u uw implementatie van SDK van het Web hebt gevormd, kunt u de de activiteitenmanager van de Dataset gebruiken om ingebedde en ontbroken partijen te zien. Als u voornamelijk ingeslikte batches ziet, is deze stap voltooid. Als u hoofdzakelijk ontbroken partijen of geen partijen ziet, controleer uw implementatie van SDK van het Web om ervoor te zorgen dat het correct gegevens naar Adobe verzendt.<br><br> als alles correct en foutloos werd gedaan, kan deze stap in minder dan een dag worden gedaan. Als er meerdere problemen met gegevensverzameling zijn, kan het oplossen van problemen aanzienlijk langer duren."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

Nadat u uw implementatie van SDK van het Web vormt, moet u de status van individuele partijen controleren om te verifiëren dat het gegeven in de dataset wordt opgenomen.

1. Selecteer **[!UICONTROL Monitoring]** in de gebruikersinterface van het Experience Platform in de linkernavigatie.

   Het dashboard Bewaking wordt weergegeven. Met dit dashboard kunt u de status van binnenkomende gegevens van batch- of streaming invoer bekijken.

   <!-- insert screenshot -->

1. Selecteer **[!UICONTROL Batch end-to-end]** om een lijst met batches weer te geven.

   Als geen partijen worden getoond, controleer uw implementatie van SDK van het Web om ervoor te zorgen dat het correct gegevens naar Adobe verzendt.

   <!-- insert screenshot -->

1. Selecteer de batch-id voor een bepaalde gegevensset en controleer vervolgens of **[!UICONTROL Success]** wordt weergegeven in het veld **[!UICONTROL Status]** .

   Als **[!UICONTROL Failed]** wordt weergegeven in het veld **[!UICONTROL Status]** , controleert u of de Web SDK-implementatie correct gegevens naar de Adobe verzendt.

   Herhaal deze stap om de status van elke batch te controleren.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.

