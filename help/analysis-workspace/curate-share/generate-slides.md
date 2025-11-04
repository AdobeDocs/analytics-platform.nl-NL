---
description: Leer hoe u presentaties in pptx-indeling kunt genereren op basis van Workspace-rapporten.
keywords: Analysis Workspace
title: Presentaties genereren op basis van Workspace-rapporten
feature: Curate and Share
role: User
source-git-commit: 87e3b3cfdf765a57ecdb70921696013bcba4feac
workflow-type: tm+mt
source-wordcount: '1524'
ht-degree: 0%

---

# Gegevensverhaal: presentaties genereren op basis van Workspace-rapporten {#generate-powerpoint}

{{release-limited-testing}}

<!-- also remove lmited testing note from: /help/technotes/access-control.md -->

De gebruikers met [&#x200B; de noodzakelijke toestemmingen &#x200B;](#permission-requirements-to-generate-slides) kunnen .pptx presentaties automatisch produceren die op de projecten van Analysis Workspace worden gebaseerd. Bij het genereren van deze diapresentaties maakt Customer Journey Analytics automatisch een artikel op basis van uw gegevens door belangrijke inzichten te identificeren en deze om te zetten in dia&#39;s die klaar zijn voor gebruik door belanghebbenden.

Dit gegenereerde gegevensverhaal verkort de tijd, moeite en expertise die nodig is om bevindingen van een Workspace-project te onthullen. Analysten kunnen zich meer richten op gegevensexploratie, terwijl het toestaan van Customer Journey Analytics om het uitvoerende verhaal te bouwen en te formatteren en het bedrijfseffect aan belanghebbenden mee te delen.

## Gegevensartikelen in diapresentaties begrijpen

A **gegevensverhaal** is het verhaal dat Customer Journey Analytics creeert gebaseerd op uw gegevens van Workspace. Met behulp van generatieve AI identificeert Customer Journey Analytics belangrijke thema&#39;s in de deelvensters en visualisaties die u in uw presentatie wilt opnemen. Het produceert inzichten, dan gaat door een deduplicatie en het scoring proces om een ondergroep van inzichten te identificeren om het gegevensverhaal tot stand te brengen.

De volgende secties beschrijven de extra waarde die gegevensverhalen verstrekken, de noodzakelijke elementen van een project die helpen het verhaal, en belangrijkste elementen vormen die in de .pptx presentatieoutput inbegrepen zijn.

### Aanvullende waarde die wordt verschaft door gegevensartikelen

Gegevensartikelen bieden waarde en inzichten aan een Workspace-project door gegevens toegankelijk te maken voor gebruikers die minder ervaring hebben met gegevensanalyse.

Gegevensverhalen vullen een analyse voor een bepaald Workspace-project aan door:

* Aanvullende context bieden

* Belangrijke inzichten benadrukken

* Bepalen of bepaalde variabelen ondergewaardeerd of overgewaardeerd zijn

* Verborgen trends, anomalieën en andere factoren die bijdragen tot de ontwikkeling van

* Het geven van ideeën voor volgende stappen

### Projectelementen die gegevensartikelen vormen

Analysis Workspace maakt gegevensartikelen door de volgende projectelementen in overweging te nemen:

* Interdimensionale en intermetrische relaties

* De afzonderlijke elementen die de basis vormen van de analyse (afmetingen, metriek, filters, vrije tabelstructuur, visualisaties en deelvensters)

* De namen die aan de deelvensters, tabellen en visualisaties worden gegeven

* De volgorde van metriek in een vrije-vormlijst (om prioriteit te bepalen)

* De volgorde van visualisaties in een deelvenster (om de prioriteit te bepalen)

* Samenvattingsnummers en samenvattingsteksten (om de metriek te bepalen die in het gegevensartikel moet worden gemarkeerd)

### Presentatie-elementen van een gegevensartikel

De artikelen van gegevens bestaan uit een titeldia, een overzichtsdia, detaildia&#39;s, en sectieverdelers.

**de dia van de Titel:** toont de titel en presentatornaam die u specificeert. De informatie toont in de spreker dat beschrijft hoe het thema en het verhaal werden gecreeerd, hoeveel inzichten werden geproduceerd en werden gebruikt, en welke panelen werden gebruikt.

**Uitvoerende samenvatting:** geeft voorrang aan de hoogste-waardeinzichten en creeert een overkoepelend verhaal dat tussen 1 en 5 zinnen in lengte is.

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

   ![&#x200B; produceer de dialoog van dia&#39;s &#x200B;](assets/generate-slides.png)

1. Geef de volgende informatie op:

   | Optie | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Cover title]** | Geef een titel op voor de presentatie. Deze titel wordt weergegeven op de titeldia van de presentatie. |
   | **[!UICONTROL Include presenter name]** | Geef de naam van de presentator op. Deze naam wordt weergegeven op de titeldia van de presentatie, onder de titel van de omslag. |
   | **[!UICONTROL Panels and visualizations to include]** | Kies de deelvensters en de visualisatie die u in de presentatie wilt opnemen. U kunt maximaal 50 visualisaties opnemen.<p>Als een visualisatie grijs wordt weergegeven, wordt deze gevolgd door de tekst **[!UICONTROL (unsupported)]** of **[!UICONTROL (restricted data)]** .</p><ul><li>**Niet gestaafd**: De meeste panelen en visualisaties worden gesteund. Voor informatie over niet gestaafde panelen en visualisatie, zie [&#x200B; Niet gestaafde projectelementen en eigenschappen &#x200B;](#unsupported-project-elements-and-features).</li><li>**Beperkte gegevens**: De visualisatie bevat een component die van wordt uitgevoerd door een beleid van het gegevensbeheer wordt beperkt dat door uw organisatie wordt afgedwongen. Neem contact op met de systeembeheerder om te zien welke componenten niet mogen worden geëxporteerd en verwijder vervolgens de beperkte componenten voordat u dia&#39;s genereert.</li></ul> |
   | **[!UICONTROL Emphasize components]** | Kies de meetgegevens en de afmetingen in uw visualisaties die u wilt benadrukken in de presentatie. De componenten die u kiest, krijgen een hogere positie en krijgen meer gewicht wanneer de thema&#39;s en het overkoepelende verhaal van het gegevensartikel worden gemaakt. <p>Wanneer geen nadruk wordt toegepast, tonen de componenten in presentaties als volgt:<ul><li>**Metriek en afmetingen:** Cursief</li><li>**de punten van Dimension:** Citatietekens</li></ul></p><p>Wanneer de nadruk wordt toegepast, tonen de componenten in presentaties als volgt:</p><ul><li>**Metriek en afmetingen:** Cursief en gewaagd</li><li>**de punten van Dimension:** Vet wanneer de overeenkomstige afmeting wordt benadrukt<p>Er wordt ook een kleur toegepast op het dimensie-item wanneer het dimensie-item in het diagram wordt gemarkeerd.</p></li></ul> |

   <!-- add this later: - **[!UICONTROL Panel and visualization descriptions]** - Choose whether to include panel and visualization descriptions in your generated slide presentation. - 
   - **[!UICONTROL Annotations]** - Choose whether annotations are visible in your generated slide presentation. For more information about annotations, see [Annotations overview](/help/components/annotations/overview.md).  -  -->

1. (Voorwaardelijk) Selecteer **[!UICONTROL Default theme]** als u dia&#39;s in minder stappen wilt genereren en als een bedrijfsthema niet vereist is voor uw presentatie.

   Kies gewoon het kleurthema van uw presentatie door de gewenste kleur te selecteren.

   ![&#x200B; produceer dia&#39;s met het standaardthema &#x200B;](assets/generate-slides-default-theme.png)

1. (Voorwaardelijk) Selecteer **[!UICONTROL Upload template]** als uw diapresentatie moet overeenkomen met een bedrijfsthema. Voor deze optie moet u een aangepaste sjabloon uploaden en aangepaste stijlen toepassen.

   De meest recente aangepaste sjabloon die u uploadt, wordt lokaal opgeslagen in de cache van uw browser en is beschikbaar wanneer u toekomstige diapresentaties genereert.

   ![&#x200B; produceer dia&#39;s met een douanemalplaatje &#x200B;](assets/generate-slides-upload-template.png)

   Voer een van de volgende twee handelingen uit om een aangepaste sjabloon te uploaden:

   * (Aanbevolen) Download een lege sjabloon en wijzig deze.

      1. Download [&#x200B; dit lege malplaatje &#x200B;](https://d30ln29764hddd.cloudfront.net/deploy/builds/data-storytelling.2025-10-20T15:10:19/resources/components/Blank.potx?).

      1. Pas uw aangepaste stijlen toe op de lege sjabloon.

      1. Upload de sjabloon opnieuw zonder de namen van de stramienlay-outs te wijzigen:

         Sleep vanuit het bestandssysteem de lege sjabloon waarop uw aangepaste stijlen zijn toegepast op het neerzetgebied.

         of

         Selecteer **[!UICONTROL Browse]** en blader naar de lege sjabloon waarop uw aangepaste stijlen zijn toegepast vanuit het bestandssysteem.

      1. In de sectie **[!UICONTROL Layout mapping]** wordt elke dialay-out die wordt gebruikt in gegenereerde presentaties, automatisch toegewezen aan een dia van het geüploade thema. Controleer de selecties om er zeker van te zijn dat deze correct zijn.

         ![&#x200B; afbeelding van de Lay-out &#x200B;](assets/generate-slides-layout-mapping.png)

      1. (Voorwaardelijk) Als een dialay-out onjuist is toegewezen, selecteert u **[!UICONTROL Change selection]** boven de dia die u hebt gekozen uit uw geüploade presentatie en kiest u de dia die overeenkomt met de lay-out.

         Herhaal dit proces voor elke dia die onjuist is toegewezen.

   * Een aangepaste sjabloon rechtstreeks uploaden.

      1. Sleep de aangepaste sjabloon vanuit het bestandssysteem naar het neerzetgebied.

         of

         Selecteer **[!UICONTROL Browse]** en blader naar de aangepaste sjabloon in het bestandssysteem en selecteer deze.

         Zorg ervoor dat het geüploade bestand stramienindelingen heeft met de volgende namen: &quot;Title_Slide,&quot; &quot;Section_Divider,&quot; &quot;Title_Text,&quot; &quot;Title_Chart,&quot; &quot;Title_Two_Content_Mixed,&quot; &quot;Title_Three_Content_Mixed.&quot;

         Er worden maximaal 15 stramienlay-outs ondersteund.

         .pptx- en .potx-bestanden van maximaal 25 MB worden ondersteund.

      1. In de sectie **[!UICONTROL Layout mapping]** wordt elke dialay-out die wordt gebruikt in gegenereerde presentaties, automatisch toegewezen aan een dia van het geüploade thema. Controleer de selecties om er zeker van te zijn dat deze correct zijn.

         ![&#x200B; Lay-out die douanemalplaatje &#x200B;](assets/generate-slides-layout-mapping-custom-template.png) in kaart brengt

      1. (Voorwaardelijk) Als een dialay-out onjuist is toegewezen, selecteert u **[!UICONTROL Change selection]** boven de dia die u hebt gekozen uit uw geüploade presentatie en kiest u de dia die overeenkomt met de lay-out.

         Herhaal dit proces voor elke dia die onjuist is toegewezen.

1. Selecteer **[!UICONTROL Export PPT]**.

   De .pptx-presentatie wordt automatisch naar uw werkstation gedownload.

1. (Aanbevolen) Open de .pptx-presentatie en bekijk deze. Breng de gewenste wijzigingen aan.

## Vereisten voor machtigingen om dia&#39;s te genereren

>[!AVAILABILITY]
>
>Als uw organisatie geen toegang heeft om diapresentaties te genereren op basis van een Workspace-project, neemt u contact op met uw Adobe-accountvertegenwoordiger voor meer informatie over licenties.

De mogelijkheid om dia&#39;s te genereren is standaard ingeschakeld voor alle gebruikers in organisaties die over de vereiste licenties beschikken.

Beheerders van productprofielen waarvan organisaties licenties hebben om dia&#39;s te genereren, kunnen de toegang indien nodig uitschakelen.

In [!UICONTROL Adobe Admin Console] bepaalt de machtiging [!UICONTROL Reporting Tools] **[!UICONTROL Data storytelling]** de toegang tot deze mogelijkheid. A [&#x200B; beheer van het productprofiel &#x200B;](https://helpx.adobe.com/nl/enterprise/using/manage-product-profiles.html) moet deze stappen in [!UICONTROL Admin Console] volgen als zij toegang willen onbruikbaar maken:
1. Ga naar **[!UICONTROL Admin Console]** > **[!UICONTROL Products and services]** > **[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Product Profiles]**
1. Selecteer de titel van het productprofiel waartoe u toegang wilt verlenen aan [!UICONTROL Data storytelling] .
1. Selecteer **[!UICONTROL Permissions]** in het specifieke productprofiel.
1. Selecteer ![&#x200B; uitgeven &#x200B;](/help/assets/icons/Edit.svg) om uit te geven **[!UICONTROL Reporting Tools]**.
1. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/RemoveCircle.svg) om **het verhaal van Gegevens** uit **[!UICONTROL Included permission items]** te verwijderen.

   <!--add screenshot of permission in the admin console-->

1. Selecteer **[!UICONTROL Save]** om de machtigingen op te slaan.

Voor meer informatie, zie [&#x200B; gebruiker-vlakke toegang &#x200B;](/help/technotes/access-control.md#user-level-access) in [&#x200B; controle van de Toegang &#x200B;](/help/technotes/access-control.md#access-control) voor meer informatie.

## Niet-ondersteunde projectelementen en -functies {#unsupported}

De volgende Analysis Workspace-elementen en -functies die in een project worden gebruikt, worden niet ondersteund bij het genereren van dia&#39;s:

* Kenmerk, deelvenster

  Dit deelvenster wordt zo gedimd weergegeven wanneer de configuratieopties worden weergegeven.

  Alle andere panelen kunnen in dia&#39;s worden omvat die van een project van Workspace worden geproduceerd.

* Sommige visualisaties

  De meeste visualisaties kunnen in dia&#39;s worden omvat die van een project van Workspace worden geproduceerd. De volgende visualisaties kunnen echter niet worden opgenomen en worden weergegeven als grijs wanneer de configuratieopties worden weergegeven:

   * Gebied

   * Opsommingsteken

   * Cohortingtabel

   * Combo

   * Fallout

   * Stroom

   * Reiscanvas

   * Spreiding

   * Treemap

* Uitsplitsingen

  De gegevens voor uitsplitsingen worden opgenomen in gegenereerde presentaties, maar worden op hetzelfde niveau weergegeven als dimensiepunten.

* Analyses met instructies

* Componenten die niet kunnen worden geëxporteerd door een beleid voor gegevensbeheer

  Voor meer informatie, zie [&#x200B; Problemen ontbroken uitvoer &#x200B;](/help/components/exports/troubleshoot-exports.md) oplossen.


