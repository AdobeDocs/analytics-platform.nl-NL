---
title: Componentinstellingen
description: De kernmontages van de mening voor een component van de gegevensmening.
exl-id: 6300d289-d308-476e-aa4e-05cdae361bb2
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: 3f20520a2021d9b6066b0492ed11a1a4619ab1d4
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Componentinstellingen

De montages van de kern die een component van de gegevensmening gebruikt.

![Componentinstellingen](../assets/component-settings.png)

| Instelling | Beschrijving/Hoofdletters gebruiken |
| --- | --- |
| [!UICONTROL Component type] | Vereist. Hiermee kunt u een component wijzigen van Metrisch in Dimension of andersom. Als u deze vervolgkeuzelijst wijzigt, wordt de component verplaatst naar het bijbehorende opgenomen componentgebied. |
| [!UICONTROL Component Name] | Vereist. Hier geeft u de vriendschappelijke naam op die in Analysis Workspace wordt weergegeven. U kunt de naam van een component wijzigen en deze een specifieke naam geven voor de gegevensweergave. |
| [!UICONTROL Description] | Optioneel, maar aanbevolen. Verstrekt informatie over de component aan andere gebruikers. |
| [!UICONTROL Tags] | Optioneel. Hiermee kunt u de component labelen met aangepaste of kant-en-klare tags, zodat u gemakkelijker kunt zoeken en filteren in de gebruikersinterface van Analysis Workspace. |
| [!UICONTROL Field Name] | De naam van het schemaveld. |
| [!UICONTROL Dataset type] | Vereist. Een niet-bewerkbaar veld dat aangeeft uit welk gegevenstype de component afkomstig is (gebeurtenis, zoekopdracht of profiel). |
| [!UICONTROL Dataset] | Een niet-bewerkbaar veld dat aangeeft van welke gegevensset de component afkomstig is. Dit veld kan meerdere gegevenssets bevatten. |
| [!UICONTROL Schema Type] | Een niet-bewerkbaar veld dat het gegevenstype van de component weergeeft.  Hoewel u elk ondersteund schemaveldtype in Platform kunt gebruiken, worden niet alle veldtypen ondersteund in CJA. De volgende gegevenstypen worden ondersteund: `Integer`, `Int`, `Long`, `Double`, `Float`, `Number`, `Short`, `Byte`, `String`, en `Boolean`. Alleen de `String` het gegevenstype van schemagegevens wordt momenteel toegestaan in de datasets van de Opzoekopdracht. |
| [!UICONTROL Component ID] | Vereist. De [CJA API](https://adobe.io/cja-apis/docs) gebruikt dit veld om naar de component te verwijzen. Elke component in een gegevensweergave moet uniek zijn. Adobe genereert automatisch een id voor elke component; u kunt echter op het bewerkingspictogram klikken en de component-id wijzigen. Wanneer u de component-id wijzigt, worden alle bestaande werkruimteprojecten die deze component bevatten, verbroken. Hoewel elke component een unieke id in één gegevensweergave nodig heeft, kunt u dezelfde component-id in andere gegevensweergaven gebruiken. Als u dezelfde component-id in andere gegevensweergaven gebruikt, kunt u Workspace-projecten compatibel maken in verschillende gegevensweergaven. |
| [!UICONTROL Schema Path] | Vereist. Een niet-bewerkbaar veld met het schemapad waaruit de component afkomstig is. |
| [!UICONTROL Hide component in reporting] | Hiermee kunt u de component uit de gegevensweergave voor niet-beheerders beheren. Beheerders hebben er nog steeds toegang toe door op [!UICONTROL Show All Components] in een Analysis Workspace-project. |

Hier volgt een video over componentinstellingen in gegevensweergaven:

>[!VIDEO](https://video.tv.adobe.com/v/333112/?quality=12)
