---
title: h1-empty
description: Uitleg en oplossing voor Docs-buildprobleem h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427275"
---
# <a name="h1-empty"></a><span data-ttu-id="1c079-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="1c079-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="1c079-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="1c079-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="1c079-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="1c079-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="1c079-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="1c079-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="1c079-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="1c079-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="1c079-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="1c079-108">Resolution</span></span>

<span data-ttu-id="1c079-109">U kunt dit probleem oplossen door ervoor te zorgen dat uw H1 inhoud bevat en niet alleen een hash.</span><span class="sxs-lookup"><span data-stu-id="1c079-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="1c079-110">Slecht:</span><span class="sxs-lookup"><span data-stu-id="1c079-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="1c079-111">Goed:</span><span class="sxs-lookup"><span data-stu-id="1c079-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]