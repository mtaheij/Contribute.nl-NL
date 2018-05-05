---
title: GitHub-bijdragewerkstroom voor kleine of onregelmatige wijzigingen
description: In dit artikel wordt beschreven hoe u de werkstroom voor minder belangrijke bijdragen gebruikt om bijdragen te leveren aan artikelen op docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>GitHub-bijdragewerkstroom voor kleine of onregelmatige wijzigingen

> [!IMPORTANT]
> Op alle opslagplaatsen die naar docs.microsoft.com publiceren, is de [Microsoft Open Source-gedragscode](https://opensource.microsoft.com/codeofconduct/) of de [.NET Foundation-gedragscode](https://dotnetfoundation.org/code-of-conduct) van toepassing. Zie [Veelgestelde vragen over de gedragscode](https://opensource.microsoft.com/codeofconduct/faq/) voor meer informatie. Of neem contact op via [opencode@microsoft.com](mailto:opencode@microsoft.com) of [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) als u vragen of opmerkingen hebt.<br>
>
> Kleine correcties of verduidelijkingen voor de documentatie en codevoorbeelden in de openbare opslagplaatsen vallen onder de [gebruiksvoorwaarden van docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Bij nieuwe inhoud of belangrijke wijzigingen wordt een opmerking gegenereerd in de pull-aanvraag, waarin u wordt gevraagd een online Contribution License Agreement (CLA) in te dienen als u geen werknemer van Microsoft bent. U moet het onlineformulier invullen voordat we uw pull-aanvraag kunnen accepteren.

## <a name="overview"></a>Overzicht

Deze werkstroom is geschikt voor het aanbrengen van kleine of onregelmatige wijzigingen met de Markdown-webeditor van GitHub. U kunt met de GitHub-editor maar een beperkt aantal handelingen verrichten, omdat de gebruikersinterface geen ondersteuning biedt voor alle Git-bewerkingen en ontwerpscenario's. Als u grote bijdragen wilt leveren of ondersteuning nodig hebt voor geavanceerde Git-functies (zoals vertakkingsbeheer of geavanceerde oplossingen voor samenvoegingsconflicten), raadpleegt u de [werkstroom voor belangrijke/langdurige wijzigingen](full-workflow.md).

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>Procedure voor het gebruik van de GitHub-editor om wijzigingen voor te stellen

1. Blader naar de GitHub-opslagplaats en het Markdown-bestand dat bij het artikel behoort. U kunt een van de volgende methoden gebruiken:

   - Blader door de Markdown-bestanden in de betreffende GitHub-opslagplaats om naar het artikel te gaan.
   - Ga naar het artikel op [docs.microsoft.com](https://docs.microsoft.com/) en selecteer de koppeling **Bewerken** in de rechterbovenhoek van de pagina.

     ![Locatie van de link Bewerken](./media/light-workflow/contributetogit.png)

2. Selecteer het potloodpictogram **Edit this file** om naar de bewerkingsmodus over te gaan:

    ![Locatie van het potloodpictogram](./media/light-workflow/editicon.png)

3. Breng wijzigingen aan met Markdown op het tabblad **Bestand bewerken** en bekijk een voorbeeld van de aangebrachte wijzigingen op het tabblad **Voorbeeld van wijzigingen**. Het gebruik van de editor is redelijk eenvoudig. Als u echter hulp nodig hebt, raadpleegt u de volgende handleidingen:

   - [Markdown gebruiken](how-to-write-use-markdown.md)
   - [Bestanden maken in GitHub](https://github.com/blog/1327-creating-files-on-github)
   - [Bestanden uploaden naar de opslagplaatsen](https://github.com/blog/2105-upload-files-to-your-repositories)

4. Scrol naar de onderkant van de pagina waar een van de volgende opties wordt weergegeven:

   - **Bestandswijziging voorstellen**: verschijnt als u alleen-lezentoegang hebt tot de opslagplaats, zoals [bestanden bewerken in de opslagplaats van een andere gebruiker](https://help.github.com/articles/editing-files-in-another-user-s-repository/). In dit geval maakt GitHub een patchvertakking in uw kopie van de opslagplaats (en maakt deze automatisch een kopie als deze nog niet bestaat). Als u de knop **Propose file change** hebt geselecteerd, verschijnt de pagina **Comparing changes**, waar u uw wijzigingen kunt controleren. U selecteert vervolgens de knop **Create pull request** om de wijzigingen te verzenden naar de wachtrij voor pull-aanvragen en u gaat verder naar de [volgende sectie](#pull-request-processing).

   - **Wijzigingen doorvoeren**: verschijnt als u schrijftoegang hebt tot de opslagplaats zoals [bestanden bewerken in uw eigen opslagplaats](https://help.github.com/articles/editing-files-in-your-repository/). In dit geval kunt u in GitHub op twee manieren de wijzigingen opslaan:

     - **De wijzigingen rechtstreeks doorvoeren in de vertakking `<branch-name>`** waar `<branch-name>` de naam is van de vertakking waar u zich bevond toen u de knop **Bewerken** hebt geselecteerd. Hierbij worden de wijzigingen rechtstreeks toegepast op de vertakking en wordt er geen pull-aanvraag gebruikt. Hiermee hebt u de bewerking voltooid.

     - **Maak een nieuwe vertakking voor deze doorvoering en start een pull-aanvraag**, waarbij u wordt gevraagd een nieuwe vertakking te maken en een standaardnaam wordt voorgesteld. Als u de knop **Propose file change** hebt geselecteerd, verschijnt de pagina **Comparing changes**, waar u uw wijzigingen kunt controleren. U selecteert vervolgens de knop **Create pull request** om de wijzigingen te verzenden naar de wachtrij voor pull-aanvragen en u gaat verder naar de [volgende sectie](#pull-request-processing).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Volgende stappen

- Ga verder naar de artikelen Belangrijke aspecten van het schrijven voor meer informatie over Markdown, de syntaxis van Markdown-extensies en meer.
