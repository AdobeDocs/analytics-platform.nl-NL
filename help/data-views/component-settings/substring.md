---
title: Instellingen van subtekenreeksen
description: Gebruik een subset van een tekenreeks als dimensie-items.
solution: Customer Journey Analytics
feature: Data Views
exl-id: a763027e-68f7-4f0a-8082-85db5283c8e3
source-git-commit: 20135c39341eebbf680783ad0e71bf6c62e5377b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!UICONTROL Substring] componentinstellingen

[!UICONTROL Substring] met componentinstellingen kunt u meerdere tekenreeksmanipulatiemethoden uitvoeren om de gewenste dimensie-items in rapporten op te halen.

![Instellingen voor subtekenreeks](../assets/substring-settings.png)

[!UICONTROL Substring] is alleen beschikbaar voor dimensies en is retroactief voor de gegevens waarop deze worden toegepast. Het is een directe gegevenstransformatie die gebeurt alvorens het filtreren of andere analyseverrichtingen worden toegepast.

## Van links/rechts

Neem een deel van een tekenreeks op basis van zijn positie naar het begin of einde van een tekenreeks. **[!UICONTROL From the Left]** en **[!UICONTROL From the Right]** de methodes verstrekken twee drop-down lijsten: **[!UICONTROL From]** (waar de uitvoer begint) en **[!UICONTROL To]** (waar de uitvoer eindigt).

* **[!UICONTROL String Start]**: Het begin van de tekenreeks.
* **[!UICONTROL String End]**: Het einde van de tekenreeks.
* **[!UICONTROL Position]**: Een statisch aantal tekens van links of rechts, afhankelijk van de methode.
* **[!UICONTROL String]**: Pas een teken of reeks tekens aan om het begin of einde van een tekenreeks aan te geven. Deze vervolgkeuzelijst toont ook extra opties:
   * **[!UICONTROL Match]**: De tekenreeks die moet overeenkomen. Als de invoer niet overeenkomt met dit veld, [Geen waardeopties](no-value-options.md) van toepassing.
   * **[!UICONTROL Index]**: De **[!UICONTROL Match]** criteria kunnen meerdere keren voorkomen in een tekenreeks. Dit geheel getal bepaalt welke overeenkomst wordt gebruikt om de uitvoer te starten of te beëindigen, afhankelijk van de methode. Bijvoorbeeld een index van `1` vertegenwoordigt de eerste gelijke. Als de index hoger is dan het aantal beschikbare overeenkomsten, [Geen waardeopties](no-value-options.md) van toepassing.
   * **[!UICONTROL Include String]**: Een selectievakje dat het **[!UICONTROL Match]** tekenreeks in de uitvoer indien ingeschakeld.
* **[!UICONTROL Length]**: Een geheel getal dat het aantal tekens opgeeft dat na de startpositie van de uitvoer moet worden opgenomen. Alleen beschikbaar onder **[!UICONTROL To]** vervolgkeuzelijst.

## Scheidingsteken

Gebruik deze methode voor velden die een scheidingsteken gebruiken om meerdere tekenreekswaarden van elkaar te scheiden. U kunt een afzonderlijk element extraheren om als uitvoer te gebruiken of de tekenreeks omzetten in een element in een arrayschema van een object.

* **[!UICONTROL Criterion]**: Hoe u de lijst met gescheiden waarden wilt behandelen.
   * **[!UICONTROL From the Left]**: Begin bij het begin van de lijst met scheidingstekens en tel vooruit.
   * **[!UICONTROL From the Right]**: Begin vanaf het einde van de lijst met scheidingstekens en tel terug.
   * **[!UICONTROL Convert to array]**: Behandel deze dimensie alsof het een schemaelement van de objecten serie is.
* **[!UICONTROL Delimiter]**: Het scheidingsteken dat in het veld wordt gebruikt.
* **[!UICONTROL Index]**: Alleen aanwezig als het criterium Van links/rechts is. Het elementnummer alsof het zich in een array bevindt. Als de tekenreeksinvoer bijvoorbeeld `"Fox,Turtle,Rabbit,Wolf"` met een index van 3, is de uitvoer `"Rabbit"`. Als de index hoger is dan het aantal gescheiden elementen, [Geen waardeopties](no-value-options.md) van toepassing.

## URL-parsering

Voor gebruik met velden die URL&#39;s bevatten. De voorbeeld-URL gebruiken `https://example.com/store/index.html?cid=campaign#cart`zijn de volgende opties beschikbaar:

* **[!UICONTROL Get protocol]**: Haal het URL-protocol op. Bijvoorbeeld, `"https://"`.
* **[!UICONTROL Get host]**: Haal de host van de URL op. Bijvoorbeeld, `"example.com"`.
* **[!UICONTROL Get path]**: Haal het pad van de URL op. Bijvoorbeeld, `"store/index.html"`.
* **[!UICONTROL Get query string value]**: Haal de waarde op uit één querytekenreeks. Plaats de gewenste parameter voor de queryreeks in het dialoogvenster **[!UICONTROL Query key]** veld. Als de bovenstaande URL wordt gebruikt met de `"cid"` querysleutel, de uitvoer is `"campaign"`.
* **[!UICONTROL Get hash value]**: Hiermee wordt de hashwaarde van de URL opgehaald. Bijvoorbeeld, `"cart"`.

