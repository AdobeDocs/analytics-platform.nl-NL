---
description: De exportaccount voor de cloud configureren waar Customer Journey Analytics-gegevens kunnen worden verzonden
keywords: Analysis Workspace
title: Cloudexportaccounts configureren
feature: Components
hide: true
hidefromtoc: true
source-git-commit: bcbd7ebb075a0d25b566fa8be164d6817bedf2e5
workflow-type: tm+mt
source-wordcount: '1288'
ht-degree: 0%

---

# Cloudexportaccounts configureren

{{select-package}}

Voordat u Customer Journey Analytics-gegevens kunt exporteren naar een cloudinrichting zoals beschreven in [Gegevens van Customers Journey Analytics exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md), moet u de plaats toevoegen en vormen waar u de gegevens wilt worden verzonden.

Dit proces bestaat uit het toevoegen en configureren van de account (zoals Amazon S3, Google Cloud Platform, enzovoort), zoals beschreven in dit artikel, en vervolgens het toevoegen en configureren van de locatie binnen die account (zoals een map binnen de account) zoals beschreven in [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md).

Ga voor informatie over het beheren van bestaande accounts, zoals het weergeven, bewerken en verwijderen van accounts naar [Locaties en accounts voor cloudexport beheren](/help/components/exports/manage-export-locations.md).

U moet Customer Journey Analytics met de noodzakelijke informatie vormen om tot uw rekening van de wolkenbestemming toegang te hebben.

Een cloudexportaccount configureren:

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].
1. Op de [!UICONTROL Exports] pagina, selecteert u de [!UICONTROL **Locatieaccounts**] tab.
1. Selecteren [!UICONTROL **Account toevoegen**].

   ![Account toevoegen](assets/account-add.png)

   Het dialoogvenster Account toevoegen wordt weergegeven.
