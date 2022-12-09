---
title: Bindingsafmetingen en metriek gebruiken in CJA
description: Kenmerkafmetingen voor complexe persistentieanalyse naar objectarrays.
exl-id: 5e7c71e9-3f22-4aa1-a428-0bea45efb394
feature: Use Cases
source-git-commit: dbb7edae43fdc970cacf5863ecd13df75deaefad
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 1%

---


# Bindingsafmetingen en metriek gebruiken in CJA

Customer Journey Analytics biedt verschillende manieren om waarden van dimensies aan te houden voorbij de hit waarop ze zijn ingesteld. Een van de persistentiemethoden die Adobe aanbiedt, wordt Binding genoemd. In vorige versies van Adobe Analytics werd dit concept ook wel &#39;merchandising&#39; genoemd.

Hoewel u bindingsdimensies kunt gebruiken met gebeurtenisgegevens op hoofdniveau, kunt u dit concept het beste gebruiken wanneer u werkt met [Objectarrays](/help/use-cases/object-arrays.md). U kunt een dimensie aan één deel van een objecten serie zonder het op alle attributen in een bepaalde gebeurtenis toe te passen toeschrijven. U kunt bijvoorbeeld een zoekterm aan één product in de array met winkelwagentobjecten toewijzen zonder die zoekterm aan de gehele gebeurtenis te binden.

## Voorbeeld 1: Bindingsdimensies gebruiken om aanvullende productkenmerken aan een aankoop toe te wijzen

U kunt dimensie-items binnen een objectarray aan een andere dimensie binden. Wanneer het gebonden afmetingspunt verschijnt, herinnert CJA de gebonden dimensie en omvat het in de gebeurtenis voor u. Overweeg de volgende klantenreis:

1. Een bezoeker bekijkt een productpagina op een wasmachine.

   ```json
   {
       "PersonID": "1",
       "product": [
           {
               "name": "Washing Machine 2000",
               "color": "white",
               "type": "front loader",
           },
       ],
       "timestamp": 1534219229
   }
   ```

1. De bezoeker bekijkt dan een productpagina op een droger.

   ```json
   {
       "PersonID": "1",
       "product": [
           {
               "name": "Dryer 2000",
               "color": "neon orange",
           },
       ],
       "timestamp": 1534219502
   }
   ```

1. Uiteindelijk kopen ze. De kleur van elk product is niet opgenomen in de aankoopgebeurtenis.

   ```json
   {
       "PersonID": "1",
       "orders": 1,
       "product": [
           {
               "name": "Washing Machine 2000",
               "price": 1600,
           },
           {
               "name": "Dryer 2000",
               "price": 499
           }
       ],
       "timestamp": 1534219768
   }
   ```

Als u omzet door kleur zonder een bindende dimensie wilt bekijken, de dimensie `product.color` De kleur van de droger blijft behouden en krijgt een onjuiste waarde:

| product.color | omzet |
| --- | --- |
| neonoranje | 2099 |

U kunt in de Manager van de Mening van Gegevens gaan en productkleur binden aan productnaam:

![Dimensie binding](../assets/binding-dimension.png)

Wanneer u dit persistentiemodel instelt, neemt CJA nota van de productnaam wanneer de productkleur wordt ingesteld. Wanneer het de zelfde productnaam in een volgende gebeurtenis voor deze bezoeker herkent, wordt de productkleur ook gebracht. Dezelfde gegevens wanneer u een productkleur bindt aan de productnaam, zien er als volgt uit:

| product.color | omzet |
| --- | --- |
| wit | 1600 |
| neonoranje | 499 |

## Voorbeeld 2: Gebruik bindingsmetriek om zoekterm aan een productaankoop te koppelen

Een van de meest gebruikte handelsmethoden in Adobe Analytics is het binden van een zoekterm aan een product, zodat elke zoekterm krediet krijgt voor het juiste product. Overweeg de volgende klantenreis:

