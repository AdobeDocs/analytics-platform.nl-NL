---
title: Hoe te om een datumwaaier in Report Builder in Customer Journey Analytics te selecteren
description: Beschrijft hoe te om de kalender, het rollen data, en douaneuitdrukkingen in Report Builder voor Customer Journey Analytics te gebruiken
role: User
feature: Report Builder
type: Documentation
exl-id: 7252214f-a7d6-451b-99c9-d39e8e47120b
solution: Customer Journey Analytics
source-git-commit: c56c77079aa21fb740fda6bec333731a1f82a48f
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# Een datumbereik selecteren

Als u het datumbereik van een bestaand gegevensblok wilt wijzigen, selecteert u Een gegevensblok bewerken of gebruikt u het deelvenster SNEL BEWERKEN.

Gebruik de volgende opties om een datumbereik voor een gegevensblok te wijzigen.

**Kalender**

Met de kalender kunt u statische of roldatums maken met behulp van de volgende opties:

- Datumbereik
- Kalender
- Vervolgkeuzemenu Voorinstelling
- Modus Roldatum
- Expressies aanpassen


**van cel**

Met de optie Van cel kunt u verwijzen naar datums die zijn ingevoerd in werkbladcellen.

U kunt vandaag uitsluiten voor elk geselecteerd datumbereik.

![ Report Builder Snel uitgeeft ruit met geselecteerde kalender en sluit vandaag geselecteerd uit.](./assets/image17.png)

## De kalender gebruiken

Wanneer u **Kalender** gebruikt, toont het gebied van de datumwaaier de huidige datumwaaier voor het verzoek van het gegevensblok. U kunt datums rechtstreeks invoeren in het veld met het datumbereik of een optie voor het selecteren van het datumbereik gebruiken.

### Datumbereik

Datums rechtstreeks invoeren in het veld Datumbereik

1. Klik op het veld voor het datumbereik naast het kalenderpictogram.

1. Voer de begin- en einddatum voor het datumbereik in.

### Kalender

Datums selecteren met de kalender

1. Klik op het kalenderpictogram om een maandkalender weer te geven.

1. Klik op een begindatum.

1. Klik op een einddatum.

Als u een datumbereik in omgekeerde volgorde wilt instellen, klikt u eerst op de einddatum en vervolgens op de begindatum.

![ de waaierruit van de de datumwaaier die van de Report Builder de kalender en de einddatum en de geselecteerde begindatum toont.](./assets/image18.png)

### Vervolgkeuzelijst Voorinstelling

Het keuzemenu met voorinstellingen bevat een standaardset vooraf ingestelde datumbereiken en componenten voor het datumbereik voor een gegevensweergave die u hebt opgeslagen of een gegevensweergave die met u is gedeeld.

### Roldatums

Met de optie voor roldatums kunt u een datumbereik selecteren met roldatums.

1. Selecteer **Gebruik het rollen data**.

1. Selecteer een roluitdrukking voor uw begin en of einddatum.

   ![ Report Builder de ruit van de datumwaaier die het Gebruik het rollen geselecteerde data en de het rollen uitdrukking tonen.](./assets/image19.png)

   **Begin van** - staat u toe om het begin van een dag, een week, een maand, een kwartaal, of een jaar te selecteren.

   **Eind van** - staat u toe om het eind van een dag, een week, een maand, een kwartaal, of een jaar te selecteren.

   **Vaste dag** - staat u toe om een begin of einddatum te bevestigen terwijl de andere datum rolt.

1. Kies dag, week, maand, kwartaal of jaar als de rolperiode.

   ![ de waaierruit van de de datumwaaier die van de Report Builder de huidige geselecteerde dag toont.](./assets/image20.png)

1. Voeg dagen, weken, maanden, kwartalen of jaren toe of trek deze af vanaf de roldatum.

   ![ Report Builder de ruit van de datumwaaier die de huidige dag plus 14 geselecteerde dagen toont.](./assets/image21.png)

1. Klik op Volgende om het datumbereik te definiëren.

   Gebruik de datumvoorvertoning om te bevestigen dat het resulterende datumbereik het gewenste bereik is.

### Aangepaste expressies

Met de optie voor aangepaste expressies kunt u het datumbereik wijzigen door een aangepaste expressie te maken of een rekenkundige formule in te voeren.

1. Selecteer **Gebruik het rollen data**.

1. Selecteer **de douaneuitdrukking van het Gebruik**.

   Wanneer u de **optie van de douaneuitdrukking van het Gebruik** selecteert, zijn de standaard het rollen controles van de datumwaaier gehandicapt.

   ![ Uitgezochte douaneuitdrukking van het Gebruik die tm-1m aan td-1d tonen.](./assets/custom_expression.png)

1. Voer een aangepaste expressie in.

   Voor een steekproeflijst van douaneuitdrukkingen, zie **uitdrukkingen van de Datum**.

