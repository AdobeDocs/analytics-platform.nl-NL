---
title: publieksanalyse configureren
description: Leer hoe te om publieksanalyse te vormen
solution: Customer Journey Analytics
feature: Audiences
role: Admin
hide: true
hidefromtoc: true
source-git-commit: 3f4b9e5929f1fe5bf0524236ab956487469c1778
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---

# publieksanalyse configureren {#configure-audience-analysis}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-audience-analysis-merge-policy"
>title="Samenvoegbeleid"
>abstract="Het beleid van de fusie combineert profielgegevens van veelvoudige datasets in verenigde klantenprofielen die voor publieksverwezenlijking worden gebruikt. Selecteer Standaardtijdbasis als er meerdere samenvoegbeleidsregels worden weergegeven en u niet zeker weet welke procedure u moet kiezen. Of raadpleeg uw gegevensteam om te leren welk publiek met elk fusiebeleid wordt geassocieerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-audience-analysis-sandbox"
>title="Sandbox"
>abstract="Selecteer de sandbox die de juiste Experience Platform-profielgegevenssets bevat. Deze datasets moeten de publieksgegevens bevatten die u in Analysis Workspace wilt melden. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-audience-person-id"
>title="Persoon-id"
>abstract="Selecteer een veld in het schema dat de persoon-id vertegenwoordigt. De selectie is beperkt tot de lijst met velden in het schema die zijn gemarkeerd als Identiteit en die een naamruimte voor identiteit hebben."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-audience-namespace"
>title="Primaire naamruimte gebruiken"
>abstract="Schakel deze optie in als u wilt dat Customer Journey Analytics de identiteit vindt in de identiteitskaart die is gemarkeerd met een kenmerk primary=true en die identiteit gebruikt als Persoon-id voor die rij. Deze identiteit is de primaire sleutel die in Experience Platform voor het verdelen wordt gebruikt. <br/> als u deze optie gehandicapt verlaat, selecteer een namespace van het de naamruimtegebied van de Identiteit hieronder. Customer Journey Analytics zoekt elke rij&#39;s Identiteitskaart naar deze namespace sleutel en gebruikt de identiteit onder die namespace als Persoon identiteitskaart voor die rij."

<!-- markdownlint-enable MD034 -->

