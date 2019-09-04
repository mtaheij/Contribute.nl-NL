---
title: ms-prod-and-technology-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236335"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="fdeda-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="fdeda-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="fdeda-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="fdeda-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="fdeda-105">Gebruik `ms.prod` om on-premises producten op te geven.</span><span class="sxs-lookup"><span data-stu-id="fdeda-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="fdeda-106">Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven.</span><span class="sxs-lookup"><span data-stu-id="fdeda-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="fdeda-107">De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="fdeda-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="fdeda-108">Uw `ms.prod` is ongeldig of de waarde voor `ms.technology` is geen geldig paar met uw `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="fdeda-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="fdeda-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="fdeda-109">Resolution</span></span>

<span data-ttu-id="fdeda-110">Controleer of de waarde van uw `ms.prod` juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="fdeda-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="fdeda-111">Kies vervolgens een geldige waarde voor `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="fdeda-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="fdeda-112">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="fdeda-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="fdeda-113">Als u nieuwe waarden wilt aanvragen, volgt u [dit proces](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="fdeda-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
