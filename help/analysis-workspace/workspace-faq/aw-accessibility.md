---
description: De steuneigenschappen van de toegankelijkheid in de Werkruimte van de Analyse
title: Toegankelijkheid in analysewerkruimte
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---


# Toegankelijkheid in analysewerkruimte

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Meer weten over toegankelijkheidsondersteuning in [!UICONTROL Analysis Workspace], het belangrijkste analyseprogramma voor Adobe Analytics.

De toegankelijkheid verwijst naar het maken van producten bruikbaar voor mensen met visuele, auditieve, cognitieve, motorische en andere handicaps. De voorbeelden van toegankelijkheidseigenschappen voor softwareproducten omvatten de steun van de het schermlezer, tekstequivalenten voor grafiek, toetsenbordkortere weg, verandering van vertoningskleuren in hoog contrast, etc.

[!UICONTROL Analysis Workspace] biedt een aantal gereedschappen die het toegankelijk maken voor gebruik, waaronder:

## navigeren [!UICONTROL Workspace] het toetsenbord gebruiken

Navigatie in [!UICONTROL Analysis Workspace] werkt boven > naar beneden en links > naar rechts. De volgende navigatie-elementen vergemakkelijken de toegankelijkheid:

* De `F6` sleutel maakt het mogelijk om landmarktoversnelingen te maken
* De `Tab` belangrijke bewegingen tussen afzonderlijke elementen.
* Wij passen nadrukindicatoren toe zodat de waargenomen toetsenbordgebruikers een duidelijke aanwijzing hebben waarvan het element UI momenteel nadruk heeft. De indicator is een blauwe grens rond het geselecteerde element.

   ![Focusindicator](assets/focus-indicator.png)

### Toetsenbordnavigatie voor interactie bij slepen en neerzetten

[!UICONTROL Analysis Workspace] is een belemmering &amp; dalingsgebruikersinterface. Nochtans, kunnen de gebruikers componenten toevoegen gebruikend het toetsenbord in plaats daarvan:

1. Tab aan een component in de linkerrail.
1. Druk `Enter` om te selecteren.
1. De pijlsleutels van het gebruik om aan het gebied te navigeren waar u de component wilt laten vallen.
1. Druk `Enter` om het onderdeel te plaatsen.

### Sneltoetsen (sneltoetsen)

[!UICONTROL Analysis Workspace] biedt een rijke reeks van [sneltoetsen](/help/analysis-workspace/build-workspace-project/fa-shortcut-keys.md) voor een naadloze werkstroom. Sommige gemeenschappelijke kortere weg voor navigatie, analyseverwezenlijking, en inzicht democratisering zijn hieronder vermeld.

#### Navigatie

| Snelkoppeling | Actie |
|---|---|
| Alt + Shift + 1 / 2 / 3 | Sprong op verschillende rails: [!UICONTROL Panels], [!UICONTROL Visualizations]of [!UICONTROL Components] |
| Alt + pijl links/rechts | Navigeer tussen deelvensters |
| Alt + M | Alle deelvensters samenvouwen/uitbreiden |
| Alt+ Ctrl + M | Het actieve paneel van de ineenstorting/breidt uit |
| Ctrl + / | Zoeken in linkerrail |

#### Analyse maken

| Snelkoppeling | Actie |
|---|---|
| Alt + 1 | Nieuwe freeformtabel |
| Ctrl + Shift + C | Nieuwe berekende metrisch |
| Ctrl + Shift + D | Nieuwe datumbereik |
| Ctrl + Shift + E | Nieuw segment |
| Ctrl + Z | ongedaan maken |
| De verschuiving van de greep (in de dropzone van het paneelsegment) | Een [druppelfilter](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html) |

#### democratisering

| Snelkoppeling | Actie |
|---|---|
| Ctrl + S | Opslaan |
| Ctrl + Shift + G | krullen |
| Ctrl + G | Delen |
| Alt + Shift + S | Planning |
| Alt + L | Koppeling naar project ophalen |
| Ctrl + Shift + B | PDF downloaden |

## Ondersteuning voor schermlezers en schermmagnifiers

Een het schermlezer leest tekst die op het computerscherm verschijnt. Het leest ook niet-tekstuele informatie, zoals knoopetiketten of beeldbeschrijvingen in de toepassing, die in toegankelijkheidsmarkeringen of attributen wordt verstrekt.

## Kleurenpaletten en contrast

[!UICONTROL Analysis Workspace] streeft naar overeenstemming met WCAG 2.1 AA, met inbegrip van vereisten voor kleurencontrast.

Bovendien kunnen de gebruikers hun eigen aangewezen kleurenpalet voor een project onder plaatsen **[!UICONTROL Project]** > **[!UICONTROL Project settings]** > [Kleurenpalet project](/help/analysis-workspace/build-workspace-project/color-palettes.md).

## Vereiste veldvalidatie in componentbouwers

Wanneer het bouwen van een component, worden de vereiste gebieden bevestigd wanneer u sparen. Als een vereist gebied geen bevestiging overgaat, zal het in rood met een foutenpictogram worden geschetst. Er verschijnt een schriftelijke beschrijving van de kwestie die moet worden vastgelegd.

Zodra een component volledig bevestigd is, drukt u op `Save` sluit de bouwer.

![Foutvalidatie](assets/error-validation.png)

## Ondersteuning voor functies voor toegankelijkheid van besturingssystemen

De Werkruimte van de analyse steunt ingebouwde MS Windows en macOS toegankelijkheidseigenschappen zoals hoog-contrastwijze, kleverige sleutels, en langzame sleutels/filtersleutels. Het verstrekt ook informatie over het gebruikersinterface aan het werkende systeem om interactie met ondersteunende technologieën, met inbegrip van het schermlezers zoals VoiceOver voor macOS en NVDA op Vensters toe te laten.