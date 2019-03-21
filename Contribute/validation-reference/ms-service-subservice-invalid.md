---
title: ms-service-and-subservice-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987633"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="929c2-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="929c2-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="929c2-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="929c2-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="929c2-105">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="929c2-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="929c2-106">Gebruik `ms.service` om cloudservices op te geven.</span><span class="sxs-lookup"><span data-stu-id="929c2-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="929c2-107">Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven.</span><span class="sxs-lookup"><span data-stu-id="929c2-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="929c2-108">De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="929c2-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="929c2-109">Uw `ms.service` is ongeldig of de waarde voor `ms.subservice` is geen geldig paar met uw `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="929c2-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="929c2-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="929c2-110">Resolution</span></span>

<span data-ttu-id="929c2-111">Controleer of de waarde van uw `ms.service` juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="929c2-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="929c2-112">Kies vervolgens een geldige waarde voor `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="929c2-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="929c2-113">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="929c2-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
