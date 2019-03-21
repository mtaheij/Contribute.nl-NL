---
title: ms-prod-and-technology-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987578"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="72383-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="72383-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="72383-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="72383-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="72383-105">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="72383-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="72383-106">Gebruik `ms.prod` om on-premises producten op te geven.</span><span class="sxs-lookup"><span data-stu-id="72383-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="72383-107">Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven.</span><span class="sxs-lookup"><span data-stu-id="72383-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="72383-108">De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="72383-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="72383-109">Uw `ms.prod` is ongeldig of de waarde voor `ms.technology` is geen geldig paar met uw `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="72383-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="72383-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="72383-110">Resolution</span></span>

<span data-ttu-id="72383-111">Controleer of de waarde van uw `ms.prod` juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="72383-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="72383-112">Kies vervolgens een geldige waarde voor `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="72383-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="72383-113">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="72383-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
