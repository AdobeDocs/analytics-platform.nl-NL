---
description: Leer hoe te om debugger te gebruiken om kwesties met uw project in Analysis Workspace problemen op te lossen.
keywords: Analysis Workspace
feature: Workspace Basics
title: Foutopsporing van project
role: User
source-git-commit: 4d902bab01c1c795cb7d852066128f6b9db0823a
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Foutopsporing van project

Debugger van het project helpt u en de Steun van Adobe om kwesties met uw projecten in Analysis Workspace problemen op te lossen. De Steun van Adobe zou u kunnen verzoeken om debugger toe te laten om kaartjes problemen op te lossen u met de Steun van Adobe hebt opgeheven. Voorbeelden van problemen zijn de laadtijd van visualisaties of beschadigde componenten in uw visualisaties.

>[!NOTE]
>
>Om debugger te gebruiken, moet u **&#x200B;**&#x200B;uitgeven of **Exemplaar** [ toegang tot het project ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-25744) hebben.
>


## Foutopsporing inschakelen

>[!IMPORTANT]
>
>Sla uw project op voordat u foutopsporing inschakelt.
>

Om debugger toe te laten:

1. Selecteer **[!UICONTROL Help]** > **[!UICONTROL Enable debugger]** in het Analysis Workspace-projectmenu.
1. Selecteer **[!UICONTROL OK]** in het dialoogvenster **[!UICONTROL Enable Debugger]** .
1. Bevestig wanneer de browser u vraagt de pagina of site opnieuw te laden.


## Foutopsporing gebruiken

Wanneer u debugger hebt toegelaten, hebben alle visualisaties in uw project een extra ![ Bug ](/help/assets/icons/Bug.svg) pictogram.

Om debugger voor een specifieke visualisatie te gebruiken:

1. Selecteer ![ Bug ](/help/assets/icons/Bug.svg) bij de bovenkant van visualisatie.

   ![ Debugger contextmenu ](assets/debugger-context-menu.png)

1. Selecteer de gewenste actie in het contextmenu. De beschikbare acties zijn afhankelijk van de visualisatie en geven het type foutopsporing aan dat u wilt uitvoeren. Als u bijvoorbeeld **[!UICONTROL Anomalies]** selecteert, wilt u fouten opsporen in de functionaliteit voor visualisatie.
1. Selecteer een tijdstempel in het submenu.
1. Er wordt een **[!UICONTROL Oberon XML]** foutopsporingsvenster geopend met informatie over de specifieke functionaliteit die door de visualisatie wordt uitgevoerd. Zie hieronder voor een voorbeeld van de uitvoer van een afwijkend verzoek.

   ![ Output zuivert verzoek ](assets/debugger-oberon.png)

   De details zijn:

   * **[!UICONTROL Request timestamp]**
   * **[!UICONTROL Response timestamp]**
   * **[!UICONTROL &#x200B; Request time]**
   * **[!UICONTROL Queue time]**
   * **[!UICONTROL Server processing time]**
   * **[!UICONTROL Lookup time]**
   * **[!UICONTROL Complexity]**
   * **[!UICONTROL Month boundaries]**
   * **[!UICONTROL Columns]**
   * **[!UICONTROL Segments]**
   * **[!UICONTROL XML]** **[!UICONTROL Request]** and **[!UICONTROL Response]**
   * **[!UICONTROL cURL Request]**
   * **[!UICONTROL JSON]** **[!UICONTROL Request]** and **[!UICONTROL Response]**

1. Het Exemplaar van het gebruik ![ ](/help/assets/icons/Copy.svg) om al te kopiëren zuivert informatie aan het klembord. **[!UICONTROL Copy all field to clipboard]** Plak de gegevens in de editor of het gereedschap van uw voorkeur. De informatie bestaat uit:

   * XML (request)
   * XML (reactie)
   * JSON (verzoek)
   * JSON (reactie)
   * Cursusverzoek

1. Het Exemplaar van het gebruik ![ **&#x200B; ](/help/assets/icons/Copy.svg) &#x200B;** d onderaan [!UICONTROL Copy to clipboard] om het verzoek aan het klembord te kopiëren.**[!UICONTROL cURL Request]**
1. Beweeg over om het even welke **[!UICONTROL Request]** of **[!UICONTROL Response]** tekstgebieden om ![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy to clipboard]** te openbaren en te selecteren om de inhoud van dat tekstgebied (XML of JSON) aan het klembord te kopiëren.

1. Uitwisseling om het even welke informatie u hebt gekopieerd en die de Steun van Adobe verzocht om de visualisaties in uw project van Analysis Workspace problemen op te lossen.

1. Selecteer **[!UICONTROL Cancel]** om het venster **[!UICONTROL Oberon XML]** Foutopsporing te sluiten en terug te keren naar uw project.

Herhaal bovenstaande stappen voor alle andere visualisatie die u wilt oplossen.

## Foutopsporing uitschakelen

>[!IMPORTANT]
>
>Alvorens u debugger onbruikbaar maakt, sparen om het even welke veranderingen u aan uw project aanbracht en als deel van de het zuiveren oefening wilt houden.
>

Het foutopsporingsprogramma uitschakelen:

1. Selecteer **[!UICONTROL Help]** > **[!UICONTROL Disable debugger]** in het Analysis Workspace-projectmenu.
1. Selecteer **[!UICONTROL OK]** in het dialoogvenster **[!UICONTROL Disable debugger]** .
1. Bevestig wanneer de browser u vraagt de pagina of site opnieuw te laden.



