---
title: Stiksel
description: Leer hoe u gebonden gegevenssets kunt maken en beheren
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
hide: true
hidefromtoc: true
exl-id: 8820a093-e573-45f9-bcd2-0933e21c231b
role: Admin
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 0%

---

# Verstikte gegevenssets maken en beheren

{{select-package}}

Met behulp van titching kunnen beheerders identiteiten koppelen aan gegevenssets die beschikbaar zijn in Customer Journey Analytics. Door gegevenssets in te stellen, vergroot u de nauwkeurigheid van de weergave van een profiel. Dit resulteert uiteindelijk in een betere analyse en rapportage.

Het stitching proces staat u toe om bestaande **blijvende identiteitskaart** in een dataset te bepalen. Dan steek die blijvend herkenningsteken voor een gespecificeerd replay venster (dagelijks, wekelijks) met nauwkeurigste **persoonsidentiteitskaart** (persoon of voor authentiek verklaard herkenningsteken) beschikbaar voor die dataset. Voorbeelden van personen-id&#39;s zijn e-mail, telefoonnummer, CRM-id of andere id&#39;s die in de grafiek zijn opgeslagen. Zie [ Overzicht ](overview.md) voor meer informatie bij het stitching.

## Maken

Om het stitching in werking te stellen, creeert u één of meerdere gestikte datasets. Een gestikte dataset maken:

1. Selecteer **[!UICONTROL ** het Plaatsen **]** van **[!UICONTROL ** het Beheer van Gegevens **]** bij de hoogste bar.

2. In het [!UICONTROL Stitched datasets] scherm, uitgezochte **[!UICONTROL ** creeer gestikte dataset **]**.

   Er wordt een dialoogvenster weergegeven met uitleg over uw verantwoordelijkheden.

3. Selecteer **[!UICONTROL ** verdergaan **]** als u deze verantwoordelijkheden goedkeurt.

   >[!NOTE]
   >
   >    Als u **[!UICONTROL ** selecteert annuleert **]**, kunt u geen gestikte dataset tot stand brengen.

4. In het [!UICONTROL Stitched datasets > Untitled stitched dataset] -scherm:

   1. Bepaal de naam van de a **[!UICONTROL ** Dataset **]** en (facultatieve) **[!UICONTROL ** Beschrijving **]**,

   2. Selecteer de zandbak van de **[!UICONTROL ** zandbak **]** lijst waar de gebeurtenisdataset wordt opgeslagen.

      ![ Aanvankelijk verwezenlijking scherm ](./assets/create-initial.png)

   3. Selecteer de **[!UICONTROL ** Uitgezochte bron dataset **]** knoop.

      In het pop-upvenster van [!UICONTROL Select one dataset to stitch] :

      ![ selecteer één dataset ](./assets/select-one-dataset.png)

      - Selecteer een dataset en selecteer **[!UICONTROL ** Uitgezocht **]** om verder te gaan.

   4. Selecteer een blijvend herkenningsteken van de **[!UICONTROL ** Blijvende identiteitskaart **]** lijst.

   5. Selecteer een persoonsidentificatie van de **[!UICONTROL ** Tijdelijke identiteitskaart **]** lijst.

      U ziet dat een voorvertoningsvenster wordt weergegeven voor het berekenen van de verzadigingssnelheden (het aantal keren dat er een waarde is voor elk van de opgegeven id&#39;s over het aantal gebeurtenissen) gedurende de laatste zeven dagen. Na het berekenen wordt in het deelvenster met kleuren weergegeven of aan de minimale voorwaarden voor stitching is voldaan (groen) of dat niet (rood).

      ![ creeer gestikte datset met staturatiecijfers ](./assets/create-before-experimenting.png)

      De minimumvoorwaarden zijn:

      - blijvende id-verzadiging: frequentie >= 95%

      - verzadiging van de identificatiecode van de persoon: frequentie >= 5%

        Als aan de minimale voorwaarden wordt voldaan, kunt u experimenteren met samplewaarden.

      - Selecteer **[!UICONTROL ** Create demo stitched identiteitskaart **]**.

        In het dialoogvenster [!UICONTROL Experiment with sample values] wordt een tabel weergegeven met een voorbeeldwaarde voor [!UICONTROL timestamp] , [!UICONTROL Persistent ID] , [!UICONTROL Transient ID] , [!UICONTROL Stitched ID (Live)] , [!UICONTROL Stitched ID (1-day replay)] en [!UICONTROL Stitched ID (7-day replay)] .

            ![Experimenteren met samplewaarden](./assets/experiment-sample-values.png) 
            
             1.  Voer een waarde in voor de **[!UICONTROL **Persistent ID**]**.
            
             2.  Selecteer ** [!UICONTROL **Refresh stitched IDs**] ** om het effect van het stitching proces op de gegevens in de dataset te zien.
            
             3.  Selecteer ** [!UICONTROL **Close**] ** wanneer u klaar bent met het experimenteren met steekproefwaarden.
        

        Terug in het [!UICONTROL Stitched datasets > _scherm van de Naam van de Dataset 0}:_]

   6. Selecteer een optie voor de frequentie en de periode van het opnieuw verklaren van historische gegevens van de **[!UICONTROL ** Replay venster **]** lijst.

      U kunt tussen de standaardwaarde **[!UICONTROL ** Vorige dag, dag **]** of **[!UICONTROL ** Vorige 7 dagen, wekelijks **]** selecteren.

   7. Selecteer een waarde van het **[!UICONTROL ** Gemiddelde aantal dagelijkse gebeurtenissen **]** lijst.

   8. Ga een waarde (tussen `0` en `12`) in **[!UICONTROL ** Aantal maanden in terug te vullen **]**.

   9. Selecteer **[!UICONTROL ** sparen **]** om uw gestikte dataset te bewaren en het stitching in werking te stellen.

