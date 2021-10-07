---
description: Leer meer over de verschillende opslagopties, zoals automatisch opslaan, opslaan als, opslaan als sjabloon en eerdere versies openen.
title: Projecten opslaan
feature: Workspace Basics
role: User, Admin
exl-id: e8206956-6e24-4a3a-8c3f-8acf1fb9d800
source-git-commit: 1c19c8cb9cad7b4b7938915d04396cc4646a1f32
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Projecten opslaan

Als u uw wijzigingen in een project wilt opslaan, gaat u naar het menu Werkruimte **[!UICONTROL Project]**. In bepaalde gevallen worden projecten ook automatisch opgeslagen in de werkruimte.

## Projectopties opslaan {#Save}

Er zijn verschillende opslaghandelingen die u kunt uitvoeren in het menu **[!UICONTROL Project]**, afhankelijk van de manier waarop u in de toekomst toegang wilt krijgen tot uw analyse.

| Handeling | Beschrijving |
|---|---|
| **[!UICONTROL Save]** | Sla de wijzigingen in uw project op. Als het project wordt gedeeld, zullen de ontvangers van het project ook de veranderingen zien. Wanneer u uw project voor het eerst opslaat, wordt u gevraagd het project een naam, (optionele) beschrijving en (optionele) tags toe te voegen. |
| **[!UICONTROL Save with notes]** | Voordat uw project wordt opgeslagen, voegt u notities toe over de wijzigingen in het project. Notities worden opgeslagen met de projectversie en zijn beschikbaar voor alle editors onder [!UICONTROL Project] > [!UICONTROL Open previous version]. |
| **[!UICONTROL Save as]** | Maak een duplicaat van uw project. Dit heeft geen invloed op het oorspronkelijke project. |
| **[!UICONTROL Save as template]** | Sla uw project op als een [aangepaste sjabloon](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html) die beschikbaar wordt voor uw organisatie onder **[!UICONTROL Project > New]** |

![](assets/save-project.png)

## Automatisch opslaan {#Autosave}

Bestaande projecten, d.w.z. projecten die minstens één keer eerder zijn opgeslagen, worden elke twee minuten automatisch opgeslagen op uw lokale computer. Nieuwe projecten die nog nooit zijn opgeslagen, worden momenteel niet automatisch opgeslagen.

Er zijn een paar scenario&#39;s die u van niet bewaarde veranderingen in een project kunnen leiden, resulterend in verschillende beschikbare acties.

### Een ander Workspace-project openen

Adobe biedt de optie om op te slaan voordat u de pagina verlaat. Nadat u een bestaand project hebt verlaten, wordt de automatisch opgeslagen lokale kopie verwijderd.

![](assets/existing-save.png)

### Navigeren weg of een tabblad sluiten

De browser waarschuwt dat niet-opgeslagen wijzigingen verloren gaan. U kunt kiezen om te vertrekken of te annuleren.

![](assets/browser-image.png)

### Browsercrashes of sessietijden uit

Voor **bestaande** projecten, bij het terugkeren naar Werkruimte, zult u **de terugwinning van het Project** modaal zien. Als u Ja selecteert, wordt het project hersteld met de automatisch opgeslagen lokale kopie. Met Nee verwijdert u de automatisch opgeslagen lokale kopie en opent u de laatst door de gebruiker opgeslagen versie van het project.

![](assets/project-recovery.png)

Voor **nieuwe** projecten die nooit zijn opgeslagen, kunnen niet-opgeslagen wijzigingen niet worden hersteld.

## Vorige versie openen {#previous-version}

>[!NOTE]
>
>Eerdere projectversies zijn momenteel in beperkte versie beschikbaar.

Een vorige versie van een project openen:

1. Ga naar **[!UICONTROL Project]** > **[!UICONTROL Open previous version]**

   ![](assets/previous-versions.png)

1. Controleer de lijst met eerdere beschikbare versies.
   [!UICONTROL Timestamp] en  [!UICONTROL Editor] worden getoond, naast  [!UICONTROL Notes] of zij werden toegevoegd toen het  [!UICONTROL Editor] bewaarde. Versies zonder aantekeningen worden gedurende 90 dagen opgeslagen; versies met notities worden gedurende 1 jaar opgeslagen .
1. Selecteer een vorige versie en klik **[!UICONTROL Load]**.
De vorige versie wordt vervolgens geladen met een melding. De vorige versie wordt pas de huidige opgeslagen versie van uw project als u **[!UICONTROL Save]** klikt. Als u bij de geladen versie vandaan navigeert, ziet u bij het retourneren de laatst opgeslagen versie van het project.
