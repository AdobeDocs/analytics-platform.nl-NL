---
title: Sessieinstellingen
description: Instellingen in een gegevensweergave die u kunt gebruiken om de duur van een sessie te definiëren en de trigger voor het starten van een nieuwe sessie
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: 25ff6feda28f0447927a52f44aed800cdd89e0cb
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---


# Sessieinstellingen

De montages van de zitting in de meningen van Gegevens veranderen hoe de Customer Journey Analytics zittingen van de gegevens in uw verbinding berekent.

Binnen de **[!UICONTROL Settings]** tabblad Gegevens kunt u op elke manier een sessie definiëren die aansluit bij de manier waarop personen met uw digitale ervaringen werken. Definities van instellingen van de sessie zijn niet-destructief en wijzigen de onderliggende gegevens niet. U kunt veelvoudige gegevensmeningen (elk met hun eigen specifieke definitie van zittingsmontages) als stichting voor uw projecten van de Werkruimte plaatsen.

De context van een sessie voor een gegevensweergave definiëren:

1. Selecteren **[!UICONTROL Data views]** in de Customer Journey Analytics-UI.

2. Maak een nieuwe of bewerk een bestaande gegevensweergave. Zie [Een gegevensweergave maken of bewerken](create-dataview.md) voor meer informatie .

3. Selecteer de **[!UICONTROL Settings]** tab. Onderliggend [!UICONTROL Session settings]:

   1. Voer een waarde in voor **[!UICONTROL Session timeout]** in [!UICONTROL minute(s)], [!UICONTROL hour(s)], [!UICONTROL day(s)], of [!UICONTROL week(s)]. De sessietime-out bepaalt hoe lang een sessie inactief kan zijn (er treden geen gebeurtenissen op) voordat een nieuwe sessie wordt gestart.

      Gebruik een korte sessietime-out (bijvoorbeeld 30 minuten) als u vooral online interacties wilt analyseren. Zo kunt u bijvoorbeeld analyseren of profielen die uw productpagina&#39;s in de online winkel bezoeken, producten aan de winkelwagentje hebben toegevoegd of zelfs online zijn aangeschaft.

      Gebruik een lange sessietime-out (bijvoorbeeld 3 maanden) als u online en offline gegevens combineert en wilt analyseren of klanten die een of meer van uw producten hebben aangeschaft, binnen de eerste drie maanden na hun aankoop contact hebben opgenomen met uw contactcentrum.


   2. Selecteer een metrische waarde in het menu **[!UICONTROL Drop a metric here]** lijst onder **[!UICONTROL Start new session with a metric]**. U kunt ook een metrische waarde slepen en neerzetten vanuit het linkerdeelvenster van het dialoogvenster **[!UICONTROL Drop a metric field]**. De geselecteerde metrische waarde bepaalt het begin van een nieuwe zitting. U kunt meerdere metrische waarden definiëren.

      U kunt om het even welk soort metrisch gebruiken om een nieuwe zitting te bepalen. Stel dat u elke keer dat een profiel uw mobiele app start, een nieuwe sessie wilt definiëren. In **[!UICONTROL Data view]** > **[!UICONTROL Components]**, definieert u een component van het metrische type, genaamd **[!UICONTROL Launches]** op basis van een **[!UICONTROL appInteraction]** **[!UICONTROL Name]** schemaveld. U geeft de **[!UICONTROL Launches]** De metrische component om slechts de waarde te tellen wanneer de waarde aanpast `launch`.

      ![Metrische componentinitialen voor interactie van app](assets/component-launches.png)

      Vervolgens sleept u en zet u de **[!UICONTROL Launches]** metrisch als metrisch om een nieuwe zitting te bepalen.

      ![Instellingen sessie worden gestart](assets/session-settings-launches-metric.png)



4. Selecteren **[!UICONTROL Save]** of **[!UICONTROL Save and finish]** om de definitie van de zittingsmontages te bewaren.

