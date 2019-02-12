---
title: ms-service-and-subservice-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713126"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="6925c-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="6925c-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="6925c-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="6925c-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="6925c-105">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="6925c-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="6925c-106">Gebruik `ms.service` om cloudservices op te geven.</span><span class="sxs-lookup"><span data-stu-id="6925c-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="6925c-107">Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven.</span><span class="sxs-lookup"><span data-stu-id="6925c-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="6925c-108">De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="6925c-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="6925c-109">Uw `ms.service` is ongeldig of de waarde voor `ms.subservice` is geen geldig paar met uw `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="6925c-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="6925c-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="6925c-110">Resolution</span></span>

<span data-ttu-id="6925c-111">Controleer of de waarde van uw `ms.service` juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="6925c-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="6925c-112">Kies vervolgens een geldige waarde voor `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="6925c-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="6925c-113">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="6925c-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
