---
description: Configureer de exportlocatie van de cloud waar Customer Journey Analytics-gegevens kunnen worden verzonden
keywords: Analysis Workspace
title: Cloudexportlocaties configureren
feature: Components
exl-id: 93f1cca0-95da-41a0-a4f9-5ab620a5b9da
role: User, Admin
source-git-commit: 6aea4179b368b50641a03a9cb53e4243fa428f4c
workflow-type: tm+mt
source-wordcount: '3132'
ht-degree: 0%

---

# Cloudexportlocaties configureren {#configure-cloud-export-locations}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-export-prefix"
>title="Voorvoegsel"
>abstract="De hoofdmap in de container waarin u de gegevens wilt plaatsen. Geef een statische mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Bijvoorbeeld: `folder_name/`"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-export-file-name"
>title="Bestandsnaam en pad"
>abstract="Geef een dynamische aangepaste bestandsnaam op die moet worden gebruikt voor automatische exportbewerkingen die naar deze locatie worden verzonden. U kunt ook een dynamisch aangepast bestandspad toevoegen aan de bestandsnaam. <br/> variabelen van het gebruik in het dossier - naam en weg om hen dynamisch te maken. <br/> Bijvoorbeeld, als u `${yyyy}/${MM}/${dd}/my-report-${instance_id}-${idx}` specificeert, zou de uitvoer die automatisch naar deze bestemming op 15 Januari wordt verzonden, 2026 de volgende dossierweg en naam hebben: `[prefix_folder_name]/2026/01/15/my-report-[UUID]-1.csv` <br/> Klik hieronder de verbinding voor een lijst van beschikbare variabelen."

<!-- markdownlint-enable MD034 -->

