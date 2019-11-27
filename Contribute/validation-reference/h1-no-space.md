---
title: h1-no-space
description: Uitleg en oplossing voor Docs-buildprobleem h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528956"
---
# <a name="h1-no-space"></a><span data-ttu-id="3a840-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="3a840-103">h1-no-space</span></span>

## <a name="warning"></a><span data-ttu-id="3a840-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="3a840-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="3a840-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="3a840-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="3a840-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="3a840-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="3a840-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="3a840-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="3a840-108">Zonder de spatie na de hash, wordt een H1 niet herkend in Docs.</span><span class="sxs-lookup"><span data-stu-id="3a840-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="3a840-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="3a840-109">Resolution</span></span>

<span data-ttu-id="3a840-110">Voeg een spatie toe na de hash in uw H1 om dit probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="3a840-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
