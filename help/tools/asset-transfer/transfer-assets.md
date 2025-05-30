---
title: Overdrachtsmiddelen
description: Leer hoe u componenten van de ene gebruiker naar de andere kunt overbrengen
role: Admin
solution: Customer Journey Analytics
exl-id: c5ed81ea-1d55-4193-9bb1-a2a93ebde91f
source-git-commit: 3e521cb4ef532d57b9f408fc12dcf138f130f059
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Overdrachtsmiddelen

Met het gereedschap Asset Transfer kunt u de eigendom van elementen overdragen aan andere gebruikers. Assets kan componenten omvatten zoals projecten, segmenten, datumwaaiers, berekende metriek, annotaties, alarm en geplande projecten.

Assets is vaak gebonden aan een individuele eigenaar en kan in sommige gevallen, zoals segmenten en berekende maatstaven, niet worden bewerkt of gedeeld, zelfs niet door beheerders. Wanneer gebruikers de organisatie verlaten of hun rolveranderingen, kan het noodzakelijk worden om eigendom van deze activa aan andere gebruikers over te brengen om continuïteit en aangewezen toegang te verzekeren.

## Machtigingen

Voor Asset Transfer is de toestemming van de productbeheerder voor Customer Journey Analytics vereist.

## Overdrachtsmiddelen

1. Navigeer in CJA naar **[!UICONTROL Tools]** > **[!UICONTROL Asset Transfer]** .

   ![ het menupunt van de overdracht van activa ](/help/tools/asset-transfer/assets/asset-transfer.png)

1. Zoek in het dialoogvenster **[!UICONTROL Users]** naar de gebruiker waarvan u elementen wilt overbrengen en selecteer de gebruiker.

   >[!IMPORTANT]
   >
   >U kunt slechts een 1:1 overdracht, van één gebruiker aan een andere gebruiker doen. Een-op-veel of een-op-een overdracht wordt niet ondersteund.


1. Nadat u een gebruiker hebt geselecteerd, wordt de optie Overdrachtselementen onder aan het scherm weergegeven.

   ![ optie van het de activa van de Overdracht ](/help/tools/asset-transfer/assets/after-selection.png)

1. Klik op **[!UICONTROL Transfer assets]**.

1. Selecteer in het scherm **[!UICONTROL Transfer assets]** eerst de ontvanger waarnaar u elementen wilt overbrengen.

1. Doorloop nu elke componentmap in de linkernavigatie om afzonderlijke componenten of alle elementen in een map te selecteren die u wilt overbrengen.

   >[!NOTE]
   >
   >Als u elementen van een beheerder naar een andere beheerder overbrengt, wordt de ontvanger niet bijgewerkt naar een beheerder.


   >[!NOTE]
   >
   >    Wanneer het overbrengen van activa die andere componenten van verwijzingen voorzien (bijvoorbeeld, projecten die andere segmenten en berekende metriek van verwijzingen voorzien), zullen de componenten niet die door de huidige eigenaar van het project worden bezeten slechts met de ontvanger worden gedeeld. De eigendom van alle andere componenten wordt overgedragen aan de ontvanger.

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

### Mogelijke redenen voor mislukte overdracht van middelen

- De afhankelijke diensten die mislukkingen veroorzaken: De overdrachtinteractie van activa met een verschillende dienst voor elk componententype (b.v. netwerkkwesties, stroomafwaartse de dienstproblemen), zodat kan dit een gedeeltelijke of volledige mislukking, of intermitterende mislukkingen veroorzaken.

- Ontbrekende component of overgedragen door een andere beheerder: een component is verwijderd door een andere gebruiker of overgedragen door een andere beheerder aan iemand anders, terwijl een elementoverdrachttaak nog bezig was.

- De POST-inhoud van de API wordt niet correct gevuld: een component wordt mogelijk niet verzonden in de POST-inhoud van de API wanneer meerdere componenttypen zijn geselecteerd.

- Gebruiker bestaat niet: de gebruiker is halverwege de overdracht verwijderd of is om een andere reden ongeldig. Als de gebruiker ongeldig is voordat de overdracht wordt gestart, wordt deze taak afgevangen en wordt de taak niet verwerkt. Als de gebruiker halverwege de overdracht werd geschrapt, kon dit gedeeltelijke mislukkingen veroorzaken.

- Verbinding/netwerkfout: verbinding gaat verloren bij overdracht halverwege. Om het even welke partijen overdrachtbanen die reeds werden overgebracht naar het achterste proces nog aan voltooiing, maar de gebruiker zal niet het bericht van het overdrachtresultaat met een samenvatting zien van wat slaagde en wat ontbrak.

- Tabblad met gesloten mid-transfer in browser: bij zeer grote overdrachten, als het browsertabblad wordt gesloten of als de pagina weg van de mid-transfer wordt genavigeerd, worden alleen de netwerkaanvragen die zijn gedaan voordat het tabblad close/page navigatie plaatsvindt, op de juiste wijze elementen overgedragen. Als de gebruiker terugnavigeert naar de pagina, ontvangen zij niet het bericht van de reactiestatus erop wijst die welke activa overmaakten, en welke niet.

## Assets overbrengen tijdens upgrade van Adobe Analytics naar Customer Journey Analytics

Een van de belangrijkste gevallen van overdracht van activa is tijdens de upgrade van Adobe Analytics naar Customer Journey Analytics.

De [ eigenschap van de Migratie van de Component ](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/component-migration/component-migration) in Adobe Analytics laat u beheer-Vertrouwde projecten aan andere beheerders migreren. Alle componenten waaruit deze projecten bestaan, worden vervolgens opnieuw gemaakt in Customer Journey Analytics en de beheerder van de ontvanger heeft al die componenten, ongeacht wie ze heeft gemaakt.

Dit hulpmiddel van de Overdracht van Activa laat later beheerders componenten aan hun rechtmatige eigenaars opnieuw toewijzen, of zij of niet worden beheerd.

>[!IMPORTANT]
>
>Terwijl u componenten kunt overbrengen gebruikend dit hulpmiddel, moet u als admin nog ervoor zorgen dat de ontvanger toegang tot de gegevensmeningen heeft die worden vereist om deze componenten te bekijken/te gebruiken. U kunt toestemmingen in [ Admin Console ](https://helpx.adobe.com/nl/enterprise/using/admin-console.html) bekijken en toewijzen.

## Exporteren naar CSV

Met de optie **[!UICONTROL Export to CSV]** kunnen beheerders alleen een lijst met gebruikers downloaden die wordt weergegeven in een CSV-bestand. Ze kunnen geen lijst met overgedragen elementen exporteren naar een CSV-bestand.

## Inactieve gebruikers

Alle eerder verwijderde gebruikers worden samen met hun wezen onder één item voor &quot;Inactieve gebruikers&quot; weergegeven. Deze componenten kunnen naar een nieuwe ontvanger worden overgebracht. Deze functie is beschikbaar in januari.

![ Inactieve gebruikers die in de activa UI van de Overdracht verschijnen ](assets/inactive-users.png)

