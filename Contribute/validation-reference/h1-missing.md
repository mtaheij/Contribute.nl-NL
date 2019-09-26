---
title: h1-missing
description: Uitleg en oplossing voor Docs-buildprobleem h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 2d0b766bba5b5ba32bff68f7ac185ab639fc7557
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247416"
---
# <a name="h1-missing"></a><span data-ttu-id="66353-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="66353-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="66353-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="66353-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="66353-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="66353-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="66353-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="66353-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="66353-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="66353-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="66353-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="66353-108">Resolution</span></span>

<span data-ttu-id="66353-109">Om dit probleem op te lossen, voegt u een H1 toe als de eerste inhoud na het blok met YML-metagegevens in uw bestand:</span><span class="sxs-lookup"><span data-stu-id="66353-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="66353-110">Deze regel geldt niet voor ingesloten bestanden.</span><span class="sxs-lookup"><span data-stu-id="66353-110">This rule does not apply to included files.</span></span> <span data-ttu-id="66353-111">Als er H1-resultaten in ingesloten bestanden worden weergegeven, moet u waarschijnlijk uw ingesloten bestanden insluiten in een `includes`-map.</span><span class="sxs-lookup"><span data-stu-id="66353-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="66353-112">De `includes`-map kan zich op een willekeurig niveau in het bestandspad bevinden.</span><span class="sxs-lookup"><span data-stu-id="66353-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="66353-113">Op basis van het pad herkent Docs-build het bestand als een ingesloten bestand en worden H1-validaties niet uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="66353-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="66353-114">Een veelvoorkomende oorzaak van ontbrekende H1's is fout gebruik van de ingesloten bestanden: de H1 bevindt zich in het ingesloten bestand, maar niet in het bovenliggende bestand.</span><span class="sxs-lookup"><span data-stu-id="66353-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="66353-115">Dit is niet toegestaan, omdat het gebruik van een H1 in een ingesloten bestand betekent dat er in bovenliggende bestanden dubbele H1's zijn, of dat het ingesloten bestand maar één keer wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="66353-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="66353-116">H1's moeten binnen een inhoudsset uniek zijn en ingesloten bestanden moeten alleen worden gebruikt om inhoud te delen tussen meerdere bestanden.</span><span class="sxs-lookup"><span data-stu-id="66353-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="66353-117">Als er `h1-missing`-resultaten worden weergegeven, omdat de H1 zich in een ingesloten bestand bevindt, is de oplossing om de H1 te verplaatsen naar het bovenliggende bestand, evenals alle ingesloten inhoud als het ingesloten bestand maar één keer wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="66353-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="66353-118">Raadpleeg het interne Microsoft-artikel [Herbruikbare inhoud in artikelen insluiten](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master) voor meer informatie over ingesloten bestanden in Docs.</span><span class="sxs-lookup"><span data-stu-id="66353-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
