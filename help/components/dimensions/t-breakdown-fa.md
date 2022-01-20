---
description: Afmetingen en dimensies in Analysis Workspace onderverdelen.
keywords: Analysis Workspace
title: Uitsplitsingsdimensies
exl-id: 6b433db3-02c1-4deb-916e-b01c0b79889e
source-git-commit: 0176f10ffed85786b0bfa77204ca7a19d9c39ba7
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 2%

---

# Afmetingen onderverdelen in werkruimte

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset wijkt enigszins af van [Analysis Workspace in het traditionele Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Afmetingen en dimensies in Analysis Workspace onderverdelen.

U kunt uw gegevens op onbeperkte wijze onderverdelen voor uw specifieke behoeften; bouwen vragen gebruikend relevante metriek, dimensies, filters, tijdlijnen, en andere waarden van de analyseonderbreking.

1. [Een project maken](/help/analysis-workspace/home.md) met een datatabel.
1. Klik in de gegevenstabel met de rechtermuisknop op een regelitem en selecteer **[!UICONTROL Breakdown]** > *`<item>`*.

   ![Stap Resultaat](assets/fa_data_table_actions.png)

   U kunt metriek onderverdelen door afmetingspunten of publieksfilters over geselecteerde tijdsperioden. U kunt ook verder naar beneden boren tot een meer korrelig niveau.

   >[!NOTE]
   >
   >Het aantal uitsplitsingen dat in de tabel moet worden weergegeven, is beperkt tot 200. Deze limiet neemt toe voor exportuitsplitsingen.

**Video: Dimension in Analysis Workspace**

>[!VIDEO](https://video.tv.adobe.com/v/23971)

**Video: Dimension-uitsplitsingen**

>[!VIDEO](https://video.tv.adobe.com/v/23969)

## Toewijzingsmodellen toepassen op uitsplitsingen

Voor elke uitsplitsing binnen een tabel kan ook een toewijzingsmodel worden toegepast. Dit attributiemodel kan hetzelfde zijn of verschillen van de bovenliggende kolom. Bijvoorbeeld, kunt u lineaire Orden op uw afmeting van de Kanalen van de Marketing analyseren maar U-Vormde Orden op de specifieke het volgen codes binnen een Kanaal toepassen. Als u het toewijzingsmodel wilt bewerken dat op een indeling is toegepast, plaatst u de muisaanwijzer boven het indelingsmodel en klikt u op **[!UICONTROL Edit]**:

![Onderbrekingsinstellingen](assets/breakdown_settings.png)

Dit is het verwachte gedrag wanneer het toepassen van attributiemodellen op onderverdelingen of het uitgeven van hen:

* Als u een attributie toepast terwijl er geen andere attributies bestaan, wordt de attributie toegepast op de gehele kolomstructuur.

* Als u een uitsplitsing toevoegt nadat een toewijzing is toegepast, wordt de standaardinstelling gebruikt voor de opgegeven uitsplitsing die is toegevoegd (als die dimensie een standaardinstelling heeft). Anders wordt de uitsplitsing van de bovenliggende kolom gebruikt. Sommige dimensies hebben een standaardtoewijzing. De tijdafmetingen en de referentie gebruiken bijvoorbeeld Gelijke aanraking. De dimensie van het Product gebruikt Last Touch. Andere afmetingen hebben geen standaardwaarde en gebruiken de toewijzing van de bovenliggende kolom.

* Als de kolomstructuur al kenmerken bevat, heeft het wijzigen van de toewijzing alleen invloed op de eigenschap die u bewerkt.

## Video&#39;s

Afmetingen en metriek toevoegen aan uw project in Analysis Workspace:

>[!VIDEO](https://video.tv.adobe.com/v/30606)

Werken met afmetingen in een tabel voor vrije vorm:

>[!VIDEO](https://video.tv.adobe.com/v/40179)

Uitsplitsingen naar positie Dimension:

>[!VIDEO](https://video.tv.adobe.com/v/24033)
