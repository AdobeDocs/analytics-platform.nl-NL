---
title: Uw CJA-gebruik schatten en beheren
description: Toont twee methodes om gebruik en één methode te schatten om het te beheren.
role: Admin
feature: CJA Basics
source-git-commit: 58d582b693708f883842fb6a18cc57d481f2b2ab
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---


# Uw CJA-gebruik schatten en beheren

Om uw gebruik van CJA te begrijpen, kunt u 2 methodes gebruiken:

* De gebeurtenisgegevens voor elke verbinding toevoegen (zie **De verbindingsgrootte schatten** hieronder)
* Analysis Workspace gebruiken om...

Je CJA-gebruik beheren:

* De CJA API gebruiken

## De verbindingsgrootte schatten {#estimate-size}

Mogelijk moet u weten hoeveel rijen met gebeurtenisgegevens u momenteel hebt in [!UICONTROL Customer Journey Analytics]. Ga als volgt te werk om een accuraat overzicht te krijgen van het gebruik van de records (gegevensrijen) met gebeurtenisgegevens van uw organisatie **voor elk van de verbindingen die door uw organisatie worden gecreeerd**.

>[!NOTE]
>
>Doe dit op de eerste vrijdag van elke maand, aangezien Adobe uw recentste gebruiksrapport op die dag in werking stelt.

1. In [!UICONTROL Customer Journey Analytics]klikt u op de knop **[!UICONTROL Connections]** tab.

   U kunt nu een lijst met al uw huidige verbindingen zien.

1. Klik op elke naam van de verbinding om deze weer te geven.

1. Voeg de **[!UICONTROL Records of event data available]** voor alle gemaakte verbindingen. (Afhankelijk van de grootte van de verbinding kan het even duren voordat het nummer wordt weergegeven.)

   ![gebeurtenisgegevens](assets/event-data.png)

1. Als u een som van alle rijen met gebeurtenisgegevens hebt, zoekt u de machtiging &quot;Rijen van gegevens&quot; op in het Customer Journey Analytics-contract dat uw bedrijf met Adobe heeft ondertekend.

   Dit geeft u het maximumaantal rijen van gegevens die in de Orde van de Verkoop worden geautoriseerd. Als het aantal rijen gegevens dat uit Stap 3 is voortgekomen groter is dan dit aantal, gaat u over.

1. U kunt deze situatie op verschillende manieren verhelpen:

   * Wijzig uw [instellingen voor gegevensbehoud](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/manage-connections.html#set-rolling-window-for-connection-data-retention).
   * [Ongebruikte verbindingen verwijderen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html#implications-of-deleting-data-components).
   * [Een gegevensset verwijderen in AEP](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html#implications-of-deleting-data-components).
   * Neem contact op met de accountmanager van de Adobe om een licentie voor extra capaciteit te verkrijgen.
