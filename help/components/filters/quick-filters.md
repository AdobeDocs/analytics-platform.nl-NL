---
description: Gebruik snelle filters in Analysis Workspace.
title: Snelle filters
feature: Workspace Basics
role: User, Admin
exl-id: 549e5db5-fcdf-43c5-bc43-590144aee309
source-git-commit: 300bc4069b77b62ae13fd5baf2eec5846676fc6e
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 1%

---

# Snelle filters

U kunt snelle filters binnen een project tot stand brengen om de ingewikkeldheid van volledige [de Bouwer van de Filter](/help/components/filters/create-filters.md) te mijden. Snelle filters

* Alleen van toepassing op projecten waarin ze zijn gemaakt (u kunt dit wijzigen).
* Maximaal 3 regels toestaan
* Plaats geen geneste containers of opeenvolgende regels.
* Werken in projecten met meerdere rapportsuites

Voor een vergelijking van wat de snelle filters kunnen doen versus volledig-afgewerkte component-lijst filters, ga [hier](/help/components/filters/filters-overview.md).

>[!IMPORTANT]
> Snelle filters worden momenteel beperkt getest en zijn nog niet algemeen beschikbaar.

## Vereisten

Gebruikers hebben de [!UICONTROL Segment Creation] machtiging in [Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/summary-tables.html?lang=en#analytics-tools) nodig om snelle filters te kunnen maken.

## Snelle filters maken

Klik in een tabel voor vrije vorm op het pictogram filter+ in de koptekst van het deelvenster:

![](assets/quick-seg1.png)

| Instelling | Beschrijving |
| --- | --- |
| Naam | De standaardnaam van een filter is een combinatie van de regelnamen in het filter. U kunt de naam van het filter wijzigen in een vriendelijkere naam. |
| Opnemen/uitsluiten | U kunt componenten in uw filterdefinitie opnemen of uitsluiten, maar niet beide. |
| Handje/Bezoek/Bezoeker container | Snelle filters omvatten slechts één [filtercontainer](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/cja-filters/filters-overview.html?lang=en#filter-containers) die u een afmeting/metrisch/datumwaaier in (of het van) de filter laat uitsluiten. [!UICONTROL Visitor] bevat overkoepelende gegevens die specifiek zijn voor de bezoeker in verschillende bezoeken en paginaweergaven. Met een container [!UICONTROL Visit] kunt u regels instellen om de gegevens van de bezoeker op basis van bezoeken af te splitsen. Met een container [!UICONTROL Hit] kunt u bezoekersinformatie afsplitsen op basis van afzonderlijke paginaweergaven. De standaardcontainer is [!UICONTROL Hit]. |
| Onderdelen (Dimension/metrisch/datumbereik) | Definieer maximaal 3 regels door de afmetingen en/of metriek en/of datumbereiken en hun waarden toe te voegen. Er zijn drie manieren om de juiste component te vinden:<ul><li>Begin het typen en [!UICONTROL Quick Filter] bouwer vindt automatisch de aangewezen component.</li><li>Gebruik de vervolgkeuzelijst om de component te zoeken.</li><li>Sleep componenten vanuit de linkerspoorstaaf.</li></ul> |
| Operator | Gebruik het vervolgkeuzemenu om standaardoperatoren en [!UICONTROL Distinct Count]-operatoren te zoeken. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/components/filteration/segment-reference/seg-operators.html?lang=en) |
| plusteken (+) | Een andere regel toevoegen |
| EN/OF kwalificatietekens | U kunt de aanduidingen AND of OR toevoegen aan de regels, maar u kunt AND en OR niet combineren in één filterdefinitie. |
| Toepassen | Pas dit filter toe op het deelvenster. Als het filter geen gegevens bevat, wordt u gevraagd of u wilt doorgaan. |
| Opbouwfunctie openen | Opent de Filter Builder. Nadat u het filter hebt opgeslagen in de Filter Builder, wordt het niet langer beschouwd als een &quot;Snel filter&quot;. Het wordt onderdeel van de filterbibliotheek van de component-lijst. |
| Annuleren | Annuleer dit snelle filter - pas het niet toe. |
| Datumbereik | De validator gebruikt het datumbereik van het deelvenster voor het opzoeken van de gegevens. Maar elk datumbereik dat u in een snel filter toepast, overschrijft het datumbereik van het deelvenster boven in het deelvenster. |
| Voorvertoning (rechtsboven) | Hiermee kunt u zien of u een geldig filter hebt en hoe breed het filter is. Geeft de uitsplitsing aan van de gegevensset die u kunt verwachten wanneer u dit filter toepast. Mogelijk ziet u een waarschuwing die aangeeft dat dit filter geen gegevens heeft. U kunt doorgaan of de filterdefinitie wijzigen. |

Hier volgt een voorbeeld van een filter waarin afmetingen en meetwaarden worden gecombineerd:

![](assets/quick-seg2.png)

Het filter verschijnt bovenaan. Let op de zijbalk met een blauwe streep, in tegenstelling tot de blauwe zijbalk voor filters op componentniveau in de filterbibliotheek aan de linkerkant.

![](assets/quick-seg3.png)

## Snelle filters bewerken

1. Houd de muisaanwijzer boven het snelle filter en selecteer het potloodpictogram.
1. Bewerk de filterdefinitie of de filternaam.

## Snelle filters opslaan

U kunt ervoor kiezen om snelle filters op te slaan in [!UICONTROL Quick Filter Builder] of [!UICONTROL Filter Builder].

>[!IMPORTANT]
>Nadat u het filter hebt opgeslagen of toegepast, kunt u het niet meer bewerken in de Snelle Filterbouwer, alleen in de gewone Filter Builder.

### Opslaan in de constructor Quick Filter

1. Zodra u het snelle filter hebt toegepast, beweegt u de muisaanwijzer over het filter en selecteert u het info-pictogram (&quot;i&quot;).
1. Klik op **[!UICONTROL Make available to all projects and add to your component list]**.
1. (Optioneel) Wijzig de naam van het filter.
1. Klik op **[!UICONTROL Save]**.

De zijbalk van het filter verandert van gestreept blauw in blauw. Het wordt nu weergegeven in uw lijst met componenten in de linkerrails.

### Opslaan in de Filterbouwer

1. Houd de muisaanwijzer boven het snelle filter en selecteer het pictogram Info (&quot;i&quot;).
1. **[!UICONTROL Save filter]** selecteren
1. Laat de naam ongewijzigd of wijzig de naam van het filter.

   Ga terug naar Workspace en zie hoe het filter nu een blauw zijpaneel heeft. Dit geeft aan dat het bestand niet langer kan worden bewerkt of geopend in de Quick Filter Builder. En door het op te slaan, wordt het onderdeel van de componentenlijst.

   ![](assets/quick-seg4.png)

Nadat u het filter hebt toegepast, kunt u verkiezen om het aan uw lijst van de filtercomponent toe te voegen en het ter beschikking te stellen van al uw projecten.

1. Houd de muisaanwijzer boven het opgeslagen filter en selecteer het potloodpictogram.

1. Boven aan de Filter Builder ziet u dit dialoogvenster:

   ![](assets/project-only.png)

1. Selecteren naast **[!UICONTROL Make available to all your projects and add to your component list.]**
1. Klik op **[!UICONTROL Save]**.
1. Het filter verschijnt nu in uw lijst van de filtercomponent voor al uw projecten.
1. U kunt het filter [ook met andere mensen in uw organisatie delen.](/help/components/filters/manage-filters.md)

## Wat zijn alleen-projectfilters?

Filters met alleen een project zijn snelle filters of ad-hocprojectfilters in de werkruimte. Wanneer het uitgeven van/het openen van hen in [!UICONTROL Filter Builder], zal het project-enige vakje verschijnen. Als u een snel filter toepast in de builder maar het selectievakje voor het beschikbaar maken niet inschakelt, is het nog steeds een filter dat alleen voor het project geldt, maar kan het niet meer worden geopend in [!UICONTROL Quick Filter Builder]. Als u het vakje controleert en **[!UICONTROL SAVE]** klikt, is het nu een component-lijst filter.
