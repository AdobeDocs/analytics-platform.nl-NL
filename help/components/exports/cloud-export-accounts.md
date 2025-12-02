---
description: De exportaccount voor de cloud configureren waar Customer Journey Analytics-gegevens kunnen worden verzonden
keywords: Analysis Workspace
title: Cloudexportaccounts configureren
feature: Components
exl-id: 7c9d100f-0dbd-4dd2-b20b-d2ee117f1b7a
role: User, Admin
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '2230'
ht-degree: 0%

---

# Cloudexportaccounts configureren

Alvorens u de rapporten van Customer Journey Analytics naar een wolkenbestemming (of van Analysis Workspace, zoals die in [&#x200B; worden beschreven de rapporten van Customer Journey Analytics van de Uitvoer naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md) of van Report Builder, zoals die in [&#x200B; de rapporten van de Uitvoer van Report Builder &#x200B;](/help/report-builder/report-builder-export.md) worden beschreven) uitvoeren, moet u de bestemming toevoegen en vormen waar u de gegevens wilt worden verzonden.

Dit proces bestaat uit het toevoegen van en het vormen van de rekening (zoals Amazon S3, het Platform van de Wolk van Google, etc.) zoals die in dit artikel wordt beschreven, en dan het toevoegen van en het vormen van de plaats binnen die rekening (zoals een omslag binnen de rekening) zoals die in [&#x200B; wordt beschreven vormt wolkenuitvoerplaatsen &#x200B;](/help/components/exports/cloud-export-locations.md).

Voor informatie over hoe te om bestaande rekeningen, met inbegrip van het bekijken, het uitgeven, en het schrappen van rekeningen te beheren, zie [&#x200B; wolkenuitvoerplaatsen en rekeningen beheren &#x200B;](/help/components/exports/manage-export-locations.md).

## Beginnen met het maken van een cloud-exportaccount

1. Zorg ervoor u aan de [&#x200B; minimumvereisten &#x200B;](/help/analysis-workspace/export/export-cloud.md#minimum-requirements) voor het uitvoeren van rapporten aan de wolk voldoet.
1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.
1. Voor de [!UICONTROL Exports] pagina, selecteer de [!UICONTROL **rekeningen van de Plaats**] tabel.

   ![&#x200B; Uitvoer paginaopties die een andere rekening tonen &#x200B;](assets/account-add.png)

1. Selecteer [!UICONTROL **toevoegen rekening**].

   Het dialoogvenster Account toevoegen wordt weergegeven.

1. Op het [!UICONTROL **de rekeningsnaam van de Plaats**] gebied, specificeer een naam voor de plaatsrekening. Deze naam wordt weergegeven wanneer u een locatie maakt.

1. Op het [!UICONTROL **gebied van de de rekeningsbeschrijving van de Plaats 0&rbrace;, verstrek een korte beschrijving van de rekening helpen het van andere rekeningen van het zelfde rekeningtype onderscheiden.**]

1. Laat de optie toe om rekening [!UICONTROL **ter beschikking te stellen van alle gebruikers in uw organisatie**] als u andere gebruikers in uw organisatie wilt toestaan om de rekening te gebruiken.

   Houd rekening met het volgende wanneer u accounts deelt:

   * Accounts die u deelt, kunnen niet worden verwijderd.

   * Gedeelde accounts kunnen alleen door de eigenaar van de account worden bewerkt.

   * Iedereen kan een locatie voor de gedeelde account maken.

1. Op het [!UICONTROL **type van Rekening**] gebied, selecteer het type van wolkenrekening u naar uitvoert. Beschikbare accounttypen zijn Amazon S3 Role ARN, Google Cloud Platform, Azure SAS, Azure RBAC, Snowflake en AEP Data Landing Zone.

1. Ga met de sectie hieronder verder die aan het [!UICONTROL **type van Rekening**] beantwoordt u selecteerde.

   * [AEP Data Landing Zone](#aep-data-landing-zone)

   * [Amazon S3 Role ARN](#amazon-s3-role-arn)

   * [Google Cloud Platform](#google-cloud-platform)

   * [Azure SAS](#azure-sas)

   * [Azure RBAC](#azure-rbac)

   * [Snowflake](#snowflake)

### AEP Data Landing Zone

>[!IMPORTANT]
>
>Houd rekening met het volgende wanneer u AEP Data Landing Zone gebruikt voor uw exportaccount:
>
> * Wanneer u Customer Journey Analytics-rapporten exporteert naar Adobe Experience Platform Data Landing Zone, moet u de gegevens binnen 7 dagen downloaden en vervolgens verwijderen uit AEP Data Landing Zone. Na 7 dagen worden de gegevens automatisch verwijderd uit AEP Data Landing Zone.
> * AEP Data Landing Zone gebruikt Azure- of AWS-opslag. Als uw organisatie een aanmeldingsbedrijf gebruikt dat is geconfigureerd om Azure te gebruiken, gebruikt de AEP Data Landing Zone Azure. Als het login bedrijf wordt gevormd om AWS te gebruiken, dan gebruikt de Gebieden van de Gegevens van AEP AWS.
>

1. Ga op een van de volgende manieren te werk om een cloud-exportaccount te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een rekening van de wolkenuitvoer &#x200B;](#begin-creating-a-cloud-export-account)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. Nadat u **[!UICONTROL AEP Data Landing Zone]** op het **[!UICONTROL Account type]** gebied selecteert, uitgezocht [!UICONTROL **sparen**].

   Afhankelijk van of uw AEP Data Landing Zone is geconfigureerd voor gebruik van Azure- of AWS-opslag, worden de volgende dialoogvensters weergegeven:

   * **Azure opslag:**

     De [!UICONTROL **gecreeerde rekening van de Uitvoer**] dialoogvertoningen.

     ![&#x200B; de rekeningsdialoog van de Uitvoer AEP Gegevens Landing Zone &#x200B;](assets/export-account-aep.png)

   * **opslag van AWS:**

     >[!AVAILABILITY]
     >
     >Deze sectie is van toepassing op implementaties van Experience Platform die op Amazon Web Services (AWS) worden uitgevoerd. Experience Platform die op AWS wordt uitgevoerd, is momenteel beschikbaar voor een beperkt aantal klanten. Meer over de gesteunde infrastructuur van Experience Platform leren, zie het [&#x200B; multi-wolkenoverzicht van Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud).

     De [!UICONTROL **gecreeerde Rekening**] dialoogvertoningen.

     ![&#x200B; de rekeningsdialoog van de Uitvoer AEP Gegevens Landing Zone &#x200B;](assets/export-account-aep-aws.png)

1. (Voorwaardelijk) Als u Azure-opslag gebruikt:

   1. Kopieer de inhoud van het [!UICONTROL **SAS URI**] gebied aan uw klembord. U gebruikt deze SAS-URI om toegang te krijgen tot de gegevens die vanuit Analysis Workspace worden geëxporteerd vanuit de AEP Data Landing Zone.

      Als dit veld leeg is, moet u toestemming krijgen om toegang te krijgen tot Adobe Experience Platform.

   1. In Adobe Experience Platform configureert u de gegevenslandingszone-container zodanig dat de door u gekopieerde SAS-URI wordt gebruikt.

      >[!NOTE]
      >
      >Als u een AEP Data Landing Zone-account gebruikt die is gebaseerd op Azure, kunt u rapporten die u exporteert naar AEP Data Landing Zone het gemakkelijkst openen met de Azure Storage Explorer. In de volgende stappen wordt deze methode gebruikt.

      1. Als u niet reeds hebt, download [&#x200B; Microsoft Azure de Ontdekkingsreiziger van de Opslag &#x200B;](https://azure.microsoft.com/en-us/products/storage/storage-explorer/).

      1. In de documentatie van Adobe Experience Platform, volg de stappen die in [&#x200B; worden beschreven verbinden uw container van de Gebieden van Gegevens aan de Verkenner van de Opslag Azure &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html#connect-your-data-landing-zone-container-to-azure-storage-explorer).

         U kunt de taken overslaan die in de secties [&#x200B; worden beschreven terugwinnen de geloofsbrieven voor uw Gegevens het Landing Zone &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html#retrieve-dlz-credentials) en [&#x200B; Gegevens het Landing van de Zone van de Update geloofsbrieven &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html#update-dlz-credentials), omdat URI die u kopieerde deze geloofsbrieven bevat.

      1. Wanneer het volgen van de documentatie van Adobe Experience Platform en u aan het [!UICONTROL **de containerSAS URL van de Blob**] gebied komt, kleef SAS URI die u in Stap 3 kopieerde.

         >[!NOTE]
         >
         >U moet deze actie om de 7 dagen uitvoeren, omdat de SAS URI 7 dagen na het creëren vervalt. U kunt een script maken om dit proces te automatiseren.

         ![&#x200B; ga het venster van Info van de Verbinding die het gebied van SAS URL tonen &#x200B;](assets/blob-container-sas-uri.png)

   1. Selecteer [!UICONTROL **daarna**] > [!UICONTROL **verbinden**].

   1. In Customer Journey Analytics, in de [!UICONTROL **gecreeerde rekening van de Uitvoer**] dialoog, uitgezochte [!UICONTROL **O.K.**].

      ![&#x200B; de rekeningsdialoog van de Uitvoer AEP Gegevens Landing Zone &#x200B;](assets/export-account-aep.png)

1. (Voorwaardelijk) Als u AWS-opslag gebruikt:

   1. Kopieer de inhoud van de volgende velden naar het klembord (u gebruikt deze informatie om toegang te krijgen tot de gegevens die vanuit Analysis Workspace worden geëxporteerd vanuit de AEP Data Landing Zone):

      * [!UICONTROL **Sleutelidentiteitskaart van de Toegang**]

      * **[!UICONTROL Secret access key]**

      * **[!UICONTROL Session token]**

      * **[!UICONTROL Bucket name]**

      * **[!UICONTROL DLZ folder]**

      ![&#x200B; de rekeningsdialoog van de Uitvoer AEP Gegevens Landing Zone &#x200B;](assets/export-account-aep-aws.png)

   1. Selecteer [!UICONTROL **O.K.**].

1. Ga met [&#x200B; verder vormen de plaatsen van de wolkenuitvoer &#x200B;](/help/components/exports/cloud-export-locations.md).

### Amazon S3 Role ARN

1. Ga op een van de volgende manieren te werk om een cloud-exportaccount te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een rekening van de wolkenuitvoer &#x200B;](#begin-creating-a-cloud-export-account)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **eigenschappen van de Rekening**] sectie van [!UICONTROL **voeg rekening**] dialoogdoos toe, specificeer de volgende informatie:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **ARN van de Rol**] | U moet een Role ARN (de Naam van het Middel van Amazon) verstrekken die Adobe kan gebruiken om tot de rekening van Amazon S3 toegang te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Voor specifieke informatie, zie [&#x200B; deze documentatie van AWS &#x200B;](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   De [!UICONTROL **gecreeerde rekening van de Uitvoer**] dialoogvertoningen.

   ![&#x200B; de rekening van de Uitvoer creeerde dialoog Amazon S3 Rol ARN &#x200B;](assets/export-account-amazons3.png)

1. Kopieer de inhoud van het [!UICONTROL **ARN van de Gebruiker**] gebied aan uw klembord. De User ARN (Amazon Resource Name) wordt opgegeven door Adobe. U moet deze gebruiker aan het beleid vastmaken u in Amazon S3 RolARN creeerde.

1. Selecteer [!UICONTROL **O.K.**].

1. Ga met [&#x200B; verder vormen de plaatsen van de wolkenuitvoer &#x200B;](/help/components/exports/cloud-export-locations.md).

### Google Cloud Platform

1. Ga op een van de volgende manieren te werk om een cloud-exportaccount te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een rekening van de wolkenuitvoer &#x200B;](#begin-creating-a-cloud-export-account)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **eigenschappen van de Rekening**] sectie van [!UICONTROL **voeg rekening**] dialoogdoos toe, specificeer de volgende informatie:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **identiteitskaart van het Project**] | Uw Google Cloud-project-id die u kopieert van uw Google Cloud-account. Zie de [&#x200B; documentatie van de Wolk van Google over het krijgen van een project identiteitskaart &#x200B;](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   De [!UICONTROL **gecreeerde rekening van de Uitvoer**] dialoogvertoningen.

   ![&#x200B; gecreeerde de rekening van de Uitvoer dialoog &#x200B;](assets/export-account-gcp.png)

1. Kopieer de inhoud van het [!UICONTROL **Belangrijkste**] gebied aan uw klembord, dan zorg ervoor dat u toestemming aan Principal verleent om dossiers aan dit emmertje in het Platform van de Wolk van Google te uploaden. <!-- add link to Google Cloud docs on how to do this -->

1. Selecteer [!UICONTROL **O.K.**].

1. Ga met [&#x200B; verder vormen de plaatsen van de wolkenuitvoer &#x200B;](/help/components/exports/cloud-export-locations.md).

### Azure SAS

1. Ga op een van de volgende manieren te werk om een cloud-exportaccount te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een rekening van de wolkenuitvoer &#x200B;](#begin-creating-a-cloud-export-account)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **eigenschappen van de Rekening**] sectie van [!UICONTROL **voeg rekening**] dialoogdoos toe, specificeer de volgende informatie:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **identiteitskaart van de Toepassing**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [&#x200B; Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft &#x200B;](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
   | [!UICONTROL **identiteitskaart van de HTENT**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [&#x200B; Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft &#x200B;](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
   | [!UICONTROL **Zeer belangrijke vault URI**] | <p>Het pad naar de SAS URI in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-URI opslaan als een geheim met Azure Key Vault. Voor informatie, zie de [&#x200B; Microsoft Azure documentatie over hoe te om een geheim van Azure Key Vault &#x200B;](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations) te plaatsen en terug te winnen.</p><p>Nadat de sleutelvault-URI is gemaakt:<ul><li>Voeg een toegangsbeleid op de Zeer belangrijke vault toe om toestemming aan de Azure toepassing te verlenen die u creeerde.<p><p>Voor informatie, zie [&#x200B; Microsoft Azure documentatie over hoe te om een Zeer belangrijk de toegangsbeleid van de Vault toe te wijzen &#x200B;](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p>of</p><p>Als u een toegangsrol direct wilt verlenen zonder een toegangsbeleid te creëren, zie [&#x200B; Microsoft Azure documentatie over hoe te om Azure rollen toe te wijzen gebruikend Azure portaal &#x200B;](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal). Hiermee voegt u de roltoewijzing voor de toepassings-id toe aan toegang tot de sleutelvault-URI. </p></li><li>Zorg ervoor dat de toepassings-id de `Key Vault Certificate User` ingebouwde rol heeft gekregen om toegang te krijgen tot de sleutelvault URI.</br><p>Voor meer informatie, zie [&#x200B; Azure ingebouwde rollen &#x200B;](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p></li></ul> |
   | [!UICONTROL **Zeer belangrijke geheime naam van de kluis**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure, wordt deze informatie gevestigd in de Belangrijkste Vault u, op de **Zeer belangrijke de montagespagina&#39;s van de Uitvault** creeerde. Voor informatie, zie de [&#x200B; Microsoft Azure documentatie over hoe te om een geheim van Azure Key Vault &#x200B;](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations) te plaatsen en terug te winnen. |
   | [!UICONTROL **het rekeningsgeheim van de Plaats**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Certificaten &amp; geheimen** lusje binnen uw toepassing. Voor meer informatie, zie [&#x200B; Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft &#x200B;](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. <!-- need to grant permission to the bucket. Jun will send info on where that is documented) --> |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   De [!UICONTROL **gecreeerde rekening van de Uitvoer**] dialoogvertoningen.

   ![&#x200B; gecreeerde de rekening van de Uitvoer dialoog &#x200B;](assets/export-account-azure.png)

1. Als u dat nog niet hebt gedaan, moet u ervoor zorgen dat u rechten toekent aan het emmertje in Azure SAS. <!-- add link to Google Cloud docs on how to do this -->

1. Selecteer [!UICONTROL **O.K.**].

1. Ga met [&#x200B; verder vormen de plaatsen van de wolkenuitvoer &#x200B;](/help/components/exports/cloud-export-locations.md).

### Azure RBAC

1. Ga op een van de volgende manieren te werk om een cloud-exportaccount te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een rekening van de wolkenuitvoer &#x200B;](#begin-creating-a-cloud-export-account)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **eigenschappen van de Rekening**] sectie van [!UICONTROL **voeg rekening**] dialoogdoos toe, specificeer de volgende informatie:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **identiteitskaart van de Toepassing**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [&#x200B; Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft &#x200B;](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
   | [!UICONTROL **identiteitskaart van de HTENT**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [&#x200B; Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft &#x200B;](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
   | [!UICONTROL **het rekeningsgeheim van de Plaats**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Certificaten &amp; geheimen** lusje binnen uw toepassing. Voor meer informatie, zie [&#x200B; Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft &#x200B;](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   De [!UICONTROL **gecreeerde rekening van de Uitvoer**] dialoogvertoningen.

   ![&#x200B; gecreeerde de rekening van de Uitvoer dialoog &#x200B;](assets/export-account-azure.png)

1. Als u nog geen machtigingen hebt, controleert u of u machtigingen hebt verleend aan het emmertje in Azure RBAC. <!-- add link to Google Cloud docs on how to do this -->

1. Selecteer [!UICONTROL **O.K.**].

1. Ga met [&#x200B; verder vormen de plaatsen van de wolkenuitvoer &#x200B;](/help/components/exports/cloud-export-locations.md).

### Snowflake

1. Ga op een van de volgende manieren te werk om een cloud-exportaccount te maken:

   * Van de pagina van Uitvoer zoals hierboven beschreven, in [&#x200B; beginnen creërend een rekening van de wolkenuitvoer &#x200B;](#begin-creating-a-cloud-export-account)

   * Wanneer [&#x200B; het uitvoeren van volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace)

1. In de [!UICONTROL **eigenschappen van de Rekening**] sectie van [!UICONTROL **voeg rekening**] dialoogdoos toe, specificeer de volgende informatie:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **identiteitskaart van de Rekening**] | Uniquely identificeert een Snowflake-account binnen uw organisatie, maar ook in het wereldwijde netwerk van door Snowflake ondersteunde cloudplatforms en -regio&#39;s. <p>U moet de account-id ophalen van uw Snowflake-account en de gegevens hier plakken.</p><p>Om te leren waar te om deze informatie te krijgen, zie de [&#x200B; pagina van de Identificatienummers van de Rekening in de documentatie van Snowflake &#x200B;](https://docs.snowflake.com/en/user-guide/admin-account-identifier).</p> |
   | [!UICONTROL **Gebruiker**] | De aanmeldnaam van de gebruiker die wordt gebruikt voor de verbinding. We raden u aan een nieuwe gebruiker te maken die specifiek voor Adobe wordt gebruikt. Geef hier de naam op en maak vervolgens in Snowflake een gebruiker met dezelfde naam. U kunt in Snowflake een gebruiker maken met de opdracht `CREATE USER` .  <p>Voor meer informatie, zie de [&#x200B; Gebruiker, Rol, &amp; Bevelen van de Voorrechten &#x200B;](https://docs.snowflake.com/en/sql-reference/commands-user-role).</p> |
   | [!UICONTROL **Rol**] | De rol die aan de gebruiker zal worden toegewezen. We raden u aan een nieuwe rol te creëren die specifiek voor Adobe zal worden gebruikt. Geef hier de rol op en maak vervolgens een rol in Snowflake met dezelfde naam en geef de rol aan de gebruiker. U kunt een rol in Snowflake maken met de opdracht `CREATE ROLE` . <p>Voor meer informatie, zie de [&#x200B; Gebruiker, Rol, &amp; Bevelen van de Voorrechten &#x200B;](https://docs.snowflake.com/en/sql-reference/commands-user-role).</p> |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   De [!UICONTROL **gecreeerde rekening van de Uitvoer**] dialoogvertoningen.

   ![&#x200B; gecreeerde de rekening van de Uitvoer dialoog &#x200B;](assets/export-account-snowflake.png)

1. Kopieer de inhoud van het [!UICONTROL **Openbare zeer belangrijke**] gebied aan uw klembord. De openbare sleutel wordt geleverd door Adobe.

   Gebruik de openbare sleutel in Snowflake om verbinding te maken met uw Snowflake-account. U moet de gebruiker associëren die u met deze openbare sleutel creeerde.

   Geef bijvoorbeeld in Snowflake de volgende opdracht op:

   ```
   CREATE USER <your_adobe_user> RSA_PUBLIC_KEY = '<your_public_key>';
   ```

   Voor meer informatie, zie de [&#x200B; Zeer belangrijke pagina van de Authentificatie van het Paar &amp; van de Omwenteling van het Zeer belangrijke Paar in de documentatie van Snowflake &#x200B;](https://docs.snowflake.com/en/user-guide/key-pair-auth).

1. Selecteer [!UICONTROL **O.K.**].

1. Ga met [&#x200B; verder vormen de plaatsen van de wolkenuitvoer &#x200B;](/help/components/exports/cloud-export-locations.md).
