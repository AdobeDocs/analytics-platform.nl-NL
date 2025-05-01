---
title: De metrische tijdsessie van Tie Quantum wordt opnieuw afgespeeld op gegevens in Customer Journey Analytics
description: Metrische Link Quantum-sessie wordt opnieuw afgespeeld met CJA-gegevens om beter te begrijpen waarom achter "wat" zit.
role: User, Admin
solution: Customer Journey Analytics
feature: Use Cases
hidefromtoc: true
hide: true
exl-id: fcc36457-4ce9-4c93-93e2-de03becfd5da
source-git-commit: a03505aeb56f99b28f50819765a496705876b89c
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 1%

---

# De metrische tijdsessie van Tie Quantum wordt opnieuw afgespeeld op gegevens in Customer Journey Analytics

Door Quantum Metric-sessiereplay te koppelen aan CJA-gegevens, kunnen klanten beter begrijpen waarom achter &quot;wat&quot; zit.  Workspace kan worden gebruikt om sessies met wrijving te ontdekken, dan kunt u hyperlinked zitting IDs klikken om zittingsreplay in Quantum Metric te onderzoeken.  Deze gegevens maken het mogelijk om gedrag binnen een sessie te bekijken en een beter inzicht te krijgen in wat de wrijving van de consument voedt.  Door sessiereacties die aan CJA zijn gekoppeld, kunt u in uw ervaring kritieke context rond het gedrag van de klant vastleggen.

## Vereisten

Bij deze stappen wordt ervan uitgegaan dat u tags gebruikt in de gegevensverzameling van Adobe Experience Platform. U kunt deze methodes van de gegevensinzameling in een handmatige implementatie van SDK van het Web aanpassen als uw organisatie geen markeringen gebruikt.

Zie de [ Metrische de markeringsuitbreiding van het Quantum ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/analytics/quantum-metric) documentatie voor meer informatie.

## Stap 1: Maak een schemaveld om de metrische sessie-id van Quantum aan te passen

Voor dit gebruik is een speciaal schemaveld vereist om gegevens naar te verzenden. U kunt dit gebied in om het even welke gewenste plaats in uw schema tot stand brengen en het noemen wat u wilt. Er worden voorbeeldwaarden gegeven als uw organisatie geen voorkeur op naam of locatie heeft.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Ga naar **[!UICONTROL Data Collection]** > **[!UICONTROL Schemas]**.
1. Selecteer het gewenste schema in de lijst.
1. Selecteer ![ voeg gebiedspictogram ](/help/assets/icons/AddCircle.svg) naast het gewenste voorwerp toe. Bijvoorbeeld naast `Implementation Details` .
1. Typ rechts in het scherm de gewenste waarde [!UICONTROL Name] . Bijvoorbeeld `qmSessionId` .
1. Voer het gewenste [!UICONTROL Display name] in. Bijvoorbeeld `Quantum Metric session ID` .
1. Selecteer [!UICONTROL Type] als **[!UICONTROL String]** .
1. Selecteer **[!UICONTROL Save]** .

## Stap 2: Leg de metrische sessie-id voor Quantum vast met de metrische tagextensie Quantum

Ga als volgt te werk om de metrische sessie-id van Quantum toe te voegen aan de gegevens die u naar Adobe Experience Platform verzendt.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Ga naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]**.
1. Selecteer de gewenste eigenschap tag.
1. Selecteer **[!UICONTROL Data Elements]** en selecteer vervolgens **[!UICONTROL Add Data Element]** .
1. Stel de volgende instellingen in:
   * **[!UICONTROL Name]**: `Quantum Metric session ID`
   * **[!UICONTROL Extension]**: [!UICONTROL Core]
   * **[!UICONTROL Data Element Type]**: [!UICONTROL Custom Code]
1. Selecteer de knop **[!UICONTROL Open Editor]** en plak in de volgende code:

   ```js
   // Check for the presence of the Quantum Metric session ID cookie
   const qmCookie = _satellite.cookie.get("QuantumMetricSessionID");
   if(qmCookie != null) return qmCookie;
   // If a cookie is not set, check local storage
   const qmLocalStorage = JSON.parse(localStorage.getItem("QM_S") || "{}");
   if (qmLocalStorage?.s != null) return qmLocalStorage.s;
   ```

1. Selecteer **[!UICONTROL Save]** .

## Stap 3: Wijs het gegevenselement aan het gewenste XDM schemagebied toe

Nu het gegevenselement logica heeft om de gewenste waarde te verkrijgen, wijst u het gegevenselement toe aan het XDM-object.

1. Selecteer **[!UICONTROL Data Elements]** binnen de eigenschap tag en selecteer vervolgens het gegevenselement waarin het XDM-object zich bevindt.
1. Navigeer in de rechterkolom van dit gegevenselement naar het pad dat is ingesteld bij het maken van het schemaveld.
1. Stel de waarde in op de naam van het gegevenselement dat wordt omgeven door procenttekens. Bijvoorbeeld `%Quantum Metric session ID%` .
1. Selecteer **[!UICONTROL Save]** .
1. Voeg een bibliotheek toe en publiceer uw wijzigingen in de productie.

Als uw XDM-object al is opgenomen in een configuratie voor een send-gebeurtenisactie, begint u gegevens te zien wanneer de wijzigingen worden gepubliceerd.

>[!NOTE]
>
>Soms werkt de SDK van het Web sneller dan de Metrische code van het Quantum. In deze gevallen wordt de sessie-id verzonden bij de volgende hit. Als een bezoeker naar buiten komt, wordt de sessie-id in deze gevallen niet verzameld.

## Stap 3: Quantum metrische sessie-id toevoegen als een beschikbare dimensie

Zodra de bovenstaande wijzigingen in uw implementatie zijn gepubliceerd, bewerkt u de bestaande gegevensweergave om de sessie-id toe te voegen als een beschikbare dimensie in Customer Journey Analytics.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Data views]** in het bovenste menu.
1. Selecteer de gewenste bestaande gegevensweergave.
1. Zoek het veld Metrische sessie-id voor Quantum aan de linkerkant en sleep dit naar het gebied met afmetingen in het midden.
1. In de juiste ruit, plaats [ persistentie ](/help/data-views/component-settings/persistence.md) het plaatsen aan `Session`.
1. Selecteer **[!UICONTROL Save]** .

## Stap 4: Vorm Analysis Workspace om de dimensie van zitting-identiteitskaart aan te passen

Creeer een vrije vormlijst in Workspace en vorm het zodat de waarden van zittingidentiteitskaart rechtstreeks met Metric Quantum verbinden.

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

Zodra u een interessant segment hebt gevonden dat u zittingsreplay wilt onderzoeken, kunt u het op het paneel toepassen dat uw verbindingen van zittingidentiteitskaart omvat. De lijst keert alle zittingen in dat segment terug, en u kunt om het even welk van hen klikken om verder in Metrisch Quantum te onderzoeken.

Zie [ de ondernemingsgids om ](https://www.quantummetric.com/resources/ebook/the-enterprise-guide-to-session-replay) op Metrisch Quantum voor meer informatie opnieuw te spelen. U kunt uw Metrische vertegenwoordiger van de klantensteun van Quantum ook contacteren of een verzoek indienen door het [ Metrische Portaal van het Verzoek van de Klant van Quantum Metrisch ](https://community.quantummetric.com/s/public-support-page).
