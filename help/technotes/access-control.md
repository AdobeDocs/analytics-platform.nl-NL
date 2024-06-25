---
title: Toegangsbeheer Customer Journey Analytics
description: Leer over manieren om toegangsbeheer in Customer Journey Analytics uit te voeren.
solution: Customer Journey Analytics
feature: Basics
exl-id: c258fa39-c0b6-45a1-8547-79516c15a215
mini-toc-levels: 3
role: Admin
source-git-commit: 1a470345a6a2748b992263c3ad25e4cd7d3daa9e
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 0%

---

# Toegangsbeheer Customer Journey Analytics

Drie toegangsniveaus of drie rollen bepalen de Customer Journey Analytics: de rol van Admin van het Product, de rol van Admin van het Profiel van het Product, en gebruiker-vlakke toegang. In dit onderwerp worden deze rollen gedetailleerder beschreven.

Bovendien bespreekt dit artikel meer korrelige manieren om toegang, zoals de kromming van de Werkruimte en rij-niveau evenals waarde-vlakke toegangsbeheer te beperken.

## De rol Productbeheerder

De gebruikers die de rol van Admin van het Product worden toegewezen worden gegeven de noodzakelijke toestemmingen om de meeste taken binnen Customer Journey Analytics door gebrek uit te voeren. Voor sommige taken zijn echter aanvullende machtigingen vereist.

Een gebruiker toevoegen als productbeheerder:

