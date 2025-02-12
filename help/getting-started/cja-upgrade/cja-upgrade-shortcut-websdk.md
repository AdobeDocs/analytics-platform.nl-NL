---
title: De kortere weg van de verbetering Migreer een AppMeasurement of de uitbreiding van de Analyse om het Web SDK te gebruiken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 83927cf0-b3b4-42b4-9ca5-0c81c091383f
source-git-commit: e4e0c3cf2e865454837df6626c3b1b09f119f07f
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Sneltoets voor upgrade: een AppMeasurement- of analyseextensie-implementatie migreren voor gebruik van de webversie van SDK {#shortcut-migrate-websdk}

>[!NOTE]
>
>Deze documentatie zou als deel van [ Adobe Analytics aan de verbeteringsvragenlijst van Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) moeten worden gebruikt.

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_migrate_aa_to_websdk"
>title="Migreer uw implementatie van Analytics om het Web SDK te gebruiken"
>abstract="In plaats van gegevens via een XDM-object te verzenden, kunt u al uw variabelen in AppMeasurement-indeling via het gegevensobject verzenden. Met deze sneltoets kunt u uw AppMeasurement-logica blijven gebruiken om gegevens naar Platform te verzenden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="migrate_aa_to_websdk"
>title="Migreer uw implementatie van Analytics om het Web SDK te gebruiken"
>abstract="In plaats van gegevens via een XDM-object te verzenden, kunt u al uw variabelen in AppMeasurement-indeling via het gegevensobject verzenden. Met deze sneltoets kunt u uw AppMeasurement-logica blijven gebruiken om gegevens naar Platform te verzenden."

<!-- markdownlint-enable MD034 -->

Wanneer bevordering aan Customer Journey Analytics, adviseert Adobe [ een nieuwe implementatie van de SDK van het Web van Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md). Nochtans, afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, zouden de geadviseerde verbeteringsstappen niet praktisch voor uw organisatie kunnen zijn.

Als uw Adobe Analytics-implementatie AppMeasurement of de extensie Analytics is, is er een upgrade-sneltoets beschikbaar waarmee u uw Adobe Analytics-implementatie kunt migreren en de Adobe Experience Platform Web SDK kunt gebruiken om gegevens naar Edge Network en Adobe Analytics te verzenden voordat u deze naar Customer Journey Analytics verzendt.

## Voordelen en nadelen

Houd rekening met de volgende voordelen en nadelen van de sneltoets voor upgrades om uw AppMeasurement- of analyseprogramma te migreren voor gebruik van de Web SDK:

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>**verstrekt alle voordelen om gegevens in Ervaring Edge Network** te ontvangen: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportering en gegevensbeschikbaarheid omdat Adobe Experience Platform aan macht [ wordt gebouwd verpersoonlijkingsgebruiksgevallen in real time ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP, enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (zoals prop, eVar, event, enzovoort)</li></ul><li>**gebruikt uw bestaande implementatie**: Terwijl deze benadering sommige implementatieveranderingen vereist, vereist het geen volledig nieuwe implementatie van kras. U kunt de bestaande gegevenslaag en -code gebruiken met minimale wijzigingen in de implementatielogica zonder dat dit van invloed is op uw bestaande Adobe Analytics-rapportage.</li><li>**verstrekt flexibiliteit om een schema XDM voor uw organisatie in een recentere tijd** tot stand te brengen: U kunt uw bestaande implementatie van Adobe Analytics migreren om het Web SDK te gebruiken en te bevestigen dat alles in Adobe Analytics werkt, dan tot het schema XDM leiden. Dankzij deze flexibiliteit is een meer methodische en doordachte upgrade naar Customer Journey Analytics mogelijk.</li></ul> | <ul><li>**vereist afbeelding om gegevens naar Platform** te verzenden: Wanneer uw organisatie klaar is om Customer Journey Analytics te gebruiken, moet u gegevens naar een gegevensreeks in Adobe Experience Platform verzenden. Deze actie vereist dat elk gebied in het gegevensvoorwerp een ingang in het hulpmiddel van de gegevenstoewijzing is dat het aan een XDM schemagebied toewijst. Voor deze workflow hoeft u slechts één keer toewijzingen uit te voeren, en dit betekent niet dat u implementatiewijzigingen aanbrengt. Het is echter een extra stap die niet vereist is bij het verzenden van gegevens in een XDM-object.</li><li>**Technische schuld**: Omdat deze benadering een gewijzigde vorm van uw bestaande implementatie gebruikt, kan het moeilijker zijn om implementatielogica te volgen en veranderingen in de toekomst uit te voeren wanneer nodig. </li></ul> |

{style="table-layout:auto"}

## Standaardstappen

Als u besluit om de verbeteringskortere weg te nemen om uw AppMeasurement of de uitbreidingsimplementatie van Analytics te migreren om het Web SDK te gebruiken, wordt een nieuwe stap toegevoegd aan de dynamisch geproduceerde stappen voor uw organisatie in [ Adobe Analytics aan de verbeteringsvragenlijst van Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/).

De basisstappen voor het migreren van een de uitbreidingsimplementatie van AppMeasurement of van Analytics om het Web SDK te gebruiken zijn:

1. Gegevens verzenden naar platform.

   Als u al gegevens naar Platform verzendt met uw Adobe Analytics-implementatie, is deze stap niet vereist. U moet eenvoudig een verbinding tussen de datasets van het Platform en Customer Journey Analytics tot stand brengen, zoals later in dit proces wordt beschreven.

1. (Optioneel) Maak een XDM-schema voor uw organisatie terwijl u tijd hebt.

1. (Voorwaardelijk) als u een XDM-schema hebt gemaakt, gebruikt u gegevenstoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.
