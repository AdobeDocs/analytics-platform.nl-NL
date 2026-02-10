---
title: Analyse publiek configureren
description: Leer hoe te om publieksanalyse te vormen
solution: Customer Journey Analytics
feature: Audiences
role: Admin
exl-id: 0db3f6f7-9d7e-41bf-8eb5-02e439bab10a
source-git-commit: 4f1299595077a1756a6ad0c4f5ef5e0247ab4973
workflow-type: tm+mt
source-wordcount: '1294'
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
>abstract="Schakel deze optie in als u wilt dat Customer Journey Analytics de identiteit vindt in de identiteitskaart die is gemarkeerd met een kenmerk primary=true en gebruik die identiteit vervolgens als Persoon-id voor die rij. Deze identiteit is de primaire sleutel die in Experience Platform voor het verdelen wordt gebruikt. <br/> als u deze optie gehandicapt verlaat, selecteer een namespace van het de naamruimtegebied van de Identiteit hieronder. Customer Journey Analytics zoekt elke rij&#39;s Identiteitskaart naar deze namespace sleutel en gebruikt de identiteit onder die namespace als Persoon identiteitskaart voor die rij."

<!-- markdownlint-enable MD034 -->

De analyse van het publiek staat u toe om de gegevens van het publiekslidmaatschap van de Gegevensreeksen van het Profiel van Experience Platform in een verbinding van Customer Journey Analytics in te voeren. Soorten publiek wordt beschikbaar als nieuwe afmetingen voor gebruik in Analysis Workspace. Voor meer gedetailleerde overzichtsinformatie over publieksanalyse, zie [&#x200B; overzicht van de analyse van het publiek &#x200B;](/help/connections/audience-analysis/audience-analysis-overview.md).

>[!IMPORTANT]
>
>De gegevens van het publiek worden elke nacht opnieuw verwerkt en gegenereerd, waardoor de gegevens van het publiek alleen voor de vorige dag (&quot;gisteren&quot;) nauwkeurig zijn.
>
>Het publiek is beschikbaar in de gegevensmeningen van Customer Journey Analytics op de dag nadat u de configuratie van de publieksanalyse creeert.

## Een configuratie voor een publieksanalyse maken

Wanneer u een configuratie voor publieksanalyse maakt, selecteert u de sandbox en voegt u het beleid samen dat is gekoppeld aan het Experience Platform-publiek dat u wilt analyseren. Customer Journey Analytics leidt tot een nieuwe raadplegingsdataset, dan voegt automatisch de raadplegingsdataset en de profieldataset aan de verbinding toe u kiest.

Alleen systeembeheerders kunnen configuraties voor publieksanalyse maken.

Om een configuratie van de publieksanalyse tot stand te brengen:

1. Selecteer in Customer Journey Analytics **[!UICONTROL Data Management]** > **[!UICONTROL Audience analysis configuration]** .

   ![&#x200B; de hoofdpagina van de de analyseanalyse van het publiek &#x200B;](assets/audience-analysis-empty.png)

1. Selecteer **[!UICONTROL Create configuration]**.

   ![&#x200B; creeer de configuratie van de publieksanalyse &#x200B;](assets/audience-analysis-create.png)

1. Geef in de sectie **[!UICONTROL Details]** de volgende informatie op:

   | Veld | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Name]** | Geef een naam voor de configuratie op. |
   | **[!UICONTROL Sandbox]** | Selecteer de Experience Platform-sandbox die de profielgegevensset bevat die u aan de verbinding wilt toevoegen. Eén sandbox biedt ondersteuning voor maximaal 100 configuraties voor publieksanalyse. <p>Adobe Experience Platform verstrekt [&#x200B; zandbakken &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) die één enkele instantie van het Platform in afzonderlijke virtuele milieu&#39;s verdelen helpen digitale ervaringstoepassingen ontwikkelen en evolueren. U kunt sandboxen zien als &#39;gegevenssilo&#39;s&#39; die gegevenssets bevatten. Sandboxen worden gebruikt om toegang tot datasets te controleren.</p> |

1. Geef in de sectie **[!UICONTROL Profile dataset]** de volgende informatie op:

   | Veld | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Merge policy]** | Selecteer het samenvoegbeleid dat aan de profieldataset beantwoordt die u voor publieksanalyse wilt gebruiken. <p>Het Beleid van de fusie bepaalt hoe Adobe Experience Platform profielgegevens van veelvoudige datasets in verenigde klantenprofielen combineert die voor publieksverwezenlijking worden gebruikt. Het samenvoegbeleid dat u selecteert, bepaalt welke profielkenmerken worden opgenomen in uw publiek. Elke dag wordt een momentopname van deze gegevens gegenereerd in Experience Platform. Deze momentopname biedt een statische weergave van de gegevens op een bepaald tijdstip en bevat geen gebeurtenisgegevens.</p><p>Selecteer het **[!UICONTROL Default Timebased]** samenvoegbeleid als er meerdere samenvoegbeleidsregels worden weergegeven en u niet zeker weet welke beleid u wilt kiezen. U kunt uw gegevensteam ook raadplegen om beter te begrijpen welk publiek met elk fusiebeleid wordt geassocieerd.</p> |
   | **[!UICONTROL Profile dataset]** | De profieldataset die met het samenvoegbeleid wordt geassocieerd u selecteerde. Deze profielgegevensset bevat de Experience Platform-publieksgegevens die u wilt analyseren. Deze profieldataset wordt toegevoegd aan de verbinding die u selecteert.<p>Nadat u een samenvoegbeleid hebt gekozen, wordt het exporteren van de profielmomentopname weergegeven. Bijvoorbeeld: `Profile-Snapshot-Export-abbc7093-80f4-4b49-b96e-e743397d763f` .</p><p>Voor meer informatie, zie {de attributendatasets van het 0} Profiel [&#x200B; in de Gids van de Dashboards van Experience Platform.](https://experienceleague.adobe.com/en/docs/experience-platform/dashboards/query#profile-attribute-datasets)</p> |

1. Klik in de sectie **[!UICONTROL Connection]** op **[!UICONTROL Select a connection]** .

1. Selecteer in het dialoogvenster Verbindingen het selectievakje naast de verbinding waar u de profielgegevensset wilt toevoegen en selecteer vervolgens **[!UICONTROL Use connection]** .

   Een verbinding kan met slechts één configuratie van de publieksanalyse worden geassocieerd.

1. Geef de volgende informatie op om de verbinding te configureren:

   | Veld | Beschrijving |
   |---------|----------|
   | **[!UICONTROL Person ID]** | Selecteer een veld in het schema dat de persoon-id vertegenwoordigt.<p>De selectie is beperkt tot de lijst met velden in het schema die zijn gemarkeerd als Identiteit en die wel een naamruimte voor identiteit hebben. **[!UICONTROL IdentityMap]** is standaard geselecteerd en is geschikt voor de meeste configuraties. </p><p>Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer personen-id&#39;s niet zijn gedefinieerd in het schema. Zie [&#x200B; identiteitsgebieden in UI &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie bepalen.</p> |
   | **[!UICONTROL Use primary identity namespace]** | Deze optie geeft aan of u **[!UICONTROL Identity Map]** selecteert voor de persoon-id. <p>Schakel deze optie in als u wilt dat Customer Journey Analytics de identiteit vindt in de identiteitskaart die is gemarkeerd met een kenmerk primary=true en gebruik die identiteit vervolgens als Persoon-id voor die rij. Deze identiteit is de primaire sleutel die in Experience Platform voor het verdelen wordt gebruikt. En deze identiteit is ook de belangrijkste kandidaat voor gebruik als identiteitskaart van de Persoon van Customer Journey Analytics (afhankelijk van hoe de dataset in een verbinding van Customer Journey Analytics wordt gevormd).</p> |
   | **[!UICONTROL Identity namespace]** | Deze optie geeft aan of u **[!UICONTROL Identity Map]** selecteert voor de persoon-id. Deze optie is uitgeschakeld als u de primaire-id-naamruimte gebruikt. <p>Identiteitsnaamruimten zijn een component van de [&#x200B; Dienst van de Identiteit van Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces). Naamruimten dienen als indicatoren voor de context waarop een identiteit betrekking heeft. Als u een naamruimte opgeeft, zoekt Customer Journey Analytics in elke rij naar Identiteitskaart voor deze naamruimtesleutel en wordt de identiteit onder die naamruimte gebruikt als Persoon-id voor die rij. Aangezien Customer Journey Analytics niet alle rijen volledig kan scannen op gegevenssets om te bepalen welke naamruimten aanwezig zijn, worden alle mogelijke naamruimten weergegeven in het keuzemenu. U moet weten welke naamruimten in de gegevens zijn opgegeven. Deze naamruimten worden niet automatisch gedetecteerd.</p> |

   <!-- Add this when B2B releases for AuA **[!UICONTROL Account ID]** [!BADGE B2B Edition]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B Edition"}|  (only displayed for account-based connections) The Account ID that is used to support account-based reporting for the dataset. -->

1. Klik in de sectie **[!UICONTROL Data views]** op **[!UICONTROL Select data views]** .

1. Schakel in het dialoogvenster Gegevens het selectievakje in naast een of meer gegevensweergaven die u wilt gebruiken voor het analyseren van Experience Platform-publieksgegevens in Analysis Workspace. Deze gegevensweergaven worden automatisch geconfigureerd met Experience Platform-publieksgegevens voor rapportage.

1. Selecteer **[!UICONTROL Use data views]**.

1. Selecteer **[!UICONTROL Create]** om de configuratie te maken.

   >[!IMPORTANT]
   >
   >Omdat de profieldataset één keer per dag wordt bijgewerkt, zijn het publiek beschikbaar in de gegevensmeningen van Customer Journey Analytics op de dag nadat u de configuratie van de publieksanalyse creeert.


1. Na 24 uren, {de afmetingen van het 0} meningspubliek in de gegevensmening [&#x200B; om te verifiëren dat de publieksafmetingen in de gegevensmeningen beschikbaar zijn die u selecteerde.](#view-audience-dimensions-in-the-data-view)

## De afmetingen van het publiek weergeven in de gegevensweergave

Nadat u [&#x200B; creeert een configuratie van de publieksanalyse &#x200B;](#create-an-audience-analysis-configuration), kunt u verifiëren dat de publieksafmetingen aan de gegevensmeningen werden toegevoegd die u tijdens de configuratie selecteerde.

Als u de afmetingen van het publiek in de gegevensweergave wilt weergeven, moet u een beheerder van het productprofiel zijn voor het productprofiel waaraan de gegevensweergave is toegewezen. Voor meer informatie, zie [&#x200B; controle van de Toegang &#x200B;](/help/technotes/access-control.md).

U kunt als volgt de afmetingen van de publieksanalyse weergeven in de gegevensweergave:

1. Selecteer in Customer Journey Analytics **[!UICONTROL Data Management]** > **[!UICONTROL Data views]** .

1. In de sectie **[!UICONTROL Dimensions]** moeten nu de volgende afmetingen beschikbaar zijn:

   * **[!UICONTROL Audience Name]**

   * **[!UICONTROL Audience Origin]**

   * **[!UICONTROL Exited Audience Origin]**

   * **[!UICONTROL Exited Audience Name]**

   Merk op dat elk van deze dimensies aan de profieldataset werd toegevoegd die met het fusiebeleid wordt geassocieerd dat u tijdens de configuratie van de publieksanalyse selecteerde, en elk werd toegevoegd aan de nieuwe raadplegingsdataset die werd gecreeerd.

   {de afmetingen van het 0} publiek beschikbaar in de gegevensmening ![](assets/audience-analysis-dataview-dataset.png)

1. Gebruik de analysen voor het publiek in Analysis Workspace.

   Gebruikers die toegang hebben tot de gegevensweergave in Analysis Workspace, kunnen nu de nieuwe afmetingen zien en deze gebruiken in hun analyses. Voor informatie over hoe te om de dimensies van de publieksanalyse in Analysis Workspace te gebruiken, zie [&#x200B; het publiek van Experience Platform in Customer Journey Analytics &#x200B;](/help/connections/audience-analysis/analyze-audiences.md) analyseren.
