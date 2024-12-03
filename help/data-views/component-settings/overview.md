---
title: Componentinstellingen
description: De kernmontages van de mening voor een component van de gegevensmening.
exl-id: 6300d289-d308-476e-aa4e-05cdae361bb2
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: 1158064d46e09435ec2507c47e6e484306ac5a53
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---

# Componentinstellingen {#component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_settings"
>title="Componentinstellingen"
>abstract="De naam, beschrijving en andere instellingen die betrekking hebben op een component weergeven en configureren.<br/><br/>**Parameters **<br/>**verbergen component in het melden**: Het controleren van dit vakje zal deze component van niet-admin gebruikers in het melden verbergen. Beheerders hebben er nog steeds toegang toe door **[!UICONTROL Show all components]** te selecteren in een Workspace-project."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_contextlabels"
>title="Contextlabels"
>abstract="Het verwijderen van een contextlabel kan gevolgen hebben voor specifieke deelvensters of rapporten waar de component wordt vereist."

<!-- markdownlint-enable MD034 -->


De volgende informatie beschrijft de montages die een component van de gegevensmening gebruikt.

![ de montages van de Component die in deze sectie ](../assets/component-settings.png) worden beschreven

| Instelling | Omschrijving/gebruik |
| --- | --- |
| [!UICONTROL Component type] | Vereist. Hiermee kunt u een component wijzigen van Metrisch in Dimension of omgekeerd. Als u deze vervolgkeuzelijst wijzigt, wordt de component verplaatst naar het bijbehorende opgenomen componentgebied. |
| [!UICONTROL Component Name] | Vereist. Hier geeft u de vriendschappelijke naam op die in Analysis Workspace wordt weergegeven. U kunt de naam van een component wijzigen en deze een specifieke naam geven voor de gegevensweergave. |
| [!UICONTROL Description] | Optioneel, maar aanbevolen. Verstrekt informatie over de component aan andere gebruikers. |
| [!UICONTROL Tags] | Optioneel. Hiermee kunt u de component labelen met aangepaste of kant-en-klare tags, zodat u gemakkelijker kunt zoeken en filteren in de gebruikersinterface van Analysis Workspace. |
| [!UICONTROL Context labels] | Optioneel. Een vervolgkeuzelijst met beschikbare door het systeem gedefinieerde labels die op een component kunnen worden toegepast. Deze etiketten kunnen worden vereist om een reeks componenten te bepalen u in experimenteren het melden kunt gebruiken gebruikend het [ paneel van de Experimentatie ](/help/analysis-workspace/c-panels/experimentation.md) in de projecten van Analysis Workspace. Zie [ met Journey Optimizer ](/help/integrations/ajo.md#data-view) integreren en [ Doel die ](/help/integrations/at.md) voor meer informatie melden. |
| [!UICONTROL Schema field name] | De naam van het schemaveld. |
| [!UICONTROL Dataset type] | Vereist. Een niet-bewerkbaar veld dat aangeeft uit welk gegevenstype de component afkomstig is (gebeurtenis, zoekopdracht of profiel). |
| [!UICONTROL Dataset] | Een niet-bewerkbaar veld dat aangeeft van welke gegevensset de component afkomstig is. Dit veld kan meerdere gegevenssets bevatten. |
| [!UICONTROL Schema Type] | Een niet-bewerkbaar veld dat het gegevenstype van de component weergeeft. Hoewel u elk ondersteund schemaveldtype kunt gebruiken in Platform, worden niet alle veldtypen ondersteund in Customer Journey Analytics. De volgende gegevenstypen worden ondersteund: `Integer`, `Int`, `Long`, `Double`, `Float`, `Number`, `Short`, `Byte`, `String` en `Boolean`. Alleen het gegevenstype van het `String` schema is momenteel toegestaan in Lookup-gegevenssets. |
| [!UICONTROL Component ID] | Vereist. De [ Customer Journey Analytics API ](https://adobe.io/cja-apis/docs) gebruikt dit gebied om de component van verwijzingen te voorzien. Elke component in een gegevensweergave moet uniek zijn. Adobe genereert automatisch een id voor elke component. U kunt echter op het bewerkingspictogram klikken en de component-id wijzigen. Wanneer u de component-id wijzigt, worden alle bestaande Workspace-projecten met deze component verbroken. Hoewel elke component een unieke id in één gegevensweergave nodig heeft, kunt u dezelfde component-id in andere gegevensweergaven gebruiken. Als u dezelfde component-id in andere gegevensweergaven gebruikt, kunt u Workspace-projecten compatibel maken in verschillende gegevensweergaven. <br/> voor profiel en raadpleging gebaseerde componenten, heeft componentenidentiteitskaart een prefix die van identiteitskaart op dataset ID wordt gebaseerd (bijvoorbeeld: `642b28fcc1f0ee1c074265a0.person.name.firstName`). Wanneer u een profiel of een op raadpleging gebaseerde component, zoals `person.name.firstName`, in uw Workspace-project opnieuw wilt gebruiken en deze component in verschillende gegevensweergaven wilt configureren, moet u ervoor zorgen dat de naam van de component-id uniek wordt gewijzigd (bijvoorbeeld: `myUniqueID.person.name.firstName` ) in de verschillende gegevensweergaven. |
| [!UICONTROL Path] | Vereist. Een niet-bewerkbaar veld met het schemapad waaruit de component afkomstig is. |
| [!UICONTROL Data Usage Labels] | Alle labels voor gegevensgebruik die in Adobe Experience Platform aan deze component zijn toegewezen. [ leer meer ](/help/data-views/data-governance.md). |
| [!UICONTROL Hide component in reporting] | Hiermee kunt u de component uit de gegevensweergave voor niet-beheerders beheren. Beheerders hebben er nog steeds toegang toe door in een Analysis Workspace-project op [!UICONTROL Show All Components] te klikken. |

{style="table-layout:auto"}

Hier volgt een video over componentinstellingen in gegevensweergaven:

>[!VIDEO](https://video.tv.adobe.com/v/333112/?quality=12)
