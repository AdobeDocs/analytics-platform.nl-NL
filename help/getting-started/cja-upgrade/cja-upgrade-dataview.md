---
title: Een gegevensweergave maken in Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 832f3f9a-1836-43ac-8185-f22ae0ded3aa
source-git-commit: eb9b749a5c61da3b4b5d2eeeed93bf5e4702a415
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Een gegevensweergave maken in Customer Journey Analytics {#upgrade-create-dataview}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-dataview"
>title="Een gegevensweergave maken in Customer Journey Analytics"
>abstract="Een gegevensweergave is een container specifiek voor Customer Journey Analytics waarmee u kunt bepalen hoe gegevens van een verbinding moeten worden geïnterpreteerd.<br><br> terwijl de aanvankelijke verwezenlijking van de gegevensmening een paar notulen neemt, kan het vormen van elke afmeting en metrisch met de gewenste componentenmontages verscheidene dagen vergen. Als u deze instellingen wijzigt, worden deze met terugwerkende kracht toegepast, zodat uw organisatie ze in de loop der tijd kan verfijnen."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-views/create-dataview.md -->

Het creëren van een gegevensmening impliceert of het creëren van metriek en dimensies van schemaelementen of het gebruiken van standaardcomponenten. De meeste schemaelementen kunnen of een afmeting of metrisch, afhankelijk van de vereisten van uw zaken zijn. Nadat u een schema-element naar een gegevensweergave hebt gesleept, worden aan de rechterkant opties weergegeven waarmee u de werking van de dimensie of de metrische instelling in Customer Journey Analytics kunt aanpassen.

Een gegevensweergave maken:

1. Login aan [&#x200B; Customer Journey Analytics &#x200B;](https://analytics.adobe.com) en selecteert **[!UICONTROL Data views]**, naar keuze van **[!UICONTROL Data management]**, in het hoogste menu.

1. Selecteer **[!UICONTROL Create new data view]** . U kunt ook een bestaande gegevensweergave selecteren in de lijst met gegevensweergaven om deze te bewerken.

1. Op [!UICONTROL **vorm**] lusje, specificeer een naam voor de gegevensmening en vorm zijn basismontages, componenten, en kalenderopties.

   Voor gedetailleerde informatie over elk gebied, zie [&#128279;](/help/data-views/create-dataview.md#configure) vormen in [&#x200B; creeer of geef een gegevensmening &#x200B;](/help/data-views/create-dataview.md) uit.

   ![&#x200B; vorm gegevensmening &#x200B;](assets/dataview-configure.png)

1. Selecteer de [!UICONTROL **Componenten**] tabel.

   Het [!UICONTROL **lusje van Componenten**] is waar u de componenten van een gegevensmening plaatst, wat betekent u metriek en dimensies van schemaelementen kunt tot stand brengen. U kunt ook standaardcomponenten gebruiken.

   ![&#x200B; Componenten tabel &#x200B;](assets/dataview-components.png)

1. Van het [!UICONTROL **lusje van Componenten**], sleep schemaelementen van het linkerspoor in de [!UICONTROL **sectie van Metriek**] of de [!UICONTROL **sectie van Dimensies**]. De schema-elementen die u toevoegt, worden metriek of afmetingen in de gegevensweergave.

   Voor gedetailleerde informatie over de beschikbare opties wanneer het toevoegen van componenten aan een gegevensmening, zie [&#x200B; Componenten &#x200B;](/help/data-views/create-dataview.md#components) in [&#x200B; creeer of geef een gegevensmening &#x200B;](/help/data-views/create-dataview.md) uit.

1. Selecteer het [!UICONTROL **lusje van Montages**]. Van hier, kunt u segmenten vormen om op uw volledige gegevensmening van toepassing te zijn en zittingsonderbreking en metriek te vormen.

   Voor gedetailleerde informatie over de opties beschikbaar wanneer het vormen van montages voor een gegevensmening, zie [&#x200B; Montages &#x200B;](/help/data-views/create-dataview.md#settings) in [&#x200B; creeer of geef een gegevensmening &#x200B;](/help/data-views/create-dataview.md) uit.

1. Selecteer **[!UICONTROL Save]** om de configuratie voor uw gegevensweergave op te slaan.

1. Selecteer **[!UICONTROL Save and finish]** nadat alle gewenste instellingen zijn opgegeven.

{{upgrade-final-step}}
