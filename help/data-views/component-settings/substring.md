---
title: Instellingen van subtekenreeksen
description: Gebruik een subset van een tekenreeks als dimensie-items.
solution: Customer Journey Analytics
feature: Data Views
exl-id: a763027e-68f7-4f0a-8082-85db5283c8e3
role: Admin
source-git-commit: a236b2126c4b998b4d97caab014556e3ee3a9e83
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# Instellingen van subtekenreeksen {#substring-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_dimension_substring"
>title="Subtekenreeks"
>abstract="Extraheer delen van een tekenreeks met regels of reguliere expressies."

<!-- markdownlint-enable MD034 -->


Met de instellingen van de component [!UICONTROL Substring] kunt u meerdere tekenreeksmanipulatiemethoden uitvoeren om de gewenste dimensie-items in rapporten op te halen.

![ montages Substring ](../assets/substring-settings.png)

[!UICONTROL Substring] is alleen beschikbaar voor dimensies en is retroactief voor de gegevens waarop het is toegepast. Het is een directe gegevenstransformatie die gebeurt alvorens het filtreren of andere analyseverrichtingen worden toegepast.

## Van links/rechts

Neem een deel van een tekenreeks op basis van zijn positie naar het begin of einde van een tekenreeks. De methoden **[!UICONTROL From the Left]** en **[!UICONTROL From the Right]** bevatten twee vervolgkeuzelijsten: **[!UICONTROL From]** (waar de uitvoer begint) en **[!UICONTROL To]** (waar de uitvoer eindigt).

* **[!UICONTROL String Start]**: Het begin van de tekenreeks.
* **[!UICONTROL String End]**: Het einde van de tekenreeks.
* **[!UICONTROL Position]**: Een statisch aantal tekens van links of rechts, afhankelijk van de methode.
* **[!UICONTROL String]**: Identiek aan een teken of reeks tekens om het begin of einde van een tekenreeks aan te geven. In deze vervolgkeuzelijst worden ook extra opties weergegeven:
   * **[!UICONTROL Match]**: De tekenreeks die moet overeenkomen. Als de input geen gelijke met dit gebied heeft, [ Geen waardeopties ](no-value-options.md) zijn van toepassing.
   * **[!UICONTROL Index]**: De criteria van **[!UICONTROL Match]** kunnen meerdere keren in een tekenreeks voorkomen. Dit geheel getal bepaalt welke overeenkomst wordt gebruikt om de uitvoer te starten of te beëindigen, afhankelijk van de methode. Een index van `1` vertegenwoordigt bijvoorbeeld de eerste overeenkomst. Als de index hoger is dan het aantal beschikbare gelijken, [ Geen waardeopties ](no-value-options.md) zijn van toepassing.
   * **[!UICONTROL Include String]**: Een selectievakje dat de **[!UICONTROL Match]** -tekenreeks indien ingeschakeld in de uitvoer opneemt.
* **[!UICONTROL Length]**: Een geheel getal dat het aantal tekens opgeeft dat na de startpositie van de uitvoer moet worden opgenomen. Alleen beschikbaar in de vervolgkeuzelijst **[!UICONTROL To]** .

## Scheidingsteken

Gebruik deze methode voor velden die een scheidingsteken gebruiken om meerdere tekenreekswaarden van elkaar te scheiden. U kunt een afzonderlijk element extraheren om als uitvoer te gebruiken of de tekenreeks omzetten in een element in een arrayschema van een object.

* **[!UICONTROL Criterion]**: Hoe u de lijst met gescheiden waarden wilt behandelen.
   * **[!UICONTROL From the Left]**: begin vanaf het begin van de lijst met scheidingstekens en tel vooruit.
   * **[!UICONTROL From the Right]**: begin vanaf het einde van de lijst met scheidingstekens en tel terug.
   * **[!UICONTROL Convert to array]**: Behandel deze dimensie alsof het een element in een schema van de objectarray is.
* **[!UICONTROL Delimiter]**: Het scheidingsteken dat in het veld wordt gebruikt.
* **[!UICONTROL Index]**: Alleen aanwezig als het criterium Van links/rechts is. Het elementnummer alsof het zich in een array bevindt. Als de tekenreeksinvoer bijvoorbeeld `"Fox,Turtle,Rabbit,Wolf"` is met index 3, is de uitvoer `"Rabbit"` . Als de index hoger is dan het aantal afgebakende elementen, [ Geen waardeopties ](no-value-options.md) zijn van toepassing.

## URL-parsering

Voor gebruik met velden die URL&#39;s bevatten. Met de voorbeeld-URL `https://example.com/store/index.html?cid=campaign#cart` zijn de volgende opties beschikbaar:

