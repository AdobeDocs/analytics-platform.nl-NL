---
title: De metrische tijdsessie van Tie Quantum wordt opnieuw afgespeeld op gegevens in Customer Journey Analytics
description: Metrische Link Quantum-sessie wordt opnieuw afgespeeld met CJA-gegevens om beter te begrijpen waarom achter "wat" zit.
role: User, Admin
solution: Customer Journey Analytics
feature: Use Cases
hidefromtoc: true
hide: true
exl-id: fcc36457-4ce9-4c93-93e2-de03becfd5da
source-git-commit: 25a2c549c27918f80202bde4cd30e305f4a295f3
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# De metrische tijdsessie van Tie Quantum wordt opnieuw afgespeeld op gegevens in Customer Journey Analytics

Door Quantum Metric-sessiereplay te koppelen aan CJA-gegevens, kunnen klanten beter begrijpen waarom achter &quot;wat&quot; zit.  Workspace kan worden gebruikt om sessies met wrijving te ontdekken, dan kunt u hyperlinked zitting IDs klikken om zittingsreplay in Quantum Metric te onderzoeken.  Deze gegevens maken het mogelijk om gedrag binnen een sessie te bekijken en beter te begrijpen wat de wrijving van de consument stimuleert.  Door sessiereacties die aan CJA zijn gekoppeld, kunt u in uw ervaring kritieke context rond het gedrag van de klant vastleggen.

## Vereisten

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
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Data views]** in het bovenste menu.
1. Selecteer de gewenste bestaande gegevensweergave.
1. Zoek de lijst met het veld Metrische sessie-id van Quantum links en sleep deze naar het gebied met afmetingen in het midden.
1. In de juiste ruit, plaats [ persistentie ](/help/data-views/component-settings/persistence.md) het plaatsen aan &quot;Zitting&quot;.
1. Klik op **[!UICONTROL Save]**.

## Stap 4: Vorm Workspace om de dimensie van zitting-identiteitskaart aan te passen

Creeer een vrije vormlijst in Workspace en vorm het zodat de waarden van zittingidentiteitskaart verbindingen direct aan Metric Quantum zijn.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Workspace]** in het bovenste menu.
1. Selecteer een bestaand project of maak een project.
1. Creeer de lijst van de a [ Vrije vorm ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md).
1. Sleep de dimensie van sessie-id naar het Workspace-canvas.
1. Klik met de rechtermuisknop op de kolomkop voor de dimensie en selecteer vervolgens **[!UICONTROL Create hyperlinks for all dimension items]** .
1. Selecteer **[!UICONTROL Create a custom URL]** .
1. Plak de volgende URL-structuur:

   ```
   https://adobe.quantummetric.com/#/replay/cookie:$value
   ```

1. Klik op **[!UICONTROL Create]**.

Elke sessie-id is nu een klikbare koppeling. Zie [ hyperlinks in een vrije vormlijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md) voor meer informatie bij het toevoegen van hyperlinks aan de afmetingspunten van Analysis Workspace creëren.

## Stap 5: sessies van Customer Journey Analytics weergeven

Zodra u een Instesting segment hebt gevonden dat u zittingsreplay wilt onderzoeken, kunt u het op het paneel toepassen dat uw verbindingen van identiteitskaart van de zitting en filter door segment omvat. De lijst keert alle zittingen in dat segment terug, en u kunt om het even welk van hen klikken om verder in Metrisch Quantum te onderzoeken.

Zie [ de ondernemingsgids om ](https://www.quantummetric.com/resources/ebook/the-enterprise-guide-to-session-replay) op Metrisch Quantum voor meer informatie opnieuw te spelen. U kunt uw Metrische vertegenwoordiger van de klantensteun van Quantum ook contacteren of een verzoek indienen door het [ Metrische Portaal van het Verzoek van de Klant van Quantum Metrisch ](https://community.quantummetric.com/s/public-support-page).
