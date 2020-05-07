---
title: Voltooiing van dev lang - Docs Authoring Pack
description: Meer informatie over hoe dev lang-voltooiing inzenders helpt in het Docs Authoring Pack, Visual Studio Code extensie.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336791"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="a6e78-103">Voltooiing van dev lang</span><span class="sxs-lookup"><span data-stu-id="a6e78-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="a6e78-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="a6e78-104">Summary</span></span>

<span data-ttu-id="a6e78-105">Inzenders hebben hulp nodig bij het bepalen van de geldige taal-id's (dev langs) die in een Markdown-bestand driedubbele apostroffen (code-afbakeningopeningen) kunnen volgen.</span><span class="sxs-lookup"><span data-stu-id="a6e78-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="a6e78-106">Helaas bestaat er geen validatie tijdens build time van dev-lang.</span><span class="sxs-lookup"><span data-stu-id="a6e78-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="a6e78-107">Het resultaat is een ongelijksoortige weergave van één taal binnen dezelfde conceptuele docset.</span><span class="sxs-lookup"><span data-stu-id="a6e78-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="a6e78-108">Kijk bijvoorbeeld eens naar C#.</span><span class="sxs-lookup"><span data-stu-id="a6e78-108">Consider C# as an example.</span></span> <span data-ttu-id="a6e78-109">Inzenders hebben `c#`, `C#`, `cs`, `csharp` en andere gebruikt als dev lang-weergaven van de taal.</span><span class="sxs-lookup"><span data-stu-id="a6e78-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="a6e78-110">Welke van de voorgaande weergaven is correct?</span><span class="sxs-lookup"><span data-stu-id="a6e78-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="a6e78-111">De functie *Voltooiing van dev lang* neemt de verwarring weg door een lijst met bekende dev langs weer te geven.</span><span class="sxs-lookup"><span data-stu-id="a6e78-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="a6e78-112">Bij het selecteren van een dev lang-naam uit IntelliSense:</span><span class="sxs-lookup"><span data-stu-id="a6e78-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="a6e78-113">De code-afbakening wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="a6e78-113">The code fence is closed.</span></span>
* <span data-ttu-id="a6e78-114">Het caret-teken bevindt zich in de code-afbakening.</span><span class="sxs-lookup"><span data-stu-id="a6e78-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="a6e78-115">Voorkeuren</span><span class="sxs-lookup"><span data-stu-id="a6e78-115">Preferences</span></span>

<span data-ttu-id="a6e78-116">Het is niet mogelijk om deze functie uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="a6e78-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="a6e78-117">De volgende instellingen zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="a6e78-117">The following settings are available:</span></span>

* [<span data-ttu-id="a6e78-118">Veelgebruikte dev langs weergeven</span><span class="sxs-lookup"><span data-stu-id="a6e78-118">Display commonly used dev langs</span></span>](#display-commonly-used-dev-langs)
* [<span data-ttu-id="a6e78-119">Alle bekende dev langs weergeven</span><span class="sxs-lookup"><span data-stu-id="a6e78-119">Display all known dev langs</span></span>](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="a6e78-120">Veelgebruikte dev langs weergeven</span><span class="sxs-lookup"><span data-stu-id="a6e78-120">Display commonly used dev langs</span></span>

<span data-ttu-id="a6e78-121">Er wordt slechts een subset van de geldige dev langs gebruikt in één docset.</span><span class="sxs-lookup"><span data-stu-id="a6e78-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="a6e78-122">De gebruikerservaring verbeteren:</span><span class="sxs-lookup"><span data-stu-id="a6e78-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="a6e78-123">Open in Visual Studio Code de docset naar de hoofdmap.</span><span class="sxs-lookup"><span data-stu-id="a6e78-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="a6e78-124">Selecteer **Bestand** > **Voorkeuren** > **Instellingen** en filter op *Docs Markdown-extensie*.</span><span class="sxs-lookup"><span data-stu-id="a6e78-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="a6e78-125">Klik op de koppeling **Bewerken in settings.json** in de sectie **Markdown: Docset-talen**.</span><span class="sxs-lookup"><span data-stu-id="a6e78-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="a6e78-126">Voeg de volgende eigenschap `markdown.docsetLanguages` toe aan het bestand *settings.json*:</span><span class="sxs-lookup"><span data-stu-id="a6e78-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="a6e78-127">Plaats het caret-teken in de lege matrix van de eigenschap en activeer IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span><span class="sxs-lookup"><span data-stu-id="a6e78-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="a6e78-128">Er wordt een lijst met namen van bekende dev langs weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a6e78-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="a6e78-129">Voeg dev lang-namen toe aan de matrix totdat u tevreden bent met de lijst.</span><span class="sxs-lookup"><span data-stu-id="a6e78-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="a6e78-130">In de volgende lijst worden bijvoorbeeld vier dev lang-namen weergegeven aan de gebruiker na het typen van driedubbele apostrof:</span><span class="sxs-lookup"><span data-stu-id="a6e78-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="a6e78-131">Sla de wijzigingen op in het bestand *settings.json*.</span><span class="sxs-lookup"><span data-stu-id="a6e78-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="a6e78-132">Een lege `markdown.docsetLanguages`-matrix zorgt ervoor dat alle bekende dev langs worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a6e78-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="a6e78-133">Alle bekende dev langs weergeven</span><span class="sxs-lookup"><span data-stu-id="a6e78-133">Display all known dev langs</span></span>

<span data-ttu-id="a6e78-134">Standaard worden alle bekende dev lang-namen weergegeven in IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="a6e78-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="a6e78-135">Deze instelling overschrijft de eigenschap `markdown.docsetLanguages` die wordt beschreven in [Veelgebruikte dev-langs weergeven](#display-commonly-used-dev-langs).</span><span class="sxs-lookup"><span data-stu-id="a6e78-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="a6e78-136">U kunt deze instelling als volgt wijzigen:</span><span class="sxs-lookup"><span data-stu-id="a6e78-136">To change this setting:</span></span>

1. <span data-ttu-id="a6e78-137">Selecteer **Bestand** > **Voorkeuren** > **Instellingen** en filter op *Docs Markdown-extensie*.</span><span class="sxs-lookup"><span data-stu-id="a6e78-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="a6e78-138">De instelling in- en uitschakelen in de sectie **Markdown: Alle beschikbare talen**.</span><span class="sxs-lookup"><span data-stu-id="a6e78-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="a6e78-139">In actie</span><span class="sxs-lookup"><span data-stu-id="a6e78-139">In action</span></span>

<span data-ttu-id="a6e78-140">Hieronder volgt een korte demonstratie van deze functie:</span><span class="sxs-lookup"><span data-stu-id="a6e78-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="a6e78-141">[![Voltooiing van dev lang](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a6e78-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
