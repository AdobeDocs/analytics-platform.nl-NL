---
title: Overdrachtsmiddelen
description: Leer hoe u componenten van de ene gebruiker naar de andere kunt overbrengen
role: Admin
solution: Customer Journey Analytics
source-git-commit: 9663a24c2430d3822cb83876ea048b6423405215
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---


# Overdrachtsmiddelen

Met het gereedschap Asset Transfer kunt u de eigendom van elementen overdragen aan andere gebruikers. Assets kan componenten omvatten zoals projecten, filters, datumwaaiers, berekende metriek, annotaties, alarm en geplande projecten.

Assets is vaak gebonden aan een individuele eigenaar en kan in sommige gevallen, zoals filters en berekende meetgegevens, niet worden bewerkt of gedeeld, zelfs niet door beheerders. Wanneer gebruikers de organisatie verlaten of hun rolveranderingen, kan het noodzakelijk worden om eigendom van deze activa aan andere gebruikers over te brengen om continuïteit en aangewezen toegang te verzekeren.

## Machtigingen

Voor de overdracht van bedrijfsmiddelen is de toestemming van de productbeheerder vereist voor de Customer Journey Analytics.

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

   >[!NOTE]
   >
   >Als u elementen van een beheerder naar een andere beheerder overbrengt, wordt de ontvanger niet bijgewerkt naar een beheerder.


   >[!NOTE]
   >
   >    Wanneer het overbrengen van activa die andere componenten van verwijzingen voorzien (bijvoorbeeld, projecten die andere filters en berekende metriek van verwijzingen voorzien), zullen de componenten niet die door de huidige eigenaar van het project worden bezeten slechts met de ontvanger worden gedeeld. De eigendom van alle andere componenten wordt overgedragen aan de ontvanger.

1. Om _alle_ activa in een omslag te selecteren, controleer het vakje naast **[!UICONTROL Name]** bij de bovenkant van de lijst.

   ![ uitgezochte activa om over te brengen ](/help/tools/asset-transfer/assets/select-assets.png)

1. Klik op **[!UICONTROL Transfer]** rechtsboven nadat u alle selecties hebt gemaakt.

1. Klik op **[!UICONTROL Confirm]** wanneer het bevestigingsbericht wordt weergegeven.

   >[!IMPORTANT]
   >
   >Sluit het scherm niet tijdens de overdracht om abortus van het proces te voorkomen. Dit zorgt voor een vloeiende overdrachtservaring.

## Overdrachtsresultaten

Er zijn drie mogelijke resultaten voor een overdracht:

- **succes van de Overdracht**: &quot;Assets bracht met succes over.&quot;

- **Gedeeltelijk succes**: &quot;Sommige activa werden met succes overgebracht.&quot;

- **de mislukking van de Overdracht**: &quot;Slaagde er niet in om activa over te brengen. Probeer het opnieuw.&quot;

## Assets overbrengen tijdens upgrade van Adobe Analytics naar Customer Journey Analytics

Een van de belangrijkste gevallen van overdracht van activa is tijdens de upgrade van Adobe Analytics naar Customer Journey Analytics.

De [ eigenschap van de Migratie van de Component ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration) in Adobe Analytics laat u beheer-Vertrouwde projecten aan andere beheerders migreren. Alle componenten waaruit deze projecten bestaan, worden vervolgens opnieuw gemaakt in de Customer Journey Analytics en de ontvangende beheerder heeft al die componenten, ongeacht wie ze heeft gemaakt.

Dit hulpmiddel van de Overdracht van Activa laat later beheerders componenten aan hun rechtmatige eigenaars opnieuw toewijzen, of zij of niet worden beheerd.

>[!IMPORTANT]
>
>Terwijl u componenten kunt overbrengen gebruikend dit hulpmiddel, moet u als admin nog ervoor zorgen dat de ontvanger toegang tot de gegevensmeningen heeft die worden vereist om deze componenten te bekijken/te gebruiken. U kunt toestemmingen in de [ Admin Console ](https://helpx.adobe.com/nl/enterprise/using/admin-console.html) bekijken en toewijzen.

## Exporteren naar CSV

Met de optie **[!UICONTROL Export to CSV]** kunnen beheerders alleen een lijst met gebruikers downloaden die wordt weergegeven in een CSV-bestand. Ze kunnen geen lijst met overgedragen elementen exporteren naar een CSV-bestand.

<!---## Unknown users

All previously deleted users appear under one unknown user entry, along with all their orphan components. These components can be transferred to a new recipient. This feature will be available in January.-->