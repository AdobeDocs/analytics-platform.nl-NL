---
title: Annotaties maken
description: Annotaties maken in Workspace.
feature: Components
exl-id: 68fef9b3-dc47-4e56-bea6-d1c4c39fb51b
role: User, Admin
source-git-commit: e4e0c3cf2e865454837df6626c3b1b09f119f07f
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# Annotaties maken

Standaard kunnen alleen beheerders annotaties maken. Gebruikers hebben rechten om annotaties weer te geven, vergelijkbaar met de manier waarop gebruikers andere componenten (zoals filters, berekende metriek, enz.) weergeven.

Beheerders kunnen gebruikers echter de **[!UICONTROL Annotation Creation]** machtiging voor **[!UICONTROL Reporting Tools]** in **[!UICONTROL Edit permissions for CJA Workspace Access]** geven via de Admin Console. Zie [ gebruiker-vlakke toegangsbeheer ](/help/technotes/access-control.md#user-level-access) voor meer informatie.

U kunt op de volgende manieren een aantekening maken:

![ creeer een aantekening ](assets/create-annotation.png)

* ?? Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer **[!UICONTROL Annotations]** . Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) [!UICONTROL **[!UICONTROL Add]**] van de [[!UICONTROL Annotations] manager ](/help/components/annotations/manage-annotations.md).
* ?? Selecteer **[!UICONTROL Create annotation from selection]** in een Workspace-project in het contextmenu in een visualisatie.
* ?? Selecteer in een Workspace-project in het contextmenu in een lijngrafiek de optie **[!UICONTROL Annotate Selection]** .
* ??In een Workspace-project selecteert u **[!UICONTROL Components]** in het menu en selecteert u **[!UICONTROL Create annotation]** .
* ?? In een Workspace-project gebruikt u de sneltoets **[!UICONTROL ctrl+shift+o]** (Windows) of **[!UICONTROL shift+command+o]** (macOS)

