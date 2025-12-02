---
title: Alternatieve methoden bij upgrade naar Customer Journey Analytics
description: Meer informatie over de alternatieve methoden bij het upgraden naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 3a0d03d1-def0-45e6-8eb2-115b88497e6d
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# Alternatief voor upgrade: verzend uw gegevenslaag naar Customer Journey Analytics {#data-collection-data-layer}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-data-layer"
>title="Gegevenslaag verzenden naar Adobe"
>abstract="In plaats van gegevens via een XDM-object te verzenden, kunt u de gehele gegevenslaag via het gegevensobject naar Adobe verzenden.<br><br> deze optie bespaart implementatietijd door u toe te staan om uw gegevenslaag aan XDM in kaart te brengen, eerder dan het bevolken van een voorwerp XDM van kras. Deze toewijzing is echter een grote hoeveelheid werk omdat er een grote hoeveelheid gegevens zal zijn die Adobe niet gemakkelijk kan interpreteren. Deze optie voegt in de loop der tijd ook extra complexiteit toe, omdat elk veld dat u later in de toekomst aan uw gegevens toevoegt, in de gegevensstroom aan XDM moet worden toegewezen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-send-data-layer"
>title="Gegevenslaag naar Adobe verzenden"
>abstract="Configureer uw implementatie om gegevens op het gewenste moment naar Adobe te verzenden en configureer de JSON-payload als de volledige gegevenslaag."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-data-layer-map"
>title="Wijs elk element van de gegevenslaag aan XDM toe"
>abstract="Wijs elk element van de gegevenslaag aan het gewenste gebied XDM toe. Om het even welke elementen van de gegevenslaag die niet aan een XDM gebied in kaart worden gebracht worden permanent gelaten vallen, aangezien Adobe niet weet waar of hoe te om die gegevens op te slaan."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

Wanneer bevordering aan Customer Journey Analytics, adviseert Adobe [ een nieuwe implementatie van de SDK van het Web van Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md). Nochtans, afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, zouden de geadviseerde verbeteringsstappen niet praktisch voor uw organisatie kunnen zijn.

U kunt de gehele gegevenslaag naar Customer Journey Analytics verzenden in plaats van gegevens te verzamelen met het XDM-object. Dit alternatief zorgt echter voor extra complexiteit in de loop der tijd.

## Voordelen en nadelen

Deze methode is wederzijds exclusief met [ gebruikend uw logica van de de gegevensinzameling van AppMeasurement met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-alternative-appmeasurement.md), omdat beide methodes de zelfde taak verwezenlijken.

Hier volgen de voor- en nadelen van het gebruik van dit upgradealternatief:

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>**verstrekt alle voordelen om gegevens in Ervaring Edge Network** te ontvangen: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportering en gegevensbeschikbaarheid omdat Adobe Experience Platform aan macht [ wordt gebouwd verpersoonlijkingsgebruiksgevallen in real time ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (zoals prop, eVar, event, enzovoort)</li></ul><li>**gebruikt uw huidige logica van de gegevenslaag**: Deze methode gebruikt uw huidige logica van de gegevenslaag in plaats van een conventionele implementatie van SDK van het Web. Hoewel deze benadering enige configuratie vereist, vereist het geen volledig nieuwe implementatie van kras en het vereist geen het bevolken van gegevenselementen of markeringsregels. Hiermee kunt u gegevens van uw gegevenslaag toewijzen aan XDM in plaats van een XDM-object helemaal opnieuw te vullen.</li></ul> | <ul><li>**vereist afbeelding om gegevens naar Platform** te verzenden: Wanneer uw organisatie klaar is om Customer Journey Analytics te gebruiken, moet u gegevens naar een gegevensreeks in Adobe Experience Platform verzenden. <p>Omdat u met deze optie de gehele gegevenslaag aan de clientzijde in het gegevensobject kunt plaatsen en naar Adobe kunt verzenden, resulteert dit in een aanzienlijke hoeveelheid gegevens die Adobe niet gemakkelijk kan interpreteren. Als u Adobe wilt toestaan de gegevens te interpreteren, moet u gegevensstroomtoewijzing gebruiken om elk afzonderlijk veld toe te wijzen aan het gewenste XDM-veld.</p></li><li>**Onbuigzame implementatie**: De implementatie wordt beperkt tot wat de gegevenslaag verstrekt op het tijdstip dat de slag wordt verzonden. Dit kan acceptabel zijn voor organisaties met basisgegevensbehoeften, maar de meeste organisaties moeten dit soort rigide implementatie vermijden ten gunste van een flexibelere implementatie die het vullen van gegevenselementen mogelijk maakt.</li><li>**de Toekomstige veranderingen zijn moeilijker uit te voeren**: Om het even welk gebied u aan uw gegevens later in de toekomst toevoegt moet aan XDM in de gegevensstroom in kaart worden gebracht.</li></ul> |

{style="table-layout:auto"}

## Standaardstappen

De basisstappen voor het verzenden van uw volledige gegevenslaag naar Customer Journey Analytics zijn:

1. Configureer uw implementatie om gegevens op het gewenste moment naar Adobe te verzenden en configureer de JSON-payload als de volledige gegevenslaag.

1. Wijs elk element van de gegevenslaag aan het gewenste gebied XDM toe.

   Om het even welke elementen van de gegevenslaag die niet aan een XDM gebied in kaart worden gebracht worden permanent gelaten vallen, aangezien Adobe niet weet waar of hoe te om die gegevens op te slaan.
