---
source-git-commit: 2f7e11106334560d3c4b54e6c5eaf84d5e1d4fb6
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---
# Fragmenten

## Beperkte tests voor releasefase {#release-limited-testing}

>[!AVAILABILITY]
>
>De functionaliteit die in dit artikel wordt beschreven, bevindt zich in de Beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het proces van de release van de Customer Journey Analytics raadpleegt u [Release van de Customer Journey Analytics-functie](/help/release-notes/releases.md).

## Beperkte testsectie voor releasefase {#release-limited-testing-section}

>[!AVAILABILITY]
>
>De in deze sectie beschreven functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het proces van de release van de Customer Journey Analytics raadpleegt u [Release van de Customer Journey Analytics-functie](/help/release-notes/releases.md).

## Pakket selecteren {#select-package}

>[!NOTE]
>
>U moet beschikken over **Selecteren** -pakket of hoger gebruiken om de in deze sectie beschreven functionaliteit te gebruiken. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

## Primair pakket {#prime-package}

>[!NOTE]
>
>U moet beschikken over **Eerste** -pakket of hoger gebruiken om de in deze sectie beschreven functionaliteit te gebruiken. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

## Ultieme verpakking {#ultimate-package}

>[!NOTE]
>
>U moet beschikken over **Ultieme** gebruiken om de in deze sectie beschreven functionaliteit te gebruiken. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.


## Criteria van het filter Gegevenswoordenboek {#dd-filter-criteria}

1. (Optioneel) Selecteer de optie **Filter** pictogram ![Filter gegevenswoordenboek, pictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg)Selecteer vervolgens een van de volgende filteropties om de lijst met componenten te filteren:

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **Goedgekeurd**] | Alleen componenten tonen die zijn gemarkeerd als goedgekeurd door een beheerder. |
   | [!UICONTROL **Favorieten**] | Alleen componenten tonen die zich in de lijst Favorieten bevinden. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [Overzicht van componenten](/help/components/overview.md). |
   | [!UICONTROL **Dimensies**] | Alleen componenten weergeven die Dimensionen zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | [!UICONTROL **Cijfers**] | Alleen componenten weergeven die Metrisch zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | [!UICONTROL **Filters**] | Alleen componenten weergeven die filters zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) <!--this is Filters in Customer Journey Analytics--> |
   | [!UICONTROL **Datumbereiken**] | Alleen componenten tonen die Datumbereik hebben. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | [!UICONTROL **Alles tonen**] | Alle componenten tonen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Niet goedgekeurd**] | Alleen componenten tonen die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Ontbrekende beschrijving**] | Alleen componenten weergeven die nog geen beschrijving hebben in het veld Beschrijving. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Duplicaten tonen**] | Alleen componenten weergeven die dezelfde naam of dezelfde beschrijving hebben als een andere component in de geselecteerde gegevensweergave. Dit geldt ook voor componenten die u maakt en de componenten die door de Adobe worden geleverd. Namen of beschrijvingen moeten exact overeenkomen om als duplicaten te kunnen worden weergegeven. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Geen recente gegevens**] | Alleen componenten weergeven die de afgelopen 90 dagen geen gegevens hebben verzameld. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Gemaakt door Adobe**] <!-- I don't see this option--> | Alleen componenten weergeven die zijn gemaakt door Adobe. Componenten die door een beheerder of een andere gebruiker in uw organisatie zijn gemaakt, worden niet weergegeven. |

   {style="table-layout:auto"}

## Componenten gegevenswoordenboek {#dd-component-information}

