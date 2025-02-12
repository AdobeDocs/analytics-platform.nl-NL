---
title: Een gegevensweergave maken in Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 832f3f9a-1836-43ac-8185-f22ae0ded3aa
source-git-commit: bb87226ee4b9acc433031f41997d403d49f48db3
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Een gegevensweergave maken in Customer Journey Analytics {#upgrade-create-dataview}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-dataview"
>title="Een gegevensweergave maken in Customer Journey Analytics"
>abstract="Een gegevensweergave is een container specifiek voor Customer Journey Analytics waarmee u kunt bepalen hoe gegevens van een verbinding moeten worden geïnterpreteerd.<br><br> terwijl de aanvankelijke verwezenlijking van de gegevensmening een paar notulen neemt, kan het vormen van elke afmeting en metrisch met de gewenste componentenmontages verscheidene dagen vergen. Als u deze instellingen wijzigt, worden deze met terugwerkende kracht toegepast, zodat uw organisatie ze in de loop der tijd kan verfijnen."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-views/create-dataview.md -->

Het creëren van een gegevensmening impliceert of het creëren van metriek en dimensies van schemaelementen of het gebruiken van standaardcomponenten. De meeste schemaelementen kunnen of een afmeting of metrisch, afhankelijk van de vereisten van uw zaken zijn. Nadat u een schema-element naar een gegevensweergave hebt gesleept, worden aan de rechterkant opties weergegeven waarmee u de werking van de dimensie of de metrische instelling in Customer Journey Analytics kunt aanpassen.

Een gegevensweergave maken:

1. Login aan [ Customer Journey Analytics ](https://analytics.adobe.com) en ga naar het **[!UICONTROL Data views]** lusje.

1. Selecteer **[!UICONTROL Create new data view]** . U kunt ook een bestaande gegevensweergave selecteren in de lijst met gegevensweergaven om deze te bewerken.

1. Op [!UICONTROL **vorm**] lusje, specificeer een naam voor de gegevensmening en vorm zijn basismontages, componenten, en kalenderopties.

   Voor gedetailleerde informatie over elk gebied, zie [ ](/help/data-views/create-dataview.md#configure) vormen in [ creeer of geef een gegevensmening ](/help/data-views/create-dataview.md) uit.

   ![ vorm gegevensmening ](assets/dataview-configure.png)

1. Selecteer de [!UICONTROL **Componenten**] tabel.

   Het [!UICONTROL **lusje van Componenten**] is waar u de componenten van een gegevensmening plaatst, wat betekent u metriek en dimensies van schemaelementen kunt tot stand brengen. U kunt ook standaardcomponenten gebruiken.

   ![ Componenten tabel ](assets/dataview-components.png)

1. Van het [!UICONTROL **lusje van Componenten**], sleep schemaelementen van het linkerspoor in de [!UICONTROL **sectie van Metriek**] of de [!UICONTROL **sectie van Dimensies**]. De schema-elementen die u toevoegt, worden metriek of afmetingen in de gegevensweergave.

   Voor gedetailleerde informatie over de beschikbare opties wanneer het toevoegen van componenten aan een gegevensmening, zie [ Componenten ](/help/data-views/create-dataview.md#components) in [ creeer of geef een gegevensmening ](/help/data-views/create-dataview.md) uit.

1. Selecteer het [!UICONTROL **lusje van Montages**]. Van hier, kunt u filters vormen om op uw volledige gegevensmening van toepassing te zijn en zittingsonderbreking en metriek te vormen.

   Voor gedetailleerde informatie over de opties beschikbaar wanneer het vormen van montages voor een gegevensmening, zie [ Montages ](/help/data-views/create-dataview.md#settings) in [ creeer of geef een gegevensmening ](/help/data-views/create-dataview.md) uit.

1. Selecteer **[!UICONTROL Save]** om de configuratie voor uw gegevensweergave op te slaan.

1. Selecteer **[!UICONTROL Save and finish]** nadat alle gewenste instellingen zijn opgegeven.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
