---
title: multiple-h1s
description: Uitleg en oplossing voor Docs-buildprobleem multiple-h1s.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528947"
---
# <a name="multiple-h1s"></a><span data-ttu-id="7b5b2-103">multiple-h1s</span><span class="sxs-lookup"><span data-stu-id="7b5b2-103">multiple-h1s</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="7b5b2-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="7b5b2-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="7b5b2-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="7b5b2-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="7b5b2-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="7b5b2-108">U kunt slechts één H1 hebben in elk bestand.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="7b5b2-109">U ziet dit bericht mogelijk ook als uw artikel een regel met isgelijktekens bevat die een dubbele onderstreping vormen, zoals dit: `=======`.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="7b5b2-110">Dit is een alternatieve Markdown-syntaxis voor een H1.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="7b5b2-111">Het komt ook vaak voor bij samenvoegingsconflicten:</span><span class="sxs-lookup"><span data-stu-id="7b5b2-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="7b5b2-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="7b5b2-112">Resolution</span></span>

<span data-ttu-id="7b5b2-113">Om dit probleem op te lossen, wijzigt u het kopniveau van H1s in H2 (`##`) of deelt u uw bestand anders in.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="7b5b2-114">Het overslaan van kopniveaus, zoals H1 laten volgen door H3, is niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="7b5b2-115">Als een extra H1 eigenlijk een dubbele onderstreping is (`=======`), moet u deze, waar van toepassing, verwijderen of vervangen door een hashtag-kop, zoals `##`.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="7b5b2-116">Als de dubbele onderstreping het gevolg van een samenvoegingsconflict is, moet u ook de begin- en eindmarkeringen van het samenvoegingsconflict en de verouderde tekst verwijderen.</span><span class="sxs-lookup"><span data-stu-id="7b5b2-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
