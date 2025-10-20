---
description: Leer hoe u presentaties in pptx-indeling kunt genereren op basis van Workspace-rapporten.
keywords: Analysis Workspace
title: Presentaties genereren op basis van Workspace-rapporten
feature: Curate and Share
role: User
hide: true
hidefromtoc: true
source-git-commit: 9e23382800326440ed2a583e80029c9f27bb2494
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Gegevensverhaal: presentaties genereren op basis van Workspace-rapporten {#generate-powerpoint}

De gebruikers met [ de noodzakelijke toestemmingen ](#permission-requirements-to-generate-slides) kunnen .pptx presentaties van de projecten van Analysis Workspace automatisch produceren. Bij het genereren van deze diapresentaties maakt Customer Journey Analytics automatisch een artikel op basis van uw gegevens door belangrijke inzichten te identificeren en deze om te zetten in dia&#39;s die klaar zijn voor gebruik door belanghebbenden.

Deze functionaliteit verkort de tijd en moeite die nodig zijn om bevindingen uit uw Workspace-projecten te onthullen en stelt u in staat om snel verhalen van managers te maken en de gevolgen voor het bedrijf aan de belanghebbenden door te geven.

Dit automatisch gegenereerde gegevensverhaal stelt analisten in staat zich te concentreren op gegevensverkenning, terwijl Customer Journey Analytics de bevindingen van de analist voor gebruik door belanghebbenden bijhoudt en opmaakt.

## Gegevensartikelen in diapresentaties begrijpen

Analysis Workspace gebruikt generatieve AI om gegevensartikelen te maken in diapresentaties. Deze gegevensverhalen vullen een analyse voor een bepaald Workspace-project aan door extra context te bieden, belangrijke hoogtepunten te zoeken en ideeën te geven voor de volgende stappen. verborgen trends, anomalieën, factoren die bijdragen tot de groei, belangrijke stuurprogramma&#39;s

### Aanvullende waarde die wordt verschaft door gegevensartikelen

Gegevensverhalen vullen een analyse voor een bepaald Workspace-project aan door:

* Aanvullende context bieden

* Belangrijke inzichten benadrukken

* Verborgen trends, anomalieën en andere factoren die bijdragen tot de ontwikkeling van

* Belangrijke stuurprogramma&#39;s identificeren

* Het geven van ideeën voor volgende stappen

### Projectelementen die gegevensartikelen vormen

Analysis Workspace maakt gegevensartikelen door de volgende projectelementen in overweging te nemen:

* Interdimensionale en intermetrische relaties

* De afzonderlijke elementen die de basis vormen van de analyse: afmetingen, meetwaarden, filters, vrije tabelstructuur, visualisaties en deelvensters

* De namen die aan de deelvensters, tabellen en visualisaties worden gegeven

* De volgorde van metriek in een vrije-vormlijst (om prioriteit te bepalen)

* Samenvattingsnummers en samenvattingsteksten (om de metriek te bepalen die in het gegevensartikel moet worden gemarkeerd)

### Presentatie-elementen van een gegevensartikel

De verhalen van gegevens bestaan uit een overzichtsdia, detaildia&#39;s, en sectieverdelers.

**Uitvoerende samenvatting:** geeft voorrang aan de hoogste-waardeinzichten en creeert een overkoepelend verhaal tussen 1 en 5 zinnen in lengte.

**dia&#39;s van het Detail:** produceert inzichten met betrekking tot om het even welke lijsten, panelen, of visualisaties in een project van Workspace. Inzichten bestaan uit trends, seizoensinvloeden, anomalieën en correlaties.

**de verdelers van de Sectie:** verdeelt inzichten met geschikt geplaatste en genoemde sectieverdelers.

## Een .pptx-presentatie genereren op basis van een Workspace-project

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-powerpoint-include-visualizations"
>title="Opgenomen deelvensters en visualisaties"
>abstract="Kies de deelvensters en visualisaties die u in de presentatie wilt opnemen. U kunt maximaal 50 visualisaties opnemen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-presentation-emphasized-components"
>title="Gemarkeerde componenten"
>abstract="Kies maximaal 5 metriek en 5 dimensies van uw visualisaties die u in de presentatie wilt benadrukken. De maatstaven die u kiest, worden cursief weergegeven, de afmetingen worden vet weergegeven en de dimensie-items worden in een contrasterende kleur weergegeven."

<!-- markdownlint-enable MD034 -->

1. Ga naar het Workspace-project dat de gegevens bevat die u als basis voor uw presentatie wilt gebruiken.

1. Selecteer **[!UICONTROL Generate slides]** rechtsboven op de pagina.

   Het dialoogvenster Dia&#39;s genereren wordt weergegeven.

   ![ produceer de dialoog van dia&#39;s ](assets/generate-slides.png)

1. Geef de volgende informatie op:

   | Optie | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Cover title]** | Geef een titel op voor de presentatie. Deze titel wordt weergegeven op de titeldia van de presentatie. |
   | **[!UICONTROL Include presenter name]** | Geef de naam van de presentator op. Deze naam wordt weergegeven op de titeldia van de presentatie, onder de titel van de omslag. |
   | **[!UICONTROL Panels and visualizations to include]** | Kies de deelvensters en de visualisatie die u in de presentatie wilt opnemen. U kunt maximaal 50 visualisaties opnemen.<p>De meeste deelvensters en visualisaties worden ondersteund. Voor informatie over niet gestaafde panelen en visualisatie, zie [ Niet gestaafde projectelementen en eigenschappen ](#unsupported-project-elements-and-features).</p> |
   | **[!UICONTROL Panel and visualization descriptions]** | |
   | **[!UICONTROL Annotations]** | |
   | **[!UICONTROL Emphasize components]** | Kies maximaal 5 metriek en 5 dimensies van uw visualisaties die u in de presentatie wilt benadrukken.<p>Wanneer geen nadruk wordt toegepast, tonen de componenten in presentaties als volgt:<ul><li>**Metriek en afmetingen:** Cursief</li><li>**de punten van Dimension:** Citatietekens</li></ul></p><p>Wanneer de nadruk wordt toegepast, tonen de componenten in presentaties als volgt:</p><ul><li>**Metriek en afmetingen:** Cursief en gewaagd</li><li>**de punten van Dimension:** Vet wanneer de overeenkomstige afmeting wordt benadrukt<p>Er wordt ook een kleur toegepast op het dimensie-item wanneer het dimensie-item in het diagram wordt gemarkeerd.</p></li></ul> |

1. (Voorwaardelijk) Selecteer **[!UICONTROL Default theme]** als u snel dia&#39;s in minder stappen wilt genereren en als een bedrijfsthema niet vereist is voor uw presentatie.

   Kies gewoon het kleurthema van uw presentatie door de gewenste kleur te selecteren.

   ![ produceer dia&#39;s met het standaardthema ](assets/generate-slides-default-theme.png)

1. (Voorwaardelijk) Selecteer **[!UICONTROL Upload template]** als uw diapresentatie moet overeenkomen met een bedrijfsthema. Voor deze optie moet u een aangepaste sjabloon uploaden en aangepaste stijlen toepassen.

   ![ produceer dia&#39;s met een douanemalplaatje ](assets/generate-slides-upload-template.png)

   Voer een van de volgende twee handelingen uit om een aangepaste sjabloon te uploaden:

   * (Aanbevolen) Download een lege sjabloon en wijzig deze.

      1. Download deze lege sjabloon. <!--add link-->

      1. Pas uw aangepaste stijlen toe op de lege sjabloon.

      1. Upload de sjabloon opnieuw zonder de namen van de stramienlay-outs te wijzigen.

   * Een aangepaste sjabloon rechtstreeks uploaden.

      1. Sleep de aangepaste sjabloon vanuit het bestandssysteem naar het neerzetgebied.

         of

         Selecteer **[!UICONTROL Browse]** en blader naar de aangepaste sjabloon in het bestandssysteem en selecteer deze.

         Zorg ervoor dat het geüploade bestand de volgende stramienlay-outs heeft: &quot;Title_Slide&quot;, &quot;Section_Divider&quot;, &quot;Title_Text&quot;, &quot;Title_Chart&quot;, &quot;Title_Two_Content_Mixed&quot;, &quot;Title_Three_Content_Mixed&quot;

         .pptx- en .potx-bestanden van maximaal 25 MB worden ondersteund.

1. Selecteer **[!UICONTROL Export PPT]**.

1. (Geadviseerd) overzicht en geef de .ppt presentatie uit en breng om het even welke noodzakelijke veranderingen aan, zoals die in de volgende sectie worden beschreven, [ geeft dia&#39;s van een eerder geproduceerde presentatie ](#edit-slides-from-a-previously-generated-presentation) uit.

## Dia&#39;s uit een eerder gegenereerde presentatie bewerken


## Een gegenereerde .pptx-presentatie downloaden



## Vereisten voor machtigingen om dia&#39;s te genereren

>[!AVAILABILITY]
>
>Als uw organisatie geen toegang heeft om diapresentaties te genereren op basis van een Workspace-project, neemt u contact op met uw Adobe-accountvertegenwoordiger voor meer informatie over licenties.
>
>Deze mogelijkheid is standaard ingeschakeld voor alle gebruikers in organisaties die over de vereiste licenties beschikken.

Beheerders van productprofielen waarvan organisaties licenties hebben om dia&#39;s te genereren, kunnen de toegang indien nodig uitschakelen.

In [!UICONTROL Adobe Admin Console] bepaalt de machtiging [!UICONTROL Reporting Tools] **[!UICONTROL Data storytelling]** de toegang tot deze mogelijkheid. A [ beheer van het productprofiel ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) moet deze stappen in [!UICONTROL Admin Console] volgen als zij toegang willen onbruikbaar maken:
1. Ga naar **[!UICONTROL Admin Console]** > **[!UICONTROL Products and services]** > **[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Product Profiles]**
1. Selecteer de titel van het productprofiel waartoe u toegang wilt verlenen aan [!UICONTROL Data storytelling] .
1. Selecteer **[!UICONTROL Permissions]** in het specifieke productprofiel.
1. Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) om uit te geven **[!UICONTROL Reporting Tools]**.
1. Selecteer ![ AddCircle ](/help/assets/icons/RemoveCircle.svg) om **het verhaal van Gegevens** uit **[!UICONTROL Included permission items]** te verwijderen.

   <!--add screenshot of permission in the admin console-->

1. Selecteer **[!UICONTROL Save]** om de machtigingen op te slaan.

Voor meer informatie, zie [ gebruiker-vlakke toegang ](/help/technotes/access-control.md#user-level-access) in [ controle van de Toegang ](/help/technotes/access-control.md#access-control) voor meer informatie.

## Niet-ondersteunde projectelementen en -functies {#unsupported}

De volgende Analysis Workspace-elementen en -functies die in een project worden gebruikt, worden niet ondersteund bij het genereren van dia&#39;s:

* Kenmerk, deelvenster

  Dit deelvenster wordt zo gedimd weergegeven wanneer de configuratieopties worden weergegeven.

  Alle andere panelen kunnen in dia&#39;s worden omvat die van een project van Workspace worden geproduceerd.

* Sommige visualisaties

  De meeste visualisaties kunnen in dia&#39;s worden omvat die van een project van Workspace worden geproduceerd. De volgende visualisaties kunnen echter niet worden opgenomen en worden weergegeven als grijs wanneer de configuratieopties worden weergegeven:

   * Cohortingtabel

   * Reiscanvas

   * Opsommingsteken

   * Combo

   * Spreiding

   * Treemap

* Uitsplitsingen

* Analyses met instructies


