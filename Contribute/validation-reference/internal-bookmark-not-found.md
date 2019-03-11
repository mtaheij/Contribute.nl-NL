---
title: internal-bookmark-not-found
description: Uitleg en oplossing voor Docs-buildprobleem internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427493"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="bf58b-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="bf58b-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="bf58b-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="bf58b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bf58b-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="bf58b-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="bf58b-106">U probeert te koppelen aan een kop in het huidige bestand dat niet bestaat.</span><span class="sxs-lookup"><span data-stu-id="bf58b-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="bf58b-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="bf58b-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="bf58b-108">Controleer de kop waaraan u wilt koppelen en werk de koppeling bij.</span><span class="sxs-lookup"><span data-stu-id="bf58b-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="bf58b-109">Als u een koppeling wilt maken naar een sectie in het huidige artikel, gebruikt u een hash-symbool gevolgd door de woorden van de kop.</span><span class="sxs-lookup"><span data-stu-id="bf58b-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="bf58b-110">Verwijder leestekens uit de kop en vervang spaties door streepjes.</span><span class="sxs-lookup"><span data-stu-id="bf58b-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="bf58b-111">Een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="bf58b-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
