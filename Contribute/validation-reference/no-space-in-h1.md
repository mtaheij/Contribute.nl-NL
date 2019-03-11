---
title: no-space-in-h1
description: Uitleg en oplossing voor Docs-buildprobleem no-space-in-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427504"
---
# <a name="no-space-in-h1"></a><span data-ttu-id="96b6a-103">no-space-in-h1</span><span class="sxs-lookup"><span data-stu-id="96b6a-103">no-space-in-h1</span></span>

## <a name="warning"></a><span data-ttu-id="96b6a-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="96b6a-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="96b6a-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="96b6a-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="96b6a-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="96b6a-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="96b6a-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="96b6a-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="96b6a-108">Zonder de spatie na de hash, wordt een H1 niet herkend in Docs.</span><span class="sxs-lookup"><span data-stu-id="96b6a-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="96b6a-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="96b6a-109">Resolution</span></span>

<span data-ttu-id="96b6a-110">Voeg een spatie toe na de hash in uw H1 om dit probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="96b6a-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]