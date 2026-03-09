---
title: Sessieinstellingen
description: Leer over de montages in een gegevensmening u kunt gebruiken om lengte van een zitting te bepalen en de trekker om een nieuwe zitting in werking te stellen
solution: Customer Journey Analytics
feature: Data Views
exl-id: 25710bf1-ec85-4a7d-a404-54549013cc2c
role: Admin
source-git-commit: 81e08ecb593b6ba789c479d0e648cbe7ba0a82d6
workflow-type: tm+mt
source-wordcount: '493'
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

1. Maak een nieuwe of bewerk een bestaande gegevensweergave. Zie [&#x200B; creeer of geef een gegevensmening &#x200B;](create-dataview.md) voor meer informatie uit.

1. Selecteer de tab **[!UICONTROL Settings]** . Onder [!UICONTROL Session settings] :

   1. Voer een waarde in voor **[!UICONTROL Session timeout]** in [!UICONTROL minute(s)] , [!UICONTROL hour(s)] , [!UICONTROL day(s)] of [!UICONTROL week(s)] . De sessietime-out bepaalt hoe lang een sessie inactief kan zijn (er treden geen gebeurtenissen op) voordat een nieuwe sessie wordt gestart.

      Gebruik een korte sessietime-out (bijvoorbeeld 30 minuten) als u vooral online interacties wilt analyseren. Zo kunt u bijvoorbeeld analyseren of profielen die uw productpagina&#39;s in de online winkel bezoeken, producten aan de winkelwagentje hebben toegevoegd of zelfs online zijn aangeschaft.

      Gebruik een lange sessietime-out (bijvoorbeeld 3 maanden) als u online en offline gegevens combineert en wilt analyseren of klanten die een of meer van uw producten hebben aangeschaft, binnen de eerste drie maanden na hun aankoop contact hebben opgenomen met uw contactcentrum.

   1. Selecteer een segment in het vervolgkeuzemenu **[!UICONTROL Add segments]** als u een gegevensweergave wilt segmenteren. Alternatief, kunt u een segment van ![&#x200B; Segmentatie &#x200B;](/help/assets/icons/Segmentation.svg) **[!UICONTROL Segments]** in de linkerruit op **[!UICONTROL _Daling hier_]** slepen en laten vallen.

      Alleen die segmenten worden vermeld die worden gedeeld, waartoe u toegang hebt en die kunnen worden geëvalueerd op basis van de componenten die u voor de gegevensweergave hebt gedefinieerd.

   1. Selecteer een metrische waarde in het keuzemenu **[!UICONTROL Start new session with a metric]** . Alternatief, kunt u metrisch van ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) slepen en laten vallen **[!UICONTROL Metrics]** in de linkerruit op **[!UICONTROL _Daling hier metrisch_]**. De geselecteerde metrische waarde bepaalt het begin van een nieuwe zitting. U kunt meerdere metrische waarden definiëren.

      U kunt om het even welk soort metrisch gebruiken om een nieuwe zitting te bepalen. Stel dat u elke keer dat een profiel uw mobiele app start, een nieuwe sessie wilt definiëren. In **[!UICONTROL Data view]** > **[!UICONTROL Components]** definieert u een component van het type metrisch, genaamd **[!UICONTROL Launch]** , op basis van een schemaveld **[!UICONTROL appInteraction]** **[!UICONTROL Name]** . U geeft verder de metrische component **[!UICONTROL Launch]** op, zodat alleen de waarde wordt geteld wanneer de waarde overeenkomt met `launch` .

      ![&#x200B; de Metrische Lanceringen van de Component van de Interactie van de Toepassing &#x200B;](assets/component-launches.png)

      Vervolgens sleept u de sjabloon en selecteert u de metrische waarde van **[!UICONTROL Launch]** als de metrische waarde om een nieuwe sessie te definiëren.

      ![&#x200B; Lanceringen van de Montages van de Zitting &#x200B;](assets/session-settings-launches-metric.png)



1. Selecteer **[!UICONTROL Save]** of **[!UICONTROL Save and finish]** om de definitie van de sessie-instellingen op te slaan.
