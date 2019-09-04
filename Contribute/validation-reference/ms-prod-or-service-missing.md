---
title: ms-prod-or-service-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 93351fa343603a0b9d60e4b3e3ae41ce90d9912e
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236259"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="b184a-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="b184a-103">ms-prod-or-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="b184a-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="b184a-104">Warning</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="b184a-105">Oplossing</span><span class="sxs-lookup"><span data-stu-id="b184a-105">Resolution</span></span>

<span data-ttu-id="b184a-106">`ms.prod` of `ms.service` is vereist. Ze kunnen niet tegelijk aanwezig zijn: `ms.prod` wordt gebruikt voor on-premises producten, `ms.service` voor cloudservices.</span><span class="sxs-lookup"><span data-stu-id="b184a-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="b184a-107">Bepaal wat van toepassing is voor uw artikel, controleer of de waarde correct is en verwijder het andere veld.</span><span class="sxs-lookup"><span data-stu-id="b184a-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="b184a-108">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b184a-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="b184a-109">Als u nieuwe waarden wilt aanvragen, volgt u [dit proces](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="b184a-109">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
