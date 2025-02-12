---
title: De bronaansluiting voor Analytics en kaartvelden maken
description: Leer hoe u de bronaansluiting voor Analytics en kaartvelden maakt
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: f96565a2-f556-4b45-b88e-984613614d2e
source-git-commit: 971600fcc7d8a5aac4ad39812ab4a7af69d45ccc
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# De bronaansluiting voor Analytics en kaartvelden maken {#create-source-connector}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector-create"
>title="De bronaansluiting voor Analytics maken"
>abstract="Gebruik de bron van Analytics schakelaar om rapportreeksgegevens voor gebruik in Customer Journey Analytics in te voeren.<br><br> Creërend de bron van Analytics schakelaar neemt enkel een paar notulen met standaardmontages."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector-map-fields"
>title="De bronaansluiting voor Analytics en kaartschemavelden maken"
>abstract="De bronschakelaar moet weten hoe te om de gebieden van Adobe Analytics aan het schema van uw organisatie in kaart te brengen. Gebruik deze interface om de bronschakelaar van die afbeelding te voorzien. Deze stap maakt deel uit van het toevoegen van historische gegevens aan Customer Journey Analytics.<br><br> de tijd die deze stap neemt hangt sterk van het aantal dimensies en metriek af die u moet in kaart brengen. Deze stap is niet zo moeilijk als vervelend en repetitief. Gegevensstroomtoewijzing wordt ongeveer een week lang voltooid."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

## Begrijp hoe de de bronschakelaar van de Analyse historische gegevens in Customer Journey Analytics kan brengen

U kunt de Analytics-bronconnector gebruiken om Adobe Analytics-rapportsuite-gegevens over te brengen naar Adobe Experience Platform. Deze gegevens kunnen vervolgens worden gebruikt als historische gegevens in Customer Journey Analytics.

Dit proces veronderstelt dat u een douaneschema [ wilt tot stand brengen om met uw implementatie van SDK van het Web van Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken, omdat u een gestroomlijnd schema wilt dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.

Als u de Analytics-bronconnector wilt gebruiken om historische gegevens over te brengen naar Customer Journey Analytics, moet u:

1. [Creeer een douaneschema voor de bronschakelaar van de Analyse](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md)

1. Als u reeds geen Analytics bronschakelaar hebt, creeer de de bronschakelaar van de Analyse en kaartgebieden aan uw schema van SDK van het douaneWeb, zoals hieronder beschreven.

   of

   Als u reeds een Analytics bronschakelaar hebt, [ kaartgebieden van de bronschakelaar aan uw schema van SDK van het douaneWeb ](/help/getting-started/cja-upgrade/cja-upgrade-from-source-connector.md).

1. [Voeg de gegevensset van de bron van de Analyse aan de verbinding toe](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md)

## De bronaansluiting voor Analytics en kaartvelden maken

Als uw aangepaste schema is gemaakt, moet u de Adobe Analytics-bronconnector maken die u voor historische gegevens wilt gebruiken. (Voor uitvoerigere, algemene richtlijnen bij het creëren van een bronschakelaar, zie [ een Adobe Analytics bronverbinding in UI ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) creëren.)

Een Adobe Analytics-bronconnector maken voor historische gegevens:

1. Selecteer **[!UICONTROL Sources]** in het gedeelte Platform UI in de sectie **[!UICONTROL Connections]** links in het scherm.

1. Selecteer **[!UICONTROL Adobe applications]** in de lijst met [!UICONTROL CATEGORIES] .

1. Selecteer **[!UICONTROL Add data]** in de tegel Adobe Analytics.

   ![ het venster van Adobe Experience Platform met Bronnen die samen met de toepassingen van Adobe worden geselecteerd en benadrukte gegevens toevoegen.](./assets/sources-overview.png)

1. Selecteer **[!UICONTROL Report suite]** en selecteer vervolgens in de lijst met rapportsuites de rapportsuite met de historische gegevens die u in Customer Journey Analytics wilt gebruiken.

   ![ Adobe Experience Platform venster dat de lijst van de Reeksen van het Rapport toont ](./assets/report-suites.png)

1. Selecteer **[!UICONTROL Next]** in de rechterbovenhoek van het scherm.

1. Selecteer **[!UICONTROL Custom schema]**, dan selecteren het schema dat u in [ creeerde een douaneschema dat de het gebiedsgroep van Adobe Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md) omvat. <!-- Deleted this, because I changed this from choosing the default schemawe're pointing them now at the schema they just created: "Adobe Experience Platform  automatically creates the schema and the corresponding dataset to map all standard fields from the selected Adobe Analytics report suite." -->

   <!-- add screenshot -->

1. Wijs elke dimensie van Adobe Analytics aan een dimensie van het douaneschema toe.

   1. Selecteer in de sectie **[!UICONTROL Map standard fields]** de tab **[!UICONTROL Custom]** .

   1. Selecteer **[!UICONTROL Add new mapping]** .

   ![ gebieden van het kaartschema ](assets/schema-mapping.png)

   1. Selecteer in **[!UICONTROL Source field]** een Adobe Analytics-veld in de veldgroep Adobe Analytics ExperienceEvent-sjabloon. Selecteer vervolgens in **[!UICONTROL Target field]** het aangepaste veld in het XDM-schema waaraan u het wilt toewijzen.

      Niet alle Adobe Analytics-velden hebben een corresponderend veld in XDM vanwege de inherente architectuurverschillen tussen AppMeasurement en XDM.

   1. Herhaal dit proces voor elk veld in de Adobe Analytics ExperienceEvent-sjabloonveldgroep dat u gebruikt om gegevens te verzamelen in Adobe Analytics.

1. Selecteer **[!UICONTROL Next]** in de rechterbovenhoek van het scherm.

1. Geef de gegevensstroom een naam en (optioneel) geef een beschrijving op.

   ![ Adobe Experience Platform venster die de sectie van het detail Dataflow ](./assets/dataflow-detail.png) benadrukt

1. Selecteer **[!UICONTROL Next]** in de rechterbovenhoek van het scherm.

1. Controleer de verbinding en selecteer vervolgens **[!UICONTROL Finish]** .

   ![ Adobe Experience Platform venster die Connect en het type van Gegevens secties voor overzicht benadrukken ](./assets/review.png)

   Nadat de verbinding wordt gecreeerd, wordt de dataflow automatisch gecreeerd om een dataset met de gegevens van Adobe Analytics van uw rapportreeks te bevolken. De gegevensstroom neemt tot 13 maanden historische gegevens voor productiestanddozen op. De back-up van niet-productie sandboxen is beperkt tot drie maanden.

   Als u de Analytics bronschakelaar gebruikt om historische gegevens in uw implementatie van SDK van het Web van Customer Journey Analytics te brengen, dan moet u deze automatisch gecreeerde dataset aan de verbinding toevoegen die u voor uw implementatie van SDK van het Web creeerde.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
