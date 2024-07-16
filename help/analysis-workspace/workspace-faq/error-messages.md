---
description: Meer informatie over foutberichten in Adobe Analysis Workspace en de bijbehorende componenten
title: Algemene foutberichten in Analysis Workspace
feature: FAQ
exl-id: 792c3b2e-bd24-4e98-b9ea-983c1189d52e
role: User
source-git-commit: fe089afb2022d8c4b50346bb81d6ba4ad6404014
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Algemene foutberichten

Er kunnen fouten optreden bij de interactie met Analysis Workspace die ook van invloed zijn op de prestaties. Hieronder ziet u de meest voorkomende fouttypen, de reden waarom deze voorkomen en optimalisaties die kunnen worden gemaakt.

| Foutbericht | Waarom gebeurt dit? | Optimalisatie |
| --- | --- | --- |
| [!UICONTROL The data view is experiencing unusually heavy reporting. Please try again later.] | Uw organisatie probeert te veel gelijktijdige aanvragen uit te voeren in een specifieke gegevensweergave. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, geplande rapporten, geplande alarm, en gezamenlijke gebruikers die het melden verzoeken. | Verspreid uw verzoeken en programma&#39;s voor de gegevensmening gelijkmatiger door de dag.<p>De beheerders kunnen de [ Rapporterende Manager van de Activiteit gebruiken om verzoeken ](/help/reporting-activity-manager/reporting-activity-overview.md) te identificeren en te annuleren die rapporteringscapaciteit verbruiken.</p> |
| [!UICONTROL This report is too complex. Please review best practices for building Analysis Workspace reports.] | Uw rapportageaanvraag is te groot en kan niet worden uitgevoerd. Medewerkers aan deze fout zijn time-outs vanwege de complexiteit van het verzoek. | Vereenvoudig uw verzoek door het datumbereik te verkorten, de filtercriteria te vereenvoudigen of kolommen of rijen uit de tabel te verwijderen. Of u kunt de tabel opsplitsen in afzonderlijke verzoeken. |
| [!UICONTROL The data view is currently exceeding its reporting capacity. Please simplify the request or try again later.] | Uw organisatie probeert te veel gelijktijdige aanvragen uit te voeren in een specifieke gegevensweergave. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, en gezamenlijke gebruikers die rapportageverzoeken indienen. | Verspreid uw verzoeken en programma&#39;s voor de gegevensmening gelijkmatiger door de dag. |
| [!UICONTROL A system error has occurred. Please log a Customer Care request under **[!UICONTROL Help > Submit Support Ticket]** and include your error code.] | Adobe heeft te maken met een probleem dat moet worden opgelost. | Stuur de foutcode naar de klantenservice. |
| [!UICONTROL Error 500: Failed to load page] | De kwesties met uw lokaal netwerk, zoals bedrijf [ firewallmontages ](https://experienceleague.adobe.com/docs/analytics/technotes/ip-addresses.html), zijn een bijdragende factor aan deze fout. Bovendien kan Adobe een probleem ervaren dat moet worden opgelost. | Meld u na enkele minuten opnieuw aan. Als het probleem zich blijft voordoen, dient u de EIM-ID-code van de instantie in bij de klantenservice. |
| [!UICONTROL Your request failed as a result of too many columns or pre-configured rows.] | Uw tabel bevat te veel vrije-vormcellen (rij * kolommen). | Verwijder kolommen of rijen in de tabel of u kunt de tabel opsplitsen in afzonderlijke aanvragen. |
