---
description: Een deelvenster waarin de volgende of vorige dimensie-items voor een specifieke dimensie worden weergegeven.
title: Paneel Volgend of vorig item
feature: Panels
role: User, Admin
exl-id: a5f6ce97-6720-4129-9ece-e2e834289d45
source-git-commit: c94e97723a4ed30e675144e02196c93016b13235
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Paneel Volgend of vorig item {#next-or-previous-item-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_button"
>title="Volgend of vorig artikel"
>abstract="Maak een deelvenster om inzicht te krijgen in de vorige dimensies waar mensen vandaan komen of de volgende dimensie waar mensen naartoe gaan."

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_panel"
>title="Volgend of vorig artikel"
>abstract="Analyseer wat de meest voorkomende plaatsen zijn waar bezoekers eerder vandaan kwamen of naartoe gaan. Geef de dimensie, het dimensie-item, de richting en de container op die u voor de visualisatie wilt gebruiken."



<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

_In dit artikel wordt het deelvenster Het volgende of het vorige item in_ ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**&#x200B;_ beschreven.<br/>_Zie [het deelvenster](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/next-previous) Volgend of vorig item voor de_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics-versie** van dit artikel._

>[!ENDSHADEBOX]

Het **[!UICONTROL Next or previous item]** deelvenster bevat een aantal tabellen en visualisaties om het volgende of vorige dimensie-item voor een specifieke dimensie te identificeren. U kunt bijvoorbeeld nagaan welke pagina&#39;s klanten het vaakst hebben bezocht nadat ze de startpagina hebben bezocht.

## Gebruiken {#use}

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_container"
>title="Container"
>abstract="Selecteer de container om de reikwijdte van uw vraag te bepalen."

Een deelvenster gebruiken **[!UICONTROL Next or previous item]** :

1. Maak een **[!UICONTROL Next or previous item]** deelvenster. Zie [Een paneel maken voor meer informatie over het maken van een deelvenster](panels.md#create-a-panel).

1. Geef de [invoer](#panel-input) voor het paneel op.

1. Let op de [uitvoer](#panel-output) van het paneel.

### Paneel invoer

U kunt het [!UICONTROL Next or previous item] paneel configureren met behulp van de volgende invoerinstellingen:

![Paneel Volgend of vorig item](assets/next-or-previous-item.png)

| Invoer | Beschrijving |
| --- | --- |
| **[!UICONTROL Dimension]** | Selecteer de dimensie waarvoor u de volgende of vorige items wilt verkennen. |
| **[!UICONTROL Dimension item]** | Selecteer het specifieke dimensie-item in het midden van uw volgende / vorige aanvraag. |
| **[!UICONTROL Direction]** | Geef aan of u op zoek bent naar het [!UICONTROL Next] item of het [!UICONTROL Previous] dimensie-item. |
| **[!UICONTROL Container]** | Selecteer de container, **[!UICONTROL Global Account]** [!BADGE B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, **[!UICONTROL Account]** [!BADGE B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, [!BADGE **[!UICONTROL Buying Group]** B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, **[!UICONTROL Session]** [!BADGE **[!UICONTROL Opportunity]** B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"} of **[!UICONTROL Person]**, om de reikwijdte van uw vraag te bepalen. |

{style="table-layout:auto"}

Selecteer **[!UICONTROL Build]** om het paneel samen te stellen.

### Paneel uitgang

Het [!UICONTROL Next or previous item] deelvenster retourneert een uitgebreide set gegevens en visualisaties om u te helpen beter te begrijpen welke exemplaren volgen op of voorafgaan aan specifieke dimensie-items.


![Uitvoer van het volgende/vorige paneel](assets/next-or-previous-item-output.png)


| Visualisatie | Beschrijving |
| --- | --- |
| **[!UICONTROL Horizontal bar]** | Geeft een overzicht van de volgende (of vorige) items op basis van het dimensie-item dat u selecteert. Als u de muisaanwijzer op een afzonderlijke balk plaatst, wordt het bijbehorende item in de Freeform-tabel gemarkeerd. |
| **[!UICONTROL Summary number]** | Overzichtsnummer op hoog niveau van alle volgende of vorige dimensie-items voor de huidige maand (tot nu toe). |
| **[!UICONTROL Freeform table]** | Geeft een overzicht van de volgende (of vorige) items op basis van het dimensie-item dat u selecteert, in een tabelindeling. Bijvoorbeeld wat de meest populaire pagina&#39;s waren (naar voorkomelijkheden) waar mensen naartoe gingen na (of voor) de startpagina of de werkruimtepagina. |

{style="table-layout:auto"}


>[!MORELIKETHIS]
>
>[Een paneel maken](/help/analysis-workspace/c-panels/panels.md#create-a-panel)
>
