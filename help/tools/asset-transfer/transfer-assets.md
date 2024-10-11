---
title: Overdrachtsmiddelen
description: Leer hoe u componenten van de ene gebruiker naar de andere kunt overbrengen
hide: true
hidefromtoc: true
source-git-commit: 1a0422144b795be7f129b13208e93f8d3645a8e7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---


# Overdrachtsmiddelen

Met het gereedschap Asset Transfer kunt u de eigendom van elementen overdragen aan andere gebruikers. Assets kan componenten omvatten zoals projecten, filters, datumwaaiers, berekende metriek, annotaties, alarm en geplande projecten.

Assets is vaak gebonden aan een individuele eigenaar en kan in sommige gevallen, zoals filters en berekende meetgegevens, niet worden bewerkt of gedeeld, zelfs niet door beheerders. Wanneer gebruikers de organisatie verlaten of hun rolveranderingen, kan het noodzakelijk worden om eigendom van deze activa aan andere gebruikers over te brengen om continuïteit en aangewezen toegang te verzekeren.

## Machtigingen

Voor de overdracht van bedrijfsmiddelen zijn bevoegdheden van de productbeheerder vereist voor de Customer Journey Analytics.

## Overdrachtsmiddelen

1. Navigeer in CJA naar **[!UICONTROL Tools]** > **[!UICONTROL Asset Transfer]** .

   ![ het menupunt van de overdracht van activa ](/help/tools/asset-transfer/assets/asset-transfer.png)

1. Zoek in het dialoogvenster **[!UICONTROL Users]** naar de gebruiker waarvan u elementen wilt overbrengen en selecteer de gebruiker.

   >[!IMPORTANT]
   >
   >U kunt slechts een 1:1 overdracht, van één gebruiker aan een andere gebruiker doen. Een-op-veel of een-op-een overdracht wordt niet ondersteund.


1. Nadat u een gebruiker hebt geselecteerd, wordt de optie Overdrachtselementen onder aan het scherm weergegeven.

   ![ menuoptie ](/help/tools/asset-transfer/assets/after-selection.png)

1. Klik op **[!UICONTROL Transfer assets]**.

1. Selecteer in het scherm **[!UICONTROL Transfer assets]** eerst de ontvanger waarnaar u elementen wilt overbrengen.

1. Doorloop nu elke componentmap in de linkernavigatie om afzonderlijke componenten of alle elementen in een map te selecteren die u wilt overbrengen.

   Houd er rekening mee dat bij het overdragen van middelen van een beheerder naar een andere beheerder de ontvanger niet wordt geüpgraded naar een beheerder.

1. Om _alle_ activa in een omslag te selecteren, controleer het vakje naast **[!UICONTROL Name]** bij de bovenkant van de lijst.

   ![ uitgezochte activa om over te brengen ](/help/tools/asset-transfer/assets/select-assets.png)

1. Klik op **[!UICONTROL Transfer]** rechtsboven nadat u alle selecties hebt gemaakt.

1. Klik op **[!UICONTROL Confirm]** wanneer het bevestigingsbericht wordt weergegeven.

   >[!IMPORTANT]
   >
   >Sluit het scherm niet tijdens de overdracht om abortus van het proces te voorkomen. Dit zorgt voor een vloeiende overdrachtservaring.

## Assets overbrengen tijdens upgrade van Adobe Analytics naar Customer Journey Analytics

Een van de belangrijkste gevallen van overdracht van activa is tijdens de upgrade van Adobe Analytics naar Customer Journey Analytics.

De [ eigenschap van de Migratie van de Component ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration) in Adobe Analytics laat u beheer-Vertrouwde projecten aan andere beheerders migreren. Alle componenten waaruit deze projecten bestaan, worden vervolgens opnieuw gemaakt in de Customer Journey Analytics en de ontvangende beheerder heeft al die componenten, ongeacht wie ze heeft gemaakt.

Dit hulpmiddel van de Overdracht van Activa laat later beheerders componenten aan hun rechtmatige eigenaars opnieuw toewijzen.

## Exporteren naar CSV

U kunt een lijst met elementen exporteren die van de ene gebruiker naar een andere gebruiker zijn overgebracht naar een CSV-bestand.

<!---## Unknown users

All previously deleted users appear under one unknown user entry, along with all their orphan components. These components can be transferred to a new recipient. This feature will be available in January.-->