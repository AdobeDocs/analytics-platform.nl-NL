---
description: De exportlocatie van de cloud configureren waar Customer Journey Analytics-gegevens kunnen worden verzonden
keywords: Analysis Workspace
title: Cloudexportlocaties configureren
feature: Components
exl-id: 93f1cca0-95da-41a0-a4f9-5ab620a5b9da
role: User, Admin
source-git-commit: 1bf36f60b0b3aec04bb1452e5f63f97051d9bb50
workflow-type: tm+mt
source-wordcount: '1928'
ht-degree: 0%

---

# Cloudexportlocaties configureren

Voordat u Customer Journey Analytics-rapporten kunt exporteren naar een cloudinrichting zoals beschreven in [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md), moet u de plaats toevoegen en vormen waar u de gegevens wilt worden verzonden.

Dit proces bestaat uit het toevoegen en configureren van de account (zoals Amazon S3, Google Cloud Platform, enzovoort) zoals beschreven in [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md)en vervolgens de locatie binnen die account (bijvoorbeeld een map binnen de account) toe te voegen en te configureren, zoals in dit artikel wordt beschreven.

Voor informatie over hoe u bestaande locaties kunt beheren, zoals het weergeven, bewerken en verwijderen van locaties, raadpleegt u [Locaties en accounts voor cloudexport beheren](/help/components/exports/manage-export-locations.md).

## Beginnen met het maken van een exportlocatie voor de cloud

1. U moet een account toevoegen voordat u een locatie kunt toevoegen. Voeg een account toe zoals beschreven in [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md).

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Locaties**] tab, dan selecteren [!UICONTROL **Locatie toevoegen**].

   ![Exporteert het venster met het geselecteerde tabblad Locatie en markeert de knop Locatie toevoegen](assets/location-add.png)

   of

   Selecteer de [!UICONTROL **Locatieaccounts**] selecteert u het pictogram met drie punten op een bestaande account waaraan u een locatie wilt toevoegen en selecteert u vervolgens [!UICONTROL **Locatie toevoegen**].

   ![GCP-account en keuzemenu voor elipsis met de optie Locatie toevoegen geselecteerd](assets/add-location-existing-account.png)

   Het dialoogvenster Locatie wordt weergegeven.

1. Geef de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam**] | De naam van de locatie.  | | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de locatie om deze te onderscheiden van andere locaties op de account. | | [!UICONTROL **Locatie beschikbaar maken voor alle gebruikers in uw organisatie**] | **Opmerking:** Deze functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Release van de Customer Journey Analytics-functie](/help/release-notes/releases.md). <p>Schakel deze optie in als u wilt dat andere gebruikers in uw organisatie de locatie kunnen gebruiken.</p> <p>Houd rekening met het volgende wanneer u locaties deelt:</p><ul><li>Locaties die u deelt, kunnen niet worden verwijderd.</li><li>Gedeelde locaties kunnen alleen door de eigenaar van de locatie worden bewerkt.</li><li>Locaties kunnen alleen worden gedeeld als de account waaraan de locatie is gekoppeld, ook wordt gedeeld.</li></ul> | | [!UICONTROL **Locatieaccount**] | Selecteer de account waar u de locatie wilt maken. Voor informatie over het maken van een account raadpleegt u [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md). |

