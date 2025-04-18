---
title: Metrische wrijvingsgebeurtenissen voor Quantum toevoegen aan Customer Journey Analytics
description: Voeg Quantum Metric verzamelde wrijvingsgebeurtenissen toe aan Customer Journey Analytics-gedragsgegevens om diepte toe te voegen aan inzichten in CJA.
role: User, Admin
solution: Customer Journey Analytics
feature: Use Cases
hidefromtoc: true
hide: true
exl-id: 1b7d5159-39b2-4ba4-be64-f448ae53c70e
source-git-commit: 9f954709a3dde01b4e01581e34aece07fe0256b1
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Metrische wrijvingsgebeurtenissen voor Quantum toevoegen aan Customer Journey Analytics

Quantum Metric verzamelt wrijvingsgebeurtenissen zoals vertraging bij het laden van pagina&#39;s, fouten bij het laden van pagina&#39;s, het klikken van rages en meer. Deze gebeurtenissen kunnen in Customer Journey Analytics worden doorgegeven als complementaire gebeurtenissen op de reis van de gebruiker. Met deze gecombineerde gegevens kunt u beter begrijpen wat de invloed van wrijving is op de stroomafwaartse metriek.

## Vereisten:

Voor dit gebruiksgeval gelden twee vereisten:

* U moet gerechtigd zijn tot het pakket van Metrische Quantum **Dev Ops**.
* U moet labels gebruiken in Adobe Experience Platform Data Collection.

## Stap 1: Leg wrijvingsgebeurtenissen vast met de metrische tagextensie Quantum

Zie [ Metrische uitbreiding van het Quantum ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/analytics/quantum-metric) in de gids van de Doelen van Adobe Experience Platform voor instructies op hoe te opstelling uw markeringen om Metrische gegevens van het Quantum te omvatten. Het gebruik van deze uitbreiding gaat meer rijen in een bestaande dataset over.

Gebruik labels in de gegevensverzameling van Adobe Experience Platform om de naam van de wrijvingsgebeurtenis handmatig in te stellen, zodat deze in het XDM-object kan worden opgenomen en geanalyseerd. Één manier om dit te doen is in de de douanecode van de regel:

```js
_satellite.setVar('qm_error_name','error rage click');
return true;
```

Voeg vervolgens het dynamisch ingestelde gegevenselement toe aan uw XDM-object:

![ het schermschot van de de foutennaam van het Quantum Metrische ](assets/error-name.png)

## Stap 2: voeg één of meerdere afmetingen en metriek aan de gegevensmening in Customer Journey Analytics toe

Bewerk de bestaande gegevensweergave om de sessie-id toe te voegen als een beschikbare dimensie in Customer Journey Analytics.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Data views]** (optioneel vanuit **[!UICONTROL Data management]** ) in het bovenste menu.
1. Selecteer de gewenste bestaande gegevensweergave.
1. Zoek de lijst met het gebeurtenisveld Quantum Metric friction aan de linkerkant en sleep deze naar het meetgebied in het midden.
1. In de juiste ruit, plaats [ omvatten/uitsluiten waarden ](/help/data-views/component-settings/include-exclude-values.md) het plaatsen aan de gewenste wrijvingsgebeurtenissen die u wilt volgen. U kunt veelvoudige wrijvingsgebeurtenissen aan zelfde metrisch toevoegen om hen te combineren. U kunt ook een andere kopie van het veld wrijvingsgebeurtenissen naar het metrische gebied slepen om andere wrijvingsgebeurtenissen als een aparte metrische waarde bij te houden.
1. Klik op **[!UICONTROL Save]** als u alle gewenste afmetingen en metriek hebt gemaakt.
1. Raadpleeg de documentatie bij Quantum Metric voor een volledige lijst met foutgebeurtenissen. Als u extra vragen hebt, contacteer uw Metrische vertegenwoordiger van de klantensteun van Quantum of voorleg een verzoek door het [ Metrische Portaal van het Verzoek van de Klant van Quantum Metrische ](https://community.quantummetric.com/s/public-support-page).

## Stap 3: Gebruik de dimensie en metriek met de rest van uw gegevens in Analysis Workspace

Met Quantum Metric friction-gebeurtenisgegevens die naast de overige bezoekersgegevens worden verzameld, kunt u ze precies gebruiken zoals u dat zou doen met andere maten of metrische gegevens in Customer Journey Analytics.

1. Login aan [ experience.adobe.com ](https://experience.adobe.com).
1. Navigeer naar Customer Journey Analytics en selecteer **[!UICONTROL Workspace]** in het bovenste menu.
1. Selecteer een bestaand project of maak een project.
1. Creeer de lijst van de a [ Vrije vorm ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md).
1. Sleep de gewenste afmetingen en afmetingen naar het Workspace-canvas voor analyse.

Mogelijke analyses zijn:

* Trend friction event data over time
* Voeg bij een fallout- of trechter-visualisatie Customer Journey Analytics-gebeurtenissen toe als een paar stappen en Quantum Metric friction-gebeurtenissen. Met dit rapport kunt u zien waar bezoekers meestal in de problemen komen.
* Een segment maken en toepassen voor bezoekers die wrijvingsgebeurtenissen ervaren voor een diepgaande analyse
