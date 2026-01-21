---
title: Customer Journey Analytics Access Control
description: Leer hoe u toegangsbeheer in Customer Journey Analytics kunt implementeren.
solution: Customer Journey Analytics
feature: Basics
exl-id: c258fa39-c0b6-45a1-8547-79516c15a215
mini-toc-levels: 3
role: Admin
source-git-commit: ea699bcacd985d9da1e3895f7770290dc77da537
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Toegangsbeheer

Customer Journey Analytics heeft drie toegangsniveaus of drie rollen: de rol van de productbeheerder, de beheerderrol van het productprofiel en de toegang op gebruikersniveau. In dit onderwerp worden deze rollen gedetailleerder beschreven.

Bovendien bespreekt dit artikel meer korrelige manieren om toegang, zoals de kromming van Workspace en rij-niveau evenals waarde-vlakke toegangsbeheer te beperken.

## Op rollen gebaseerd toegangsbeheer

De volgende op rol-gebaseerde toegangsbeheerniveaus zijn beschikbaar.

### De rol van productbeheerder

Gebruikers aan wie de rol van productbeheerder is toegewezen, krijgen de benodigde machtigingen om de meeste taken standaard in Customer Journey Analytics uit te voeren. Voor sommige taken zijn echter aanvullende machtigingen vereist.

Een gebruiker toevoegen als productbeheerder:

1. Ga naar [&#x200B; Admin Console &#x200B;](https://adminconsole.adobe.com/enterprise/).

1. Selecteer [!UICONTROL **Customer Journey Analytics**] > [!UICONTROL **Admins**] lusje > [!UICONTROL **Admin**] toevoegen.

   De gebruikers die u toevoegde worden gegeven de [&#x200B; beheerder standaardtoestemmingen van het Product &#x200B;](#product-admin-default-permissions). U kunt hen [&#x200B; extra toestemmingen &#x200B;](#product-admin-additional-permissions) ook verlenen indien nodig.

#### Standaardrechten voor productbeheerders

Productbeheerders hebben de rechten om de meeste taken binnen Customer Journey Analytics uit te voeren.

Productbeheerders krijgen standaard de benodigde machtigingen om de volgende taken uit te voeren:

* Werk en schrap projecten, segmenten, berekende metriek, publiek, annotaties, of segmenten bij die door andere gebruikers worden gecreeerd
* Workspace-projecten delen met alle gebruikers
* Beheer rapporteringsactiviteit in de [&#x200B; Rapporterende Manager van de Activiteit &#x200B;](/help/reporting-activity-manager/reporting-activity-overview.md)
* [&#x200B; de Uitvoer volledige lijsten &#x200B;](/help/analysis-workspace/export/export-cloud.md) van Analysis Workspace

#### Aanvullende machtigingen voor productbeheerder

Naast het zijn toegevoegd als productbeheerder in het **Customer Journey Analytics Product Profile** in de [Admin Console](https://adminconsole.adobe.com/enterprise/), zijn extra rechten vereist om de volgende taken binnen Customer Journey Analytics uit te voeren:

* Creeer, werk, en schrap [&#x200B; gegevensmeningen &#x200B;](/help/data-views/data-views.md) bij.
* Creeer, werk, en schrap [&#x200B; verbindingen &#x200B;](/help/connections/overview.md) bij

  Om deze taak uit te voeren, moeten de gebruikers deel uitmaken van een **Profiel van het Product van Experience Platform** dat de volgende toestemmingen verstrekt:

  | Categorie | Machtiging | Beschrijving |
  |---|---|---|
  | [!UICONTROL Sandboxes] | [!UICONTROL At least one] | Toegang tot relevante sandboxes voor verbindingen. |
  | [!UICONTROL Data Modeling] | [!UICONTROL View Schemas] | Alleen-lezen toegang tot schema&#39;s en gerelateerde bronnen. |
  | [!UICONTROL Data Modeling] | [!UICONTROL Manage Schemas] | Toegang om schema&#39;s en gerelateerde bronnen te lezen, aanmaken, bewerken en verwijderen. |
  | [!UICONTROL Data Management] | [!UICONTROL View Datasets] | Alleen-lezen toegang voor datasets en schema&#39;s. |
  | [!UICONTROL Identity Management] | [!UICONTROL View Identity Namespaces] | Alleen-lezen toegang voor naamruimten. |

  Voor meer informatie over de toestemmingen van Experience Platform, zie [&#x200B; toestemmingen voor een productprofiel &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/ui/permissions) beheren.


* Als Journey Optimizer is geïntegreerd met Customer Journey Analytics waar Journey Optimizer Connections bestaat, moeten ook de rechten voor reizen worden toegevoegd aan de toegangsverbindingen:

  | Categorie | Machtiging | Beschrijving |
  |---|---|---|
  | [!UICONTROL Journeys] | [!UICONTROL View Journeys Events, Data Sources and Actions] | Alleen-lezen toegang tot reisgebeurtenissen, aangepaste acties voor reizen en gegevensbronnen voor reizen. |
  | [!UICONTROL Journeys] | [!UICONTROL Manage Journeys Events, Data Sources and Actions] | Gebeurtenissen, bronnen of handelingen lezen, maken, bewerken en verwijderen. |
  | [!UICONTROL Journeys] | [!UICONTROL View Journeys] | Alleen-lezen toegang tot reizen. |
  | [!UICONTROL Journeys] | [!UICONTROL Manage Journeys] | Reizen lezen, maken, bewerken en verwijderen. |

* De datasets van de uitvoer aan [&#x200B; bestemmingen &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/destinations/ui/activate/export-datasets)

  Om deze taak uit te voeren, moeten gebruikers deel uitmaken van een **Experience Platform Product Profile** dat de volgende permissies biedt:

  | Categorie | Machtiging | Beschrijving |
  |---|---|---|
  | [!UICONTROL Destinations] | [!UICONTROL Manage Destinations] | Toegang om bestemmingsverbindingen en bestemmingsaccounts te lezen, aan te maken en te verwijderen. |
  | [!UICONTROL Destinations] | [!UICONTROL Activate Destinations] | Sta gebruikers toe om segmenten aan bestaande bestemmingen te activeren. Hiermee schakelt u de toewijzingsstap in de activeringsworkflow in. Deze toestemming vereist ook de toestemming van de Doelen van de Mening die aan de gebruiker moet worden verleend die gegevens aan bestemmingen wil activeren. |

  Voor meer informatie over de toestemmingen van Experience Platform, zie [&#x200B; toestemmingen voor een productprofiel &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/ui/permissions) beheren.

* Gebruik de [&#x200B; uitbreiding van BI &#x200B;](../data-views/bi-extension.md)

  Voor gebruikers om de uitbreiding van BI te gebruiken, een beheerder van het Product

   * moet ervoor zorgen dat de Experience Platform-machtigingen voor de gebruiker een rol bevatten die over de bron Query Service beschikt met de opties Query&#39;s beheren en Query Service Integration beheren. Voor meer informatie over de toestemmingen van Experience Platform, zie [&#x200B; toestemmingen voor een productprofiel &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/ui/permissions) beheren.

     | Categorie | Machtiging | Beschrijving |
     |---|---|---|
     | [!UICONTROL Query Service] | [!UICONTROL Manage Queries] | Toegang tot het lezen, creëren, uitgeven, en schrappen van gestructureerde SQL vragen voor de gegevens van het Platform. |
     | [!UICONTROL Query Service] | [!UICONTROL Manage Query Service Integration] | Toegang tot het creëren, bijwerken, en schrappen van niet-vervallende geloofsbrieven voor de toegang van de Dienst van de Vraag. |

   * moet de juiste Customer Journey Analytics-machtigingen voor de gebruiker garanderen:
      * toestemming voor toegang tot de relevante gegevensweergaven. Zie [!UICONTROL Data Views] in [&#x200B; gebruiker-vlakke toegang &#x200B;](#user-level-access).
      * toestemming voor toegang tot de extensie Customer Journey Analytics BI. Zie [!UICONTROL Data View Tools] in [&#x200B; gebruiker-vlakke toegang &#x200B;](#user-level-access).

### Beheerdersrol voor productprofiel

Een productprofiel is een set machtigingen. Productbeheerders maken productprofielen en kunnen beheerders van productprofielen toewijzen om een of meer productprofielen te beheren. Een beheerder van het productprofiel kan dan:

* De toegewezen productprofielen beheren. U kunt bijvoorbeeld gebruikers of gebruikersgroepen toevoegen of verwijderen en de machtigingen voor de productprofielen wijzigen.

* In Customer Journey Analytics kunt u gegevensweergaven bewerken die deel uitmaken van een toegewezen productprofiel. Beheerders van productprofielen kunnen geen nieuwe gegevensweergaven maken.

### Toegang op gebruikersniveau

In de onderstaande tabel staan de belangrijkste toegangsmachtigingen voor verschillende Customer Journey Analytics-mogelijkheden die u voor relevante gebruikers kunt configureren. U kunt verschillende niveaus van gebruikerstoegang door productprofielen beheren. Een productprofiel combineert een aantal machtigingen die u vervolgens kunt toewijzen aan individuele gebruikers of gebruikersgroepen.

Het **[!UICONTROL Permissions]** tabblad maakt deel uit van elk productprofiel in de [Admin Console](https://adminconsole.adobe.com/enterprise/).

![Beheerdersconsolerechten](assets/permissions.png)

| Categorie | Machtiging | Beschrijving |
| --- | --- | ---|
| [!UICONTROL Data Views] | *naam van de gegevensmening* | Als u **[!UICONTROL Auto-Include]** instelt op **[!UICONTROL On]** , kunnen gebruikers die deel uitmaken van dit productprofiel alle bestaande en nieuwe gegevensweergaven bekijken. Als deze instelling is ingesteld op **[!UICONTROL Off]** , kunt u specifieke gegevensweergaven selecteren waartoe gebruikers toegang hebben. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Analysis Workspace Access] | Laat gebruikers tot [&#x200B; Analysis Workspace &#x200B;](/help/analysis-workspace/home.md) toegang hebben. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Guided Analysis Access] | Laat gebruikers tot [&#x200B; Geleide Analyse &#x200B;](/help/guided-analysis/overview.md) toegang hebben. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Calculated Metrics Creation] | Laat gebruikers [&#x200B; berekende metriek &#x200B;](/help/components/calc-metrics/calc-metr-overview.md) creëren. Gebruikers kunnen alleen de berekende meetgegevens die zij maken of de berekende meetgegevens die met hen worden gedeeld, labelen, delen, verwijderen, hernoemen, goedkeuren of goedkeuren. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Segment Creation] | Laat gebruikers [&#x200B; segmenten &#x200B;](/help/components/segments/seg-overview.md) tot stand brengen. Gebruikers kunnen alleen de segmenten die zij maken of de segmenten die met hen worden gedeeld, labelen, delen, verwijderen, hernoemen, goedkeuren of niet goedkeuren. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Labs Access] | Laat gebruikers tot het [&#x200B; lusje van Laboratoria &#x200B;](/help/labs/labs.md) in Customer Journey Analytics toegang hebben. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Annotation Creation] | Laat gebruikers [&#x200B; annotaties &#x200B;](/help/components/annotations/overview.md) tot stand brengen. Gebruikers kunnen alleen de annotaties die zij maken of gedeeld met hen delen, taggen, delen en hernoemen. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Audience View] | Laat gebruikers [&#x200B; publiek &#x200B;](/help/components/audiences/audiences-overview.md) bekijken. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Audience Creation] | Laat gebruikers [&#x200B; publiek &#x200B;](/help/components/audiences/audiences-overview.md) tot stand brengen. Vereist [&#x200B; beheert Segmenten &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/home) in Adobe Experience Platform. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Data storytelling] | Laat gebruikers [diapresentaties genereren op basis van Workspace-projecten.](/help/analysis-workspace/curate-share/generate-slides.md)<p>Data storytelling bevindt zich in de Limited Testing-fase van release en is mogelijk nog niet beschikbaar in jouw omgeving. Deze opmerking wordt verwijderd zodra de functionaliteit algemeen beschikbaar is. Voor informatie over het releaseproces van Customer Journey Analytics, zie [Customer Journey Analytics feature releases](/help/release-notes/releases.md).</p> |
| [!UICONTROL Reporting Tools] | [!UICONTROL Audit Logs Access] | Dwing de toestemmingscontrole op [&#x200B; API &#x200B;](https://developer.adobe.com/cja-apis/docs/endpoints/auditlogs/) en de controlelogboeken UI af. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Share Project Links With Anyone] | Laat gebruikers [&#x200B; projecten met iedereen delen.](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/curate-share/share-projects) |
| [!UICONTROL Reporting Tools] | [!UICONTROL Forecasting] | Laat gebruikers tot de [&#x200B; Voorspelling &#x200B;](../analysis-workspace/c-forecast/forecasting.md) eigenschap in Analysis Workspace toegang hebben |
| [!UICONTROL Reporting Tools] | [!UICONTROL AI Assistant: Product Knowledge] | Laat gebruikers tot de [&#x200B; Medewerker AI &#x200B;](../ai-assistant.md) voor productkennis toegang hebben. |
| [!UICONTROL Reporting Tools] | [!UICONTROL Intelligent Captions] | Laat gebruikers tot [&#x200B; Intelligente titels &#x200B;](/help/analysis-workspace/visualizations/intelligent-captions.md) toegang hebben. |
| [!UICONTROL Data View Tools] | [!UICONTROL Full Table Export] | Laat gebruikers [&#x200B; volledige lijsten naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md) uitvoeren. |
| [!UICONTROL Data View Tools] | [!UICONTROL CJA BI Extension] | Laat gebruikers de [&#x200B; uitbreiding van BI &#x200B;](../data-views/bi-extension.md) gebruiken. |

{style="table-layout:auto"}

## Workspace project curation

Een ander niveau van toegangscontrole kan op het Workspace rapporteringsniveau worden gebruikt. U kunt de toegang tot specifieke componenten voor bepaalde gebruikers beperken. Voor meer informatie over hoe te om componenten (afmetingen, metriek, segmenten, datumwaaiers) op het het projectniveau van Workspace te beperken, en hoe de besnoeiing aan gegevensmeningen gebonden is, zie [&#x200B; projecten van de Kromme &#x200B;](/help/analysis-workspace/curate-share/curate.md).

## Verleen toegang tot individuele metrics of dimensies

Je kunt geen toestemming geven of weigeren voor individuele metrics of dimensies in Customer Journey Analytics zoals in traditionele Adobe Analytics. Statistieken en afmetingen kunnen worden aangepast in [dataweergaven](/help/data-views/data-views.md) en zijn daardoor onderhevig aan verandering in Customer Journey Analytics. Het wijzigen ervan verandert ook achteraf de rapportage.

## Gebruikssituaties

Hier zijn een paar gebruikssituaties die illustreren hoe toegangscontrole in echte situaties kan worden toegepast.

### Toegang van derden

U kunt het beleid van het Profiel van het Product toegang tot een teamlood van een derde verstrekken die uw bedrijf werkt. Deze beheerder kan gebruikers van het team van het bedrijf aan dit productprofiel toevoegen. Deze systeembeheerder van het Productprofiel kan toegang tot specifieke gegevensmeningen geven en andere gebruikers binnen de derde aan dit productprofiel toevoegen. De beheerder van het Profiel van het Product kan gegevensmeningen wijzigen om de vereisten van het derde team te passen.

### Toegangsbeheer op rijniveau

U wilt gebruikers slechts vanaf één dag toegang geven tot gegevens. Hieronder wordt beschreven hoe u de toegang tot die specifieke rijen beperkt:

1. Maak een segment in [!UICONTROL Settings] van een specifieke gegevensweergave, waar [!UICONTROL Day] gelijk is aan de datum waarop de gegevens toegankelijk moeten zijn. Zie [&#x200B; gegevensmening &#x200B;](/help/data-views/create-dataview.md#settings-filters) voor meer informatie creëren.
1. Sparen de gegevensmening, die het segment op het gegevensdeel van de datasets in de onderliggende verbinding toepast. Om het even welke rijen die niet de segmentdefinitie passen worden automatisch uitgesloten van de gegevensmening en niet beschikbaar aan Analysis Workspace wanneer het gebruiken van deze gegevensmening.
1. Creeer een nieuw [&#x200B; profiel van het Product &#x200B;](#product-profile-admin-role) in Admin Console, voeg gebruikers aan het productprofiel toe, en omvat slechts deze specifieke gegevensmening aan het productprofiel.

### Toegangsbeheer op waardeniveau

Gebruikers die toegang hebben tot een gegevensweergave, kunnen alleen werken met de afmetingen en metriek die de beheerder in deze gegevensweergave heeft opgenomen. De beheerders kunnen [&#x200B; gebruiken omvatten/uitsluiten functionaliteit &#x200B;](/help/data-views/component-settings/include-exclude-values.md) of [&#x200B; het knippen van de Waarde &#x200B;](../data-views/component-settings/value-bucketing.md) componentenmontages in een gegevensmening om bepaalde afmetingswaarden van een gegevensmening uit te sluiten of samen te voegen.

Bijvoorbeeld: U creeert metrisch genoemd *Hypertensie* in een gegevensmening van een component die individuele patiëntgegevens van de dataset bevat. U gebruikt waarde het knippen om slechts toegang tot ingesloten waarden te verlenen, zodat zien de gebruikers van de gegevens de individuele patiëntgegevens niet.
