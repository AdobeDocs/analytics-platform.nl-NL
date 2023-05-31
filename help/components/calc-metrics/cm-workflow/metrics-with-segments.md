---
description: Het filtreren op individuele metriek staat u toe om metrische vergelijkingen binnen het zelfde rapport te maken.
title: Gefilterde metriek
feature: Calculated Metrics
exl-id: 37cc93df-9f51-42b3-918f-ed5864991621
source-git-commit: 82ba31eec1455bf3d0c746cf5eebc81ce6162a00
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Gefilterde metriek

In de Berekende metrische bouwer, kunt u filters binnen uw metrische definitie toepassen. Dit is nuttig als u nieuwe metriek aan gebruik in uw analyse wilt afleiden. Houd in mening, kunnen de filterdefinities door de Bouwer van de Filter worden bijgewerkt. Als er wijzigingen worden aangebracht, wordt het filter automatisch bijgewerkt op de locatie waar het wordt toegepast, ook als het deel uitmaakt van een berekende definitie van metrische waarde.

![](assets/german-visitors.png)

## Een gefilterde metriek maken {#create}

Laten we zeggen dat u verschillende aspecten van een filter &quot;Duitse bezoekers&quot; wilt vergelijken met die van een filter &quot;Internationale Bezoekers&quot;. U kunt metriek tot stand brengen die u inzichten zoals zal geven:

* Hoe vergelijk het gedrag van bladeren door inhoud tussen de twee groepen? (Een ander voorbeeld is: Hoe vergelijk de omrekeningskoers tussen de twee filters?)
* Als percentage van het totale aantal personen, hoeveel Duitse personen op bepaalde pagina&#39;s surfen, tegenover internationale personen?
* Waar zijn de grootste verschillen in termen van welke inhoud door deze verschillende filters wordt betreden?

Bouw en bewaar metrisch genoemd &quot;Duitse Bezoekers&quot;en metrisch genoemd &quot;Internationale Bezoekers&quot;:

1. Maak een ad-hocfilter in de berekende metrische builder met de naam &quot;Duitse bezoekers&quot;, waarbij &quot;Landen&quot; gelijk is aan &quot;Duitsland&quot;. Sleep de dimensie Landen naar het canvas Definitie en selecteer [!UICONTROL **Duitsland**] als waarde:

   ![](assets/segment-from-dimension.png)

   >[!NOTE]
   >
   >U kunt dit ook doen in het dialoogvenster [Filter Builder](/help/components/filters/create-filters.md), maar we hebben de workflow vereenvoudigd door afmetingen beschikbaar te maken in de builder van het type Berekende metrische gegevens. &quot;Ad hoc&quot; betekent dat het filter niet zichtbaar is in de **[!UICONTROL Filters]** lijst in de linkerspoorstaaf. U kunt het echter openbaar maken door de muisaanwijzer boven het pictogram &quot;i&quot; naast het pictogram te plaatsen en op **[!UICONTROL Make public]**.

1. Sleep het filter Duitsland naar het canvas Definition en sleep de metrische waarde van de Unique Visitors erin:

   ![](assets/german-visitors.png)

1. Selecteren [!UICONTROL **Opslaan**] om berekende metrisch te bewaren.

1. Maak een ad-hocfilter in de builder van berekende metrische gegevens met de naam &quot;internationale bezoekers&quot;, waarbij &quot;Landen&quot; niet gelijk is aan &quot;Duitsland&quot;.

   Sleep de dimensie Landen naar het canvas Definitie en selecteer [!UICONTROL **Duitsland**] als waarde selecteert u vervolgens [!UICONTROL **is niet gelijk aan**] als de operator.

1. Sleep de metrische gegevens van de Unieke Bezoekers erin.

1. Selecteren [!UICONTROL **Opslaan**] om berekende metrisch te bewaren.

1. Sleep in Analysis Workspace de **[!UICONTROL Page]** Dimension in een lijst van de Vrije Vorm en sleep de 2 nieuwe berekende metriek naast elkaar aan de bovenkant:

   ![](assets/workspace-pages.png)

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12)

## Percentage van totale metriek {#percent-total}

U kunt het voorbeeld boven een stap verder zetten door uw filter te vergelijken met een totale populatie. Hiertoe maakt u twee nieuwe meeteenheden: &quot;% van de totale Duitse bezoekers&quot; en &quot;% van de totale internationale bezoekers&quot;:

1. Zet het filter Duitse (of internationale) bezoekers neer op het canvas.
1. Zet een ander Duits (of Internationaal) filter Bezoekers hieronder neer. Deze keer klikt u echter op het pictogram voor configuratie (versnelling) om het metrische type &quot;Totaal&quot; te selecteren. De notatie moet &#39;Percentage&#39; zijn. De exploitant zou &quot;gedeeld door&quot;moeten zijn. U eindigt omhoog met deze metrische definitie:

   ![](assets/cm_metric_total.png)

1. Pas deze metrisch op uw project toe:

   ![](assets/cm_percent_total.png)