1. Een bezoeker arriveert op uw site en zoekt naar &quot;bokshandschoenen&quot;. De metrische toename van zoekopdrachten wordt met één verhoogd en de bovenste drie zoekresultaten worden weergegeven.

   ```json
   {
       "PersonID": "1",
       "page_name": "Search results",
       "search": "1",
       "search_term": "boxing gloves",
       "product": [
           {
               "name": "Beginner gloves",
           },
           {
               "name": "Tier 3 gloves",
           },
           {
               "name": "Professional gloves",
           }
       ]
   }
   ```

2. Ze vinden een paar handschoenen die ze leuk vinden en voegen het toe aan hun kar.

   ```json
   {
       "PersonID": "1",
       "page_name": "Shopping cart",
       "cart_add": "1",
       "product": [
           {
               "name": "Tier 3 gloves",
           }
       ]
   }
   ```

3. De bezoeker zoekt vervolgens naar &quot;tennisracket&quot;. De metrische toename van zoekopdrachten wordt met één verhoogd en de bovenste drie zoekresultaten worden weergegeven.

   ```json
   {
       "PersonID": "1",
       "page_name": "Search results",
       "search": "1",
       "search_term": "tennis racket",
       "product": [
           {
               "name": "Shock absorb racket",
           },
           {
               "name": "Women's open racket",
           },
           {
               "name": "Extreme racket",
           }
       ]
   }
   ```

4. Ze vinden een racket die ze leuk vinden en voegen het toe aan hun winkelwagen.

   ```json
   {
       "PersonID": "1",
       "page_name": "Shopping cart",
       "cart_add": "1",
       "product": [
           {
               "name": "Tier 3 gloves",
           },
           {
               "name": "Shock absorb racket",
           }
       ]
   }
   ```

5. De bezoeker zoekt een derde keer naar &quot;schoenen&quot;. De metrische toename van zoekopdrachten wordt met één verhoogd en de bovenste drie zoekresultaten worden weergegeven.

   ```json
   {
       "PersonID": "1",
       "page_name": "Search results",
       "search": "1",
       "search_term": "shoes",
       "product": [
           {
               "name": "Men's walking shoes",
           },
           {
               "name": "Tennis shoes",
           },
           {
               "name": "Skate shoes",
           }
       ]
   }
   ```

6. Ze vinden een paar schoenen die ze leuk vinden en voegen het toe aan hun winkelwagen.

   ```json
   {
       "PersonID": "1",
       "page_name": "Shopping cart",
       "cart_add": "1",
       "product": [
           {
               "name": "Tier 3 gloves",
           },
           {
               "name": "Shock absorb racket",
           },
           {
               "name": "Skate shoes",
           }
       ]
   }
   ```

7. De bezoeker doorloopt het afrekenproces en koopt deze drie objecten.

   ```json
   {
       "PersonID": "1",
       "page_name": "Thank you for your purchase",
       "purchase": "1",
       "product": [
           {
               "name": "Tier 3 gloves",
               "price": "89.99"
           },
           {
               "name": "Shock absorb racket",
               "price": "34.99"
           },
           {
               "name": "Skate shoes",
               "price": "79.99"
           }
       ]
   }
   ```

Als u een toewijzingsmodel gebruikt dat geen bindende dimensie met onderzoekstermijn omvat, kenmerken alle drie producten opbrengst aan slechts één enkele onderzoekstermijn. Als u bijvoorbeeld Originele toewijzing hebt gebruikt met de zoekterm dimensie:

| search_term | omzet |
| --- | --- |
| bokshandschoenen | $ 204,97 |

Als u Recentste toewijzing met de dimensie van de onderzoekstermijn gebruikte, kenmerken alle drie producten nog opbrengst aan één enkele onderzoekstermijn:

| search_term | omzet |
| --- | --- |
| schoenen | $ 204,97 |

Hoewel dit voorbeeld slechts één bezoeker omvat, kunnen veel bezoekers die naar verschillende dingen zoeken, zoektermen verkeerd aan verschillende producten toeschrijven, waardoor het moeilijk wordt te bepalen wat de beste zoekresultaten eigenlijk zijn.

