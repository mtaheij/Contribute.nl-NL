---
title: ms-prod-and-technology-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713264"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="403fa-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="403fa-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="403fa-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="403fa-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="403fa-105">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="403fa-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="403fa-106">Gebruik `ms.prod` om on-premises producten op te geven.</span><span class="sxs-lookup"><span data-stu-id="403fa-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="403fa-107">Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven.</span><span class="sxs-lookup"><span data-stu-id="403fa-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="403fa-108">De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="403fa-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="403fa-109">Uw `ms.prod` is ongeldig of de waarde voor `ms.technology` is geen geldig paar met uw `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="403fa-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="403fa-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="403fa-110">Resolution</span></span>

<span data-ttu-id="403fa-111">Controleer of de waarde van uw `ms.prod` juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="403fa-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="403fa-112">Kies vervolgens een geldige waarde voor `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="403fa-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="403fa-113">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="403fa-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
