---
title: external-bookmark-not-found
description: Uitleg en oplossing voor Docs-buildprobleem external-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427457"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="f4e1b-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="f4e1b-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="f4e1b-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="f4e1b-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="f4e1b-105">U probeert te koppelen aan een kop in een ander bestand dat niet bestaat.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="f4e1b-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="f4e1b-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="f4e1b-107">Controleer het bestand waaraan u wilt koppelen en werk uw bladwijzerkoppeling bij om te verwijzen naar een geldige sectie in het bestand.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="f4e1b-108">Als u wilt koppelen naar een sectiekop in een ander artikel, gebruikt u de koppeling ten opzichte van het bestand of de site plus een hash-symbool gevolgd door de woorden van de kop.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="f4e1b-109">Verwijder leestekens uit de kop en vervang spaties door streepjes.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="f4e1b-110">Een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="f4e1b-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
