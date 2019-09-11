---
title: internal-bookmark-not-found
description: Uitleg en oplossing voor Docs-buildprobleem internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856215"
---
# <a name="bookmark-not-found"></a><span data-ttu-id="7e9d1-103">bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="7e9d1-103">bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="7e9d1-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="7e9d1-104">Warning</span></span>

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

<span data-ttu-id="7e9d1-105">U probeert te koppelen aan een kop in het huidige bestand of een ander bestand dat niet bestaat.</span><span class="sxs-lookup"><span data-stu-id="7e9d1-105">You're trying to link to a heading in the current file or another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="7e9d1-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="7e9d1-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="7e9d1-107">Controleer de kop waaraan u wilt koppelen en werk de koppeling bij.</span><span class="sxs-lookup"><span data-stu-id="7e9d1-107">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="7e9d1-108">Als u een koppeling wilt maken naar een sectie in het huidige artikel, gebruikt u een hash-symbool gevolgd door de woorden van de kop.</span><span class="sxs-lookup"><span data-stu-id="7e9d1-108">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="7e9d1-109">Verwijder leestekens uit de kop en vervang spaties door streepjes.</span><span class="sxs-lookup"><span data-stu-id="7e9d1-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="7e9d1-110">Een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="7e9d1-110">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="7e9d1-111">Als u een koppeling wilt maken met een kop in een ander bestand, gebruikt u een relatieve koppeling naar dat bestand, gevolgd door een hash-symbool en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="7e9d1-111">To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading.</span></span> <span data-ttu-id="7e9d1-112">Verwijder leestekens uit de kop en vervang spaties door streepjes.</span><span class="sxs-lookup"><span data-stu-id="7e9d1-112">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="7e9d1-113">Een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="7e9d1-113">The following is an example:</span></span>

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
