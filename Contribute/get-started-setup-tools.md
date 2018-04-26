---
title: Hulpprogramma's installeren om inhoud aan te passen
description: In dit artikel leert u hoe u clienthulpprogramma's downloadt en installeert die u nodig hebt voor Git en het bewerken van Markdown-bestanden.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a>Hulpprogramma's installeren om inhoud aan te passen

Dit artikel beschrijft de stappen om interactief Git-clienthulpprogramma's en Visual Studio Code te installeren.
> [!div class="checklist"]
> * [Git voor Windows](https://git-scm.com/download/win) installeren
> * [Visual Studio Code](https://code.visualstudio.com/) installeren

>[!IMPORTANT]
> Als u alleen kleine wijzigingen aanbrengt in een artikel, hoeft u de stappen in dit artikel *niet* uit te voeren en kunt u rechtstreeks doorgaan naar de [werkstroom voor kleine/onregelmatige wijzigingen](light-workflow.md).
>
> Belangrijke inzenders wordt aangeraden deze stappen uit te voeren, zodat ze de [werkstroom voor belangrijke/langdurige wijzigingen](full-workflow.md) kunnen gebruiken. Zelfs als u over schrijfmachtigingen beschikt in de hoofdopslagplaats, *is het raadzaam (en wordt dit in deze handleiding aangenomen) dat u de opslagplaats splitst en kloont*, zodat u over lees-/schrijfmachtigingen beschikt om de door u voorgestelde wijzigingen in uw fork op te slaan.

## <a name="install-git-client-tools-on-windows"></a>Git-clienthulpprogramma's in Windows installeren

 Installeer de nieuwste versie van [de Git-clienttools van Software Freedom Conservancy](https://git-scm.com/download/). Deze installatie bevat het Git-versiebeheersysteem en Git Bash, de opdrachtregel-app die u gebruikt voor interactie met uw lokale Git-opslagplaats.

Als u de voorkeur geeft aan een grafische gebruikersinterface (GUI) boven een opdrachtregelinterface (CLI), raadpleegt u [de pagina met beschikbare GUI-clients van Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop van GitHub ](https://desktop.github.com/) of [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) voor een aantal veelgebruikte opties.

Volg de installatie- en configuratie-instructies voor de client van uw keuze.

In het volgende artikel [stelt u een Git-opslagplaats in](get-started-setup-local.md).

   Aanvullende Git-bronnen vindt u hier: [Git terminology](https://help.github.com/articles/github-glossary) (Git-terminologie) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) (Grondbeginselen van Git) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/) (Git en GitHub onder de knie krijgen)

## <a name="understand-markdown-editors"></a>Inzicht in Markdown-editors

Markdown is een eenvoudige opmaaktaal die gemakkelijk is te lezen en te leren. Daarom is het al snel een standaardopmaaktaal geworden. Als u artikelen wilt schrijven in Markdown, kunt u het beste eerst een Markdown-editor downloaden en installeren.  [Visual Studio-Code](https://code.visualstudio.com/) geniet bij Microsoft de voorkeur om Markdown te bewerken. [Atom](https://atom.io) is een ander populair hulpprogramma voor het bewerken van Markdown.

Markdown-tekst wordt opgeslagen in bestanden met de extensie .md.

Aanvullende informatie over het schrijven met Markdown, waaronder de basisprincipes van Markdown en de functies die worden ondersteund door de aangepaste Markdown-extensies van OPS, worden verderop beschreven in het artikel [Markdown gebruiken](how-to-write-use-markdown.md).

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio-Code](https://code.visualstudio.com/), ook wel bekend als VS Code, is een lichtgewicht editor die geschikt is voor Windows, Linux en Mac. De editor biedt Git-integratie en ondersteuning voor extensies.

Download en installeer [VS Code](https://code.visualstudio.com/). Als het goed is, detecteert de startpagina van VS Code uw besturingssysteem automatisch.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> Voer de opdracht `code .` uit via de opdrachtregel of Bash-shell om VS Code te starten en de huidige map te openen. Als de huidige map deel uitmaakt van een lokale Git-opslagplaats, wordt de GitHub-integratie automatisch in Visual Studio Code weergegeven.

## <a name="next-steps"></a>Volgende stappen

U bent nu klaar om een [lokale Git-opslagplaats in te stellen](get-started-setup-local.md).
