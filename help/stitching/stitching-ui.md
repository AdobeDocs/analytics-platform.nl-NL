---
title: Stiksel
description: Leer hoe u gebonden gegevenssets kunt maken en beheren
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
hide: true
hidefromtoc: true
exl-id: 8820a093-e573-45f9-bcd2-0933e21c231b
role: Admin
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 0%

---

# Verstikte gegevenssets maken en beheren

{{select-package}}

Door middel van titelformaat kunnen beheerders identiteiten op gegevenssets die beschikbaar zijn in Customer Journey Analytics aan elkaar koppelen. Door gegevenssets in te stellen, vergroot u de nauwkeurigheid van de weergave van een profiel. Dit resulteert uiteindelijk in een betere analyse en rapportage.

Met het koppelingsproces kunt u een bestaande **blijvende id** in een gegevensset. Koppel die permanente id vervolgens aan voor een opgegeven afspeelvenster (dagelijks, wekelijks) met de meest accurate **transient ID** (persoon of voor authentiek verklaard herkenningsteken) beschikbaar voor die dataset. Voorbeelden van transient-id&#39;s zijn e-mail, telefoonnummer, CRM-id of andere id&#39;s die in de grafiek zijn opgeslagen. Zie [Overzicht](overview.md) voor meer informatie over stitching .

## Maken

Om het stitching in werking te stellen, creeert u één of meerdere gestikte datasets. Een gestikte dataset maken:

1. Selecteren **[!UICONTROL ** Stiksel **]** van **[!UICONTROL **&#x200B; Gegevensbeheer &#x200B;**]** op de bovenste balk.

2. In de [!UICONTROL Stitched datasets] scherm, selecteren **[!UICONTROL **&#x200B; Verstikte gegevensset maken &#x200B;**]**.

   Er wordt een dialoogvenster weergegeven met uitleg over uw verantwoordelijkheden.

3. Selecteren **[!UICONTROL **&#x200B; Doorgaan &#x200B;**]** als u deze verantwoordelijkheden aanvaardt.

   >[!NOTE]
   >
   >    Als u **[!UICONTROL **&#x200B; Annuleren &#x200B;**]**, kunt u geen gestikte dataset tot stand brengen.

4. In de [!UICONTROL Stitched datasets > Untitled stitched dataset] scherm:

   1. Een **[!UICONTROL ** Naam gegevensset **]** en (optioneel) **[!UICONTROL **&#x200B; Beschrijving &#x200B;**]**,

   2. Selecteer de sandbox in het menu **[!UICONTROL **&#x200B; Sandbox &#x200B;**]** lijst waar de gebeurtenisdataset wordt opgeslagen.

      ![Beginscherm](./assets/create-initial.png)

   3. Selecteer de **[!UICONTROL **&#x200B; Brongegevensset selecteren &#x200B;**]** knop.

      In de [!UICONTROL Select one dataset to stitch] pop-upvenster:

      ![Eén gegevensset selecteren](./assets/select-one-dataset.png)

      - Selecteer een gegevensset en selecteer **[!UICONTROL **&#x200B; Selecteren &#x200B;**]** om door te gaan.

   4. Selecteer een permanente id in het menu **[!UICONTROL **&#x200B; Blijvende id &#x200B;**]** lijst.

   5. Selecteer een tijdelijke id in het menu **[!UICONTROL **&#x200B; Tijdelijke id &#x200B;**]** lijst.

      U ziet dat een voorvertoningsvenster wordt weergegeven voor het berekenen van de verzadigingssnelheden (het aantal keren dat er een waarde is voor elk van de opgegeven id&#39;s over het aantal gebeurtenissen) gedurende de laatste zeven dagen. Na het berekenen wordt in het deelvenster met kleuren weergegeven of aan de minimale voorwaarden voor stitching is voldaan (groen) of dat niet (rood).

      ![Verstikte gegevensset met staturatiesnelheden maken](./assets/create-before-experimenting.png)

      De minimumvoorwaarden zijn:

      - blijvende id-verzadiging: frequentie >= 95%

      - verzadiging van transient identifier: snelheid >= 5%

        Als aan de minimale voorwaarden wordt voldaan, kunt u experimenteren met samplewaarden.

      - Selecteren **[!UICONTROL **&#x200B; Aan demo bevestigde id&#39;s maken &#x200B;**]**.

        In de [!UICONTROL Experiment with sample values] wordt een tabel weergegeven met de voorbeeldwaarde voor [!UICONTROL timestamp], [!UICONTROL Persistent ID], [!UICONTROL Transient ID], [!UICONTROL Stitched ID (Live)], [!UICONTROL Stitched ID (1-day replay)], en [!UICONTROL Stitched ID (7-day replay)].

            ![Experimenteren met samplewaarden](./assets/experiment-sample-values.png)
            
            1. Voer een waarde in voor de **[!UICONTROL **Persistent ID**]**.
            
            2. Selecteren **[!UICONTROL **Refresh stitched IDs**]** om het effect van het stitching proces op de gegevens in de dataset te zien.
            
            3. Selecteren **[!UICONTROL **Close**]** als u klaar bent met het experimenteren met samplewaarden.
        

        Terug in de [!UICONTROL Stitched datasets > _Naam gegevensset_] scherm:

   6. Selecteer een optie voor de frequentie en de periode waarin historische gegevens opnieuw moeten worden vermeld in het dialoogvenster **[!UICONTROL **&#x200B; Venster opnieuw afspelen &#x200B;**]** lijst.

      U kunt kiezen tussen de standaardwaarde **[!UICONTROL ** Vorige dag, dag **]** of **[!UICONTROL **&#x200B; Vorige 7 dagen, wekelijks &#x200B;**]**.

   7. Selecteer een waarde in het menu **[!UICONTROL **&#x200B; Gemiddeld aantal dagelijkse gebeurtenissen &#x200B;**]** lijst.

   8. Voer een waarde in (tussen `0` en `12`) in **[!UICONTROL **&#x200B; Aantal maanden dat moet worden hersteld &#x200B;**]**.

   9. Selecteren **[!UICONTROL **&#x200B; Opslaan &#x200B;**]** om uw gestikte dataset te bewaren en het stitching in werking te stellen.

## Status weergeven

U kunt de status van stitching weergeven in het dialoogvenster [!UICONTROL Stitched datasets] lijst.

- Selecteren **[!UICONTROL ** Stiksel **]** van **[!UICONTROL **&#x200B; Gegevensbeheer &#x200B;**]** op de bovenste balk.

  U ziet een lijst met gestikte gegevenssets, elk geïdentificeerd met [!UICONTROL Sandbox], [!UICONTROL Source dataset], [!UICONTROL Status], [!UICONTROL Backfill status], [!UICONTROL Owner], en [!UICONTROL Date created].

  ![Overzicht van vastgezette gegevenssets](./assets/overview-stitched-datasetts.png)

  Mogelijke waarden voor [!UICONTROL Status] zijn:

  | Waarde | Toelichting |
  |-----|-----|
  | **[!UICONTROL **&#x200B; In wachtrij &#x200B;**]** | Het verzoek wordt ontvangen en verwerkt spoedig. |
  | **[!UICONTROL **&#x200B; Maken &#x200B;**]** in uitvoering | De middelen en onlangs gestikte dataset zijn in creatie. |
  | **[!UICONTROL **&#x200B; Telling wordt uitgevoerd &#x200B;**]** | De middelen en de stitching dataset bestaan en het stitching is lopend |
  | **[!UICONTROL **&#x200B; Fout &#x200B;**] **&#x200B; | Er is een probleem met stitching. Mogelijk is een schema gewijzigd tussen de brondataset en de gebonden dataset, is het dagelijkse volume te groot, of... (_**&#x200B;meer informatie nodig...**_) |

  >[!INFO]
  >
  >    Wanneer een status verandert, wordt een melding verzonden met het bericht **[!UICONTROL **&#x200B; Stitched dataset _naam van gegevensset_ is gewijzigd in status _naam van status _**]**.


  De [!UICONTROL Backfill status] U kunt de volgende waarden hebben: 0%, 25%, 50%, 75% of 100%.

  U kunt het informatiepictogram selecteren om een pop-up met meer details op de geselecteerde gestikte dataset te tonen.


## Verwijderen

>[!NOTE]
>
>U kunt alleen gegevenssets verwijderen die de status hebben [!UICONTROL Stitching in progress], [!UICONTROL Error], of [!UICONTROL Queued].


Eén verankerde gegevensset verwijderen:

- Selecteren **[!UICONTROL **...**]** voor de genormaliseerde gegevensset en selecteer **[!UICONTROL **&#x200B; Verwijderen &#x200B;**]** in het menu.

  ![Een gestikte gegevensset verwijderen](./assets/delete-stitched-dataset.png)

Meerdere gestikte gegevens verwijderen:

- Selecteer veelvoudige gestikte datasets gebruikend checkbox bij het begin van elke vermelde dataset.

- Selecteren **[!UICONTROL **...**]** van één van de geselecteerde gestikte datasets en selecteer **[!UICONTROL **&#x200B; Verwijderen &#x200B;**]** in het menu.
