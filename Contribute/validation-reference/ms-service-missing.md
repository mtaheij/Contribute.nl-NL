---
title: ms-service-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236493"
---
# <a name="ms-service-missing"></a><span data-ttu-id="2cd7a-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="2cd7a-103">ms-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="2cd7a-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="2cd7a-104">Warning</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="2cd7a-105">Gebruik `ms.service` om cloudservices op te geven.</span><span class="sxs-lookup"><span data-stu-id="2cd7a-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="2cd7a-106">Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven, maar als u `ms.subservice` opgeeft, moet u ook `ms.service` opgeven.</span><span class="sxs-lookup"><span data-stu-id="2cd7a-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="2cd7a-107">De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="2cd7a-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="2cd7a-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="2cd7a-108">Resolution</span></span>

<span data-ttu-id="2cd7a-109">Controleer of de waarde voor `ms.subservice` die u hebt opgegeven, juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="2cd7a-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="2cd7a-110">Voeg vervolgens de juiste waarde voor `ms.service` toe die als geldige bovenliggende waarde voor de `ms.subservice` kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2cd7a-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="2cd7a-111">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="2cd7a-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="2cd7a-112">Als u nieuwe waarden wilt aanvragen, volgt u [dit proces](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="2cd7a-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
