---
title: Inname van gegevenssets controleren bij upgrade naar Customer Journey Analytics
description: Leer hoe u de opname van gegevenssets kunt controleren bij de upgrade naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 35fcd213-d831-4da0-b946-f6f0d8561f60
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Inname van gegevenssets controleren bij upgrade naar Customer Journey Analytics {#monitor-ingestion}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-dataset-validate"
>title="Gegevens in de gegevensset valideren"
>abstract="Nu u uw implementatie hebt gevormd, kunt u de de activiteitenmanager van de Dataset gebruiken om opgenomen en ontbroken partijen te zien. Als u voornamelijk ingeslikte batches ziet, is deze stap voltooid. Als u vooral ontbroken partijen of geen partijen ziet, controleer uw implementatie om ervoor te zorgen dat het correct gegevens naar Adobe verzendt."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

Nadat u uw implementatie van het Web SDK of API vormt, moet u de status van individuele partijen controleren om te verifiëren dat het gegeven in de dataset wordt opgenomen.

1. Selecteer **[!UICONTROL Monitoring]** in de gebruikersinterface van Experience Platform in de linkernavigatie.

   Het dashboard Bewaking wordt weergegeven. Met dit dashboard kunt u de status van binnenkomende gegevens van batch- of streaming invoer bekijken.

   <!-- insert screenshot -->

1. Selecteer **[!UICONTROL Batch end-to-end]** om een lijst met batches weer te geven.

   Als er geen batches worden weergegeven, controleert u de implementatie om te controleren of deze gegevens correct naar Adobe verzendt.

   <!-- insert screenshot -->

1. Selecteer de batch-id voor een bepaalde gegevensset en controleer vervolgens of **[!UICONTROL Success]** wordt weergegeven in het veld **[!UICONTROL Status]** .

   Als **[!UICONTROL Failed]** wordt weergegeven in het veld **[!UICONTROL Status]** , controleert u de implementatie om te controleren of deze gegevens correct naar Adobe verzendt.

   Herhaal deze stap om de status van elke batch te controleren.

{{upgrade-final-step}}

