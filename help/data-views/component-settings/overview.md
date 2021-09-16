---
title: Componentinstellingen
description: De kerninstellingen van een component weergeven.
source-git-commit: af357167e65f4a577880832818221f6edbfc8b0a
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Componentinstellingen

Kerninstellingen die een component gebruikt.

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
| [!UICONTROL Schema Data Type] | Een niet-bewerkbaar veld dat het gegevenstype van de component weergeeft.  Hoewel u elk ondersteund schemaveldtype in Platform kunt gebruiken, worden niet alle veldtypen ondersteund in CJA. De volgende gegevenstypen worden ondersteund: `Integer`, `Int`, `Long`, `Double`, `Float`, `Number`, `Short`, `Byte`, `String` en `Boolean`. Alleen het schemagegevenstype `String` is op dit moment toegestaan in datasets opzoeken. |
| [!UICONTROL Component ID] | Vereist. De [CJA API](https://adobe.io/cja-apis/docs) gebruikt dit veld om naar de component te verwijzen. Elke component in een gegevensweergave moet uniek zijn. Adobe genereert automatisch een id voor elke component; u kunt echter op het bewerkingspictogram klikken en de component-id wijzigen. Wanneer u de component-id wijzigt, worden alle bestaande werkruimteprojecten die deze component bevatten, verbroken. Hoewel elke component een unieke id in één gegevensweergave nodig heeft, kunt u dezelfde component-id in andere gegevensweergaven gebruiken. Als u dezelfde component-id in andere gegevensweergaven gebruikt, kunt u Workspace-projecten compatibel maken in verschillende gegevensweergaven. |
| [!UICONTROL Schema Path] | Vereist. Een niet-bewerkbaar veld met het schemapad waaruit de component afkomstig is. |
| [!UICONTROL Hide component in reporting] | Hiermee kunt u de component uit de gegevensweergave voor niet-beheerders beheren. Beheerders hebben er nog steeds toegang toe door in een Analysis Workspace-project op [!UICONTROL Show All Components] te klikken. |
