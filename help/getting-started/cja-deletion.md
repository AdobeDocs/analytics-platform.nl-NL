---
title: Gevolgen van verwijdering
description: Wat gebeurt wanneer u verbindingen, datasets, of partijen in Customer Journey Analytics of Adobe Experience Platform schrapt.
source-git-commit: 3fa2c562abaf4aa1f18baa5de5ee66c7ad828f52
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Gevolgen van verwijdering

Overweeg dit alvorens u verbindingen, datasets, of partijen in Customer Journey Analytics of Adobe Experience Platform schrapt:

| Wanneer u... | Dit gebeurt... |
| --- | --- |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics] | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Op dezelfde manier zullen om het even welke projecten van de Werkruimte die van gegevensmeningen in de geschrapte verbinding afhangen ophouden werkend.</li></ul> |
| Een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform] (AEP) | Het schrappen van een dataset in AEP zal gegevensstroom van die dataset aan om het even welke verbindingen tegenhouden die die dataset omvatten. Om het even welke gegevens van die dataset worden niet automatisch geschrapt van bijbehorende Verbindingen CJA. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics] | U kunt momenteel geen dataset verwijderen binnen een verbinding die is opgeslagen. U moet de gehele verbinding verwijderen en opnieuw beginnen. (U kunt echter een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform].) |
| Een batch uit een gegevensset verwijderen (in [!UICONTROL Adobe Experience Platform]) | Als een partij uit een [!UICONTROL Adobe Experience Platform] dataset wordt geschrapt, zal de zelfde partij uit om het even welke [!UICONTROL Customer Journey Analytics] verbindingen worden verwijderd die die specifieke partij bevatten. [!UICONTROL Customer Journey Analytics] wordt op de hoogte gesteld van partijen die zijn verwijderd in  [!UICONTROL Adobe Experience Platform]. |
| Een batch **verwijderen tijdens het invoegen** in [!UICONTROL Customer Journey Analytics] | Als er slechts één partij in de dataset is, zullen geen gegevens of gedeeltelijke gegevens van die partij in [!UICONTROL Customer Journey Analytics] verschijnen. De inname wordt teruggedraaid. Als, bijvoorbeeld, er 5 partijen in de dataset zijn en 3 van hen reeds zijn opgenomen toen de dataset werd geschrapt, zullen de gegevens van die 3 partijen in [!UICONTROL Customer Journey Analytics] verschijnen. |
| Opzoekgegevenssets verwijderen in [!UICONTROL Adobe Experience Platform] | Terwijl het schrappen van datasets voor andere bronschakelaars mogelijk is, wordt het momenteel niet gesteund voor [Gegevensschakelaar van de Classificaties van Analytics](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/classifications.html?lang=en). Neem contact op met de klantenservice van Adobe als u per ongeluk een gegevensset verwijdert. |