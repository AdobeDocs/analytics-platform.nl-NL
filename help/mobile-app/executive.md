---
description: Instructies voor het gebruik van de dashboards scorecards.
title: Uitvoeringshandleiding voor analytische dashboards
feature: Analytics Dashboards
role: User
exl-id: 12901a76-cb88-45a5-81e9-59fb310328be
solution: Customer Journey Analytics
source-git-commit: f03c82375a907821c8e3f40b32b4d4200a47323f
workflow-type: tm+mt
source-wordcount: '1273'
ht-degree: 0%

---

# Snelle handleiding voor gebruikers

De volgende informatie verstrekt uitvoerende gebruikers van informatie over beste praktijken voor het gebruiken van en het bekijken van de dashboards van Analytics.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ stafmedewerkers bijstaan om tot mobiele scorecards ](https://video.tv.adobe.com/v/3444842?captions=dut){target="_blank"} voor een demo video toegang te hebben.

>[!ENDSHADEBOX]

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
>Hoewel de mobiele app in de App Store de naam Adobe Analytics-dashboard heeft, kan de app ook worden gebruikt met mobiele Customer Journey Analytics-scorecards.

**voor uitvoerende gebruikers op iOS:**

Klik op de volgende koppeling (deze is ook beschikbaar in Customer Journey Analytics onder **[!UICONTROL Tools]** > **[!UICONTROL Analytics dashboards (mobile app)]** ) en volg de instructies om de app te downloaden, installeren en openen:

[ verbinding van iOS ](https://apple.co/2zXq0aN)

**voor uitvoerende gebruikers op Android:**

Klik op de volgende koppeling (deze is ook beschikbaar in Customer Journey Analytics onder **[!UICONTROL Tools]** > **[!UICONTROL Analytics dashboards (mobile app)]** ) en volg de instructies om de app te downloaden, installeren en openen:

[ verbinding van Android ](https://bit.ly/2LM38Oo)

Zodra ze zijn gedownload en geïnstalleerd, kunnen gebruikers zich aanmelden bij de app met hun bestaande Customer Journey Analytics-referenties.

![ Customer Journey Analytics app welkomstscherm ](assets/welcome.png)

## Dashboards gebruiken {#use-dashboards}

U kunt als volgt dashboards gebruiken:

1. Meld u aan bij de app. Het aanmeldingsscherm wordt weergegeven wanneer u dashboards start. Volg de aanwijzingen op basis van uw bestaande Customer Journey Analytics-gebruikersgegevens. Wij ondersteunen zowel Adobe- als Enterprise-/federatieve id&#39;s.

   ![ Teken in opeenvolging ](assets/signseq.png)

1. Kies een bedrijf. Nadat u zich hebt aangemeld bij dashboards, wordt het scherm **[!UICONTROL Choose a company]** weergegeven. Dit scherm maakt een lijst van de login bedrijven waartot u behoort. Tik op de bedrijfsnaam die is gekoppeld aan de scorecard die met u wordt gedeeld.

   De scorecard lijst toont alle scorecards die met u worden gedeeld.

1. Tik op de scorecard die u wilt weergeven.

   Als u toegang tot meer dan één organisatie onder één login hebt, zijn alle scorecards van uw organisaties beschikbaar in de scorecard lijst.

   U kunt de scorecardlijst sorteren op scorecardtitel, organisatienaam, of onlangs bekeken. U kunt zelfs naar een specifieke scorecard zoeken.

   ![ kies een bedrijf ](assets/mobile-home-screen.png)

   Als u zich aanmeldt en een bericht ziet waarin wordt gemeld dat er niets is gedeeld, controleert u het volgende met uw curator:

   * U kunt zich aanmelden bij de juiste Customer Journey Analytics-sandbox.
   * Het scorebord is met u gedeeld.

   ![ niets gedeelde ](assets/nothing.png)

1. Onderzoek hoe de tegels in Scorecard verschijnen (het eerste Scorecard wordt getoond in donkere wijze; zie **[!UICONTROL Preferences]** hieronder voor meer informatie).

   ![ verklaarde Tegels ](assets/newexplain.png)

   Aanvullende informatie over tegels:

   * De korreligheid van de sparklines is afhankelijk van de lengte van het datumbereik:

      * Op een dag is er een uurtrend
      * Meer dan een dag en minder dan een jaar laten een dagelijkse trend zien
      * Een jaar of langer toont een wekelijkse trend

   * De formule van de percentagewaardeverandering is metrisch totaal (huidige datumwaaier) - metrisch totaal (de waaier van de vergelijkingsdatum) / metrisch totaal (de waaier van de vergelijkingsdatum).

   * U kunt het scherm omlaag trekken om het Scorecard te vernieuwen.

   Het volgende voorbeeldscorebord wordt getoond in normale wijze:

   ![ Scorecard van het Voorbeeld ](assets/intro_scorecard.png)

1. Tik op een tegel om te zien hoe een gedetailleerde uitsplitsing van de tegel werkt.

   ![ mening van de Schaduw ](assets/sparkline.png)


1. U wijzigt de datumbereiken voor uw scorebord als volgt:

   ![ data van de Verandering ](assets/changedate.png)

   * U kunt de datumbereiken ook op dezelfde manier wijzigen in de bovenstaande uitsplitsingsweergave.

   * Afhankelijk van het interval u tikt (**Dag**, **Week**, **Maand**, of **Jaar**), zult u twee opties voor datum bereiken-of de huidige spanwijdte van tijd of onmiddellijk voorafgaand aan het zien. Tik op een van deze twee opties om het eerste bereik te selecteren. Tik in de lijst **[!UICONTROL COMPARE TO]** op een van de opties die worden weergegeven om de gegevens van deze tijdsperiode te vergelijken met de gegevens van het eerste datumbereik dat u hebt geselecteerd. Tik op **[!UICONTROL Done]** rechtsboven in het scherm. De velden **[!UICONTROL Date Ranges]** en Scorecard worden bijgewerkt met de nieuwe vergelijkingsgegevens uit de nieuwe bereiken die u hebt geselecteerd.

1. Als u een segment wilt toepassen op uw scorebord, tikt u op het vervolgkeuzemenu voor segmenten en selecteert u een segment dat door de curator is geconfigureerd. [ Segmenten ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html?lang=nl-NL) in app functioneren de zelfde manier zij in Workspace doen.

   ![ Segment ](assets/segment_filter.png)

1. Download [!UICONTROL Scorecard] updates. Als een [!UICONTROL Scorecard] niet alle metrische gegevens of uitsplitsingen bevat waarin u wellicht geïnteresseerd bent, neemt u contact op met uw Customer Journey Analytics-team om het scorebord bij te werken. Na de update kunt u de kaart op het scherm terugtrekken om deze te vernieuwen en de onlangs toegevoegde gegevens te laden.

1. Feedback geven op deze app:

   1. Tik op het instellingenpictogram rechtsboven in het toepassingsscherm.
   2. Tik op het **[!UICONTROL Settings]** -scherm op de optie **[!UICONTROL Feedback]** .
   3. Tik om de opties voor het geven van feedback weer te geven.

      ![ het scherm van Montages ](assets/settings.png)

1. Tik op de bovenstaande optie **[!UICONTROL Preferences]** om de voorkeuren te wijzigen. Bij de voorkeuren kunt u de biometrische aanmelding inschakelen of de app voor de donkere modus instellen, zoals hieronder wordt weergegeven:

   ![ Donkere wijze ](assets/darkmode.png)


**om een insect** te melden:

Tik op de optie en kies een subcategorie van de bug. Geef in het formulier voor het melden van een fout uw e-mailadres op in het bovenste veld en uw beschrijving van de fout op in het veld eronder. Een het schermschot van uw rekeningsinfo wordt automatisch in bijlage aan het bericht, maar u kunt dit schrappen als u wilt door **X** in het gehechtheidsbeeld te tikken. U hebt ook opties voor het opnemen van een scherm, het toevoegen van meer schermafbeeldingen of het bijvoegen van bestanden. Tik op het pictogram van het papieren vlak rechtsboven in het formulier om het rapport te verzenden.

![ bug van het Rapport ](assets/newbug.png)

**om een verbetering** voor te stellen:

Tik op de optie en kies een subcategorie voor de suggestie. Geef in het aanvraagformulier uw e-mailadres op in het bovenste veld en uw beschrijving van de fout op in het veld eronder. Een het schermschot van uw rekeningsinfo wordt automatisch in bijlage aan het bericht, maar u kunt dit schrappen als u wilt door **X** in het gehechtheidsbeeld te tikken. U hebt ook opties voor het opnemen van een scherm, het toevoegen van meer schermafbeeldingen of het bijvoegen van bestanden. Tik op het pictogram van het papieren vlak rechtsboven in het formulier om de suggestie te verzenden.

**om een vraag** te stellen:

Tik op de optie en geef uw e-mailadres op in het bovenste veld en uw vraag in het veld eronder. Een het schermschot wordt automatisch in bijlage aan het bericht, maar u kunt dit schrappen als u door **X** in het gehechtheidsbeeld te tikken wilt. U hebt ook opties voor het opnemen van een scherm, het toevoegen van meer schermafbeeldingen of het bijvoegen van bestanden. Tik op het pictogram van het papieren vlak rechtsboven in het formulier om de vraag te verzenden.

## Verklarende woordenlijst

| Term | Definitie |
|--- |--- |
| Consumenten | Executive-gebruiker die belangrijke metriek en inzichten van Customer Journey Analytics op een mobiel apparaat bekijkt |
| Curator | Personeelsleden die inzichten van Customer Journey Analytics vinden en verspreiden en de Scorecards configureren die door de consument moeten worden bekeken |
| Curation | Het creëren of bewerken van een mobiele scorecard met relevante meetgegevens, afmetingen en andere componenten voor de consument |
| Scorecard | Een dashboardweergave met een of meer tegels |
| Tegel | Een rendering voor metrische gegevens in een scorebordweergave |
| Uitsplitsing | Een secundaire weergave die toegankelijk is door te tikken op een tegel in het scorebord. Deze mening breidt metrisch uit die op de tegel wordt getoond en naar keuze rapporten over extra verdelingsafmetingen. |
| Datumbereik | Het primaire datumbereik voor dashboardrapportage |
| Vergelijkingsdatumbereik | Het datumbereik dat wordt vergeleken met het primaire datumbereik |
