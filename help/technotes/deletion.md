---
title: Gevolgen van verwijdering
description: Wat gebeurt wanneer u verbindingen, datasets, of partijen in Customer Journey Analytics of Adobe Experience Platform schrapt.
exl-id: a89694c9-0909-440e-939c-b245fc4dd6bf
solution: Customer Journey Analytics
feature: Basics
role: Admin
source-git-commit: 928c79f9ccf30cc33e0f334f715bf3190a257019
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Gevolgen van verwijdering

Overweeg dit alvorens u verbindingen, datasets, of partijen in Customer Journey Analytics of Adobe Experience Platform schrapt:

| Wanneer u... | Dit gebeurt... |
| --- | --- |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Ook Workspace-projecten die afhankelijk zijn van gegevensweergaven in de verwijderde verbinding, werken niet meer.</li></ul>U kunt geen Customers Journey Analytics verwijderen die: <ul><li>Zijn gekoppeld aan Adobe Experience Platform-sandboxen waarvoor u geen machtigingen hebt. Zelfs als u machtigingen hebt voor de gegevensweergaven die op deze verbindingen zijn gebaseerd, kunt u de verbindingen pas verwijderen als u machtigingen hebt gekregen voor de onderliggende Adobe Experience Platform-sandboxen.</li><li>Zorg dat de volgende compatibiliteitsoptie is geselecteerd voor een gegevensweergave die aan de verbinding is gekoppeld: **[!UICONTROL Set as default data view in Adobe Journey Optimizer]**<p>Voor meer informatie over deze configuratieoptie, zie [ Verenigbaarheid ](/help/data-views/create-dataview.md#compatibility) in [ creeer of geef een gegevensmening ](/help/data-views/create-dataview.md) uit</p></li></ul> |
| Een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform] | Het schrappen van een dataset in AEP zal gegevensstroom van die dataset aan om het even welke verbindingen tegenhouden die die dataset omvatten. Om het even welke gegevens van die dataset worden automatisch geschrapt van bijbehorende verbindingen van de Customer Journey Analytics. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics] | Wanneer u een dataset van een verbinding in Customer Journey Analytics schrapt, zullen om het even welke gegevensmeningen en projecten die zich op die dataset baseerden niet meer werken. |
| Een batch uit een dataset verwijderen (in [!UICONTROL Adobe Experience Platform]) | Als een batch wordt verwijderd uit een [!UICONTROL Adobe Experience Platform] dataset, wordt dezelfde batch verwijderd uit [!UICONTROL Customer Journey Analytics] -verbindingen die die specifieke batch bevatten. [!UICONTROL Customer Journey Analytics] wordt op de hoogte gesteld van batches die zijn verwijderd in [!UICONTROL Adobe Experience Platform] . |
| Schrap een partij **terwijl het** in [!UICONTROL Customer Journey Analytics] wordt opgenomen | Als er slechts één partij in de dataset is, zullen geen gegevens of gedeeltelijke gegevens van die partij in [!UICONTROL Customer Journey Analytics] verschijnen. De inname wordt teruggedraaid. Als er bijvoorbeeld 5 batches in de gegevensset zitten en er 3 al zijn ingevoerd toen de gegevensset werd verwijderd, worden gegevens van die 3 batches weergegeven in [!UICONTROL Customer Journey Analytics] . |
| Opzoekgegevenssets verwijderen in [!UICONTROL Adobe Experience Platform] | Terwijl het schrappen van datasets voor andere bronschakelaars mogelijk is, wordt het momenteel niet gesteund voor [ de Schakelaar van Source van de Classificaties van Analytics van de Classificaties ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/classifications.html). Neem contact op met de klantenservice van de Adobe als u per ongeluk een gegevensset verwijdert. |
