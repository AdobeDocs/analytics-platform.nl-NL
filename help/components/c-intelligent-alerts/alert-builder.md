---
description: Krijg alarm wanneer de projectcomponenten bepaalde drempels bereiken.
title: Waarschuwingen maken
feature: Workspace Basics
role: User, Admin
exl-id: 5b4b2e2b-0a73-48df-a40c-98d2c47f94c8
source-git-commit: 56ac1c5a6d13a972aed90cab79cbc5f794cedc9e
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 0%

---

# Waarschuwingen maken {#create-alerts}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_alerts_timegranularity"
>title="Tijdkorreligheid"
>abstract="De tijdsgranulariteit heeft zowel betrekking op de frequentie waarmee de waarschuwing wordt gecontroleerd als op de frequentie waarmee de waarschuwing wordt opgenomen"

<!-- markdownlint-enable MD034 -->


>[!NOTE]
>
>Het gebruiken van alarm met anomalieopsporing (die ook als _Intelligente Alarm_ wordt bekend) is beschikbaar slechts aan organisaties met een pakket van Customer Journey Analytics Prime of Ultimate.

Met waarschuwingen in Customer Journey Analytics kunt u op basis van gewijzigde percentages of specifieke gegevenspunten op de hoogte worden gesteld. Afhankelijk van het Customer Journey Analytics-pakket kunt u ook waarschuwingen gebruiken die op basis van afwijkende drempelwaarden moeten worden geactiveerd.

Voor meer gedetailleerde overzichtsinformatie over alarm, zie [ het overzicht van Alarm ](/help/components/c-intelligent-alerts/intelligent-alerts.md).

Een waarschuwing maken:

