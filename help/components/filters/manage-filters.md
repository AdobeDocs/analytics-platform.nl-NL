---
title: Filters beheren
description: slanken hoe te om filters in Customer Journey Analytics te beheren
exl-id: b8869560-0cf1-4e5d-a03c-dfca85d05e66
translation-type: tm+mt
source-git-commit: 76260b7362396c76942dadab599607cd038ed651
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 1%

---

# Filters beheren

Filterbeheer biedt verschillende manieren om filters te krommen, zoals delen, labelen, goedkeuren, kopiëren, verwijderen en markeren als favorieten.

In Filterbeheer worden alle filters weergegeven die u hebt en die met u zijn gedeeld. Gebruikers op beheerniveau kunnen alle filters in de organisatie zien. In dit overzicht worden de gebruikersinterface en de mogelijkheden van Filterbeheer weergegeven.

Open Filterbeheer door in de bovenste navigatie naar **[!UICONTROL Customer Journey Analysis]** > **[!UICONTROL Components]** > **[!UICONTROL Filters]** te gaan.

## Gebruikersinterface voor filterbeheer

![](assets/filter-manager-ui.png)

| Aantal | UI-onderdeel | Beschrijving |
|---|---|---|
| 3 | Filterbeheerbalk | Nadat u een filter hebt gecontroleerd, wordt deze werkbalk weergegeven. De meeste beheertaken kunnen vanaf deze werkbalk worden voltooid. |
| 2 | Selectievakjes | Controleer een filter om het te beheren. |
| 4 | Favorieten | Wanneer u op de ster naast een filter klikt, wordt de ster geel en wordt het filter als favoriet gemarkeerd. |
| 5 | Titel en beschrijving | Opgegeven in de Filter Builder. Als u de titel en beschrijving wilt bewerken, klikt u op de titelkoppeling. Hiermee gaat u terug naar de Filterbouwer. |
| 7 | Eigenaar | Hiermee wordt aangegeven wie de eigenaar van het filter is. Als niet-beheerder kunt u alleen filters zien die u bezit of die met u gedeeld zijn. |
| 8 | Labels (niet gecontroleerd in kolomkiezer, vandaar dat de kolom niet wordt weergegeven) | Tags die op het filter zijn toegepast, door u of door personen die het filter met u hebben gedeeld. |
| 9 | Gedeeld met | Hier worden personen of groepen weergegeven (alleen Admin) of Alle personen (alleen Admin) waarmee u het filter hebt gedeeld. |
| 10 | Datum gewijzigd | Hiermee wordt de datum weergegeven waarop het filter voor het laatst is gewijzigd. |
| 11 | Kolomkiezer | (Rechtsboven) Hiermee kunt u selecteren welke kolommen u wilt weergeven in Filterbeheer. |
| 12 | Gedeeld pictogram | Geeft aan dat dit filter door u of met u wordt gedeeld. |
| 13 | Goedgekeurd pictogram | Geeft aan dat dit filter is goedgekeurd door een beheerder. |
| 14 | Overige filters | Hiermee kunt u filters weergeven op basis van tags, gegevensweergaven, eigenaars en andere opties (Alles tonen, Mijne, Gedeeld met mij, Goedgekeurd, Favorieten.) |

## Abonnementsfilters

Wanneer u enige tijd besteedt aan het plannen van filters, wordt de kans groter dat deze voor uw organisatie nuttig zijn en dat de nummers van deze filters gecontroleerd blijven.

* Kijk naar het publiek: Wie zal het consumeren? Met wie gaat u het delen? Welke groepen mensen gebruiken dit filter en hoe moet ik het dienovereenkomstig labelen? Dit betekent ook dat u een goede filterbeschrijving moet geven. De beschrijving moet ten minste de volgende vragen beantwoorden:

   * Wanneer is dit filter nuttig?

   * Wanneer moet ik dit filter gebruiken?

* Bepaal het filterbereik. Welke [filtercontainer](/help/components/filters/filters-overview.md) het beste vertegenwoordigt het werkingsgebied? Gebruik de kleinst mogelijke container.

* Bepaal welke elementen u in de filterdefinitie wilt opnemen en welke waarden.

* Overweeg hoe u uw goedkeuringsproces wilt ontvouwen. Zal één persoon filters controleren en goedkeuren of zal het een besluit van een commissie zijn?

* Definieer uw filters met het oog op een filterbibliotheek die zakelijke gebruikers de mogelijkheid biedt om filteronderdelen of componenten op modulaire wijze te stapelen en opnieuw te gebruiken. Welke &quot;modules&quot;moet u bepalen om deze bibliotheek tot realiteit te maken?

