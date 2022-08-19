---
description: Leer hoe u de resultaten van A/B-tests kunt analyseren in het deelvenster CJA-experimenten.
title: Deelvenster Experimentatie
feature: Panels
exl-id: e11169b4-2c73-4dd4-bca7-c26189d60631
source-git-commit: 57a52c21b1850574e5d85ab560fb5399f9b37631
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Deelvenster Experimentatie

>[!NOTE]
>
>Deze functionaliteit is momenteel in [beperkte tests](/help/release-notes/releases.md).

De **[!UICONTROL Experimentation]** in dit deelvenster kunnen analisten verschillende gebruikerservaringen, marketing of berichtvariaties vergelijken om te bepalen wat het beste is om een bepaald resultaat te bepalen. U kunt de lift en het vertrouwen van om het even welk A/B experiment van om het even welk experimentatieplatform evalueren - online, off-line, van Adobe oplossingen, Adobe Journey Optimizer, en zelfs (breng-uw-eigen) gegevens BYO.

>[!IMPORTANT]
>
>Op dit punt [Adobe Analytics for Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) (A4T) gegevens die via de Analytics Source Connector naar Adobe Experience Platform worden gebracht **kan** worden geanalyseerd in het [!UICONTROL Experimentation] deelvenster. We verwachten dat er in 2023 een resolutie over deze kwestie komt.

## Toegangsbeheer

Het deelvenster Experimentatie kan door alle Customer Journey Analytics-gebruikers (CJA) worden gebruikt. Er zijn geen beheerdersrechten of andere machtigingen vereist. Voor de installatie (stappen 1 en 2 hieronder) zijn echter handelingen vereist die alleen door beheerders kunnen worden uitgevoerd.

## Stap 1: Verbinding maken om gegevensset(s) te experimenteren

Nadat uw experimentele gegevens zijn [ingesloten](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=en) naar Adobe Experience Platform, [een verbinding maken in CJA](/help/connections/create-connection.md) naar een of meer experimentele gegevenssets.

## Stap 2: Contextlabels toevoegen in gegevensweergaven

In de weergave-instellingen van CJA-gegevensweergaven kunnen beheerders toevoegen [contextlabels](/help/data-views/component-settings/overview.md) aan een afmeting of metrisch en de diensten CJA zoals [!UICONTROL Experimentation] kunnen deze labels voor hun doeleinden gebruiken. Voor het deelvenster Experimentatie worden twee vooraf gedefinieerde labels gebruikt:

* [!UICONTROL Experiment]
* [!UICONTROL Variant]

In uw gegevensmening die experimentatiegegevens bevat, kies twee afmeting, één met de experimentatiegegevens en één met de variantgegevens. Geef vervolgens een label aan deze afmetingen met de **[!UICONTROL Experiment]** en de **[!UICONTROL Variant]** labels.

![contextlabel](assets/context-label.png)

Zonder deze labels werkt het deelvenster Experimenten niet, omdat er geen experimenten zijn om mee te werken.

## Stap 3: Het deelvenster Experimenteren configureren

1. Sleep het deelvenster Experimentatie naar een project in de CJA-werkruimte.

![deelvenster experimenteren](assets/experiment.png)

>[!IMPORTANT]
>Als de noodzakelijke opstelling in CJA- gegevensmeningen niet is voltooid, zult u een bericht aan dat effect ontvangen alvorens u kunt te werk gaan.

1. Configureer de instellingen voor deelvensterinvoer.

   | Instelling | Definitie |
   | --- | --- |
   | **[!UICONTROL Experiment]** | Een reeks variaties op een ervaring die aan eindgebruikers werden blootgesteld om te bepalen welke ervaring het beste in onbeperkte tijd kan worden bewaard. Een experiment bestaat uit twee of meer varianten, waarvan er één als de besturingsvariant wordt beschouwd. Deze instelling is vooraf gevuld met de afmetingen die zijn gelabeld met de  **[!UICONTROL Experiment]** in gegevensweergaven en de waarde van het experiment van de laatste drie maanden. |
   | **[!UICONTROL Control Variant]** | Een van twee of meer wijzigingen in de ervaring van een eindgebruiker die worden vergeleken om het betere alternatief te identificeren. Eén variant moet als controlevariant worden gekozen en slechts één variant kan als controlevariant worden beschouwd. Deze instelling is vooraf gevuld met de afmetingen die zijn gelabeld met de  **[!UICONTROL Variant]** label in gegevensweergaven. Deze instelling geeft de variantgegevens weer die bij dit experiment horen. |
   | **[!UICONTROL Success Metrics]** | De metrische of metrische waarde waarmee een gebruiker varianten vergelijkt. De variant met het meest gewenste resultaat voor de omzettingsmeting (hoogste of laagste) wordt de &quot;best presterende variant&quot; van een experiment genoemd. U kunt maximaal vijf metriek toevoegen. |
   | **[!UICONTROL Normalizing Metric]** | De basis ([!UICONTROL People], [!UICONTROL Sessions], of [!UICONTROL Events]) waarop een test wordt uitgevoerd. Een test kan bijvoorbeeld de conversiesnelheden van verschillende variaties vergelijken, waarbij **[!UICONTROL Conversion rate]** wordt berekend als **[!UICONTROL Conversions per session]** of **[!UICONTROL Conversions per person]**. |

1. Klik op **[!UICONTROL Build]**.

## Stap 4: De uitvoer van het deelvenster interpreteren

Het deelvenster Experimentatie bevat een uitgebreide set gegevens en visualisaties waarmee u beter kunt begrijpen hoe uw experimenten werken. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren. U kunt het deelvenster op elk gewenst moment bewerken door in de rechterbovenhoek op het potlood te klikken.

U krijgt ook een tekstsamenvatting die aangeeft of het experiment al dan niet overtuigend is en die het resultaat samenvat. Conclusiviteit is gebaseerd op statistische significantie. (Zie &quot;Statistische methodologie&quot; hieronder.) U kunt samenvattingsnummers zien voor de best presterende variant met de hoogste lichtsterkte en betrouwbaarheid.

>[!NOTE]
>
>Lift en Vertrouwen zijn ook geavanceerde berekende metrische functies in CJA, zodat kunt u uw eigen lift en betrouwbaarheidsmetriek bouwen.

![experimenteren met uitvoer](assets/exp-output1.png)

Voor elke succesmetrische metrisch u selecteerde, zullen één vrije lijst en één trend van de omzettingssnelheid worden getoond:

![experimenteren met uitvoer](assets/exp-output2.png)

De [!UICONTROL Line] de grafiek geeft u [!UICONTROL Control] versus [!UICONTROL Control Variant] prestaties:

![experimenteren met uitvoer](assets/exp-output3.png)


## Statistische methodologie

Om te volgen.



