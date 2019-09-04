---
title: ms-prod-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236295"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="61d74-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="61d74-103">ms-prod-missing</span></span>

## <a name="warning"></a><span data-ttu-id="61d74-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="61d74-104">Warning</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="61d74-105">Gebruik `ms.prod` om on-premises producten op te geven.</span><span class="sxs-lookup"><span data-stu-id="61d74-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="61d74-106">Geef optioneel `ms.technology` op om gedetailleerdere informatie over `ms.prod` op te geven, maar als u `ms.technology` opgeeft, moet u ook `ms.prod` opgeven.</span><span class="sxs-lookup"><span data-stu-id="61d74-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="61d74-107">De waarden voor `ms.prod` en `ms.technology` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="61d74-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="61d74-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="61d74-108">Resolution</span></span>

<span data-ttu-id="61d74-109">Controleer of de waarde voor `ms.technology` die u hebt opgegeven, juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="61d74-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="61d74-110">Voeg vervolgens de juiste waarde voor `ms.prod` toe die als geldige bovenliggende waarde voor de `ms.technology` kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="61d74-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="61d74-111">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="61d74-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="61d74-112">Als u nieuwe waarden wilt aanvragen, volgt u [dit proces](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="61d74-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