Alvorens u de rapporten van Customer Journey Analytics naar een wolkenbestemming (of van [&#x200B; Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md) of van [&#x200B; Report Builder &#x200B;](/help/report-builder/report-builder-export.md)) kunt uitvoeren, moet u de plaats toevoegen en vormen waar u de gegevens wilt worden verzonden. Dit proces bestaat uit:

1. Toevoegend en vormend de rekening (zoals Amazon S3, het Platform van de Wolk van Google, etc.) zoals die in [&#x200B; wordt beschreven vormt wolkenuitvoerrekeningen &#x200B;](/help/components/exports/cloud-export-accounts.md)

1. De locatie binnen die account toevoegen en configureren (bijvoorbeeld een map binnen de account), zoals beschreven in dit artikel.

Voor informatie over hoe te om bestaande plaatsen, met inbegrip van het bekijken, het uitgeven, en het schrappen van plaatsen te beheren, zie [&#x200B; wolkenuitvoerplaatsen en rekeningen beheren &#x200B;](/help/components/exports/manage-export-locations.md).

## Beginnen met het maken van een exportlocatie voor de cloud

1. U moet een account toevoegen voordat u een locatie kunt toevoegen. Als u niet reeds hebt, voeg een rekening toe zoals die in [&#x200B; wordt beschreven vormt de rekeningen van de wolkenuitvoer &#x200B;](/help/components/exports/cloud-export-accounts.md).

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer het [!UICONTROL **lusje van Plaatsen**], dan uitgezocht [!UICONTROL **plaats**] toevoegen.

   ![&#x200B; het venster van Uitvoer met het geselecteerde lusje van de Plaats die de Add plaatsknoop &#x200B;](assets/location-add.png) benadrukken

   of

   Selecteer de [!UICONTROL **rekeningen van de Plaats**] tabel, selecteer het 3 puntpictogram op een bestaande rekening waar u een plaats wilt toevoegen, dan selecteren [!UICONTROL **plaats**] toevoegen.

   ![&#x200B; GCP- rekening en ellipse drop-down menu die de Add geselecteerde plaats tonen &#x200B;](assets/add-location-existing-account.png)

   Het dialoogvenster Locatie wordt weergegeven.

1. Geef de volgende informatie op:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Naam**] | De naam van de locatie. |
   | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de locatie om deze te onderscheiden van andere locaties op de account. |
   | [!UICONTROL **plaats van het Merk beschikbaar aan alle gebruikers in uw organisatie**] | Schakel deze optie in als u wilt dat andere gebruikers in uw organisatie de locatie kunnen gebruiken. <p>Houd rekening met het volgende wanneer u locaties deelt:</p><ul><li>Locaties die u deelt, kunnen niet worden verwijderd.</li><li>Gedeelde locaties kunnen alleen door de eigenaar van de locatie worden bewerkt.</li><li>Locaties kunnen alleen worden gedeeld als de account waaraan de locatie is gekoppeld, ook wordt gedeeld.</li></ul> |
   | [!UICONTROL **de rekening van de Plaats**] | Selecteer de account waar u de locatie wilt maken. Voor informatie over hoe te om een rekening tot stand te brengen, zie [&#x200B; de rekeningen van de wolkenuitvoer &#x200B;](/help/components/exports/cloud-export-accounts.md) vormen. |

1. In de [!UICONTROL **eigenschappen van de Plaats**] sectie, specificeer informatie specifiek voor het accounttype van uw plaatsrekening.

   Ga met de sectie onder verder die aan het accounttype beantwoordt dat u op het [!UICONTROL **de rekeningsrekening van de Plaats**] gebied selecteerde.

   * [AEP Data Landing Zone](#aep-data-landing-zone)
   * [Amazon S3 Role ARN](#amazon-s3-role-arn)
   * [Google Cloud Platform](#google-cloud-platform)
   * [Azure SAS](#azure-sas)
   * [Azure RBAC](#azure-rbac)
   * [Snowflake](#snowflake)

### AEP Data Landing Zone

>[!IMPORTANT]
>
>Wanneer u rapporten van Customers Journey Analytics exporteert naar Adobe Experience Platform Data Landing Zone, dient u ervoor te zorgen dat u de gegevens binnen 7 dagen downloadt en deze vervolgens uit de AEP Data Landing Zone verwijdert. Na 7 dagen worden de gegevens automatisch verwijderd uit de AEP Data Landing Zone.

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; begin creërend een plaats van de wolkenuitvoer &#x200B;](#begin-creating-a-cloud-export-location)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables)

1. In de [!UICONTROL **eigenschappen van de Plaats**] sectie van [!UICONTROL **voeg plaats**] dialoogdoos toe, specificeer de volgende informatie om een plaats van de Gebied van de Gegevens van Adobe Experience Platform te vormen Landing:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Prefix**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een statische mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Bijvoorbeeld: `folder_name/` |
   | [!UICONTROL **de naam en weg van het Dossier**] | Geef een dynamische aangepaste bestandsnaam op die moet worden gebruikt voor geautomatiseerde exportbewerkingen die naar deze locatie worden verzonden. U kunt de bestandsnaam ook vooraf laten gaan door een dynamisch aangepast bestandspad. <p>Met deze optie kunt u het maken van bestandsnamen en het plaatsen van mappen automatiseren, zodat bestandsnamen voorspelbaar zijn en op een logische manier in mappen worden ingedeeld. Bestandsnamen kunnen bijvoorbeeld een naam krijgen op basis van de dag waarop ze zijn geleverd, en vervolgens worden geplaatst in mappen die met elke maand overeenkomen.</p><p>Gebruik een van de volgende variabelen in de bestandsnaam en het pad om ze dynamisch te maken:</p><ul><li>**{yyyy}**: kalenderjaar van 4 cijfers (hoofdlettergevoelig)</li><li>**{yy}**: 2-cijferig kalenderjaar (hoofdlettergevoelig)</li><li>**{MM}**: maand met 2 cijfers (hoofdlettergevoelig)</li><li>**{dd}**: Dag met 2 cijfers (hoofdlettergevoelig)</li><li>**{HH}**: 2-cijferig uur (hoofdlettergevoelig)</li><li>**{mm}**: 2-cijferige minuten (hoofdlettergevoelig)</li><li>**{ss}**: 2-cijferige seconden (hoofdlettergevoelig)</li><li>**{fff}**: 3-cijferige nanoseconden (hoofdlettergevoelig)</li><li>**{instance_id}**: UUID aanvragen (instantie)</li><li>**{export_id}**: UUID exporteren (planning)</li><li>**{idx}**: indexbegin vanaf 0 (telkens verhoogd voor elk bestand)</li><li>**{total}**: totaal bestandsnummer voor gehele overdrachtstaak</li><li>**{completion_millis}**: Overdrachtstijd in milliseconden</li></ul></p><p>Bijvoorbeeld, als u `${yyyy}/${MM}/${dd}/my-report-${instance_id} -${idx}` specificeert, zou de uitvoer die automatisch naar deze bestemming op 15 Januari wordt verzonden, 2026 de volgende dossierweg en naam hebben: [ prefix_folder_name ]/2026/01/15/my-report - [ UUID ] - 1.csv</p> |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Voor informatie over hoe te om gegevens naar de wolk uit te voeren, zie [&#x200B; projectgegevens van de Uitvoer naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md).

1. De eenvoudigste manier om toegang te krijgen tot uw gegevens in AEP Data Landing Zone is met de Microsoft Azure Storage Explorer. De Ontdekkingsreiziger van de Opslag is het zelfde hulpmiddel dat in de instructies wordt gebruikt om de [&#x200B; AEP Gegevens Landing Rekening van de Zone &#x200B;](/help/components/exports/cloud-export-accounts.md#aep-data-landing-zone) te vormen.

   1. Open de [&#x200B; Ontdekkingsreiziger van de Opslag van Microsoft Azure &#x200B;](https://azure.microsoft.com/en-us/products/storage/storage-explorer/).

   1. Ga naar [!UICONTROL **de Rekeningen van de Opslag**] > [!UICONTROL **(in bijlage)**] > [!UICONTROL **Blokcontainers**] > **[!UICONTROL cjaexport-_aantal_]** > ***your_container_name***.

      >[!NOTE]
      >
      >De omslagnaam **[!UICONTROL cjaexport-_aantal_]** is de standaardnaam die door de Ontdekkingsreiziger van de Opslag van Azure wordt verstrekt. Als u slechts één verbinding aan uw SAS URI (wat normaal is) hebt verbonden, dan zal de naam van deze omslag **[!UICONTROL cjaexport-1]** zijn.


      ![&#x200B; dossiers van de Toegang in de opslagontdekkingsreiziger van Azure &#x200B;](assets/azure-storage-explorer-access.png)

   1. Selecteer de uitvoer die u wilt downloaden, dan selecteren [!UICONTROL **Download**] om te downloaden.

### Amazon S3 Role ARN

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een wolkenuitvoerplaats &#x200B;](#begin-creating-a-cloud-export-location)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables)

1. In de [!UICONTROL **eigenschappen van de Plaats**] sectie van [!UICONTROL **voeg plaats**] dialoogdoos toe, specificeer de volgende informatie om een Amazon S3 plaats van de Rol ARN te vormen:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Emmertje**] | Het emmertje in uw Amazon S3-account waarin u Customer Journey Analytics-gegevens wilt verzenden. <p>Zorg ervoor dat de door Adobe verschafte Gebruiker-ARN over de `S3:PutObject` -machtiging beschikt om bestanden te uploaden naar dit emmertje. </p><p>Emmernamen moeten voldoen aan specifieke naamgevingsregels. Ze moeten bijvoorbeeld tussen 3 en 63 tekens lang zijn, ze mogen alleen bestaan uit kleine letters, cijfers, puntjes (.) en afbreekstreepjes (-) en ze moeten beginnen en eindigen met een letter of getal. [&#x200B; Een volledige lijst van het noemen van regels is beschikbaar in de documentatie van AWS &#x200B;](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
   | [!UICONTROL **Prefix**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een statische mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Map_name/ |
   | [!UICONTROL **de naam en weg van het Dossier**] | Geef een dynamische aangepaste bestandsnaam op die moet worden gebruikt voor automatische exportbewerkingen die naar deze locatie worden verzonden. U kunt ook een dynamisch aangepast bestandspad toevoegen aan de bestandsnaam. <p>Met deze optie kunt u het maken van bestandsnamen en het plaatsen van mappen automatiseren, zodat bestandsnamen voorspelbaar zijn en op logische wijze in mappen worden ingedeeld. Bestandsnamen kunnen bijvoorbeeld een naam krijgen die is gebaseerd op de dag waarop ze zijn bezorgd en vervolgens worden geplaatst in mappen die overeenkomen met elke maand.</p><p>Gebruik een van de volgende variabelen in de bestandsnaam en het pad om ze dynamisch te maken:</p><ul><li>**{yyyy}**: kalenderjaar van 4 cijfers (hoofdlettergevoelig)</li><li>**{yy}**: 2-cijferig kalenderjaar (hoofdlettergevoelig)</li><li>**{MM}**: maand met 2 cijfers (hoofdlettergevoelig)</li><li>**{dd}**: dag van 2 cijfers (hoofdlettergevoelig)</li><li>**{HH}**: 2-cijferig uur (hoofdlettergevoelig)</li><li>**{mm}**: minuten van 2 cijfers (hoofdlettergevoelig)</li><li>**{ss}**: seconden van 2 cijfers (hoofdlettergevoelig)</li><li>**{fff}**: 3-cijferige nanoseconden (hoofdlettergevoelig)</li><li>**{instance_id}**: UUID aanvragen (instantie)</li><li>**{export_id}**: UUID exporteren (planning)</li><li>**{idx}**: indexbegin vanaf 0 (verhoogd voor elk bestand)</li><li>**{total}**: Totaal aantal bestanden voor gehele overdrachtstaak</li><li>**{completion_millis}**: Overdrachtstijd in milliseconden</li></ul></p><p>Bijvoorbeeld, als u `${yyyy}/${MM}/${dd}/my-report-${instance_id} -${idx}` specificeert, zou de uitvoer die automatisch naar deze bestemming op 15 Januari wordt verzonden, 2026 de volgende dossierweg en naam hebben: [ prefix_folder_name ]/2026/01/15/my-report-[ UUID ] - 1.csv</p> |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

1. U kunt nu gegevens vanuit Analysis Workspace exporteren naar het account en de locatie die u hebt geconfigureerd. Voor informatie over hoe te om gegevens naar de wolk uit te voeren, zie [&#x200B; projectgegevens van de Uitvoer naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md).

### Google Cloud Platform

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een wolkenuitvoerplaats &#x200B;](#begin-creating-a-cloud-export-location)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables)

1. In de [!UICONTROL **eigenschappen van de Plaats**] sectie van [!UICONTROL **voeg plaats**] dialoogdoos toe, specificeer de volgende informatie om een plaats van het Platform van de Wolk van Google te vormen:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Emmertje**] | Het emmertje binnen uw GCP rekening waar u de gegevens van Customer Journey Analytics wilt worden verzonden. <p>Zorg ervoor dat u `roles/storage.objectCreator` toestemming hebt verleend aan Opdrachtgever die door Adobe wordt geleverd. (Het Belangrijkste wordt verstrekt wanneer [&#x200B; het vormen van de rekening van het Platform van de Wolk van Google &#x200B;](/help/components/exports/cloud-export-accounts.md).) <p>Voor informatie over het verlenen van toestemmingen, zie [&#x200B; een hoofd aan een emmertje-vlakke beleid &#x200B;](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in de documentatie van de Wolk van Google toevoegen.</p><p>Als uw organisatie [&#x200B; het beleidsbeperkingen van de Organisatie &#x200B;](https://cloud.google.com/storage/docs/org-policy-constraints) gebruikt om slechts de rekening van het Platform van de Wolk van Google in uw lijst van gewenste personen toe te staan, hebt u de volgende Adobe bezeten de organisatieidentiteitskaart van het Platform van Google Cloud nodig: <ul><li>`DISPLAY_NAME`: `adobe.com`</li><li>`ID`: `178012854243`</li><li>`DIRECTORY_CUSTOMER_ID`: `C02jo8puj`</li></ul> </p> |
   | [!UICONTROL **Prefix**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een statische mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Map_name/ |
   | [!UICONTROL **de naam en weg van het Dossier**] | Geef een dynamische aangepaste bestandsnaam op die moet worden gebruikt voor automatische exportbewerkingen die naar deze locatie worden verzonden. U kunt ook een dynamisch aangepast bestandspad toevoegen aan de bestandsnaam. <p>Met deze optie kunt u het maken van bestandsnamen en het plaatsen van mappen automatiseren, zodat bestandsnamen voorspelbaar zijn en op logische wijze in mappen worden ingedeeld. Bestandsnamen kunnen bijvoorbeeld een naam krijgen die is gebaseerd op de dag waarop ze zijn bezorgd en vervolgens worden geplaatst in mappen die overeenkomen met elke maand.</p><p>Gebruik een van de volgende variabelen in de bestandsnaam en het pad om ze dynamisch te maken:</p><ul><li>**{yyyy}**: kalenderjaar van 4 cijfers (hoofdlettergevoelig)</li><li>**{yy}**: 2-cijferig kalenderjaar (hoofdlettergevoelig)</li><li>**{MM}**: maand met 2 cijfers (hoofdlettergevoelig)</li><li>**{dd}**: Dag met 2 cijfers (hoofdlettergevoelig)</li><li>**{HH}**: 2-cijferig uur (hoofdlettergevoelig)</li><li>**{mm}**: minuten van 2 cijfers (hoofdlettergevoelig)</li><li>**{ss}**: 2-cijferige seconden (hoofdlettergevoelig)</li><li>**{fff}**: 3-cijferige nanoseconden (hoofdlettergevoelig)</li><li>**{instance_id}**: UUID aanvragen (instantie)</li><li>**{export_id}**: UUID exporteren (planning)</li><li>**{idx}**: indexbegin vanaf 0 (telkens verhoogd voor elk bestand)</li><li>**{total}**: totaal bestandsnummer voor gehele overdrachtstaak</li><li>**{completion_millis}**: Overdrachtstijd in milliseconden</li></ul></p><p>Bijvoorbeeld, als u `${yyyy}/${MM}/${dd}/my-report-${instance_id} -${idx}` specificeert, zou de uitvoer die automatisch naar deze bestemming op 15 Januari wordt verzonden, 2026 de volgende dossierweg en naam hebben: [ prefix_folder_name ]/2026/01/15/my-report - [ UUID ] - 1.csv</p> |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Voor informatie over hoe te om gegevens naar de wolk uit te voeren, zie [&#x200B; projectgegevens van de Uitvoer naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md).

### Azure SAS

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een wolkenuitvoerplaats &#x200B;](#begin-creating-a-cloud-export-location)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables)

1. In de [!UICONTROL **eigenschappen van de Plaats**] sectie van [!UICONTROL **voeg plaats**] dialoogdoos toe, specificeer de volgende informatie om een plaats van Azure SAS te vormen:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Naam van de Container**] | De container in het account dat u hebt opgegeven, waarin u de gegevens van de Customer Journey Analytics wilt verzenden. |
   | [!UICONTROL **Prefix**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een statische mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Bijvoorbeeld: `folder_name/`<p>Zorg ervoor dat de `Write` machtiging is verleend voor de opslag van SAS-token die u in het geheime naamveld Key Vault hebt opgegeven bij de configuratie van de Azure SAS-account. Hierdoor kan de SAS-token bestanden in uw Azure-container maken. <p>Als u wilt dat het SAS-token ook bestanden kan overschrijven, controleert u of de SAS-token-winkel de machtiging `Delete` heeft.</p><p>Voor meer informatie, zie [&#x200B; de opslagmiddelen van de Blob &#x200B;](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources) in de Azure documentatie van de Opslag van Blob.</p> |
   | [!UICONTROL **Naam van het Dossier en weg**] | Geef een dynamische aangepaste bestandsnaam op die moet worden gebruikt voor automatische exportbewerkingen die naar deze locatie worden verzonden. U kunt de bestandsnaam ook vooraf laten gaan door een dynamisch aangepast bestandspad. <p>Met deze optie kunt u het maken van bestandsnamen en het plaatsen van mappen automatiseren, zodat bestandsnamen voorspelbaar zijn en op een logische manier in mappen worden ingedeeld. Bestandsnamen kunnen bijvoorbeeld een naam krijgen op basis van de dag waarop ze zijn geleverd, en vervolgens worden geplaatst in mappen die met elke maand overeenkomen.</p><p>Gebruik een van de volgende variabelen in de bestandsnaam en het pad om ze dynamisch te maken:</p><ul><li>**{yyyy}**: kalenderjaar van 4 cijfers (hoofdlettergevoelig)</li><li>**{yy}**: 2-cijferig kalenderjaar (hoofdlettergevoelig)</li><li>**{MM}**: maand met 2 cijfers (hoofdlettergevoelig)</li><li>**{dd}**: Dag met 2 cijfers (hoofdlettergevoelig)</li><li>**{HH}**: 2-cijferig uur (hoofdlettergevoelig)</li><li>**{mm}**: 2-cijferige minuten (hoofdlettergevoelig)</li><li>**{ss}**: 2-cijferige seconden (hoofdlettergevoelig)</li><li>**{fff}**: 3-cijferige nanoseconden (hoofdlettergevoelig)</li><li>**{instance_id}**: UUID aanvragen (instantie)</li><li>**{export_id}**: UUID exporteren (planning)</li><li>**{idx}**: indexbegin vanaf 0 (telkens verhoogd voor elk bestand)</li><li>**{total}**: totaal bestandsnummer voor gehele overdrachtstaak</li><li>**{completion_millis}**: Overdrachtstijd in milliseconden</li></ul></p><p>Bijvoorbeeld, als u `${yyyy}/${MM}/${dd}/my-report-${instance_id} -${idx}` specificeert, zou de uitvoer die automatisch naar deze bestemming op 15 Januari wordt verzonden, 2026 de volgende dossierweg en naam hebben: [ prefix_folder_name ]/2026/01/15/my-report - [ UUID ] - 1.csv</p> |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Voor informatie over hoe te om gegevens naar de wolk uit te voeren, zie [&#x200B; projectgegevens van de Uitvoer naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md).

### Azure RBAC

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een wolkenuitvoerplaats &#x200B;](#begin-creating-a-cloud-export-location)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables)

1. In de [!UICONTROL **eigenschappen van de Plaats**] sectie van [!UICONTROL **voeg plaats**] dialoogdoos toe, specificeer de volgende informatie om een plaats van Azure RBAC te vormen:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Container**] | De container in de account die u hebt opgegeven, waarnaar u Customer Journey Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
   | [!UICONTROL **Prefix**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een statische mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Bijvoorbeeld: `folder_name/`<p>Zorg ervoor dat de toepassings-id die u hebt opgegeven bij het configureren van het Azure RBAC-account, is toegewezen aan de rol `Storage Blob Data Contributor` om toegang te krijgen tot de container (map).</p> <p>Voor meer informatie, zie [&#x200B; Azure ingebouwde rollen &#x200B;](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p> |
   | [!UICONTROL **de naam en weg van het Dossier**] | Geef een dynamische aangepaste bestandsnaam op die moet worden gebruikt voor automatische exportbewerkingen die naar deze locatie worden verzonden. U kunt ook een dynamisch aangepast bestandspad toevoegen aan de bestandsnaam. <p>Met deze optie kunt u het maken van bestandsnamen en het plaatsen van mappen automatiseren, zodat bestandsnamen voorspelbaar zijn en op logische wijze in mappen worden ingedeeld. Bestandsnamen kunnen bijvoorbeeld een naam krijgen die is gebaseerd op de dag waarop ze zijn bezorgd en vervolgens worden geplaatst in mappen die overeenkomen met elke maand.</p> <p>Gebruik een van de volgende variabelen in de bestandsnaam en het pad om ze dynamisch te maken:</p><ul><li>**{yyyy}**: kalenderjaar van 4 cijfers (hoofdlettergevoelig)</li><li>**{yy}**: 2-cijferig kalenderjaar (hoofdlettergevoelig)</li><li>**{MM}**: maand met 2 cijfers (hoofdlettergevoelig)</li><li>**{dd}**: Dag met 2 cijfers (hoofdlettergevoelig)</li><li>**{HH}**: 2-cijferig uur (hoofdlettergevoelig)</li><li>**{mm}**: 2-cijferige minuten (hoofdlettergevoelig)</li><li>**{ss}**: 2-cijferige seconden (hoofdlettergevoelig)</li><li>**{fff}**: 3-cijferige nanoseconden (hoofdlettergevoelig)</li><li>**{instance_id}**: UUID aanvragen (instantie)</li><li>**{export_id}**: UUID exporteren (planning)</li><li>**{idx}**: indexbegin vanaf 0 (verhoogd voor elk bestand)</li><li>**{total}**: Totaal aantal bestanden voor gehele overdrachtstaak</li><li>**{completion_millis}**: tijdstip van overdracht in milliseconden</li></ul></p><p>Bijvoorbeeld, als u `${yyyy}/${MM}/${dd}/my-report-${instance_id} -${idx}` specificeert, zou de uitvoer die automatisch naar deze bestemming op 15 Januari wordt verzonden, 2026 de volgende dossierweg en naam hebben: [ prefix_folder_name ]/2026/01/15/my-report-[ UUID ] - 1.csv</p> |
   | [!UICONTROL **Rekening**] | De Azure-opslagaccount. |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Voor informatie over hoe te om gegevens naar de wolk uit te voeren, zie [&#x200B; projectgegevens van de Uitvoer naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md).

### Snowflake

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een wolkenuitvoerplaats &#x200B;](#begin-creating-a-cloud-export-location)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables)

1. In de [!UICONTROL **eigenschappen van de Plaats**] sectie van [!UICONTROL **voeg plaats**] dialoogdoos toe, specificeer de volgende informatie om een plaats van Snowflake te vormen:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **OB**] | De opgegeven database moet een bestaande database zijn. De rol u creeerde moet voorrechten hebben om tot dit gegevensbestand toegang te hebben.<p>Dit is de database die is gekoppeld aan de naam van het werkgebied.</p><p>U kunt deze rol voorrechten aan het gegevensbestand in Snowflake verlenen gebruikend het volgende bevel: `GRANT USAGE ON DATABASE <your_database> TO ROLE <your_role>;`</p> <p>Voor meer informatie, zie het [&#x200B; Gegevensbestand, Schema, en de pagina van de Bevelen van het Aandeel in de documentatie van Snowflake &#x200B;](https://docs.snowflake.com/en/sql-reference/commands-database).</p> |
   | [!UICONTROL **Schema**] | Het opgegeven schema moet een bestaand schema zijn. De rol u creeerde moet voorrechten hebben om tot dit schema toegang te hebben.<p>Dit is het schema dat aan de naam van het werkgebied is gekoppeld.</p><p>U kunt de rol die u hebt gemaakt, rechten toekennen aan het schema in Snowflake met de volgende opdracht: `GRANT USAGE ON SCHEMA <your_database>.<your_schema> TO ROLE <your_role>;`</p><p>Voor meer informatie, zie het [&#x200B; Gegevensbestand, Schema, en de pagina van de Bevelen van het Aandeel in de documentatie van Snowflake &#x200B;](https://docs.snowflake.com/en/sql-reference/commands-database).</p> |
   | [!UICONTROL **naam van het Stadium**] | De naam van het interne werkgebied waarin gegevensbestanden worden opgeslagen in Snowflake.<p>Zorg ervoor dat de rol die u op de account hebt opgegeven, lees- en schrijftoegang heeft tot deze werkgebiednaam. (Omdat u Lezen en Schrijven toegang verleent, adviseren wij gebruikend een stadium dat slechts door Adobe wordt gebruikt.)</p><p>U kunt Lezen en Schrijven toegang tot de werkgebiednaam verlenen in Snowflake met de volgende opdracht: `GRANT READ, WRITE ON STAGE <your_database>.<your_schema>.<your_stage_name> TO ROLE <your_role>;`</p> <p>Voor informatie over het verlenen van voorrechten aan een rol, zie [&#x200B; voorrechten van de Verlening in de documentatie van Snowflake &#x200B;](https://docs.snowflake.com/en/sql-reference/sql/grant-privilege).</p> <p>Voor meer informatie over de werkgebiednaam, zie [&#x200B; het Kiezen van een Intern Stadium voor de Lokale pagina van Dossiers in de documentatie van Snowflake &#x200B;](https://docs.snowflake.com/en/user-guide/data-load-local-file-system-create-stage).</p> |
   | [!UICONTROL **weg van het Stadium**] | Het pad naar de locatie waar gegevensbestanden worden opgeslagen in Snowflake. <p>Voor meer informatie, zie [&#x200B; het Kiezen van een Intern Stadium voor de Lokale pagina van Dossiers in de documentatie van Snowflake &#x200B;](https://docs.snowflake.com/en/user-guide/data-load-local-file-system-create-stage).</p> |
   | [!UICONTROL **de naam en weg van het Dossier**] | Geef een dynamische aangepaste bestandsnaam op die moet worden gebruikt voor automatische exportbewerkingen die naar deze locatie worden verzonden. U kunt ook een dynamisch aangepast bestandspad toevoegen aan de bestandsnaam. <p>Met deze optie kunt u het maken van bestandsnamen en het plaatsen van mappen automatiseren, zodat bestandsnamen voorspelbaar zijn en op logische wijze in mappen worden ingedeeld. Bestandsnamen kunnen bijvoorbeeld een naam krijgen die is gebaseerd op de dag waarop ze zijn bezorgd en vervolgens worden geplaatst in mappen die overeenkomen met elke maand.</p><p>Gebruik een van de volgende variabelen in de bestandsnaam en het pad om ze dynamisch te maken:</p><ul><li>**{yyyy}**: kalenderjaar van 4 cijfers (hoofdlettergevoelig)</li><li>**{yy}**: 2-cijferig kalenderjaar (hoofdlettergevoelig)</li><li>**{MM}**: maand met 2 cijfers (hoofdlettergevoelig)</li><li>**{dd}**: Dag met 2 cijfers (hoofdlettergevoelig)</li><li>**{HH}**: 2-cijferig uur (hoofdlettergevoelig)</li><li>**{mm}**: 2-cijferige minuten (hoofdlettergevoelig)</li><li>**{ss}**: 2-cijferige seconden (hoofdlettergevoelig)</li><li>**{fff}**: 3-cijferige nanoseconden (hoofdlettergevoelig)</li><li>**{instance_id}**: UUID aanvragen (instantie)</li><li>**{export_id}**: UUID exporteren (planning)</li><li>**{idx}**: indexbegin vanaf 0 (telkens verhoogd voor elk bestand)</li><li>**{total}**: totaal bestandsnummer voor gehele overdrachtstaak</li><li>**{completion_millis}**: Overdrachtstijd in milliseconden</li></ul></p><p>Bijvoorbeeld, als u `${yyyy}/${MM}/${dd}/my-report-${instance_id} -${idx}` specificeert, zou de uitvoer die automatisch naar deze bestemming op 15 Januari wordt verzonden, 2026 de volgende dossierweg en naam hebben: [ prefix_folder_name ]/2026/01/15/my-report - [ UUID ] - 1.csv</p> |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Voor informatie over hoe te om gegevens naar de wolk uit te voeren, zie [&#x200B; projectgegevens van de Uitvoer naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md).
