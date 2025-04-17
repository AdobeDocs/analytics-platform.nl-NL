---
title: Quantum metric session ID's verzamelen in Customer Journey Analytics
description: Wijzig uw implementatie om sessie-id's op te nemen zodat u deze kunt analyseren in Customer Journey Analytics.
role: User, Admin
solution: Customer Journey Analytics
feature: Use Cases
hidefromtoc: true
hide: true
exl-id: cfe4bafd-afe6-4738-94f1-30882893b3b6
source-git-commit: 03e9fb37684f8796a18a76dc0a93c4e14e6e7640
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Quantum metric session ID&#39;s verzamelen in Customer Journey Analytics

Sommige gebruiksgevallen, zoals [ het binden van de Metrische zitting van Quantum replay ](tie-session-replays.md) of [ gebruikend Metrische Quantum heatmaps ](heatmap.md) vereisen dat u uw implementatie wijzigt om Quantum Metrische zittingsIdentiteitskaart te verzamelen. Deze pagina schetst dat proces om die gegevens in uw bestaande implementatie met succes over te brengen.

## Vereisten:

Bij deze stappen wordt ervan uitgegaan dat u tags gebruikt in de gegevensverzameling van Adobe Experience Platform. U kunt deze methodes van de gegevensinzameling in een handmatige implementatie van SDK van het Web aanpassen als uw organisatie geen markeringen gebruikt.

Zie de [ Metrische de markeringsuitbreiding van het Quantum ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/analytics/quantum-metric) documentatie voor meer informatie.

## Stap 1: Leg de metrische sessie-id voor Quantum vast met de extensie Metrische tags Quantum

Ga als volgt te werk om de metrische sessie-id van Quantum toe te voegen aan de gegevens die u naar Adobe Experience Platform verzendt.

1. Gebruik de extensie Quantum Metric in de tags UI om gegevens naar Quantum Metric te verzenden.
1. Vier gegevenselementen maken:
   1. Een die de metrische sessie-id van Quantum vastlegt uit het cookie van Quantum Metric met de naam `QuantumMetricSessionID`
   1. Een id die de metrische sessie-id voor Quantum extraheert uit `localStorage` . Soms wordt dit gegevenselement sneller geladen dan de cookie die in het andere gegevenselement is ingesteld.
   1. Gebruik de gegevenselementassistent of aangepaste JavaScript om het knooppunt `s` uit het gegevenselement `localStorage` te extraheren.
   1. Een die logica gebruikt om eerst naar het element van de koekjesgegevens te zoeken en het terug te keren naar een XDM objecten weg indien gevonden. Probeer het geëxtraheerde `localStorage` -objectelement, indien niet gedefinieerd, te bekijken.
1. Verzend het laatste Quantum Metric session ID-gegevenselement naar het XDM-object dat in elke gebeurtenis wordt verzonden.

>[!NOTE]
>Soms werkt de SDK van het Web sneller dan de Metrische code van het Quantum. In deze gevallen wordt de sessie-id verzonden bij de volgende hit. Als een bezoeker naar buiten komt, wordt de sessie-id in deze gevallen niet verzameld.

## Stap 2: Ingesloten gegevenssetvelden bevestigen

Bevestig dat de datasets in uw verbinding nu Quantum Metric zittings identiteitskaart in de gewenste dataset hebben.

## Stap 3: Quantum metrische sessie-id toevoegen als een beschikbare dimensie

Bewerk de bestaande gegevensweergave om de sessie-id toe te voegen als een beschikbare dimensie in Customer Journey Analytics.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Data views]** (optioneel vanuit **[!UICONTROL Data management]** ) in het bovenste menu.
1. Selecteer de gewenste bestaande gegevensweergave.
1. Zoek de lijst met het veld Metrische sessie-id van Quantum links en sleep deze naar het gebied met afmetingen in het midden.
1. In de juiste ruit, plaats [ persistentie ](/help/data-views/component-settings/persistence.md) het plaatsen aan &quot;Zitting&quot;.
1. Klik op **[!UICONTROL Save]**.


