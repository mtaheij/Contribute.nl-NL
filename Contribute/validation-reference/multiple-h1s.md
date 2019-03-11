---
title: multiple-h1
description: Uitleg en oplossing voor Docs-buildprobleem multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427525"
---
# <a name="multiple-h1"></a><span data-ttu-id="4e79f-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="4e79f-103">multiple-h1</span></span>

## <a name="warning"></a><span data-ttu-id="4e79f-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="4e79f-104">Warning</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="4e79f-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="4e79f-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="4e79f-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="4e79f-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="4e79f-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="4e79f-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="4e79f-108">U kunt slechts één H1 hebben in elk bestand.</span><span class="sxs-lookup"><span data-stu-id="4e79f-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="4e79f-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="4e79f-109">Resolution</span></span>

<span data-ttu-id="4e79f-110">Om dit probleem op te lossen, wijzigt u het kopniveau van H1s in H2 (`##`) of deelt u uw bestand anders in.</span><span class="sxs-lookup"><span data-stu-id="4e79f-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="4e79f-111">Het overslaan van kopniveaus, zoals H1 laten volgen door H3, is niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="4e79f-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]