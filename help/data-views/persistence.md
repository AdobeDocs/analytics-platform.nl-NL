---
title: Wat is dimensie persistentie in Customer Journey Analytics?
description: Dimension persistentie is een combinatie van allocatie en vervaldatum. Samen bepalen ze welke waarden voor dimensies behouden blijven.
translation-type: tm+mt
source-git-commit: b99e108e9f6dd1c27c6ebb9b443f995beb71bdbd
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---


# Persistentie

Dimension persistentie is een combinatie van allocatie en vervaldatum. Samen bepalen ze welke waarden voor dimensies behouden blijven. Adobe adviseert hoogst dat u binnen uw organisatie bespreekt hoe de veelvoudige waarden voor elke afmeting (toewijzing) worden behandeld en wanneer de afmetingswaarden het persisteren van gegevens (afloop) tegenhouden.

* Een waarde voor de dimensie gebruikt standaard de laatste toewijzing. Nieuwe waarden overschrijven persistente waarden.
* Een waarde voor de dimensie gebruikt standaard de vervaldatum [!UICONTROL Session].

## Toewijzing

Bepaalt hoe CJA krediet voor een succesgebeurtenis toewijst als een variabele veelvoudige waarden vóór de gebeurtenis ontvangt. Tot de ondersteunde waarden behoren:

* Recentste versie: De laatste waarde van de eVar ontvangt altijd krediet voor succesgebeurtenissen tot die eVar verloopt.
* Oorspronkelijke waarde: De eerste eVar krijgt altijd krediet voor succesgebeurtenissen tot die eVar verloopt.
* Instantie: ??

Opmerking: Als u van of naar Lineair schakelt, worden historische gegevens niet weergegeven. Het mengen van toewijzingstypes in de rapporteringsinterface kan tot misverklaarbare gegevens in rapporten leiden. Zo kan lineaire toewijzing inkomsten verdelen over een aantal verschillende eVar. Na het terugkeren naar de meest recente toewijzing, zou 100% van die opbrengst met de meest recente enige waarde worden geassocieerd. Deze koppeling kan leiden tot onjuiste conclusies van gebruikers.

Om de kans op verwarring bij het rapporteren te vermijden, maakt Analytics de historische gegevens niet aan de interface beschikbaar. U kunt deze weergeven als u de opgegeven eVar wilt wijzigen in de oorspronkelijke toewijzingsinstelling, maar u kunt de instellingen voor de eVar-toewijzing niet wijzigen om alleen toegang te krijgen tot de historische gegevens. Adobe raadt aan een nieuwe eVar te gebruiken wanneer nieuwe toewijzingsinstellingen gewenst zijn voor gegevens die al worden geregistreerd, in plaats van toewijzingsinstellingen te wijzigen voor een eVar waarin al een aanzienlijke hoeveelheid historische gegevens is opgebouwd.

## Verlopen

De waarden van Dimension verlopen na de tijdspanne die u specificeert. Nadat de afmetingswaarde verloopt, ontvangt het geen krediet meer voor metrisch. Dimension kunnen ook worden gevormd om op metriek te verlopen. Als je bijvoorbeeld een interne aanbieding hebt die aan het einde van een bezoek vervalt, ontvangt de interne aanbieding alleen kredieten voor aankopen of registraties die plaatsvinden tijdens het bezoek waarin ze zijn geactiveerd.

Er zijn twee manieren om een eVar te verlopen:

U kunt instellen dat de eVar na een opgegeven tijdsperiode of gebeurtenis vervalt.
U kunt de vervaldatum van een eVar forceren door deze opnieuw in te stellen. Dit is handig wanneer u een variabele opnieuw gebruikt.
Als u bijvoorbeeld de vervaldatum van een eVar wijzigt van 30 tot 90 dagen, blijven de verzamelde eVar behouden gedurende de nieuwe vervaldatum (in dit geval 90 dagen). Het systeem bekijkt eenvoudig de huidige die vervalbepaling en laatste vastgestelde timestamp van de eVar waarde wordt verzameld om afloop te bepalen. Alleen de optie Herstellen vervalt waarden en doet dit onmiddellijk.

Een ander voorbeeld: Als een eVar in Mei wordt gebruikt om interne bevorderingen te weerspiegelen en na 21 dagen verloopt, en in juni wordt het gebruikt om interne onderzoekssleutelwoorden te vangen, dan zou u op 1 Juni de afloop van, of het terugstellen van, de variabele moeten dwingen. Als u dat doet, blijven de interne promotiewaarden buiten de verslagen van juni.