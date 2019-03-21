---
title: ms-prod-and-service
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b685144e92485df2dddb9bdda09fea47d75f588f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987670"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="03f84-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="03f84-103">ms-prod-and-service</span></span>

<span data-ttu-id="03f84-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="03f84-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="03f84-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="03f84-105">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="03f84-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="03f84-106">Resolution</span></span>

<span data-ttu-id="03f84-107">`ms.prod` of `ms.service` is vereist. Ze kunnen niet tegelijk aanwezig zijn: `ms.prod` wordt gebruikt voor on-premises producten, `ms.service` voor cloudservices.</span><span class="sxs-lookup"><span data-stu-id="03f84-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="03f84-108">Bepaal wat van toepassing is voor uw artikel, controleer of de waarde correct is en verwijder het andere veld.</span><span class="sxs-lookup"><span data-stu-id="03f84-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="03f84-109">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="03f84-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
