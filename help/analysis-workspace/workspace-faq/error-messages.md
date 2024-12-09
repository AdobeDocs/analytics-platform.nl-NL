---
description: Meer informatie over de foutberichten en over het oplossen van problemen in Adobe Analysis Workspace
title: Algemene fouten en probleemoplossing in Analysis Workspace
feature: FAQ
exl-id: 792c3b2e-bd24-4e98-b9ea-983c1189d52e
role: User
source-git-commit: 4942c83e34b129e3718084601d5a733bcebf4de9
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 9%

---

# Fouten en problemen oplossen

Bij interactie met Analysis Workspace kunnen er fouten optreden die de functionaliteit of prestaties kunnen beïnvloeden. Hieronder ziet u de meest voorkomende fouttypen, de reden waarom deze voorkomen en optimalisaties die kunnen worden gemaakt.

## Foutberichten

Sommige veelvoorkomende foutberichten die u kunt zien bij het gebruik van Analysis Workspace:

| Foutbericht | Waarom treedt de fout op? | Optimalisatie |
| --- | --- | --- |
| [!UICONTROL The data view is experiencing unusually heavy reporting. Please try again later.] | Uw organisatie probeert te veel gelijktijdige aanvragen uit te voeren in een specifieke gegevensweergave. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, geplande rapporten, geplande alarm, en gezamenlijke gebruikers die het melden verzoeken. | Verspreid uw verzoeken en programma&#39;s voor de gegevensmening gelijkmatiger door de dag.<p>De beheerders kunnen de [ Rapporterende Manager van de Activiteit gebruiken om verzoeken ](/help/reporting-activity-manager/reporting-activity-overview.md) te identificeren en te annuleren die rapporteringscapaciteit verbruiken.</p> |
| [!UICONTROL This report is too complex. Please review best practices for building Analysis Workspace reports.] | Uw rapportageaanvraag is te groot en kan niet worden uitgevoerd. Medewerkers aan deze fout zijn time-outs vanwege de complexiteit van het verzoek. | Vereenvoudig uw verzoek. U kunt bijvoorbeeld het datumbereik verkorten of de filtercriteria vereenvoudigen of kolommen of rijen uit de tabel verwijderen. U zou ook kunnen overwegen de lijst in afzonderlijke verzoeken te verdelen. |
| [!UICONTROL The data view is currently exceeding its reporting capacity. Please simplify the request or try again later.] | Uw organisatie probeert te veel gelijktijdige aanvragen uit te voeren in een specifieke gegevensweergave. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, en gezamenlijke gebruikers die rapportageverzoeken indienen. | Verspreid uw verzoeken en programma&#39;s voor de gegevensmening gelijkmatiger door de dag. |
| [!UICONTROL A system error has occurred. Please log a Customer Care request under **[!UICONTROL Help > Submit Support Ticket]** and include your error code.] | Adobe heeft te maken met een probleem dat moet worden opgelost. | Stuur de foutcode naar de klantenservice. |
| [!UICONTROL Error 500: Failed to load page] | De kwesties met uw lokaal netwerk, zoals bedrijf [ firewallmontages ](/help/technotes/ip-addresses.md), zijn een bijdragende factor aan deze fout. Bovendien kan Adobe een probleem ervaren dat moet worden opgelost. | Meld u na enkele minuten opnieuw aan. Als het probleem zich blijft voordoen, dient u de EIM-ID-code van de instantie in bij de klantenservice. |
| [!UICONTROL Your request failed as a result of too many columns or pre-configured rows.] | Uw tabel bevat te veel vrije-vormcellen (rij * kolommen). | Verwijder kolommen of rijen in de tabel of u kunt de tabel opsplitsen in afzonderlijke aanvragen. |


## Problemen oplossen

Wanneer het gebruiken van de Werkruimte van de Analyse, kunt u de informatie gebruiken hieronder om sommige gemeenschappelijke kwesties problemen op te lossen.

| Probleem | Hoe te om problemen op te lossen |
|---|---|
| Wanneer ik metrisch over sleep, zegt het *Ongeldige gegevens*. | De melding &quot;Ongeldige data&quot; betekent dat Adobe geen data kan retourneren met de combinatie van dimensies en metrics die in het rapport wordt gebruikt. Zo kunnen twee metrics die boven op elkaar zijn gestapeld, niet als data worden geretourneerd, omdat er geen manier is om twee metrics op die manier weer te geven. Plaats de metriek in plaats daarvan naast elkaar. |
| Wanneer ik metrisch over sleep, zie ik geen daadwerkelijke gegevens - enkel nul. | Als u een werkruimterapport hebt gemaakt maar er geen gegevens zijn, kunt u een aantal dingen controleren:<ul><li>Als u een filter in uw rapport toepaste, zouden de filtercriteria geen gegevens kunnen aanpassen. Probeer het filter te verwijderen of de filterdefinitie aan te passen.</li><li>Controleer het datumbereik in de rechterbovenhoek en zorg ervoor dat het is ingesteld op een waarde die u verwacht.</li><li>Navigeer aan uw website en gebruik [ Debugger ](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) om te bevestigen dat het gegeven wordt verzameld.</li></ul> |