De analyse van het publiek staat u toe om de gegevens van het publiekslidmaatschap van de Gegevensreeksen van het Profiel van Experience Platform in een verbinding van Customer Journey Analytics in te voeren. Soorten publiek wordt beschikbaar als nieuwe afmetingen voor gebruik in Analysis Workspace. Voor meer gedetailleerde overzichtsinformatie over publieksanalyse, zie [&#x200B; overzicht van de analyse van het publiek &#x200B;](/help/connections/audience-analysis/audience-analysis-overview.md).

Wanneer u een configuratie voor publieksanalyse maakt, selecteert u de sandbox en voegt u het beleid samen dat is gekoppeld aan het Experience Platform-publiek dat u wilt analyseren. Customer Journey Analytics leidt tot een nieuwe raadplegingsdataset, dan voegt automatisch de raadplegingsdataset en de profieldataset aan de verbinding toe u kiest.

Om een configuratie van de publieksanalyse tot stand te brengen:

1. Selecteer in Customer Journey Analytics **[!UICONTROL Data Management]** > **[!UICONTROL Audience analysis configuration]** .

   ![&#x200B; de hoofdpagina van de de analyseanalyse van het publiek &#x200B;](assets/audience-analysis-empty.png)

1. Selecteer **[!UICONTROL Create configuration]**.

   ![&#x200B; creeer de configuratie van de publieksanalyse &#x200B;](assets/audience-analysis-create.png)

1. Geef in de sectie **[!UICONTROL Details]** de volgende informatie op:

   | Veld | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Name]** | Geef een naam voor de configuratie op. |
   | **[!UICONTROL Sandbox]** | Selecteer de zandbak die de profieldataset bevat die u aan uw verbinding wilt toevoegen. <p>Adobe Experience Platform verstrekt [&#x200B; zandbakken &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) die één enkele instantie van het Platform in afzonderlijke virtuele milieu&#39;s verdelen helpen digitale ervaringstoepassingen ontwikkelen en evolueren. U kunt sandboxen zien als &#39;gegevenssilo&#39;s&#39; die gegevenssets bevatten. Sandboxen worden gebruikt om toegang tot datasets te controleren.</p> |

1. Geef in de sectie **[!UICONTROL Profile dataset]** de volgende informatie op:

   | Veld | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Merge policy]** | Selecteer het samenvoegbeleid dat aan de profieldataset beantwoordt die u voor publieksanalyse wilt gebruiken. <p>Het Beleid van de fusie bepaalt hoe Adobe Experience Platform profielgegevens van veelvoudige datasets in verenigde klantenprofielen combineert die voor publieksverwezenlijking worden gebruikt. Het samenvoegbeleid dat u selecteert, bepaalt welke profielkenmerken worden opgenomen in uw publiek. Elke dag wordt een momentopname van deze gegevens gegenereerd in Experience Platform. Deze momentopname biedt een statische weergave van de gegevens op een bepaald tijdstip en bevat geen gebeurtenisgegevens.</p><p>Selecteer het **[!UICONTROL Default Timebased]** samenvoegbeleid als er meerdere samenvoegbeleidsregels worden weergegeven en u niet zeker weet welke beleid u wilt kiezen. U kunt uw gegevensteam ook raadplegen om beter te begrijpen welk publiek met elk fusiebeleid wordt geassocieerd.</p> |
   | **[!UICONTROL Profile dataset]** | De profieldataset die met het samenvoegbeleid wordt geassocieerd u selecteerde. Deze profielgegevensset bevat de Experience Platform-publieksgegevens die u wilt analyseren. Deze profieldataset wordt toegevoegd aan de verbinding die u selecteert.<p>Nadat u een samenvoegbeleid hebt gekozen, wordt het exporteren van de profielmomentopname weergegeven. Bijvoorbeeld: `Profile-Snapshot-Export-abbc7093-80f4-4b49-b96e-e743397d763f` .</p><p>Voor meer informatie, zie [&#x200B; de attributendatasets van het Profiel &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/dashboards/query#profile-attribute-datasets) in de Gids van de Dashboards van Experience Platform.</p> |

1. Klik in de sectie **[!UICONTROL Connection]** op **[!UICONTROL Select a connection]** .

1. Selecteer in het dialoogvenster Verbindingen het selectievakje naast de verbinding waar u de profielgegevensset wilt toevoegen en selecteer vervolgens **[!UICONTROL Use connection]** .

1. Geef de volgende informatie op om de verbinding te configureren:

   | Veld | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Person ID]** | Selecteer een veld in het schema dat de persoon-id vertegenwoordigt. De selectie is beperkt tot de lijst met velden in het schema die zijn gemarkeerd als Identiteit en die wel een naamruimte voor identiteit hebben.<p>Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer personen-id&#39;s niet zijn gedefinieerd in het schema. Zie [&#x200B; identiteitsgebieden in UI &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie bepalen.</p> |
   | **[!UICONTROL Use primary identity namespace]** | Deze optie geeft aan of u **[!UICONTROL Identity Map]** selecteert voor de persoon-id.<p>Schakel deze optie in als u wilt dat Customer Journey Analytics de identiteit vindt in de identiteitskaart die is gemarkeerd met een kenmerk primary=true en die identiteit gebruikt als Persoon-id voor die rij. Deze identiteit is de primaire sleutel die in Experience Platform voor het verdelen wordt gebruikt. En deze identiteit is ook de belangrijkste kandidaat voor gebruik als identiteitskaart van de Persoon van Customer Journey Analytics (afhankelijk van hoe de dataset in een verbinding van Customer Journey Analytics wordt gevormd).</p> |
   | **[!UICONTROL Identity namespace]** | Deze optie geeft aan of u **[!UICONTROL Identity Map]** selecteert voor de persoon-id. Deze optie is uitgeschakeld als u de primaire-id-naamruimte gebruikt. <p>Identiteitsnaamruimten zijn een component van de [&#x200B; Dienst van de Identiteit van Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces). Naamruimten dienen als indicatoren voor de context waarop een identiteit betrekking heeft. Als u een naamruimte opgeeft, zoekt Customer Journey Analytics in elke rij naar Identiteitskaart voor deze naamruimtesleutel en wordt de identiteit onder die naamruimte gebruikt als Persoon-id voor die rij. Aangezien Customer Journey Analytics niet alle rijen volledig kan aftasten dataset om te bepalen welke namespaces aanwezig zijn, worden alle mogelijke namespaces getoond in het drop-down menu. Weet welke naamruimten in de gegevens zijn opgegeven; deze naamruimten worden niet automatisch gedetecteerd.</p> |

1. Klik in de sectie **[!UICONTROL Data views]** op **[!UICONTROL Select data views]** .

1. Schakel in het dialoogvenster Gegevens het selectievakje in naast een of meer gegevensweergaven die u wilt gebruiken voor het analyseren van Experience Platform-publieksgegevens in Analysis Workspace. Deze gegevensweergaven worden automatisch geconfigureerd met Experience Platform-publieksgegevens voor rapportage.

1. Selecteer **[!UICONTROL Use data views]**.

1. Selecteer **[!UICONTROL Create]** om de configuratie te maken.

   Omdat de profieldataset één keer per dag wordt bijgewerkt, zijn het publiek beschikbaar in de gegevensmeningen van Customer Journey Analytics op de dag nadat u de configuratie van de publieksanalyse creeert.