Als u de annotatie wilt definiëren, gebruikt u de instructie [[!UICONTROL Annotation builder]](#annotation-builder) :

<!-- Should we really mention API here. If so, we can do it all over the place in the docs...
| **Use the [Customer Journey Analytics Annotations API](https://developer.adobe.com/cja-apis/docs/endpoints/annotations/)** | The Customer Journey Analytics Annotations APIs allow you to create, update, or retrieve annotations programmatically through Adobe Developer. These APIs use the same data and methods that Adobe uses inside the product UI. |
-->


## Annotatiebuilder {#annotation-builder}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_annotations_details"
>title="Details van aantekening"
>abstract="Met annotaties kunt u op effectieve wijze contextuele gegevensnuances en inzichten aan uw organisatie meedelen. Met deze sjablonen kunt u kalendergebeurtenissen koppelen aan specifieke afmetingen/metriek."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_annotations_scope"
>title="Toepassingsgebied"
>abstract="Met het bereik kunt u aanpassen welke gegevens worden geannoteerd. Berekende metriek en segmenten zullen automatisch geen annotaties erven die worden toegepast op componenten die in hun definities worden gebruikt. U kunt nieuwe berekende metriek aan de werkingsgebiedsectie van een bestaande aantekening toevoegen. Voor nieuwe segmenten is een nieuwe annotatie vereist."

<!-- markdownlint-enable MD034 -->


Het dialoogvenster **[!UICONTROL Annotations builder]** wordt gebruikt om nieuwe annotaties te maken of bestaande annotaties te bewerken. Het dialoogvenster krijgt de naam **[!UICONTROL New annotation]** of **[!UICONTROL Edit annotation]** voor annotaties die u maakt of beheert met de [[!UICONTROL Annotations] manager ](/help/components/annotations/manage-annotations.md) .


>[!BEGINTABS]

>[!TAB  Bouwer van de Annotatie ]

![ het venster van de details van de Annotatie die gebieden en opties tonen in de volgende sectie worden beschreven.](assets/annotation-builder.png)

>[!TAB  creeer/geef aantekening ] uit

![ het venster van de details van de Annotatie die gebieden en opties tonen in de volgende sectie worden beschreven.](assets/create-edit-annotation.png)

>[!ENDTABS]

1. Specificeer de volgende details (![ Vereiste ](/help/assets/icons/Required.svg) wordt vereist):

   | Element | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Data view]** | U kunt de gegevensweergave voor de annotatie selecteren. De annotatie die u definieert, is beschikbaar als een annotatie in de Workspace-projecten op basis van de geselecteerde gegevensweergave. Deze selectie wordt genegeerd wanneer u [!UICONTROL Apply to all data views] hebt ingeschakeld. |
   | **[!UICONTROL Project-only Annotation]** | Een informatievak om uit te leggen dat de annotatie die u maakt, alleen zichtbaar is in het Workspace-project waaraan u werkt. Schakel **[!UICONTROL Make this Annotation available to all your projects]** in om de annotatie zichtbaar te maken voor al uw projecten. Dit informatievak is alleen zichtbaar wanneer u een annotatie maakt vanuit een Workspace-project. |
   | **[!UICONTROL Title]** ![ Vereiste ](/help/assets/icons/Required.svg) | Geef de annotatie bijvoorbeeld de naam `Needs further investigation` . |
   | **[!UICONTROL Description]** | Geef een beschrijving voor de annotatie, bijvoorbeeld `We never expected such a fluctuation in numbers.` . |
   | **[!UICONTROL Tags]** | U ordent de annotatie door een of meer tags te maken of toe te passen. Begin te typen om naar bestaande tags te zoeken die u kunt selecteren. Of druk op **[!UICONTROL Enter]** om een nieuwe tag toe te voegen. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om een markering te verwijderen. |
   | **[!UICONTROL Applied date]** ![ Vereiste ](/help/assets/icons/Required.svg) | Selecteer de datum of het datumbereik dat aanwezig moet zijn om de annotatie zichtbaar te maken. Wanneer u een annotatie maakt met de sneltoets, wordt de annotatie standaard ingesteld op een datumbereik voor alleen de dag. Wanneer u een annotatie maakt met behulp van een selectie in een visualisatie, wordt de annotatie standaard ingesteld op het datumbereik op basis van het datumbereik van het deelvenster waartoe de visualisatie behoort. |
   | **[!UICONTROL Color]** | Pas een kleur toe op de annotatie. De annotatie wordt in het project weergegeven met de geselecteerde kleur. De kleur kan worden gebruikt om annotaties te categoriseren, zoals feestdagen, externe gebeurtenissen, problemen bij het bijhouden van wijzigingen, enzovoort. |
   | **[!UICONTROL Scope]** | Sleep metriek van het componentenpaneel dat de annotatie teweegbrengt. Bijvoorbeeld Personen, Sessies en Gebeurtenissen. Sleep vervolgens de afmetingen of filters uit het deelvenster met componenten die fungeren als filters om te bepalen of de annotatie moet worden weergegeven of niet. Als u geen bereik opgeeft, wordt de annotatie toegepast op al uw gegevens. <br/> u hebt twee opties:<ul><li>**[!UICONTROL Any of these metrics are present]**: sleep en zet tot 10 metriek neer die de annotatie teweegbrengen om te tonen.<br/> Bijvoorbeeld, metrische Inkomsten zijn ophouden inzamelend gegevens voor een specifieke datumwaaier. Sleep metrisch van de Opbrengst in dit vakje.</li><li>**[!UICONTROL With all of these filters]**: Sleep en zet tot 10 afmetingen of filters neer die filteren of de annotatie wordt weergegeven.</li></ul><p><p>**Nota:** Om het even welke die annotatie op een component wordt toegepast die dan als deel van een berekende metrische of filterdefinitie wordt gebruikt erft automatisch niet de annotatie. De gewenste berekende metrisch moet ook aan de werkingsgebiedsectie worden toegevoegd om de aantekening te tonen. Er moet echter een nieuwe annotatie worden gemaakt voor elk filter dat u met dezelfde informatie wilt annoteren. U past bijvoorbeeld een aantekening toe op [!UICONTROL Orders] op een bepaalde dag. Vervolgens gebruikt u [!UICONTROL Orders] in een berekende metrische waarde voor hetzelfde datumbereik. De nieuwe berekende metrische waarde geeft niet automatisch de annotatie voor bestellingen weer. Voeg ook de berekende metrische waarde toe aan de bereiksectie voor de annotatie die moet worden weergegeven. |
   | **[!UICONTROL Apply to all data views]** | Standaard wordt de annotatie toegepast op de gegevensweergave die wordt gegenereerd. Als u dit selectievakje inschakelt, kunt u de annotatie toepassen op alle gegevensweergaven in het bedrijf. |

   {style="table-layout:auto"}

1. Selecteren
   * **[!UICONTROL Save]** om de aantekening op te slaan.
   * **[!UICONTROL Save As]** om een kopie van de annotatie op te slaan.
   * **[!UICONTROL Delete]** om een aantekening te verwijderen.
   * **[!UICONTROL Cancel]** om eventuele wijzigingen in een annotatie te annuleren of om het maken van een nieuwe annotatie te annuleren.
