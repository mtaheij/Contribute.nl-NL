---
title: ms-prod-service-mismatch
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713172"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="45b5f-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="45b5f-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="45b5f-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="45b5f-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="45b5f-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="45b5f-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="45b5f-106">Gebruik `ms.prod` om on-premises producten op te geven, `ms.service` voor cloudservices.</span><span class="sxs-lookup"><span data-stu-id="45b5f-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="45b5f-107">Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven.</span><span class="sxs-lookup"><span data-stu-id="45b5f-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="45b5f-108">Geef `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven.</span><span class="sxs-lookup"><span data-stu-id="45b5f-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="45b5f-109">U kunt `ms.prod` niet gebruiken met `ms.subservice` of `ms.service` niet met `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="45b5f-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="45b5f-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="45b5f-110">Resolution</span></span>

<span data-ttu-id="45b5f-111">Controleer eerst of u de juiste bovenliggende waarde (`ms.prod` of `ms.service`) voor uw artikel hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="45b5f-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="45b5f-112">Voeg vervolgens het juiste onderliggende veld toe met een geldige gepaarde waarde.</span><span class="sxs-lookup"><span data-stu-id="45b5f-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="45b5f-113">Verwijder eventuele extra velden.</span><span class="sxs-lookup"><span data-stu-id="45b5f-113">Remove any extra fields.</span></span>

<span data-ttu-id="45b5f-114">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="45b5f-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