### Labelfilters

In Filterbeheer kunt u de filters organiseren door ze te labelen. Alle gebruikers kunnen labels voor filters maken en een of meer tags op een filter toepassen. U kunt echter alleen tags zien voor de filters die u bezit of die met u zijn gedeeld.

Welke soorten markeringen moet u creëren? Hier volgen enkele suggesties voor handige tags:

* Tags die zijn gebaseerd op teamnamen, zoals Sociale marketing, Mobiele marketing.

* Projectlabels (analysetags), zoals analyse van de pagina Entry.

* Categorielabels: Mannen; geografie.

* Workflowlabels: goed te keuren; Gecurreerd voor (een specifieke bedrijfseenheid)

Een filter labelen:

1. Markeer in Filterbeheer het selectievakje naast het filter dat u wilt labelen. De werkbalk voor filterbeheer wordt weergegeven.

1. Klik **[!UICONTROL Tag]** en of

   * uit bestaande tags selecteren, of

   * Voer een nieuwe tagnaam in en druk op **[!UICONTROL Enter]**.

1. Klik nogmaals **[!UICONTROL Tag]** om het filter te labelen.

Het label moet nu in de kolom Codes staan. (Klik op het tandwielpictogram rechtsboven om de kolommen te beheren.)
U kunt ook filteren op tags door naar **[!UICONTROL Filters > Tags]** te gaan.

### Filters goedkeuren

Binnen de Manager van de Filter, kunt u opstelling een werkschema dat het goedkeuren van filter voor diverse niveaus van toepassing, voor specifieke afdelingen of groepen, en verenigbaar met het rapporteringsbeleid omvat.

Hieronder wordt beschreven hoe u een filter kunt markeren zoals het is goedgekeurd:

1. Schakel in Filterbeheer het selectievakje links van de titel Filter in.

1. Klik op **[!UICONTROL Approve]** in de taakbalk voor filterbeheer.

1. U kunt overwegen de goedgekeurde filters met uw organisatie te delen.

1. Klik op **[!UICONTROL OK]**.

   Let op het goedkeuringspictogram naast het filter in de lijst:

   ![](assets/seg_approved.png)

1. U kunt een goedgekeurd filter ook niet goedkeuren door **[!UICONTROL Unapprove]** te klikken.

### Filters delen

Afhankelijk van uw machtigingen kunt u filters delen met uw hele organisatie, groepen of individuele gebruikers.

| Beheerder | Niet-beheerder |
|---|---|
| Kan filters delen met Alles, met groepen en met gebruikers. Zie de [documentatie van de Admin Console](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) voor meer informatie. | Filters kunnen alleen met individuele gebruikers worden gedeeld. |

Wanneer zou u filters met het volledige bedrijf tegenover enkel een groep gebruikers of individuen moeten delen? Hier volgen enkele aanbevolen procedures:

* Als Admin, deel een filter met allen als het van nut voor het volledige bedrijf is en iedereen het comfortabel gebruikt. In dit geval moet u ook overwegen om er een goedgekeurd filter van te maken.

* Als Admin, deel een filter met een specifiek Profiel van het Product als de filter goede bedrijfswaarde voor dat team verstrekt. Dit type filter niet officieel goedkeuren.

* Als Admin of een individuele gebruiker, deel een filter met andere individuen om een filter te onderzoeken en te bevestigen. Als het niet nuttig blijkt, kan het worden verworpen. Dit type filter niet officieel goedkeuren.

Een filter delen:

1. Markeer in Filterbeheer het selectievakje naast het filter dat u wilt delen.

1. Klik op **[!UICONTROL Share]** in de werkbalk voor filterbeheer.

1. Als u een beheerder bent, kunt u Alles selecteren of kiezen uit Groepen en Gebruikers in uw organisatie. Als niet-beheerder kunt u alleen individuele gebruikers zien. Gebruik het veld Zoeken om te zoeken naar groepen of gebruikers. Klik op **[!UICONTROL Share]**. Het pictogram Gedeeld wordt weergegeven naast het filter: ![](assets/share_icon.png)

1. U kunt filteren op filters die met u worden gedeeld door naar Filters > Andere Filters > met mij worden gedeeld.

### Filters markeren als favorieten

Filters markeren als favorieten is een andere manier om ze te ordenen voor gebruiksgemak.

1. Controleer in Filterbeheer de ster naast een filter dat u als favoriet wilt markeren. De ster wordt geel wanneer u deze selecteert.

1. U kunt ook filteren op favorieten onder Filters > Overige filters > Favorieten.
