---
title: Verbindingen beheren
description: Beschrijft hoe te om verbindingen aan de datasets van het Platform te beheren.
translation-type: tm+mt
source-git-commit: 65b51ff6a792a0407d8c73794c1bab4a6e3f0fa1
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---


# Verbindingen beheren

Zodra u één of meerdere verbindingen hebt gecreeerd, kunt u hen in [!UICONTROL Connections] Manager beheren. U kunt

* Een verbinding verwijderen.
* Wijzig de naam van een verbinding.
* Maak een gegevensweergave via een verbinding.
* Gegevensstreaming starten en stoppen.

![Verbindingsbeheer](assets/connections-manager.png)

1. Klik op het tabblad **[!UICONTROL Connections]**.

2. Selecteer welke verbinding(en) u wilt bewerken of beheren.

3. Voer een van de volgende handelingen uit:

   | Handeling | Beschrijving |
   |---|---|
   | [!UICONTROL Delete] | Als u een verbinding verwijdert, wordt de gegevensset niet verwijderd, omdat de gegevens zich nog in [!DNL Adobe Experience Platform] bevinden. Zie &quot;Verbindingen verwijderen&quot; hieronder. |
   | [!UICONTROL Rename] | U kunt de naam van de verbinding wijzigen met een beschrijvende naam. |
   | [!UICONTROL Create Data View] | Deze verbinding neemt u aan [de bouwer van de gegevensmening](/help/data-views/create-dataview.md). |
   | [!UICONTROL Start or stop data streaming] | &quot;Streaming&quot; betekent dat als er nieuwe batches worden toegevoegd aan een van de gegevenssets in de verbinding, deze nieuwe gegevens worden overgebracht naar [!UICONTROL Customer Journey Analytics] voor rapportage. |

## Verbindingen verwijderen

| Wat als ik... | Dit gebeurt |
| --- | --- |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics]? | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Op dezelfde manier zullen om het even welke projecten van de Werkruimte die van gegevensmeningen in de geschrapte verbinding afhangen ophouden werkend.</li></ul> |
| Een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform]? | Het schrappen van een dataset in AEP zal gegevensstroom van die dataset aan om het even welke verbindingen tegenhouden die die dataset omvatten. Om het even welke gegevens van die dataset worden niet automatisch geschrapt van bijbehorende Verbindingen CJA. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics]? | U kunt momenteel geen dataset verwijderen binnen een verbinding die is opgeslagen. U moet de gehele verbinding verwijderen en opnieuw beginnen. (U kunt echter een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform].) |
| Een batch uit een dataset verwijderen (in [!UICONTROL Adobe Experience Platform])? | Als een partij uit een [!UICONTROL Adobe Experience Platform] dataset wordt geschrapt, zal de zelfde partij uit om het even welke [!UICONTROL Customer Journey Analytics] verbindingen worden verwijderd die die specifieke partij bevatten. [!UICONTROL Customer Journey Analytics] wordt op de hoogte gesteld van partijen die zijn verwijderd in  [!UICONTROL Adobe Experience Platform]. |
| Wilt u een batch **verwijderen terwijl deze in** wordt opgenomen?[!UICONTROL Customer Journey Analytics] | Als er slechts één partij in de dataset is, zullen geen gegevens of gedeeltelijke gegevens van die partij in [!UICONTROL Customer Journey Analytics] verschijnen. De inname wordt teruggedraaid. Als, bijvoorbeeld, er 5 partijen in de dataset zijn en 3 van hen reeds zijn opgenomen toen de dataset werd geschrapt, zullen de gegevens van die 3 partijen in [!UICONTROL Customer Journey Analytics] verschijnen. |
