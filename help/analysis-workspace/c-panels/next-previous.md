---
description: Een deelvenster waarin de volgende of vorige dimensie-items voor een specifieke dimensie worden weergegeven.
title: Volgend of vorig deelvenster met items
feature: Panels
role: User, Admin
exl-id: a5f6ce97-6720-4129-9ece-e2e834289d45
source-git-commit: f8abf388e0cb1e2e2eb9ff69fed2c542a26dcd66
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Volgend of vorig deelvenster met items {#next-or-previous-item-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_button"
>title="Volgende of vorige item"
>abstract="Maak een deelvenster om te begrijpen welke dimensies mensen uit het verleden hebben gekregen of waar mensen uit de volgende dimensie naar toe gaan."

<!-- markdownlint-disable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_panel"
>title="Nesten of vorig item"
>abstract="Analyseer wat de meest gangbare plaatsen zijn waar bezoekers eerder vandaan kwamen of naar de volgende gaan.<br/><br/>**Dimension**: Selecteer een afmeting. Bijvoorbeeld **Pagina**.<br/>**punt van het Dimension**: Selecteer een specifiek afmetingspunt. Bijvoorbeeld **Homepage**.<br/>**Richting**: Selecteer **daarna** om de afmetingspunten onmiddellijk na uw geselecteerd afmetingspunt te zien. Selecteer **Vorige** om de afmetingspunten te zien die tot uw geselecteerd afmetingspunt leiden.<br/>**Container**: Selecteer **Zitting** om de volgende/vorige afmetingspunten binnen de zelfde zitting te zien, of **Persoon** te selecteren om het volgende/vorige afmetingspunt voor de zelfde persoon te zien."

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

*dit artikel documenteert het Volgende of vorige puntenpaneel in ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg)**Customer Journey Analytics**.<br/> zie [ Volgende of vorig puntenpaneel ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/next-previous) voor ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg)**Adobe Analytics**versie van dit artikel.*

>[!ENDSHADEBOX]

Het deelvenster **[!UICONTROL Next or previous item]** bevat een aantal tabellen en visualisaties om het volgende of vorige dimensie-item voor een specifieke dimensie te identificeren. U kunt bijvoorbeeld bekijken naar welke pagina&#39;s klanten het vaakst zijn gegaan nadat ze de startpagina hebben bezocht.

## Gebruiken

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
| **[!UICONTROL Container]** | Selecteer de container [!UICONTROL Session] of [!UICONTROL Person] (standaard) om het bereik van uw vraag te bepalen. |

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
