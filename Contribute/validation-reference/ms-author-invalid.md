---
title: ms-author-invalid
description: Uitleg en oplossing voor Docs-buildprobleem ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246290"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="c33c4-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="c33c4-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="c33c4-104">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="c33c4-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="c33c4-105">Oplossing</span><span class="sxs-lookup"><span data-stu-id="c33c4-105">Resolution</span></span>

<span data-ttu-id="c33c4-106">Werk de `ms.author`-waarde bij met een geldige Microsoft-alias van de huidige auteur.</span><span class="sxs-lookup"><span data-stu-id="c33c4-106">Update the `ms.author` value with the current author's valid Microsoft alias.</span></span> <span data-ttu-id="c33c4-107">We adviseren dat de aangewezen auteur een voltijds werknemer of teamdistributielijst (DL) is in plaats van een leverancier voor de korte termijn.</span><span class="sxs-lookup"><span data-stu-id="c33c4-107">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="c33c4-108">Als de alias een distributielijst is, moet deze ook in de toegestane lijst voor `ms.author` worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c33c4-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="c33c4-109">U vindt geldige waarden voor `ms.author`-DL's op [deze interne Microsoft-site](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="c33c4-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
