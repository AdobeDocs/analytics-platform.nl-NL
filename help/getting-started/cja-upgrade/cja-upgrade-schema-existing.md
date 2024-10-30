---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad bij de upgrade van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 711e92db7084592dc562eda3d0dcf33bcb4a62d4
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---

# Adobe Analytics-schema met Customer Journey Analytics gebruiken

>[!NOTE]
>
>Deze documentatie zou als deel van [ Adobe Analytics aan de vragenlijst van de de verbeteringsverbetering van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) moeten worden gebruikt.

<!-- this page exists as the "Learn more" link in the info icon for the option "I am comfortable using my Adobe Analytics schema as a basis" -->

De optie om een bestaand Adobe Analytics-schema met Customer Journey Analytics te gebruiken is alleen beschikbaar als uw Adobe Analytics-implementatie is geconfigureerd met de Adobe Experience Platform Web SDK. <!-- correct? Or can you do this with an AppMeasurement implementation?-->

Houd rekening met de volgende voor- en nadelen van het gebruik van uw Adobe Analytics-schema met Customer Journey Analytics:

| Voordelen | Nadelen |
|----------|---------|
| <p>De voordelen van het gebruik van het Adobe Analytics-schema zijn:</p><ul><li>Versnelling<p>Als u al gegevens naar Adobe Analytics verzendt met de Adobe Experience Platform Web SDK, kunt u een extra service aan uw gegevensstroom toevoegen om gegevens naar Adobe Experience Platform te verzenden (die vervolgens in uw Customer Journey Analytics-configuratie kan worden gebruikt).</p></li></ul> | <p>De nadelen van het gebruik van het Adobe Analytics-schema zijn:</p><ul><li>Wanneer u het Adobe Analytics-schema gebruikt, beperkt u niet de manier waarop het kan worden gebruikt met andere platformtoepassingen, maar resulteert dit in een schema dat complexer is dan het anders zou kunnen zijn. Dit komt doordat het Adobe Analytics-schema veel objecten bevat die specifiek zijn voor Adobe Analytics en die waarschijnlijk niet door uw organisatie zullen worden gebruikt.<p>Wanneer wijzigingen in het schema vereist zijn, moet u door duizenden ongebruikte velden bladeren om het veld te vinden dat moet worden bijgewerkt.</p></li></ul> |

<!-- Not sure about any of this: 

If you plan to use your Adobe Analytics schema, the following steps are required:

For Adobe Analytics implementations using AppMeasurement:

1. Datastream mapping

For Adobe Analytics implementations using the Web SDK:

1. 



the upgrade steps provided by the [Adobe Analytics to Customer Journey Analytics upgrade questionnaire](https://gigazelle.github.io/cja-ttv/).

If you want to create an XDM schema to use with Customer Journey Analytics, continue with [Create an XDM schema to use with Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md).


Tags: (All 3 require data prep mapping. Would need to go into the datastream and map every single field to its appropriate place in XDM. Because whenever you use the data object, it always requires mapping. If you send something in the data object and it doesn't get mapped, the it is permanently lost and can't be recovered.)

1. Shim - Intercepts and instead of sending data to a report suite, it sends it to a Data View. (Data object)

1. Russ special - convert current implementation to a Web SDK implementation - put everything in the data object. 

1. Plop entire data layer into the data object and send that to the datastream. (not documented. Might be the Web SDK docs.)

-->