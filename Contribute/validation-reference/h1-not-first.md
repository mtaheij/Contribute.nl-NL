---
title: h1-not-first
description: Uitleg en oplossing voor Docs-buildprobleem h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528915"
---
# <a name="h1-not-first"></a><span data-ttu-id="ecac2-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="ecac2-103">h1-not-first</span></span>

## <a name="warning"></a><span data-ttu-id="ecac2-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="ecac2-104">Warning</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="ecac2-105">Alleen de header van de YAML-metagegevens kan vóór de H1 komen in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="ecac2-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="ecac2-106">Als u bijvoorbeeld boven aan het artikel een notitie of een afbeelding wilt toevoegen, moet deze na H1 komen.</span><span class="sxs-lookup"><span data-stu-id="ecac2-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="ecac2-107">Het volgende is niet toegestaan:</span><span class="sxs-lookup"><span data-stu-id="ecac2-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="ecac2-108">Doe dit in plaats daarvan:</span><span class="sxs-lookup"><span data-stu-id="ecac2-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="ecac2-109">Een andere veelvoorkomende oorzaak van dit probleem is [byte order marks (BOM's)](http://www.websina.com/bugzero/kb/unicode-bom.html) vóór de YAML-header.</span><span class="sxs-lookup"><span data-stu-id="ecac2-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="ecac2-110">Deze worden soms geïntroduceerd door coderingsproblemen bij het doorvoeren van inhoud naar opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="ecac2-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="ecac2-111">Ze veroorzaken een ongeldige rendering in GitHub en moeten worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="ecac2-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="ecac2-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="ecac2-112">Resolution</span></span>

<span data-ttu-id="ecac2-113">Verwijder andere inhoud dan de header van de YAML-metagegevens voor de H1.</span><span class="sxs-lookup"><span data-stu-id="ecac2-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
