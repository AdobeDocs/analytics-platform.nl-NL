---
description: Meer informatie over foutberichten in Adobe Analysis Workspace en de bijbehorende componenten
title: Algemene foutberichten in Analysis Workspace
feature: FAQ
exl-id: 792c3b2e-bd24-4e98-b9ea-983c1189d52e
role: User
source-git-commit: caf53fe1727c77b4dcb5a9f7b67c368fade2f86c
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# Algemene foutberichten

Er kunnen fouten optreden bij de interactie met Analysis Workspace die ook van invloed zijn op de prestaties. Hieronder ziet u de meest voorkomende fouttypen, de reden waarom deze voorkomen en optimalisaties die kunnen worden gemaakt.

| Foutbericht | Waarom gebeurt dit? | Optimalisatie |
| --- | --- | --- |
| [!UICONTROL The data view is currently exceeding its reporting capacity. Please simplify the request or try again later.] |   |   |
| [!UICONTROL A system error has occurred. Please log a Customer Care request under **[!UICONTROL Help > Submit Support Ticket]** and include your error code.] | Adobe heeft te maken met een probleem dat moet worden opgelost. | Stuur de foutcode naar de klantenservice. |
| [!UICONTROL Error 500: Failed to load page] | De kwesties met uw lokaal netwerk, zoals bedrijf [firewallinstellingen](https://experienceleague.adobe.com/docs/analytics/technotes/ip-addresses.html), een factor die aan deze fout bijdraagt. Bovendien kan Adobe een probleem ervaren dat moet worden opgelost. | Meld u na enkele minuten opnieuw aan. Als het probleem zich blijft voordoen, dient u de EIM-ID-code van de instantie in bij de klantenservice. |
| [!UICONTROL One of the filters or the search in this visualization contains a text search that returned too many results.] | De filtercriteria of het rapportfilter zijn te breed. | Verfijn uw zoektekstcriteria en probeer het verzoek opnieuw. |
| [!UICONTROL The request is too complex.] | Uw rapportageaanvraag is te groot en kan niet worden uitgevoerd. Medewerkers aan deze fout zijn onderbrekingen vanwege de grootte van het verzoek, te veel overeenkomende items in een filter of zoekfilter, te veel meetgegevens, incompatibele afmetingen en metrische combinaties, enz. | Vereenvoudig uw verzoek door sommige kolommen of rijen in uw lijst te verwijderen, of denk na het splitsen van de lijst in afzonderlijke verzoeken. |
| [!UICONTROL Your request failed as a result of too many columns or pre-configured rows.] | Uw tabel bevat te veel vrije-vormcellen (rij * kolommen). | Verwijder kolommen of rijen in de tabel of u kunt de tabel opsplitsen in afzonderlijke aanvragen. |
