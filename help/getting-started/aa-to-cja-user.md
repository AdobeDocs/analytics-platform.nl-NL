---
title: CJA-gebruikershandleiding voor Adobe Analytics-gebruikers
description: Wat vanuit het perspectief van de gebruiker te overwegen wanneer uw bedrijf gegevens van Adobe Analytics aan Customer Journey Analytics verplaatst
role: User
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: eeb56599c81dd9cd20bf91c864aa57a783ef13fd
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# CJA-gebruikershandleiding voor Adobe Analytics-gebruikers

Gefeliciteerd, uw bedrijf heeft minstens een deel van zijn gegevens naar Customer Journey Analytics verplaatst! Wanneer u met Customer Journey Analytics begint te werken, zult u grote verschillen en enkele gelijkenissen zien. Deze pagina is bedoeld om de dingen uit te leggen die niet zijn gewijzigd, en ook een aantal van de grote verschillen.

Wij zullen u ook vertellen hoe u meer informatie over nieuwe concepten kunt krijgen, en verdere stappen om UW klantenreis gemakkelijker en succesvoller te maken.

## Wat niet is gewijzigd

Veel van wat u op de verslaggevende kant kent, is niet veranderd. U kunt nog steeds gebruikmaken van de kracht van Analysis Workspace om uw gegevens te analyseren, plus Adobe Analytics-dashboards en een nieuwe versie van Report Builder. Werkruimte en dashboards werken in wezen hetzelfde als in traditionele Adobe Analytics. Report Builder heeft een nieuwe interface en loopt nu op PCs, de computers van Mac, en de Webversie van Excel. Meldend-wijs, wat verschillend is is dat u toegang tot veel meer dwars-kanaalgegevens hebt om te analyseren. Hier volgt een voorbeeld van een werkruimte

## Nieuwe architectuur

Op het gebied van architectuur krijgt Customer Journey Analytics gegevens van Adobe Experience Platform. Met Experience Platform kunt u klantgegevens en inhoud van elk systeem of kanaal centraliseren en standaardiseren. Bovendien kunt u door middel van het leren van gegevens en computers het ontwerp en de levering van persoonlijke ervaringen verbeteren.

De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Zie voor meer informatie over het platform [Overzicht van Adobe Experience Platform-architectuur](https://experienceleague.adobe.com/docs/platform-learn/tutorials/intro-to-platform/basic-architecture.html?lang=en).

Uw CJA Admin zal verbindingen aan de gegevens in Platform vestigen, en bouwt gegevensmeningen binnen die verbindingen. Beschouw gegevensweergaven als vergelijkbaar met virtuele rapportsuites. Gegevensweergaven vormen de basis voor rapportage in Customer Journey Analytics.

## Nieuwe concepten en terminologie

Verschillende functies in CJA zijn in vergelijking met traditionele Adobe Analytics hernoemd en opnieuw ontworpen om aan de industrienormen te voldoen. Sommige bijgewerkte terminologie omvat segmenten, virtuele rapportsuites, classificaties, klantenattributen, en containernamen. Vertrouwde concepten zoals eVars en props bestaan niet meer, samen met de beperkingen die ze opleggen.

### Segmenten zijn nu &#39;filters&#39;


### Virtuele rapportsets zijn nu &#39;gegevensweergaven&#39;


### Classificaties zijn nu &#39;Gegevensbestanden opzoeken&#39;

### Klantkenmerken zijn nu &#39;Profielgegevenssets&#39;


### Handcontainers zijn nu &#39;Event&#39;-containers

### Bezoek containers zijn nu &#39;Sessie&#39;-containers

### Bezoekerscontainers zijn nu &#39;Person&#39;-containers

## Veelgestelde vragen over Adobe Analytics-componenten

| Vraag | Antwoord |
| --- | --- |
| Kan ik delen/publiceren [!UICONTROL filters] ([!UICONTROL segments]) van [!DNL Customer Journey Analytics] aan Experience Platform Verenigd Profiel, of andere toepassingen van Experience Cloud? | Nog niet, maar we werken actief aan het leveren van deze capaciteit. |
| Wat is er gebeurd met mijn oude [!UICONTROL eVar] instellen? | [!UICONTROL eVars], [!UICONTROL props], en [!UICONTROL events] in de traditionele Adobe Analytics-zin niet meer bestaan in [!UICONTROL Customer Journey Analytics]. U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd. |
| Waar zijn al mijn zitting en veranderlijke persistentie montages nu? | [!UICONTROL Customer Journey Analytics] Hiermee past u al deze instellingen toe tijdens de rapporttijd. Deze instellingen worden nu live weergegeven in de gegevensweergave. De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken! |
| Wat gebeurt er met onze bestaande segmenten/berekende maatstaven? | [!UICONTROL Customer Journey Analytics] gebruikt niet langer eVars, props of gebeurtenissen en gebruikt in plaats daarvan een AEP-schema. Dit betekent dat geen van de bestaande segmenten of statistische gegevens compatibel zijn met [!UICONTROL Customer Journey Analytics]. |
| Hoe werkt [!UICONTROL Customer Journey Analytics] handgreep `Uniques Exceeded` beperkingen? | [!UICONTROL Customer Journey Analytics] heeft geen unieke waardebeperkingen, dus hoeft u zich daar geen zorgen over te maken! |
| Als ik een bestaande [!DNL Data Workbench] klant, kan ik naar [!UICONTROL Customer Journey Analytics] nu? | Het hangt af van uw gebruikscase. Werk met uw Adobe-accountteam. Je huidige gebruikscase is mogelijk al geschikt voor Customer Journey Analytics! |
