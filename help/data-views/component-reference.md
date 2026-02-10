---
title: Standaardcomponentverwijzing
description: Meer informatie over details en informatie over alle standaardcomponenten die u kunt toevoegen aan elke gegevensweergave.
exl-id: e23ce27a-77ab-4641-a126-93f00d4e6e14
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: 4f1299595077a1756a6ad0c4f5ef5e0247ab4973
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 1%

---

# Standaardcomponentverwijzing

De meeste dimensies en metriek in Customer Journey Analytics zijn gebaseerd op schema-elementen uit uw dataset van Adobe Experience Platform. Er zijn echter verschillende componenten beschikbaar om aan een gegevensweergave toe te voegen, ongeacht de verbinding die u gebruikt.

[!UICONTROL Standard components] zijn componenten die niet uit de gebieden van het datasetschema worden geproduceerd maar in plaats daarvan systeem geproduceerd. Sommige systeemonderdelen zijn vereist om de rapportagemogelijkheden in Analysis Workspace te vergemakkelijken, terwijl andere systeemonderdelen optioneel zijn.

![ Standaardcomponenten ](assets/dataview-standard-components.png)

## Vereiste standaardonderdelen {#required}

Deze vereiste standaardcomponenten worden standaard toegevoegd aan elke gegevensweergave. Ze zijn essentieel voor de rapportagemogelijkheden die Customer Journey Analytics biedt.

### Standaardafmetingen

{{standard-dimensions}}


### Standaardwaarden

{{standard-metrics}}


## Optionele standaardonderdelen {#optional}

Optionele standaardcomponenten zijn beschikbaar via **[!UICONTROL Data views]** > **[!UICONTROL Edit data view]** > **[!UICONTROL Components]** tab > **[!UICONTROL Standard Components]** tab.

| Componentnaam | Dimension of Metric | Notities en waarden |
| --- | --- | --- |
| [!UICONTROL AM/PM] | Afmeting van tijd-paring | AM of PM |
| [!UICONTROL Batch ID] | Dimension | Id voor de Experience Platform-batch waarvan een [!UICONTROL Event] deel uitmaakte. |
| [!UICONTROL Dataset ID] | Dimension | Identifier voor de Experience Platform-gegevensset waarvan een [!UICONTROL Event] deel uitmaakte. |
| [!UICONTROL Day of Month] | Afmeting van tijd-paring | 1-31 |
| [!UICONTROL Day of Week] | Afmeting van tijd-paring | Maandag, dinsdag, woensdag, donderdag, vrijdag, zaterdag, zondag |
| [!UICONTROL Day of Year] | Afmeting van tijd-paring | 1-366 |
| [!UICONTROL Hour of Day] | Afmeting van tijd-paring | 0-23 |
| [!UICONTROL  Month of Year] | Afmeting van tijd-paring | Januari - december |
| [!UICONTROL First-time Sessions] | Metrisch | De eerste sessie van een persoon is gedefinieerd in het rapportagevenster. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views-usecases.html#new-repeat) |
| [!UICONTROL Return Sessions] | Metrisch | Het aantal sessies dat niet de eerste sessie van een persoon was. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views-usecases.html#new-repeat) |
| [!UICONTROL Person ID] | Dimension | Voor elk gegevenssetschema dat in de Experience Platform is gedefinieerd, kan een eigen set met een of meer identiteiten zijn gedefinieerd en gekoppeld aan een naamruimte. Elk van deze identiteiten kan worden gebruikt als de persoon-id. Voorbeelden zijn Cookie-id, Stitched ID, Gebruikersnaam, Trackingcode enzovoort. De [!UICONTROL Person ID] -dimensie is de basis voor het combineren van gegevenssets en het identificeren van unieke personen in Customer Journey Analytics.<p>Mogelijke gebruiksgevallen zijn:<ul><li>Creeer een segment op een specifieke waarde van identiteitskaart van de persoon om alles neer aan het gedrag van die gebruiker te segmenteren.</li><li>Foutopsporing: zorg dat de gegevens voor een specifieke cookie-id (of een specifieke klant-id) aanwezig zijn.</li><li>Het identificeren van de gebruikers die binnen aan een vraagcentrum riepen.</li></ul> |
| [!UICONTROL Person ID namespace] | Dimension | Welk type id de [!UICONTROL Person ID] bevat. Voorbeelden zijn: `email address` , `cookie ID` , `Analytics ID` |
| [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/>[!UICONTROL Global Account ID] | Dimension | De lus [!UICONTROL Global Account ID] wanneer u de globale-accountcontainer in uw verbinding gebruikt. |
| [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/>[!UICONTROL Account ID] | Dimension | De lus [!UICONTROL Account ID] wanneer u de container Account in uw verbinding gebruikt. |
| [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/>[!UICONTROL Opportunity ID] | Dimension | De lus [!UICONTROL Opportunity ID] wanneer u de container Opportunity in uw verbinding gebruikt. |
| [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/>[!UICONTROL Buying Group ID] | Dimension | De lus [!UICONTROL Buying Group ID] wanneer u de container voor de koopgroep gebruikt in de verbinding. |
| [!UICONTROL Quarter of Year] | Afmeting van tijd-paring | Q1, Q2, Q3, Q4 |
| [!UICONTROL Repeat session] | Metrisch | Het aantal sessies dat niet de eerste sessie van een persoon was. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views-usecases.html#new-repeat) |
| [!UICONTROL Session Type] | Dimension | Deze dimensie heeft twee waarden: 1. [!UICONTROL First-Time] en 2. Terugsturen. Het [!UICONTROL First-time] lijn punt omvat al gedrag (metriek tegen deze dimensie) van een zitting die als bepaalde eerste zitting van een persoon is bepaald. Alle andere elementen worden opgenomen in het regelitem [!UICONTROL Returning] (ervan uitgaande dat alles tot een sessie behoort). Wanneer metriek geen deel uitmaken van een sessie, vallen ze voor deze dimensie in het emmertje &quot;Niet van toepassing&quot;. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views-usecases.html#new-repeat) |
| [!UICONTROL Time Spent per Event] | Dimension | Sluit de metrische waarde [!UICONTROL Time Spent] in [!UICONTROL Event] emmers. |
| [!UICONTROL Time Spent per Session] | Dimension | Sluit de metrische waarde [!UICONTROL Time Spent] in [!UICONTROL Session] emmers. |
| [!UICONTROL Time Spent per Person] | Dimension | Sluit de metrische waarde [!UICONTROL Time Spent] in [!UICONTROL Person] emmers. |
| [!UICONTROL Weekend]/[!UICONTROL Weekday] | Afmeting van tijd-paring | Weekend of Weekdag |

{style="table-layout:auto"}


>[!MORELIKETHIS]
>
>[ ontdekt de diepere Inzichten van de Klant met de Eigenschap van de Diepte van de Gebeurtenis ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/discover-deeper-customer-insights-with-adobe-customer-journey/ba-p/753947#M576)
>