* **[!UICONTROL Get protocol]**: Haal het URL-protocol op. Bijvoorbeeld `"https://"` .
* **[!UICONTROL Get host]**: Haal de host van de URL op. Bijvoorbeeld `"example.com"` .
* **[!UICONTROL Get path]**: haal het pad van de URL op. Bijvoorbeeld `"store/index.html"` .
* **[!UICONTROL Get query string value]**: Haal de waarde op uit één queryreeks. Plaats de gewenste parameter voor de querytekenreeks in het veld **[!UICONTROL Query key]** . Als de bovenstaande URL wordt gebruikt met de query-toets `"cid"` , is de uitvoer `"campaign"` .
* **[!UICONTROL Get hash value]**: verwijder de hashwaarde van de URL. Bijvoorbeeld `"cart"` .

Als de input geen geldige URL is of als de gewenste component URL niet aanwezig is, [ Geen waardeopties ](no-value-options.md) zijn van toepassing.

## Verkleinen

Witruimte of speciale tekens uit de tekenreeks bijsnijden.

* **[!UICONTROL Trim whitespaces]**: Een selectievakje waarmee alle witruimte aan het begin en einde van de tekenreeks wordt verwijderd als deze is ingeschakeld.
* **[!UICONTROL Trim special characters]**: Een selectievakje waarmee een invoerveld van **[!UICONTROL Special characters]** wordt weergegeven als dit is ingeschakeld. Alle tekens in dit veld worden uit de uitvoer verwijderd. Multi-bytetekens worden niet ondersteund.

## Regex

Pas reguliere expressies toe op een dimensie om de gewenste waarde op te halen.

* **[!UICONTROL Regex]**: De reguliere-expressieformule.
* **[!UICONTROL Output format]**: Een optioneel veld waarmee u tekst kunt toevoegen of de volgorde van de uitvoer van de regex-subgroep kunt wijzigen. Als dit veld leeg is, is de tekenreeksuitvoer de geëvalueerde regex-expressie.
* **[!UICONTROL Case sensitive]**: Een selectievakje waarmee wordt afgedwongen dat de reguliere expressie hoofdlettergevoelig is als deze is ingeschakeld.

Customer Journey Analytics gebruikt een subset van de Perl regex syntaxis. Als de input niet de regelmatige uitdrukking aanpast en **[!UICONTROL Output format]** leeg is, [ Geen waardeopties ](no-value-options.md) van toepassing zijn. De volgende expressies worden ondersteund:

| Uitdrukking | Beschrijving |
| --- | --- |
| `a` | Eén teken `a` . |
| `a\|b` | Een enkel teken `a` of `b` . |
| `[abc]` | Eén teken `a` , `b` of `c` . |
| `[^abc]` | Eén teken behalve `a` , `b` of `c` . |
| `[a-z]` | Om het even welk enkel karakter in de waaier van `a` - `z`. |
| `[a-zA-Z0-9]` | Om het even welk enig karakter in de waaier van `a` - `z`, `A` - `Z`, of cijfers `0` - `9`. |
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
| `a?` | Nul of een van `a` . |
| `a*` | Nul of meer van `a` . |
| `a+` | Nog één meer van `a` . |
| `a{3}` | Precies 3 van `a` . |
| `a{3,}` | 3 of meer van `a` . |
| `a{3,6}` | Tussen 3 en 6 van `a` . |

Plaatsaanduidingen voor uitvoer worden ook ondersteund. U kunt deze reeksen gebruiken in **[!UICONTROL Output format]** om het even welk aantal tijden en in om het even welke orde om de gewenste koordoutput te bereiken.

| Tijdelijke plaatsaanduidingsreeks uitvoeren | Beschrijving |
| --- | --- |
| `$&` | Hiermee wordt uitgevoerd wat overeenkomt met de gehele expressie. |
| `$n` | Hiermee wordt uitgevoerd wat overeenkomt met de nde subexpressie. `$1` geeft bijvoorbeeld als uitvoer de eerste subexpressie. |
| ``$` `` | Hiermee wordt de tekst uitgevoerd tussen het einde van de laatste gevonden overeenkomst (of het begin van de tekst als er geen vorige overeenkomst is gevonden) en het begin van de huidige overeenkomst. |
| `$+` | Hiermee wordt uitgevoerd wat overeenkomt met de laatst gemarkeerde subexpressie in de reguliere expressie. |
| `$$` | Geeft als uitvoer het teken van de tekenreeks `"$"` . |

{style="table-layout:auto"}