1. Ga naar de [Admin Console](https://adminconsole.adobe.com/enterprise/).

1. Selecteren [!UICONTROL **Customer Journey Analytics**] > [!UICONTROL **Admins**] tab > [!UICONTROL **Admin toevoegen**].

   De gebruikers die u hebt toegevoegd, krijgen de [Standaardmachtigingen voor productbeheer](#product-admin-default-permissions). U kunt ze ook verlenen [aanvullende machtigingen](#product-admin-additional-permissions) indien nodig.

### Standaardmachtigingen voor productbeheer

Productbeheerders hebben machtigingen om de meeste taken binnen de Customer Journey Analytics uit te voeren.

Productbeheerders krijgen standaard de benodigde machtigingen om de volgende taken uit te voeren:

* Gegevensweergaven maken, bijwerken en verwijderen
* Werk en schrap projecten, filters, berekende metriek, publiek, annotaties, of filters bij die door andere gebruikers worden gecreeerd
* Werkruimteprojecten delen met alle gebruikers
* Rapportactiviteiten beheren in het dialoogvenster [Activity Manager rapporteren](/help/reporting-activity-manager/reporting-activity-overview.md)
* [Volledige tabellen exporteren](/help/analysis-workspace/export/export-cloud.md) uit Analysis Workspace

### Aanvullende machtigingen voor productbeheer

Naast het toevoegen als productbeheerder in de **Productprofiel Customer Journey Analytics** in de [Admin Console](https://adminconsole.adobe.com/enterprise/), zijn extra toestemmingen vereist om de volgende taken binnen Customer Journey Analytics te voltooien:

* Gegevens maken, bijwerken en verwijderen [Verbindingen](/help/connections/overview.md)

  Om deze taak uit te voeren, moeten de gebruikers deel uitmaken van een **Productprofiel Experience Platform** die de volgende machtigingen biedt:
   * Gegevensmodellering: Schema&#39;s weergeven, Schema&#39;s beheren
   * gegevensbeheer: gegevenssets weergeven, gegevenssets beheren
   * Gegevensinname: Bronnen beheren
   * Identiteitsnaamruimten weergeven

     Zie voor meer informatie over machtigingen voor Experience Platforms [Toegangsbeheer in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

* Gegevenssets exporteren naar cloud [Doelen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html)

  Om deze taak uit te voeren, hebben de gebruikers de volgende toestemmingen van het Experience Platform nodig:

   * Doelen beheren
   * Doelen activeren

     Voor meer informatie over de toestemmingen van de Doelen van het Experience Platform, zie [Overzicht van doelen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home).

* Gebruik de [BI-extensie](../data-views/bi-extension.md)

  Voor gebruikers om de extensie BI te gebruiken, voert u een productbeheerder

   * moet ervoor zorgen dat de Experience Platform toestemmingen voor de gebruiker een rol omvatten die het middel van de Dienst van de Vraag met de Manage Opties heeft van de Vragen en van de Dienst van de Vraag beheren de opties van de Integratie van de Vraag. Zie [Rechten voor een productprofiel beheren](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/permissions).
   * moet de juiste machtigingen voor de Customer Journey Analytics voor de gebruiker garanderen:
      * toestemming voor toegang tot de relevante gegevensweergaven. Zie Gegevens weergeven in [Machtigingen Customer Journey Analytics in Admin Console](#customer-journey-analytics-permissions-in-admin-console).
      * toestemming om toegang te krijgen tot de extensie CJA BI. Zie Gereedschappen voor gegevensweergave in [Machtigingen Customer Journey Analytics in Admin Console](#customer-journey-analytics-permissions-in-admin-console).

## Beheerdersrol productprofiel

Een productprofiel is een set machtigingen. Beheerders van productprofielen kunnen

* Maak en beheer afzonderlijke productprofielen. Bijvoorbeeld nieuwe gebruikers toevoegen of gebruikersgroepen en de bijbehorende productprofielen beheren.

* In Customer Journey Analytics, geef gegevensmeningen uit die deel van een productprofiel uitmaken dat zij beheren. Ze kunnen geen nieuwe gegevensweergaven maken.

## Toegang op gebruikersniveau

In de onderstaande matrix worden de belangrijkste toegangsmachtigingen voor verschillende Customer Journey Analytics-mogelijkheden voor niet-productbeheerders en Customer Journey Analytics-productbeheerders beschreven. Als u deze machtigingen begrijpt, kunnen gebruikers effectief navigeren en Customer Journey Analytics gebruiken op basis van hun rol en verantwoordelijkheden binnen de organisatie.

| Productfunctionaliteit | Niet-productbeheerders (gebruikers) | Productbeheerders |
| --- | --- | --- |
| **Gegevensweergaven** | Kan niet weergeven/bijwerken/maken/verwijderen | Kan maken/bijwerken/verwijderen |
| **Verbindingen** | Kan niet weergeven/bijwerken/maken/verwijderen | Kan maken/bijwerken/verwijderen |
| **Filters** | Kan maken | Kan maken |
| **Projecten** | Kan maken | Kan maken/bijwerken/verwijderen |
| **Soorten publiek** | Kan maken met speciale machtigingen in Admin Console | Kan maken |
| **Berekende standaarden** | Kan maken met speciale machtigingen in Admin Console | Kan maken |

{style="table-layout:auto"}

## Workspace-projectcursus

Een ander niveau van toegangsbeheer kan op het de rapportniveau van de Werkruimte worden gebruikt. U kunt de toegang tot specifieke componenten voor bepaalde gebruikers beperken. Voor meer informatie over hoe te om componenten (afmetingen, metriek, filters, datumwaaiers) op het het projectniveau van de Werkruimte te beperken, en hoe de kromming aan gegevensmeningen gebonden is, zie [Cursieve projecten](/help/analysis-workspace/curate-share/curate.md).

## Toegang verlenen tot individuele metriek of dimensies

U kunt geen toestemmingen voor individuele metriek of dimensies in Customer Journey Analytics verlenen of ontkennen zoals u in traditionele Adobe Analytics kunt. Metriek en afmetingen kunnen worden gewijzigd in [gegevensweergaven](/help/data-views/data-views.md) en zijn derhalve onderhevig aan wijziging van de Customer Journey Analytics. Als u ze wijzigt, wordt de rapportage ook met terugwerkende kracht gewijzigd.

## Gebruik hoofdletters

Hier zijn een paar gebruiksgevallen die illustreren hoe de toegangscontrole in real-life scenario&#39;s kan worden gebruikt.

### Toegang van derden

Een derde waarmee uw bedrijf samenwerkt, heeft een teamlead waarmee u productprofielbeheer kunt maken. Deze beheerder kan gebruikers van het team van het bedrijf aan dit productprofiel toevoegen. Deze beheerder kan toegang geven tot specifieke gegevensweergaven en andere gebruikers toevoegen aan dit productprofiel. Zij kunnen die gegevensmeningen ook wijzigen waarover zij controle hebben om de behoeften van hun team te passen.

### Toegangsbeheer op rijniveau

Laten we zeggen dat u gebruikers slechts vanaf één dag toegang wilt geven tot gegevens. Hieronder wordt beschreven hoe u de toegang tot die specifieke rijen beperkt:

1. Een filter maken in de Customer Journey Analytics waar **[!UICONTROL Day]** is gelijk aan de datum u hen gegevenstoegang tot wilt hebben.
1. In [!UICONTROL Data views] > [!UICONTROL Settings], voegt u dat filter toe aan de gegevensweergave.
1. Sla de gegevensweergave op en past het filter automatisch toe op de gegevensset. Alle rijen die niet in de filterdefinitie passen, worden nu automatisch uitgesloten van de bewerkte gegevensweergave.
1. Maak een nieuw productprofiel in de Admin Console, voeg er gebruikers aan toe en beperk de toegang tot deze gegevensweergave.

### Toegangsbeheer op waardeniveau

Gebruikers die toegang hebben tot een gegevensweergave, kunnen alleen werken met de cijfers en afmetingen die de beheerder in deze gegevensweergave heeft opgenomen. Beheerders kunnen de opdracht [Functionaliteit opnemen/uitsluiten](/help/data-views/component-settings/include-exclude-values.md) in gegevensweergaven waarin u bijvoorbeeld bepaalde waarden van dimensies wilt uitsluiten van een gegevensweergave.

Hier is een voorbeeld dat betrekking heeft op de gezondheidszorg: Laten we zeggen dat u een metrische waarde maakt die &#39;Hypertensie&#39; wordt genoemd in een gegevensweergave, op basis van een dataset die deze gegevens bevat. Het feit dat het een metrische waarde is, zou je in staat stellen de totale waarde van deze metrische waarde te zien, maar niet de individuele patiënten die eronder vallen.

## Machtigingen Customer Journey Analytics in Admin Console

De **[!UICONTROL Permissions]** is onderdeel van elk productprofiel in [Admin Console](https://adminconsole.adobe.com/enterprise/). U kunt gebruikers toevoegen aan specifieke productprofielen. Vervolgens wijst u rechten toe aan specifieke gegevensweergaven en geeft u op welke machtigingen de gebruikers in een productprofiel hebben. Hier zijn de Customer Journey Analytics-specifieke toestemmingen:

![beheerdersrechten](assets/permissions.png)

| Machtiging | Definitie |
| --- | --- |
| **[!UICONTROL Data Views]** | Als u schakelt **[!UICONTROL Auto-Include]** tot **[!UICONTROL On]** Gebruikers die deel uitmaken van dit productprofiel, kunnen alle bestaande en nieuwe gegevensweergaven bekijken. Als deze instelling is ingesteld op **[!UICONTROL Off]**, kunt u specifieke gegevensweergaven selecteren waartoe gebruikers toegang hebben. |
| **[!UICONTROL Reporting Tools]**: |   |
| **[!UICONTROL Audit Logs Access]** | Deze toestemming dwingt de toestemmingscontrole op [API](https://www.adobe.io/cja-apis/docs/endpoints/auditlogs/) en de gebruikersinterface voor auditlogbestanden. |
| **[!UICONTROL Analysis Workspace Access]** | Laat gebruikers Analysis Workspace openen in Customer Journey Analytics. |
| [!UICONTROL **Toegang tot geleide analyse**] | Gebruikers laten maken [Projecten met geleide analyse](/help/guided-analysis/overview.md). |
| [!UICONTROL **Voorspelling**] | Gebruikers toegang geven tot de functie voor prognoses in Analysis Workspace |
| **[!UICONTROL Reporting Usage Admin]** | Laat gebruikers om het even welk rapport bekijken en schrappen dat in hun bedrijf loopt. |
| **[!UICONTROL Reporting Usage View]** | Laat gebruikers alle gelijktijdige rapportageaanvragen zien. |
| [!UICONTROL **Volledige tabelexport**] | Gebruikers toestaan [volledige tabellen exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md). |
| **[!UICONTROL Calculated Metrics Creation]** | Gebruikers laten maken [berekende meetwaarden](/help/components/calc-metrics/calc-metr-overview.md). |
| **[!UICONTROL Filter Creation]** | Gebruikers laten maken [filters](/help/components/filters/filters-overview.md). |
| **[!UICONTROL Labs Access]** | Gebruikers toegang geven tot de [Labs](/help/labs/labs.md) in Customer Journey Analytics. |
| **[!UICONTROL Annotation Creation]** | Gebruikers laten maken [annotaties](/help/components/annotations/overview.md). |
| **[!UICONTROL Audience Creation]** | Gebruikers laten maken [publiek](/help/components/audiences/audiences-overview.md). |
| **[!UICONTROL Audience View]** | Gebruikers weergeven [publiek](/help/components/audiences/audiences-overview.md). |
| [!UICONTROL **Projectkoppelingen delen met iedereen**] | Gebruikers toestaan [delen projecten met iedereen.](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/curate-share/share-projects) |
| **[!UICONTROL Data View Tools]**: |   |
| [!UICONTROL **Volledige tabelexport**] | Gebruikers toestaan [volledige tabellen exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md). |
| **[!UICONTROL [!UICONTROL CJA BI Extension]]** | Gebruikers de opdracht [BI-extensie](../data-views/bi-extension.md). |

{style="table-layout:auto"}