| Optie | Functie |
|---------|----------|
| [!UICONTROL **Goedgekeurd**] | <p>Geeft aan dat de component is gecontroleerd en goedgekeurd door de beheerder.</p><p>Beheerders zien een optie voor [!UICONTROL **Niet goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Niet goedgekeurd&quot; voor gebruikers.</p> |
| [!UICONTROL **Niet goedgekeurd**] | <p>Geeft aan dat de component nog niet is gereviseerd en goedgekeurd door de beheerder.</p><p>Beheerders zien een optie voor [!UICONTROL **Goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Goedgekeurd&quot; voor gebruikers.</p> |
| [!UICONTROL **Beschrijving**] | Beschrijft de voorgenomen functie van de component. (Deze informatie wordt toegevoegd door de beheerder van Analytics, zoals die in [Componentbeschrijvingen toevoegen](/help/components/add-component-descriptions.md).) |
| [!UICONTROL **Vaak gebruikt met**] | <p>Geeft componenten weer die het meest worden gebruikt met de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Filter en Datumbereik.</p><p>Deze lijst is gebaseerd op gegevens uit de afgelopen 90 dagen. Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Beheerders kunnen de componenten beheren die gebruikers in deze sectie zien door de gewenste componenten te selecteren in het dialoogvenster [!UICONTROL **Altijd opnemen**] en [!UICONTROL **Altijd uitsluiten**] vervolgkeuzelijsten. Voordat u de componenten beheert die gebruikers zien, moet u eerst de opdracht **Alles tonen** om ervoor te zorgen dat u componenten ziet die niet met u worden gedeeld en die door een andere beheerder kunnen zijn toegevoegd.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p> |
| [!UICONTROL **Vergelijkbaar met**] | <p>Geeft componenten weer met vergelijkbare namen als de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Filter en Datumbereik.</p><p>Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Alle dubbele componenten in de gegevensweergave worden hier weergegeven. Analysebeheerders moeten alle dubbele componenten identificeren en verwijderen, zoals beschreven in [Gezondheid gegevenswoordenboek controleren](/help/components/data-dictionary/monitor-data-dictionary-health.md).</p><p>Beheerders kunnen de componenten beheren die gebruikers in deze sectie zien door de gewenste componenten te selecteren in het dialoogvenster [!UICONTROL **Altijd opnemen**] en [!UICONTROL **Altijd uitsluiten**] vervolgkeuzelijsten. Voordat u de componenten beheert die gebruikers zien, moet u eerst de opdracht **Alles tonen** om ervoor te zorgen dat u componenten ziet die niet met u worden gedeeld en die door een andere beheerder kunnen zijn toegevoegd.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p><p>**OPMERKING:** Op dit moment wordt **Vergelijkbaar met** Deze sectie bevat alleen componenten die u maakt en niet de componenten die door Adobe worden geleverd. In een toekomstige release worden componenten toegevoegd die door de Adobe worden geleverd.</p> |
| [!UICONTROL **Tags**] | Hiermee worden alle tags weergegeven die op de component zijn toegepast. Gebruikers met beheerdersrechten kunnen tags toevoegen wanneer ze de component bewerken. |
| [!UICONTROL **Componenttype**] | Hiermee wordt het type component weergegeven dat het is, ongeacht of het een Dimension, Metrisch, Filter of Datumbereik betreft. |
| [!UICONTROL **Gemaakt door**] | Geeft de naam weer van de gebruiker die de component heeft gemaakt. |
| [!UICONTROL **Voorvertoning**] | Toont een voorproef van hoe de component in Analysis Workspace kijkt. |
| [!UICONTROL **Datum van laatste wijziging**] | Hiermee geeft u de dag weer waarop de component voor het laatst is gewijzigd. Deze sectie wordt weergegeven wanneer u Filters, Metriek, Berekende meetgegevens en Datumbereiken weergeeft. |

{style="table-layout:auto"}

## Sorteeropties voor componenten {#components-sort-options}

| Optie | Functie |
|---------|----------|
| [!UICONTROL **Aanbevolen**] | Hiermee sorteert u componenten met de componenten die boven aan de lijst worden aanbevolen. Componenten die het vaakst en het laatst door u of anderen in uw organisatie worden gebruikt, worden hoger weergegeven in de lijst. |
| [!UICONTROL **Alfabetisch**] | Hiermee worden componenten alfabetisch gesorteerd. |
| [!UICONTROL **Categorisch**] | Hiermee worden componenten gesorteerd op componenttype (afmetingen, metrisch, filter, datumbereik). |

{style="table-layout:auto"}

## Tijdvergelijking {#apply-time-comparison}

U kunt de huidige tijdsperiode vergelijken met een vorige tijdsperiode. Als u een optie in dit menu selecteert, ontvangt elk gegevenspunt een met punten gelijkende kleur. Deze tegenhanger vertegenwoordigt die zelfde metrisch in de geselecteerde vorige datumwaaier. Als u deze optie instelt, verdubbelt u het aantal items in het diagram en de rijen in de tabel.

De beschikbare opties voor tijdvergelijking omvatten de vorige periode, 13 weken vóór, 52 weken vóór en een aangepast datumbereik. Als u Aangepast datumbereik selecteert, worden aanvullende opties weergegeven waarmee u het getal en de granulariteit kunt selecteren. Als u Geen selecteert, wordt de datumvergelijking verwijderd.