1. Gebruik de datumvoorvertoning om te controleren of het resulterende datumbereik het gewenste bereik is.

#### Een aangepaste expressie maken

1. Ga de verwijzing van de a **Datum** in.

1. Voeg **exploitanten van de Datum** toe om de datum naar het verleden of de toekomst te bewegen.

U kunt een aangepaste datumexpressie invoeren die meerdere operatoren bevat, zoals ```tm-11m-1d``` .

#### Datumverwijzingen

In de volgende tabel staan voorbeelden van datumverwijzingen.

| Datumverwijzing | Type | Beschrijving |
|----------------|--------------|----------------------------|
| 01-01-10 | Statische datum | Ingevoerd in ISO-datumnotatie |
| td | Roldatum | Begin van huidige dag |
| tw | Roldatum | Begin van huidige week |
| tm | Roldatum | Begin van huidige maand |
| tq | Roldatum | Begin van het lopende kwartaal |
| ty | Roldatum | Begin van het lopende jaar |

#### Datumoperatoren

In de volgende tabel worden voorbeelden van datumoperatoren weergegeven.

| Datumoperatoren | Eenheid | Beschrijving |
|----------------|---------|--------------------|
| +6d | Dag | 6 dagen toevoegen aan de datumreferentie |
| +1w | Week | Eén volledige week toevoegen aan de Date Reference |
| -2 m | Maand | 2 volledige maanden aftrekken van de datumreferentie |
| -4q | Kwart | Vier kwartalen aftrekken van de datumreferentie |
| -1 y | Jaar | Eén jaar aftrekken van de datumreferentie |

#### Datumexpressies

In de volgende tabel staan voorbeelden van datumexpressies.

| Datumuitdrukking | Betekenis |
|-----------------|--------------------------------------|
| td-1w | Eerste dag van vorige week |
| tm-1d | Laatste dag van vorige maand |
| td-52w | Dezelfde dag, 52 weken geleden |
| tm-11m-1d | Laatste dag van dezelfde maand vorig jaar |
| 2020-09-06 | 9 september 2020 |

## Datumbereik van cel

Het datumbereik kan worden opgegeven in werkbladcellen. Gebruik de **waaier van de Datum van cel** optie om het begin en einddatum van het gegevensblok van geselecteerde cellen te kiezen. Wanneer u **van cel** optie selecteert, toont het paneel **van** en **aan** gebieden waar u een celplaats kunt ingaan.

![ Uitgezocht van cel Sheet1!H4 aan Sheet1!I4 ](./assets/image23.png)

## Vandaag uitsluiten

Kies **vandaag uitsluiten** optie om vandaag van een geselecteerde datumwaaier uit te sluiten. Als u vandaag kiest voor opname, worden mogelijk onvolledige gegevens gebruikt voor vandaag.

Wanneer geselecteerd, sluit **vandaag** optie uit sluit de huidige dag van alle wijzen van de datumwaaier met inbegrip van kalender, het rollen data, of douaneuitdrukkingen uit.

## Geldige datumbereiken

In de volgende lijst worden geldige datumbereikindelingen beschreven.

- De begin- en einddatum moeten de volgende notatie hebben: JJJJ-MM-DD

- De begindatum moet eerder zijn dan de einddatum. Beide datums kunnen op de toekomst worden ingesteld.

- Wanneer u roldatums gebruikt, moet de begindatum vandaag of in het verleden zijn. Het moet in het verleden zijn als **vandaag uitsluiten** wordt gecontroleerd.

- U kunt een statisch datumbereik maken dat is ingesteld voor de toekomst. Het kan bijvoorbeeld nodig zijn een datum in te stellen voor een marketingcampagne die volgende week wordt gestart. Deze optie leidt tot een werkboek controle voor een campagne vooruit.

## Het datumbereik wijzigen

U kunt het datumbereik van een bestaand gegevensblok bewerken door Gegevensblok bewerken te selecteren in het deelvenster OPDRACHTEN of door de koppeling voor het datumbereik te selecteren in het deelvenster SNEL BEWERKEN.

**geeft gegevensblok** uit - staat u toe om veelvoudige parameters van het gegevensblok, met inbegrip van datumwaaier, voor één enkel gegevensblok uit te geven.

**Snel geeft uit: De waaier van de Datum** - staat u toe om de datumwaaier van één of meerdere gegevensblokken uit te geven.

Het datumbereik bewerken via het deelvenster SNEL BEWERKEN

1. Selecteer cellen in een of meer gegevensblokken in een werkblad.

1. Klik de **waaier van de Datum** verbinding in het SNEL EDIT paneel.

1. Selecteer het datumbereik met een van de opties voor datumselectie.

1. Klik **toepassen**.


Report Builder past het nieuwe datumbereik toe op alle gegevensblokken in de selectie.