1. Geef de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam van locatieaccount**] | De naam van de locatieaccount. Deze naam wordt weergegeven wanneer u een locatie maakt | | [!UICONTROL **Beschrijving van locatieaccount**] | Geef een korte beschrijving van de rekening om deze te kunnen onderscheiden van andere rekeningen van hetzelfde type. | | [!UICONTROL **Accounttype**] | Selecteer het type cloudaccount waarnaar u exporteert. Beschikbare accounttypen zijn Amazon S3 Role ARN, Google Cloud Platform, Azure SAS, Azure RBAC, Snowflake en Adobe Experience Platform. |
1. In de [!UICONTROL **Accounteigenschappen**] in, geeft u specifieke informatie op over het accounttype dat u hebt geselecteerd.

   Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met de [!UICONTROL **Accounttype**] die u hebt geselecteerd.

   +++Amazon S3 Role ARN

   Geef de volgende informatie op om een Amazon S3 Role ARN-account te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Rol ARN**] | U moet een Rol ARN (de Naam van het Middel van Amazon) verstrekken die de Adobe kan gebruiken om toegang tot de rekening van Amazon S3 te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Zie voor specifieke informatie [deze AWS-documentatie](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
   | [!UICONTROL **ARN gebruiker**] | De Gebruiker ARN (de Naam van het Middel van Amazon) wordt verstrekt door Adobe. U moet deze gebruiker aan het beleid vastmaken u creeerde. |

   {style="table-layout:auto"}

+++

   +++Google Cloud Platform

   Geef de volgende informatie op om een Google Cloud Platform-account te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Project-id**] | Uw Google Cloud-project-id die u kopieert van uw Google Cloud-account. Zie de [Google Cloud-documentatie over het ophalen van een project-id](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |
   | [!UICONTROL **Opdrachtgever**] | De Opdrachtgever wordt door Adobe verstrekt. Klik op de knop [!UICONTROL **Kopiëren**] pictogram naast [!UICONTROL **Opdrachtgever**] om de inhoud van het veld te kopiëren en zorg er vervolgens voor dat u de Opdrachtgever toestemming geeft om bestanden te uploaden naar dit emmertje in Google Cloud Platform. <!-- add link to Google Cloud docs on how to do this --> |

   {style="table-layout:auto"}

+++

   +++Azure SAS

   Geef de volgende informatie op om een Azure SAS-account te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **URI sleutelvault**] | <p>Het pad naar het SAS-token in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-token opslaan als een geheim met Azure Key Vault. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nadat de sleutelvault-URI is gemaakt, voegt u een toegangsbeleid toe aan de Key Vault om toestemming te verlenen aan de Azure-toepassing die u hebt gemaakt. Zie voor meer informatie de [Microsoft Azure-documentatie over het toewijzen van een beleid voor toegang tot Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
   | [!UICONTROL **geheime naam sleutelvault**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure vindt u deze informatie in de Key Vault die u hebt gemaakt, op de **Key Vault** instellingenpagina&#39;s. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
   | [!UICONTROL **Locatierekeninggeheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). <!-- need to grant permission to the bucket. Jun will send info on where that is documented) --> |

   {style="table-layout:auto"}

+++

   +++Azure RBAC

   Geef de volgende informatie op om een Azure RBAC-account te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Locatierekeninggeheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

   {style="table-layout:auto"}

+++

   +++Snowflake

   Specificeer de volgende informatie om een rekening van de Snowflake te vormen:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Account-id**] | Identificeer uniek een rekening van de Snowflake binnen uw organisatie, evenals door het wereldwijde netwerk van Snowflake-gesteunde wolkenplatforms en wolkengebieden. <p>Zie de klasse [De pagina Account Identifiers in de documentatie van de Snowflake](https://docs.snowflake.com/en/user-guide/admin-account-identifier).</p> |
   | [!UICONTROL **Gebruiker**] | Hier geeft u de aanmeldingsnaam op van de gebruiker voor de verbinding. Dit is een gebruiker die specifiek voor Adobe zal worden gebruikt. U kunt de gebruiker in Snowflake tot stand brengen nadat het specificeren van de gebruikersbenaming hier. <p>Zie de klasse [Referentiepagina voor de parameter voor de JDBC-stuurprogramma-verbinding in de documentatie bij Snowflake](https://docs.snowflake.com/en/developer-guide/jdbc/jdbc-parameters).</p> |
   | [!UICONTROL **Rol**] | De standaardtoegangsbeheerrol die in de zitting van de Snowflake te gebruiken door de bestuurder in werking wordt gesteld. U zou een rol specifiek voor Adobe moeten tot stand brengen die gelezen en toegang heeft schrijven.<p>Zie de klasse [Referentiepagina voor de parameter voor de JDBC-stuurprogramma-verbinding in de documentatie bij Snowflake](https://docs.snowflake.com/en/developer-guide/jdbc/jdbc-parameters).</p> |
   | [!UICONTROL **Openbare sleutel**] | De openbare sleutel wordt verstrekt door Adobe. Selecteer het pictogram Kopiëren naast de knop [!UICONTROL **Openbare sleutel**] om de inhoud van het veld te kopiëren, gebruikt u vervolgens de openbare sleutel in uw account van de Snowflake. Zie de klasse [Verificatie van sleutelpaar en rotatie van sleutelpaar in de documentatie bij Snowflake](https://docs.snowflake.com/en/user-guide/key-pair-auth). |

+++

   +++Adobe Experience Platform

   Alle Adobe Experience Platform-klanten kunnen gegevens exporteren naar AEP Landing Zone.

   Geef de volgende informatie op om een Adobe Experience Platform-account te configureren.

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **IMS Org ID**] | De IMS Org-id wordt opgegeven door Adobe. Klik op het pictogram Kopiëren naast de knop [!UICONTROL **IMS Org ID**] om de inhoud van het veld te kopiëren, gebruikt u de id in uw account van het Platform voor Adobe. |

+++

1. Selecteren [!UICONTROL **Opslaan**].

1. Doorgaan met [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md).

