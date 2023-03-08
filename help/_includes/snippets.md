---
source-git-commit: 02ff498456fb3d770b9e3c73c3847ac5a55cd705
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 1%

---
# Fragmenten

## Beperkte tests voor releasefase {#release-limited-testing}

>[!AVAILABILITY]
>
>De functionaliteit die in dit artikel wordt beschreven, bevindt zich in de Beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Customer Journey Analytics-functiereleases](/help/release-notes/releases.md).

## Beperkte testsectie voor releasefase {#release-limited-testing-section}

>[!AVAILABILITY]
>
>De in deze sectie beschreven functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Customer Journey Analytics-functiereleases](/help/release-notes/releases.md).

## Criteria van het filter Gegevenswoordenboek {#dd-filter-criteria}

1. (Optioneel) Selecteer de optie **Filter** pictogram ![Filter gegevenswoordenboek, pictogram](/help/components/data-dictionary/assets/data-dictionary-filter-icon.png)Selecteer vervolgens een van de volgende filteropties om de lijst met componenten te filteren:

   | Optie | -functie |
   |---------|----------|
   | [!UICONTROL **Goedgekeurd**] | Alleen componenten tonen die zijn gemarkeerd als goedgekeurd door een beheerder. |
   | [!UICONTROL **Favorieten**] | Alleen componenten tonen die zich in de lijst Favorieten bevinden. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [Overzicht van componenten](/help/components/overview.md). |
   | [!UICONTROL **Dimensies**] | Alleen componenten weergeven die Dimension zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | [!UICONTROL **Cijfers**] | Alleen componenten weergeven die Metrisch zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | [!UICONTROL **Filters**] | Alleen componenten weergeven die filters zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) <!--this is Filters in CJA--> |
   | [!UICONTROL **Datumbereiken**] | Alleen componenten tonen die Datumbereik hebben. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | [!UICONTROL **Alles tonen**] | Alle componenten tonen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Niet goedgekeurd**] | Alleen componenten tonen die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Ontbrekende beschrijving**] | Alleen componenten weergeven die nog geen beschrijving hebben in het veld Beschrijving. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Duplicaten tonen**] | Alleen componenten weergeven die hetzelfde label of dezelfde beschrijving hebben als een andere component in de geselecteerde rapportsuite. Dit geldt ook voor componenten die u maakt en voor componenten die door Adobe worden geleverd. Labels of beschrijvingen moeten exact overeenkomen om te worden weergegeven als duplicaten. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Geen recente gegevens**] | Alleen componenten weergeven die de afgelopen 90 dagen geen gegevens hebben verzameld. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Gemaakt door Adobe**] <!-- I don't see this option--> | Alleen componenten weergeven die zijn gemaakt door Adobe. Componenten die door een beheerder of een andere gebruiker in uw organisatie zijn gemaakt, worden niet weergegeven. |

   {style="table-layout:auto"}

## Componenten gegevenswoordenboek {#dd-component-information}

| Optie | -functie |
|---------|----------|
| [!UICONTROL **Goedgekeurd**] | <p>Geeft aan dat de component is gecontroleerd en goedgekeurd door de beheerder.</p><p>Beheerders zien een optie voor [!UICONTROL **Niet goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Niet goedgekeurd&quot; voor gebruikers.</p> |
| [!UICONTROL **Niet goedgekeurd**] | <p>Geeft aan dat de component nog niet is gereviseerd en goedgekeurd door de beheerder.</p><p>Beheerders zien een optie voor [!UICONTROL **Goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Goedgekeurd&quot; voor gebruikers.</p> |
| [!UICONTROL **Beschrijving**] | Beschrijft de voorgenomen functie van de component. (Deze informatie wordt toegevoegd door de beheerder van Analytics, zoals die in [Componentbeschrijvingen toevoegen](/help/components/add-component-descriptions.md).) |
| [!UICONTROL **Vaak gebruikt met**] | <p>Geeft componenten weer die het meest worden gebruikt met de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Filter en Datumbereik.</p><p>Deze lijst is gebaseerd op gegevens uit de afgelopen 90 dagen. Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Beheerders zien opties voor [!UICONTROL **Altijd opnemen**] en [!UICONTROL **Altijd uitsluiten**]. Met deze opties kunnen beheerders de componenten beheren die gebruikers in deze sectie zien.</p> |
| [!UICONTROL **Vergelijkbaar met**] | <p>Hiermee geeft u componenten weer met labels die vergelijkbaar zijn met de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Filter en Datumbereik.</p><p>Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Om het even welke dubbele componenten in uw rapportreeks zullen hier tonen. Analysebeheerders moeten alle dubbele componenten identificeren en verwijderen, zoals beschreven in [Gezondheid gegevenswoordenboek controleren](/help/components/data-dictionary/monitor-data-dictionary-health.md).</p><p>Beheerders zien opties voor [!UICONTROL **Altijd opnemen**] en [!UICONTROL **Altijd uitsluiten**]. Met deze opties kunnen beheerders de componenten beheren die gebruikers in deze sectie zien.</p> |
| [!UICONTROL **Tags**] | Hiermee worden alle tags weergegeven die op de component zijn toegepast. Gebruikers met beheerdersrechten kunnen tags toevoegen wanneer ze de component bewerken. |
| [!UICONTROL **Componenttype**] | Hiermee wordt het type component weergegeven dat het is, ongeacht of het een Dimension-, Metrisch-, Filter- of Datumbereik betreft. |
| [!UICONTROL **Gemaakt door**] | Geeft de naam weer van de gebruiker die de component heeft gemaakt. |
| [!UICONTROL **Voorvertoning**] | Toont een voorproef van hoe de component in Analysis Workspace kijkt. |
| [!UICONTROL **Datum van laatste wijziging**] | Hiermee geeft u de dag weer waarop de component voor het laatst is gewijzigd. Deze sectie wordt weergegeven bij het weergeven van filters, metriek, berekende meetgegevens en datumbereiken. |

{style="table-layout:auto"}