U kunt onderzoekstermen aan productnaam binden wanneer metrisch van Zoekopdrachten aanwezig is om correct onderzoeksterm aan opbrengst te Attribueren.

![Metrische binding](../assets/binding-metric.png)

In Analysis Workspace zou het resulterende verslag er als volgt uitzien:

| search_term | omzet |
| --- | --- |
| bokshandschoenen | $ 89,99 |
| tennisracket | $ 34,99 |
| schoenen | $ 79,99 |

CJA detecteert automatisch de relatie tussen de geselecteerde dimensie en de bindingsdimensie. Wanneer de bindingsdimensie zich in een objectenarray bevindt terwijl de geselecteerde dimensie zich op een hoger niveau bevindt, is een bindingsmetrische waarde vereist. Een bindende metrische handelingen als trekker voor een bindende afmeting, zodat bindt het zich slechts aan gebeurtenissen waar metrisch binden aanwezig is. In het bovenstaande voorbeeld bevat de pagina met zoekresultaten altijd een zoekterm en een metrische zoekopdracht.

Als u de zoekterm instelt op dit persistentiemodel, wordt de volgende logica uitgevoerd:

* Wanneer de dimensie van de zoekterm is ingesteld, controleert u of de productnaam aanwezig is.
* Als de productnaam er niet is, doet u niets.
* Als de productnaam er is, controleer de aanwezigheid van metrisch onderzoek.
* Als de metrische zoekopdracht er niet is, doet u niets.
* Als metrische zoekopdrachten daar zijn, bindt u de zoekterm aan alle productnamen in die gebeurtenis. Het kopieert zich tot het zelfde niveau zoals productnaam voor die gebeurtenis. In dit voorbeeld wordt het behandeld als product.search_term.
* Als dezelfde productnaam in een volgende gebeurtenis wordt weergegeven, wordt de gebonden zoekterm ook naar die gebeurtenis overgedragen.

## Voorbeeld 3: Zoekterm voor video binden aan gebruikersprofiel

U kunt een zoekterm aan een gebruikersprofiel binden, zodat de persistentie tussen de profielen volledig gescheiden blijft. Uw organisatie voert bijvoorbeeld een streamingservice uit waarbij een overkoepelende account meerdere profielen kan hebben. De bezoeker heeft een onderliggend profiel en een profiel voor volwassenen.

1. De account meldt zich aan onder het onderliggende profiel en zoekt naar de tv-show van een kind. De `"ProfileID"` is `2` om het onderliggende profiel te vertegenwoordigen.

   ```json
   {
       "PersonID": "7078",
       "ProfileID": "2",
       "Searches": "1",
       "search_term": "kids show"
   }
   ```

1. Ze vinden de show &quot;Orangey&quot; en spelen hem zodat hun kind het kan bekijken.

   ```json
   {
       "PersonID": "7078",
       "ProfileID": "2",
       "ShowName": "Orangey",
       "VideoStarts": "1"
   }
   ```

1. Later die avond schakelt de bovenliggende toepassing over naar het profiel en zoekt deze naar inhoud voor volwassenen. De `"ProfileID"` is `1` om het profiel voor volwassenen te vertegenwoordigen. Beide profielen maken deel uit van dezelfde account, voorgesteld door hetzelfde `"PersonID"`.

   ```json
   {
       "PersonID": "7078",
       "ProfileID": "1",
       "Searches": "1",
       "search_term": "grownup movie"
   }
   ```

1. Zoek naar de show &quot;Analytics After Hours&quot; en geniet van hun avondeten.

   ```json
   {
       "PersonID": "7078",
       "ProfileID": "1",
       "ShowName": "Analytics After Hours",
       "VideoStarts": "1"
   }
   ```