Als de invoer geen geldige URL is of als de gewenste URL-component niet aanwezig is, [Geen waardeopties](no-value-options.md) van toepassing.

## Verkleinen

Witruimte of speciale tekens uit de tekenreeks bijsnijden.

* **[!UICONTROL Trim whitespaces]**: Een selectievakje waarmee alle witruimte aan het begin en einde van de tekenreeks wordt verwijderd, indien ingeschakeld.
* **[!UICONTROL Trim special characters]**: Een selectievakje dat een **[!UICONTROL Special characters]** invoerveld indien ingeschakeld. Alle tekens in dit veld worden uit de uitvoer verwijderd. Multi-bytetekens worden niet ondersteund.

## Regex

Pas reguliere expressies toe op een dimensie om de gewenste waarde op te halen.

* **[!UICONTROL Regex]**: De reguliere-expressieformule.
* **[!UICONTROL Output format]**: Een optioneel veld waarmee u tekst kunt toevoegen of de volgorde van de uitvoer van de regex-subgroep kunt wijzigen. Als dit veld leeg is, is de tekenreeksuitvoer de geëvalueerde regex-expressie.
* **[!UICONTROL Case sensitive]**: Een selectievakje waarmee de reguliere expressie, indien ingeschakeld, hoofdlettergevoelig wordt gemaakt.

CJA gebruikt een subset van de Perl regex syntaxis. Als de invoer niet overeenkomt met de reguliere expressie en de **[!UICONTROL Output format]** leeg is, [Geen waardeopties](no-value-options.md) van toepassing. De volgende expressies worden ondersteund:

| Uitdrukking | Beschrijving |
| --- | --- |
| `a` | Eén teken `a`. |
| `a|b` | Eén teken `a` of `b`. |
| `[abc]` | Eén teken `a`, `b`, of `c`. |
| `[^abc]` | Elk enkel teken behalve `a`, `b`, of `c`. |
| `[a-z]` | Eén teken in het bereik van `a`-`z`. |
| `[a-zA-Z0-9]` | Eén teken in het bereik van `a`-`z`, `A`-`Z`, of cijfers `0`-`9`. |
| `^` | Komt overeen met het begin van de regel. |
| `$` | Komt overeen met het einde van de regel. |
| `\A` | Begin van tekenreeks. |
| `\z` | Einde van tekenreeks. |
| `.` | Komt overeen met elk willekeurig teken. |
| `\s` | Willekeurig teken voor witruimte. |
| `\S` | Willekeurig teken zonder spatie. |
| `\d` | Willekeurig cijfer. |
| `\D` | Willekeurig niet-cijfer. |
| `\w` | Een letter, cijfer of onderstrepingsteken. |
| `\W` | Willekeurig niet-woordteken. |
| `\b` | Elke woordgrens. |
| `\B` | Willekeurig teken dat geen woordgrens is. |
| `\<` | Begin van woord. |
| `\>` | Einde van woord. |
| `(...)` | Leg alles vast. |
| `(?:...)` | Niet-markeren vastleggen. Voorkomt dat in de uitvoertekenreeks naar de overeenkomst wordt verwezen. |
| `a?` | Nul of één van `a`. |
| `a*` | Nul of meer van `a`. |
| `a+` | Eén of meer van `a`. |
| `a{3}` | Precies 3 van `a`. |
| `a{3,}` | 3 of meer van `a`. |
| `a{3,6}` | Tussen 3 en 6 van `a`. |

Plaatsaanduidingen voor uitvoer worden ook ondersteund. U kunt deze reeksen gebruiken in het dialoogvenster **[!UICONTROL Output format]** om het even welk aantal tijden en in om het even welke orde om de gewenste koordoutput te bereiken.

| Tijdelijke plaatsaanduidingsreeks uitvoeren | Beschrijving |
| --- | --- |
| `$&` | Hiermee wordt uitgevoerd wat overeenkomt met de gehele expressie. |
| `$n` | Hiermee wordt uitgevoerd wat overeenkomt met de nde subexpressie. Bijvoorbeeld: `$1` Hiermee wordt de eerste subexpressie uitgevoerd. |
| ``$` `` | Hiermee wordt de tekst uitgevoerd tussen het einde van de laatste gevonden overeenkomst (of het begin van de tekst als er geen vorige overeenkomst is gevonden) en het begin van de huidige overeenkomst. |
| `$+` | Hiermee wordt uitgevoerd wat overeenkomt met de laatst gemarkeerde subexpressie in de reguliere expressie. |
| `$$` | Hiermee wordt het teken van de tekenreeks uitgevoerd `"$"`. |

{style="table-layout:auto"}
