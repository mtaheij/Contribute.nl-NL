---
title: h1-missing
description: Uitleg en oplossing voor Docs-buildprobleem h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 677127d09349445bb80778dfb501d7d4294ea46b
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848474"
---
# <a name="h1-missing"></a><span data-ttu-id="8f43e-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="8f43e-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="8f43e-104">Suggestie</span><span class="sxs-lookup"><span data-stu-id="8f43e-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="8f43e-105">H1 verwijst naar de eerste kop in een Markdown-bestand.</span><span class="sxs-lookup"><span data-stu-id="8f43e-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="8f43e-106">Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.</span><span class="sxs-lookup"><span data-stu-id="8f43e-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="8f43e-107">U maakt een H1 door een regel te beginnen met één hash (#), gevolgd door een spatie en de tekst van de kop.</span><span class="sxs-lookup"><span data-stu-id="8f43e-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="8f43e-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="8f43e-108">Resolution</span></span>

<span data-ttu-id="8f43e-109">Om dit probleem op te lossen, voegt u een H1 toe als de eerste inhoud na het blok met YML-metagegevens in uw bestand:</span><span class="sxs-lookup"><span data-stu-id="8f43e-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="8f43e-110">Deze regel geldt niet voor ingesloten bestanden.</span><span class="sxs-lookup"><span data-stu-id="8f43e-110">This rule does not apply to included files.</span></span> <span data-ttu-id="8f43e-111">Als er H1-waarschuwingen op ingesloten bestanden worden weergegeven, moet u waarschijnlijk uw ingesloten bestanden insluiten in een `includes`-map.</span><span class="sxs-lookup"><span data-stu-id="8f43e-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="8f43e-112">De `includes`-map kan zich op een willekeurig niveau in het bestandspad bevinden.</span><span class="sxs-lookup"><span data-stu-id="8f43e-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="8f43e-113">Op basis van het pad herkent Docs-build het bestand als een ingesloten bestand en worden H1-validaties niet uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8f43e-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]