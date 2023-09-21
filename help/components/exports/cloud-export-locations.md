---
description: De exportlocatie van de cloud configureren waar Customer Journey Analytics-gegevens kunnen worden verzonden
keywords: Analysis Workspace
title: Cloudexportlocaties configureren
feature: Components
hide: true
hidefromtoc: true
source-git-commit: c8f855ad5b586ed9ac3cde6889b6e73ecb216efa
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 1%

---

# Cloudexportlocaties configureren

Voordat u Customer Journey Analytics-rapporten kunt exporteren naar een cloudinrichting zoals beschreven in [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md), moet u de plaats toevoegen en vormen waar u de gegevens wilt worden verzonden.

Dit proces bestaat uit het toevoegen en configureren van de account (zoals Amazon S3, Google Cloud Platform, enzovoort) zoals beschreven in [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md)en vervolgens de locatie binnen die account (bijvoorbeeld een map binnen de account) toe te voegen en te configureren, zoals in dit artikel wordt beschreven.

Voor informatie over hoe u bestaande locaties kunt beheren, zoals het weergeven, bewerken en verwijderen van locaties, raadpleegt u [Locaties en accounts voor cloudexport beheren](/help/components/exports/manage-export-locations.md).

Een exportlocatie voor de cloud configureren:

1. U moet een account toevoegen voordat u een locatie kunt toevoegen. Voeg een account toe zoals beschreven in [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md).
1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].
1. Selecteer de [!UICONTROL **Locaties**] tab, dan selecteren [!UICONTROL **Locatie toevoegen**].

   ![knop Locatie toevoegen](assets/location-add.png)

   of

   Selecteer de [!UICONTROL **Locatieaccounts**] selecteert u het pictogram met drie punten op een bestaande account waaraan u een locatie wilt toevoegen en selecteert u vervolgens [!UICONTROL **Locatie toevoegen**].

   ![Locatie toevoegen aan bestaande account](assets/add-location-existing-account.png)

   Het dialoogvenster Locatie wordt weergegeven.

1. Geef de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam**] | De naam van de locatie.  | | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de rekening om deze te kunnen onderscheiden van andere rekeningen van hetzelfde type. | | [!UICONTROL **Locatieaccount**] | Selecteer de account waar u de locatie wilt maken. Voor informatie over het maken van een account raadpleegt u [Cloudexportaccounts configureren](/help/components/exports/cloud-export-accounts.md). |

1. In de [!UICONTROL **Locatie-eigenschappen**] in, geeft u specifieke informatie op over het accounttype van uw locatieaccount.

   Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met het accounttype dat u in het dialoogvenster [!UICONTROL **Locatieaccounts**] veld.

   +++Adobe Experience Platform Data Landing Zone

   Geef de volgende informatie op om een locatie in een Adobe Experience Platform Data Landing Zone te configureren:

   <!-- still need to update; can't create AEP account -->

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **IMS Org ID**] | De IMS Org-id wordt opgegeven door Adobe. Klik op het pictogram Kopiëren naast de knop [!UICONTROL **IMS Org ID**] om de inhoud van het veld te kopiëren, gebruikt u de id in uw account van het Platform voor Adobe. |
   | [!UICONTROL **Voorvoegsel**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |

+++

   +++Amazon S3 Role ARN

   Geef de volgende informatie op om een ARN-locatie voor Amazon S3 Role te configureren:

   <!-- still need to update; can't create S3 role ARN account -->

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat de gebruiker-ARN die door de Adobe is geleverd, toegang heeft om bestanden naar dit emmertje te uploaden. |
   | [!UICONTROL **Voorvoegsel**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

+++

   +++Google Cloud Platform

   Geef de volgende informatie op om een locatie voor een Google Cloud Platform te configureren:

   <!-- still need to update; can't create GCP account -->

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Emmertje**] | Het emmertje binnen uw rekening GCP waar u de gegevens van de Customer Journey Analytics wilt worden verzonden. Zorg ervoor dat u aan Opdrachtgever toestemming hebt verleend die door Adobe wordt verstrekt om dossiers aan dit emmertje te uploaden. (De Opdrachtgever wordt verstrekt wanneer [configureren van Google Cloud Platform-account](/help/components/exports/cloud-export-accounts.md).) Zie voor informatie over het verlenen van machtigingen [Voeg een hoofd aan een beleid op het niveau van de emmertje toe](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in de Google Cloud-documentatie. |
   | [!UICONTROL **Voorvoegsel**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

+++

   +++Azure SAS

   Geef de volgende informatie op om een Azure SAS-locatie te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Containernaam**] | De container binnen de account die u hebt opgegeven, waarin u de gegevens van de Customer Journey Analytics wilt verzenden. |
   | [!UICONTROL **Voorvoegsel**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |

   {style="table-layout:auto"}

+++

   +++Azure RBAC

   Geef de volgende informatie op om een Azure RBAC-locatie te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Container**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
   | [!UICONTROL **Voorvoegsel**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |
   | [!UICONTROL **Account**] | De Azure-opslagaccount. |

   {style="table-layout:auto"}

+++

   +++Snowflake

   Geef de volgende informatie op om de locatie van een Snowflake te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **DB**] | De standaarddatabase die moet worden gebruikt wanneer verbinding wordt gemaakt, of geeft een lege tekenreeks op. De opgegeven database moet een bestaande database zijn waarvoor de opgegeven standaardrol rechten heeft. <p>Zie de klasse [Referentiepagina voor de parameter voor de JDBC-stuurprogramma-verbinding in de documentatie bij Snowflake](https://docs.snowflake.com/en/developer-guide/jdbc/jdbc-parameters).</p> |
   | [!UICONTROL **Schema**] | Het standaardschema dat voor het gespecificeerde gegevensbestand moet worden gebruikt zodra verbonden, of specificeert een lege koord. Het gespecificeerde schema zou een bestaand schema moeten zijn waarvoor de gespecificeerde standaardrol voorrechten heeft. <p>Zie de klasse [Referentiepagina voor de parameter voor de JDBC-stuurprogramma-verbinding in de documentatie bij Snowflake](https://docs.snowflake.com/en/developer-guide/jdbc/jdbc-parameters).</p> |
   | [!UICONTROL **Werkgebiednaam**] | De naam van de locatie waar gegevensbestanden in Snowflake worden opgeslagen. <p>Zie de klasse [Een pagina Intern werkgebied voor lokale bestanden kiezen in de documentatie van Snowflake](https://docs.snowflake.com/en/user-guide/data-load-local-file-system-create-stage).</p> |
   | [!UICONTROL **Werkgebiedpad**] | Het pad naar de locatie waar gegevensbestanden in Snowflake worden opgeslagen. <p>Zie de klasse [Een pagina Intern werkgebied voor lokale bestanden kiezen in de documentatie van Snowflake](https://docs.snowflake.com/en/user-guide/data-load-local-file-system-create-stage).</p> |

   {style="table-layout:auto"}

+++

1. Selecteren [!UICONTROL **Opslaan**].

1. U kunt nu gegevens van Analysis Workspace exporteren naar de account en locatie die u hebt geconfigureerd. Ga voor informatie over het exporteren van gegevens naar de cloud naar [Projectgegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).
