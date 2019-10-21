---
title: h1-in-moniker
description: Uitleg en oplossing voor Docs-buildprobleem h1-in-moniker.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3730385cfaf86c3a2a6165f1958d644e71ad7b56
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246355"
---
# <a name="h1-in-moniker"></a><span data-ttu-id="460da-103">h1-in-moniker</span><span class="sxs-lookup"><span data-stu-id="460da-103">h1-in-moniker</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="460da-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="460da-104">Suggestion</span></span>

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

<span data-ttu-id="460da-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="460da-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="460da-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="460da-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="460da-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="460da-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="460da-108">U kunt slechts één H1 hebben in elk bestand.</span><span class="sxs-lookup"><span data-stu-id="460da-108">You can only have one H1 in each file.</span></span> <span data-ttu-id="460da-109">H1 is niet toegestaan in moniker-secties omdat H1-in-moniker-exemplaren eenvoudig kunnen leiden tot dubbele of ontbrekende H1-exemplaren, afhankelijk van de manier waarop versiebeheer is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="460da-109">H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.</span></span>

<span data-ttu-id="460da-110">U ziet dit bericht mogelijk ook als een moniker-sectie een regel met isgelijktekens bevat die een dubbele onderstreping vormen, zoals dit: `=======`.</span><span class="sxs-lookup"><span data-stu-id="460da-110">You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="460da-111">Dit is een alternatieve Markdown-syntaxis voor een H1.</span><span class="sxs-lookup"><span data-stu-id="460da-111">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="460da-112">Het komt ook vaak voor bij samenvoegingsconflicten:</span><span class="sxs-lookup"><span data-stu-id="460da-112">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="460da-113">Oplossing</span><span class="sxs-lookup"><span data-stu-id="460da-113">Resolution</span></span>

<span data-ttu-id="460da-114">U kunt dit probleem oplossen door alle H1-exemplaren uit alle moniker-secties te verwijderen en te zorgen dat de H1 bovenaan het artikel gepast is voor alle moniker-secties.</span><span class="sxs-lookup"><span data-stu-id="460da-114">To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections.</span></span> <span data-ttu-id="460da-115">Het overslaan van kopniveaus, zoals H1 laten volgen door H3, is niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="460da-115">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

<span data-ttu-id="460da-116">Als een H1 in een moniker-sectie eigenlijk een dubbele onderstreping is (`=======`), moet u deze, waar van toepassing, verwijderen of vervangen door een hashtag-kop, zoals `##`.</span><span class="sxs-lookup"><span data-stu-id="460da-116">If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="460da-117">Als de dubbele onderstreping het gevolg van een samenvoegingsconflict is, moet u ook de begin- en eindmarkeringen van het samenvoegingsconflict en de verouderde tekst verwijderen.</span><span class="sxs-lookup"><span data-stu-id="460da-117">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
