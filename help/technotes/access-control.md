---
title: Toegangsbeheer Customer Journey Analytics
description: Leer over manieren om toegangsbeheer in Customer Journey Analytics uit te voeren.
solution: Customer Journey Analytics
feature: Basics
exl-id: c258fa39-c0b6-45a1-8547-79516c15a215
mini-toc-levels: 3
role: Admin
source-git-commit: 39e4c17336d3648cbf20cace535668d14510186f
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 0%

---

# Toegangsbeheer Customer Journey Analytics

Customer Journey Analytics wordt bepaald door drie toegangsniveaus of drie rollen: de rol van Admin van het Product, de rol van Admin van het Profiel van het Product, en gebruiker-vlakke toegang. In dit onderwerp worden deze rollen gedetailleerder beschreven.

Bovendien bespreken wij meer korrelige manieren om toegang, zoals de kromming van de Werkruimte en rij-niveau evenals waarde-vlakke toegangsbeheer te beperken.

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

Naast het toevoegen als productbeheerder in de **Productprofiel Customer Journey Analytics** in de [Admin Console](https://adminconsole.adobe.com/enterprise/), is extra toestemming vereist om de volgende taken binnen Customer Journey Analytics te voltooien:

* Gegevens maken, bijwerken en verwijderen [Verbindingen](/help/connections/overview.md)

  Om deze taak uit te voeren, moeten de gebruikers deel uitmaken van een **Productprofiel Experience Platform** die de volgende machtigingen biedt:
   * Gegevensmodellering: Schema&#39;s weergeven, Schema&#39;s beheren
   * gegevensbeheer: gegevenssets weergeven, gegevenssets beheren
   * Gegevensinname: Bronnen beheren
   * Identiteitsnaamruimten weergeven

     Zie voor meer informatie over machtigingen voor Experience Platforms [Toegangsbeheer in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html).

* Gegevenssets exporteren naar cloud [Doelen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html)

  >[!AVAILABILITY]
  >
  >De mogelijkheid om gegevenssets naar de cloud te exporteren bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het proces van de release van de Customer Journey Analytics raadpleegt u [Release van de Customer Journey Analytics-functie](/help/release-notes/releases.md).

  Om deze taak uit te voeren, hebben de gebruikers ook de volgende toestemmingen van het Experience Platform nodig:
   * Doelen beheren
   * Doelen activeren

     Voor meer informatie over de toestemmingen van de Doelen van het Experience Platform, zie [Overzicht van doelen](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html#access-controls).

## Beheerdersrol productprofiel

Een productprofiel is een set machtigingen. Beheerders van productprofielen kunnen

* Afzonderlijke productprofielen maken en beheren, zoals nieuwe gebruikers toevoegen of gebruikersgroepen en de bijbehorende productprofielen beheren.

* In Customer Journey Analytics, geef gegevensmeningen uit die deel van een productprofiel uitmaken dat zij beheren. Ze kunnen geen nieuwe gegevensweergaven maken.

## Toegang op gebruikersniveau

In de onderstaande matrix worden de belangrijkste toegangsmachtigingen voor verschillende Customer Journey Analytics-mogelijkheden voor niet-productbeheerders en CJA-productbeheerders beschreven. Als u deze machtigingen begrijpt, kunnen gebruikers beter door CJA navigeren en CJA gebruiken op basis van hun rol en verantwoordelijkheden binnen de organisatie.

| CJA-productfunctionaliteit | Niet-productbeheerders (gebruikers) | Productbeheerders |
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

Een derde waarmee uw bedrijf samenwerkt, heeft een teamlead waarmee u productprofielbeheer kunt maken. Deze beheerder kan vervolgens gebruikers in zijn team toevoegen aan dit productprofiel. Deze beheerder kan toegang geven tot specifieke gegevensweergaven en andere gebruikers toevoegen aan dit productprofiel. Zij kunnen die gegevensmeningen ook wijzigen waarover zij controle hebben om de behoeften van hun team te passen.

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
| **[!UICONTROL Audit Logs Access]** | Deze toestemming dwingt de toestemmingscontrole op [API](https://adobe.io/cja-apis/docs/endpoints/auditlogs/) en de gebruikersinterface voor auditlogbestanden. |
| **[!UICONTROL Analysis Workspace Access]** | Gebruikers krijgen toegang tot Analysis Workspace in Customer Journey Analytics. |
| [!UICONTROL **Toegang tot geleide analyse**] | Gebruikers kunnen [Projecten met geleide analyse](/help/guided-analysis/overview.md). |
| [!UICONTROL **Voorspelling**] | Hiermee hebben gebruikers toegang tot de functie voor prognoses in Analysis Workspace |
| **[!UICONTROL Reporting Usage Admin]** | Laat gebruikers om het even welk rapport bekijken en schrappen dat in hun bedrijf loopt. |
| **[!UICONTROL Reporting Usage View]** | Hiermee kunnen gebruikers alle gelijktijdige rapportageaanvragen bekijken. |
| [!UICONTROL **Volledige tabelexport**] | Gebruikers toestaan [volledige tabellen exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md). |
| **[!UICONTROL Calculated Metrics Creation]** | Gebruikers kunnen [berekende meetwaarden](/help/components/calc-metrics/calc-metr-overview.md). |
| **[!UICONTROL Filter Creation]** | Gebruikers kunnen [filters](/help/components/filters/filters-overview.md). |
| **[!UICONTROL Labs Access]** | Hiermee kunnen gebruikers toegang krijgen tot de [Labs](/help/labs/labs.md) in Customer Journey Analytics. |
| **[!UICONTROL Annotation Creation]** | Gebruikers kunnen [annotaties](/help/components/annotations/overview.md). |
| **[!UICONTROL Audience Creation]** | Gebruikers kunnen [publiek](/help/components/audiences/audiences-overview.md). |
| **[!UICONTROL Audience View]** | Hiermee kunnen gebruikers de weergave [publiek](/help/components/audiences/audiences-overview.md). |
| [!UICONTROL **Projectkoppelingen delen met iedereen**] | Gebruikers toestaan [delen projecten met iedereen.](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/share-projects.html#share-public-link) |
| **[!UICONTROL Data View Tools]**: |   |
| [!UICONTROL **Volledige tabelexport**] | Gebruikers toestaan [volledige tabellen exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md). |
| [!UICONTROL **Toegang tot SQL Query Service**] | Gebruikers kunnen toegang krijgen [Query-service in AEP](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl). |

{style="table-layout:auto"}
