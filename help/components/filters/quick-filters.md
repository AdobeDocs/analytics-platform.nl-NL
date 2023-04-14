---
description: Snelfilters gebruiken in Analysis Workspace voor Customer Journey Analytics
title: Snelle filters
feature: CJA Workspace Basics
role: User, Admin
exl-id: 549e5db5-fcdf-43c5-bc43-590144aee309
source-git-commit: cb1654cef651c5143667302c3fc592ba503dfe0a
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Snelle filters

Met snelle filters kunt u eenvoudig gegevens binnen een bepaald project verkennen zonder dat u een complexer component-list filter hoeft te maken in het dialoogvenster [Filter Builder](/help/components/filters/create-filters.md).

Houd rekening met het volgende wanneer u snelle filters maakt:

* Snelle filters zijn alleen van toepassing op het project waar ze zijn gemaakt. Ze zijn niet beschikbaar in andere projecten en kunnen niet worden gedeeld met andere gebruikers.
* Er zijn maximaal drie regels toegestaan.
* Geneste containers of sequentiële regels worden niet ondersteund.

In de volgende video ziet u hoe u snelle filters kunt gebruiken. (Opmerking: in deze video wordt de term &#39;&#39;snelle segmenten&#39;&#39; gebruikt in plaats van &#39;&#39;snelle filters&#39;&#39;. De functionaliteit is echter hetzelfde.)

>[!VIDEO](https://video.tv.adobe.com/v/341466/?quality=12&learn=on)

## Een snel filter maken {#create}

Elke gebruiker in de Anlysis-werkruimte kan een snelfilter maken.

Een snelfilter maken:

1. Kies een van de volgende methoden om het snelfilter te maken:

   * **Ad hoc (slepen en neerzetten):** Sleep een component van de linkerspoorstaaf naar de neerzetzone naast de **Filter** in de koptekst van het deelvenster en selecteert u vervolgens het pictogram **Bewerken** pictogram om het filter aan te passen.

      ![Ad-hocfilter bewerken](assets/filter-adhoc-edit.png)

      >[!NOTE]
      >
      > Houd rekening met het volgende wanneer u een snel filter ad hoc (slepen en neerzetten) maakt:
      > * De volgende componenttypen worden niet ondersteund: berekende metriek en afmetingen, evenals metriek waarvan u geen filters kunt bouwen.
      > * Voor volledige afmetingen en gebeurtenissen maakt Analysis Workspace &#39;exists&#39; raakfilters. Voorbeelden: `Hit where eVar1 exists` of `Hit where event1 exists`.
      > * Als &#39;unspecified&#39; of &#39;none&#39; wordt neergezet in de neerzetzone van het filter, wordt deze automatisch omgezet in een filter &#39;does not exist&#39;, zodat deze op de juiste wijze wordt behandeld tijdens het filteren.



   * **Het filterpictogram gebruiken:** Selecteer in een tabel met vrije vorm de optie **Filter** in de koptekst van het deelvenster.

      ![Segment, filter](assets/quick-seg1.png)

1. Pas een van de volgende instellingen aan:

   | Instelling | Beschrijving |
   | --- | --- |
   | [!UICONTROL Name] | De standaardnaam van een filter is een combinatie van de regelnamen in het filter. U kunt de naam van het filter wijzigen in een vriendelijkere naam. |
   | [!UICONTROL Include/exclude] | U kunt componenten in uw filterdefinitie opnemen of uitsluiten, maar niet beide. |
   | [!UICONTROL Hit/Visit/Visitor] container | Snelle filters omvatten één [filtercontainer](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/cja-filters/filters-overview.html#filter-containers) alleen dat u een dimensie/metrisch/datumbereik in het filter kunt opnemen (of dit kunt uitsluiten). [!UICONTROL Visitor] bevat overkoepelende gegevens die specifiek zijn voor de bezoeker in verschillende bezoeken en paginaweergaven. A [!UICONTROL Visit] Met de container kunt u regels instellen om de gegevens van de bezoeker op basis van bezoeken te splitsen, en een [!UICONTROL Hit] Met de container kunt u bezoekersinformatie onderverdelen op basis van afzonderlijke paginaweergaven. De standaardcontainer is [!UICONTROL Hit]. |
   | [!UICONTROL Components] (Dimension/metrisch/datumbereik) | Definieer maximaal 3 regels door componenten (afmetingen, metriek, datumbereiken of afmetingswaarden) toe te voegen. Er zijn drie manieren om de juiste component te vinden:<ul><li>Begin te typen en de snelle filterbuilder vindt automatisch de juiste component.</li><li>Gebruik de vervolgkeuzelijst om de component te zoeken.</li><li>Sleep componenten vanuit de linkerspoorstaaf.</li></ul> |
   | [!UICONTROL Operator] | Gebruik het vervolgkeuzemenu om standaardoperatoren te zoeken en [!UICONTROL Distinct Count] operatoren. Zie [Filteroperatoren](operators.md). |
   | plusteken (+) | Een andere regel toevoegen |
   | EN/OF kwalificatietekens | U kunt de aanduidingen AND of OR toevoegen aan de regels, maar u kunt AND en OR niet combineren in één filterdefinitie. |
   | [!UICONTROL Apply] | Pas dit filter toe op het deelvenster. Als het filter geen gegevens bevat, wordt u gevraagd of u wilt doorgaan. |
   | [!UICONTROL Open builder] | Opent de Filter Builder. Nadat u het filter in de Bouwer van de Filter opslaat of toepast, wordt het niet meer beschouwd als een &quot;Snelle Filter&quot;. Het wordt onderdeel van de filterbibliotheek van de component-lijst. <p>Als u de component beschikbaar wilt maken voor al uw projecten en in het linkerspoor, selecteert u de optie [!UICONTROL **Maak dit filter beschikbaar aan al uw projecten en voeg het aan uw componentenlijst toe**].</p><p>Zie de sectie voor meer informatie [Een snel filter opslaan als een filter voor een lijst met componenten](#save-a-quick-filter-as-a-component-list-filter) in dit artikel.</p><p>**Opmerking:** Alleen gebruikers met de machtiging Filter maken in het dialoogvenster [Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/summary-tables.html#analytics-tools) kan de Filterbouwer openen.</p> |
   | [!UICONTROL Cancel] | Annuleer dit snelle filter (pas het niet toe). |
   | [!UICONTROL Date range] | De validator gebruikt het datumbereik van het deelvenster voor het opzoeken van de gegevens. Maar elk datumbereik dat u in een snel filter toepast, overschrijft het datumbereik van het deelvenster boven in het deelvenster. |
   | Voorvertoning (rechtsboven) | Hiermee kunt u zien of u een geldig filter hebt en hoe breed het filter is. Geeft de uitsplitsing aan van de gegevensset die u kunt verwachten wanneer u dit filter toepast. Er kan een melding verschijnen dat aangeeft dat dit filter geen gegevens heeft. In dit geval kunt u doorgaan of de filterdefinitie wijzigen. |

1. Selecteren [!UICONTROL **Toepassen**] om uw wijzigingen op te slaan.

## Een snelfilter bewerken {#edit}

1. Houd de muisaanwijzer boven het snelle filter dat u wilt bewerken en selecteer vervolgens het gereedschap **Bewerken** pictogram.

   ![Ad-hocfilter bewerken](assets/filter-adhoc-edit.png)

1. Bewerk de filterdefinitie of de filternaam.
1. Selecteren [!UICONTROL **Toepassen**] om uw wijzigingen op te slaan.

## Een snel filter opslaan als een filter voor een lijst met componenten {#save}

>[!IMPORTANT]
>
> Houd rekening met het volgende wanneer u een snel filter opslaat:
> 
> * Als u een snel filter wilt opslaan, hebt u de machtiging Filterontwerp nodig in het dialoogvenster [Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/summary-tables.html#analytics-tools).
> 
> * Nadat u het filter hebt opgeslagen of toegepast, kan het niet meer worden bewerkt in de snelle filterbuilder. In plaats daarvan moet u de gewone Filter Builder gebruiken.


U kunt ervoor kiezen om snelle filters op te slaan als filters voor lijsten met componenten. De voordelen van de filters voor de lijst van componenten zijn:

* Beschikbaarheid voor al uw werkruimteprojecten
* Complexere filters en opeenvolgende filters ondersteunen

U kunt filters opslaan vanuit de functie Snel filter maken of vanuit de functie [!UICONTROL Filter Builder].

### Opslaan in de snelle filterbuilder {#save2}

1. Nadat u het snelle filter hebt toegepast, houdt u de muisaanwijzer boven het filter en selecteert u het pictogram Info (&quot;i&quot;).
1. Selecteren **[!UICONTROL Make available to all projects and add to your component list]**.
1. (Optioneel) Wijzig de naam van het filter.
1. Selecteren **[!UICONTROL Save]**.

   Het filter wordt nu weergegeven in de lijst met componenten in de linkertrack. Let er ook op dat de zijbalk van het filter verandert van lichtblauw in donkerder blauw, wat aangeeft dat deze niet langer kan worden bewerkt of geopend in de snelle filterconstructor.

### Opslaan in de Filter Builder {#save3}

1. Nadat u het snelle filter hebt toegepast, houdt u de muisaanwijzer boven het filter en selecteert u het pictogram Info (&quot;i&quot;).
1. Selecteren **[!UICONTROL Save filter]**
1. (Optioneel) Wijzig de naam van het filter en selecteer [!UICONTROL **Toepassen**].

   Ga terug naar Workspace en merk op dat de zijbalk van het filter verandert van lichtblauw in donkerder blauw om aan te geven dat deze niet langer kan worden bewerkt of geopend in de snelle filterbuilder. En door het op te slaan, wordt het onderdeel van de componentenlijst.

   ![Lijst met filtercomponenten](assets/quick-seg4.png)

Nadat u het filter hebt toegepast, kunt u het toevoegen aan de lijst met filtercomponenten en het beschikbaar maken voor al uw projecten.

1. Houd de muisaanwijzer boven het opgeslagen filter en selecteer het potloodpictogram.

1. Selecteren [!UICONTROL **Opbouwfunctie openen**].

1. Boven aan de Filter Builder ziet u dit dialoogvenster:

   ![Dialoogvenster Filter](assets/project-only-filter-dialog.png)

1. Schakel het selectievakje in naast **[!UICONTROL Make this filtr available to all your projects and add it to your component list.]**

1. Selecteren **[!UICONTROL Save]**.

   Het filter verschijnt nu in uw lijst van de filtercomponent voor al uw projecten.
U kunt ook [delen, filter](/help/components/filters/manage-filters.md) met andere mensen in uw organisatie.

## Voorbeeld van snel filter

In het volgende voorbeeld van een filter worden afmetingen en meetwaarden gecombineerd:

![Voorbeeld van filterdefinitie](assets/quick-seg2.png)

