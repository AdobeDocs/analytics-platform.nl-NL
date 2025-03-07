---
title: Kies uw schema voor Customer Journey Analytics
description: Meer informatie over de beschikbare opties bij het kiezen van een schema voor Customer Journey Analytics en over de voor- en nadelen van beide
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: a2b90ab2-2fcb-4bf4-a862-2f0675dc2fe2
source-git-commit: 765b6863cdafa06b54b76fbf0983afb4c14c21d4
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Kies uw schema voor Customer Journey Analytics {#choose-schema}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-schema-tailored"
>title="Een aangepast schema gebruiken"
>abstract="(Aanbevolen) Door uw schema aan te passen, kan uw organisatie alleen bijhouden wat u nodig hebt en kunt u overhead voorkomen die aan rommelige en onnodige velden is gekoppeld. Deze optie omvat gebiedsgroepen die door het Web SDK worden toegevoegd en gebiedsgroepen die aan uw organisatie worden aangepast."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-schema-default"
>title="Het standaardschema gebruiken"
>abstract="(Niet aanbevolen) Het Adobe Analytics-schema bevat meer dan duizend velden, wat tot een onoverzichtelijk en complex schema kan leiden. Uw organisatie zou gedwongen worden het concept van props en eVars te blijven volgen, een erfenisconcept dat niet in Customer Journey Analytics wordt gebruikt. Integratie met andere Adobe Experience Platform-services is moeilijker."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

<!-- this page exists as the "Learn more" link in the info icons for the options "I am comfortable using my Adobe Analytics schema as a basis" and "I want to use a schema tailored to my organization" -->

Bij de upgrade naar Customer Journey Analytics raadt Adobe aan een XDM-schema (Custom Experience Data Model) te maken dat beter aansluit bij de behoeften van uw organisatie wanneer u andere platformservices gaat gebruiken. U kunt ook het bestaande Adobe Analytics-schema gebruiken.

Houd rekening met de voor- en nadelen van beide.

## Een aangepast schema maken voor uw organisatie (aanbevolen)

Adobe raadt u aan een aangepast schema te maken wanneer u een upgrade naar Customer Journey Analytics uitvoert.

| Voordelen | Nadelen |
|----------|---------|
| <ul><p>De voordelen van het bijwerken aan uw eigen douaneschema omvatten:</p><ul><li>Een gestroomlijnd schema dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.</li><p>Wanneer veranderingen in het schema worden vereist, moet u niet door duizenden ongebruikte gebieden bewegen om het gebied te vinden dat het bijwerken vereist.</p></ul> | <p>De nadelen van het bijwerken aan uw eigen douaneschema omvatten:</p><ul><li>Het bijwerken van uw schema is een tijdrovend proces dat wordt vereist alvorens u begint gegevens naar Platform te verzenden.</li></ul> |

## Het bestaande Adobe Analytics-schema gebruiken

De optie om uw bestaande Adobe Analytics-schema met Customer Journey Analytics te gebruiken is alleen beschikbaar als uw Adobe Analytics-implementatie is geconfigureerd met de Adobe Experience Platform Web SDK. <!-- correct? Or can you do this with an AppMeasurement implementation?-->

| Voordelen | Nadelen |
|----------|---------|
| <p>De voordelen van het Adobe Analytics-schema zijn:</p><ul><li>Eenvoudig upgraden<p>Als u reeds gegevens naar Adobe Analytics met het Web SDK van Adobe Experience Platform verzendt, kunt u de extra dienst aan uw gegevensstroom toevoegen om gegevens naar Adobe Experience Platform te verzenden (die dan in uw configuratie van Customer Journey Analytics kan worden gebruikt).</p></li></ul> | <p>De nadelen van het gebruik van het Adobe Analytics-schema zijn:</p><ul><li>Terwijl het gebruiken van het schema van Adobe Analytics beperkt u niet in termen van hoe het met andere toepassingen van het Platform kan worden gebruikt, resulteert het in een schema dat complexer is dan het anders zou kunnen zijn. Dit komt omdat het Adobe Analytics-schema veel objecten bevat die specifiek zijn voor Adobe Analytics en die waarschijnlijk niet door uw organisatie zullen worden gebruikt.<p>Wanneer wijzigingen in het schema vereist zijn, moet u door duizenden ongebruikte velden bladeren om het veld te zoeken dat moet worden bijgewerkt.</p></li></ul> |




<!-- Not sure about any of this: 

If you plan to use your Adobe Analytics schema, the following steps are required:

For Adobe Analytics implementations using AppMeasurement:

1. Datastream mapping

For Adobe Analytics implementations using the Web SDK:

1. 



the upgrade steps provided by the Customer Journey Analytics Upgrade Guide.

If you want to create an XDM schema to use with Customer Journey Analytics, continue with [Create an XDM schema to use with Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md).


Tags: (All 3 require data prep mapping. Would need to go into the datastream and map every single field to its appropriate place in XDM. Because whenever you use the data object, it always requires mapping. If you send something in the data object and it doesn't get mapped, the it is permanently lost and can't be recovered.)

1. Shim - Intercepts and instead of sending data to a report suite, it sends it to a Data View. (Data object)

1. Russ special - convert current implementation to a Web SDK implementation - put everything in the data object. 

1. Plop entire data layer into the data object and send that to the datastream. (not documented. Might be the Web SDK docs.)

-->
