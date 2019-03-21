---
title: ms-prod-or-service-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987555"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="94934-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="94934-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="94934-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="94934-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="94934-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="94934-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="94934-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="94934-106">Resolution</span></span>

<span data-ttu-id="94934-107">`ms.prod` of `ms.service` is vereist. Ze kunnen niet tegelijk aanwezig zijn: `ms.prod` wordt gebruikt voor on-premises producten, `ms.service` voor cloudservices.</span><span class="sxs-lookup"><span data-stu-id="94934-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="94934-108">Bepaal wat van toepassing is voor uw artikel, controleer of de waarde correct is en verwijder het andere veld.</span><span class="sxs-lookup"><span data-stu-id="94934-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="94934-109">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="94934-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]