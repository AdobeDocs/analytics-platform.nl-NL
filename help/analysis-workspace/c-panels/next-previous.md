---
description: Begrijp hoe te om het Volgende of vorige puntenpaneel te gebruiken dat de volgende of vorige punten voor een specifieke afmeting toont.
title: Deelvenster Volgende of Vorige item
feature: Panels
role: User, Admin
exl-id: a5f6ce97-6720-4129-9ece-e2e834289d45
source-git-commit: ce4a21b1a1e89f14316a92fbdce38281db61e666
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Volgend of vorig deelvenster met items {#next-or-previous-item-panel}

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_button"
>title="Volgende of vorige item"
>abstract="Maak een deelvenster om te begrijpen welke dimensies mensen uit het verleden hebben gekregen of waar mensen uit de volgende dimensie naar toe gaan."

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_panel"
>title="Volgende of vorige item"
>abstract="Analyseer wat de meest gangbare plaatsen zijn waar bezoekers eerder vandaan kwamen of naar de volgende gaan. Geef afmetingen, afmetingen, richting en container op die u voor de visualisatie wilt gebruiken."


>[!BEGINSHADEBOX]

_dit artikel documenteert het Volgende of vorige puntenpaneel in_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**&#x200B;_.<br/>_zie [ Volgende of vorig puntenpaneel ](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/panels/next-previous) voor_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics** versie van dit artikel._

>[!ENDSHADEBOX]

Het deelvenster **[!UICONTROL Next or previous item]** bevat een aantal tabellen en visualisaties om het volgende of vorige dimensie-item voor een specifieke dimensie te identificeren. U kunt bijvoorbeeld bekijken naar welke pagina&#39;s klanten het vaakst zijn gegaan nadat ze de startpagina hebben bezocht.

## Gebruiken {#use}

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_container"
>title="Container"
>abstract="Selecteer de container om het bereik van uw vraag te bepalen."

Een deelvenster **[!UICONTROL Next or previous item]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Next or previous item]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [ een paneel ](panels.md#create-a-panel) creëren.

1. Specificeer de [ input ](#panel-input) voor het paneel.

1. Neem de [ output ](#panel-output) voor het paneel waar.

### Deelvensterinvoer

U kunt het deelvenster [!UICONTROL Next or previous item] configureren met de volgende invoerinstellingen:

![ Volgende of vorige puntenpaneel ](assets/next-or-previous-item.png)

| Invoer | Beschrijving |
| --- | --- |
| **[!UICONTROL Dimension]** | Selecteer de dimensie waarvoor u volgende of vorige punten wilt onderzoeken. |
| **[!UICONTROL Dimension item]** | Selecteer het specifieke dimensie-item in het midden van uw volgende/vorige vraag. |
| **[!UICONTROL Direction]** | Geef op of u naar het dimensie-item [!UICONTROL Next] of [!UICONTROL Previous] zoekt. |
| **[!UICONTROL Container]** | Selecteer de container, **[!UICONTROL Global Account]** [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, **[!UICONTROL Account]** [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, **[!UICONTROL Buying Group]** [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, **[!UICONTROL Opportunity]** [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, **[!UICONTROL Session]** of **[!UICONTROL Person]**, om het werkingsgebied van uw onderzoek te bepalen. |

{style="table-layout:auto"}

Selecteer **[!UICONTROL Build]** om het deelvenster te maken.

### Deelvensteruitvoer

Het deelvenster [!UICONTROL Next or previous item] retourneert een uitgebreide set gegevens en visualisaties om u te helpen beter te begrijpen welke instanties specifieke dimensie-items volgen of hieraan voorafgaan.


![ Volgende/Vorige paneeloutput ](assets/next-or-previous-item-output.png)


| Visualisatie | Beschrijving |
| --- | --- |
| **[!UICONTROL Horizontal bar]** | Hiermee geeft u de volgende (of vorige) items weer op basis van het dimensie-item dat u selecteert. Als u de cursor boven een afzonderlijke balk houdt, wordt het bijbehorende item in de tabel Vrije vorm gemarkeerd. |
| **[!UICONTROL Summary number]** | Samenvattingsaantal op hoog niveau van alle volgende of vorige instanties van afmetingspunten voor de huidige maand (tot nu toe). |
| **[!UICONTROL Freeform table]** | Hiermee geeft u de volgende (of vorige) items weer op basis van het dimensie-item dat u selecteert, in een tabelindeling. Dit waren bijvoorbeeld de populairste pagina&#39;s (op voorvallen) die mensen na (of vóór) de startpagina of de werkruimtenpagina hebben weergegeven. |

{style="table-layout:auto"}


>[!MORELIKETHIS]
>
>[ creeer een paneel ](/help/analysis-workspace/c-panels/panels.md#create-a-panel)
>
