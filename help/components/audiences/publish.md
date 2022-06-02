---
title: Een publiek maken en publiceren naar het realtime profiel van de klant
description: Leer hoe u publiek kunt publiceren vanuit Customer Journey Analytics
source-git-commit: 7895342fb33118f0bbe97ce4a7adc22664adf000
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---


# Soorten publiek maken en publiceren

Dit onderwerp bespreekt hoe te om publiek te publiceren dat in Customer Journey Analytics (CJA) wordt ontdekt aan [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) in Adobe Experience Platform voor klantgerichtheid en personalisatie.

## publiek maken

1. U kunt op drie manieren een publiek maken:

   | Aanmaakmethode | Details |
   | --- | --- |
   | Van **[!UICONTROL Components]>[!UICONTROL Audiences]** | De pagina Soortbeheer wordt geopend. Klikken **[!UICONTROL Create audience]** en de [!UICONTROL Audience builder] wordt geopend. |
   | Vanuit een tabel voor vrije vorm | Klik met de rechtermuisknop op een item in een tabel voor vrije vorm en selecteer **[!UICONTROL Create an audience from selection]**. Met deze methode wordt het filter vooraf gevuld met de dimensie of het dimensie-item dat u in de tabel hebt geselecteerd. |
   | Via de interface voor het bewerken van filters | Schakel het selectievakje **[!UICONTROL Create an audience from this filter]**. Met deze methode wordt het filter vooraf gevuld. |

   {style=&quot;table-layout:auto&quot;}

1. Configureer het publiek.

   | Instelling | Beschrijving |
   | --- | --- |
   | [!UICONTROL Name] | De naam van het publiek. |
   | [!UICONTROL Tags] | Alle tags die u aan het publiek wilt toewijzen voor organisatorische doeleinden. U kunt een bestaande tag gebruiken of een nieuwe tag invoeren. |
   | [!UICONTROL Description] | Voeg een goede beschrijving van het publiek toe om het van anderen te onderscheiden. |
   | [!UICONTROL Refresh frequency] | De frequentie waarmee u het publiek wilt vernieuwen.<ul><li>U kunt kiezen om een eenmalig publiek te maken (standaard) dat niet hoeft te worden vernieuwd. Dit is bijvoorbeeld handig voor specifieke eenmalige campagnes.</li><li>U kunt andere vernieuwingsintervallen selecteren. Voor de frequentie van 4 uur, is er een grens van 150 publiek, aangezien dit vernieuwingstarief zeer verwerkingsintensief is. Voor andere interventies is er geen maximumaantal doelgroepen.</li></ul> |
   | Vervaldatum | Wanneer het publiek stopt met vernieuwen. De standaardwaarde is 1 jaar vanaf de aanmaakdatum. |
   | Zoekvenster vernieuwen | Hiermee geeft u aan hoe ver u wilt teruggaan in uw gegevensvenster om dit publiek te maken. De maximale waarde. is 90 dagen. Het uitbreiden van het publiek wordt op dezelfde manier behandeld als het verlopen van geplande rapporten - admin krijgt een e-mail een maand alvorens het programma verloopt. |
   | [!UICONTROL One-time date range] | Datumbereik wanneer u wilt dat het eenmalig publiek wordt gepubliceerd. |
   | [!UICONTROL Filter] | Filters zijn de belangrijkste invoer voor het publiek. U kunt maximaal 20 filters toevoegen. Deze filters kunnen worden aangesloten met `And` of `Or` operatoren. |

   {style=&quot;table-layout:auto&quot;}

1. De gegevensvoorvertoning interpreteren.

   De voorvertoning voor het publiek wordt weergegeven in de rechtertrack.

   | Voorvertoning instellen | Beschrijving |
   | --- | --- |
   | Venster Gegevensvoorbeeld | Het datumbereik voor het publiek. |
   | Totaal aantal mensen in het publiek | Een samenvattingsgetal dat kan oplopen tot 100 miljoen. |
   | Limiet voor doelgrootte | Toont hoe ver van de 100 miljoen grens dit publiek is. |
   | Geschatte resultaat voor publiek |  |
   | Geraamd op terugkeer | Een samenvattingsnummer... |
   | Metrische voorvertoningen |  |

   {style=&quot;table-layout:auto&quot;}


