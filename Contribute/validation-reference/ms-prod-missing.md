---
title: ms-prod-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713218"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="f6f32-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="f6f32-103">ms-prod-missing</span></span>

<span data-ttu-id="f6f32-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="f6f32-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f6f32-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="f6f32-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="f6f32-106">Gebruik `ms.prod` om on-premises producten op te geven.</span><span class="sxs-lookup"><span data-stu-id="f6f32-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="f6f32-107">Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven, maar als u `ms.technology` opgeeft, moet u ook `ms.prod` opgeven.</span><span class="sxs-lookup"><span data-stu-id="f6f32-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="f6f32-108">De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="f6f32-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="f6f32-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="f6f32-109">Resolution</span></span>

<span data-ttu-id="f6f32-110">Controleer of de waarde voor `ms.technology` die u hebt opgegeven, juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="f6f32-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="f6f32-111">Voeg vervolgens de juiste waarde voor `ms.prod` toe die als geldige bovenliggende waarde voor de `ms.technology` kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f6f32-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="f6f32-112">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="f6f32-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
