---
title: Een afgeleid veld voor een marketingkanaal maken voor Customer Journey Analytics
description: Leer hoe u een van een marketingkanaal afgeleid veld voor Customer Journey Analytics maakt
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 1e4c14334da54a5a6e4a0f36b3538c6e4d1a0b6f
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Een afgeleid veld voor een marketingkanaal maken voor Customer Journey Analytics

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

Wanneer het gebruiken van de Bron van Analytics schakelaar, stromen de marketing kanaalgegevens in Customer Journey Analytics door die schakelaar. De regels van het Kanaal van de marketing worden gevormd in traditionele Adobe Analytics en sommige regels worden niet gesteund. Voor meer informatie, zie [ de dimensies van het gebruiks marketing kanaal ](/help/use-cases/aa-data/marketing-channels.md).

Om marketing kanalen in Customer Journey Analytics te gebruiken wanneer het gebruiken van het Web SDK van het Experience Platform, kunt u afgeleide gebieden in een gegevensmening gebruiken om de zelfde marketing kanalen en verwerkingsregels voor Customer Journey Analytics opnieuw tot stand te brengen.

1. Selecteer in Customer Journey Analytics de gegevensweergave waaraan u marketingkanalen wilt toevoegen.

1. Selecteer de tab **[!UICONTROL Components]** in de gegevensweergave.

1. Selecteer **[!UICONTROL Create derived field]** in het linkerspoor.

1. Selecteer in het dialoogvenster **[!UICONTROL Create derived field]** de optie **[!UICONTROL Function templates]** in de vervolgkeuzelijst.

   ![ creeer afgeleide malplaatjes van de gebiedsfunctie ](assets/derived-field-create.png)

1. Sleep de sjabloon **[!UICONTROL Marketing channels]** naar het lege canvas.

1. Pas de logica voor elk marketingkanaal aan om ervoor te zorgen dat deze overeenkomt met de logica die u gebruikt om elk kanaal in uw Adobe Analytics-omgeving te identificeren.

   U kunt de namen van het uitvoerkanaal wijzigen of logica toevoegen om extra kanalen te identificeren specifiek voor uw organisatie.

1. Geef in de rechterkolom een naam en een beschrijving voor het marketingkanaal op.

1. Selecteer **[!UICONTROL Save]** .

   Uw nieuwe afgeleide gebied wordt toegevoegd aan de Afgeleide gebieden > container, als deel van de gebieden van het Schema in de linkerspoorstaaf van uw mening van Gegevens.

