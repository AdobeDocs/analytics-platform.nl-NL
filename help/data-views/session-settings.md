---
title: Sessieinstellingen
description: Instellingen in een gegevensweergave die u kunt gebruiken om de duur van een sessie te definiëren en de trigger voor het starten van een nieuwe sessie
solution: Customer Journey Analytics
feature: Data Views
exl-id: 25710bf1-ec85-4a7d-a404-54549013cc2c
role: Admin
source-git-commit: 15a3d7b6f2ec4f37fd861315871e06ddefa5348a
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Sessieinstellingen {#session-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_settings_datapreview"
>title="Gegevensvoorbeeld"
>abstract="Vergelijkt de gegevens van deze gegevensweergave met gegevens van de verbinding. Het voorproefpercentage is gebaseerd op het totale aantal in de verbinding van **laatste 90 dagen**.<br><br/> als de voorproef niet laadt, zou uw verbinding nog kunnen terugvullen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-enable MD034 -->


In Customer Journey Analytics kunt u op elke manier een sessie definiëren die aansluit bij de manier waarop personen met uw digitale ervaringen werken. U configureert de sessiemontages in een gegevensweergave.

Definities van instellingen van de sessie zijn niet-destructief en wijzigen de onderliggende gegevens niet. U kunt veelvoudige gegevensmeningen (elk met hun eigen specifieke definitie van zittingsmontages) als basis voor uw projecten van Workspace plaatsen.

De context van een sessie in een gegevensweergave definiëren:

1. Selecteer **[!UICONTROL Data views]** (optioneel) in **[!UICONTROL Data management]** in de hoofdnavigatie van de gebruikersinterface van Customer Journey Analytics.

2. Maak een nieuwe of bewerk een bestaande gegevensweergave. Zie [&#x200B; creeer of geef een gegevensmening &#x200B;](create-dataview.md) voor meer informatie uit.

3. Selecteer de tab **[!UICONTROL Settings]** . Onder [!UICONTROL Session settings] :

   1. Voer een waarde in voor **[!UICONTROL Session timeout]** in [!UICONTROL minute(s)] , [!UICONTROL hour(s)] , [!UICONTROL day(s)] of [!UICONTROL week(s)] . De sessietime-out bepaalt hoe lang een sessie inactief kan zijn (er treden geen gebeurtenissen op) voordat een nieuwe sessie wordt gestart.

      Gebruik een korte sessietime-out (bijvoorbeeld 30 minuten) als u vooral online interacties wilt analyseren. Zo kunt u bijvoorbeeld analyseren of profielen die uw productpagina&#39;s in de online winkel bezoeken, producten aan de winkelwagentje hebben toegevoegd of zelfs online zijn aangeschaft.

      Gebruik een lange sessietime-out (bijvoorbeeld 3 maanden) als u online en offline gegevens combineert en wilt analyseren of klanten die een of meer van uw producten hebben aangeschaft, binnen de eerste drie maanden na hun aankoop contact hebben opgenomen met uw contactcentrum.


   2. Selecteer een metrische waarde in de lijst **[!UICONTROL Drop a metric here]** eronder **[!UICONTROL Start new session with a metric]** . U kunt ook een metrische waarde slepen en neerzetten vanuit het linkerdeelvenster van de **[!UICONTROL Drop a metric field]** . De geselecteerde metrische waarde bepaalt het begin van een nieuwe zitting. U kunt meerdere metrische waarden definiëren.

      U kunt om het even welk soort metrisch gebruiken om een nieuwe zitting te bepalen. Stel dat u elke keer dat een profiel uw mobiele app start, een nieuwe sessie wilt definiëren. In **[!UICONTROL Data view]** > **[!UICONTROL Components]** definieert u een component van het type metrisch, genaamd **[!UICONTROL Launch]** , op basis van een schemaveld **[!UICONTROL appInteraction]** **[!UICONTROL Name]** . U geeft verder de metrische component **[!UICONTROL Launch]** op, zodat alleen de waarde wordt geteld wanneer de waarde overeenkomt met `launch` .

      ![&#x200B; de Metrische Lanceringen van de Component van de Interactie van de Toepassing &#x200B;](assets/component-launches.png)

      Vervolgens sleept u de sjabloon en selecteert u de metrische waarde van **[!UICONTROL Launch]** als de metrische waarde om een nieuwe sessie te definiëren.

      ![&#x200B; Lanceringen van de Montages van de Zitting &#x200B;](assets/session-settings-launches-metric.png)



4. Selecteer **[!UICONTROL Save]** of **[!UICONTROL Save and finish]** om de definitie van de sessie-instellingen op te slaan.
