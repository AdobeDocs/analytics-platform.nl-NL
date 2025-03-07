---
description: Gebruikers instellen om de mobiele app Adobe Analytics te gebruiken
title: Stel managers in voor het gebruik van dashboards
feature: Analytics Dashboards
role: User, Admin
exl-id: 647f192a-e317-4011-92bc-a8bb8494a3c7
solution: Customer Journey Analytics
source-git-commit: d8286e34edba128113ba99602ba24eea67c5dea8
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Uitvoerende gebruikers instellen voor het gebruik van dashboards

In sommige gevallen hebben uitvoerende gebruikers wellicht extra hulp nodig om de app te openen en te gebruiken. Deze sectie verstrekt informatie om curators te helpen die hulp verstrekken.

## Zorg ervoor dat gebruikers van apps toegang hebben tot Adobe Analytics

1. Opstelling nieuwe gebruikers in [ Experience Cloud Admin Console ](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html).

1. Om scorecards te kunnen delen, moet u app gebruikers toestemmingen verlenen om tot scorecard componenten zoals Analysis Workspace, de gegevensmeningen toegang te hebben die scorecards, evenals segmenten, metriek en dimensies gebaseerd zijn.

## Systeemvereisten voor gebruikers van de app

Om ervoor te zorgen dat de uitvoerende gebruikers toegang tot uw scorecards op app hebben, zorg ervoor dat:

* De minimale mobiele besturingssysteemvereisten op hun apparaten zijn iOS versie 10 of hoger, of Android versie 4.4 (KitKat) of hoger
* Ze hebben een geldige aanmelding bij Customer Journey Analytics.
* U hebt op de juiste wijze mobiele scorecards voor hen gemaakt en deze scorecards met hen gedeeld.
* Zij hebben toegang tot de Componenten die scorecard omvat. U kunt een optie selecteren wanneer u uw scorecards deelt naar **[!UICONTROL Share embedded components]** .

## Help-managers om app te downloaden en installeren

>[!NOTE]
>
>Hoewel de mobiele app in de App Store de naam Adobe Analytics-dashboard heeft, kan de app ook worden gebruikt met mobiele Customer Journey Analytics-scorecards.

**voor uitvoerende gebruikers op iOS:**

Klik op de volgende koppeling (deze is ook beschikbaar in Customer Journey Analytics onder **[!UICONTROL Tools]** > **[!UICONTROL Analytics dashboards (mobile opp)]** ) en volg de instructies om de app te downloaden, installeren en openen:

`[iOS link](https://apple.co/2zXq0aN)`

**voor uitvoerende gebruikers op Android:**

Klik op de volgende koppeling (deze is ook beschikbaar in Customer Journey Analytics onder **[!UICONTROL Tools]** > **[!UICONTROL Analytics dashboards (mobile app)]** ) en volg de instructies om de app te downloaden, installeren en openen:

`[Android link](https://bit.ly/2LM38Oo)`

Zodra ze zijn gedownload en geïnstalleerd, kunnen uitvoerende gebruikers zich aanmelden bij de app met hun bestaande Customer Journey Analytics-referenties; we ondersteunen zowel Adobe- als Enterprise/Federated-id&#39;s.

![ Adobe Analytics dashboards welkomstscherm ](assets/welcome.png)

## Help managers toegang te krijgen tot uw scorecard

1. Gebruikers met een zelfstudie moeten zich aanmelden bij de app.

   Het scherm **[!UICONTROL Choose a company]** wordt weergegeven. Dit scherm maakt een lijst van de login bedrijven waartot de uitvoerende gebruiker behoort.

1. Laat ze op de naam van het aanmeldingsbedrijf of Experience Cloud Org tikken die van toepassing is op de scorecard die u hebt gedeeld.

   De Scorecard lijst toont dan alle scorecards die met het uitvoerend onder dat login bedrijf zijn gedeeld.

1. Deze lijst op **[!UICONTROL Most recently modified]** sorteren, indien van toepassing.

1. Laat ze op de naam van het scorebord tikken om het weer te geven.

   ![ kies een bedrijf ](assets/accesscard.png)


### Verklaar scorecard UI

Verklaar aan de uitvoerende gebruiker hoe de tegels in de scorecards verschijnen u deelt.

![ verklaart tegels met inbegrip van de datumwaaier, het segment, en metriek en geselecteerde dimensies ](assets/newexplain.png)

![ Scorecard van het Voorbeeld ](assets/intro_scorecard.png)

Aanvullende informatie over tegels:

* De korreligheid van de sparklines is afhankelijk van de lengte van het datumbereik:
* Op een dag is er een uurtrend
   * Meer dan een dag en minder dan een jaar laten een dagelijkse trend zien
   * Een jaar of langer toont een wekelijkse trend
   * De formule van de percentagewaardeverandering is metrisch totaal (huidige datumwaaier) - metrisch totaal (de waaier van de vergelijkingsdatum) / metrisch totaal (de waaier van de vergelijkingsdatum).
   * U kunt het scherm omlaag trekken om het Scorecard te vernieuwen.


1. Tik op een tegel om te tonen hoe een gedetailleerde uitsplitsing voor de tegel werkt.

   ![ mening van de Onderbreking ](assets/sparkline.png)

   * Tik op een willekeurig punt op een dunne lijn om de gegevens weer te geven die aan dat punt op de lijn zijn gekoppeld.

   * Er wordt een tabel opgenomen waarin de aan de tegel toegevoegde afmetingen worden weergegeven. Tik op de pijl omlaag om de afmetingen te selecteren. Als er geen dimensie aan de tegel is toegevoegd, worden de diagramgegevens weergegeven in de tabel.

1. Als u datumbereiken voor uw scorebord wilt wijzigen, tikt u op de Datumkop en selecteert u de combinatie van het primaire bereik en het vergelijkingsdatumbereik dat u wilt weergeven.

   ![ data van de Verandering ](assets/changedate.png)

## Toepassingsvoorkeuren wijzigen

Tik op de bovenstaande optie **[!UICONTROL Preferences]** om de voorkeuren te wijzigen. Bij de voorkeuren kunt u de biometrische aanmelding inschakelen of de app voor de donkere modus instellen, zoals hieronder wordt weergegeven:

![ Donkere wijze ](assets/darkmode.png)

## Problemen oplossen

Als de uitvoerende gebruiker zich aanmeldt en een bericht ziet waarin wordt gemeld dat er niets is gedeeld:

![ niets gedeelde ](assets/nothing.png)

* De uitvoerende gebruiker heeft mogelijk de verkeerde Customer Journey Analytics-sandbox geselecteerd, of
* De scorecard is mogelijk niet gedeeld met de uitvoerende gebruiker.

Controleer of de uitvoerende gebruiker zich kan aanmelden bij de juiste Customer Journey Analytics-sandbox en of de scorecard is gedeeld.