1. In Customer Journey Analytics selecteert u <!-- add this back in after the other methods are available like in AA and make a bulleted list: "You can access the alert builder in any of the following ways:" --> **[!UICONTROL Components]** > **[!UICONTROL Alerts]** . In de [ manager van het Alarm ](alert-manager.md), uitgezochte ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** om een nieuw alarm tot stand te brengen, of om het even welk vermeld alarm te selecteren om een bestaand alarm te wijzigen.

   De [ Waakzame bouwer ](#alert-builder) interfacevertoningen.

1. Selecteer **[!UICONTROL Save]** om de waarschuwing op te slaan. Selecteer **[!UICONTROL Save as]** om een kopie van de waarschuwing op te slaan.


## Alert builder

De interface van de Bouwer van de Alarm is vertrouwd aan degenen die segmenten of berekende metriek in Customer Journey Analytics hebben gebouwd:

![ Alert bouwerinterface ](assets/alert-builder.png)

Geef de volgende gegevens op in de wizard Alarm Builder voor een waarschuwing:

| Element | Beschrijving |
|---------|----------|
| **[!UICONTROL Title]** | Geef een naam op voor de waarschuwing. De waakzame naam zou de naam van het rapport of de metriedrempel kunnen bevatten. |
| **[!UICONTROL Description (optional)]** | Geef een beschrijving voor de waarschuwing op. |
| **[!UICONTROL Time granularity]** | Selecteer hoe vaak u de metrische waarde wilt controleren: Dagelijks, Wekelijks of Maandelijks.<p><b> Nota:</b> voor gegevensmeningen met een douanekalender, steunen wij geen maandelijkse granulariteit in de Waakzame Bouwer.<!--true?--></p> |
| **[!UICONTROL Recipients]** | Geef op waar de waarschuwing kan worden verzonden. Een waarschuwing kan naar een gebruiker van de Analyse, een groep van Analytics, een onbewerkt e-mailadres, of naar een telefoonaantal worden verzonden.<p><b> Belangrijk:</b> het telefoonaantal moet door a &quot;+&quot;en a [ landcode ](https://countrycode.org/) worden voorafgegaan.</p><p>Het e-mailbericht dat een gebruiker ontvangt nadat een waarschuwing is geactiveerd, ziet er ongeveer als volgt uit:</p><p>![ Alert e-mail ](assets/alerts-email.PNG)</p> |
| **[!UICONTROL Expiration date]** | Stel de datum en tijd in waarop de waarschuwing moet verlopen. |
| **[!UICONTROL Delay]** | De tijd die nodig is voordat de gegevens zijn voltooid en beschikbaar zijn voor rapportage in Customer Journey Analytics, varieert per organisatie, meestal van 3 tot 9 uur na de tijd van de gegevensgebeurtenis. Voor waarschuwingen is accuraat, moeten de gebeurtenisgegevens voor een bepaald gebeurtenisbereik volledig zijn, wat betekent dat Adobe geen gebeurtenisgegevens meer ontvangt voor het opgegeven gebeurtenisbereik.<p>Voor deze vertraging in de innametijd hebben waarschuwingen een standaardvertraging van 9 uur voordat ze worden verzonden.</p><p>U kunt de standaardvertraging van 9 uur aanpassen aan een willekeurige locatie tussen 0 en 24 uur. Als u echter de vertraging tot minder dan 9 uur verkort, kan dit betekenen dat u onvolledige gegevens rapporteert, wat leidt tot onjuiste waarschuwingsinformatie.</p><p>Overweeg het volgende wanneer het verminderen van de vertragingstijd:</p><ul><li>**Begrijp gegevensbeschikbaarheid vs. gegevens volledigheid**: Terwijl sommige gegevens beschikbaar zouden kunnen zijn om over vroeger te rapporteren, worden alle partijgegevens opgenomen in een dataset van het Platform slechts na een periode van 3 tot 9 uur. Voor nauwkeurige waarschuwingen moet de gegevensinvoer volledig zijn, met alle partijgegevens beschikbaar in de dataset.</li><li>**bepaalt hoe lang het voor uw gegevens vergt om volledig en beschikbaar in de dataset** te zijn: De tijden van de opname van gegevens verschillen door organisatie. Zorg ervoor dat de vertragingstijd u voor waakzame levering kiest het zelfde of minder frequent is dan de tijd het voor de partijgegevens neemt om in de dataset van het Platform beschikbaar te zijn <!--add link? -->.</li><p>**Uiteinde:** de nauwkeurigste manier om de tijd te kennen die voor alle partijgegevens wordt vereist om volledig en in de dataset van het Platform worden opgenomen is de gegevensingenieurs in uw organisatie te raadplegen.</p><p>Alternatief, kunt u een algemeen idee krijgen van hoe lang het voor de partijlevering in uw organisatie om in de dataset van het Platform beschikbaar te zijn door de volgende vrije vormlijst in Analysis Workspace te creëren vergt:</p><ol><li>In een vrije vormlijst in Analysis Workspace, voeg metrische en 3&rbrace; dimensie van de Dag van a [!UICONTROL **Gebeurtenissen**] en van a [!UICONTROL **toe.**]</li><li>Onderdeel de **dimensie van de Dag 0&rbrace; {gebruikend een** 3} dimensie van Uren &lbrace;.[!UICONTROL **&#x200B;**]<p>Uren zonder gegevens worden weergegeven als 0.</p></li></ol><li>**Rekening voor fouten in uw berekeningen**: Als u de standaardvertragingstijd vermindert, adviseren wij vormend de vertraging minstens een uur langer dan de tijd het uw organisatie voor volledigheid van gegevensopname neemt. Als er bijvoorbeeld een vertraging van 3 uur is voordat de gegevens zijn ingevoerd, moet u de vertraging instellen op 4 uur.</li></ul><p>Voor meer informatie, zie [ de ingangstijden van Gegevens in Customer Journey Analytics ](/help/components/c-intelligent-alerts/alerts-feature-comparison.md#data-ingestion-times-vary-in-customer-journey-analytics) in de de eigenschapvergelijking van het artikel [ Alarm variëren: Customer Journey Analytics en Adobe Analytics ](/help/components/c-intelligent-alerts/alerts-feature-comparison.md). |
| **[!UICONTROL Send an alert when]** | [!UICONTROL **om het even welk van deze metrieke trekker**]: Sleep en dalingsmetriek (met inbegrip van berekende metriek) hier om trekkers voor het alarm tot stand te brengen.<p>Een **&quot;incompatibele componenten&quot;** bericht verschijnt als niet alle metriek, dimensies, of segmenten in de alarm compatibel zijn met de momenteel geselecteerde gegevensmening.</p><p>Bepaal de drempel die metrisch moet overschrijden alvorens een alarm wordt geplaatst. U kunt deze waarde instellen op een drempel en vervolgens op een van de volgende voorwaarden:</p><ul><li>anomalie bestaat</li><li>anomalie is groter dan verwacht</li><li>anomalie is minder dan verwacht</li><li>is boven of gelijk aan</li><li>is lager of gelijk aan</li><li>wijzigingen door</li><li>U kunt een drempel instellen van 90%, 95%, 99%, 99,75% en 99,9%.</li></ul><p>[!UICONTROL **met elk van deze filters**]: Sleep en dalingssegmenten of dimensies om filters aan het alarm toe te voegen. Bijvoorbeeld, zou het toevoegen van a *Mobiele Apparaten slechts* segment betekenen dat de regel slechts voor mobiele apparaten teweegbrengt. U kunt extra filters toevoegen door een EN verklaring te gebruiken. U kunt EN of OF regels toevoegen door het tandwielpictogram te klikken.</p><p>Zie [ Alarm - gebruiksgevallen ](/help/components/c-intelligent-alerts/alerts-use-cases.md) bijvoorbeeld gebruiksgevallen.</p> |
| **[!UICONTROL Preview]** | De interactieve waarschuwingsvoorvertoning laat zien hoe vaak, ongeveer, een waarschuwing wordt geactiveerd op basis van eerdere ervaringen.<p>Als u bijvoorbeeld de tijdsgranulariteit instelt op dagelijks, kan de voorvertoning u vertellen dat de waarschuwing gedurende een bepaalde metrische x-maal in de afgelopen 30 of 31 dagen zou zijn geactiveerd.</p><p>Als u vindt dat teveel alarm zou teweeggebracht zijn, kunt u de drempel in [ aanpassen leidt alarm ](/help/components/c-intelligent-alerts/alert-manager.md).</p><p>![](assets/alert-preview.png){width="50%"}</p> |
