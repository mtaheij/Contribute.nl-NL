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
ms.openlocfilehash: 0ca942e557640db1ba36d3f5b1064656ed3dea8d
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="67586-103">Hulpprogramma's installeren om inhoud aan te passen</span><span class="sxs-lookup"><span data-stu-id="67586-103">Install content authoring tools</span></span>

<span data-ttu-id="67586-104">Dit artikel beschrijft de stappen om interactief Git-clienthulpprogramma's en Visual Studio Code te installeren.</span><span class="sxs-lookup"><span data-stu-id="67586-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="67586-105">[Git voor Windows](https://git-scm.com/download/win) installeren</span><span class="sxs-lookup"><span data-stu-id="67586-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="67586-106">[Visual Studio Code](https://code.visualstudio.com/) installeren</span><span class="sxs-lookup"><span data-stu-id="67586-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="67586-107">Als u alleen kleine wijzigingen aanbrengt in een artikel, hoeft u de stappen in dit artikel *niet* uit te voeren en kunt u rechtstreeks doorgaan naar de [werkstroom voor kleine wijzigingen](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="67586-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="67586-108">Belangrijke inzenders wordt aangeraden deze stappen uit te voeren, zodat ze de [werkstroom voor belangrijke/langdurige wijzigingen](how-to-write-workflows-major.md) kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="67586-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="67586-109">Zelfs als u over schrijfmachtigingen beschikt in de hoofdopslagplaats, *is het raadzaam (en wordt dit in deze handleiding aangenomen) dat u de opslagplaats splitst en kloont*, zodat u over lees-/schrijfmachtigingen beschikt om de door u voorgestelde wijzigingen in uw fork op te slaan.</span><span class="sxs-lookup"><span data-stu-id="67586-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="67586-110">Git-clienthulpprogramma's in Windows installeren</span><span class="sxs-lookup"><span data-stu-id="67586-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="67586-111">Installeer de nieuwste versie van [de Git-clienttools van Software Freedom Conservancy](https://git-scm.com/download/).</span><span class="sxs-lookup"><span data-stu-id="67586-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="67586-112">Deze installatie bevat het Git-versiebeheersysteem en Git Bash, de opdrachtregel-app die u gebruikt voor interactie met uw lokale Git-opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="67586-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="67586-113">Als u de voorkeur geeft aan een grafische gebruikersinterface (GUI) boven een opdrachtregelinterface (CLI), raadpleegt u [de pagina met beschikbare GUI-clients van Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop van GitHub ](https://desktop.github.com/) of [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) voor een aantal veelgebruikte opties.</span><span class="sxs-lookup"><span data-stu-id="67586-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="67586-114">Volg de installatie- en configuratie-instructies voor de client van uw keuze.</span><span class="sxs-lookup"><span data-stu-id="67586-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="67586-115">In het volgende artikel [stelt u een Git-opslagplaats in](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="67586-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="67586-116">Aanvullende Git-bronnen vindt u hier: [Git terminology](https://help.github.com/articles/github-glossary) (Git-terminologie) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) (Grondbeginselen van Git) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/) (Git en GitHub onder de knie krijgen)</span><span class="sxs-lookup"><span data-stu-id="67586-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="67586-117">Inzicht in Markdown-editors</span><span class="sxs-lookup"><span data-stu-id="67586-117">Understand Markdown editors</span></span>

<span data-ttu-id="67586-118">Markdown is een eenvoudige opmaaktaal die gemakkelijk is te lezen en te leren.</span><span class="sxs-lookup"><span data-stu-id="67586-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="67586-119">Daarom is het al snel een standaardopmaaktaal geworden.</span><span class="sxs-lookup"><span data-stu-id="67586-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="67586-120">Als u artikelen wilt schrijven in Markdown, kunt u het beste eerst een Markdown-editor downloaden en installeren.</span><span class="sxs-lookup"><span data-stu-id="67586-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="67586-121">[Visual Studio-Code](https://code.visualstudio.com/) geniet bij Microsoft de voorkeur om Markdown te bewerken.</span><span class="sxs-lookup"><span data-stu-id="67586-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="67586-122">[Atom](https://atom.io) is een ander populair hulpprogramma voor het bewerken van Markdown.</span><span class="sxs-lookup"><span data-stu-id="67586-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="67586-123">Markdown-tekst wordt opgeslagen in bestanden met de extensie .md.</span><span class="sxs-lookup"><span data-stu-id="67586-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="67586-124">Aanvullende informatie over het schrijven met Markdown, waaronder de basisprincipes van Markdown en de functies die worden ondersteund door de aangepaste Markdown-extensies van OPS, worden verderop beschreven in het artikel [Markdown gebruiken](how-to-write-use-markdown.md).</span><span class="sxs-lookup"><span data-stu-id="67586-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="67586-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="67586-125">Visual Studio Code</span></span>

<span data-ttu-id="67586-126">[Visual Studio-Code](https://code.visualstudio.com/), ook wel bekend als VS Code, is een lichtgewicht editor die geschikt is voor Windows, Linux en Mac.</span><span class="sxs-lookup"><span data-stu-id="67586-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="67586-127">De editor biedt Git-integratie en ondersteuning voor extensies.</span><span class="sxs-lookup"><span data-stu-id="67586-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="67586-128">Download en installeer [VS Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="67586-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="67586-129">Als het goed is, detecteert de startpagina van VS Code uw besturingssysteem automatisch.</span><span class="sxs-lookup"><span data-stu-id="67586-129">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="67586-130">Windows</span><span class="sxs-lookup"><span data-stu-id="67586-130">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="67586-131">Mac</span><span class="sxs-lookup"><span data-stu-id="67586-131">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="67586-132">Linux</span><span class="sxs-lookup"><span data-stu-id="67586-132">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="67586-133">Voer de opdracht `code .` uit via de opdrachtregel of Bash-shell om VS Code te starten en de huidige map te openen.</span><span class="sxs-lookup"><span data-stu-id="67586-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="67586-134">Als de huidige map deel uitmaakt van een lokale Git-opslagplaats, wordt de GitHub-integratie automatisch in Visual Studio Code weergegeven.</span><span class="sxs-lookup"><span data-stu-id="67586-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="67586-135">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="67586-135">Next steps</span></span>

<span data-ttu-id="67586-136">U bent nu klaar om een [lokale Git-opslagplaats in te stellen](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="67586-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