## Status weergeven

U kunt de status van stitching in de [!UICONTROL Stitched datasets] lijst bekijken.

- Selecteer **[!UICONTROL ** het Plaatsen **]** van **[!UICONTROL ** het Beheer van Gegevens **]** bij de hoogste bar.

  Er wordt een lijst met naastgelegen gegevenssets weergegeven, elk geïdentificeerd met [!UICONTROL Sandbox] , [!UICONTROL Source dataset] , [!UICONTROL Status] , [!UICONTROL Backfill status] , [!UICONTROL Owner] en [!UICONTROL Date created] .

  ![ Overzicht van gestikte datasets ](./assets/overview-stitched-datasetts.png)

  Mogelijke waarden voor [!UICONTROL Status] zijn:

  | Waarde | Toelichting |
  |-----|-----|
  | **[!UICONTROL ** In wachtrij geplaatst **]** | Het verzoek wordt ontvangen en verwerkt spoedig. |
  | **[!UICONTROL ** Creatie **]** lopend | De middelen en onlangs gestikte dataset zijn in creatie. |
  | **[!UICONTROL ** het Plaatsen lopend **]** | De middelen en de stitching dataset bestaan en het stitching is lopend |
  | **[!UICONTROL ** Fout **]** | Er is een probleem met stitching. Misschien veranderde een schema tussen brondataset en gestikte dataset, is het dagelijkse volume te groot, of... (_**behoefte meer informatie hier...**_) |

  >[!INFO]
  >
  >    Wanneer een status verandert, wordt een bericht verzonden met het bericht **[!UICONTROL ** Gestitched dataset _naam van dataset_ is veranderd in status _naam van status _**]**.


  [!UICONTROL Backfill status] kan de volgende waarden hebben: 0%, 25%, 50%, 75% of 100%.

  U kunt het informatiepictogram selecteren om een pop-up met meer details op de geselecteerde gestikte dataset te tonen.


## Verwijderen

>[!NOTE]
>
>U kunt alleen gegevenssets verwijderen die de status [!UICONTROL Stitching in progress], [!UICONTROL Error] of [!UICONTROL Queued] hebben.


Eén verankerde gegevensset verwijderen:

- Selecteer **[!UICONTROL **... **]** voor de gestikte dataset en selecteer **[!UICONTROL ** Schrapping **]** van het menu.

  ![ Schrap een gestikte dataset ](./assets/delete-stitched-dataset.png)

Meerdere gestikte gegevens verwijderen:

- Selecteer veelvoudige gestikte datasets gebruikend checkbox bij het begin van elke vermelde dataset.

- Selecteer **[!UICONTROL **... **]** van één van de geselecteerde gestikte datasets en selecteer **[!UICONTROL ** Schrapping **]** van het menu.
