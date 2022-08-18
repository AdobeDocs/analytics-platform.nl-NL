---
description: Leer hoe u de resultaten van A/B-tests kunt analyseren in het deelvenster CJA-experimenten.
title: Deelvenster Experimentatie
feature: Panels
source-git-commit: 2c217c7d31819ac8eb27d2d1010e0df787601e21
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---


# Deelvenster Experimentatie

>[!NOTE]
>
>Deze functionaliteit is momenteel in [beperkte tests](/help/release-notes/releases.md).

De **[!UICONTROL Experimentation]** kunt u verschillende gebruikerservaring, marketing, of overseinenvariaties vergelijken om te bepalen welke het best in het drijven van een specifiek resultaat is. U kunt de lift en het vertrouwen van om het even welk A/B experiment van om het even welk experimentatieplatform evalueren - online, off-line, van Adobe oplossingen, Adobe Journey Optimizer, en zelfs (breng-uw-eigen) gegevens BYO.

>[!IMPORTANT]
>
>Op dit punt [Adobe Analytics for Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) (A4T) gegevens kunnen niet worden geëvalueerd in de [!UICONTROL Experimentation] deelvenster.

## Toegangsbeheer

Het deelvenster Experimentatie is beschikbaar voor alle Customer Journey Analytics-gebruikers (CJA). Er zijn geen beheerdersrechten of andere machtigingen vereist. Voor de installatie zijn echter labels vereist in gegevensweergaven die alleen door beheerders kunnen worden toegewezen.

## Terminologie

* **Experimenteer**: Een experiment is een reeks variaties op een ervaring die aan eindgebruikers werden blootgesteld om te bepalen wat het beste is om in eeuwigheid te blijven. Een experiment bestaat uit twee of meer variaties, waarvan er één als variatie in de controlegroep wordt beschouwd.

* **Variatie**: Een van twee of meer wijzigingen in de ervaring van een eindgebruiker die worden vergeleken om het betere alternatief te identificeren. Als controleorgaan moet één variant worden gekozen en slechts één variant kan als controlevariant worden beschouwd.

* **Control**: Een specifieke variant die de status quo of de standaardstatus van een gebruikerservaring vertegenwoordigt. Waarmet alle andere variaties worden vergeleken.

* **Metrisch normaliseren**: De basis (sessies of personen) waarop een test wordt uitgevoerd. Een test kan bijvoorbeeld de omrekeningskoersen van verschillende variaties vergelijken, waarbij de omrekeningskoers wordt berekend als omzettingen per sessie of omzettingen per persoon.

* **Omzettingsmetrisch**: De metrische waarde waarmee een gebruiker variaties vergelijkt. De variatie met het meest gewenste resultaat voor de omzettingsmeting (hoogste of laagste) wordt als &quot;winnaar&quot; van een experiment aangemerkt.

## Stap 1: Verbinding maken om gegevensset(s) te experimenteren

Nadat uw experimentele gegevens zijn [ingesloten](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=en) naar Adobe Experience Platform, [een verbinding maken in CJA](/help/connections/create-connection.md) naar een of meer experimentele gegevenssets.

## Stap 2: Contextlabels toevoegen in gegevensweergaven

In de weergave-instellingen van CJA-gegevensweergaven kunnen beheerders toevoegen [contextlabels](/help/data-views/component-settings/overview.md) aan een afmeting of metrisch en de diensten CJA zoals [!UICONTROL Experimentation] kunnen deze labels voor hun doeleinden gebruiken. Voor het deelvenster Experimentatie worden twee vooraf gedefinieerde labels gebruikt:

* [!UICONTROL Experiment]
* [!UICONTROL Variant]

In uw gegevensmening die experimentatiegegevens bevat, kies twee afmeting, één met de experimentatiegegevens en één met de variantgegevens. Geef vervolgens een label aan deze afmetingen met de **[!UICONTROL Experiment]** en de **[!UICONTROL Variant]** labels.

![contextlabel](assets/context-label.png)

Zonder deze labels werkt het deelvenster Experimenteren niet.

## Stap 3: Het deelvenster Experimenteren configureren

1. Sleep het deelvenster Experimentatie naar een project in de CJA-werkruimte.

![deelvenster experimenteren](assets/experiment.png)




