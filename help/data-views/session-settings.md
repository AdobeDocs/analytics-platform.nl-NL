---
title: Sessieinstellingen
description: Instellingen in een gegevensweergave die u kunt gebruiken om de duur van een sessie te definiëren en de trigger voor het starten van een nieuwe sessie
solution: Customer Journey Analytics
feature: Data Views
exl-id: 25710bf1-ec85-4a7d-a404-54549013cc2c
role: Admin
source-git-commit: 614e15a492b247d98e4e32c0f06d8ae438ca6d45
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Sessieinstellingen {#session-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_settings_datapreview"
>title="Gegevensvoorbeeld"
>abstract="Vergelijkt de gegevens van deze gegevensweergave met gegevens van de verbinding. Het voorproefpercentage is gebaseerd op het totale aantal in de verbinding van **laatste 90 dagen**.<br><br/> als de voorproef niet laadt, zou uw verbinding nog kunnen terugvullen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-enable MD034 -->


In Customer Journey Analytics, kunt u een zitting op om het even welke manier bepalen om hoe de mensen met uw digitale ervaringen in wisselwerking staan. U configureert de sessiemontages in een gegevensweergave.

Definities van instellingen van de sessie zijn niet-destructief en wijzigen de onderliggende gegevens niet. U kunt veelvoudige gegevensmeningen (elk met hun eigen specifieke definitie van zittingsmontages) als basis voor uw projecten van Workspace plaatsen.

De context van een sessie in een gegevensweergave definiëren:

1. Selecteer **[!UICONTROL Data views]** in de gebruikersinterface van de Customer Journey Analytics.

2. Maak een nieuwe of bewerk een bestaande gegevensweergave. Zie [ creeer of geef een gegevensmening ](create-dataview.md) voor meer informatie uit.

3. Selecteer de tab **[!UICONTROL Settings]** . Onder [!UICONTROL Session settings] :

   1. Voer een waarde in voor **[!UICONTROL Session timeout]** in [!UICONTROL minute(s)] , [!UICONTROL hour(s)] , [!UICONTROL day(s)] of [!UICONTROL week(s)] . De sessietime-out bepaalt hoe lang een sessie inactief kan zijn (er treden geen gebeurtenissen op) voordat een nieuwe sessie wordt gestart.

      Gebruik een korte sessietime-out (bijvoorbeeld 30 minuten) als u vooral online interacties wilt analyseren. Zo kunt u bijvoorbeeld analyseren of profielen die uw productpagina&#39;s in de online winkel bezoeken, producten aan de winkelwagentje hebben toegevoegd of zelfs online zijn aangeschaft.

      Gebruik een lange sessietime-out (bijvoorbeeld 3 maanden) als u online en offline gegevens combineert en wilt analyseren of klanten die een of meer van uw producten hebben aangeschaft, binnen de eerste drie maanden na hun aankoop contact hebben opgenomen met uw contactcentrum.


   2. Selecteer een metrische waarde in de lijst **[!UICONTROL Drop a metric here]** eronder **[!UICONTROL Start new session with a metric]** . U kunt ook een metrische waarde slepen en neerzetten vanuit het linkerdeelvenster van de **[!UICONTROL Drop a metric field]** . De geselecteerde metrische waarde bepaalt het begin van een nieuwe zitting. U kunt meerdere metrische waarden definiëren.

      U kunt om het even welk soort metrisch gebruiken om een nieuwe zitting te bepalen. Stel dat u elke keer dat een profiel uw mobiele app start, een nieuwe sessie wilt definiëren. In **[!UICONTROL Data view]** > **[!UICONTROL Components]** definieert u een component van het type metrisch, genaamd **[!UICONTROL Launches]** , op basis van een schemaveld **[!UICONTROL appInteraction]** **[!UICONTROL Name]** . U geeft verder de metrische component **[!UICONTROL Launches]** op, zodat alleen de waarde wordt geteld wanneer de waarde overeenkomt met `launch` .

      ![ de Metrische Lanceringen van de Component van de Interactie van de Toepassing ](assets/component-launches.png)

      Vervolgens sleept u de sjabloon en selecteert u de metrische waarde van **[!UICONTROL Launches]** als de metrische waarde om een nieuwe sessie te definiëren.

      ![ Lanceringen van de Montages van de Zitting ](assets/session-settings-launches-metric.png)



4. Selecteer **[!UICONTROL Save]** of **[!UICONTROL Save and finish]** om de definitie van de sessie-instellingen op te slaan.
