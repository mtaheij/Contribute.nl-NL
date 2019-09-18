---
title: h1-not-first
description: Uitleg en oplossing voor Docs-buildprobleem h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895457"
---
# <a name="h1-not-first"></a><span data-ttu-id="3ea47-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="3ea47-103">h1-not-first</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="3ea47-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="3ea47-104">Suggestion</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="3ea47-105">Alleen de header van de YAML-metagegevens kan vóór de H1 komen in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="3ea47-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="3ea47-106">Als u bijvoorbeeld boven aan het artikel een notitie of een afbeelding wilt toevoegen, moet deze na H1 komen.</span><span class="sxs-lookup"><span data-stu-id="3ea47-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="3ea47-107">Het volgende is niet toegestaan:</span><span class="sxs-lookup"><span data-stu-id="3ea47-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="3ea47-108">Doe dit in plaats daarvan:</span><span class="sxs-lookup"><span data-stu-id="3ea47-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="3ea47-109">Een andere veelvoorkomende oorzaak van dit probleem is [byte order marks (BOM's)](http://www.websina.com/bugzero/kb/unicode-bom.html) vóór de YAML-header.</span><span class="sxs-lookup"><span data-stu-id="3ea47-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="3ea47-110">Deze worden soms geïntroduceerd door coderingsproblemen bij het doorvoeren van inhoud naar opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="3ea47-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="3ea47-111">Ze veroorzaken een ongeldige rendering in GitHub en moeten worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="3ea47-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="3ea47-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="3ea47-112">Resolution</span></span>

<span data-ttu-id="3ea47-113">Verwijder andere inhoud dan de header van de YAML-metagegevens voor de H1.</span><span class="sxs-lookup"><span data-stu-id="3ea47-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
