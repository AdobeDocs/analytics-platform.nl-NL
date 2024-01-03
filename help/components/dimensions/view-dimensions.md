---
description: Hiermee geeft u de bovenste 5-waarden weer voor afmetingen die niet bij de tijd horen (en 15 voor tijdafmetingen).
title: Afmetingen voorvertonen in de werkruimte Customer Journey Analytics
feature: Dimensions
exl-id: 3e620bfa-825c-4f25-956c-83c905c49f84
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 24%

---

# Afmetingen voorvertonen in Analysis Workspace

Houd de muisaanwijzer boven het informatiepictogram (i) naast een dimensie. Dit toont de hoogste 5 waarden voor niet-tijdafmetingen (en 15 voor tijddimensies). We hielden die waarden altijd statisch (de 5 gekozen waarden zijn dus nooit gewijzigd).

![Hoogste 5 waarden voor afmetingen die niet in de tijd zijn.](assets/dimension-preview.png)

Nu, door gebrek, tonen wij dynamische waarden in plaats van statische degenen, met de optie om hen in statische waarden te veranderen. Andere opmerkzame zaken:

* Wanneer uw data worden bijgewerkt, worden ook de kolommen met dynamische dimensies bijgewerkt met de huidige 5/15-dimensie-items.
* Als een kolom met een dynamische dimensie wordt gekopieerd of verplaatst, wordt deze statisch.
* Wanneer u de muis boven een kolom met een statische dimensie houdt, ziet u een vergrendelingspictogram. Dit geeft aan dat de dimensie statisch is.

![Dimension kolom popup die het slotpictogram benadrukt.](assets/dimension_static.png)

## Dimensie-items tonen

Wanneer u de cursor boven een dimensie houdt en op de grijze pijl-rechts naast de dimensie klikt, wordt een lijst met de bijbehorende dimensie-items weergegeven. Een lijst met dimensie-items toont doorgaans de bovenste items voor de laatste 30 dagen.

Als u omlaag schuift naar de onderkant van de lijst, ziet u een **[!UICONTROL Show Top Items From Last 6 Months]**. Klik op deze optie om items met de bovenste dimensie van de afgelopen 180 dagen weer te geven.
