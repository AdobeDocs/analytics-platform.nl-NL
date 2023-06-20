---
title: Gevolgen van verwijdering
description: Wat gebeurt wanneer u verbindingen, datasets, of partijen in Customer Journey Analytics of Adobe Experience Platform schrapt.
exl-id: a89694c9-0909-440e-939c-b245fc4dd6bf
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: ca329bd551990c1fefeda2fe272ed17551cfaac8
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Gevolgen van verwijdering

Overweeg dit alvorens u verbindingen, datasets, of partijen in Customer Journey Analytics of Adobe Experience Platform schrapt:

| Wanneer u... | Dit gebeurt... |
| --- | --- |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Op dezelfde manier zullen om het even welke projecten van de Werkruimte die van gegevensmeningen in de geschrapte verbinding afhangen ophouden werkend.</li></ul>U kunt geen Customer Journey Analytics-verbindingen verwijderen die zijn gekoppeld aan Adobe Experience Platform-sandboxen waarvoor u geen machtigingen hebt. Zelfs als u machtigingen hebt voor de gegevensweergaven die op deze verbindingen zijn gebaseerd, kunt u de verbindingen pas verwijderen als u machtigingen hebt gekregen voor de onderliggende Adobe Experience Platform-sandboxen. |
| Een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform] | Het schrappen van een dataset in AEP zal gegevensstroom van die dataset aan om het even welke verbindingen tegenhouden die die dataset omvatten. Om het even welke gegevens van die dataset worden niet automatisch geschrapt van bijbehorende Verbindingen van Customer Journey Analytics. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics] | Wanneer u een dataset van een verbinding in Customer Journey Analytics schrapt, zullen om het even welke gegevensmeningen en projecten die zich op die dataset baseerden niet meer werken. |
| Een batch verwijderen uit een dataset (in [!UICONTROL Adobe Experience Platform]) | Als een partij uit een [!UICONTROL Adobe Experience Platform] dataset, zal de zelfde partij uit om het even welk worden verwijderd [!UICONTROL Customer Journey Analytics] verbindingen die die specifieke partij bevatten. [!UICONTROL Customer Journey Analytics] wordt op de hoogte gesteld van partijen die zijn verwijderd in [!UICONTROL Adobe Experience Platform]. |
| Een batch verwijderen **tijdens de inname** in [!UICONTROL Customer Journey Analytics] | Als er slechts één partij in de dataset is, zullen geen gegevens of gedeeltelijke gegevens van die partij in verschijnen [!UICONTROL Customer Journey Analytics]. De inname wordt teruggedraaid. Als, bijvoorbeeld, er 5 partijen in de dataset zijn en 3 van hen reeds zijn opgenomen toen de dataset werd geschrapt, zullen de gegevens van die 3 partijen in verschijnen [!UICONTROL Customer Journey Analytics]. |
| Opzoekgegevenssets verwijderen in [!UICONTROL Adobe Experience Platform] | Terwijl het schrappen van datasets voor andere bronschakelaars mogelijk is, wordt het momenteel niet gesteund voor [Bronaansluiting voor analytische classificaties](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/classifications.html). Neem contact op met de klantenservice van Adobe als u per ongeluk een gegevensset verwijdert. |
