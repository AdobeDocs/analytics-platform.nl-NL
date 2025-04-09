---
title: Concepten en functies van Customer Journey Analytics B2B edition
description: Concepten en functies voor de B2B edition of Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Basics
role: User, Admin
hide: true
hidefromtoc: true
badgePremium: label="B2B edition"
exl-id: df2cc922-d214-49b9-8fdb-443cc1dac05b
source-git-commit: 3812b10e558c1b8a3ee4fe474405543c68433d8e
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# B2B edition-concepten en -functies

{{draft-b2b}}

In dit artikel worden algemene concepten en kenmerken op datasets en containers beschreven en wordt uitgelegd hoe deze verschillen tussen de standaard en de B2B edition van Customer Journey Analytics.

Datasets zijn de bronnen van een verbinding. Als deel van vestiging een verbinding, bepaalt u datasets om deel van die verbinding te uitmaken.

Containers worden in Customer Journey Analytics gebruikt om functies zoals filters, berekende meetgegevens en geavanceerde analysemogelijkheden te ondersteunen en te vereenvoudigen.




## Standaardcontainers

De *standaard* versie van Customer Journey Analytics is bouwt rond het concept drie containers: Persoon, Zitting, en Gebeurtenis. In een standaard Customer Journey Analytics-instelling worden deze containers impliciet gegenereerd op basis van uw installatie.

U kunt opnieuw bepalen hoe deze containers worden genoemd wanneer u een mening van Gegevens vormt maar conceptueel gebruikt de standaardversie een op persoon-gebaseerde containerhiërarchie.

![ B2C ](assets/b2c-containers.svg){zoomable="yes"}

In de verbinding voegt u gegevenssets voor gebeurtenissen, profielen en opzoeken toe en selecteert u identiteiten die u wilt gebruiken om de verbinding tussen deze gegevenssets te definiëren. Als onderdeel van de verbinding wordt automatisch een op personen gebaseerde containerhiërarchie gegenereerd. In die hiërarchie wordt de sessiecontainer gedefinieerd door de [sessie-instellingen](/help/data-views/session-settings.md) in de gegevensweergave.


## B2B-containers

In Customer Journey Analytics B2B Edition wordt een accountcontainer toegevoegd aan de lijst met gegenereerde containers.  En u hebt de optie om de generatie van extra containers, zoals Globale Rekening, het Kopen Groep, en Kans te vormen.

![ B2B ](assets/b2b-containers.svg){zoomable="yes"}

In de verbinding, voegt u Gebeurtenis, Rekening, Globale Rekening, Kans, het Kopen Groep en andere datasets van de Opzoekopdracht toe. U selecteert Account als primaire id voor de verbinding, zodat u op account gebaseerde identiteiten kunt gebruiken om de verbinding tussen de gegevenssets te definiëren. Als onderdeel van de verbinding wordt automatisch een containerhiërarchie op basis van een account gegenereerd. In die hiërarchie wordt de container van de Zitting tussen de container van de Persoon en de container van de Gebeurtenis bepaald door de [ montages van de Zitting ](/help/data-views/session-settings.md) in uw mening van Gegevens. Aanvullende sessiecontainers, bijvoorbeeld tussen Account en Event, worden momenteel niet ondersteund.

Opportunity, Buying Group en Person zijn alle containers op hetzelfde niveau van de container van de account. Zie de tabel hieronder voor een beschrijving en basisgebruik.

| B2B-container | Beschrijving <br/> Basis gebruiksgeval |
|---|---|
| Account | Een bedrijf dat een klant of potentiële klant van uw zaken is. Dit zou een dochteronderneming of afdeling van een grotere organisatie kunnen zijn. Account vertegenwoordigt de organisatie waarnaar u verkoopt en die u wilt bijhouden op organisatieniveau. |
| Globale account (optioneel) | De belangrijkste moedermaatschappij van een groep verbonden ondernemingen. Een global account heeft geen moedermaatschappij, maar kan dochterondernemingen of afdelingen hebben die tot de global account behoren. Een account zonder moedermaatschappij of dochterondernemingen moet zowel in het accountveld als in het veld voor de globale account worden vermeld, als beide accounts zijn ingeschakeld als onderdeel van het instellen van een verbinding. |
| Opportunity (optioneel) | Een verzameling producten en diensten die samen worden verkocht. Bij een gelegenheid waren vaak verschillende fasen van de verkoopcyclus betrokken om als verkoop te worden gesloten.<br> u zou opportuniteitsgegevens gebruiken om de opportuniteitsvooruitgang door de verkooptrechter te meten. Bijvoorbeeld, een rapport dat details over de topkansen verstrekt die van opportuniteitsfase 3 aan fase 4 zijn overgegaan. |
| Groep voor kopen (optioneel) | Een verzameling van mensen binnen een organisatie die betrokken zijn bij het besluitvormingsproces om een product of dienst aan te schaffen. <br/>U zou gegevens van koopgroepen gebruiken om koopgroepen te volgen via campagnebeheer. Bijvoorbeeld, buikd een publiekssegment van de belangrijkste inkoopgroepen.<br/> U wilt waarschijnlijk een zoekopdracht van de koopgroep naar profielgegevens, zodat u kunt rapporteren over de mensen in een koopgroep. |
| Persoon | Een individu, dat vaak door een uniek e-mailadres wordt geïdentificeerd dat met het bedrijf in wisselwerking heeft gestaan. <br/> u zou de profielgegevens gebruiken om mensen te identificeren die voor een rekening werken. Bijvoorbeeld: richt alle mensen bij een rekening die zich voor een conferentie hebben aangemeld. |


## Afstemmen op container of veld

Wanneer u een verbinding in Customer Journey Analytics bepaalt, kunt u voor elke verslag (profiel of raadpleging) dataset bepalen, of die dataset door container wordt aangepast of door gebied.

### Afstemmen op container

Als een recorddataset door container, bijvoorbeeld het Kopen Groep wordt aangepast, wordt de recorddataset behandeld als een type van profieldataset en als dataset van het Profiel in het gebruikersinterface.

### Overeenkomst per veld

Als een recorddataset door gebied, bijvoorbeeld het Lid van de Lijst van de Marketing wordt aangepast, wordt de recorddataset behandeld als een type van raadplegingsdataset en als dataset van de Opzoekopdracht in het gebruikersinterface.



## Rapport over op personen en rekeningen gebaseerde gegevens

Als u op persoon-gebaseerde containers (en persoonsidentiteiten) en op rekening-gebaseerde containers (en rekeningsidentiteiten) wilt rapporteren, zou u twee afzonderlijke verbinding binnen Customer Journey Analytics moeten opzetten. Bij één verbinding selecteert u Persoon als primaire id en bij één verbinding selecteert u Account als primaire id. Customer Journey Analytics biedt geen ondersteuning voor op personen gebaseerde en op account gebaseerde rapportage vanuit dezelfde container.
