---
title: Omleidingen sorteren - Docs Authoring Pack
description: Meer informatie over het sorteren van omleidingen met het Docs Authoring Pack, Visual Studio Code-extensie.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336676"
---
# <a name="sort-redirects"></a><span data-ttu-id="e8ce0-103">Omleidingen sorteren</span><span class="sxs-lookup"><span data-stu-id="e8ce0-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="e8ce0-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="e8ce0-104">Summary</span></span>

<span data-ttu-id="e8ce0-105">Met de ontwikkeling van een docs.microsoft.com-docset worden sommige Markdown-bestanden uiteindelijk verwijderd.</span><span class="sxs-lookup"><span data-stu-id="e8ce0-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="e8ce0-106">Wanneer een Markdown-bestand wordt verwijderd, moeten we een omleiding bieden, zodat alle verwijzingen naar het verwijderde artikel op de juiste wijze worden omgezet via de omleiding.</span><span class="sxs-lookup"><span data-stu-id="e8ce0-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="e8ce0-107">Omleidingen zijn te vinden in het bestand *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="e8ce0-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="e8ce0-108">Open het Opdrachtpalet en druk op <kbd>F1</kbd> (of op <kbd>⇧ ⌘ P</kbd> in macOS)</span><span class="sxs-lookup"><span data-stu-id="e8ce0-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="e8ce0-109">Type: **Docs: Masteromleidingsbestand sorteren**</span><span class="sxs-lookup"><span data-stu-id="e8ce0-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="e8ce0-110">Selecteer de opdracht om deze uit te voeren</span><span class="sxs-lookup"><span data-stu-id="e8ce0-110">Select the command to execute it</span></span>
1. <span data-ttu-id="e8ce0-111">Bekijk wijzigingen in het bestand *.openpublishing.redirection.json*</span><span class="sxs-lookup"><span data-stu-id="e8ce0-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="e8ce0-112">Aandachtspunten</span><span class="sxs-lookup"><span data-stu-id="e8ce0-112">Considerations</span></span>

<span data-ttu-id="e8ce0-113">Het concept van ketenvorming volgt uit de manier waarop het bestand *.openpublishing.redirection.json* oorspronkelijk is ontworpen.</span><span class="sxs-lookup"><span data-stu-id="e8ce0-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="e8ce0-114">Bestanden die als een omleiding worden toegevoegd, raken na verloop van tijd verouderd.</span><span class="sxs-lookup"><span data-stu-id="e8ce0-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="e8ce0-115">Dit gebeurt wanneer bestand A wordt verwijderd en een omleiding naar bestand B nodig heeft, waarna het bestand B wordt verwijderd en vervolgens wordt omgeleid naar bestand C. In het ideale geval verwijzen beide vermeldingen naar C, zodat A omleidt naar C en B hetzelfde blijft.</span><span class="sxs-lookup"><span data-stu-id="e8ce0-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="e8ce0-116">Dit is een kleine prestatieverbetering en er wordt actief gewerkt aan de functie.</span><span class="sxs-lookup"><span data-stu-id="e8ce0-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="e8ce0-117">In actie</span><span class="sxs-lookup"><span data-stu-id="e8ce0-117">In action</span></span>

<span data-ttu-id="e8ce0-118">Hieronder volgt een korte demonstratie van deze functie.</span><span class="sxs-lookup"><span data-stu-id="e8ce0-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="e8ce0-119">[![Voorbeeld van omleidingen sorteren](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="e8ce0-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
