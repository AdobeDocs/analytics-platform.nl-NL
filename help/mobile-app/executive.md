---
description: Instructies voor het gebruik van de dashboards scorecards.
title: Uitvoeringshandleiding voor analytische dashboards
feature: Analytics Dashboards
role: User, Admin
exl-id: 12901a76-cb88-45a5-81e9-59fb310328be
solution: Customer Journey Analytics
source-git-commit: c343a729de4cb13473a7acc04e837b5e5f69809b
workflow-type: tm+mt
source-wordcount: '1285'
ht-degree: 0%

---

# Snelle handleiding voor executive gebruikers

De volgende informatie verstrekt uitvoerende gebruikers van informatie over beste praktijken voor het gebruiken van en het bekijken van de dashboards van Analytics. Hier volgt een video waarin deze informatie wordt getoond:

>[!VIDEO](https://video.tv.adobe.com/v/343460/)

Deze gids is bedoeld om uitvoerende gebruikers te helpen scorecards op de dashboards van Analytics lezen en interpreteren. Met de app kunnen uitvoerende gebruikers snel en gemakkelijk een brede weergave van belangrijke samenvattingsgegevens op hun eigen mobiele apparaten bekijken.

## Stel dashboards in op uw apparaat

Om de dashboards effectief te gebruiken, zult u uw hulp van de Curator van het Scorecard moeten hebben u opstelling het. In dit gedeelte vindt u informatie die u helpt bij het instellen van uw curator.

### Toegang verkrijgen

Als u toegang wilt tot scoreborden op dashboards, moet u ervoor zorgen dat:

* U hebt een geldige aanmelding bij Customer Journey Analytics
* Uw curator heeft op de juiste wijze mobiele scoreborden gemaakt en deze met u gedeeld

### Dashboards downloaden en installeren

Voer de stappen uit volgens het besturingssysteem op uw apparaat om de app te downloaden en installeren.

>[!NOTE]
>
>Hoewel de mobiele app in de App Store de naam Adobe Analytics-dashboard heeft, kan de app ook worden gebruikt bij mobiele scorecards voor Customers Journey Analytics.

**Voor uitvoerende gebruikers op iOS:**

Klik op de volgende koppeling (deze is ook beschikbaar in de Customer Journey Analytics onder **[!UICONTROL Tools]** > **[!UICONTROL Analytics dashboards (mobile app)]**) en volgt u de aanwijzingen om de app te downloaden, installeren en openen:

[iOS-koppeling](https://apple.co/2zXq0aN)

**Voor uitvoerende gebruikers op Android:**

Klik op de volgende koppeling (deze is ook beschikbaar in de Customer Journey Analytics onder **[!UICONTROL Tools]** > **[!UICONTROL Analytics dashboards (mobile app)]**) en volgt u de aanwijzingen om de app te downloaden, installeren en openen:

[Android-koppeling](https://bit.ly/2LM38Oo)

Zodra ze zijn gedownload en geïnstalleerd, kunnen gebruikers zich aanmelden bij de app met hun bestaande Customer Journey Analytics.

![Welkomstscherm van Customer Journey Analytics-app](assets/welcome.png)

## Dashboards gebruiken {#use-dashboards}

U kunt als volgt dashboards gebruiken:

1. Meld u aan bij de app. Het aanmeldingsscherm wordt weergegeven wanneer u dashboards start. Volg de aanwijzingen op basis van de bestaande referenties van de Customer Journey Analytics. Wij ondersteunen zowel Adobe als Enterprise/Federated ID&#39;s.

   ![Volgorde aanmelden](assets/signseq.png)

1. Kies een bedrijf. Nadat u zich hebt aangemeld bij de dashboards, worden de **[!UICONTROL Choose a company]** wordt weergegeven. Dit scherm maakt een lijst van de login bedrijven waartot u behoort. Tik op de bedrijfsnaam die is gekoppeld aan de scorecard die met u wordt gedeeld.

   De scorecard lijst toont alle scorecards die met u worden gedeeld.

1. Tik op de scorecard die u wilt weergeven.

   Als u toegang tot meer dan één organisatie onder één login hebt, zijn alle scorecards van uw organisaties beschikbaar in de scorecard lijst.

   U kunt de scorecardlijst sorteren op scorecardtitel, organisatienaam, of onlangs bekeken. U kunt zelfs naar een specifieke scorecard zoeken.

   ![Kies een bedrijf](assets/mobile-home-screen.png)

   Als u zich aanmeldt en een bericht ziet waarin wordt gemeld dat er niets is gedeeld, controleert u het volgende met uw curator:

   * U kunt zich aanmelden bij de juiste Customer Journey Analytics-sandbox.
   * Het scorebord is met u gedeeld.

   ![Niets gedeeld](assets/nothing.png)

1. Onderzoek hoe de tegels in Scorecard verschijnen (het eerste Scorecard wordt getoond in donkere wijze; zie **[!UICONTROL Preferences]** hieronder voor meer informatie ) .

   ![Getegrafeerde tegels](assets/newexplain.png)

   Aanvullende informatie over tegels:

   * De korreligheid van de sparklines is afhankelijk van de lengte van het datumbereik:

      * Op een dag is er een uurtrend
      * Meer dan een dag en minder dan een jaar laten een dagelijkse trend zien
      * Een jaar of langer toont een wekelijkse trend

   * De formule van de percentagewaardeverandering is metrisch totaal (huidige datumwaaier) - metrisch totaal (de waaier van de vergelijkingsdatum) / metrisch totaal (de waaier van de vergelijkingsdatum).

   * U kunt het scherm omlaag trekken om het Scorecard te vernieuwen.

   Het volgende voorbeeldscorebord wordt getoond in normale wijze:

   ![Voorbeeld van scorebord](assets/intro_scorecard.png)

1. Tik op een tegel om te zien hoe een gedetailleerde uitsplitsing van de tegel werkt.

   ![Weergave Schaduwen](assets/sparkline.png)


1. U wijzigt de datumbereiken voor uw scorebord als volgt:

   ![Datums wijzigen](assets/changedate.png)

   * U kunt de datumbereiken ook op dezelfde manier wijzigen in de bovenstaande uitsplitsingsweergave.

   * Afhankelijk van het interval dat u tikt (**Dag**, **Week**, **Maand**, of **Jaar**), ziet u twee opties voor datumbereiken—ofwel de huidige tijdsperiode of de reeks die er direct aan voorafgaat. Tik op een van deze twee opties om het eerste bereik te selecteren. Onder de **[!UICONTROL COMPARE TO]** tikt u op een van de voorgestelde opties om de gegevens van deze tijdsperiode te vergelijken met de gegevens van het eerste datumbereik dat u hebt geselecteerd. Tikken **[!UICONTROL Done]** rechtsboven in het scherm. De **[!UICONTROL Date Ranges]** worden de nieuwe vergelijkingsgegevens uit de nieuwe bereiken die u hebt geselecteerd, bijgewerkt met de scorebordtegels.

1. Als u een segmentfilter op uw scorebord wilt toepassen, tikt u op de vervolgkeuzelijst met filters en selecteert u een segment dat door de curator is geconfigureerd. [Filters](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html) in de app werken op dezelfde manier als in Workspace.

   ![Segment, filter](assets/segment_filter.png)

1. Download de Scorecard-updates. Als een Scorecard niet alle metrisch of onderverdelingen omvat die u in kunt geinteresseerd zijn, gelieve uw team van de Customer Journey Analytics te contacteren om Scorecard te hebben bijgewerkt. Na de update kunt u de kaart op het scherm terugtrekken om deze te vernieuwen en de onlangs toegevoegde gegevens te laden.

1. Feedback geven op deze app:

   1. Tik op het instellingenpictogram rechtsboven in het toepassingsscherm.
   2. Op de **[!UICONTROL Settings]** scherm tikken, tikken op **[!UICONTROL Feedback]** -optie.
   3. Tik om de opties voor het geven van feedback weer te geven.

      ![Instellingenscherm](assets/settings.png)

1. Tik op de knop **[!UICONTROL Preferences]** hierboven weergegeven. Bij de voorkeuren kunt u de biometrische aanmelding inschakelen of de app voor de donkere modus instellen, zoals hieronder wordt weergegeven:

   ![Donkere modus](assets/darkmode.png)


**Een fout rapporteren**:

Tik op de optie en kies een subcategorie van de bug. Geef in het formulier voor het melden van een fout uw e-mailadres op in het bovenste veld en uw beschrijving van de fout op in het veld eronder. Er wordt automatisch een schermafbeelding van uw accountgegevens aan het bericht toegevoegd, maar u kunt dit desgewenst verwijderen door op de knop **X** in de bijlage. U hebt ook opties voor het opnemen van een scherm, het toevoegen van meer schermafbeeldingen of het bijvoegen van bestanden. Tik op het pictogram van het papieren vlak rechtsboven in het formulier om het rapport te verzenden.

![Fout rapporteren](assets/newbug.png)

**Om een verbetering voor te stellen**:

Tik op de optie en kies een subcategorie voor de suggestie. Geef in het aanvraagformulier uw e-mailadres op in het bovenste veld en uw beschrijving van de fout op in het veld eronder. Er wordt automatisch een schermafbeelding van uw accountgegevens aan het bericht toegevoegd, maar u kunt dit desgewenst verwijderen door op de knop **X** in de bijlage. U hebt ook opties voor het opnemen van een scherm, het toevoegen van meer schermafbeeldingen of het bijvoegen van bestanden. Tik op het pictogram van het papieren vlak rechtsboven in het formulier om de suggestie te verzenden.

**Een vraag stellen**:

Tik op de optie en geef uw e-mailadres op in het bovenste veld en uw vraag in het veld eronder. Er wordt automatisch een schermafbeelding aan het bericht gekoppeld, maar u kunt dit desgewenst verwijderen door op de knop **X** in de bijlage. U hebt ook opties voor het opnemen van een scherm, het toevoegen van meer schermafbeeldingen of het bijvoegen van bestanden. Tik op het pictogram van het papieren vlak rechtsboven in het formulier om de vraag te verzenden.

## Verklarende woordenlijst

| Term | Definitie |
|--- |--- |
| Consumenten | Executive-gebruiker die belangrijke metriek en inzichten van Customer Journey Analytics op een mobiel apparaat bekijkt |
| Curator | De gegevens schrijven mensen voor die inzicht van Customer Journey Analytics vinden en verspreiden en de Scorecards vormen die door de consument moeten worden bekeken |
| Curation | Het creëren of bewerken van een mobiele scorecard met relevante meetgegevens, afmetingen en andere componenten voor de consument |
| Scorecard | Een dashboardweergave met een of meer tegels |
| Tegel | Een rendering voor metrische gegevens in een scorebordweergave |
| Uitsplitsing | Een secundaire weergave die toegankelijk is door te tikken op een tegel in het scorebord. Deze mening breidt metrisch uit die op de tegel wordt getoond en naar keuze rapporten over extra verdelingsafmetingen. |
| Datumbereik | Het primaire datumbereik voor dashboardrapportage |
| Vergelijkingsdatumbereik | Het datumbereik dat wordt vergeleken met het primaire datumbereik |
