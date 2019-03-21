---
title: ms-service-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987716"
---
# <a name="ms-service-missing"></a><span data-ttu-id="60cc0-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="60cc0-103">ms-service-missing</span></span>

<span data-ttu-id="60cc0-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="60cc0-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="60cc0-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="60cc0-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="60cc0-106">Gebruik `ms.service` om cloudservices op te geven.</span><span class="sxs-lookup"><span data-stu-id="60cc0-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="60cc0-107">Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven, maar als u `ms.subservice` opgeeft, moet u ook `ms.service` opgeven.</span><span class="sxs-lookup"><span data-stu-id="60cc0-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="60cc0-108">De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="60cc0-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="60cc0-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="60cc0-109">Resolution</span></span>

<span data-ttu-id="60cc0-110">Controleer of de waarde voor `ms.subservice` die u hebt opgegeven, juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="60cc0-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="60cc0-111">Voeg vervolgens de juiste waarde voor `ms.service` toe die als geldige bovenliggende waarde voor de `ms.subservice` kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="60cc0-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="60cc0-112">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="60cc0-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
