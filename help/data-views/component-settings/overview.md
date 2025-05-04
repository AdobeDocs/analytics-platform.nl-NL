---
title: Componentinstellingen
description: De kernmontages van de mening voor een component van de gegevensmening.
exl-id: 6300d289-d308-476e-aa4e-05cdae361bb2
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: f03c82375a907821c8e3f40b32b4d4200a47323f
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Componentinstellingen {#component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_settings"
>title="Componentinstellingen"
>abstract="De naam, beschrijving en andere instellingen die betrekking hebben op een component weergeven en configureren. Schakel dit vakje in om deze component te verbergen voor gebruikers die geen beheerder zijn in de rapportage. Beheerders hebben nog steeds toegang tot de component door **[!UICONTROL Show all components]** te selecteren in een Workspace-project."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_contextlabels"
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
| [!UICONTROL Context labels] | Optioneel. Een vervolgkeuzemenu met beschikbare door het systeem gedefinieerde labels die op een component kunnen worden toegepast. <p>Deze etiketten kunnen in de volgende situaties worden vereist:</p> <ul><li>Om een reeks componenten te bepalen kunt u in experimenteren die het gebruiken van het [ paneel van de Experimentatie ](/help/analysis-workspace/c-panels/experimentation.md) in de projecten van Analysis Workspace gebruiken.<p>Voor meer informatie, zie [ met Journey Optimizer ](/help/integrations/ajo.md#data-view) integreren en [ Doel rapporterend ](/help/integrations/at.md).</p></li><li>Als je sjablonen gebruikt die door Adobe worden aangeboden. Bepaalde sjablonen die door Adobe worden aangeboden, werken standaard niet omdat ze componenten bevatten die niet in de gegevensweergave staan.<p>Voor elke ontbrekende component is er een contextlabel beschikbaar in de gegevensweergave. U moet het overeenkomende contextlabel toevoegen aan een component die zich al in de gegevensweergave bevindt, of u moet een nieuwe component aan de gegevensweergave toevoegen en er een contextlabel aan toevoegen.</p><p>Voor meer informatie, zie [ ontbrekende componenten aan de gegevensmening voor een bepaalde malplaatje ](/help/analysis-workspace/templates/create-templates.md#add-missing-components-to-the-data-view-for-a-given-template) in het artikel [ toevoegen en malplaatjes ](/help/analysis-workspace/templates/create-templates.md) beheren.</p> |
| [!UICONTROL Schema field name] | De naam van het schemaveld. |
| [!UICONTROL Dataset type] | Vereist. Een niet-bewerkbaar veld dat aangeeft uit welk gegevenstype de component afkomstig is (gebeurtenis, zoekopdracht of profiel). |
| [!UICONTROL Dataset] | Een niet-bewerkbaar veld dat aangeeft van welke gegevensset de component afkomstig is. Dit veld kan meerdere gegevenssets bevatten. |
| [!UICONTROL Schema Type] | Een niet-bewerkbaar veld dat het gegevenstype van de component weergeeft. Hoewel u elk ondersteund schemaveldtype kunt gebruiken in Platform, worden niet alle veldtypen ondersteund in Customer Journey Analytics. De volgende gegevenstypen worden ondersteund: `Integer`, `Int`, `Long`, `Double`, `Float`, `Number`, `Short`, `Byte`, `String` en `Boolean`. Alleen het gegevenstype van het `String` schema is momenteel toegestaan in Lookup-gegevenssets. |
| [!UICONTROL Component ID] | Vereist. De [ Customer Journey Analytics API ](https://adobe.io/cja-apis/docs) gebruikt dit gebied om de component van verwijzingen te voorzien. Elke component in een gegevensweergave moet uniek zijn. Adobe genereert automatisch een id voor elke component. U kunt echter op het bewerkingspictogram klikken en de component-id wijzigen. Wanneer u de component-id wijzigt, worden alle bestaande Workspace-projecten met deze component verbroken. Hoewel elke component een unieke id in één gegevensweergave nodig heeft, kunt u dezelfde component-id in andere gegevensweergaven gebruiken. Als u dezelfde component-id in andere gegevensweergaven gebruikt, kunt u Workspace-projecten compatibel maken in verschillende gegevensweergaven. <br/> voor profiel en raadpleging gebaseerde componenten, heeft componentenidentiteitskaart een prefix die van identiteitskaart op dataset ID wordt gebaseerd (bijvoorbeeld: `642b28fcc1f0ee1c074265a0.person.name.firstName`). Wanneer u een profiel of een op raadpleging gebaseerde component, zoals `person.name.firstName`, in uw Workspace-project opnieuw wilt gebruiken en deze component in verschillende gegevensweergaven wilt configureren, moet u ervoor zorgen dat de naam van de component-id uniek wordt gewijzigd (bijvoorbeeld: `myUniqueID.person.name.firstName` ) in de verschillende gegevensweergaven. |
| [!UICONTROL Path] | Vereist. Een niet-bewerkbaar veld met het schemapad waaruit de component afkomstig is. |
| [!UICONTROL Data Usage Labels] | Alle labels voor gegevensgebruik die in Adobe Experience Platform aan deze component zijn toegewezen. [ leer meer ](/help/data-views/data-governance.md). |
| [!UICONTROL Hide component in reporting] | Hiermee kunt u de component uit de gegevensweergave voor niet-beheerders beheren. Beheerders hebben er nog steeds toegang toe door in een Analysis Workspace-project op [!UICONTROL Show All Components] te klikken. |

{style="table-layout:auto"}



>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ het type van Component montages ](https://video.tv.adobe.com/v/333112/?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


