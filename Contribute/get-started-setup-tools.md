---
title: Hulpprogramma's installeren om inhoud aan te passen
description: In dit artikel leert u hoe u clienthulpprogramma's downloadt en installeert die u nodig hebt voor Git en het bewerken van Markdown-bestanden.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 04/30/2018
ms.openlocfilehash: 24d47c4e094c318be75a27dbaaec11d8ead94452
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288550"
---
# <a name="install-content-authoring-tools"></a>Hulpprogramma's installeren om inhoud aan te passen

Dit artikel beschrijft de stappen om interactief Git-clienthulpprogramma's en Visual Studio Code te installeren.
> [!div class="checklist"]
> * [Git](https://git-scm.com/) installeren
> * [Visual Studio Code](https://code.visualstudio.com/) installeren
> * [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) installeren

>[!IMPORTANT]
> Als u alleen kleine wijzigingen aanbrengt in een artikel, hoeft u de stappen in dit artikel *niet* uit te voeren en kunt u rechtstreeks doorgaan naar de [werkstroom voor kleine wijzigingen](index.md#quick-edits-to-existing-documents).
>
> Belangrijke inzenders wordt aangeraden deze stappen uit te voeren, zodat ze de [werkstroom voor belangrijke/langdurige wijzigingen](how-to-write-workflows-major.md) kunnen gebruiken. Zelfs als u over schrijfmachtigingen beschikt in de hoofdopslagplaats, *is het raadzaam (en wordt dit in deze handleiding aangenomen) dat u de opslagplaats splitst en kloont*, zodat u over lees-/schrijfmachtigingen beschikt om de door u voorgestelde wijzigingen in uw fork op te slaan.

## <a name="install-git-client-tools"></a>Git-clienttools installeren 

 Installeer de nieuwste versie van [de Git-clienttools van Software Freedom Conservancy](https://git-scm.com/download/) voor uw platform. 

* [Git voor Windows](https://git-scm.com/download/win). Deze installatie bevat het Git-versiebeheersysteem en Git Bash, de opdrachtregel-app die u gebruikt voor interactie met uw lokale Git-opslagplaats.
* Git voor Mac wordt aangeboden als onderdeel van de Xcode Command Line Tools. Voer `git` uit vanaf de opdrachtregel. Indien nodig wordt u gevraagd om de opdrachtregelhulpprogramma's te installeren. U kunt [Git voor Mac](https://git-scm.com/download/mac) ook downloaden op de website van de Software Freedom Conservancy.
* [Git voor Linux en Unix](https://git-scm.com/download/linux)

Als u de voorkeur geeft aan een grafische gebruikersinterface (GUI) boven een opdrachtregelinterface (CLI), raadpleegt u [de pagina met beschikbare GUI-clients van Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop van GitHub ](https://desktop.github.com/) of [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) voor een aantal veelgebruikte opties.

Volg de installatie- en configuratie-instructies voor de client van uw keuze.

In het volgende artikel [stelt u een Git-opslagplaats in](get-started-setup-local.md).

   Extra Git-resources zijn hier beschikbaar: [Git-terminologie](https://help.github.com/articles/github-glossary) | [Basisprincipes van Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Git en GitHub leren gebruiken](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>Inzicht in Markdown-editors

Markdown is een eenvoudige opmaaktaal die gemakkelijk is te lezen en te leren. Daarom is het al snel een standaardopmaaktaal geworden. Als u artikelen wilt schrijven in Markdown, kunt u het beste eerst een Markdown-editor downloaden en installeren.  [Visual Studio-Code](https://code.visualstudio.com/) geniet bij Microsoft de voorkeur om Markdown te bewerken. [Atom](https://atom.io) is een ander populair hulpprogramma voor het bewerken van Markdown.

Markdown-tekst wordt opgeslagen in bestanden met de extensie .md.

De artikelen [Markdown gebruiken voor het schrijven van documenten](how-to-write-use-markdown.md) en [Markdown-naslaginformatie voor OPS](markdown-reference.md). bevatten aanvullende informatie over het schrijven met Markdown, waaronder de basisprincipes van Markdown en de functies die worden ondersteund door de aangepaste Markdown-extensies van Open Publishing Services (OPS).

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio-Code](https://code.visualstudio.com/), ook wel bekend als VS Code, is een lichtgewicht editor die geschikt is voor Windows, Linux en Mac. De editor biedt Git-integratie en ondersteuning voor extensies.

Download en installeer [VS Code](https://code.visualstudio.com/). Als het goed is, detecteert de startpagina van VS Code uw besturingssysteem automatisch.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> Voer de opdracht `code .` uit via de opdrachtregel of Bash-shell om VS Code te starten en de huidige map te openen. Als de huidige map deel uitmaakt van een lokale Git-opslagplaats, wordt de GitHub-integratie automatisch in Visual Studio Code weergegeven.

## <a name="docs-authoring-pack"></a>Docs Authoring Pack
Installeer het Docs Authoring Pack voor Visual Studio Code. Deze set extensies bevat beknopte ontwerphulp bij het schrijven van Markdown, evenals een preview-functie zodat u kunt zien hoe de Markdown wordt weergegeven in de stijl van de docs.microsoft.com-pagina.

   Bezoek deze [marktplaats-pagina](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) en selecteer **Installeren**, of zoek in de extensielijst van uw VS Code-venster naar `docsmsft.docs-authoring-pack`. 

   Het Docs Authoring Pack is toegankelijk door in VS Code de toetsencombinatie Alt+M te gebruiken. De werkbalk wordt standaard verborgen, maar kan ook worden weergegeven. U kunt de weergave van de werkbalk inschakelen door in de instellingen voor VS Code (sneltoets Ctrl+,) de gebruikersinstelling `"markdown.showToolbar": true` toe te voegen.

   Raadpleeg voor meer informatie de pagina [Docs Authoring Pack](how-to-write-docs-auth-pack.md).


## <a name="next-steps"></a>Volgende stappen

U bent nu klaar om een [lokale Git-opslagplaats in te stellen](get-started-setup-local.md).
