---
title: Slimme aanhalingstekens automatisch vervangen - Docs Authoring Pack
description: Meer informatie over hoe u slimme aanhalingstekens automatisch vervangt met het Docs Authoring Pack, en de Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336699"
---
# <a name="smart-quote-replacement"></a><span data-ttu-id="1ded9-103">Slimme aanhalingstekens vervangen</span><span class="sxs-lookup"><span data-stu-id="1ded9-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="1ded9-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="1ded9-104">Summary</span></span>

<span data-ttu-id="1ded9-105">Ontwikkelaars van inhoud hebben een aantal van de meest geavanceerde functies van moderne technologieën en intelligence ontwikkeld, maar onze tools geven nog steeds de voorkeur aan 'domme aanhalingstekens' in Markdown.</span><span class="sxs-lookup"><span data-stu-id="1ded9-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="1ded9-106">De antoniem is natuurlijk 'slimme aanhalingstekens'.</span><span class="sxs-lookup"><span data-stu-id="1ded9-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="1ded9-107">Slimme aanhalingstekens zijn gebruikelijk met ideale typografieën, maar hebben niet de voorkeur met Markdown en gerenderde HTML.</span><span class="sxs-lookup"><span data-stu-id="1ded9-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="1ded9-108">Wanneer u bijvoorbeeld werkt aan Microsoft Word-documenten, hebt u wellicht wel gezien dat wanneer u de <kbd>Shift</kbd>-toets ingedrukt houdt en een <kbd>"</kbd> typt, het teken `"` snel wordt vervangen door een slim aanhalingsteken `“`.</span><span class="sxs-lookup"><span data-stu-id="1ded9-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="1ded9-109">Description</span><span class="sxs-lookup"><span data-stu-id="1ded9-109">Description</span></span>        | <span data-ttu-id="1ded9-110">Unicode</span><span class="sxs-lookup"><span data-stu-id="1ded9-110">Unicode</span></span>  | <span data-ttu-id="1ded9-111">Slim aanhalingsteken</span><span class="sxs-lookup"><span data-stu-id="1ded9-111">Smart Quote</span></span> | <span data-ttu-id="1ded9-112">Vervanging</span><span class="sxs-lookup"><span data-stu-id="1ded9-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="1ded9-113">Dubbel aanhalingsteken links</span><span class="sxs-lookup"><span data-stu-id="1ded9-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="1ded9-114">Dubbel aanhalingsteken rechts</span><span class="sxs-lookup"><span data-stu-id="1ded9-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="1ded9-115">Enkel aanhalingsteken links</span><span class="sxs-lookup"><span data-stu-id="1ded9-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="1ded9-116">Enkel aanhalingsteken rechts</span><span class="sxs-lookup"><span data-stu-id="1ded9-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="1ded9-117">Wanneer u in een Markdown-bestand ( *\*.md*) tekst plakt of wanneer u inhoud bijwerkt: met deze functie wordt de inhoud actief geëvalueerd en worden waarden automatisch dienovereenkomstig vervangen.</span><span class="sxs-lookup"><span data-stu-id="1ded9-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="1ded9-118">Met de functie voor het vervangen van een slim aanhalingsteken worden ook andere tekens vervangen, zoals, maar niet beperkt tot; (`©, ™, ®, •`, subscript- en superscripttekens).</span><span class="sxs-lookup"><span data-stu-id="1ded9-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="1ded9-119">Dit is handig wanneer u tekst uit Word-documenten plakt.</span><span class="sxs-lookup"><span data-stu-id="1ded9-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="1ded9-120">Voorkeuren</span><span class="sxs-lookup"><span data-stu-id="1ded9-120">Preferences</span></span>

<span data-ttu-id="1ded9-121">Deze functie is optioneel, maar wordt standaard ingesteld op `true`.</span><span class="sxs-lookup"><span data-stu-id="1ded9-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="1ded9-122">Deze functie in- of uitschakelen:</span><span class="sxs-lookup"><span data-stu-id="1ded9-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="1ded9-123">Selecteer **Bestand** > **Voorkeuren** > **Instellingen** en filter op *Docs Markdown-extensie*.</span><span class="sxs-lookup"><span data-stu-id="1ded9-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="1ded9-124">De instelling in- en uitschakelen in de sectie **Markdown: Sectie Slimme aanhalingstekens vervangen**.</span><span class="sxs-lookup"><span data-stu-id="1ded9-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="1ded9-125">In actie</span><span class="sxs-lookup"><span data-stu-id="1ded9-125">In action</span></span>

<span data-ttu-id="1ded9-126">Hieronder volgt een korte demonstratie van deze functie.</span><span class="sxs-lookup"><span data-stu-id="1ded9-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="1ded9-127">[![Voorbeeld van slimme aanhalingstekens vervangen](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="1ded9-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
