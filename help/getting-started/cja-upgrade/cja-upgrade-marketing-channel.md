---
title: Een afgeleid veld voor een marketingkanaal maken voor Customer Journey Analytics
description: Meer informatie over het maken van een afgeleid veld voor een marketingkanaal voor Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 2a74da97-61cb-4c98-949b-3fc428839d70
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Een afgeleid veld voor een marketingkanaal maken voor Customer Journey Analytics {#create-marketing-channel-derived-field}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-marketing-channel"
>title="Een van een markeringskanaal afgeleid veld maken"
>abstract="Afgeleide velden worden gemaakt in een gegevensweergave.<br><br> Gebruikend een standaard marketing kanaalopstelling neemt slechts een paar notulen; het creëren van een hoogst aangepaste marketing kanaalopstelling zou verscheidene uren kunnen vergen."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

Wanneer het gebruiken van de de bronschakelaar van de Analyse, stromen de marketing kanaalgegevens in Customer Journey Analytics door die schakelaar. De regels van het Kanaal van de marketing worden gevormd in traditionele Adobe Analytics en sommige regels worden niet gesteund. Voor meer informatie, zie [&#x200B; de dimensies van het gebruiks marketing kanaal &#x200B;](/help/use-cases/aa-data/marketing-channels.md).

Als u marketingkanalen in Customer Journey Analytics wilt gebruiken wanneer u de Experience Platform Web SDK gebruikt, kunt u afgeleide velden in een gegevensweergave gebruiken om dezelfde marketingkanalen en verwerkingsregels voor Customer Journey Analytics opnieuw te maken.

1. Selecteer in Customer Journey Analytics de gegevensweergave waaraan u marketingkanalen wilt toevoegen.

1. Selecteer de tab **[!UICONTROL Components]** in de gegevensweergave.

1. Selecteer **[!UICONTROL Create derived field]** in het linkerspoor.

1. Selecteer in het dialoogvenster **[!UICONTROL Create derived field]** de optie **[!UICONTROL Function templates]** in de vervolgkeuzelijst.

   ![&#x200B; creeer afgeleide malplaatjes van de gebiedsfunctie &#x200B;](assets/derived-field-create.png)

1. Sleep de sjabloon **[!UICONTROL Marketing channels]** naar het lege canvas.

1. Pas de logica voor elk marketingkanaal aan om ervoor te zorgen dat deze overeenkomt met de logica die u gebruikt om elk kanaal in uw Adobe Analytics-omgeving te identificeren.

   U kunt de namen van het uitvoerkanaal wijzigen of logica toevoegen om extra kanalen te identificeren specifiek voor uw organisatie.

1. Geef in de rechterkolom een naam en een beschrijving voor het marketingkanaal op.

1. Selecteer **[!UICONTROL Save]**.

   Uw nieuwe afgeleide gebied wordt toegevoegd aan de Afgeleide gebieden > container, als deel van de gebieden van het Schema in de linkerspoorstaaf van uw mening van Gegevens.

{{upgrade-final-step}}
