---
title: Hulpprogramma's installeren om inhoud aan te passen
description: In dit artikel leert u hoe u clienthulpprogramma's downloadt en installeert die u nodig hebt voor Git en het bewerken van Markdown-bestanden.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1011c3fc829202a3df134ddc80eb05b8959b7bf6
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/22/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="737a5-103">Hulpprogramma's installeren om inhoud aan te passen</span><span class="sxs-lookup"><span data-stu-id="737a5-103">Install content authoring tools</span></span>

<span data-ttu-id="737a5-104">Dit artikel beschrijft de stappen om interactief Git-clienthulpprogramma's en Visual Studio Code te installeren.</span><span class="sxs-lookup"><span data-stu-id="737a5-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="737a5-105">[Git voor Windows](https://git-scm.com/download/win) installeren</span><span class="sxs-lookup"><span data-stu-id="737a5-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="737a5-106">[Visual Studio Code](https://code.visualstudio.com/) installeren</span><span class="sxs-lookup"><span data-stu-id="737a5-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>
> * <span data-ttu-id="737a5-107">[Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) installeren</span><span class="sxs-lookup"><span data-stu-id="737a5-107">Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="737a5-108">Als u alleen kleine wijzigingen aanbrengt in een artikel, hoeft u de stappen in dit artikel *niet* uit te voeren en kunt u rechtstreeks doorgaan naar de [werkstroom voor kleine wijzigingen](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="737a5-108">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="737a5-109">Belangrijke inzenders wordt aangeraden deze stappen uit te voeren, zodat ze de [werkstroom voor belangrijke/langdurige wijzigingen](how-to-write-workflows-major.md) kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="737a5-109">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="737a5-110">Zelfs als u over schrijfmachtigingen beschikt in de hoofdopslagplaats, *is het raadzaam (en wordt dit in deze handleiding aangenomen) dat u de opslagplaats splitst en kloont*, zodat u over lees-/schrijfmachtigingen beschikt om de door u voorgestelde wijzigingen in uw fork op te slaan.</span><span class="sxs-lookup"><span data-stu-id="737a5-110">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="737a5-111">Git-clienthulpprogramma's in Windows installeren</span><span class="sxs-lookup"><span data-stu-id="737a5-111">Install Git client tools on Windows</span></span>

 <span data-ttu-id="737a5-112">Installeer de nieuwste versie van [de Git-clienttools van Software Freedom Conservancy](https://git-scm.com/download/).</span><span class="sxs-lookup"><span data-stu-id="737a5-112">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="737a5-113">Deze installatie bevat het Git-versiebeheersysteem en Git Bash, de opdrachtregel-app die u gebruikt voor interactie met uw lokale Git-opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="737a5-113">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="737a5-114">Als u de voorkeur geeft aan een grafische gebruikersinterface (GUI) boven een opdrachtregelinterface (CLI), raadpleegt u [de pagina met beschikbare GUI-clients van Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop van GitHub ](https://desktop.github.com/) of [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) voor een aantal veelgebruikte opties.</span><span class="sxs-lookup"><span data-stu-id="737a5-114">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="737a5-115">Volg de installatie- en configuratie-instructies voor de client van uw keuze.</span><span class="sxs-lookup"><span data-stu-id="737a5-115">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="737a5-116">In het volgende artikel [stelt u een Git-opslagplaats in](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="737a5-116">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="737a5-117">Aanvullende Git-bronnen vindt u hier: [Git terminology](https://help.github.com/articles/github-glossary) (Git-terminologie) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) (Grondbeginselen van Git) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/) (Git en GitHub onder de knie krijgen)</span><span class="sxs-lookup"><span data-stu-id="737a5-117">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="737a5-118">Inzicht in Markdown-editors</span><span class="sxs-lookup"><span data-stu-id="737a5-118">Understand Markdown editors</span></span>

<span data-ttu-id="737a5-119">Markdown is een eenvoudige opmaaktaal die gemakkelijk is te lezen en te leren.</span><span class="sxs-lookup"><span data-stu-id="737a5-119">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="737a5-120">Daarom is het al snel een standaardopmaaktaal geworden.</span><span class="sxs-lookup"><span data-stu-id="737a5-120">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="737a5-121">Als u artikelen wilt schrijven in Markdown, kunt u het beste eerst een Markdown-editor downloaden en installeren.</span><span class="sxs-lookup"><span data-stu-id="737a5-121">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="737a5-122">[Visual Studio-Code](https://code.visualstudio.com/) geniet bij Microsoft de voorkeur om Markdown te bewerken.</span><span class="sxs-lookup"><span data-stu-id="737a5-122">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="737a5-123">[Atom](https://atom.io) is een ander populair hulpprogramma voor het bewerken van Markdown.</span><span class="sxs-lookup"><span data-stu-id="737a5-123">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="737a5-124">Markdown-tekst wordt opgeslagen in bestanden met de extensie .md.</span><span class="sxs-lookup"><span data-stu-id="737a5-124">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="737a5-125">Aanvullende informatie over het schrijven met Markdown, waaronder de basisprincipes van Markdown en de functies die worden ondersteund door de aangepaste Markdown-extensies van OPS, worden verderop beschreven in het artikel [Markdown gebruiken](how-to-write-use-markdown.md).</span><span class="sxs-lookup"><span data-stu-id="737a5-125">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="737a5-126">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="737a5-126">Visual Studio Code</span></span>

<span data-ttu-id="737a5-127">[Visual Studio-Code](https://code.visualstudio.com/), ook wel bekend als VS Code, is een lichtgewicht editor die geschikt is voor Windows, Linux en Mac.</span><span class="sxs-lookup"><span data-stu-id="737a5-127">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="737a5-128">De editor biedt Git-integratie en ondersteuning voor extensies.</span><span class="sxs-lookup"><span data-stu-id="737a5-128">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="737a5-129">Download en installeer [VS Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="737a5-129">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="737a5-130">Als het goed is, detecteert de startpagina van VS Code uw besturingssysteem automatisch.</span><span class="sxs-lookup"><span data-stu-id="737a5-130">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="737a5-131">Windows</span><span class="sxs-lookup"><span data-stu-id="737a5-131">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="737a5-132">Mac</span><span class="sxs-lookup"><span data-stu-id="737a5-132">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="737a5-133">Linux</span><span class="sxs-lookup"><span data-stu-id="737a5-133">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="737a5-134">Voer de opdracht `code .` uit via de opdrachtregel of Bash-shell om VS Code te starten en de huidige map te openen.</span><span class="sxs-lookup"><span data-stu-id="737a5-134">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="737a5-135">Als de huidige map deel uitmaakt van een lokale Git-opslagplaats, wordt de GitHub-integratie automatisch in Visual Studio Code weergegeven.</span><span class="sxs-lookup"><span data-stu-id="737a5-135">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="docs-authoring-pack"></a><span data-ttu-id="737a5-136">Docs Authoring Pack</span><span class="sxs-lookup"><span data-stu-id="737a5-136">Docs Authoring Pack</span></span>
<span data-ttu-id="737a5-137">Installeer het Docs Authoring Pack voor Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="737a5-137">Install the Docs Authoring Pack for Visual Studio Code.</span></span> <span data-ttu-id="737a5-138">Deze set extensies bevat beknopte ontwerphulp bij het schrijven van Markdown, evenals een preview-functie zodat u kunt zien hoe de Markdown wordt weergegeven in de stijl van de docs.microsoft.com-pagina.</span><span class="sxs-lookup"><span data-stu-id="737a5-138">This set of extensions includes basic authoring assistance for help when writing Markdown, and a preview feature, so that you can see what the Markdown looks like in the style of the docs.microsoft.com site.</span></span>

   <span data-ttu-id="737a5-139">Bezoek deze [marktplaats-pagina](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) en selecteer **Installeren**, of zoek in de extensielijst van uw VS Code-venster naar `docsmsft.docs-authoring-pack`.</span><span class="sxs-lookup"><span data-stu-id="737a5-139">Visit this [marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**, or search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window.</span></span> 

   <span data-ttu-id="737a5-140">Het Docs Authoring Pack is toegankelijk door in VS Code de toetsencombinatie Alt+M te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="737a5-140">The Docs Authoring Pack is accessible by pressing Alt+M inside of VS Code.</span></span> <span data-ttu-id="737a5-141">De werkbalk wordt standaard verborgen, maar kan ook worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="737a5-141">The toolbar is hidden by default but can be shown.</span></span> <span data-ttu-id="737a5-142">U kunt de weergave van de werkbalk inschakelen door in de instellingen voor VS Code (sneltoets Ctrl+,) de gebruikersinstelling `"markdown.showToolbar": true` toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="737a5-142">Edit the VS Code settings (Control+comma) and adding user setting `"markdown.showToolbar": true` to show the toolbar.</span></span>

   <span data-ttu-id="737a5-143">Raadpleeg voor meer informatie de pagina [Docs Authoring Pack](how-to-write-docs-auth-pack.md).</span><span class="sxs-lookup"><span data-stu-id="737a5-143">For more information, see the [Docs Authoring Pack](how-to-write-docs-auth-pack.md) page.</span></span>


## <a name="next-steps"></a><span data-ttu-id="737a5-144">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="737a5-144">Next steps</span></span>

<span data-ttu-id="737a5-145">U bent nu klaar om een [lokale Git-opslagplaats in te stellen](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="737a5-145">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