1. De volgende dag zetten ze de show &quot;Orangey&quot; voor hun kind voort. Ze hoeven niet te zoeken omdat ze nu al op de hoogte zijn van de show.

   ```json
   {
       "PersonID": "7078",
       "ProfileID": "2",
       "ShowName": "Orangey",
       "VideoStarts": "1"
   }
   ```

Als u Recentste toewijzing gebruikt bij Person-vervaldatum, kunt u de optie `"grownup movie"` zoekterm wordt toegeschreven aan de laatste weergave van de show van het kind .

| Zoekterm | Video start |
| --- | --- |
| gegroeide film | 2 |
| kindershow | 1 |

Als u echter gebonden bent `search_term` tot `ProfileID`, worden de zoekopdrachten van elk profiel geïsoleerd naar hun eigen profiel, omdat de juiste zoekopdrachten naar dit profiel worden verwezen.

![Bezoekersbinding](../assets/binding-visitor.png)

Analysis Workspace zou de tweede aflevering van Orangey correct aan de zoekterm toewijzen `"kids show"` zonder rekening te houden met zoekopdrachten uit andere profielen.

| Zoekterm | Video start |
| --- | --- |
| kindershow | 2 |
| gegroeide film | 1 |

## Voorbeeld 4: Evalueer browse vs. onderzoeksgedrag in een detailhandelplaatsen

U kunt waarden binden aan dimensies die zijn ingesteld bij vorige gebeurtenissen. Wanneer u een variabele met een bindende afmeting plaatst, houdt CJA rekening met de persisted waarde. Als dit ongewenste gedrag is, kunt u de persistentie-instellingen van de bindende dimensie aanpassen. Neem het volgende voorbeeld waar `product_finding_method` wordt ingesteld op een gebeurtenis en vervolgens gebonden aan de gebeurtenis &#39;Winkelwagentjes toevoegen&#39; op de volgende gebeurtenis.

1. Een bezoeker voert een zoekopdracht uit naar `"camera"`. Er zijn geen producten ingesteld op deze pagina.

   ```json
   {
       "search_term": "camera",
       "product_finding_method": "search"
   }
   ```

1. Ze klikken op een camera die ze leuk vinden en voegen deze toe aan hun winkelwagentje.

   ```json
   {
       "Product": [
           {
               "name": "DSLR Camera"
           }
       ],
       "CartAdd": "1"
   }
   ```

1. De bezoeker bladert dan in de categorie van de mangordels zonder een onderzoek uit te voeren. Er zijn geen producten ingesteld op deze pagina.

   ```json
   {
       "category": "Men's belts",
       "product_finding_method": "browse"
   }
   ```

1. Ze klikken op een gordel die ze leuk vinden en voegen het toe aan hun wagen.

   ```json
   {
       "Product": [
           {
               "name": "Ratchet belt"
           }
       ],
       "CartAdd": "1"
   }
   ```

1. Ze doorlopen het afrekenproces en kopen deze twee objecten.

   ```json
   {
       "Product": [
           {
               "name": "DSLR Camera",
               "price": "399.99"
           },
           {
               "name": "Ratchet belt",
               "price": "19.99"
           }
       ],
       "Purchase": "1"
   }
   ```

Als de persistentie wordt ingesteld op de meest recente toewijzing zonder een bindende dimensie, wordt alle $419,98 aan inkomsten toegewezen aan de `browse` zoekmethode.

| Productzoekmethode | Omzet |
| --- | --- |
| doorbladeren | 419,98 |

Als persistentie wordt ingesteld met behulp van de oorspronkelijke toewijzing zonder een bindende dimensie, wordt alle $419,98 aan inkomsten toegewezen aan de `search` zoekmethode.

| Productzoekmethode | Omzet |
| --- | --- |
| zoeken | 419,98 |

Als u echter bindt `product_finding_method` Aan de Kaart voegt metrisch toe, kenmerkt het resulterende rapport elk product aan de correcte het vinden methode.

| Productzoekmethode | Omzet |
| --- | --- |
| zoeken | 399,99 |
| doorbladeren | 19,99 |
