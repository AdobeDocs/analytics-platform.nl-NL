---
title: Componentinstellingen
description: De kernmontages van de mening voor een component van de gegevensmening.
exl-id: 6300d289-d308-476e-aa4e-05cdae361bb2
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: e7e3affbc710ec4fc8d6b1d14d17feb8c556befc
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 1%

---

# Componentinstellingen

De montages van de kern die een component van de gegevensmening gebruikt.

![Componentinstellingen](../assets/component-settings.png)

| Instelling | Beschrijving/Hoofdletters gebruiken |
| --- | --- |
| [!UICONTROL Component type] | Vereist. Hiermee kunt u een component wijzigen van Metrisch in Dimension of omgekeerd. Als u deze vervolgkeuzelijst wijzigt, wordt de component verplaatst naar het bijbehorende opgenomen componentgebied. |
| [!UICONTROL Component Name] | Vereist. Hier geeft u de vriendschappelijke naam op die in Analysis Workspace wordt weergegeven. U kunt de naam van een component wijzigen en deze een specifieke naam geven voor de gegevensweergave. |
| [!UICONTROL Description] | Optioneel, maar aanbevolen. Verstrekt informatie over de component aan andere gebruikers. |
| [!UICONTROL Tags] | Optioneel. Hiermee kunt u de component labelen met aangepaste of kant-en-klare tags, zodat u gemakkelijker kunt zoeken en filteren in de gebruikersinterface van Analysis Workspace. |
| [!UICONTROL Context labels] | Optioneel. Een vervolgkeuzelijst met beschikbare door het systeem gedefinieerde labels die op een component kunnen worden toegepast. Deze labels kunnen nodig zijn om een set componenten te definiëren die worden gebruikt voor rapportage in Analysis Workspace-projecten of -deelvensters. |
| [!UICONTROL Schema field name] | De naam van het schemaveld. |
| [!UICONTROL Dataset type] | Vereist. Een niet-bewerkbaar veld dat aangeeft uit welk gegevenstype de component afkomstig is (gebeurtenis, zoekopdracht of profiel). |
| [!UICONTROL Dataset] | Een niet-bewerkbaar veld dat aangeeft van welke gegevensset de component afkomstig is. Dit veld kan meerdere gegevenssets bevatten. |
| [!UICONTROL Schema Type] | Een niet-bewerkbaar veld dat het gegevenstype van de component weergeeft. Hoewel u elk ondersteund schemaveldtype in het Platform kunt gebruiken, worden niet alle veldtypen ondersteund in Customer Journey Analytics. De volgende gegevenstypen worden ondersteund: `Integer`, `Int`, `Long`, `Double`, `Float`, `Number`, `Short`, `Byte`, `String`, en `Boolean`. Alleen de `String` het gegevenstype van schemagegevens wordt toegestaan in de datasets van de Opzoekopdracht momenteel. |
| [!UICONTROL Component ID] | Vereist. De [Customer Journey Analytics API](https://adobe.io/cja-apis/docs) gebruikt dit veld om naar de component te verwijzen. Elke component in een gegevensweergave moet uniek zijn. Adobe genereert automatisch een id voor elke component; u kunt echter op het bewerkingspictogram klikken en de component-id wijzigen. Wanneer u de component-id wijzigt, worden alle bestaande werkruimteprojecten die deze component bevatten, verbroken. Hoewel elke component een unieke id in één gegevensweergave nodig heeft, kunt u dezelfde component-id in andere gegevensweergaven gebruiken. Als u dezelfde component-id in andere gegevensweergaven gebruikt, kunt u Workspace-projecten compatibel maken in verschillende gegevensweergaven. <br/>Voor op profiel en raadpleging gebaseerde componenten, heeft componentid een prefix van identiteitskaart die op dataset ID wordt gebaseerd (bijvoorbeeld: `642b28fcc1f0ee1c074265a0.person.name.firstName`). Wanneer u een profiel of op raadpleging gebaseerde component, zoals wilt opnieuw gebruiken `person.name.firstName`, in uw project van de Werkruimte, en vorm deze component in verschillende gegevensmeningen, zorg ervoor u unieke identiteitskaart van de component anders noemt (bijvoorbeeld: `myUniqueID.person.name.firstName`) in uw gegevensweergaven. |
| [!UICONTROL Path] | Vereist. Een niet-bewerkbaar veld met het schemapad waaruit de component afkomstig is. |
| [!UICONTROL Data Usage Labels] | Alle labels voor gegevensgebruik die in Adobe Experience Platform aan deze component zijn toegewezen. [Meer informatie](/help/data-views/data-governance.md) |
| [!UICONTROL Hide component in reporting] | Hiermee kunt u de component uit de gegevensweergave voor niet-beheerders beheren. Beheerders hebben er nog steeds toegang toe door op [!UICONTROL Show All Components] in een Analysis Workspace-project. |

{style="table-layout:auto"}

Hier volgt een video over componentinstellingen in gegevensweergaven:

>[!VIDEO](https://video.tv.adobe.com/v/333112/?quality=12)
