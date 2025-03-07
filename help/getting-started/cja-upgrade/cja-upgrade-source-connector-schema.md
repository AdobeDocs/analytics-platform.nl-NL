---
title: Creeer een douaneschema voor de bronschakelaar van de Analyse
description: Leer hoe te om een douaneschema voor de bron van Analytics schakelaar tot stand te brengen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: fad62c04-b435-466a-ab3c-cf2d174ddbfb
source-git-commit: ac3ec479938acf509bbd26be282b75e75dd49c33
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Creeer een douaneschema voor de bronschakelaar van de Analyse {#create-custom-schema}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector-create-schema"
>title="Creeer een schema voor de bron van de Analyse schakelaar"
>abstract="Dit schema is een combinatie van de Adobe Analytics ExperienceEvent-veldgroep met alle veldgroepen die het aangepaste schema van uw organisatie vormen. Het staat u toe om de gebieden in kaart te brengen die door de bron van de Analyse schakelaar aan het schema van uw organisatie worden gebruikt, en slechts voor historische gegevens wordt gebruikt.<br><br> terwijl technisch in aard, kan het creëren van dit schema in uren, misschien sneller worden voltooid als u precies weet welke gebiedsgroepen omhoog het douaneschema van uw organisatie maken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector-historical"
>title="De bronaansluiting Analytics maken voor historische gegevens"
>abstract="U kunt de Analytics-bronconnector gebruiken om Adobe Analytics-rapportsuite-gegevens over te brengen naar Adobe Experience Platform. Deze gegevens kunnen vervolgens worden gebruikt als historische gegevens in Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

## Begrijp hoe de de bronschakelaar van de Analyse historische gegevens in Customer Journey Analytics kan brengen

U kunt de Analytics-bronconnector gebruiken om Adobe Analytics-rapportsuite-gegevens over te brengen naar Adobe Experience Platform. Deze gegevens kunnen vervolgens worden gebruikt als historische gegevens in Customer Journey Analytics.

Dit proces veronderstelt dat u een douaneschema [ wilt tot stand brengen om met uw implementatie van SDK van het Web van Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken, omdat u een gestroomlijnd schema wilt dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.

Als u de Analytics-bronconnector wilt gebruiken om historische gegevens over te brengen naar Customer Journey Analytics, moet u:

1. Maak een aangepast schema voor de bronconnector Analytics, zoals hieronder wordt beschreven.

1. Als u reeds geen Analytics bronschakelaar hebt, [ creeer de de bronschakelaar van de Analyse en kaartgebieden aan uw douaneschema ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md).

   of

   Als u reeds een Analytics bronschakelaar hebt, [ kaartgebieden van de bronschakelaar aan uw schema XDM ](/help/getting-started/cja-upgrade/cja-upgrade-from-source-connector.md).

1. [Voeg de gegevensset van de bron van de Analyse aan de verbinding toe](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md)

## Creeer een douaneschema voor de bronschakelaar van de Analyse

U zou reeds [ een nieuw douaneschema ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) voor uw implementatie van SDK van het Web van Experience Platform aan gebruik met Customer Journey Analytics moeten hebben gecreeerd. Dit schema moet alle veldgroepen bevatten voor velden waarop u gegevens wilt verzamelen.

U moet nu die zelfde gebiedsgroepen van uw schema van SDK van het Web gebruiken en hen toevoegen aan een nieuw schema dat u met de Analytics bronschakelaar kunt gebruiken.

Dit schema voor de de bronschakelaar van de Analyse moet bevatten:

* Alle gebiedsgroepen (met inbegrip van om het even welke groepen van het douanegebied die u) creeerde die in uw douaneschema inbegrepen zijn dat u voor uw implementatie van SDK van het Web creeerde. (Om het even welke douanevelden die geen deel van een standaardgebiedsgroep uitmaken zouden aan uw schema van SDK van het Web als deel van een groep van het douanegebied moeten zijn toegevoegd.)

* De Adobe Analytics ExperienceEvent-sjabloonveldgroep

Om het douaneschema tot stand te brengen om met de Analytics bronschakelaar te gebruiken:

1. In Adobe Experience Platform, begin creërend een nieuw douaneschema zoals die in [ wordt beschreven creeer een douaneschema om met uw implementatie van SDK van het Web van Customer Journey Analytics te gebruiken ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md).

1. Voeg alle gebiedsgroepen (met inbegrip van om het even welke groepen van het douanegebied) toe die in het schema inbegrepen zijn dat u voor uw implementatie van SDK van het Web creeerde.

1. Nadat u deze veldgroepen hebt toegevoegd, voegt u de Adobe Analytics ExperienceEvent-veldgroep toe:

   Selecteer in de sectie **[!UICONTROL Field groups]** de optie **[!UICONTROL Add]** om een extra veldgroep toe te voegen.

   ![ voeg gebiedsgroep aan schema toe ](assets/schema-add-field-group.png)

1. Zoek naar en selecteer de **[!UICONTROL Adobe Analytics ExperienceEvent Template]** gebiedsgroep.

   ![ voeg de het gebiedsgroep van Adobe Analytics ExperienceEvent ](assets/schema-experienceevent.png) toe

1. Selecteer **[!UICONTROL Add field groups]** .

1. Selecteer **[!UICONTROL Save]** om het schema op te slaan.

{{upgrade-final-step}}
