---
title: Maak een XDM-schema voor de bronconnector van Analytics
description: Leer hoe te om een schema XDM voor de bron van Analytics schakelaar tot stand te brengen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: fad62c04-b435-466a-ab3c-cf2d174ddbfb
source-git-commit: 8bcc6b3b2a1e6f75bd0c868f77a375913412f988
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Maak een XDM-schema voor de bronconnector van Analytics

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

## Begrijp hoe de de bronschakelaar van de Analyse historische gegevens in Customer Journey Analytics kan brengen

U kunt de Analytics-bronconnector gebruiken om Adobe Analytics-rapportsuite-gegevens over te brengen naar Adobe Experience Platform. Deze gegevens kunnen vervolgens als historische gegevens in Customer Journey Analytics worden gebruikt.

Dit proces veronderstelt dat u een schema wilt [ tot stand brengen XDM wanneer het bevorderen aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md), omdat u een gestroomlijnd schema wilt dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.

Om de bron van Analytics schakelaar te gebruiken om historische gegevens in Customer Journey Analytics te brengen, moet u:

1. Maak een XDM-schema voor de bronconnector Analytics, zoals hieronder wordt beschreven.

1. Als u reeds geen Analytics bronschakelaar hebt, [ creeer de Analytics bronschakelaar en kaartgebieden aan uw XDM schema ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md).

   of

   Als u reeds een Analytics bronschakelaar hebt, [ kaartgebieden van de bronschakelaar aan uw schema XDM ](/help/getting-started/cja-upgrade/cja-upgrade-from-source-connector.md).

1. [Voeg de gegevensset van de bron van de Analyse aan de verbinding toe](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md)

## Maak een XDM-schema voor de bronconnector van Analytics

U zou reeds [ een nieuw schema XDM ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) voor uw implementatie van SDK van het Web van Experience Platforms aan gebruik met Customer Journey Analytics moeten hebben gecreeerd. Dit schema moet alle veldgroepen bevatten voor velden waarop u gegevens wilt verzamelen.

U moet nu die zelfde gebiedsgroepen van uw schema van SDK van het Web gebruiken en hen toevoegen aan een nieuw schema dat u met de Analytics bronschakelaar kunt gebruiken.

Dit schema voor de de bronschakelaar van de Analyse moet bevatten:

* Alle gebiedsgroepen (met inbegrip van om het even welke groepen van het douanegebied die u) creeerde die in uw douaneschema inbegrepen zijn dat u voor uw implementatie van SDK van het Web creeerde. (Om het even welke douanevelden die geen deel van een standaardgebiedsgroep uitmaken zouden aan uw schema van SDK van het Web als deel van een groep van het douanegebied moeten zijn toegevoegd.)

* De Adobe Analytics ExperienceEvent-sjabloonveldgroep

U kunt als volgt het XDM-schema maken voor gebruik met de bronconnector Analytics:

1. In Adobe Experience Platform, begin creërend een nieuw schema XDM zoals die in [ wordt beschreven creeer een schema XDM met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken.

1. Voeg alle gebiedsgroepen (met inbegrip van om het even welke groepen van het douanegebied) toe die in het schema inbegrepen zijn dat u voor uw implementatie van SDK van het Web creeerde.

1. Nadat u deze veldgroepen hebt toegevoegd, voegt u de Adobe Analytics ExperienceEvent-veldgroep toe:

   Selecteer in de sectie **[!UICONTROL Field groups]** de optie **[!UICONTROL Add]** om een extra veldgroep toe te voegen.

   ![ voeg gebiedsgroep aan schema toe ](assets/schema-add-field-group.png)

1. Zoek naar en selecteer de **[!UICONTROL Adobe Analytics ExperienceEvent Template]** gebiedsgroep.

   ![ voeg de het gebiedsgroep van Adobe Analytics ExperienceEvent ](assets/schema-experienceevent.png) toe

1. Selecteer **[!UICONTROL Add field groups]** .

1. Selecteer **[!UICONTROL Save]** om het schema op te slaan.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
