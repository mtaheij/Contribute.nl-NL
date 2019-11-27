---
title: h1-empty
description: Uitleg en oplossing voor Docs-buildprobleem h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528793"
---
# <a name="h1-empty"></a><span data-ttu-id="805f3-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="805f3-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="805f3-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="805f3-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="805f3-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="805f3-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="805f3-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="805f3-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="805f3-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="805f3-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="805f3-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="805f3-108">Resolution</span></span>

<span data-ttu-id="805f3-109">U kunt dit probleem oplossen door ervoor te zorgen dat uw H1 inhoud bevat en niet alleen een hash.</span><span class="sxs-lookup"><span data-stu-id="805f3-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="805f3-110">Slecht:</span><span class="sxs-lookup"><span data-stu-id="805f3-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="805f3-111">Goed:</span><span class="sxs-lookup"><span data-stu-id="805f3-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
