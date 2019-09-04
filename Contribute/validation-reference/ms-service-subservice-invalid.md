---
title: ms-service-and-subservice-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236526"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="cc390-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="cc390-103">ms-service-and-subservice-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="cc390-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="cc390-104">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="cc390-105">Gebruik `ms.service` om cloudservices op te geven.</span><span class="sxs-lookup"><span data-stu-id="cc390-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="cc390-106">Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven.</span><span class="sxs-lookup"><span data-stu-id="cc390-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="cc390-107">De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="cc390-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="cc390-108">Uw `ms.service` is ongeldig of de waarde voor `ms.subservice` is geen geldig paar met uw `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="cc390-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="cc390-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="cc390-109">Resolution</span></span>

<span data-ttu-id="cc390-110">Controleer of de waarde van uw `ms.service` juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="cc390-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="cc390-111">Kies vervolgens een geldige waarde voor `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="cc390-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="cc390-112">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="cc390-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="cc390-113">Als u nieuwe waarden wilt aanvragen, volgt u [dit proces](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="cc390-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
