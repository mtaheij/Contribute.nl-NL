---
title: ms-service-missing
description: Uitleg en oplossing voor Docs-buildprobleem ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713080"
---
# <a name="ms-service-missing"></a><span data-ttu-id="79201-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="79201-103">ms-service-missing</span></span>

<span data-ttu-id="79201-104">**Binnenkort beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="79201-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="79201-105">Suggestie</span><span class="sxs-lookup"><span data-stu-id="79201-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="79201-106">Gebruik `ms.service` om cloudservices op te geven.</span><span class="sxs-lookup"><span data-stu-id="79201-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="79201-107">Geef optioneel `ms.subservice` op om gedetailleerdere informatie over `ms.service` op te geven, maar als u `ms.subservice` opgeeft, moet u ook `ms.service` opgeven.</span><span class="sxs-lookup"><span data-stu-id="79201-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="79201-108">De waarden voor `ms.service` en `ms.subservice` moeten een geldig paar zijn.</span><span class="sxs-lookup"><span data-stu-id="79201-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="79201-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="79201-109">Resolution</span></span>

<span data-ttu-id="79201-110">Controleer of de waarde voor `ms.subservice` die u hebt opgegeven, juist is voor uw artikel.</span><span class="sxs-lookup"><span data-stu-id="79201-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="79201-111">Voeg vervolgens de juiste waarde voor `ms.service` toe die als geldige bovenliggende waarde voor de `ms.subservice` kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="79201-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="79201-112">U vindt geldige waarden op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="79201-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