1. In de [!UICONTROL **Locatie-eigenschappen**] in, geeft u specifieke informatie op over het accounttype van uw locatieaccount.

   Doorgaan met de sectie hieronder die overeenkomt met het accounttype dat u hebt geselecteerd in het dialoogvenster [!UICONTROL **Locatieaccount**] veld.

   * [AEP gegevenslandingszone](#aep-data-landing-zone)
   * [Amazon S3 Role ARN](#amazon-s3-role-arn)
   * [Google Cloud Platform](#google-cloud-platform)
   * [Azure SAS](#azure-sas)
   * [Azure RBAC](#azure-rbac)
   * [Snowflake](#snowflake)

### AEP gegevenslandingszone

>[!IMPORTANT]
>
>Wanneer het uitvoeren van de rapporten van de Customer Journey Analytics aan de Landing Zone van Adobe Experience Platform Gegevens, zorg ervoor dat u de gegevens binnen 7 dagen downloadt, dan schrapt het uit de Gebied van Gegevens AEP. Na 7 dagen worden de gegevens automatisch verwijderd uit de AEP Data Landing Zone.

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Vanaf de pagina Exporteren, zoals hierboven beschreven, in [Beginnen met het maken van een exportlocatie voor de cloud](#begin-creating-a-cloud-export-location)

   * Wanneer [volledige tabellen exporteren vanuit Analysis Workspace](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **Locatie-eigenschappen**] van de [!UICONTROL **Locatie toevoegen**] geeft u de volgende informatie op om een locatie in een Adobe Experience Platform Data Landing Zone te configureren:

   <!-- still need to update; can't create AEP account -->

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Voorvoegsel**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Bijvoorbeeld: `folder_name/` |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Ga voor informatie over het exporteren van gegevens naar de cloud naar [Projectgegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).

1. De eenvoudigste manier om toegang te krijgen tot uw gegevens in de AEP Data Landing Zone is om de Microsoft Azure Storage Explorer te gebruiken. Dit is het zelfde hulpmiddel dat in de instructies wordt gebruikt om te vormen [AEP-rekening gegevenslandingszone](/help/components/exports/cloud-export-accounts.md#aep-data-landing-zone).

   1. Open de [Microsoft Azure Storage Explorer](https://azure.microsoft.com/en-us/products/storage/storage-explorer/).

   1. Ga naar [!UICONTROL **Opslagaccounts**] > [!UICONTROL **(Bijgevoegde containers)**] > [!UICONTROL **Kloddercontainers**] > **[!UICONTROL cjaexport-_getal_]** > ***your_container_name***.

      >[!NOTE]
      >
      >De mapnaam **[!UICONTROL cjaexport-_getal_]** Dit is de standaardnaam die wordt verschaft door Azure Storage Explorer. Als u slechts één verbinding verbonden met uw SAS URI (wat normaal is) hebt, dan zal de naam van deze omslag zijn **[!UICONTROL cjaexport-1]**.


      ![Bestanden openen in Azure Storage Explorer](assets/azure-storage-explorer-access.png)

   1. Selecteer de exportbewerking die u wilt downloaden en selecteer vervolgens [!UICONTROL **Downloaden**] om te downloaden.

### Amazon S3 Role ARN

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Vanaf de pagina Exporteren, zoals hierboven beschreven, in [Beginnen met het maken van een exportlocatie voor de cloud](#begin-creating-a-cloud-export-location)

   * Wanneer [volledige tabellen exporteren vanuit Analysis Workspace](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **Locatie-eigenschappen**] van de [!UICONTROL **Locatie toevoegen**] geeft u de volgende informatie op om een ARN-locatie voor Amazon S3 Role te configureren:

   <!-- still need to update; can't create S3 role ARN account -->

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Emmertje**] | Het emmertje binnen uw Amazon S3 rekening waar u de gegevens van de Customer Journey Analytics wilt verzenden. <p>Zorg ervoor dat de gebruiker-ARN die door de Adobe is geleverd, de `S3:PutObject` toestemming om bestanden naar dit emmertje te uploaden. </p><p>Emmernamen moeten voldoen aan specifieke naamgevingsregels. Ze moeten bijvoorbeeld tussen 3 en 63 tekens lang zijn, ze mogen alleen bestaan uit kleine letters, cijfers, puntjes (.) en afbreekstreepjes (-) en ze moeten beginnen en eindigen met een letter of getal. [Een volledige lijst met naamgevingsregels is beschikbaar in de documentatie van AWS](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
   | [!UICONTROL **Voorvoegsel**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Ga voor informatie over het exporteren van gegevens naar de cloud naar [Projectgegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).

### Google Cloud Platform

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Vanaf de pagina Exporteren, zoals hierboven beschreven, in [Beginnen met het maken van een exportlocatie voor de cloud](#begin-creating-a-cloud-export-location)

   * Wanneer [volledige tabellen exporteren vanuit Analysis Workspace](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **Locatie-eigenschappen**] van de [!UICONTROL **Locatie toevoegen**] geeft u de volgende informatie op om een locatie voor een Google Cloud Platform te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Emmertje**] | Het emmertje binnen uw rekening GCP waar u de gegevens van de Customer Journey Analytics wilt worden verzonden. <p>Zorg ervoor dat u de `roles/storage.objectCreator` toestemming aan de Opdrachtgever verleend door Adobe. (De Opdrachtgever wordt verstrekt wanneer [configureren van Google Cloud Platform-account](/help/components/exports/cloud-export-accounts.md).) <p>Zie voor informatie over het verlenen van machtigingen [Voeg een hoofd aan een beleid op het niveau van de emmertje toe](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in de Google Cloud-documentatie.</p><p>Als uw organisatie [Beleidsbeperkingen van de organisatie](https://cloud.google.com/storage/docs/org-policy-constraints) Als u alleen de Google Cloud Platform-account in uw lijst van gewenste personen wilt toestaan, hebt u de volgende Google Cloud Platform-organisatie-id nodig die eigendom is van de Adobe: <ul><li>`DISPLAY_NAME`: `adobe.com`</li><li>`ID`: `178012854243`</li><li>`DIRECTORY_CUSTOMER_ID`: `C02jo8puj`</li></ul> </p> |
   | [!UICONTROL **Voorvoegsel**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Ga voor informatie over het exporteren van gegevens naar de cloud naar [Projectgegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).

### Azure SAS

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Vanaf de pagina Exporteren, zoals hierboven beschreven, in [Beginnen met het maken van een exportlocatie voor de cloud](#begin-creating-a-cloud-export-location)

   * Wanneer [volledige tabellen exporteren vanuit Analysis Workspace](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **Locatie-eigenschappen**] van de [!UICONTROL **Locatie toevoegen**] geeft u de volgende informatie op om een Azure SAS-locatie te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Containernaam**] | De container binnen de account die u hebt opgegeven, waarin u de gegevens van de Customer Journey Analytics wilt verzenden. |
   | [!UICONTROL **Voorvoegsel**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Bijvoorbeeld: `folder_name/`<p>Zorg ervoor dat het SAS-tokenarchief dat u in het geheime naamveld Key Vault hebt opgegeven bij de configuratie van de Azure SAS-account, de `Write` toestemming. Hierdoor kan de SAS-token bestanden in uw Azure-container maken. <p>Als u wilt dat het SAS-token ook bestanden kan overschrijven, zorgt u ervoor dat de SAS-tokenwinkel de `Delete` toestemming.</p><p>Zie voor meer informatie [Bronnen voor blokopslag](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources) in de Azure Blob Storage-documentatie.</p> |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Ga voor informatie over het exporteren van gegevens naar de cloud naar [Projectgegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).

### Azure RBAC

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Vanaf de pagina Exporteren, zoals hierboven beschreven, in [Beginnen met het maken van een exportlocatie voor de cloud](#begin-creating-a-cloud-export-location)

   * Wanneer [volledige tabellen exporteren vanuit Analysis Workspace](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **Locatie-eigenschappen**] van de [!UICONTROL **Locatie toevoegen**] geeft u de volgende informatie op om een Azure RBAC-locatie te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Container**] | De container binnen de account die u hebt opgegeven, waarin u de gegevens van de Customer Journey Analytics wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
   | [!UICONTROL **Voorvoegsel**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens na de naam een schuine streep toe om de map te maken. Bijvoorbeeld: `folder_name/`<p>Zorg ervoor dat de toepassings-id die u hebt opgegeven bij het configureren van de Azure RBAC-account, is toegewezen aan de `Storage Blob Data Contributor` rol om tot de container (omslag) toegang te hebben.</p> <p>Zie voor meer informatie [Azure ingebouwde rollen](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p> |
   | [!UICONTROL **Account**] | De Azure-opslagaccount. |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Ga voor informatie over het exporteren van gegevens naar de cloud naar [Projectgegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).

### Snowflake

1. Ga op een van de volgende manieren te werk om een exportlocatie voor de cloud te maken:

   * Vanaf de pagina Exporteren, zoals hierboven beschreven, in [Beginnen met het maken van een exportlocatie voor de cloud](#begin-creating-a-cloud-export-location)

   * Wanneer [volledige tabellen exporteren vanuit Analysis Workspace](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **Locatie-eigenschappen**] van de [!UICONTROL **Locatie toevoegen**] geeft u de volgende informatie op om de locatie van een Snowflake te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **DB**] | De opgegeven database moet een bestaande database zijn. De rol u creeerde moet voorrechten hebben om tot dit gegevensbestand toegang te hebben.<p>Dit is de database die is gekoppeld aan de naam van het werkgebied.</p><p>U kunt deze rolvoorrechten aan het gegevensbestand in Snowflake verlenen gebruikend het volgende bevel: `GRANT USAGE ON DATABASE <your_database> TO ROLE <your_role>;`</p> <p>Zie de klasse [Database-, Schema- en Share Commands-pagina in de documentatie van de Snowflake](https://docs.snowflake.com/en/sql-reference/commands-database).</p> |
   | [!UICONTROL **Schema**] | Het opgegeven schema moet een bestaand schema zijn. De rol u creeerde moet voorrechten hebben om tot dit schema toegang te hebben.<p>Dit is het schema dat aan de naam van het werkgebied is gekoppeld.<p>U kunt de rol verlenen die u voorrechten aan het schema in Snowflake gebruikend het volgende bevel creeerde: `GRANT USAGE ON SCHEMA <your_database>.<your_schema> TO ROLE <your_role>;`</p><p>Zie de klasse [Database-, Schema- en Share Commands-pagina in de documentatie van de Snowflake](https://docs.snowflake.com/en/sql-reference/commands-database).</p> |
   | [!UICONTROL **Werkgebiednaam**] | De naam van het interne werkgebied waarin gegevensbestanden in Snowflake worden opgeslagen.<p>Zorg ervoor dat de rol die u op de account hebt opgegeven, lees- en schrijftoegang heeft tot deze werkgebiednaam. (Omdat u Gelezen en schrijft toegang verleent, adviseren wij gebruikend een stadium dat slechts door Adobe wordt gebruikt.)<p>U kunt Lezen en schrijven toegang tot de werkgebiednaam in Snowflake verlenen gebruikend het volgende bevel: `GRANT READ, WRITE ON STAGE <your_database>.<your_schema>.<your_stage_name> TO ROLE <your_role>;`</p> <p>Voor informatie over het verlenen van bevoegdheden aan een rol raadpleegt u [Rechten verlenen in de documentatie van de Snowflake](https://docs.snowflake.com/en/sql-reference/sql/grant-privilege). <p>Zie de klasse [Een pagina Intern werkgebied voor lokale bestanden kiezen in de documentatie van Snowflake](https://docs.snowflake.com/en/user-guide/data-load-local-file-system-create-stage).</p> |
   | [!UICONTROL **Werkgebiedpad**] | Het pad naar de locatie waar gegevensbestanden in Snowflake worden opgeslagen. <p>Zie de klasse [Een pagina Intern werkgebied voor lokale bestanden kiezen in de documentatie van Snowflake](https://docs.snowflake.com/en/user-guide/data-load-local-file-system-create-stage).</p> |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Ga voor informatie over het exporteren van gegevens naar de cloud naar [Projectgegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).
